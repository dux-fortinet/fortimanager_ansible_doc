:source: fmgr_wanprof_system_virtualwanlink.py

:orphan:

.. _fmgr_wanprof_system_virtualwanlink:

fmgr_wanprof_system_virtualwanlink -- Configure redundant internet connections using SD-WAN (formerly virtual WAN link).
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.0.0

.. warning::
   Starting in version 3.0.0, all input arguments will be named using the underscore naming convention (snake_case).
  
   - Argument name before 3.0.0: ``var-name``, ``var name``, ``var.name``
   - New argument name starting in 3.0.0: ``var_name``
  
   FortiManager Ansible v2.4+ supports both previous argument name and new underscore name.
   You will receive deprecation warnings if you keep using the previous argument name.
   You can ignore the warning by setting deprecation_warnings=False in ansible.cfg.

.. contents::
   :local:
   :depth: 1


Synopsis
--------

- This module is able to configure a FortiManager device.
- Examples include all parameters and values need to be adjusted to data sources before usage.
- Tested with FortiManager v7.x.


Requirements
------------
The below requirements are needed on the host that executes this module.

- ansible>=2.15.0


FortiManager Version Compatibility
----------------------------------
.. raw:: html

 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>



Parameters
----------
.. raw:: html

 <ul>
 <li><span class="li-head">access_token</span> -The token to access FortiManager without using username and password. <span class="li-normal">type: str</span> <span class="li-required">required: false</span></li> <li><span class="li-head">bypass_validation</span> - Only set to True when module schema diffs with FortiManager API structure, module continues to execute without validating parameters. <span class="li-normal">type: bool</span> <span class="li-required">required: false</span> <span class="li-normal"> default: False</span> </li>
 <li><span class="li-head">enable_log</span> - Enable/Disable logging for task. <span class="li-normal">type: bool</span> <span class="li-required">required: false</span> <span class="li-normal"> default: False</span> </li>
 <li><span class="li-head">forticloud_access_token</span> - Access token of forticloud managed API users, this option is available with FortiManager later than 6.4.0. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> </li>
 <li><span class="li-head">proposed_method</span> - The overridden method for the underlying Json RPC request. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> <span class="li-normal"> choices: set, update, add</span> </li>
 <li><span class="li-head">rc_succeeded</span> - The rc codes list with which the conditions to succeed will be overriden. <span class="li-normal">type: list</span> <span class="li-required">required: false</span> </li>
 <li><span class="li-head">rc_failed</span> - The rc codes list with which the conditions to fail will be overriden. <span class="li-normal">type: list</span> <span class="li-required">required: false</span> </li>
 <li><span class="li-head">workspace_locking_adom</span> - Acquire the workspace lock if FortiManager is running in workspace mode. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> <span class="li-normal"> choices: global, custom adom including root</span> </li>
 <li><span class="li-head">workspace_locking_timeout</span> - The maximum time in seconds to wait for other users to release workspace lock. <span class="li-normal">type: integer</span> <span class="li-required">required: false</span>  <span class="li-normal">default: 300</span> </li>
 <li><span class="li-head">adom</span> - The parameter in requested url <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
 <li><span class="li-head">wanprof</span> - The parameter in requested url <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
 <li><span class="li-head">wanprof_system_virtualwanlink</span> - Configure redundant internet connections using SD-WAN <span class="li-normal">type: dict</span></li>
 <ul class="ul-self">
 <li><span class="li-head">fail_detect</span> <b>(Alias name: fail-detect)</b>  Enable/disable sd-wan internet connection status checking (failure detection). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label0' href="javascript:ContentClick('label1', 'label0');" onmouseover="ContentPreview('label1');" onmouseout="ContentUnpreview('label1');" title="click to collapse or expand..."> more... </a>
 <div id="label1" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">health_check</span> <b>(Alias name: health-check)</b>  Health check. <span class="li-normal">type: list</span>
 <a id='label2' href="javascript:ContentClick('label3', 'label2');" onmouseover="ContentPreview('label3');" onmouseout="ContentUnpreview('label3');" title="click to collapse or expand..."> more... </a>
 <div id="label3" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">_dynamic_server</span> <b>(Alias name: _dynamic-server)</b>  Dynamic server. <span class="li-normal">type: str</span>
 <a id='label4' href="javascript:ContentClick('label5', 'label4');" onmouseover="ContentPreview('label5');" onmouseout="ContentUnpreview('label5');" title="click to collapse or expand..."> more... </a>
 <div id="label5" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v6.4.15</code></p>
 </div>
 </li>
 <li><span class="li-head">addr_mode</span> <b>(Alias name: addr-mode)</b>  Address mode (ipv4 or ipv6). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ipv4, ipv6]</span> 
 <a id='label6' href="javascript:ContentClick('label7', 'label6');" onmouseover="ContentPreview('label7');" onmouseout="ContentUnpreview('label7');" title="click to collapse or expand..."> more... </a>
 <div id="label7" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">failtime</span> Number of failures before server is considered lost (1 - 3600, default = 5). <span class="li-normal">type: int</span>
 <a id='label8' href="javascript:ContentClick('label9', 'label8');" onmouseover="ContentPreview('label9');" onmouseout="ContentUnpreview('label9');" title="click to collapse or expand..."> more... </a>
 <div id="label9" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">http_agent</span> <b>(Alias name: http-agent)</b>  String in the http-agent field in the http header. <span class="li-normal">type: str</span>
 <a id='label10' href="javascript:ContentClick('label11', 'label10');" onmouseover="ContentPreview('label11');" onmouseout="ContentUnpreview('label11');" title="click to collapse or expand..."> more... </a>
 <div id="label11" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">http_get</span> <b>(Alias name: http-get)</b>  Url used to communicate with the server if the protocol if the protocol is http. <span class="li-normal">type: str</span>
 <a id='label12' href="javascript:ContentClick('label13', 'label12');" onmouseover="ContentPreview('label13');" onmouseout="ContentUnpreview('label13');" title="click to collapse or expand..."> more... </a>
 <div id="label13" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">http_match</span> <b>(Alias name: http-match)</b>  Response string expected from the server if the protocol is http. <span class="li-normal">type: str</span>
 <a id='label14' href="javascript:ContentClick('label15', 'label14');" onmouseover="ContentPreview('label15');" onmouseout="ContentUnpreview('label15');" title="click to collapse or expand..."> more... </a>
 <div id="label15" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">interval</span> Status check interval, or the time between attempting to connect to the server (1 - 3600 sec, default = 5). <span class="li-normal">type: int</span>
 <a id='label16' href="javascript:ContentClick('label17', 'label16');" onmouseover="ContentPreview('label17');" onmouseout="ContentUnpreview('label17');" title="click to collapse or expand..."> more... </a>
 <div id="label17" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">members</span> Member sequence number list. <span class="li-normal">type: list or str</span>
 <a id='label18' href="javascript:ContentClick('label19', 'label18');" onmouseover="ContentPreview('label19');" onmouseout="ContentUnpreview('label19');" title="click to collapse or expand..."> more... </a>
 <div id="label19" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">name</span> Status check or health check name. <span class="li-normal">type: str</span>
 <a id='label20' href="javascript:ContentClick('label21', 'label20');" onmouseover="ContentPreview('label21');" onmouseout="ContentUnpreview('label21');" title="click to collapse or expand..."> more... </a>
 <div id="label21" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">packet_size</span> <b>(Alias name: packet-size)</b>  Packet size of a twamp test session, <span class="li-normal">type: int</span>
 <a id='label22' href="javascript:ContentClick('label23', 'label22');" onmouseover="ContentPreview('label23');" onmouseout="ContentUnpreview('label23');" title="click to collapse or expand..."> more... </a>
 <div id="label23" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">password</span> Twamp controller password in authentication mode <span class="li-normal">type: list</span>
 <a id='label24' href="javascript:ContentClick('label25', 'label24');" onmouseover="ContentPreview('label25');" onmouseout="ContentUnpreview('label25');" title="click to collapse or expand..."> more... </a>
 <div id="label25" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">port</span> Port number used to communicate with the server over the selected protocol. <span class="li-normal">type: int</span>
 <a id='label26' href="javascript:ContentClick('label27', 'label26');" onmouseover="ContentPreview('label27');" onmouseout="ContentUnpreview('label27');" title="click to collapse or expand..."> more... </a>
 <div id="label27" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">protocol</span> Protocol used to determine if the fortigate can communicate with the server. <span class="li-normal">type: str</span> <span class="li-normal">choices: [ping, tcp-echo, udp-echo, http, twamp, ping6, dns]</span> 
 <a id='label28' href="javascript:ContentClick('label29', 'label28');" onmouseover="ContentPreview('label29');" onmouseout="ContentUnpreview('label29');" title="click to collapse or expand..."> more... </a>
 <div id="label29" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">recoverytime</span> Number of successful responses received before server is considered recovered (1 - 3600, default = 5). <span class="li-normal">type: int</span>
 <a id='label30' href="javascript:ContentClick('label31', 'label30');" onmouseover="ContentPreview('label31');" onmouseout="ContentUnpreview('label31');" title="click to collapse or expand..."> more... </a>
 <div id="label31" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">security_mode</span> <b>(Alias name: security-mode)</b>  Twamp controller security mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, authentication]</span> 
 <a id='label32' href="javascript:ContentClick('label33', 'label32');" onmouseover="ContentPreview('label33');" onmouseout="ContentUnpreview('label33');" title="click to collapse or expand..."> more... </a>
 <div id="label33" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">server</span> Ip address or fqdn name of the server. <span class="li-normal">type: list</span>
 <a id='label34' href="javascript:ContentClick('label35', 'label34');" onmouseover="ContentPreview('label35');" onmouseout="ContentUnpreview('label35');" title="click to collapse or expand..."> more... </a>
 <div id="label35" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sla</span> Sla. <span class="li-normal">type: list</span>
 <a id='label36' href="javascript:ContentClick('label37', 'label36');" onmouseover="ContentPreview('label37');" onmouseout="ContentUnpreview('label37');" title="click to collapse or expand..."> more... </a>
 <div id="label37" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">id</span> Sla id. <span class="li-normal">type: int</span>
 <a id='label38' href="javascript:ContentClick('label39', 'label38');" onmouseover="ContentPreview('label39');" onmouseout="ContentUnpreview('label39');" title="click to collapse or expand..."> more... </a>
 <div id="label39" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">jitter_threshold</span> <b>(Alias name: jitter-threshold)</b>  Jitter for sla to make decision in milliseconds. <span class="li-normal">type: int</span>
 <a id='label40' href="javascript:ContentClick('label41', 'label40');" onmouseover="ContentPreview('label41');" onmouseout="ContentUnpreview('label41');" title="click to collapse or expand..."> more... </a>
 <div id="label41" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">latency_threshold</span> <b>(Alias name: latency-threshold)</b>  Latency for sla to make decision in milliseconds. <span class="li-normal">type: int</span>
 <a id='label42' href="javascript:ContentClick('label43', 'label42');" onmouseover="ContentPreview('label43');" onmouseout="ContentUnpreview('label43');" title="click to collapse or expand..."> more... </a>
 <div id="label43" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">link_cost_factor</span> <b>(Alias name: link-cost-factor)</b>  Criteria on which to base link selection. <span class="li-normal">type: list</span> <span class="li-normal">choices: [latency, jitter, packet-loss]</span> 
 <a id='label44' href="javascript:ContentClick('label45', 'label44');" onmouseover="ContentPreview('label45');" onmouseout="ContentUnpreview('label45');" title="click to collapse or expand..."> more... </a>
 <div id="label45" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">packetloss_threshold</span> <b>(Alias name: packetloss-threshold)</b>  Packet loss for sla to make decision in percentage. <span class="li-normal">type: int</span>
 <a id='label46' href="javascript:ContentClick('label47', 'label46');" onmouseover="ContentPreview('label47');" onmouseout="ContentUnpreview('label47');" title="click to collapse or expand..."> more... </a>
 <div id="label47" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">threshold_alert_jitter</span> <b>(Alias name: threshold-alert-jitter)</b>  Alert threshold for jitter (ms, default = 0). <span class="li-normal">type: int</span>
 <a id='label48' href="javascript:ContentClick('label49', 'label48');" onmouseover="ContentPreview('label49');" onmouseout="ContentUnpreview('label49');" title="click to collapse or expand..."> more... </a>
 <div id="label49" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">threshold_alert_latency</span> <b>(Alias name: threshold-alert-latency)</b>  Alert threshold for latency (ms, default = 0). <span class="li-normal">type: int</span>
 <a id='label50' href="javascript:ContentClick('label51', 'label50');" onmouseover="ContentPreview('label51');" onmouseout="ContentUnpreview('label51');" title="click to collapse or expand..."> more... </a>
 <div id="label51" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">threshold_alert_packetloss</span> <b>(Alias name: threshold-alert-packetloss)</b>  Alert threshold for packet loss (percentage, default = 0). <span class="li-normal">type: int</span>
 <a id='label52' href="javascript:ContentClick('label53', 'label52');" onmouseover="ContentPreview('label53');" onmouseout="ContentUnpreview('label53');" title="click to collapse or expand..."> more... </a>
 <div id="label53" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">threshold_warning_jitter</span> <b>(Alias name: threshold-warning-jitter)</b>  Warning threshold for jitter (ms, default = 0). <span class="li-normal">type: int</span>
 <a id='label54' href="javascript:ContentClick('label55', 'label54');" onmouseover="ContentPreview('label55');" onmouseout="ContentUnpreview('label55');" title="click to collapse or expand..."> more... </a>
 <div id="label55" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">threshold_warning_latency</span> <b>(Alias name: threshold-warning-latency)</b>  Warning threshold for latency (ms, default = 0). <span class="li-normal">type: int</span>
 <a id='label56' href="javascript:ContentClick('label57', 'label56');" onmouseover="ContentPreview('label57');" onmouseout="ContentUnpreview('label57');" title="click to collapse or expand..."> more... </a>
 <div id="label57" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">threshold_warning_packetloss</span> <b>(Alias name: threshold-warning-packetloss)</b>  Warning threshold for packet loss (percentage, default = 0). <span class="li-normal">type: int</span>
 <a id='label58' href="javascript:ContentClick('label59', 'label58');" onmouseover="ContentPreview('label59');" onmouseout="ContentUnpreview('label59');" title="click to collapse or expand..."> more... </a>
 <div id="label59" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">update_cascade_interface</span> <b>(Alias name: update-cascade-interface)</b>  Enable/disable update cascade interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label60' href="javascript:ContentClick('label61', 'label60');" onmouseover="ContentPreview('label61');" onmouseout="ContentUnpreview('label61');" title="click to collapse or expand..."> more... </a>
 <div id="label61" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">update_static_route</span> <b>(Alias name: update-static-route)</b>  Enable/disable updating the static route. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label62' href="javascript:ContentClick('label63', 'label62');" onmouseover="ContentPreview('label63');" onmouseout="ContentUnpreview('label63');" title="click to collapse or expand..."> more... </a>
 <div id="label63" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_id</span> <b>(Alias name: internet-service-id)</b>  Internet service id. <span class="li-normal">type: str</span>
 <a id='label64' href="javascript:ContentClick('label65', 'label64');" onmouseover="ContentPreview('label65');" onmouseout="ContentUnpreview('label65');" title="click to collapse or expand..."> more... </a>
 <div id="label65" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.2.0</code></p>
 </div>
 </li>
 <li><span class="li-head">probe_packets</span> <b>(Alias name: probe-packets)</b>  Enable/disable transmission of probe packets. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label66' href="javascript:ContentClick('label67', 'label66');" onmouseover="ContentPreview('label67');" onmouseout="ContentUnpreview('label67');" title="click to collapse or expand..."> more... </a>
 <div id="label67" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sla_fail_log_period</span> <b>(Alias name: sla-fail-log-period)</b>  Time interval in seconds that sla fail log messages will be generated (0 - 3600, default = 0). <span class="li-normal">type: int</span>
 <a id='label68' href="javascript:ContentClick('label69', 'label68');" onmouseover="ContentPreview('label69');" onmouseout="ContentUnpreview('label69');" title="click to collapse or expand..."> more... </a>
 <div id="label69" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sla_pass_log_period</span> <b>(Alias name: sla-pass-log-period)</b>  Time interval in seconds that sla pass log messages will be generated (0 - 3600, default = 0). <span class="li-normal">type: int</span>
 <a id='label70' href="javascript:ContentClick('label71', 'label70');" onmouseover="ContentPreview('label71');" onmouseout="ContentUnpreview('label71');" title="click to collapse or expand..."> more... </a>
 <div id="label71" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">timeout</span> How long to wait before not receiving a reply from the server to consider the connetion attempt a failure (1 - 255 sec, default = 1). <span class="li-normal">type: int</span>
 <a id='label72' href="javascript:ContentClick('label73', 'label72');" onmouseover="ContentPreview('label73');" onmouseout="ContentUnpreview('label73');" title="click to collapse or expand..."> more... </a>
 <div id="label73" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v6.4.15</code></p>
 </div>
 </li>
 <li><span class="li-head">ha_priority</span> <b>(Alias name: ha-priority)</b>  Ha election priority (1 - 50). <span class="li-normal">type: int</span>
 <a id='label74' href="javascript:ContentClick('label75', 'label74');" onmouseover="ContentPreview('label75');" onmouseout="ContentUnpreview('label75');" title="click to collapse or expand..."> more... </a>
 <div id="label75" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.2 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">diffservcode</span> Differentiated services code point (dscp) in the ip header of the probe packet. <span class="li-normal">type: str</span>
 <a id='label76' href="javascript:ContentClick('label77', 'label76');" onmouseover="ContentPreview('label77');" onmouseout="ContentUnpreview('label77');" title="click to collapse or expand..."> more... </a>
 <div id="label77" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">probe_timeout</span> <b>(Alias name: probe-timeout)</b>  Time to wait before a probe packet is considered lost (500 - 5000 msec, default = 500). <span class="li-normal">type: int</span>
 <a id='label78' href="javascript:ContentClick('label79', 'label78');" onmouseover="ContentPreview('label79');" onmouseout="ContentUnpreview('label79');" title="click to collapse or expand..."> more... </a>
 <div id="label79" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dns_request_domain</span> <b>(Alias name: dns-request-domain)</b>  Fully qualified domain name to resolve for the dns probe. <span class="li-normal">type: str</span>
 <a id='label80' href="javascript:ContentClick('label81', 'label80');" onmouseover="ContentPreview('label81');" onmouseout="ContentUnpreview('label81');" title="click to collapse or expand..."> more... </a>
 <div id="label81" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> v6.4.0</code></p>
 </div>
 </li>
 <li><span class="li-head">probe_count</span> <b>(Alias name: probe-count)</b>  Number of most recent probes that should be used to calculate latency and jitter (5 - 30, default = 30). <span class="li-normal">type: int</span>
 <a id='label82' href="javascript:ContentClick('label83', 'label82');" onmouseover="ContentPreview('label83');" onmouseout="ContentUnpreview('label83');" title="click to collapse or expand..."> more... </a>
 <div id="label83" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> v6.4.0</code></p>
 </div>
 </li>
 <li><span class="li-head">system_dns</span> <b>(Alias name: system-dns)</b>  Enable/disable system dns as the probe server. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label84' href="javascript:ContentClick('label85', 'label84');" onmouseover="ContentPreview('label85');" onmouseout="ContentUnpreview('label85');" title="click to collapse or expand..."> more... </a>
 <div id="label85" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> v6.4.0</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">load_balance_mode</span> <b>(Alias name: load-balance-mode)</b>  Algorithm or mode to use for load balancing internet traffic to sd-wan members. <span class="li-normal">type: str</span> <span class="li-normal">choices: [source-ip-based, weight-based, usage-based, source-dest-ip-based, measured-volume-based]</span> 
 <a id='label86' href="javascript:ContentClick('label87', 'label86');" onmouseover="ContentPreview('label87');" onmouseout="ContentUnpreview('label87');" title="click to collapse or expand..."> more... </a>
 <div id="label87" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">members</span> Members. <span class="li-normal">type: list</span>
 <a id='label88' href="javascript:ContentClick('label89', 'label88');" onmouseover="ContentPreview('label89');" onmouseout="ContentUnpreview('label89');" title="click to collapse or expand..."> more... </a>
 <div id="label89" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">_dynamic_member</span> <b>(Alias name: _dynamic-member)</b>  Dynamic member. <span class="li-normal">type: str</span>
 <a id='label90' href="javascript:ContentClick('label91', 'label90');" onmouseover="ContentPreview('label91');" onmouseout="ContentUnpreview('label91');" title="click to collapse or expand..."> more... </a>
 <div id="label91" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v6.4.15</code></p>
 </div>
 </li>
 <li><span class="li-head">comment</span> Comments. <span class="li-normal">type: str</span>
 <a id='label92' href="javascript:ContentClick('label93', 'label92');" onmouseover="ContentPreview('label93');" onmouseout="ContentUnpreview('label93');" title="click to collapse or expand..."> more... </a>
 <div id="label93" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">gateway</span> The default gateway for this interface. <span class="li-normal">type: str</span>
 <a id='label94' href="javascript:ContentClick('label95', 'label94');" onmouseover="ContentPreview('label95');" onmouseout="ContentUnpreview('label95');" title="click to collapse or expand..."> more... </a>
 <div id="label95" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">gateway6</span> Ipv6 gateway. <span class="li-normal">type: str</span>
 <a id='label96' href="javascript:ContentClick('label97', 'label96');" onmouseover="ContentPreview('label97');" onmouseout="ContentUnpreview('label97');" title="click to collapse or expand..."> more... </a>
 <div id="label97" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ingress_spillover_threshold</span> <b>(Alias name: ingress-spillover-threshold)</b>  Ingress spillover threshold for this interface (0 - 16776000 kbit/s). <span class="li-normal">type: int</span>
 <a id='label98' href="javascript:ContentClick('label99', 'label98');" onmouseover="ContentPreview('label99');" onmouseout="ContentUnpreview('label99');" title="click to collapse or expand..."> more... </a>
 <div id="label99" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">interface</span> Interface name. <span class="li-normal">type: str</span>
 <a id='label100' href="javascript:ContentClick('label101', 'label100');" onmouseover="ContentPreview('label101');" onmouseout="ContentUnpreview('label101');" title="click to collapse or expand..."> more... </a>
 <div id="label101" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">priority</span> Priority of the interface (0 - 4294967295). <span class="li-normal">type: int</span>
 <a id='label102' href="javascript:ContentClick('label103', 'label102');" onmouseover="ContentPreview('label103');" onmouseout="ContentUnpreview('label103');" title="click to collapse or expand..."> more... </a>
 <div id="label103" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">seq_num</span> <b>(Alias name: seq-num)</b>  Sequence number(1-255). <span class="li-normal">type: int</span>
 <a id='label104' href="javascript:ContentClick('label105', 'label104');" onmouseover="ContentPreview('label105');" onmouseout="ContentUnpreview('label105');" title="click to collapse or expand..."> more... </a>
 <div id="label105" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">source</span> Source ip address used in the health-check packet to the server. <span class="li-normal">type: str</span>
 <a id='label106' href="javascript:ContentClick('label107', 'label106');" onmouseover="ContentPreview('label107');" onmouseout="ContentUnpreview('label107');" title="click to collapse or expand..."> more... </a>
 <div id="label107" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">source6</span> Source ipv6 address used in the health-check packet to the server. <span class="li-normal">type: str</span>
 <a id='label108' href="javascript:ContentClick('label109', 'label108');" onmouseover="ContentPreview('label109');" onmouseout="ContentUnpreview('label109');" title="click to collapse or expand..."> more... </a>
 <div id="label109" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">spillover_threshold</span> <b>(Alias name: spillover-threshold)</b>  Egress spillover threshold for this interface (0 - 16776000 kbit/s). <span class="li-normal">type: int</span>
 <a id='label110' href="javascript:ContentClick('label111', 'label110');" onmouseover="ContentPreview('label111');" onmouseout="ContentUnpreview('label111');" title="click to collapse or expand..."> more... </a>
 <div id="label111" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">status</span> Enable/disable this interface in the sd-wan. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label112' href="javascript:ContentClick('label113', 'label112');" onmouseover="ContentPreview('label113');" onmouseout="ContentUnpreview('label113');" title="click to collapse or expand..."> more... </a>
 <div id="label113" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">volume_ratio</span> <b>(Alias name: volume-ratio)</b>  Measured volume ratio (this value / sum of all values = percentage of link volume, 0 - 255). <span class="li-normal">type: int</span>
 <a id='label114' href="javascript:ContentClick('label115', 'label114');" onmouseover="ContentPreview('label115');" onmouseout="ContentUnpreview('label115');" title="click to collapse or expand..."> more... </a>
 <div id="label115" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">weight</span> Weight of this interface for weighted load balancing. <span class="li-normal">type: int</span>
 <a id='label116' href="javascript:ContentClick('label117', 'label116');" onmouseover="ContentPreview('label117');" onmouseout="ContentUnpreview('label117');" title="click to collapse or expand..."> more... </a>
 <div id="label117" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">cost</span> Cost of this interface for services in sla mode (0 - 4294967295, default = 0). <span class="li-normal">type: int</span>
 <a id='label118' href="javascript:ContentClick('label119', 'label118');" onmouseover="ContentPreview('label119');" onmouseout="ContentUnpreview('label119');" title="click to collapse or expand..."> more... </a>
 <div id="label119" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.6.2</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">service</span> Service. <span class="li-normal">type: list</span>
 <a id='label120' href="javascript:ContentClick('label121', 'label120');" onmouseover="ContentPreview('label121');" onmouseout="ContentUnpreview('label121');" title="click to collapse or expand..."> more... </a>
 <div id="label121" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">addr_mode</span> <b>(Alias name: addr-mode)</b>  Address mode (ipv4 or ipv6). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ipv4, ipv6]</span> 
 <a id='label122' href="javascript:ContentClick('label123', 'label122');" onmouseover="ContentPreview('label123');" onmouseout="ContentUnpreview('label123');" title="click to collapse or expand..."> more... </a>
 <div id="label123" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_weight</span> <b>(Alias name: bandwidth-weight)</b>  Coefficient of reciprocal of available bidirectional bandwidth in the formula of custom-profile-1. <span class="li-normal">type: int</span>
 <a id='label124' href="javascript:ContentClick('label125', 'label124');" onmouseover="ContentPreview('label125');" onmouseout="ContentUnpreview('label125');" title="click to collapse or expand..."> more... </a>
 <div id="label125" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">default</span> Enable/disable use of sd-wan as default service. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label126' href="javascript:ContentClick('label127', 'label126');" onmouseover="ContentPreview('label127');" onmouseout="ContentUnpreview('label127');" title="click to collapse or expand..."> more... </a>
 <div id="label127" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp_forward</span> <b>(Alias name: dscp-forward)</b>  Enable/disable forward traffic dscp tag. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label128' href="javascript:ContentClick('label129', 'label128');" onmouseover="ContentPreview('label129');" onmouseout="ContentUnpreview('label129');" title="click to collapse or expand..."> more... </a>
 <div id="label129" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp_forward_tag</span> <b>(Alias name: dscp-forward-tag)</b>  Forward traffic dscp tag. <span class="li-normal">type: str</span>
 <a id='label130' href="javascript:ContentClick('label131', 'label130');" onmouseover="ContentPreview('label131');" onmouseout="ContentUnpreview('label131');" title="click to collapse or expand..."> more... </a>
 <div id="label131" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp_reverse</span> <b>(Alias name: dscp-reverse)</b>  Enable/disable reverse traffic dscp tag. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label132' href="javascript:ContentClick('label133', 'label132');" onmouseover="ContentPreview('label133');" onmouseout="ContentUnpreview('label133');" title="click to collapse or expand..."> more... </a>
 <div id="label133" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp_reverse_tag</span> <b>(Alias name: dscp-reverse-tag)</b>  Reverse traffic dscp tag. <span class="li-normal">type: str</span>
 <a id='label134' href="javascript:ContentClick('label135', 'label134');" onmouseover="ContentPreview('label135');" onmouseout="ContentUnpreview('label135');" title="click to collapse or expand..."> more... </a>
 <div id="label135" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dst</span> Destination address name. <span class="li-normal">type: list or str</span>
 <a id='label136' href="javascript:ContentClick('label137', 'label136');" onmouseover="ContentPreview('label137');" onmouseout="ContentUnpreview('label137');" title="click to collapse or expand..."> more... </a>
 <div id="label137" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dst_negate</span> <b>(Alias name: dst-negate)</b>  Enable/disable negation of destination address match. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label138' href="javascript:ContentClick('label139', 'label138');" onmouseover="ContentPreview('label139');" onmouseout="ContentUnpreview('label139');" title="click to collapse or expand..."> more... </a>
 <div id="label139" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">dst6</span> Destination address6 name. <span class="li-normal">type: list or str</span>
 <a id='label140' href="javascript:ContentClick('label141', 'label140');" onmouseover="ContentPreview('label141');" onmouseout="ContentUnpreview('label141');" title="click to collapse or expand..."> more... </a>
 <div id="label141" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">end_port</span> <b>(Alias name: end-port)</b>  End destination port number. <span class="li-normal">type: int</span>
 <a id='label142' href="javascript:ContentClick('label143', 'label142');" onmouseover="ContentPreview('label143');" onmouseout="ContentUnpreview('label143');" title="click to collapse or expand..."> more... </a>
 <div id="label143" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">gateway</span> Enable/disable sd-wan service gateway. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label144' href="javascript:ContentClick('label145', 'label144');" onmouseover="ContentPreview('label145');" onmouseout="ContentUnpreview('label145');" title="click to collapse or expand..."> more... </a>
 <div id="label145" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">groups</span> User groups. <span class="li-normal">type: list or str</span>
 <a id='label146' href="javascript:ContentClick('label147', 'label146');" onmouseover="ContentPreview('label147');" onmouseout="ContentUnpreview('label147');" title="click to collapse or expand..."> more... </a>
 <div id="label147" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">health_check</span> <b>(Alias name: health-check)</b>  Health check. <span class="li-normal">type: str</span>
 <a id='label148' href="javascript:ContentClick('label149', 'label148');" onmouseover="ContentPreview('label149');" onmouseout="ContentUnpreview('label149');" title="click to collapse or expand..."> more... </a>
 <div id="label149" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">hold_down_time</span> <b>(Alias name: hold-down-time)</b>  Waiting period in seconds when switching from the back-up member to the primary member (0 - 10000000, default = 0). <span class="li-normal">type: int</span>
 <a id='label150' href="javascript:ContentClick('label151', 'label150');" onmouseover="ContentPreview('label151');" onmouseout="ContentUnpreview('label151');" title="click to collapse or expand..."> more... </a>
 <div id="label151" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">id</span> Priority rule id (1 - 4000). <span class="li-normal">type: int</span>
 <a id='label152' href="javascript:ContentClick('label153', 'label152');" onmouseover="ContentPreview('label153');" onmouseout="ContentUnpreview('label153');" title="click to collapse or expand..."> more... </a>
 <div id="label153" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service</span> <b>(Alias name: internet-service)</b>  Enable/disable use of internet service for application-based load balancing. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label154' href="javascript:ContentClick('label155', 'label154');" onmouseover="ContentPreview('label155');" onmouseout="ContentUnpreview('label155');" title="click to collapse or expand..."> more... </a>
 <div id="label155" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_ctrl</span> <b>(Alias name: internet-service-ctrl)</b>  Control-based internet service id list. <span class="li-normal">type: list</span>
 <a id='label156' href="javascript:ContentClick('label157', 'label156');" onmouseover="ContentPreview('label157');" onmouseout="ContentUnpreview('label157');" title="click to collapse or expand..."> more... </a>
 <div id="label157" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.2.1</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_ctrl_group</span> <b>(Alias name: internet-service-ctrl-group)</b>  Control-based internet service group list. <span class="li-normal">type: list or str</span>
 <a id='label158' href="javascript:ContentClick('label159', 'label158');" onmouseover="ContentPreview('label159');" onmouseout="ContentUnpreview('label159');" title="click to collapse or expand..."> more... </a>
 <div id="label159" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.2.1</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_custom</span> <b>(Alias name: internet-service-custom)</b>  Custom internet service name list. <span class="li-normal">type: list or str</span>
 <a id='label160' href="javascript:ContentClick('label161', 'label160');" onmouseover="ContentPreview('label161');" onmouseout="ContentUnpreview('label161');" title="click to collapse or expand..."> more... </a>
 <div id="label161" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_custom_group</span> <b>(Alias name: internet-service-custom-group)</b>  Custom internet service group list. <span class="li-normal">type: list or str</span>
 <a id='label162' href="javascript:ContentClick('label163', 'label162');" onmouseover="ContentPreview('label163');" onmouseout="ContentUnpreview('label163');" title="click to collapse or expand..."> more... </a>
 <div id="label163" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_group</span> <b>(Alias name: internet-service-group)</b>  Internet service group list. <span class="li-normal">type: list or str</span>
 <a id='label164' href="javascript:ContentClick('label165', 'label164');" onmouseover="ContentPreview('label165');" onmouseout="ContentUnpreview('label165');" title="click to collapse or expand..."> more... </a>
 <div id="label165" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_id</span> <b>(Alias name: internet-service-id)</b>  Internet service id list. <span class="li-normal">type: list or str</span>
 <a id='label166' href="javascript:ContentClick('label167', 'label166');" onmouseover="ContentPreview('label167');" onmouseout="ContentUnpreview('label167');" title="click to collapse or expand..."> more... </a>
 <div id="label167" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">jitter_weight</span> <b>(Alias name: jitter-weight)</b>  Coefficient of jitter in the formula of custom-profile-1. <span class="li-normal">type: int</span>
 <a id='label168' href="javascript:ContentClick('label169', 'label168');" onmouseover="ContentPreview('label169');" onmouseout="ContentUnpreview('label169');" title="click to collapse or expand..."> more... </a>
 <div id="label169" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">latency_weight</span> <b>(Alias name: latency-weight)</b>  Coefficient of latency in the formula of custom-profile-1. <span class="li-normal">type: int</span>
 <a id='label170' href="javascript:ContentClick('label171', 'label170');" onmouseover="ContentPreview('label171');" onmouseout="ContentUnpreview('label171');" title="click to collapse or expand..."> more... </a>
 <div id="label171" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">link_cost_factor</span> <b>(Alias name: link-cost-factor)</b>  Link cost factor. <span class="li-normal">type: str</span> <span class="li-normal">choices: [latency, jitter, packet-loss, inbandwidth, outbandwidth, bibandwidth, custom-profile-1]</span> 
 <a id='label172' href="javascript:ContentClick('label173', 'label172');" onmouseover="ContentPreview('label173');" onmouseout="ContentUnpreview('label173');" title="click to collapse or expand..."> more... </a>
 <div id="label173" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">link_cost_threshold</span> <b>(Alias name: link-cost-threshold)</b>  Percentage threshold change of link cost values that will result in policy route regeneration (0 - 10000000, default = 10). <span class="li-normal">type: int</span>
 <a id='label174' href="javascript:ContentClick('label175', 'label174');" onmouseover="ContentPreview('label175');" onmouseout="ContentUnpreview('label175');" title="click to collapse or expand..."> more... </a>
 <div id="label175" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">member</span> Member sequence number. <span class="li-normal">type: str</span>
 <a id='label176' href="javascript:ContentClick('label177', 'label176');" onmouseover="ContentPreview('label177');" onmouseout="ContentUnpreview('label177');" title="click to collapse or expand..."> more... </a>
 <div id="label177" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.2.1</code></p>
 </div>
 </li>
 <li><span class="li-head">mode</span> Control how the priority rule sets the priority of interfaces in the sd-wan. <span class="li-normal">type: str</span> <span class="li-normal">choices: [auto, manual, priority, sla, load-balance]</span> 
 <a id='label178' href="javascript:ContentClick('label179', 'label178');" onmouseover="ContentPreview('label179');" onmouseout="ContentUnpreview('label179');" title="click to collapse or expand..."> more... </a>
 <div id="label179" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">name</span> Priority rule name. <span class="li-normal">type: str</span>
 <a id='label180' href="javascript:ContentClick('label181', 'label180');" onmouseover="ContentPreview('label181');" onmouseout="ContentUnpreview('label181');" title="click to collapse or expand..."> more... </a>
 <div id="label181" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">packet_loss_weight</span> <b>(Alias name: packet-loss-weight)</b>  Coefficient of packet-loss in the formula of custom-profile-1. <span class="li-normal">type: int</span>
 <a id='label182' href="javascript:ContentClick('label183', 'label182');" onmouseover="ContentPreview('label183');" onmouseout="ContentUnpreview('label183');" title="click to collapse or expand..."> more... </a>
 <div id="label183" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">priority_members</span> <b>(Alias name: priority-members)</b>  Member sequence number list. <span class="li-normal">type: list or str</span>
 <a id='label184' href="javascript:ContentClick('label185', 'label184');" onmouseover="ContentPreview('label185');" onmouseout="ContentUnpreview('label185');" title="click to collapse or expand..."> more... </a>
 <div id="label185" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">protocol</span> Protocol number. <span class="li-normal">type: int</span>
 <a id='label186' href="javascript:ContentClick('label187', 'label186');" onmouseover="ContentPreview('label187');" onmouseout="ContentUnpreview('label187');" title="click to collapse or expand..."> more... </a>
 <div id="label187" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">quality_link</span> <b>(Alias name: quality-link)</b>  Quality grade. <span class="li-normal">type: int</span>
 <a id='label188' href="javascript:ContentClick('label189', 'label188');" onmouseover="ContentPreview('label189');" onmouseout="ContentUnpreview('label189');" title="click to collapse or expand..."> more... </a>
 <div id="label189" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">route_tag</span> <b>(Alias name: route-tag)</b>  Ipv4 route map route-tag. <span class="li-normal">type: int</span>
 <a id='label190' href="javascript:ContentClick('label191', 'label190');" onmouseover="ContentPreview('label191');" onmouseout="ContentUnpreview('label191');" title="click to collapse or expand..."> more... </a>
 <div id="label191" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sla</span> Sla. <span class="li-normal">type: list</span>
 <a id='label192' href="javascript:ContentClick('label193', 'label192');" onmouseover="ContentPreview('label193');" onmouseout="ContentUnpreview('label193');" title="click to collapse or expand..."> more... </a>
 <div id="label193" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">health_check</span> <b>(Alias name: health-check)</b>  Virtual wan link health-check. <span class="li-normal">type: str</span>
 <a id='label194' href="javascript:ContentClick('label195', 'label194');" onmouseover="ContentPreview('label195');" onmouseout="ContentUnpreview('label195');" title="click to collapse or expand..."> more... </a>
 <div id="label195" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">id</span> Sla id. <span class="li-normal">type: int</span>
 <a id='label196' href="javascript:ContentClick('label197', 'label196');" onmouseover="ContentPreview('label197');" onmouseout="ContentUnpreview('label197');" title="click to collapse or expand..."> more... </a>
 <div id="label197" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">src</span> Source address name. <span class="li-normal">type: list or str</span>
 <a id='label198' href="javascript:ContentClick('label199', 'label198');" onmouseover="ContentPreview('label199');" onmouseout="ContentUnpreview('label199');" title="click to collapse or expand..."> more... </a>
 <div id="label199" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">src_negate</span> <b>(Alias name: src-negate)</b>  Enable/disable negation of source address match. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label200' href="javascript:ContentClick('label201', 'label200');" onmouseover="ContentPreview('label201');" onmouseout="ContentUnpreview('label201');" title="click to collapse or expand..."> more... </a>
 <div id="label201" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">src6</span> Source address6 name. <span class="li-normal">type: list or str</span>
 <a id='label202' href="javascript:ContentClick('label203', 'label202');" onmouseover="ContentPreview('label203');" onmouseout="ContentUnpreview('label203');" title="click to collapse or expand..."> more... </a>
 <div id="label203" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">start_port</span> <b>(Alias name: start-port)</b>  Start destination port number. <span class="li-normal">type: int</span>
 <a id='label204' href="javascript:ContentClick('label205', 'label204');" onmouseover="ContentPreview('label205');" onmouseout="ContentUnpreview('label205');" title="click to collapse or expand..."> more... </a>
 <div id="label205" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">status</span> Enable/disable sd-wan service. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label206' href="javascript:ContentClick('label207', 'label206');" onmouseover="ContentPreview('label207');" onmouseout="ContentUnpreview('label207');" title="click to collapse or expand..."> more... </a>
 <div id="label207" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">tos</span> Type of service bit pattern. <span class="li-normal">type: str</span>
 <a id='label208' href="javascript:ContentClick('label209', 'label208');" onmouseover="ContentPreview('label209');" onmouseout="ContentUnpreview('label209');" title="click to collapse or expand..."> more... </a>
 <div id="label209" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">tos_mask</span> <b>(Alias name: tos-mask)</b>  Type of service evaluated bits. <span class="li-normal">type: str</span>
 <a id='label210' href="javascript:ContentClick('label211', 'label210');" onmouseover="ContentPreview('label211');" onmouseout="ContentUnpreview('label211');" title="click to collapse or expand..."> more... </a>
 <div id="label211" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">users</span> User name. <span class="li-normal">type: list or str</span>
 <a id='label212' href="javascript:ContentClick('label213', 'label212');" onmouseover="ContentPreview('label213');" onmouseout="ContentUnpreview('label213');" title="click to collapse or expand..."> more... </a>
 <div id="label213" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_app_ctrl</span> <b>(Alias name: internet-service-app-ctrl)</b>  Application control based internet service id list. <span class="li-normal">type: list</span>
 <a id='label214' href="javascript:ContentClick('label215', 'label214');" onmouseover="ContentPreview('label215');" onmouseout="ContentUnpreview('label215');" title="click to collapse or expand..."> more... </a>
 <div id="label215" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_app_ctrl_group</span> <b>(Alias name: internet-service-app-ctrl-group)</b>  Application control based internet service group list. <span class="li-normal">type: list or str</span>
 <a id='label216' href="javascript:ContentClick('label217', 'label216');" onmouseover="ContentPreview('label217');" onmouseout="ContentUnpreview('label217');" title="click to collapse or expand..."> more... </a>
 <div id="label217" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">role</span> Service role to work with neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: [primary, secondary, standalone]</span> 
 <a id='label218' href="javascript:ContentClick('label219', 'label218');" onmouseover="ContentPreview('label219');" onmouseout="ContentUnpreview('label219');" title="click to collapse or expand..."> more... </a>
 <div id="label219" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sla_compare_method</span> <b>(Alias name: sla-compare-method)</b>  Method to compare sla value for sla and load balance mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [order, number]</span> 
 <a id='label220' href="javascript:ContentClick('label221', 'label220');" onmouseover="ContentPreview('label221');" onmouseout="ContentUnpreview('label221');" title="click to collapse or expand..."> more... </a>
 <div id="label221" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">standalone_action</span> <b>(Alias name: standalone-action)</b>  Enable/disable service when selected neighbor role is standalone while service role is not standalone. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label222' href="javascript:ContentClick('label223', 'label222');" onmouseover="ContentPreview('label223');" onmouseout="ContentUnpreview('label223');" title="click to collapse or expand..."> more... </a>
 <div id="label223" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">input_device</span> <b>(Alias name: input-device)</b>  Source interface name. <span class="li-normal">type: list or str</span>
 <a id='label224' href="javascript:ContentClick('label225', 'label224');" onmouseover="ContentPreview('label225');" onmouseout="ContentUnpreview('label225');" title="click to collapse or expand..."> more... </a>
 <div id="label225" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.2 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">internet_service_name</span> <b>(Alias name: internet-service-name)</b>  Internet service name list. <span class="li-normal">type: str</span>
 <a id='label226' href="javascript:ContentClick('label227', 'label226');" onmouseover="ContentPreview('label227');" onmouseout="ContentUnpreview('label227');" title="click to collapse or expand..."> more... </a>
 <div id="label227" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> v6.4.0</code></p>
 </div>
 </li>
 <li><span class="li-head">input_device_negate</span> <b>(Alias name: input-device-negate)</b>  Enable/disable negation of input device match. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label228' href="javascript:ContentClick('label229', 'label228');" onmouseover="ContentPreview('label229');" onmouseout="ContentUnpreview('label229');" title="click to collapse or expand..."> more... </a>
 <div id="label229" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.1 -> v7.6.2</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">status</span> Enable/disable sd-wan. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label230' href="javascript:ContentClick('label231', 'label230');" onmouseover="ContentPreview('label231');" onmouseout="ContentUnpreview('label231');" title="click to collapse or expand..."> more... </a>
 <div id="label231" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">neighbor</span> Neighbor. <span class="li-normal">type: list</span>
 <a id='label232' href="javascript:ContentClick('label233', 'label232');" onmouseover="ContentPreview('label233');" onmouseout="ContentUnpreview('label233');" title="click to collapse or expand..."> more... </a>
 <div id="label233" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">health_check</span> <b>(Alias name: health-check)</b>  Sd-wan health-check name. <span class="li-normal">type: str</span>
 <a id='label234' href="javascript:ContentClick('label235', 'label234');" onmouseover="ContentPreview('label235');" onmouseout="ContentUnpreview('label235');" title="click to collapse or expand..."> more... </a>
 <div id="label235" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ip</span> Ip address of neighbor. <span class="li-normal">type: str</span>
 <a id='label236' href="javascript:ContentClick('label237', 'label236');" onmouseover="ContentPreview('label237');" onmouseout="ContentUnpreview('label237');" title="click to collapse or expand..."> more... </a>
 <div id="label237" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">member</span> Member sequence number. <span class="li-normal">type: str</span>
 <a id='label238' href="javascript:ContentClick('label239', 'label238');" onmouseover="ContentPreview('label239');" onmouseout="ContentUnpreview('label239');" title="click to collapse or expand..."> more... </a>
 <div id="label239" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">role</span> Role of neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: [primary, secondary, standalone]</span> 
 <a id='label240' href="javascript:ContentClick('label241', 'label240');" onmouseover="ContentPreview('label241');" onmouseout="ContentUnpreview('label241');" title="click to collapse or expand..."> more... </a>
 <div id="label241" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sla_id</span> <b>(Alias name: sla-id)</b>  Sla id. <span class="li-normal">type: int</span>
 <a id='label242' href="javascript:ContentClick('label243', 'label242');" onmouseover="ContentPreview('label243');" onmouseout="ContentUnpreview('label243');" title="click to collapse or expand..."> more... </a>
 <div id="label243" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">neighbor_hold_boot_time</span> <b>(Alias name: neighbor-hold-boot-time)</b>  Waiting period in seconds when switching from the primary neighbor to the secondary neighbor from the neighbor start. <span class="li-normal">type: int</span>
 <a id='label244' href="javascript:ContentClick('label245', 'label244');" onmouseover="ContentPreview('label245');" onmouseout="ContentUnpreview('label245');" title="click to collapse or expand..."> more... </a>
 <div id="label245" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">neighbor_hold_down</span> <b>(Alias name: neighbor-hold-down)</b>  Enable/disable hold switching from the secondary neighbor to the primary neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label246' href="javascript:ContentClick('label247', 'label246');" onmouseover="ContentPreview('label247');" onmouseout="ContentUnpreview('label247');" title="click to collapse or expand..."> more... </a>
 <div id="label247" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">neighbor_hold_down_time</span> <b>(Alias name: neighbor-hold-down-time)</b>  Waiting period in seconds when switching from the secondary neighbor to the primary neighbor when hold-down is disabled. <span class="li-normal">type: int</span>
 <a id='label248' href="javascript:ContentClick('label249', 'label248');" onmouseover="ContentPreview('label249');" onmouseout="ContentUnpreview('label249');" title="click to collapse or expand..."> more... </a>
 <div id="label249" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">fail_alert_interfaces</span> <b>(Alias name: fail-alert-interfaces)</b>  Physical interfaces that will be alerted. <span class="li-normal">type: list</span>
 <a id='label250' href="javascript:ContentClick('label251', 'label250');" onmouseover="ContentPreview('label251');" onmouseout="ContentUnpreview('label251');" title="click to collapse or expand..."> more... </a>
 <div id="label251" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.3 -> v7.6.2</code></p>
 </div>
 </li>
 </ul>
 </ul>



