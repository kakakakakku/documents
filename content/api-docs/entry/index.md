---
Title: Mackerel API Documents (v0)
Date: 2016-02-12T19:23:55+09:00
URL: https://mackerel.io/api-docs/entry/index
EditURL: https://blog.hatena.ne.jp/mackerelio/mackerelio-api.hatenablog.mackerel.io/atom/entry/6653586347157001366
---

<div id="api-documents-entry">

<div class="hatena-module-search-box">
  <form class="search-form" role="search" action="https://mackerel.io/api-docs/search" method="get">
    <input type="text" name="q" class="search-module-input" value="" placeholder="Search this API documents" required="">
    <input type="submit" value="検索" class="search-module-button">
  </form>
</div>

<div id="api-summary">
  <h2 id="summary">Summary</h2>
  <ul>
    <li>The base URL is <code>https://api.mackerelio.com/</code>. (<code>https://kcps-mackerel.io</code> for KCPS users) </li>
    <li>POST/PUT input and the success response should be in JSON (<code>application/json</code>). </li>
    <li>Please specify JSON that is valid against RFC. </li>
    <li><b><code>X-Api-Key</code> header (required): the API key of the organization to which targeted hosts and services belong.</b>
      <ul>
        <li>You can see your API keys in the <a href="https://mackerel.io/my?tab=apikeys">Dashboard</a>.</li>
        <li>Each API key's Read and Write permissions can be configured.
          <ul>
            <li>API keys that only have Read permission cannot be used for APIs that require Write permission.</li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</div>

