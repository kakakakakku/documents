---
Title: サービスメトリック
Date: 2016-03-22T10:33:51+09:00
URL: https://mackerel.io/ja/api-docs/entry/service-metrics
EditURL: https://blog.hatena.ne.jp/mackerelio/mackerelio-api-jp.hatenablog.mackerel.io/atom/entry/10328537792368064365
---

<ul class="internal-nav">
  <li><a href="#post">サービスメトリックの投稿</a></li>
  <li><a href="#get">サービスメトリックの値の取得</a></li>
</ul>

<h2 id="post">サービスメトリックの投稿</h2>

サービスに紐づくメトリック（計測値）を Mackerel に送信します。

<p class="type-post">
  <code>POST</code>
  <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/tsdb</code>
</p>

APIに対して過去の値を送信した場合、Mackerel上の値は上書きされます。24時間以上前の古いタイムスタンプで投稿した場合は、そのメトリックは記録されません（ステータスコード 200 でレスポンスを返します）。また、アラートの発生はMackerel上の最新の値に基づいて行われるため、そのデータが最新の値ではない場合には、閾値を超えていたとしてもアラートは発生しません。

### APIキーに必要な権限

<ul class="api-key">
  <li class="label-read">Read</li>
  <li class="label-write">Write</li>
</ul>

### 入力

```json
[ <metricValue>, <metricValue>, … ]
```

<i>`<metricValue>`</i>: 以下のキーをもつオブジェクトです。

| KEY     | TYPE   | DESCRIPTION |
| -------- | ------ | ----------- |
| `name`   | *string* | メトリック名（`[a-zA-Z0-9._-]+`） |
| `time`   | *number* | エポック秒。 |
| `value`  | *number* | `time` 時点での計測値。 |

### 応答

#### 成功時

```json
{
  "success": true
}
```

#### 失敗時

<table class="default api-error-table">
  <thead>
    <tr>
      <th class="status-code">STATUS CODE</th>
      <th class="description">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>403</td>
      <td>APIキーに書き込み権限がないとき / <a href="https://mackerel.io/ja/docs/entry/faq/organization/ip-restriction" target="_blank">許可されたIPアドレス範囲</a>外からのアクセスの場合</td>
    </tr>
    <tr>
      <td>429</td>
      <td>分間のリクエスト数が過剰のとき。投稿頻度を1分間隔にする、複数のメトリックをまとめて投稿するなどの修正をお願いします。</td>
    </tr>
    <tr>
      <td>200以外</td>
      <td>上記以外のエラー</td>
    </tr>
  </tbody>
</table>

----------------------------------------------

<h2 id="get">サービスメトリックの値の取得</h2>

サービスに紐づくメトリックの値を取得できます。

<p class="type-get">
  <code>GET</code>
  <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metrics</code>
</p>

### APIキーに必要な権限

<ul class="api-key">
  <li class="label-read">Read</li>
</ul>

### 入力（クエリパラメータ）

次のパラメータでメトリック名と取得する期間を指定します。

| KEY     | TYPE     | DESCRIPTION |
| ------- | -------- | ----------- |
| `name`  | *string* | メトリック名。 |
| `from`  | *number* | メトリックを取得したい期間の最初 (epoch秒) |
| `to`    | *number* | メトリックを取得したい期間の最後 (epoch秒) |

### 応答

#### 成功時

```json
{
  "metrics": [
    {
      "time": <time>,
      "value": <value>
    },
    {
      "time": <time>,
      "value": <value>
    },
    …
  ]
}
```

- 並び順は、時刻が古い順です
- メトリックの時刻を表す <i>`<time>`</i> はエポック秒です

#### 失敗時

<table class="default api-error-table">
  <thead>
    <tr>
      <th class="status-code">STATUS CODE</th>
      <th class="description">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>404</td>
      <td>サービスまたはメトリックが存在しない時</td>
    </tr>
    <tr>
      <td>200以外</td>
      <td>上記以外のエラー</td>
    </tr>
  </tbody>
</table>