Notes
-----
.. note::
   - Running in workspace locking mode is supported in this FortiManager module, the top level parameters workspace_locking_adom and workspace_locking_timeout help do the work.
   - To create or update an object, use state: present directive.
   - To delete an object, use state: absent directive
   - Normally, running one module can fail when a non-zero rc is returned. you can also override the conditions to fail or succeed with parameters rc_failed and rc_succeeded

Examples
--------

.. code-block:: yaml+jinja

  - name: Example playbook (generated based on argument schema)
    hosts: fortimanagers
    connection: httpapi
    gather_facts: false
    vars:
      ansible_httpapi_use_ssl: true
      ansible_httpapi_validate_certs: false
      ansible_httpapi_port: 443
    tasks:
      - name: Configure redundant internet connections using SD-WAN
        fortinet.fortimanager.fmgr_wanprof_system_virtualwanlink:
          # bypass_validation: false
          workspace_locking_adom: <value in [global, custom adom including root]>
          workspace_locking_timeout: 300
          # rc_succeeded: [0, -2, -3, ...]
          # rc_failed: [-2, -3, ...]
          adom: <your own value>
          wanprof: <your own value>
          wanprof_system_virtualwanlink:
            # fail_detect: <value in [disable, enable]>
            # health_check:
            #   - _dynamic_server: <string>
            #     addr_mode: <value in [ipv4, ipv6]>
            #     failtime: <integer>
            #     http_agent: <string>
            #     http_get: <string>
            #     http_match: <string>
            #     interval: <integer>
            #     members: <list or string>
            #     name: <string>
            #     packet_size: <integer>
            #     password: <list or string>
            #     port: <integer>
            #     protocol: <value in [ping, tcp-echo, udp-echo, ...]>
            #     recoverytime: <integer>
            #     security_mode: <value in [none, authentication]>
            #     server: <list or string>
            #     sla:
            #       - id: <integer>
            #         jitter_threshold: <integer>
            #         latency_threshold: <integer>
            #         link_cost_factor:
            #           - "latency"
            #           - "jitter"
            #           - "packet-loss"
            #         packetloss_threshold: <integer>
            #     threshold_alert_jitter: <integer>
            #     threshold_alert_latency: <integer>
            #     threshold_alert_packetloss: <integer>
            #     threshold_warning_jitter: <integer>
            #     threshold_warning_latency: <integer>
            #     threshold_warning_packetloss: <integer>
            #     update_cascade_interface: <value in [disable, enable]>
            #     update_static_route: <value in [disable, enable]>
            #     internet_service_id: <string>
            #     probe_packets: <value in [disable, enable]>
            #     sla_fail_log_period: <integer>
            #     sla_pass_log_period: <integer>
            #     timeout: <integer>
            #     ha_priority: <integer>
            #     diffservcode: <string>
            #     probe_timeout: <integer>
            #     dns_request_domain: <string>
            #     probe_count: <integer>
            #     system_dns: <value in [disable, enable]>
            # load_balance_mode: <value in [source-ip-based, weight-based, usage-based, ...]>
            # members:
            #   - _dynamic_member: <string>
            #     comment: <string>
            #     gateway: <string>
            #     gateway6: <string>
            #     ingress_spillover_threshold: <integer>
            #     interface: <string>
            #     priority: <integer>
            #     seq_num: <integer>
            #     source: <string>
            #     source6: <string>
            #     spillover_threshold: <integer>
            #     status: <value in [disable, enable]>
            #     volume_ratio: <integer>
            #     weight: <integer>
            #     cost: <integer>
            # service:
            #   - addr_mode: <value in [ipv4, ipv6]>
            #     bandwidth_weight: <integer>
            #     default: <value in [disable, enable]>
            #     dscp_forward: <value in [disable, enable]>
            #     dscp_forward_tag: <string>
            #     dscp_reverse: <value in [disable, enable]>
            #     dscp_reverse_tag: <string>
            #     dst: <list or string>
            #     dst_negate: <value in [disable, enable]>
            #     dst6: <list or string>
            #     end_port: <integer>
            #     gateway: <value in [disable, enable]>
            #     groups: <list or string>
            #     health_check: <string>
            #     hold_down_time: <integer>
            #     id: <integer>
            #     internet_service: <value in [disable, enable]>
            #     internet_service_ctrl: <list or integer>
            #     internet_service_ctrl_group: <list or string>
            #     internet_service_custom: <list or string>
            #     internet_service_custom_group: <list or string>
            #     internet_service_group: <list or string>
            #     internet_service_id: <list or string>
            #     jitter_weight: <integer>
            #     latency_weight: <integer>
            #     link_cost_factor: <value in [latency, jitter, packet-loss, ...]>
            #     link_cost_threshold: <integer>
            #     member: <string>
            #     mode: <value in [auto, manual, priority, ...]>
            #     name: <string>
            #     packet_loss_weight: <integer>
            #     priority_members: <list or string>
            #     protocol: <integer>
            #     quality_link: <integer>
            #     route_tag: <integer>
            #     sla:
            #       - health_check: <string>
            #         id: <integer>
            #     src: <list or string>
            #     src_negate: <value in [disable, enable]>
            #     src6: <list or string>
            #     start_port: <integer>
            #     status: <value in [disable, enable]>
            #     tos: <string>
            #     tos_mask: <string>
            #     users: <list or string>
            #     internet_service_app_ctrl: <list or integer>
            #     internet_service_app_ctrl_group: <list or string>
            #     role: <value in [primary, secondary, standalone]>
            #     sla_compare_method: <value in [order, number]>
            #     standalone_action: <value in [disable, enable]>
            #     input_device: <list or string>
            #     internet_service_name: <string>
            #     input_device_negate: <value in [disable, enable]>
            # status: <value in [disable, enable]>
            # neighbor:
            #   - health_check: <string>
            #     ip: <string>
            #     member: <string>
            #     role: <value in [primary, secondary, standalone]>
            #     sla_id: <integer>
            # neighbor_hold_boot_time: <integer>
            # neighbor_hold_down: <value in [disable, enable]>
            # neighbor_hold_down_time: <integer>
            # fail_alert_interfaces: <list or string>