<div class="index-rows">
  
  <h2>Contents</h2>
  <div class="index-row">
    <h3><a href="entry/services">Services</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/services#list">
          <p>List of Services</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/services#create">
          <p>Register Services</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/services</code>
          </p>
        </a>
      </div>      
      <div class="api">
        <a href="entry/services#delete">
          <p>Delete Services</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/services#rolelist">
          <p>List of Roles</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/services#rolecreate">
          <p>Register roles</p>
          <p class="type-post">
              <code>POST</code>
              <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/services#roledelete">
          <p>Delete roles</p>
          <p class="type-delete">
              <code>DELETE</code>
              <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles/<em>&lt;roleName&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/services#metric-names">
          <p>List of metric names</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metric-names</code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/hosts">Hosts</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/hosts#create">
          <p>Registering host information</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/hosts</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#get">
          <p>Getting host information</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#update-information">
          <p>Updating host information</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#update-status">
          <p>Updating host status</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/status</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#update-roles">
          <p>Updating host roles</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/role-fullnames</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#retire">
          <p>Retiring hosts</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/retire</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#list">
          <p>List of hosts</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/hosts</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/hosts#metric-names">
          <p>List of metric names</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/metric-names</code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/host-metrics">Host Metrics</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/host-metrics#post">
          <p>Posting metrics</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/tsdb</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/host-metrics#get">
          <p>Getting host metrics</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/metrics</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/host-metrics#get-latest">
        <p>Getting latest metrics</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/tsdb/latest</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/host-metrics#post-graphdef">
          <p>Posting graph definitions</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/graph-defs/create</code>
          </p>
        </a>
      </div>
    </div>
  </div>
  
  <div class="index-row">
    <h3><a href="entry/service-metrics">Service metric</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/service-metrics#post">
          <p>Posting service metrics</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/tsdb</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/service-metrics#get">
        <p>Getting service metrics</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metrics</code>
          </p>
        </a>
      </div>
    </div>
  </div>
  
  <div class="index-row">
    <h3><a href="entry/check-monitoring">Check monitoring</a></h3>
    <div class="apis">  
      <div class="api">
        <a href="entry/check-monitoring#post">
          <p>Posting monitoring check reports</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/monitoring/checks/report</code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/metadata">Metadata</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/metadata#get">
          <p>Get host metadata</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#hostput">
          <p>Create / Update host metadata</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#hostdelete">
          <p>Delete host metadata</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#hostlist">
          <p>List host metadata</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/hosts/<em>&lt;hostId&gt;</em>/metadata</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#serviceget">
          <p>Get service metadata</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#serviceput">
          <p>Register / Update service metadata</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#servicedelete">
          <p>Delete service metadata</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#servicelist">
          <p>List of service metadata</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/metadata</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#roleget">
          <p>Get role metadata</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles/<em>&lt;roleName&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#roleput">
          <p>Register / Update role metadata</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles/<em>&lt;roleName&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#roledelete">
          <p>Delete role metadata</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles/<em>&lt;roleName&gt;</em>/metadata/<em>&lt;namespace&gt</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/metadata#rolelist">
          <p>List of role metadata</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/services/<em>&lt;serviceName&gt;</em>/roles/<em>&lt;roleName&gt;</em>/metadata</code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/monitors">Monitors</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/monitors#create">
          <p>Register monitor configurations</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/monitors</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/monitors#list">
          <p>List of monitor configurations</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/monitors</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/monitors#get">
          <p>Get monitor configurations</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/monitors/<em>&lt;monitorId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/monitors#update">
          <p>Update monitor configurations</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/monitors/<em>&lt;monitorId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/monitors#delete">
          <p>Delete monitor configurations</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/monitors/<em>&lt;monitorId&gt;</em></code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/channels">Notification channels</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/channels#get">
          <p>Get notification channel list</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/channels</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/channels#create">
          <p>Register notification channels</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/channels</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/channels#delete">
          <p>Delete notification channels</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/channels/<em>&lt;channelId&gt;</em></code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/notification-groups">Notification groups</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/notification-groups#create">
          <p>Register notification groups</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/notification-groups</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/notification-groups#get">
          <p>Get notification group list</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/notification-groups</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/notification-groups#update">
          <p>Update notification groups</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/notification-groups/<em>&lt;notificationGroupId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/notification-groups#delete">
          <p>Delete notification groups</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/notification-groups/<em>&lt;notificationGroupId&gt;</em></code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/alerts">Alerts</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/alerts#get">
          <p>Getting Alerts</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/alerts</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/alerts#close">
          <p>Closing Alerts</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/alerts/<em>&lt;alertId&gt;</em>/close</code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/dashboards">Dashboards</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/dashboards#create">
          <p>Creating Dashboards</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/dashboards</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/dashboards#get">
          <p>Getting Dashboards</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/dashboards/<em>&lt;dashboardId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/dashboards#update">
          <p>Updating Dashboards</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/dashboards/<em>&lt;dashboardId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/dashboards#delete">
          <p>Deleting Dashboards</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/dashboards/<em>&lt;dashboardId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/dashboards#list">
          <p>List of Dashboards</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/dashboards</code>
          </p>
        </a>
      </div>
    </div>
  </div>

  <div class="index-row">
    <h3><a href="entry/graph-annotations">Graph annotations</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/graph-annotations#create">
          <p>Creating graph annotations</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/graph-annotations</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/graph-annotations#get">
          <p>Obtaining graph annotations</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/graph-annotations</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/graph-annotations#update">
          <p>Updating graph annotations</p>
          <p class="type-put">
            <code>PUT</code>
            <code>/api/v0/graph-annotations/<em>&lt;annotationId&gt;</em></code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/graph-annotations#delete">
          <p>Deleting graph annotations</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/graph-annotations/<em>&lt;annotationId&gt;</em></code>
          </p>
        </a>
      </div>
    </div>
  </div>


  <div class="index-row">
    <h3><a href="entry/users">Users</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/users#list">
          <p>List of users</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/users</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/users#delete">
          <p>Delete users</p>
          <p class="type-delete">
            <code>DELETE</code>
            <code>/api/v0/users/<em>&lt;userId&gt;</em></code>
          </p>
        </a>
      </div>
    </div>
  </div>
  
  <div class="index-row">
    <h3><a href="entry/invitations">Invitations</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/invitations#list">
          <p>List of invitations</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/invitations</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/invitations#create">
          <p>Creating an invitation</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/invitations</code>
          </p>
        </a>
      </div>
      <div class="api">
        <a href="entry/invitations#revoke">
          <p>Cancelling an invitation</p>
          <p class="type-post">
            <code>POST</code>
            <code>/api/v0/invitations/revoke</code>
          </p>
        </a>
      </div>
    </div>
  </div>
 

  <div class="index-row">
    <h3><a href="entry/organizations">Organization</a></h3>
    <div class="apis">
      <div class="api">
        <a href="entry/organizations#get">
          <p>Get organization information</p>
          <p class="type-get">
            <code>GET</code>
            <code>/api/v0/org</code>
          </p>
        </a>
      </div>
    </div>
  </div>

</div>

<h2 id="data-types">Data types</h2>
<ul>
  <li>Host ID <code><em>&lt;hostId&gt;</em></code>
    <ul>
      <li>This is a string that is provided by Mackerel when a host is registered. It is used to distinguish and identify each unique host the agent is running on.</li>
    </ul>
  </li>
  <li>Service name <code><em>&lt;serviceName&gt;</em></code>
    <ul>
      <li>This is the name of a service registered with Mackerel.</li>
    </ul>
  </li>
</ul>

</div>

<div id="contact-human">
  <p id="human-image"><img src="/assets/images/blog/support.png" alt="" /></p>
  <h4>Need even more help?</h4>
  <p id="contact-human-info">Send us an email at support@mackerel.io. We'll get back to you right away.</p> 
  <p id="contact-human-button"><a href="mailto:support@mackerel.io" class="ui-button button-blue">Email Us</a></p>
</div>
<div id="about-container">
  <h4 id="about"><span>About</span></h4>
  <p>This is the page containing Mackerel's <https://mackerel.io> instructional documents.</p>
</div>