Return Values
-------------

Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

 <ul>
 <li> <span class="li-return">meta</span> - The result of the request.<span class="li-normal">returned: always</span> <span class="li-normal">type: dict</span></li>
 <ul class="ul-self"> <li> <span class="li-return">request_url</span> - The full url requested. <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: /sys/login/user</span></li>
 <li> <span class="li-return">response_code</span> - The status of api request. <span class="li-normal">returned: always</span> <span class="li-normal">type: int</span> <span class="li-normal">sample: 0</span></li>
 <li> <span class="li-return">response_data</span> - The data body of the api response. <span class="li-normal">returned: optional</span> <span class="li-normal">type: list or dict</span></li>
 <li> <span class="li-return">response_message</span> - The descriptive message of the api response. <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: OK</span></li>
 <li> <span class="li-return">system_information</span> - The information of the target system. <span class="li-normal">returned: always</span> <span class="li-normal">type: dict</span></li>
 </ul>
 <li> <span class="li-return">rc</span> - The status the request. <span class="li-normal">returned: always</span> <span class="li-normal">type: int</span> <span class="li-normal">sample: 0</span></li>
 <li> <span class="li-return">version_check_warning</span> - Warning if the parameters used in the playbook are not supported by the current FortiManager version. <span class="li-normal">returned: if at least one parameter not supported by the current FortiManager version</span> <span class="li-normal">type: list</span> </li>
 </ul>


Status
------

- This module is not guaranteed to have a backwards compatible interface.


Authors
-------

- Xinwei Du (@dux-fortinet)
- Xing Li (@lix-fortinet)
- Jie Xue (@JieX19)
- Link Zheng (@chillancezen)
- Frank Shen (@fshen01)
- Hongbin Lu (@fgtdev-hblu)
