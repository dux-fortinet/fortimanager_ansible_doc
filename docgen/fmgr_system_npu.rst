:source: fmgr_system_npu.py

:orphan:

.. _fmgr_system_npu:

fmgr_system_npu -- Configure NPU attributes.
++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.1.0

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

 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>



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
 <li><span class="li-head">system_npu</span> - Configure NPU attributes. <span class="li-normal">type: dict</span></li>
 <ul class="ul-self">
 <li><span class="li-head">capwap_offload</span> <b>(Alias name: capwap-offload)</b>  Enable/disable offloading managed fortiap and fortilink capwap sessions. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label0' href="javascript:ContentClick('label1', 'label0');" onmouseover="ContentPreview('label1');" onmouseout="ContentUnpreview('label1');" title="click to collapse or expand..."> more... </a>
 <div id="label1" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dedicated_management_affinity</span> <b>(Alias name: dedicated-management-affinity)</b>  Affinity setting for management deamons (hexadecimal value up to 256 bits in the format of xxxxxxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label2' href="javascript:ContentClick('label3', 'label2');" onmouseover="ContentPreview('label3');" onmouseout="ContentUnpreview('label3');" title="click to collapse or expand..."> more... </a>
 <div id="label3" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dedicated_management_cpu</span> <b>(Alias name: dedicated-management-cpu)</b>  Enable to dedicate one cpu for gui and cli connections when nps are busy. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label4' href="javascript:ContentClick('label5', 'label4');" onmouseover="ContentPreview('label5');" onmouseout="ContentUnpreview('label5');" title="click to collapse or expand..."> more... </a>
 <div id="label5" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fastpath</span> Enable/disable np6 offloading (also called fast path). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label6' href="javascript:ContentClick('label7', 'label6');" onmouseover="ContentPreview('label7');" onmouseout="ContentUnpreview('label7');" title="click to collapse or expand..."> more... </a>
 <div id="label7" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fp_anomaly</span> <b>(Alias name: fp-anomaly)</b>  Fp anomaly. <span class="li-normal">type: dict</span>
 <a id='label8' href="javascript:ContentClick('label9', 'label8');" onmouseover="ContentPreview('label9');" onmouseout="ContentUnpreview('label9');" title="click to collapse or expand..."> more... </a>
 <div id="label9" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">esp_minlen_err</span> <b>(Alias name: esp-minlen-err)</b>  Invalid ipv4 esp short packet anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label10' href="javascript:ContentClick('label11', 'label10');" onmouseover="ContentPreview('label11');" onmouseout="ContentUnpreview('label11');" title="click to collapse or expand..."> more... </a>
 <div id="label11" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_csum_err</span> <b>(Alias name: icmp-csum-err)</b>  Invalid ipv4 icmp packet checksum anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label12' href="javascript:ContentClick('label13', 'label12');" onmouseover="ContentPreview('label13');" onmouseout="ContentUnpreview('label13');" title="click to collapse or expand..."> more... </a>
 <div id="label13" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_minlen_err</span> <b>(Alias name: icmp-minlen-err)</b>  Invalid ipv4 icmp short packet anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label14' href="javascript:ContentClick('label15', 'label14');" onmouseover="ContentPreview('label15');" onmouseout="ContentUnpreview('label15');" title="click to collapse or expand..."> more... </a>
 <div id="label15" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_csum_err</span> <b>(Alias name: ipv4-csum-err)</b>  Invalid ipv4 packet checksum anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label16' href="javascript:ContentClick('label17', 'label16');" onmouseover="ContentPreview('label17');" onmouseout="ContentUnpreview('label17');" title="click to collapse or expand..."> more... </a>
 <div id="label17" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_ihl_err</span> <b>(Alias name: ipv4-ihl-err)</b>  Invalid ipv4 header length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label18' href="javascript:ContentClick('label19', 'label18');" onmouseover="ContentPreview('label19');" onmouseout="ContentUnpreview('label19');" title="click to collapse or expand..."> more... </a>
 <div id="label19" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_len_err</span> <b>(Alias name: ipv4-len-err)</b>  Invalid ipv4 packet length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label20' href="javascript:ContentClick('label21', 'label20');" onmouseover="ContentPreview('label21');" onmouseout="ContentUnpreview('label21');" title="click to collapse or expand..."> more... </a>
 <div id="label21" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_opt_err</span> <b>(Alias name: ipv4-opt-err)</b>  Invalid ipv4 option parsing anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label22' href="javascript:ContentClick('label23', 'label22');" onmouseover="ContentPreview('label23');" onmouseout="ContentUnpreview('label23');" title="click to collapse or expand..."> more... </a>
 <div id="label23" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_ttlzero_err</span> <b>(Alias name: ipv4-ttlzero-err)</b>  Invalid ipv4 ttl field zero anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label24' href="javascript:ContentClick('label25', 'label24');" onmouseover="ContentPreview('label25');" onmouseout="ContentUnpreview('label25');" title="click to collapse or expand..."> more... </a>
 <div id="label25" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_ver_err</span> <b>(Alias name: ipv4-ver-err)</b>  Invalid ipv4 header version anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label26' href="javascript:ContentClick('label27', 'label26');" onmouseover="ContentPreview('label27');" onmouseout="ContentUnpreview('label27');" title="click to collapse or expand..."> more... </a>
 <div id="label27" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_exthdr_len_err</span> <b>(Alias name: ipv6-exthdr-len-err)</b>  Invalid ipv6 packet chain extension header total length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label28' href="javascript:ContentClick('label29', 'label28');" onmouseover="ContentPreview('label29');" onmouseout="ContentUnpreview('label29');" title="click to collapse or expand..."> more... </a>
 <div id="label29" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_exthdr_order_err</span> <b>(Alias name: ipv6-exthdr-order-err)</b>  Invalid ipv6 packet extension header ordering anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label30' href="javascript:ContentClick('label31', 'label30');" onmouseover="ContentPreview('label31');" onmouseout="ContentUnpreview('label31');" title="click to collapse or expand..."> more... </a>
 <div id="label31" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_ihl_err</span> <b>(Alias name: ipv6-ihl-err)</b>  Invalid ipv6 packet length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label32' href="javascript:ContentClick('label33', 'label32');" onmouseover="ContentPreview('label33');" onmouseout="ContentUnpreview('label33');" title="click to collapse or expand..."> more... </a>
 <div id="label33" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_plen_zero</span> <b>(Alias name: ipv6-plen-zero)</b>  Invalid ipv6 packet payload length zero anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label34' href="javascript:ContentClick('label35', 'label34');" onmouseover="ContentPreview('label35');" onmouseout="ContentUnpreview('label35');" title="click to collapse or expand..."> more... </a>
 <div id="label35" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_ver_err</span> <b>(Alias name: ipv6-ver-err)</b>  Invalid ipv6 packet version anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label36' href="javascript:ContentClick('label37', 'label36');" onmouseover="ContentPreview('label37');" onmouseout="ContentUnpreview('label37');" title="click to collapse or expand..."> more... </a>
 <div id="label37" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_csum_err</span> <b>(Alias name: tcp-csum-err)</b>  Invalid ipv4 tcp packet checksum anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label38' href="javascript:ContentClick('label39', 'label38');" onmouseover="ContentPreview('label39');" onmouseout="ContentUnpreview('label39');" title="click to collapse or expand..."> more... </a>
 <div id="label39" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_hlen_err</span> <b>(Alias name: tcp-hlen-err)</b>  Invalid ipv4 tcp header length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label40' href="javascript:ContentClick('label41', 'label40');" onmouseover="ContentPreview('label41');" onmouseout="ContentUnpreview('label41');" title="click to collapse or expand..."> more... </a>
 <div id="label41" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_plen_err</span> <b>(Alias name: tcp-plen-err)</b>  Invalid ipv4 tcp packet length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label42' href="javascript:ContentClick('label43', 'label42');" onmouseover="ContentPreview('label43');" onmouseout="ContentUnpreview('label43');" title="click to collapse or expand..."> more... </a>
 <div id="label43" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_csum_err</span> <b>(Alias name: udp-csum-err)</b>  Invalid ipv4 udp packet checksum anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label44' href="javascript:ContentClick('label45', 'label44');" onmouseover="ContentPreview('label45');" onmouseout="ContentUnpreview('label45');" title="click to collapse or expand..."> more... </a>
 <div id="label45" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_hlen_err</span> <b>(Alias name: udp-hlen-err)</b>  Invalid ipv4 udp packet header length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label46' href="javascript:ContentClick('label47', 'label46');" onmouseover="ContentPreview('label47');" onmouseout="ContentUnpreview('label47');" title="click to collapse or expand..."> more... </a>
 <div id="label47" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_len_err</span> <b>(Alias name: udp-len-err)</b>  Invalid ipv4 udp packet length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label48' href="javascript:ContentClick('label49', 'label48');" onmouseover="ContentPreview('label49');" onmouseout="ContentUnpreview('label49');" title="click to collapse or expand..."> more... </a>
 <div id="label49" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_plen_err</span> <b>(Alias name: udp-plen-err)</b>  Invalid ipv4 udp packet minimum length anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label50' href="javascript:ContentClick('label51', 'label50');" onmouseover="ContentPreview('label51');" onmouseout="ContentUnpreview('label51');" title="click to collapse or expand..."> more... </a>
 <div id="label51" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udplite_cover_err</span> <b>(Alias name: udplite-cover-err)</b>  Invalid ipv4 udp-lite packet coverage anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label52' href="javascript:ContentClick('label53', 'label52');" onmouseover="ContentPreview('label53');" onmouseout="ContentUnpreview('label53');" title="click to collapse or expand..."> more... </a>
 <div id="label53" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udplite_csum_err</span> <b>(Alias name: udplite-csum-err)</b>  Invalid ipv4 udp-lite packet checksum anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host, allow]</span> 
 <a id='label54' href="javascript:ContentClick('label55', 'label54');" onmouseover="ContentPreview('label55');" onmouseout="ContentUnpreview('label55');" title="click to collapse or expand..."> more... </a>
 <div id="label55" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">unknproto_minlen_err</span> <b>(Alias name: unknproto-minlen-err)</b>  Invalid ipv4 l4 unknown protocol short packet anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label56' href="javascript:ContentClick('label57', 'label56');" onmouseover="ContentPreview('label57');" onmouseout="ContentUnpreview('label57');" title="click to collapse or expand..."> more... </a>
 <div id="label57" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_fin_only</span> <b>(Alias name: tcp-fin-only)</b>  Tcp syn flood with only fin flag set anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label58' href="javascript:ContentClick('label59', 'label58');" onmouseover="ContentPreview('label59');" onmouseout="ContentUnpreview('label59');" title="click to collapse or expand..."> more... </a>
 <div id="label59" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_optsecurity</span> <b>(Alias name: ipv4-optsecurity)</b>  Security option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label60' href="javascript:ContentClick('label61', 'label60');" onmouseover="ContentPreview('label61');" onmouseout="ContentUnpreview('label61');" title="click to collapse or expand..."> more... </a>
 <div id="label61" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_optralert</span> <b>(Alias name: ipv6-optralert)</b>  Router alert option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label62' href="javascript:ContentClick('label63', 'label62');" onmouseover="ContentPreview('label63');" onmouseout="ContentUnpreview('label63');" title="click to collapse or expand..."> more... </a>
 <div id="label63" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_syn_fin</span> <b>(Alias name: tcp-syn-fin)</b>  Tcp syn flood syn/fin flag set anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label64' href="javascript:ContentClick('label65', 'label64');" onmouseover="ContentPreview('label65');" onmouseout="ContentUnpreview('label65');" title="click to collapse or expand..."> more... </a>
 <div id="label65" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_proto_err</span> <b>(Alias name: ipv4-proto-err)</b>  Invalid layer 4 protocol anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label66' href="javascript:ContentClick('label67', 'label66');" onmouseover="ContentPreview('label67');" onmouseout="ContentUnpreview('label67');" title="click to collapse or expand..."> more... </a>
 <div id="label67" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_saddr_err</span> <b>(Alias name: ipv6-saddr-err)</b>  Source address as multicast anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label68' href="javascript:ContentClick('label69', 'label68');" onmouseover="ContentPreview('label69');" onmouseout="ContentUnpreview('label69');" title="click to collapse or expand..."> more... </a>
 <div id="label69" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_frag</span> <b>(Alias name: icmp-frag)</b>  Layer 3 fragmented packets that could be part of layer 4 icmp anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label70' href="javascript:ContentClick('label71', 'label70');" onmouseover="ContentPreview('label71');" onmouseout="ContentUnpreview('label71');" title="click to collapse or expand..."> more... </a>
 <div id="label71" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_optssrr</span> <b>(Alias name: ipv4-optssrr)</b>  Strict source record route option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label72' href="javascript:ContentClick('label73', 'label72');" onmouseover="ContentPreview('label73');" onmouseout="ContentUnpreview('label73');" title="click to collapse or expand..."> more... </a>
 <div id="label73" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_opthomeaddr</span> <b>(Alias name: ipv6-opthomeaddr)</b>  Home address option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label74' href="javascript:ContentClick('label75', 'label74');" onmouseover="ContentPreview('label75');" onmouseout="ContentUnpreview('label75');" title="click to collapse or expand..."> more... </a>
 <div id="label75" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_land</span> <b>(Alias name: udp-land)</b>  Udp land anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label76' href="javascript:ContentClick('label77', 'label76');" onmouseover="ContentPreview('label77');" onmouseout="ContentUnpreview('label77');" title="click to collapse or expand..."> more... </a>
 <div id="label77" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_optinvld</span> <b>(Alias name: ipv6-optinvld)</b>  Invalid option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label78' href="javascript:ContentClick('label79', 'label78');" onmouseover="ContentPreview('label79');" onmouseout="ContentUnpreview('label79');" title="click to collapse or expand..."> more... </a>
 <div id="label79" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_fin_noack</span> <b>(Alias name: tcp-fin-noack)</b>  Tcp syn flood with fin flag set without ack setting anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label80' href="javascript:ContentClick('label81', 'label80');" onmouseover="ContentPreview('label81');" onmouseout="ContentUnpreview('label81');" title="click to collapse or expand..."> more... </a>
 <div id="label81" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_proto_err</span> <b>(Alias name: ipv6-proto-err)</b>  Layer 4 invalid protocol anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label82' href="javascript:ContentClick('label83', 'label82');" onmouseover="ContentPreview('label83');" onmouseout="ContentUnpreview('label83');" title="click to collapse or expand..."> more... </a>
 <div id="label83" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_land</span> <b>(Alias name: tcp-land)</b>  Tcp land anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label84' href="javascript:ContentClick('label85', 'label84');" onmouseover="ContentPreview('label85');" onmouseout="ContentUnpreview('label85');" title="click to collapse or expand..."> more... </a>
 <div id="label85" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_unknopt</span> <b>(Alias name: ipv4-unknopt)</b>  Unknown option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label86' href="javascript:ContentClick('label87', 'label86');" onmouseover="ContentPreview('label87');" onmouseout="ContentUnpreview('label87');" title="click to collapse or expand..."> more... </a>
 <div id="label87" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_optstream</span> <b>(Alias name: ipv4-optstream)</b>  Stream option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label88' href="javascript:ContentClick('label89', 'label88');" onmouseover="ContentPreview('label89');" onmouseout="ContentUnpreview('label89');" title="click to collapse or expand..."> more... </a>
 <div id="label89" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_optjumbo</span> <b>(Alias name: ipv6-optjumbo)</b>  Jumbo options anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label90' href="javascript:ContentClick('label91', 'label90');" onmouseover="ContentPreview('label91');" onmouseout="ContentUnpreview('label91');" title="click to collapse or expand..."> more... </a>
 <div id="label91" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_land</span> <b>(Alias name: icmp-land)</b>  Icmp land anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label92' href="javascript:ContentClick('label93', 'label92');" onmouseover="ContentPreview('label93');" onmouseout="ContentUnpreview('label93');" title="click to collapse or expand..."> more... </a>
 <div id="label93" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_winnuke</span> <b>(Alias name: tcp-winnuke)</b>  Tcp winnuke anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label94' href="javascript:ContentClick('label95', 'label94');" onmouseover="ContentPreview('label95');" onmouseout="ContentUnpreview('label95');" title="click to collapse or expand..."> more... </a>
 <div id="label95" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_daddr_err</span> <b>(Alias name: ipv6-daddr-err)</b>  Destination address as unspecified or loopback address anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label96' href="javascript:ContentClick('label97', 'label96');" onmouseover="ContentPreview('label97');" onmouseout="ContentUnpreview('label97');" title="click to collapse or expand..."> more... </a>
 <div id="label97" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_land</span> <b>(Alias name: ipv4-land)</b>  Land anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label98' href="javascript:ContentClick('label99', 'label98');" onmouseover="ContentPreview('label99');" onmouseout="ContentUnpreview('label99');" title="click to collapse or expand..."> more... </a>
 <div id="label99" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_opttunnel</span> <b>(Alias name: ipv6-opttunnel)</b>  Tunnel encapsulation limit option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label100' href="javascript:ContentClick('label101', 'label100');" onmouseover="ContentPreview('label101');" onmouseout="ContentUnpreview('label101');" title="click to collapse or expand..."> more... </a>
 <div id="label101" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_no_flag</span> <b>(Alias name: tcp-no-flag)</b>  Tcp syn flood with no flag set anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label102' href="javascript:ContentClick('label103', 'label102');" onmouseover="ContentPreview('label103');" onmouseout="ContentUnpreview('label103');" title="click to collapse or expand..."> more... </a>
 <div id="label103" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_land</span> <b>(Alias name: ipv6-land)</b>  Land anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label104' href="javascript:ContentClick('label105', 'label104');" onmouseover="ContentPreview('label105');" onmouseout="ContentUnpreview('label105');" title="click to collapse or expand..."> more... </a>
 <div id="label105" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_optlsrr</span> <b>(Alias name: ipv4-optlsrr)</b>  Loose source record route option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label106' href="javascript:ContentClick('label107', 'label106');" onmouseover="ContentPreview('label107');" onmouseout="ContentUnpreview('label107');" title="click to collapse or expand..."> more... </a>
 <div id="label107" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_opttimestamp</span> <b>(Alias name: ipv4-opttimestamp)</b>  Timestamp option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label108' href="javascript:ContentClick('label109', 'label108');" onmouseover="ContentPreview('label109');" onmouseout="ContentUnpreview('label109');" title="click to collapse or expand..."> more... </a>
 <div id="label109" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_optrr</span> <b>(Alias name: ipv4-optrr)</b>  Record route option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label110' href="javascript:ContentClick('label111', 'label110');" onmouseover="ContentPreview('label111');" onmouseout="ContentUnpreview('label111');" title="click to collapse or expand..."> more... </a>
 <div id="label111" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_optnsap</span> <b>(Alias name: ipv6-optnsap)</b>  Network service access point address option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label112' href="javascript:ContentClick('label113', 'label112');" onmouseover="ContentPreview('label113');" onmouseout="ContentUnpreview('label113');" title="click to collapse or expand..."> more... </a>
 <div id="label113" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_unknopt</span> <b>(Alias name: ipv6-unknopt)</b>  Unknown option anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label114' href="javascript:ContentClick('label115', 'label114');" onmouseover="ContentPreview('label115');" onmouseout="ContentUnpreview('label115');" title="click to collapse or expand..."> more... </a>
 <div id="label115" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_syn_data</span> <b>(Alias name: tcp-syn-data)</b>  Tcp syn flood packets with data anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label116' href="javascript:ContentClick('label117', 'label116');" onmouseover="ContentPreview('label117');" onmouseout="ContentUnpreview('label117');" title="click to collapse or expand..."> more... </a>
 <div id="label117" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_optendpid</span> <b>(Alias name: ipv6-optendpid)</b>  End point identification anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label118' href="javascript:ContentClick('label119', 'label118');" onmouseover="ContentPreview('label119');" onmouseout="ContentUnpreview('label119');" title="click to collapse or expand..."> more... </a>
 <div id="label119" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gtpu_plen_err</span> <b>(Alias name: gtpu-plen-err)</b>  Gtpu plen err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label120' href="javascript:ContentClick('label121', 'label120');" onmouseover="ContentPreview('label121');" onmouseout="ContentUnpreview('label121');" title="click to collapse or expand..."> more... </a>
 <div id="label121" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">vxlan_minlen_err</span> <b>(Alias name: vxlan-minlen-err)</b>  Vxlan minlen err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label122' href="javascript:ContentClick('label123', 'label122');" onmouseover="ContentPreview('label123');" onmouseout="ContentUnpreview('label123');" title="click to collapse or expand..."> more... </a>
 <div id="label123" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">capwap_minlen_err</span> <b>(Alias name: capwap-minlen-err)</b>  Capwap minlen err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label124' href="javascript:ContentClick('label125', 'label124');" onmouseover="ContentPreview('label125');" onmouseout="ContentUnpreview('label125');" title="click to collapse or expand..."> more... </a>
 <div id="label125" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">gre_csum_err</span> <b>(Alias name: gre-csum-err)</b>  Gre csum err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host, allow]</span> 
 <a id='label126' href="javascript:ContentClick('label127', 'label126');" onmouseover="ContentPreview('label127');" onmouseout="ContentUnpreview('label127');" title="click to collapse or expand..."> more... </a>
 <div id="label127" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">nvgre_minlen_err</span> <b>(Alias name: nvgre-minlen-err)</b>  Nvgre minlen err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label128' href="javascript:ContentClick('label129', 'label128');" onmouseover="ContentPreview('label129');" onmouseout="ContentUnpreview('label129');" title="click to collapse or expand..."> more... </a>
 <div id="label129" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sctp_l4len_err</span> <b>(Alias name: sctp-l4len-err)</b>  Sctp l4len err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label130' href="javascript:ContentClick('label131', 'label130');" onmouseover="ContentPreview('label131');" onmouseout="ContentUnpreview('label131');" title="click to collapse or expand..."> more... </a>
 <div id="label131" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_hlenvsl4len_err</span> <b>(Alias name: tcp-hlenvsl4len-err)</b>  Tcp hlenvsl4len err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label132' href="javascript:ContentClick('label133', 'label132');" onmouseover="ContentPreview('label133');" onmouseout="ContentUnpreview('label133');" title="click to collapse or expand..."> more... </a>
 <div id="label133" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sctp_crc_err</span> <b>(Alias name: sctp-crc-err)</b>  Sctp crc err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label134' href="javascript:ContentClick('label135', 'label134');" onmouseover="ContentPreview('label135');" onmouseout="ContentUnpreview('label135');" title="click to collapse or expand..."> more... </a>
 <div id="label135" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sctp_clen_err</span> <b>(Alias name: sctp-clen-err)</b>  Sctp clen err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label136' href="javascript:ContentClick('label137', 'label136');" onmouseover="ContentPreview('label137');" onmouseout="ContentUnpreview('label137');" title="click to collapse or expand..."> more... </a>
 <div id="label137" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">uesp_minlen_err</span> <b>(Alias name: uesp-minlen-err)</b>  Uesp minlen err. <span class="li-normal">type: str</span> <span class="li-normal">choices: [drop, trap-to-host]</span> 
 <a id='label138' href="javascript:ContentClick('label139', 'label138');" onmouseover="ContentPreview('label139');" onmouseout="ContentUnpreview('label139');" title="click to collapse or expand..."> more... </a>
 <div id="label139" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">sctp_csum_err</span> <b>(Alias name: sctp-csum-err)</b>  Invalid ipv4 sctp checksum anomalies. <span class="li-normal">type: str</span> <span class="li-normal">choices: [allow, drop, trap-to-host]</span> 
 <a id='label140' href="javascript:ContentClick('label141', 'label140');" onmouseover="ContentPreview('label141');" onmouseout="ContentUnpreview('label141');" title="click to collapse or expand..."> more... </a>
 <div id="label141" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.5 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">gtp_enhanced_cpu_range</span> <b>(Alias name: gtp-enhanced-cpu-range)</b>  Gtp enhanced cpu range option. <span class="li-normal">type: str</span> <span class="li-normal">choices: [0, 1, 2]</span> 
 <a id='label142' href="javascript:ContentClick('label143', 'label142');" onmouseover="ContentPreview('label143');" onmouseout="ContentUnpreview('label143');" title="click to collapse or expand..."> more... </a>
 <div id="label143" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gtp_enhanced_mode</span> <b>(Alias name: gtp-enhanced-mode)</b>  Enable/disable gtp enhanced mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label144' href="javascript:ContentClick('label145', 'label144');" onmouseover="ContentPreview('label145');" onmouseout="ContentUnpreview('label145');" title="click to collapse or expand..."> more... </a>
 <div id="label145" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">host_shortcut_mode</span> <b>(Alias name: host-shortcut-mode)</b>  Set np6 host shortcut mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [bi-directional, host-shortcut]</span> 
 <a id='label146' href="javascript:ContentClick('label147', 'label146');" onmouseover="ContentPreview('label147');" onmouseout="ContentUnpreview('label147');" title="click to collapse or expand..."> more... </a>
 <div id="label147" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">htx_gtse_quota</span> <b>(Alias name: htx-gtse-quota)</b>  Configure htx gtse quota. <span class="li-normal">type: str</span> <span class="li-normal">choices: [100Mbps, 200Mbps, 300Mbps, 400Mbps, 500Mbps, 600Mbps, 700Mbps, 800Mbps, 900Mbps, 1Gbps, 2Gbps, 4Gbps, 8Gbps, 10Gbps]</span> 
 <a id='label148' href="javascript:ContentClick('label149', 'label148');" onmouseover="ContentPreview('label149');" onmouseout="ContentUnpreview('label149');" title="click to collapse or expand..."> more... </a>
 <div id="label149" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">intf_shaping_offload</span> <b>(Alias name: intf-shaping-offload)</b>  Enable/disable npu offload when doing interface-based traffic shaping according to the egress-shaping-profile. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label150' href="javascript:ContentClick('label151', 'label150');" onmouseover="ContentPreview('label151');" onmouseout="ContentUnpreview('label151');" title="click to collapse or expand..."> more... </a>
 <div id="label151" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">iph_rsvd_re_cksum</span> <b>(Alias name: iph-rsvd-re-cksum)</b>  Enable/disable ip checksum re-calculation for packets with iph. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label152' href="javascript:ContentClick('label153', 'label152');" onmouseover="ContentPreview('label153');" onmouseout="ContentUnpreview('label153');" title="click to collapse or expand..."> more... </a>
 <div id="label153" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_dec_subengine_mask</span> <b>(Alias name: ipsec-dec-subengine-mask)</b>  Ipsec decryption subengine mask (0x1 - 0xff, default 0xff). <span class="li-normal">type: str</span>
 <a id='label154' href="javascript:ContentClick('label155', 'label154');" onmouseover="ContentPreview('label155');" onmouseout="ContentUnpreview('label155');" title="click to collapse or expand..."> more... </a>
 <div id="label155" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_enc_subengine_mask</span> <b>(Alias name: ipsec-enc-subengine-mask)</b>  Ipsec encryption subengine mask (0x1 - 0xff, default 0xff). <span class="li-normal">type: str</span>
 <a id='label156' href="javascript:ContentClick('label157', 'label156');" onmouseover="ContentPreview('label157');" onmouseout="ContentUnpreview('label157');" title="click to collapse or expand..."> more... </a>
 <div id="label157" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_inbound_cache</span> <b>(Alias name: ipsec-inbound-cache)</b>  Enable/disable ipsec inbound cache for anti-replay. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label158' href="javascript:ContentClick('label159', 'label158');" onmouseover="ContentPreview('label159');" onmouseout="ContentUnpreview('label159');" title="click to collapse or expand..."> more... </a>
 <div id="label159" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_mtu_override</span> <b>(Alias name: ipsec-mtu-override)</b>  Enable/disable np6 ipsec mtu override. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label160' href="javascript:ContentClick('label161', 'label160');" onmouseover="ContentPreview('label161');" onmouseout="ContentUnpreview('label161');" title="click to collapse or expand..."> more... </a>
 <div id="label161" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_over_vlink</span> <b>(Alias name: ipsec-over-vlink)</b>  Enable/disable ipsec over vlink. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label162' href="javascript:ContentClick('label163', 'label162');" onmouseover="ContentPreview('label163');" onmouseout="ContentUnpreview('label163');" title="click to collapse or expand..."> more... </a>
 <div id="label163" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">isf_np_queues</span> <b>(Alias name: isf-np-queues)</b>  Isf np queues. <span class="li-normal">type: dict</span>
 <a id='label164' href="javascript:ContentClick('label165', 'label164');" onmouseover="ContentPreview('label165');" onmouseout="ContentUnpreview('label165');" title="click to collapse or expand..."> more... </a>
 <div id="label165" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">cos0</span> Cos profile name for cos 0. <span class="li-normal">type: str</span>
 <a id='label166' href="javascript:ContentClick('label167', 'label166');" onmouseover="ContentPreview('label167');" onmouseout="ContentUnpreview('label167');" title="click to collapse or expand..."> more... </a>
 <div id="label167" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos1</span> Cos profile name for cos 1. <span class="li-normal">type: str</span>
 <a id='label168' href="javascript:ContentClick('label169', 'label168');" onmouseover="ContentPreview('label169');" onmouseout="ContentUnpreview('label169');" title="click to collapse or expand..."> more... </a>
 <div id="label169" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos2</span> Cos profile name for cos 2. <span class="li-normal">type: str</span>
 <a id='label170' href="javascript:ContentClick('label171', 'label170');" onmouseover="ContentPreview('label171');" onmouseout="ContentUnpreview('label171');" title="click to collapse or expand..."> more... </a>
 <div id="label171" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos3</span> Cos profile name for cos 3. <span class="li-normal">type: str</span>
 <a id='label172' href="javascript:ContentClick('label173', 'label172');" onmouseover="ContentPreview('label173');" onmouseout="ContentUnpreview('label173');" title="click to collapse or expand..."> more... </a>
 <div id="label173" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos4</span> Cos profile name for cos 4. <span class="li-normal">type: str</span>
 <a id='label174' href="javascript:ContentClick('label175', 'label174');" onmouseover="ContentPreview('label175');" onmouseout="ContentUnpreview('label175');" title="click to collapse or expand..."> more... </a>
 <div id="label175" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos5</span> Cos profile name for cos 5. <span class="li-normal">type: str</span>
 <a id='label176' href="javascript:ContentClick('label177', 'label176');" onmouseover="ContentPreview('label177');" onmouseout="ContentUnpreview('label177');" title="click to collapse or expand..."> more... </a>
 <div id="label177" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos6</span> Cos profile name for cos 6. <span class="li-normal">type: str</span>
 <a id='label178' href="javascript:ContentClick('label179', 'label178');" onmouseover="ContentPreview('label179');" onmouseout="ContentUnpreview('label179');" title="click to collapse or expand..."> more... </a>
 <div id="label179" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos7</span> Cos profile name for cos 7. <span class="li-normal">type: str</span>
 <a id='label180' href="javascript:ContentClick('label181', 'label180');" onmouseover="ContentPreview('label181');" onmouseout="ContentUnpreview('label181');" title="click to collapse or expand..."> more... </a>
 <div id="label181" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">lag_out_port_select</span> <b>(Alias name: lag-out-port-select)</b>  Enable/disable lag outgoing port selection based on incoming traffic port. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label182' href="javascript:ContentClick('label183', 'label182');" onmouseover="ContentPreview('label183');" onmouseout="ContentUnpreview('label183');" title="click to collapse or expand..."> more... </a>
 <div id="label183" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mcast_session_accounting</span> <b>(Alias name: mcast-session-accounting)</b>  Enable/disable traffic accounting for each multicast session through tae counter. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, session-based, tpe-based]</span> 
 <a id='label184' href="javascript:ContentClick('label185', 'label184');" onmouseover="ContentPreview('label185');" onmouseout="ContentUnpreview('label185');" title="click to collapse or expand..."> more... </a>
 <div id="label185" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">np6_cps_optimization_mode</span> <b>(Alias name: np6-cps-optimization-mode)</b>  Enable/disable np6 connection per second (cps) optimization mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label186' href="javascript:ContentClick('label187', 'label186');" onmouseover="ContentPreview('label187');" onmouseout="ContentUnpreview('label187');" title="click to collapse or expand..."> more... </a>
 <div id="label187" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">per_session_accounting</span> <b>(Alias name: per-session-accounting)</b>  Enable/disable per-session accounting. <span class="li-normal">type: str</span> <span class="li-normal">choices: [enable, disable, enable-by-log, all-enable, traffic-log-only]</span> 
 <a id='label188' href="javascript:ContentClick('label189', 'label188');" onmouseover="ContentPreview('label189');" onmouseout="ContentUnpreview('label189');" title="click to collapse or expand..."> more... </a>
 <div id="label189" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port_cpu_map</span> <b>(Alias name: port-cpu-map)</b>  Port cpu map. <span class="li-normal">type: list</span>
 <a id='label190' href="javascript:ContentClick('label191', 'label190');" onmouseover="ContentPreview('label191');" onmouseout="ContentUnpreview('label191');" title="click to collapse or expand..."> more... </a>
 <div id="label191" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">cpu_core</span> <b>(Alias name: cpu-core)</b>  The cpu core to map to an interface. <span class="li-normal">type: str</span>
 <a id='label192' href="javascript:ContentClick('label193', 'label192');" onmouseover="ContentPreview('label193');" onmouseout="ContentUnpreview('label193');" title="click to collapse or expand..."> more... </a>
 <div id="label193" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">interface</span> The interface to map to a cpu core. <span class="li-normal">type: str</span>
 <a id='label194' href="javascript:ContentClick('label195', 'label194');" onmouseover="ContentPreview('label195');" onmouseout="ContentUnpreview('label195');" title="click to collapse or expand..."> more... </a>
 <div id="label195" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">port_npu_map</span> <b>(Alias name: port-npu-map)</b>  Port npu map. <span class="li-normal">type: list</span>
 <a id='label196' href="javascript:ContentClick('label197', 'label196');" onmouseover="ContentPreview('label197');" onmouseout="ContentUnpreview('label197');" title="click to collapse or expand..."> more... </a>
 <div id="label197" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">interface</span> Set npu interface port to npu group map. <span class="li-normal">type: str</span>
 <a id='label198' href="javascript:ContentClick('label199', 'label198');" onmouseover="ContentPreview('label199');" onmouseout="ContentUnpreview('label199');" title="click to collapse or expand..."> more... </a>
 <div id="label199" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">npu_group_index</span> <b>(Alias name: npu-group-index)</b>  Mapping npu group index. <span class="li-normal">type: int</span>
 <a id='label200' href="javascript:ContentClick('label201', 'label200');" onmouseover="ContentPreview('label201');" onmouseout="ContentUnpreview('label201');" title="click to collapse or expand..."> more... </a>
 <div id="label201" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">priority_protocol</span> <b>(Alias name: priority-protocol)</b>  Priority protocol. <span class="li-normal">type: dict</span>
 <a id='label202' href="javascript:ContentClick('label203', 'label202');" onmouseover="ContentPreview('label203');" onmouseout="ContentUnpreview('label203');" title="click to collapse or expand..."> more... </a>
 <div id="label203" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">bfd</span> Enable/disable npu bfd priority protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label204' href="javascript:ContentClick('label205', 'label204');" onmouseover="ContentPreview('label205');" onmouseout="ContentUnpreview('label205');" title="click to collapse or expand..."> more... </a>
 <div id="label205" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bgp</span> Enable/disable npu bgp priority protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label206' href="javascript:ContentClick('label207', 'label206');" onmouseover="ContentPreview('label207');" onmouseout="ContentUnpreview('label207');" title="click to collapse or expand..."> more... </a>
 <div id="label207" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">slbc</span> Enable/disable npu slbc priority protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label208' href="javascript:ContentClick('label209', 'label208');" onmouseover="ContentPreview('label209');" onmouseout="ContentUnpreview('label209');" title="click to collapse or expand..."> more... </a>
 <div id="label209" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">qos_mode</span> <b>(Alias name: qos-mode)</b>  Qos mode on switch and np. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, priority, round-robin]</span> 
 <a id='label210' href="javascript:ContentClick('label211', 'label210');" onmouseover="ContentPreview('label211');" onmouseout="ContentUnpreview('label211');" title="click to collapse or expand..."> more... </a>
 <div id="label211" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rdp_offload</span> <b>(Alias name: rdp-offload)</b>  Enable/disable rdp offload. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label212' href="javascript:ContentClick('label213', 'label212');" onmouseover="ContentPreview('label213');" onmouseout="ContentUnpreview('label213');" title="click to collapse or expand..."> more... </a>
 <div id="label213" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">recover_np6_link</span> <b>(Alias name: recover-np6-link)</b>  Enable/disable internal link failure check and recovery after boot up. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label214' href="javascript:ContentClick('label215', 'label214');" onmouseover="ContentPreview('label215');" onmouseout="ContentUnpreview('label215');" title="click to collapse or expand..."> more... </a>
 <div id="label215" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">session_denied_offload</span> <b>(Alias name: session-denied-offload)</b>  Enable/disable offloading of denied sessions. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label216' href="javascript:ContentClick('label217', 'label216');" onmouseover="ContentPreview('label217');" onmouseout="ContentUnpreview('label217');" title="click to collapse or expand..."> more... </a>
 <div id="label217" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sse_backpressure</span> <b>(Alias name: sse-backpressure)</b>  Enable/disable sse backpressure. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label218' href="javascript:ContentClick('label219', 'label218');" onmouseover="ContentPreview('label219');" onmouseout="ContentUnpreview('label219');" title="click to collapse or expand..."> more... </a>
 <div id="label219" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">strip_clear_text_padding</span> <b>(Alias name: strip-clear-text-padding)</b>  Enable/disable stripping clear text padding. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label220' href="javascript:ContentClick('label221', 'label220');" onmouseover="ContentPreview('label221');" onmouseout="ContentUnpreview('label221');" title="click to collapse or expand..."> more... </a>
 <div id="label221" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">strip_esp_padding</span> <b>(Alias name: strip-esp-padding)</b>  Enable/disable stripping esp padding. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label222' href="javascript:ContentClick('label223', 'label222');" onmouseover="ContentPreview('label223');" onmouseout="ContentUnpreview('label223');" title="click to collapse or expand..."> more... </a>
 <div id="label223" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sw_eh_hash</span> <b>(Alias name: sw-eh-hash)</b>  Sw eh hash. <span class="li-normal">type: dict</span>
 <a id='label224' href="javascript:ContentClick('label225', 'label224');" onmouseover="ContentPreview('label225');" onmouseout="ContentUnpreview('label225');" title="click to collapse or expand..."> more... </a>
 <div id="label225" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">computation</span> Set hashing computation. <span class="li-normal">type: str</span> <span class="li-normal">choices: [xor16, xor8, xor4, crc16]</span> 
 <a id='label226' href="javascript:ContentClick('label227', 'label226');" onmouseover="ContentPreview('label227');" onmouseout="ContentUnpreview('label227');" title="click to collapse or expand..."> more... </a>
 <div id="label227" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">destination_ip_lower_16</span> <b>(Alias name: destination-ip-lower-16)</b>  Include/exclude destination ip address lower 16 bits. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label228' href="javascript:ContentClick('label229', 'label228');" onmouseover="ContentPreview('label229');" onmouseout="ContentUnpreview('label229');" title="click to collapse or expand..."> more... </a>
 <div id="label229" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">destination_ip_upper_16</span> <b>(Alias name: destination-ip-upper-16)</b>  Include/exclude destination ip address upper 16 bits. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label230' href="javascript:ContentClick('label231', 'label230');" onmouseover="ContentPreview('label231');" onmouseout="ContentUnpreview('label231');" title="click to collapse or expand..."> more... </a>
 <div id="label231" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">destination_port</span> <b>(Alias name: destination-port)</b>  Include/exclude destination port if tcp/udp. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label232' href="javascript:ContentClick('label233', 'label232');" onmouseover="ContentPreview('label233');" onmouseout="ContentUnpreview('label233');" title="click to collapse or expand..."> more... </a>
 <div id="label233" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip_protocol</span> <b>(Alias name: ip-protocol)</b>  Include/exclude ip protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label234' href="javascript:ContentClick('label235', 'label234');" onmouseover="ContentPreview('label235');" onmouseout="ContentUnpreview('label235');" title="click to collapse or expand..."> more... </a>
 <div id="label235" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">netmask_length</span> <b>(Alias name: netmask-length)</b>  Network mask length. <span class="li-normal">type: int</span>
 <a id='label236' href="javascript:ContentClick('label237', 'label236');" onmouseover="ContentPreview('label237');" onmouseout="ContentUnpreview('label237');" title="click to collapse or expand..."> more... </a>
 <div id="label237" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">source_ip_lower_16</span> <b>(Alias name: source-ip-lower-16)</b>  Include/exclude source ip address lower 16 bits. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label238' href="javascript:ContentClick('label239', 'label238');" onmouseover="ContentPreview('label239');" onmouseout="ContentUnpreview('label239');" title="click to collapse or expand..."> more... </a>
 <div id="label239" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">source_ip_upper_16</span> <b>(Alias name: source-ip-upper-16)</b>  Include/exclude source ip address upper 16 bits. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label240' href="javascript:ContentClick('label241', 'label240');" onmouseover="ContentPreview('label241');" onmouseout="ContentUnpreview('label241');" title="click to collapse or expand..."> more... </a>
 <div id="label241" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">source_port</span> <b>(Alias name: source-port)</b>  Include/exclude source port if tcp/udp. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label242' href="javascript:ContentClick('label243', 'label242');" onmouseover="ContentPreview('label243');" onmouseout="ContentUnpreview('label243');" title="click to collapse or expand..."> more... </a>
 <div id="label243" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">sw_np_bandwidth</span> <b>(Alias name: sw-np-bandwidth)</b>  Bandwidth from switch to np. <span class="li-normal">type: str</span> <span class="li-normal">choices: [0G, 2G, 4G, 5G, 6G, 7G, 8G, 9G]</span> 
 <a id='label244' href="javascript:ContentClick('label245', 'label244');" onmouseover="ContentPreview('label245');" onmouseout="ContentUnpreview('label245');" title="click to collapse or expand..."> more... </a>
 <div id="label245" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">switch_np_hash</span> <b>(Alias name: switch-np-hash)</b>  Switch-np trunk port selection criteria. <span class="li-normal">type: str</span> <span class="li-normal">choices: [src-ip, dst-ip, src-dst-ip]</span> 
 <a id='label246' href="javascript:ContentClick('label247', 'label246');" onmouseover="ContentPreview('label247');" onmouseout="ContentUnpreview('label247');" title="click to collapse or expand..."> more... </a>
 <div id="label247" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">uesp_offload</span> <b>(Alias name: uesp-offload)</b>  Enable/disable udp-encapsulated esp offload (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label248' href="javascript:ContentClick('label249', 'label248');" onmouseover="ContentPreview('label249');" onmouseout="ContentUnpreview('label249');" title="click to collapse or expand..."> more... </a>
 <div id="label249" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">np_queues</span> <b>(Alias name: np-queues)</b>  Np queues. <span class="li-normal">type: dict</span>
 <a id='label250' href="javascript:ContentClick('label251', 'label250');" onmouseover="ContentPreview('label251');" onmouseout="ContentUnpreview('label251');" title="click to collapse or expand..."> more... </a>
 <div id="label251" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">ethernet_type</span> <b>(Alias name: ethernet-type)</b>  Ethernet type. <span class="li-normal">type: list</span>
 <a id='label252' href="javascript:ContentClick('label253', 'label252');" onmouseover="ContentPreview('label253');" onmouseout="ContentUnpreview('label253');" title="click to collapse or expand..."> more... </a>
 <div id="label253" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">name</span> Ethernet type name. <span class="li-normal">type: str</span>
 <a id='label254' href="javascript:ContentClick('label255', 'label254');" onmouseover="ContentPreview('label255');" onmouseout="ContentUnpreview('label255');" title="click to collapse or expand..."> more... </a>
 <div id="label255" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">queue</span> Queue number. <span class="li-normal">type: int</span>
 <a id='label256' href="javascript:ContentClick('label257', 'label256');" onmouseover="ContentPreview('label257');" onmouseout="ContentUnpreview('label257');" title="click to collapse or expand..."> more... </a>
 <div id="label257" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">type</span> Ethernet type. <span class="li-normal">type: int</span>
 <a id='label258' href="javascript:ContentClick('label259', 'label258');" onmouseover="ContentPreview('label259');" onmouseout="ContentUnpreview('label259');" title="click to collapse or expand..."> more... </a>
 <div id="label259" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">weight</span> Class weight. <span class="li-normal">type: int</span>
 <a id='label260' href="javascript:ContentClick('label261', 'label260');" onmouseover="ContentPreview('label261');" onmouseout="ContentUnpreview('label261');" title="click to collapse or expand..."> more... </a>
 <div id="label261" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">ip_protocol</span> <b>(Alias name: ip-protocol)</b>  Ip protocol. <span class="li-normal">type: list</span>
 <a id='label262' href="javascript:ContentClick('label263', 'label262');" onmouseover="ContentPreview('label263');" onmouseout="ContentUnpreview('label263');" title="click to collapse or expand..."> more... </a>
 <div id="label263" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">name</span> Ip protocol name. <span class="li-normal">type: str</span>
 <a id='label264' href="javascript:ContentClick('label265', 'label264');" onmouseover="ContentPreview('label265');" onmouseout="ContentUnpreview('label265');" title="click to collapse or expand..."> more... </a>
 <div id="label265" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protocol</span> Ip protocol. <span class="li-normal">type: int</span>
 <a id='label266' href="javascript:ContentClick('label267', 'label266');" onmouseover="ContentPreview('label267');" onmouseout="ContentUnpreview('label267');" title="click to collapse or expand..."> more... </a>
 <div id="label267" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">queue</span> Queue number. <span class="li-normal">type: int</span>
 <a id='label268' href="javascript:ContentClick('label269', 'label268');" onmouseover="ContentPreview('label269');" onmouseout="ContentUnpreview('label269');" title="click to collapse or expand..."> more... </a>
 <div id="label269" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">weight</span> Class weight. <span class="li-normal">type: int</span>
 <a id='label270' href="javascript:ContentClick('label271', 'label270');" onmouseover="ContentPreview('label271');" onmouseout="ContentUnpreview('label271');" title="click to collapse or expand..."> more... </a>
 <div id="label271" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">ip_service</span> <b>(Alias name: ip-service)</b>  Ip service. <span class="li-normal">type: list</span>
 <a id='label272' href="javascript:ContentClick('label273', 'label272');" onmouseover="ContentPreview('label273');" onmouseout="ContentUnpreview('label273');" title="click to collapse or expand..."> more... </a>
 <div id="label273" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">dport</span> Destination port. <span class="li-normal">type: int</span>
 <a id='label274' href="javascript:ContentClick('label275', 'label274');" onmouseover="ContentPreview('label275');" onmouseout="ContentUnpreview('label275');" title="click to collapse or expand..."> more... </a>
 <div id="label275" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">name</span> Ip service name. <span class="li-normal">type: str</span>
 <a id='label276' href="javascript:ContentClick('label277', 'label276');" onmouseover="ContentPreview('label277');" onmouseout="ContentUnpreview('label277');" title="click to collapse or expand..."> more... </a>
 <div id="label277" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protocol</span> Ip protocol. <span class="li-normal">type: int</span>
 <a id='label278' href="javascript:ContentClick('label279', 'label278');" onmouseover="ContentPreview('label279');" onmouseout="ContentUnpreview('label279');" title="click to collapse or expand..."> more... </a>
 <div id="label279" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">queue</span> Queue number. <span class="li-normal">type: int</span>
 <a id='label280' href="javascript:ContentClick('label281', 'label280');" onmouseover="ContentPreview('label281');" onmouseout="ContentUnpreview('label281');" title="click to collapse or expand..."> more... </a>
 <div id="label281" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sport</span> Source port. <span class="li-normal">type: int</span>
 <a id='label282' href="javascript:ContentClick('label283', 'label282');" onmouseover="ContentPreview('label283');" onmouseout="ContentUnpreview('label283');" title="click to collapse or expand..."> more... </a>
 <div id="label283" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">weight</span> Class weight. <span class="li-normal">type: int</span>
 <a id='label284' href="javascript:ContentClick('label285', 'label284');" onmouseover="ContentPreview('label285');" onmouseout="ContentUnpreview('label285');" title="click to collapse or expand..."> more... </a>
 <div id="label285" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">profile</span> Profile. <span class="li-normal">type: list</span>
 <a id='label286' href="javascript:ContentClick('label287', 'label286');" onmouseover="ContentPreview('label287');" onmouseout="ContentUnpreview('label287');" title="click to collapse or expand..."> more... </a>
 <div id="label287" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">cos0</span> Queue number of cos 0. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label288' href="javascript:ContentClick('label289', 'label288');" onmouseover="ContentPreview('label289');" onmouseout="ContentUnpreview('label289');" title="click to collapse or expand..."> more... </a>
 <div id="label289" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos1</span> Queue number of cos 1. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label290' href="javascript:ContentClick('label291', 'label290');" onmouseover="ContentPreview('label291');" onmouseout="ContentUnpreview('label291');" title="click to collapse or expand..."> more... </a>
 <div id="label291" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos2</span> Queue number of cos 2. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label292' href="javascript:ContentClick('label293', 'label292');" onmouseover="ContentPreview('label293');" onmouseout="ContentUnpreview('label293');" title="click to collapse or expand..."> more... </a>
 <div id="label293" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos3</span> Queue number of cos 3. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label294' href="javascript:ContentClick('label295', 'label294');" onmouseover="ContentPreview('label295');" onmouseout="ContentUnpreview('label295');" title="click to collapse or expand..."> more... </a>
 <div id="label295" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos4</span> Queue number of cos 4. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label296' href="javascript:ContentClick('label297', 'label296');" onmouseover="ContentPreview('label297');" onmouseout="ContentUnpreview('label297');" title="click to collapse or expand..."> more... </a>
 <div id="label297" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos5</span> Queue number of cos 5. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label298' href="javascript:ContentClick('label299', 'label298');" onmouseover="ContentPreview('label299');" onmouseout="ContentUnpreview('label299');" title="click to collapse or expand..."> more... </a>
 <div id="label299" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos6</span> Queue number of cos 6. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label300' href="javascript:ContentClick('label301', 'label300');" onmouseover="ContentPreview('label301');" onmouseout="ContentUnpreview('label301');" title="click to collapse or expand..."> more... </a>
 <div id="label301" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">cos7</span> Queue number of cos 7. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label302' href="javascript:ContentClick('label303', 'label302');" onmouseover="ContentPreview('label303');" onmouseout="ContentUnpreview('label303');" title="click to collapse or expand..."> more... </a>
 <div id="label303" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp0</span> Queue number of dscp 0. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label304' href="javascript:ContentClick('label305', 'label304');" onmouseover="ContentPreview('label305');" onmouseout="ContentUnpreview('label305');" title="click to collapse or expand..."> more... </a>
 <div id="label305" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp1</span> Queue number of dscp 1. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label306' href="javascript:ContentClick('label307', 'label306');" onmouseover="ContentPreview('label307');" onmouseout="ContentUnpreview('label307');" title="click to collapse or expand..."> more... </a>
 <div id="label307" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp10</span> Queue number of dscp 10. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label308' href="javascript:ContentClick('label309', 'label308');" onmouseover="ContentPreview('label309');" onmouseout="ContentUnpreview('label309');" title="click to collapse or expand..."> more... </a>
 <div id="label309" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp11</span> Queue number of dscp 11. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label310' href="javascript:ContentClick('label311', 'label310');" onmouseover="ContentPreview('label311');" onmouseout="ContentUnpreview('label311');" title="click to collapse or expand..."> more... </a>
 <div id="label311" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp12</span> Queue number of dscp 12. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label312' href="javascript:ContentClick('label313', 'label312');" onmouseover="ContentPreview('label313');" onmouseout="ContentUnpreview('label313');" title="click to collapse or expand..."> more... </a>
 <div id="label313" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp13</span> Queue number of dscp 13. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label314' href="javascript:ContentClick('label315', 'label314');" onmouseover="ContentPreview('label315');" onmouseout="ContentUnpreview('label315');" title="click to collapse or expand..."> more... </a>
 <div id="label315" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp14</span> Queue number of dscp 14. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label316' href="javascript:ContentClick('label317', 'label316');" onmouseover="ContentPreview('label317');" onmouseout="ContentUnpreview('label317');" title="click to collapse or expand..."> more... </a>
 <div id="label317" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp15</span> Queue number of dscp 15. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label318' href="javascript:ContentClick('label319', 'label318');" onmouseover="ContentPreview('label319');" onmouseout="ContentUnpreview('label319');" title="click to collapse or expand..."> more... </a>
 <div id="label319" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp16</span> Queue number of dscp 16. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label320' href="javascript:ContentClick('label321', 'label320');" onmouseover="ContentPreview('label321');" onmouseout="ContentUnpreview('label321');" title="click to collapse or expand..."> more... </a>
 <div id="label321" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp17</span> Queue number of dscp 17. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label322' href="javascript:ContentClick('label323', 'label322');" onmouseover="ContentPreview('label323');" onmouseout="ContentUnpreview('label323');" title="click to collapse or expand..."> more... </a>
 <div id="label323" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp18</span> Queue number of dscp 18. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label324' href="javascript:ContentClick('label325', 'label324');" onmouseover="ContentPreview('label325');" onmouseout="ContentUnpreview('label325');" title="click to collapse or expand..."> more... </a>
 <div id="label325" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp19</span> Queue number of dscp 19. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label326' href="javascript:ContentClick('label327', 'label326');" onmouseover="ContentPreview('label327');" onmouseout="ContentUnpreview('label327');" title="click to collapse or expand..."> more... </a>
 <div id="label327" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp2</span> Queue number of dscp 2. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label328' href="javascript:ContentClick('label329', 'label328');" onmouseover="ContentPreview('label329');" onmouseout="ContentUnpreview('label329');" title="click to collapse or expand..."> more... </a>
 <div id="label329" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp20</span> Queue number of dscp 20. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label330' href="javascript:ContentClick('label331', 'label330');" onmouseover="ContentPreview('label331');" onmouseout="ContentUnpreview('label331');" title="click to collapse or expand..."> more... </a>
 <div id="label331" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp21</span> Queue number of dscp 21. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label332' href="javascript:ContentClick('label333', 'label332');" onmouseover="ContentPreview('label333');" onmouseout="ContentUnpreview('label333');" title="click to collapse or expand..."> more... </a>
 <div id="label333" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp22</span> Queue number of dscp 22. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label334' href="javascript:ContentClick('label335', 'label334');" onmouseover="ContentPreview('label335');" onmouseout="ContentUnpreview('label335');" title="click to collapse or expand..."> more... </a>
 <div id="label335" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp23</span> Queue number of dscp 23. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label336' href="javascript:ContentClick('label337', 'label336');" onmouseover="ContentPreview('label337');" onmouseout="ContentUnpreview('label337');" title="click to collapse or expand..."> more... </a>
 <div id="label337" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp24</span> Queue number of dscp 24. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label338' href="javascript:ContentClick('label339', 'label338');" onmouseover="ContentPreview('label339');" onmouseout="ContentUnpreview('label339');" title="click to collapse or expand..."> more... </a>
 <div id="label339" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp25</span> Queue number of dscp 25. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label340' href="javascript:ContentClick('label341', 'label340');" onmouseover="ContentPreview('label341');" onmouseout="ContentUnpreview('label341');" title="click to collapse or expand..."> more... </a>
 <div id="label341" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp26</span> Queue number of dscp 26. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label342' href="javascript:ContentClick('label343', 'label342');" onmouseover="ContentPreview('label343');" onmouseout="ContentUnpreview('label343');" title="click to collapse or expand..."> more... </a>
 <div id="label343" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp27</span> Queue number of dscp 27. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label344' href="javascript:ContentClick('label345', 'label344');" onmouseover="ContentPreview('label345');" onmouseout="ContentUnpreview('label345');" title="click to collapse or expand..."> more... </a>
 <div id="label345" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp28</span> Queue number of dscp 28. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label346' href="javascript:ContentClick('label347', 'label346');" onmouseover="ContentPreview('label347');" onmouseout="ContentUnpreview('label347');" title="click to collapse or expand..."> more... </a>
 <div id="label347" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp29</span> Queue number of dscp 29. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label348' href="javascript:ContentClick('label349', 'label348');" onmouseover="ContentPreview('label349');" onmouseout="ContentUnpreview('label349');" title="click to collapse or expand..."> more... </a>
 <div id="label349" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp3</span> Queue number of dscp 3. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label350' href="javascript:ContentClick('label351', 'label350');" onmouseover="ContentPreview('label351');" onmouseout="ContentUnpreview('label351');" title="click to collapse or expand..."> more... </a>
 <div id="label351" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp30</span> Queue number of dscp 30. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label352' href="javascript:ContentClick('label353', 'label352');" onmouseover="ContentPreview('label353');" onmouseout="ContentUnpreview('label353');" title="click to collapse or expand..."> more... </a>
 <div id="label353" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp31</span> Queue number of dscp 31. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label354' href="javascript:ContentClick('label355', 'label354');" onmouseover="ContentPreview('label355');" onmouseout="ContentUnpreview('label355');" title="click to collapse or expand..."> more... </a>
 <div id="label355" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp32</span> Queue number of dscp 32. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label356' href="javascript:ContentClick('label357', 'label356');" onmouseover="ContentPreview('label357');" onmouseout="ContentUnpreview('label357');" title="click to collapse or expand..."> more... </a>
 <div id="label357" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp33</span> Queue number of dscp 33. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label358' href="javascript:ContentClick('label359', 'label358');" onmouseover="ContentPreview('label359');" onmouseout="ContentUnpreview('label359');" title="click to collapse or expand..."> more... </a>
 <div id="label359" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp34</span> Queue number of dscp 34. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label360' href="javascript:ContentClick('label361', 'label360');" onmouseover="ContentPreview('label361');" onmouseout="ContentUnpreview('label361');" title="click to collapse or expand..."> more... </a>
 <div id="label361" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp35</span> Queue number of dscp 35. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label362' href="javascript:ContentClick('label363', 'label362');" onmouseover="ContentPreview('label363');" onmouseout="ContentUnpreview('label363');" title="click to collapse or expand..."> more... </a>
 <div id="label363" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp36</span> Queue number of dscp 36. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label364' href="javascript:ContentClick('label365', 'label364');" onmouseover="ContentPreview('label365');" onmouseout="ContentUnpreview('label365');" title="click to collapse or expand..."> more... </a>
 <div id="label365" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp37</span> Queue number of dscp 37. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label366' href="javascript:ContentClick('label367', 'label366');" onmouseover="ContentPreview('label367');" onmouseout="ContentUnpreview('label367');" title="click to collapse or expand..."> more... </a>
 <div id="label367" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp38</span> Queue number of dscp 38. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label368' href="javascript:ContentClick('label369', 'label368');" onmouseover="ContentPreview('label369');" onmouseout="ContentUnpreview('label369');" title="click to collapse or expand..."> more... </a>
 <div id="label369" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp39</span> Queue number of dscp 39. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label370' href="javascript:ContentClick('label371', 'label370');" onmouseover="ContentPreview('label371');" onmouseout="ContentUnpreview('label371');" title="click to collapse or expand..."> more... </a>
 <div id="label371" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp4</span> Queue number of dscp 4. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label372' href="javascript:ContentClick('label373', 'label372');" onmouseover="ContentPreview('label373');" onmouseout="ContentUnpreview('label373');" title="click to collapse or expand..."> more... </a>
 <div id="label373" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp40</span> Queue number of dscp 40. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label374' href="javascript:ContentClick('label375', 'label374');" onmouseover="ContentPreview('label375');" onmouseout="ContentUnpreview('label375');" title="click to collapse or expand..."> more... </a>
 <div id="label375" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp41</span> Queue number of dscp 41. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label376' href="javascript:ContentClick('label377', 'label376');" onmouseover="ContentPreview('label377');" onmouseout="ContentUnpreview('label377');" title="click to collapse or expand..."> more... </a>
 <div id="label377" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp42</span> Queue number of dscp 42. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label378' href="javascript:ContentClick('label379', 'label378');" onmouseover="ContentPreview('label379');" onmouseout="ContentUnpreview('label379');" title="click to collapse or expand..."> more... </a>
 <div id="label379" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp43</span> Queue number of dscp 43. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label380' href="javascript:ContentClick('label381', 'label380');" onmouseover="ContentPreview('label381');" onmouseout="ContentUnpreview('label381');" title="click to collapse or expand..."> more... </a>
 <div id="label381" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp44</span> Queue number of dscp 44. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label382' href="javascript:ContentClick('label383', 'label382');" onmouseover="ContentPreview('label383');" onmouseout="ContentUnpreview('label383');" title="click to collapse or expand..."> more... </a>
 <div id="label383" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp45</span> Queue number of dscp 45. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label384' href="javascript:ContentClick('label385', 'label384');" onmouseover="ContentPreview('label385');" onmouseout="ContentUnpreview('label385');" title="click to collapse or expand..."> more... </a>
 <div id="label385" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp46</span> Queue number of dscp 46. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label386' href="javascript:ContentClick('label387', 'label386');" onmouseover="ContentPreview('label387');" onmouseout="ContentUnpreview('label387');" title="click to collapse or expand..."> more... </a>
 <div id="label387" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp47</span> Queue number of dscp 47. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label388' href="javascript:ContentClick('label389', 'label388');" onmouseover="ContentPreview('label389');" onmouseout="ContentUnpreview('label389');" title="click to collapse or expand..."> more... </a>
 <div id="label389" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp48</span> Queue number of dscp 48. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label390' href="javascript:ContentClick('label391', 'label390');" onmouseover="ContentPreview('label391');" onmouseout="ContentUnpreview('label391');" title="click to collapse or expand..."> more... </a>
 <div id="label391" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp49</span> Queue number of dscp 49. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label392' href="javascript:ContentClick('label393', 'label392');" onmouseover="ContentPreview('label393');" onmouseout="ContentUnpreview('label393');" title="click to collapse or expand..."> more... </a>
 <div id="label393" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp5</span> Queue number of dscp 5. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label394' href="javascript:ContentClick('label395', 'label394');" onmouseover="ContentPreview('label395');" onmouseout="ContentUnpreview('label395');" title="click to collapse or expand..."> more... </a>
 <div id="label395" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp50</span> Queue number of dscp 50. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label396' href="javascript:ContentClick('label397', 'label396');" onmouseover="ContentPreview('label397');" onmouseout="ContentUnpreview('label397');" title="click to collapse or expand..."> more... </a>
 <div id="label397" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp51</span> Queue number of dscp 51. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label398' href="javascript:ContentClick('label399', 'label398');" onmouseover="ContentPreview('label399');" onmouseout="ContentUnpreview('label399');" title="click to collapse or expand..."> more... </a>
 <div id="label399" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp52</span> Queue number of dscp 52. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label400' href="javascript:ContentClick('label401', 'label400');" onmouseover="ContentPreview('label401');" onmouseout="ContentUnpreview('label401');" title="click to collapse or expand..."> more... </a>
 <div id="label401" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp53</span> Queue number of dscp 53. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label402' href="javascript:ContentClick('label403', 'label402');" onmouseover="ContentPreview('label403');" onmouseout="ContentUnpreview('label403');" title="click to collapse or expand..."> more... </a>
 <div id="label403" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp54</span> Queue number of dscp 54. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label404' href="javascript:ContentClick('label405', 'label404');" onmouseover="ContentPreview('label405');" onmouseout="ContentUnpreview('label405');" title="click to collapse or expand..."> more... </a>
 <div id="label405" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp55</span> Queue number of dscp 55. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label406' href="javascript:ContentClick('label407', 'label406');" onmouseover="ContentPreview('label407');" onmouseout="ContentUnpreview('label407');" title="click to collapse or expand..."> more... </a>
 <div id="label407" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp56</span> Queue number of dscp 56. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label408' href="javascript:ContentClick('label409', 'label408');" onmouseover="ContentPreview('label409');" onmouseout="ContentUnpreview('label409');" title="click to collapse or expand..."> more... </a>
 <div id="label409" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp57</span> Queue number of dscp 57. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label410' href="javascript:ContentClick('label411', 'label410');" onmouseover="ContentPreview('label411');" onmouseout="ContentUnpreview('label411');" title="click to collapse or expand..."> more... </a>
 <div id="label411" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp58</span> Queue number of dscp 58. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label412' href="javascript:ContentClick('label413', 'label412');" onmouseover="ContentPreview('label413');" onmouseout="ContentUnpreview('label413');" title="click to collapse or expand..."> more... </a>
 <div id="label413" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp59</span> Queue number of dscp 59. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label414' href="javascript:ContentClick('label415', 'label414');" onmouseover="ContentPreview('label415');" onmouseout="ContentUnpreview('label415');" title="click to collapse or expand..."> more... </a>
 <div id="label415" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp6</span> Queue number of dscp 6. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label416' href="javascript:ContentClick('label417', 'label416');" onmouseover="ContentPreview('label417');" onmouseout="ContentUnpreview('label417');" title="click to collapse or expand..."> more... </a>
 <div id="label417" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp60</span> Queue number of dscp 60. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label418' href="javascript:ContentClick('label419', 'label418');" onmouseover="ContentPreview('label419');" onmouseout="ContentUnpreview('label419');" title="click to collapse or expand..."> more... </a>
 <div id="label419" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp61</span> Queue number of dscp 61. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label420' href="javascript:ContentClick('label421', 'label420');" onmouseover="ContentPreview('label421');" onmouseout="ContentUnpreview('label421');" title="click to collapse or expand..."> more... </a>
 <div id="label421" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp62</span> Queue number of dscp 62. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label422' href="javascript:ContentClick('label423', 'label422');" onmouseover="ContentPreview('label423');" onmouseout="ContentUnpreview('label423');" title="click to collapse or expand..."> more... </a>
 <div id="label423" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp63</span> Queue number of dscp 63. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label424' href="javascript:ContentClick('label425', 'label424');" onmouseover="ContentPreview('label425');" onmouseout="ContentUnpreview('label425');" title="click to collapse or expand..."> more... </a>
 <div id="label425" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp7</span> Queue number of dscp 7. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label426' href="javascript:ContentClick('label427', 'label426');" onmouseover="ContentPreview('label427');" onmouseout="ContentUnpreview('label427');" title="click to collapse or expand..."> more... </a>
 <div id="label427" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp8</span> Queue number of dscp 8. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label428' href="javascript:ContentClick('label429', 'label428');" onmouseover="ContentPreview('label429');" onmouseout="ContentUnpreview('label429');" title="click to collapse or expand..."> more... </a>
 <div id="label429" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dscp9</span> Queue number of dscp 9. <span class="li-normal">type: str</span> <span class="li-normal">choices: [queue0, queue1, queue2, queue3, queue4, queue5, queue6, queue7]</span> 
 <a id='label430' href="javascript:ContentClick('label431', 'label430');" onmouseover="ContentPreview('label431');" onmouseout="ContentUnpreview('label431');" title="click to collapse or expand..."> more... </a>
 <div id="label431" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">id</span> Profile id. <span class="li-normal">type: int</span>
 <a id='label432' href="javascript:ContentClick('label433', 'label432');" onmouseover="ContentPreview('label433');" onmouseout="ContentUnpreview('label433');" title="click to collapse or expand..."> more... </a>
 <div id="label433" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">type</span> Profile type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [cos, dscp]</span> 
 <a id='label434' href="javascript:ContentClick('label435', 'label434');" onmouseover="ContentPreview('label435');" onmouseout="ContentUnpreview('label435');" title="click to collapse or expand..."> more... </a>
 <div id="label435" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">weight</span> Class weight. <span class="li-normal">type: int</span>
 <a id='label436' href="javascript:ContentClick('label437', 'label436');" onmouseover="ContentPreview('label437');" onmouseout="ContentUnpreview('label437');" title="click to collapse or expand..."> more... </a>
 <div id="label437" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">scheduler</span> Scheduler. <span class="li-normal">type: list</span>
 <a id='label438' href="javascript:ContentClick('label439', 'label438');" onmouseover="ContentPreview('label439');" onmouseout="ContentUnpreview('label439');" title="click to collapse or expand..."> more... </a>
 <div id="label439" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">mode</span> Scheduler mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, priority, round-robin]</span> 
 <a id='label440' href="javascript:ContentClick('label441', 'label440');" onmouseover="ContentPreview('label441');" onmouseout="ContentUnpreview('label441');" title="click to collapse or expand..."> more... </a>
 <div id="label441" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">name</span> Scheduler name. <span class="li-normal">type: str</span>
 <a id='label442' href="javascript:ContentClick('label443', 'label442');" onmouseover="ContentPreview('label443');" onmouseout="ContentUnpreview('label443');" title="click to collapse or expand..."> more... </a>
 <div id="label443" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">custom_etype_lookup</span> <b>(Alias name: custom-etype-lookup)</b>  Enable/disable np-queue lookup for custom ethernet types. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label444' href="javascript:ContentClick('label445', 'label444');" onmouseover="ContentPreview('label445');" onmouseout="ContentUnpreview('label445');" title="click to collapse or expand..."> more... </a>
 <div id="label445" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.7 -> v7.4.7</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">udp_timeout_profile</span> <b>(Alias name: udp-timeout-profile)</b>  Udp timeout profile. <span class="li-normal">type: list</span>
 <a id='label446' href="javascript:ContentClick('label447', 'label446');" onmouseover="ContentPreview('label447');" onmouseout="ContentUnpreview('label447');" title="click to collapse or expand..."> more... </a>
 <div id="label447" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">id</span> Timeout profile id (5-63) <span class="li-normal">type: int</span>
 <a id='label448' href="javascript:ContentClick('label449', 'label448');" onmouseover="ContentPreview('label449');" onmouseout="ContentUnpreview('label449');" title="click to collapse or expand..."> more... </a>
 <div id="label449" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_idle</span> <b>(Alias name: udp-idle)</b>  Set udp idle timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label450' href="javascript:ContentClick('label451', 'label450');" onmouseover="ContentPreview('label451');" onmouseout="ContentUnpreview('label451');" title="click to collapse or expand..."> more... </a>
 <div id="label451" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">qtm_buf_mode</span> <b>(Alias name: qtm-buf-mode)</b>  Qtm channel configuration for packet buffer. <span class="li-normal">type: str</span> <span class="li-normal">choices: [6ch, 4ch]</span> 
 <a id='label452' href="javascript:ContentClick('label453', 'label452');" onmouseover="ContentPreview('label453');" onmouseout="ContentUnpreview('label453');" title="click to collapse or expand..."> more... </a>
 <div id="label453" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">default_qos_type</span> <b>(Alias name: default-qos-type)</b>  Set default qos type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [policing, shaping, policing-enhanced]</span> 
 <a id='label454' href="javascript:ContentClick('label455', 'label454');" onmouseover="ContentPreview('label455');" onmouseout="ContentUnpreview('label455');" title="click to collapse or expand..."> more... </a>
 <div id="label455" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_rst_timeout</span> <b>(Alias name: tcp-rst-timeout)</b>  Tcp rst timeout in seconds (0-3600, default = 5). <span class="li-normal">type: int</span>
 <a id='label456' href="javascript:ContentClick('label457', 'label456');" onmouseover="ContentPreview('label457');" onmouseout="ContentUnpreview('label457');" title="click to collapse or expand..."> more... </a>
 <div id="label457" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_local_uesp_port</span> <b>(Alias name: ipsec-local-uesp-port)</b>  Ipsec local uesp port. <span class="li-normal">type: int</span>
 <a id='label458' href="javascript:ContentClick('label459', 'label458');" onmouseover="ContentPreview('label459');" onmouseout="ContentUnpreview('label459');" title="click to collapse or expand..."> more... </a>
 <div id="label459" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">htab_dedi_queue_nr</span> <b>(Alias name: htab-dedi-queue-nr)</b>  Set the number of dedicate queue for hash table messages. <span class="li-normal">type: int</span>
 <a id='label460' href="javascript:ContentClick('label461', 'label460');" onmouseover="ContentPreview('label461');" onmouseout="ContentUnpreview('label461');" title="click to collapse or expand..."> more... </a>
 <div id="label461" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">double_level_mcast_offload</span> <b>(Alias name: double-level-mcast-offload)</b>  Enable double level mcast offload. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label462' href="javascript:ContentClick('label463', 'label462');" onmouseover="ContentPreview('label463');" onmouseout="ContentUnpreview('label463');" title="click to collapse or expand..."> more... </a>
 <div id="label463" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dse_timeout</span> <b>(Alias name: dse-timeout)</b>  Dse timeout in seconds (0-3600, default = 10). <span class="li-normal">type: int</span>
 <a id='label464' href="javascript:ContentClick('label465', 'label464');" onmouseover="ContentPreview('label465');" onmouseout="ContentUnpreview('label465');" title="click to collapse or expand..."> more... </a>
 <div id="label465" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ippool_overload_low</span> <b>(Alias name: ippool-overload-low)</b>  Low threshold for overload ippool port reuse (100%-2000%, default = 150). <span class="li-normal">type: int</span>
 <a id='label466' href="javascript:ContentClick('label467', 'label466');" onmouseover="ContentPreview('label467');" onmouseout="ContentUnpreview('label467');" title="click to collapse or expand..."> more... </a>
 <div id="label467" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">pba_eim</span> <b>(Alias name: pba-eim)</b>  Configure option for pba(non-overload)/eim combination. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disallow, allow]</span> 
 <a id='label468' href="javascript:ContentClick('label469', 'label468');" onmouseover="ContentPreview('label469');" onmouseout="ContentUnpreview('label469');" title="click to collapse or expand..."> more... </a>
 <div id="label469" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">policy_offload_level</span> <b>(Alias name: policy-offload-level)</b>  Configure firewall policy offload level (disable, default, dos-offload, full-offload). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, dos-offload, full-offload]</span> 
 <a id='label470' href="javascript:ContentClick('label471', 'label470');" onmouseover="ContentPreview('label471');" onmouseout="ContentUnpreview('label471');" title="click to collapse or expand..."> more... </a>
 <div id="label471" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_session_timeout</span> <b>(Alias name: max-session-timeout)</b>  Maximum time interval for refreshing npu-offloaded sessions (10 - 1000 sec, default 40 sec). <span class="li-normal">type: int</span>
 <a id='label472' href="javascript:ContentClick('label473', 'label472');" onmouseover="ContentPreview('label473');" onmouseout="ContentUnpreview('label473');" title="click to collapse or expand..."> more... </a>
 <div id="label473" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port_path_option</span> <b>(Alias name: port-path-option)</b>  Port path option. <span class="li-normal">type: dict</span>
 <a id='label474' href="javascript:ContentClick('label475', 'label474');" onmouseover="ContentPreview('label475');" onmouseout="ContentUnpreview('label475');" title="click to collapse or expand..."> more... </a>
 <div id="label475" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">ports_using_npu</span> <b>(Alias name: ports-using-npu)</b>  Set ha/aux ports to handle traffic with npu (otherise traffic goes to intel-nic and then cpu). <span class="li-normal">type: list</span>
 <a id='label476' href="javascript:ContentClick('label477', 'label476');" onmouseover="ContentPreview('label477');" onmouseout="ContentUnpreview('label477');" title="click to collapse or expand..."> more... </a>
 <div id="label477" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">vlan_lookup_cache</span> <b>(Alias name: vlan-lookup-cache)</b>  Enable/disable vlan lookup cache (default enabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label478' href="javascript:ContentClick('label479', 'label478');" onmouseover="ContentPreview('label479');" onmouseout="ContentUnpreview('label479');" title="click to collapse or expand..."> more... </a>
 <div id="label479" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dos_options</span> <b>(Alias name: dos-options)</b>  Dos options. <span class="li-normal">type: dict</span>
 <a id='label480' href="javascript:ContentClick('label481', 'label480');" onmouseover="ContentPreview('label481');" onmouseout="ContentUnpreview('label481');" title="click to collapse or expand..."> more... </a>
 <div id="label481" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">npu_dos_meter_mode</span> <b>(Alias name: npu-dos-meter-mode)</b>  Set dos meter npu offloading mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [local, global]</span> 
 <a id='label482' href="javascript:ContentClick('label483', 'label482');" onmouseover="ContentPreview('label483');" onmouseout="ContentUnpreview('label483');" title="click to collapse or expand..."> more... </a>
 <div id="label483" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">npu_dos_synproxy_mode</span> <b>(Alias name: npu-dos-synproxy-mode)</b>  Set npu dos synproxy mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [synack2ack, pass-synack]</span> 
 <a id='label484' href="javascript:ContentClick('label485', 'label484');" onmouseover="ContentPreview('label485');" onmouseout="ContentUnpreview('label485');" title="click to collapse or expand..."> more... </a>
 <div id="label485" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">npu_dos_tpe_mode</span> <b>(Alias name: npu-dos-tpe-mode)</b>  Enable/disable insertion of dos meter id to session table. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label486' href="javascript:ContentClick('label487', 'label486');" onmouseover="ContentPreview('label487');" onmouseout="ContentUnpreview('label487');" title="click to collapse or expand..."> more... </a>
 <div id="label487" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">hash_tbl_spread</span> <b>(Alias name: hash-tbl-spread)</b>  Enable/disable hash table entry spread (default enabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label488' href="javascript:ContentClick('label489', 'label488');" onmouseover="ContentPreview('label489');" onmouseout="ContentUnpreview('label489');" title="click to collapse or expand..."> more... </a>
 <div id="label489" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_timeout_profile</span> <b>(Alias name: tcp-timeout-profile)</b>  Tcp timeout profile. <span class="li-normal">type: list</span>
 <a id='label490' href="javascript:ContentClick('label491', 'label490');" onmouseover="ContentPreview('label491');" onmouseout="ContentUnpreview('label491');" title="click to collapse or expand..."> more... </a>
 <div id="label491" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">close_wait</span> <b>(Alias name: close-wait)</b>  Set close-wait timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label492' href="javascript:ContentClick('label493', 'label492');" onmouseover="ContentPreview('label493');" onmouseout="ContentUnpreview('label493');" title="click to collapse or expand..."> more... </a>
 <div id="label493" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fin_wait</span> <b>(Alias name: fin-wait)</b>  Set fin-wait timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label494' href="javascript:ContentClick('label495', 'label494');" onmouseover="ContentPreview('label495');" onmouseout="ContentUnpreview('label495');" title="click to collapse or expand..."> more... </a>
 <div id="label495" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">id</span> Timeout profile id (5-47) <span class="li-normal">type: int</span>
 <a id='label496' href="javascript:ContentClick('label497', 'label496');" onmouseover="ContentPreview('label497');" onmouseout="ContentUnpreview('label497');" title="click to collapse or expand..."> more... </a>
 <div id="label497" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">syn_sent</span> <b>(Alias name: syn-sent)</b>  Set syn-sent timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label498' href="javascript:ContentClick('label499', 'label498');" onmouseover="ContentPreview('label499');" onmouseout="ContentUnpreview('label499');" title="click to collapse or expand..."> more... </a>
 <div id="label499" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">syn_wait</span> <b>(Alias name: syn-wait)</b>  Set syn-wait timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label500' href="javascript:ContentClick('label501', 'label500');" onmouseover="ContentPreview('label501');" onmouseout="ContentUnpreview('label501');" title="click to collapse or expand..."> more... </a>
 <div id="label501" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_idle</span> <b>(Alias name: tcp-idle)</b>  Set tcp establish timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label502' href="javascript:ContentClick('label503', 'label502');" onmouseover="ContentPreview('label503');" onmouseout="ContentUnpreview('label503');" title="click to collapse or expand..."> more... </a>
 <div id="label503" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">time_wait</span> <b>(Alias name: time-wait)</b>  Set time-wait timeout(seconds) <span class="li-normal">type: int</span>
 <a id='label504' href="javascript:ContentClick('label505', 'label504');" onmouseover="ContentPreview('label505');" onmouseout="ContentUnpreview('label505');" title="click to collapse or expand..."> more... </a>
 <div id="label505" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">ip_reassembly</span> <b>(Alias name: ip-reassembly)</b>  Ip reassembly. <span class="li-normal">type: dict</span>
 <a id='label506' href="javascript:ContentClick('label507', 'label506');" onmouseover="ContentPreview('label507');" onmouseout="ContentUnpreview('label507');" title="click to collapse or expand..."> more... </a>
 <div id="label507" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">max_timeout</span> <b>(Alias name: max-timeout)</b>  Maximum timeout value for ip reassembly (5 us - 600,000,000 us). <span class="li-normal">type: int</span>
 <a id='label508' href="javascript:ContentClick('label509', 'label508');" onmouseover="ContentPreview('label509');" onmouseout="ContentUnpreview('label509');" title="click to collapse or expand..."> more... </a>
 <div id="label509" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">min_timeout</span> <b>(Alias name: min-timeout)</b>  Minimum timeout value for ip reassembly (5 us - 600,000,000 us). <span class="li-normal">type: int</span>
 <a id='label510' href="javascript:ContentClick('label511', 'label510');" onmouseover="ContentPreview('label511');" onmouseout="ContentUnpreview('label511');" title="click to collapse or expand..."> more... </a>
 <div id="label511" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">status</span> Set ip reassembly processing status. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label512' href="javascript:ContentClick('label513', 'label512');" onmouseover="ContentPreview('label513');" onmouseout="ContentUnpreview('label513');" title="click to collapse or expand..."> more... </a>
 <div id="label513" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">gtp_support</span> <b>(Alias name: gtp-support)</b>  Enable/disable np7 gtp support <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label514' href="javascript:ContentClick('label515', 'label514');" onmouseover="ContentPreview('label515');" onmouseout="ContentUnpreview('label515');" title="click to collapse or expand..."> more... </a>
 <div id="label515" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">htx_icmp_csum_chk</span> <b>(Alias name: htx-icmp-csum-chk)</b>  Set htx icmp csum checking mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [pass, drop]</span> 
 <a id='label516' href="javascript:ContentClick('label517', 'label516');" onmouseover="ContentPreview('label517');" onmouseout="ContentUnpreview('label517');" title="click to collapse or expand..."> more... </a>
 <div id="label517" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">hpe</span> Hpe. <span class="li-normal">type: dict</span>
 <a id='label518' href="javascript:ContentClick('label519', 'label518');" onmouseover="ContentPreview('label519');" onmouseout="ContentUnpreview('label519');" title="click to collapse or expand..."> more... </a>
 <div id="label519" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">all_protocol</span> <b>(Alias name: all-protocol)</b>  Maximum packet rate of each host queue except high priority traffic(1k - 32m pps, default = 400k pps), set 0 to disable. <span class="li-normal">type: int</span>
 <a id='label520' href="javascript:ContentClick('label521', 'label520');" onmouseover="ContentPreview('label521');" onmouseout="ContentUnpreview('label521');" title="click to collapse or expand..."> more... </a>
 <div id="label521" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">arp_max</span> <b>(Alias name: arp-max)</b>  Maximum arp packet rate (1k - 32m pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label522' href="javascript:ContentClick('label523', 'label522');" onmouseover="ContentPreview('label523');" onmouseout="ContentUnpreview('label523');" title="click to collapse or expand..."> more... </a>
 <div id="label523" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">enable_shaper</span> <b>(Alias name: enable-shaper)</b>  Enable/disable npu host protection engine (hpe) for packet type shaper. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label524' href="javascript:ContentClick('label525', 'label524');" onmouseover="ContentPreview('label525');" onmouseout="ContentUnpreview('label525');" title="click to collapse or expand..."> more... </a>
 <div id="label525" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">esp_max</span> <b>(Alias name: esp-max)</b>  Maximum esp packet rate (1k - 32m pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label526' href="javascript:ContentClick('label527', 'label526');" onmouseover="ContentPreview('label527');" onmouseout="ContentUnpreview('label527');" title="click to collapse or expand..."> more... </a>
 <div id="label527" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">high_priority</span> <b>(Alias name: high-priority)</b>  Maximum packet rate for high priority traffic packets (1k - 32m pps, default = 400k pps). <span class="li-normal">type: int</span>
 <a id='label528' href="javascript:ContentClick('label529', 'label528');" onmouseover="ContentPreview('label529');" onmouseout="ContentUnpreview('label529');" title="click to collapse or expand..."> more... </a>
 <div id="label529" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_max</span> <b>(Alias name: icmp-max)</b>  Maximum icmp packet rate (1k - 32m pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label530' href="javascript:ContentClick('label531', 'label530');" onmouseover="ContentPreview('label531');" onmouseout="ContentUnpreview('label531');" title="click to collapse or expand..."> more... </a>
 <div id="label531" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip_frag_max</span> <b>(Alias name: ip-frag-max)</b>  Maximum fragmented ip packet rate (1k - 32m pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label532' href="javascript:ContentClick('label533', 'label532');" onmouseover="ContentPreview('label533');" onmouseout="ContentUnpreview('label533');" title="click to collapse or expand..."> more... </a>
 <div id="label533" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip_others_max</span> <b>(Alias name: ip-others-max)</b>  Maximum ip packet rate for other packets (packet types that cannot be set with other options) (1k - 32g pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label534' href="javascript:ContentClick('label535', 'label534');" onmouseover="ContentPreview('label535');" onmouseout="ContentUnpreview('label535');" title="click to collapse or expand..."> more... </a>
 <div id="label535" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l2_others_max</span> <b>(Alias name: l2-others-max)</b>  Maximum l2 packet rate for l2 packets that are not arp packets (1k - 32m pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label536' href="javascript:ContentClick('label537', 'label536');" onmouseover="ContentPreview('label537');" onmouseout="ContentUnpreview('label537');" title="click to collapse or expand..."> more... </a>
 <div id="label537" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">pri_type_max</span> <b>(Alias name: pri-type-max)</b>  Maximum overflow rate of priority type traffic(1k - 32m pps, default = 40k pps). <span class="li-normal">type: int</span>
 <a id='label538' href="javascript:ContentClick('label539', 'label538');" onmouseover="ContentPreview('label539');" onmouseout="ContentUnpreview('label539');" title="click to collapse or expand..."> more... </a>
 <div id="label539" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sctp_max</span> <b>(Alias name: sctp-max)</b>  Maximum sctp packet rate (1k - 32m pps, default = 5k pps). <span class="li-normal">type: int</span>
 <a id='label540' href="javascript:ContentClick('label541', 'label540');" onmouseover="ContentPreview('label541');" onmouseout="ContentUnpreview('label541');" title="click to collapse or expand..."> more... </a>
 <div id="label541" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_max</span> <b>(Alias name: tcp-max)</b>  Maximum tcp packet rate (1k - 32m pps, default = 40k pps). <span class="li-normal">type: int</span>
 <a id='label542' href="javascript:ContentClick('label543', 'label542');" onmouseover="ContentPreview('label543');" onmouseout="ContentUnpreview('label543');" title="click to collapse or expand..."> more... </a>
 <div id="label543" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcpfin_rst_max</span> <b>(Alias name: tcpfin-rst-max)</b>  Maximum tcp carries fin or rst flags packet rate (1k - 32m pps, default = 40k pps). <span class="li-normal">type: int</span>
 <a id='label544' href="javascript:ContentClick('label545', 'label544');" onmouseover="ContentPreview('label545');" onmouseout="ContentUnpreview('label545');" title="click to collapse or expand..."> more... </a>
 <div id="label545" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcpsyn_ack_max</span> <b>(Alias name: tcpsyn-ack-max)</b>  Maximum tcp carries syn and ack flags packet rate (1k - 32m pps, default = 40k pps). <span class="li-normal">type: int</span>
 <a id='label546' href="javascript:ContentClick('label547', 'label546');" onmouseover="ContentPreview('label547');" onmouseout="ContentUnpreview('label547');" title="click to collapse or expand..."> more... </a>
 <div id="label547" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcpsyn_max</span> <b>(Alias name: tcpsyn-max)</b>  Maximum tcp syn packet rate (1k - 40m pps, default = 32k pps). <span class="li-normal">type: int</span>
 <a id='label548' href="javascript:ContentClick('label549', 'label548');" onmouseover="ContentPreview('label549');" onmouseout="ContentUnpreview('label549');" title="click to collapse or expand..."> more... </a>
 <div id="label549" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_max</span> <b>(Alias name: udp-max)</b>  Maximum udp packet rate (1k - 32m pps, default = 40k pps). <span class="li-normal">type: int</span>
 <a id='label550' href="javascript:ContentClick('label551', 'label550');" onmouseover="ContentPreview('label551');" onmouseout="ContentUnpreview('label551');" title="click to collapse or expand..."> more... </a>
 <div id="label551" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">enable_queue_shaper</span> <b>(Alias name: enable-queue-shaper)</b>  Enable/disable npu host protection engine (hpe) queue shaper. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label552' href="javascript:ContentClick('label553', 'label552');" onmouseover="ContentPreview('label553');" onmouseout="ContentUnpreview('label553');" title="click to collapse or expand..."> more... </a>
 <div id="label553" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">exception_code</span> <b>(Alias name: exception-code)</b>  Maximum exception code rate of traffic(1k - 32m pps, default = 1m pps). <span class="li-normal">type: int</span>
 <a id='label554' href="javascript:ContentClick('label555', 'label554');" onmouseover="ContentPreview('label555');" onmouseout="ContentUnpreview('label555');" title="click to collapse or expand..."> more... </a>
 <div id="label555" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fragment_with_sess</span> <b>(Alias name: fragment-with-sess)</b>  Maximum fragment with session rate of traffic(1k - 32m pps, default = 1m pps). <span class="li-normal">type: int</span>
 <a id='label556' href="javascript:ContentClick('label557', 'label556');" onmouseover="ContentPreview('label557');" onmouseout="ContentUnpreview('label557');" title="click to collapse or expand..."> more... </a>
 <div id="label557" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fragment_without_session</span> <b>(Alias name: fragment-without-session)</b>  Maximum fragment without session rate of traffic(1k - 32m pps, default = 1m pps). <span class="li-normal">type: int</span>
 <a id='label558' href="javascript:ContentClick('label559', 'label558');" onmouseover="ContentPreview('label559');" onmouseout="ContentUnpreview('label559');" title="click to collapse or expand..."> more... </a>
 <div id="label559" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">queue_shaper_max</span> <b>(Alias name: queue-shaper-max)</b>  Maximum per queue byte rate of traffic(1k - 32m pps, default = 1m pps). <span class="li-normal">type: int</span>
 <a id='label560' href="javascript:ContentClick('label561', 'label560');" onmouseover="ContentPreview('label561');" onmouseout="ContentUnpreview('label561');" title="click to collapse or expand..."> more... </a>
 <div id="label561" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">dsw_dts_profile</span> <b>(Alias name: dsw-dts-profile)</b>  Dsw dts profile. <span class="li-normal">type: list</span>
 <a id='label562' href="javascript:ContentClick('label563', 'label562');" onmouseover="ContentPreview('label563');" onmouseout="ContentUnpreview('label563');" title="click to collapse or expand..."> more... </a>
 <div id="label563" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">action</span> Set npu dsw dts profile action. <span class="li-normal">type: str</span> <span class="li-normal">choices: [wait, drop, drop_tmr_0, drop_tmr_1, enque, enque_0, enque_1]</span> 
 <a id='label564' href="javascript:ContentClick('label565', 'label564');" onmouseover="ContentPreview('label565');" onmouseout="ContentUnpreview('label565');" title="click to collapse or expand..."> more... </a>
 <div id="label565" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">min_limit</span> <b>(Alias name: min-limit)</b>  Set npu dsw dts profile min-limt. <span class="li-normal">type: int</span>
 <a id='label566' href="javascript:ContentClick('label567', 'label566');" onmouseover="ContentPreview('label567');" onmouseout="ContentUnpreview('label567');" title="click to collapse or expand..."> more... </a>
 <div id="label567" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">profile_id</span> <b>(Alias name: profile-id)</b>  Set npu dsw dts profile profile id. <span class="li-normal">type: int</span>
 <a id='label568' href="javascript:ContentClick('label569', 'label568');" onmouseover="ContentPreview('label569');" onmouseout="ContentUnpreview('label569');" title="click to collapse or expand..."> more... </a>
 <div id="label569" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">step</span> Set npu dsw dts profile step. <span class="li-normal">type: int</span>
 <a id='label570' href="javascript:ContentClick('label571', 'label570');" onmouseover="ContentPreview('label571');" onmouseout="ContentUnpreview('label571');" title="click to collapse or expand..."> more... </a>
 <div id="label571" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">hash_config</span> <b>(Alias name: hash-config)</b>  Configure npu trunk hash. <span class="li-normal">type: str</span> <span class="li-normal">choices: [5-tuple, src-ip, src-dst-ip]</span> 
 <a id='label572' href="javascript:ContentClick('label573', 'label572');" onmouseover="ContentPreview('label573');" onmouseout="ContentUnpreview('label573');" title="click to collapse or expand..."> more... </a>
 <div id="label573" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_ob_np_sel</span> <b>(Alias name: ipsec-ob-np-sel)</b>  Ipsec np selection for ob sa offloading. <span class="li-normal">type: str</span> <span class="li-normal">choices: [RR, rr, Packet, Hash]</span> 
 <a id='label574' href="javascript:ContentClick('label575', 'label574');" onmouseover="ContentPreview('label575');" onmouseout="ContentUnpreview('label575');" title="click to collapse or expand..."> more... </a>
 <div id="label575" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">napi_break_interval</span> <b>(Alias name: napi-break-interval)</b>  Napi break interval (default 0). <span class="li-normal">type: int</span>
 <a id='label576' href="javascript:ContentClick('label577', 'label576');" onmouseover="ContentPreview('label577');" onmouseout="ContentUnpreview('label577');" title="click to collapse or expand..."> more... </a>
 <div id="label577" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">background_sse_scan</span> <b>(Alias name: background-sse-scan)</b>  Background sse scan. <span class="li-normal">type: dict</span>
 <a id='label578' href="javascript:ContentClick('label579', 'label578');" onmouseover="ContentPreview('label579');" onmouseout="ContentUnpreview('label579');" title="click to collapse or expand..."> more... </a>
 <div id="label579" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">scan</span> Enable/disable background sse scan by driver thread(default enabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label580' href="javascript:ContentClick('label581', 'label580');" onmouseover="ContentPreview('label581');" onmouseout="ContentUnpreview('label581');" title="click to collapse or expand..."> more... </a>
 <div id="label581" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">stats_update_interval</span> <b>(Alias name: stats-update-interval)</b>  Stats update interval(>=5*60 seconds, default 5*60 seconds). <span class="li-normal">type: int</span>
 <a id='label582' href="javascript:ContentClick('label583', 'label582');" onmouseover="ContentPreview('label583');" onmouseout="ContentUnpreview('label583');" title="click to collapse or expand..."> more... </a>
 <div id="label583" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_keepalive_interval</span> <b>(Alias name: udp-keepalive-interval)</b>  Udp keepalive interval(>=90 seconds, default 90 seconds). <span class="li-normal">type: int</span>
 <a id='label584' href="javascript:ContentClick('label585', 'label584');" onmouseover="ContentPreview('label585');" onmouseout="ContentUnpreview('label585');" title="click to collapse or expand..."> more... </a>
 <div id="label585" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">scan_stale</span> <b>(Alias name: scan-stale)</b>  Configure scanning of active or stale sessions (default = 0 = active sessions). <span class="li-normal">type: int</span>
 <a id='label586' href="javascript:ContentClick('label587', 'label586');" onmouseover="ContentPreview('label587');" onmouseout="ContentUnpreview('label587');" title="click to collapse or expand..."> more... </a>
 <div id="label587" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">scan_vt</span> <b>(Alias name: scan-vt)</b>  Select version/type to scan: bit-0: 44; bit-1: 46; bit-2: 64; bit-3: 66 (default = 0xf). <span class="li-normal">type: int</span>
 <a id='label588' href="javascript:ContentClick('label589', 'label588');" onmouseover="ContentPreview('label589');" onmouseout="ContentUnpreview('label589');" title="click to collapse or expand..."> more... </a>
 <div id="label589" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">stats_qual_access</span> <b>(Alias name: stats-qual-access)</b>  Statistics update access qualification in seconds (0 - int_max, default = 180). <span class="li-normal">type: int</span>
 <a id='label590' href="javascript:ContentClick('label591', 'label590');" onmouseover="ContentPreview('label591');" onmouseout="ContentUnpreview('label591');" title="click to collapse or expand..."> more... </a>
 <div id="label591" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">stats_qual_duration</span> <b>(Alias name: stats-qual-duration)</b>  Statistics update duration qualification in seconds (0 - int_max, default = 300). <span class="li-normal">type: int</span>
 <a id='label592' href="javascript:ContentClick('label593', 'label592');" onmouseover="ContentPreview('label593');" onmouseout="ContentUnpreview('label593');" title="click to collapse or expand..."> more... </a>
 <div id="label593" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_qual_access</span> <b>(Alias name: udp-qual-access)</b>  Udp keepalive access qualification in seconds (0 - int_max, default = 30). <span class="li-normal">type: int</span>
 <a id='label594' href="javascript:ContentClick('label595', 'label594');" onmouseover="ContentPreview('label595');" onmouseout="ContentUnpreview('label595');" title="click to collapse or expand..."> more... </a>
 <div id="label595" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">udp_qual_duration</span> <b>(Alias name: udp-qual-duration)</b>  Udp keepalive duration qualification in seconds (0 - int_max, default = 90). <span class="li-normal">type: int</span>
 <a id='label596' href="javascript:ContentClick('label597', 'label596');" onmouseover="ContentPreview('label597');" onmouseout="ContentUnpreview('label597');" title="click to collapse or expand..."> more... </a>
 <div id="label597" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">inbound_dscp_copy_port</span> <b>(Alias name: inbound-dscp-copy-port)</b>  Physical interfaces that support inbound-dscp-copy. <span class="li-normal">type: list</span>
 <a id='label598' href="javascript:ContentClick('label599', 'label598');" onmouseover="ContentPreview('label599');" onmouseout="ContentUnpreview('label599');" title="click to collapse or expand..."> more... </a>
 <div id="label599" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">session_acct_interval</span> <b>(Alias name: session-acct-interval)</b>  Session accounting update interval (1 - 10 sec, default 5 sec). <span class="li-normal">type: int</span>
 <a id='label600' href="javascript:ContentClick('label601', 'label600');" onmouseover="ContentPreview('label601');" onmouseout="ContentUnpreview('label601');" title="click to collapse or expand..."> more... </a>
 <div id="label601" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">htab_msg_queue</span> <b>(Alias name: htab-msg-queue)</b>  Set hash table message queue mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [idle, data, dedicated]</span> 
 <a id='label602' href="javascript:ContentClick('label603', 'label602');" onmouseover="ContentPreview('label603');" onmouseout="ContentUnpreview('label603');" title="click to collapse or expand..."> more... </a>
 <div id="label603" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dsw_queue_dts_profile</span> <b>(Alias name: dsw-queue-dts-profile)</b>  Dsw queue dts profile. <span class="li-normal">type: list</span>
 <a id='label604' href="javascript:ContentClick('label605', 'label604');" onmouseover="ContentPreview('label605');" onmouseout="ContentUnpreview('label605');" title="click to collapse or expand..."> more... </a>
 <div id="label605" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">iport</span> Set npu dsw dts in port. <span class="li-normal">type: str</span> <span class="li-normal">choices: [EIF0, eif0, EIF1, eif1, EIF2, eif2, EIF3, eif3, EIF4, eif4, EIF5, eif5, EIF6, eif6, EIF7, eif7, HTX0, htx0, HTX1, htx1, SSE0, sse0, SSE1, sse1, SSE2, sse2, SSE3, sse3, RLT, rlt, DFR, dfr, IPSECI, ipseci, IPSECO, ipseco, IPTI, ipti, IPTO, ipto, VEP0, vep0, VEP2, vep2, VEP4, vep4, VEP6, vep6, IVS, ivs, L2TI1, l2ti1, L2TO, l2to, L2TI0, l2ti0, PLE, ple, SPATH, spath, QTM, qtm]</span> 
 <a id='label606' href="javascript:ContentClick('label607', 'label606');" onmouseover="ContentPreview('label607');" onmouseout="ContentUnpreview('label607');" title="click to collapse or expand..."> more... </a>
 <div id="label607" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">name</span> Name. <span class="li-normal">type: str</span>
 <a id='label608' href="javascript:ContentClick('label609', 'label608');" onmouseover="ContentPreview('label609');" onmouseout="ContentUnpreview('label609');" title="click to collapse or expand..."> more... </a>
 <div id="label609" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">oport</span> Set npu dsw dts out port. <span class="li-normal">type: str</span> <span class="li-normal">choices: [EIF0, eif0, EIF1, eif1, EIF2, eif2, EIF3, eif3, EIF4, eif4, EIF5, eif5, EIF6, eif6, EIF7, eif7, HRX, hrx, SSE0, sse0, SSE1, sse1, SSE2, sse2, SSE3, sse3, RLT, rlt, DFR, dfr, IPSECI, ipseci, IPSECO, ipseco, IPTI, ipti, IPTO, ipto, VEP0, vep0, VEP2, vep2, VEP4, vep4, VEP6, vep6, IVS, ivs, L2TI1, l2ti1, L2TO, l2to, L2TI0, l2ti0, PLE, ple, SYNK, sync, NSS, nss, TSK, tsk, QTM, qtm, l2tO]</span> 
 <a id='label610' href="javascript:ContentClick('label611', 'label610');" onmouseover="ContentPreview('label611');" onmouseout="ContentUnpreview('label611');" title="click to collapse or expand..."> more... </a>
 <div id="label611" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">profile_id</span> <b>(Alias name: profile-id)</b>  Set npu dsw dts profile id. <span class="li-normal">type: int</span>
 <a id='label612' href="javascript:ContentClick('label613', 'label612');" onmouseover="ContentPreview('label613');" onmouseout="ContentUnpreview('label613');" title="click to collapse or expand..."> more... </a>
 <div id="label613" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">queue_select</span> <b>(Alias name: queue-select)</b>  Set npu dsw dts queue id select (0 - reset to default). <span class="li-normal">type: int</span>
 <a id='label614' href="javascript:ContentClick('label615', 'label614');" onmouseover="ContentPreview('label615');" onmouseout="ContentUnpreview('label615');" title="click to collapse or expand..."> more... </a>
 <div id="label615" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">hw_ha_scan_interval</span> <b>(Alias name: hw-ha-scan-interval)</b>  Hw ha periodical scan interval in seconds (0-3600, default = 120, 0 to disable). <span class="li-normal">type: int</span>
 <a id='label616' href="javascript:ContentClick('label617', 'label616');" onmouseover="ContentPreview('label617');" onmouseout="ContentUnpreview('label617');" title="click to collapse or expand..."> more... </a>
 <div id="label617" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ippool_overload_high</span> <b>(Alias name: ippool-overload-high)</b>  High threshold for overload ippool port reuse (100%-2000%, default = 200). <span class="li-normal">type: int</span>
 <a id='label618' href="javascript:ContentClick('label619', 'label618');" onmouseover="ContentPreview('label619');" onmouseout="ContentUnpreview('label619');" title="click to collapse or expand..."> more... </a>
 <div id="label619" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">nat46_force_ipv4_packet_forwarding</span> <b>(Alias name: nat46-force-ipv4-packet-forwarding)</b>  Enable/disable mandatory ipv4 packet forwarding in nat46. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label620' href="javascript:ContentClick('label621', 'label620');" onmouseover="ContentPreview('label621');" onmouseout="ContentUnpreview('label621');" title="click to collapse or expand..."> more... </a>
 <div id="label621" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">prp_port_out</span> <b>(Alias name: prp-port-out)</b>  Egress port configured to allow the prp trailer not be stripped off when the prp packets go out. <span class="li-normal">type: list or str</span>
 <a id='label622' href="javascript:ContentClick('label623', 'label622');" onmouseover="ContentPreview('label623');" onmouseout="ContentUnpreview('label623');" title="click to collapse or expand..."> more... </a>
 <div id="label623" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">isf_np_rx_tr_distr</span> <b>(Alias name: isf-np-rx-tr-distr)</b>  Select isf np rx trunk distribution (psc) mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [port-flow, round-robin, randomized]</span> 
 <a id='label624' href="javascript:ContentClick('label625', 'label624');" onmouseover="ContentPreview('label625');" onmouseout="ContentUnpreview('label625');" title="click to collapse or expand..."> more... </a>
 <div id="label625" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mcast_session_counting6</span> <b>(Alias name: mcast-session-counting6)</b>  Enable/disable traffic accounting for each multicast session6 through tae counter. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, session-based, tpe-based]</span> 
 <a id='label626' href="javascript:ContentClick('label627', 'label626');" onmouseover="ContentPreview('label627');" onmouseout="ContentUnpreview('label627');" title="click to collapse or expand..."> more... </a>
 <div id="label627" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">prp_port_in</span> <b>(Alias name: prp-port-in)</b>  Ingress port configured to allow the prp trailer not be stripped off when the prp packets come in. <span class="li-normal">type: list or str</span>
 <a id='label628' href="javascript:ContentClick('label629', 'label628');" onmouseover="ContentPreview('label629');" onmouseout="ContentUnpreview('label629');" title="click to collapse or expand..."> more... </a>
 <div id="label629" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rps_mode</span> <b>(Alias name: rps-mode)</b>  Enable/disable receive packet steering (rps) optimization mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label630' href="javascript:ContentClick('label631', 'label630');" onmouseover="ContentPreview('label631');" onmouseout="ContentUnpreview('label631');" title="click to collapse or expand..."> more... </a>
 <div id="label631" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">per_policy_accounting</span> <b>(Alias name: per-policy-accounting)</b>  Set per-policy accounting. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label632' href="javascript:ContentClick('label633', 'label632');" onmouseover="ContentPreview('label633');" onmouseout="ContentUnpreview('label633');" title="click to collapse or expand..."> more... </a>
 <div id="label633" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mcast_session_counting</span> <b>(Alias name: mcast-session-counting)</b>  Mcast session counting. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, session-based, tpe-based]</span> 
 <a id='label634' href="javascript:ContentClick('label635', 'label634');" onmouseover="ContentPreview('label635');" onmouseout="ContentUnpreview('label635');" title="click to collapse or expand..."> more... </a>
 <div id="label635" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">inbound_dscp_copy</span> <b>(Alias name: inbound-dscp-copy)</b>  Enable/disable copying the dscp field from outer ip header to inner ip header. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label636' href="javascript:ContentClick('label637', 'label636');" onmouseover="ContentPreview('label637');" onmouseout="ContentUnpreview('label637');" title="click to collapse or expand..."> more... </a>
 <div id="label637" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_host_dfclr</span> <b>(Alias name: ipsec-host-dfclr)</b>  Enable/disable df clearing of np4lite host ipsec offload. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label638' href="javascript:ContentClick('label639', 'label638');" onmouseover="ContentPreview('label639');" onmouseout="ContentUnpreview('label639');" title="click to collapse or expand..."> more... </a>
 <div id="label639" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.2.1</code></p>
 </div>
 </li>
 <li><span class="li-head">process_icmp_by_host</span> <b>(Alias name: process-icmp-by-host)</b>  Enable/disable process icmp by host when received from ipsec tunnel and payload size < 119. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label640' href="javascript:ContentClick('label641', 'label640');" onmouseover="ContentPreview('label641');" onmouseout="ContentUnpreview('label641');" title="click to collapse or expand..."> more... </a>
 <div id="label641" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> v7.2.1</code></p>
 </div>
 </li>
 <li><span class="li-head">dedicated_tx_npu</span> <b>(Alias name: dedicated-tx-npu)</b>  Enable/disable dedication of 3rd npu for slow path tx. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label642' href="javascript:ContentClick('label643', 'label642');" onmouseover="ContentPreview('label643');" onmouseout="ContentUnpreview('label643');" title="click to collapse or expand..."> more... </a>
 <div id="label643" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.7 -> v6.4.15</code></p>
 </div>
 </li>
 <li><span class="li-head">ull_port_mode</span> <b>(Alias name: ull-port-mode)</b>  Set ull ports speed to 10g/25g (default 10g). <span class="li-normal">type: str</span> <span class="li-normal">choices: [10G, 25G]</span> 
 <a id='label644' href="javascript:ContentClick('label645', 'label644');" onmouseover="ContentPreview('label645');" onmouseout="ContentUnpreview('label645');" title="click to collapse or expand..."> more... </a>
 <div id="label645" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.9 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sse_ha_scan</span> <b>(Alias name: sse-ha-scan)</b>  Sse ha scan. <span class="li-normal">type: dict</span>
 <a id='label646' href="javascript:ContentClick('label647', 'label646');" onmouseover="ContentPreview('label647');" onmouseout="ContentUnpreview('label647');" title="click to collapse or expand..."> more... </a>
 <div id="label647" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.10 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">gap</span> Scanning message gap(0~32767, default 6000) <span class="li-normal">type: int</span>
 <a id='label648' href="javascript:ContentClick('label649', 'label648');" onmouseover="ContentPreview('label649');" onmouseout="ContentUnpreview('label649');" title="click to collapse or expand..."> more... </a>
 <div id="label649" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.10 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_session_cnt</span> <b>(Alias name: max-session-cnt)</b>  If the session count(in millions) is larger than this, ha scan will be skipped. <span class="li-normal">type: int</span>
 <a id='label650' href="javascript:ContentClick('label651', 'label650');" onmouseover="ContentPreview('label651');" onmouseout="ContentUnpreview('label651');" title="click to collapse or expand..."> more... </a>
 <div id="label651" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.10 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">min_duration</span> <b>(Alias name: min-duration)</b>  Scanning filter for minimum duration of the session. <span class="li-normal">type: int</span>
 <a id='label652' href="javascript:ContentClick('label653', 'label652');" onmouseover="ContentPreview('label653');" onmouseout="ContentUnpreview('label653');" title="click to collapse or expand..."> more... </a>
 <div id="label653" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.10 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">hash_ipv6_sel</span> <b>(Alias name: hash-ipv6-sel)</b>  Select which 4bytes of the ipv6 address are used for traffic hash(0~3). <span class="li-normal">type: int</span>
 <a id='label654' href="javascript:ContentClick('label655', 'label654');" onmouseover="ContentPreview('label655');" onmouseout="ContentUnpreview('label655');" title="click to collapse or expand..."> more... </a>
 <div id="label655" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip_fragment_offload</span> <b>(Alias name: ip-fragment-offload)</b>  Enable/disable np7 npu ip fragment offload. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label656' href="javascript:ContentClick('label657', 'label656');" onmouseover="ContentPreview('label657');" onmouseout="ContentUnpreview('label657');" title="click to collapse or expand..."> more... </a>
 <div id="label657" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.4 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ple_non_syn_tcp_action</span> <b>(Alias name: ple-non-syn-tcp-action)</b>  Configure action for the ple to take on tcp packets that have the syn field unset. <span class="li-normal">type: str</span> <span class="li-normal">choices: [forward, drop]</span> 
 <a id='label658' href="javascript:ContentClick('label659', 'label658');" onmouseover="ContentPreview('label659');" onmouseout="ContentUnpreview('label659');" title="click to collapse or expand..."> more... </a>
 <div id="label659" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.5 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">npu_group_effective_scope</span> <b>(Alias name: npu-group-effective-scope)</b>  Npu-group-effective-scope defines under which npu-group cmds such as list/purge will be excecuted. <span class="li-normal">type: int</span>
 <a id='label660' href="javascript:ContentClick('label661', 'label660');" onmouseover="ContentPreview('label661');" onmouseout="ContentUnpreview('label661');" title="click to collapse or expand..."> more... </a>
 <div id="label661" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.6 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_STS_timeout</span> <b>(Alias name: ipsec-STS-timeout)</b>  Set np7lite ipsec sts msg timeout. <span class="li-normal">type: str</span> <span class="li-normal">choices: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]</span> 
 <a id='label662' href="javascript:ContentClick('label663', 'label662');" onmouseover="ContentPreview('label663');" onmouseout="ContentUnpreview('label663');" title="click to collapse or expand..."> more... </a>
 <div id="label663" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_throughput_msg_frequency</span> <b>(Alias name: ipsec-throughput-msg-frequency)</b>  Set np7lite ipsec throughput msg frequency: 0--disable 1--32kb 3--64kb . <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, 32KB, 64KB, 128KB, 256KB, 512KB, 1MB, 2MB, 4MB, 8MB, 16MB, 32MB, 64MB, 128MB, 256MB, 512MB, 1GB]</span> 
 <a id='label664' href="javascript:ContentClick('label665', 'label664');" onmouseover="ContentPreview('label665');" onmouseout="ContentUnpreview('label665');" title="click to collapse or expand..."> more... </a>
 <div id="label665" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipt_STS_timeout</span> <b>(Alias name: ipt-STS-timeout)</b>  Set np7lite ipt sts msg timeout. <span class="li-normal">type: str</span> <span class="li-normal">choices: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]</span> 
 <a id='label666' href="javascript:ContentClick('label667', 'label666');" onmouseover="ContentPreview('label667');" onmouseout="ContentUnpreview('label667');" title="click to collapse or expand..."> more... </a>
 <div id="label667" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipt_throughput_msg_frequency</span> <b>(Alias name: ipt-throughput-msg-frequency)</b>  Set np7lite ipt throughput msg frequency: 0--disable 1--32kb 3--64kb . <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, 32KB, 64KB, 128KB, 256KB, 512KB, 1MB, 2MB, 4MB, 8MB, 16MB, 32MB, 64MB, 128MB, 256MB, 512MB, 1GB]</span> 
 <a id='label668' href="javascript:ContentClick('label669', 'label668');" onmouseover="ContentPreview('label669');" onmouseout="ContentUnpreview('label669');" title="click to collapse or expand..."> more... </a>
 <div id="label669" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.9 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.4 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">default_tcp_refresh_dir</span> <b>(Alias name: default-tcp-refresh-dir)</b>  Default sse timeout tcp refresh direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: [both, outgoing, incoming]</span> 
 <a id='label670' href="javascript:ContentClick('label671', 'label670');" onmouseover="ContentPreview('label671');" onmouseout="ContentUnpreview('label671');" title="click to collapse or expand..."> more... </a>
 <div id="label671" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">default_udp_refresh_dir</span> <b>(Alias name: default-udp-refresh-dir)</b>  Default sse timeout udp refresh direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: [both, outgoing, incoming]</span> 
 <a id='label672' href="javascript:ContentClick('label673', 'label672');" onmouseover="ContentPreview('label673');" onmouseout="ContentUnpreview('label673');" title="click to collapse or expand..."> more... </a>
 <div id="label673" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">nss_threads_option</span> <b>(Alias name: nss-threads-option)</b>  Configure thread options for the np7s nss module. <span class="li-normal">type: str</span> <span class="li-normal">choices: [4t-eif, 4t-noeif, 2t]</span> 
 <a id='label674' href="javascript:ContentClick('label675', 'label674');" onmouseover="ContentPreview('label675');" onmouseout="ContentUnpreview('label675');" title="click to collapse or expand..."> more... </a>
 <div id="label675" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.12 -> v7.0.13</code>, <code class="docutils literal notranslate">v7.2.6 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">prp_session_clear_mode</span> <b>(Alias name: prp-session-clear-mode)</b>  Prp session clear mode for excluded ip sessions. <span class="li-normal">type: str</span> <span class="li-normal">choices: [blocking, non-blocking, do-not-clear]</span> 
 <a id='label676' href="javascript:ContentClick('label677', 'label676');" onmouseover="ContentPreview('label677');" onmouseout="ContentUnpreview('label677');" title="click to collapse or expand..."> more... </a>
 <div id="label677" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">shaping_stats</span> <b>(Alias name: shaping-stats)</b>  Enable/disable np7 traffic shaping statistics (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label678' href="javascript:ContentClick('label679', 'label678');" onmouseover="ContentPreview('label679');" onmouseout="ContentUnpreview('label679');" title="click to collapse or expand..."> more... </a>
 <div id="label679" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sw_tr_hash</span> <b>(Alias name: sw-tr-hash)</b>  Sw tr hash. <span class="li-normal">type: dict</span>
 <a id='label680' href="javascript:ContentClick('label681', 'label680');" onmouseover="ContentPreview('label681');" onmouseout="ContentUnpreview('label681');" title="click to collapse or expand..."> more... </a>
 <div id="label681" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.4 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">draco15</span> Enable/disable draco15 hashing. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label682' href="javascript:ContentClick('label683', 'label682');" onmouseover="ContentPreview('label683');" onmouseout="ContentUnpreview('label683');" title="click to collapse or expand..."> more... </a>
 <div id="label683" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_udp_port</span> <b>(Alias name: tcp-udp-port)</b>  Include/exclude tcp/udp source and destination port for unicast trunk traffic. <span class="li-normal">type: str</span> <span class="li-normal">choices: [include, exclude]</span> 
 <a id='label684' href="javascript:ContentClick('label685', 'label684');" onmouseover="ContentPreview('label685');" onmouseout="ContentUnpreview('label685');" title="click to collapse or expand..."> more... </a>
 <div id="label685" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.4 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">pba_port_select_mode</span> <b>(Alias name: pba-port-select-mode)</b>  Port selection mode for pba ip pool. <span class="li-normal">type: str</span> <span class="li-normal">choices: [random, direct]</span> 
 <a id='label686' href="javascript:ContentClick('label687', 'label686');" onmouseover="ContentPreview('label687');" onmouseout="ContentUnpreview('label687');" title="click to collapse or expand..."> more... </a>
 <div id="label687" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.5 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">spa_port_select_mode</span> <b>(Alias name: spa-port-select-mode)</b>  Port selection mode for spa ip pool. <span class="li-normal">type: str</span> <span class="li-normal">choices: [random, direct]</span> 
 <a id='label688' href="javascript:ContentClick('label689', 'label688');" onmouseover="ContentPreview('label689');" onmouseout="ContentUnpreview('label689');" title="click to collapse or expand..."> more... </a>
 <div id="label689" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.5 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">split_ipsec_engines</span> <b>(Alias name: split-ipsec-engines)</b>  Enable/disable split ipsec engines. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label690' href="javascript:ContentClick('label691', 'label690');" onmouseover="ContentPreview('label691');" onmouseout="ContentUnpreview('label691');" title="click to collapse or expand..."> more... </a>
 <div id="label691" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.5 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tunnel_over_vlink</span> <b>(Alias name: tunnel-over-vlink)</b>  Enable/disable selection of which np6 chip the tunnel uses (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label692' href="javascript:ContentClick('label693', 'label692');" onmouseover="ContentPreview('label693');" onmouseout="ContentUnpreview('label693');" title="click to collapse or expand..."> more... </a>
 <div id="label693" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.5 -> v7.2.9</code>, <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_receive_unit</span> <b>(Alias name: max-receive-unit)</b>  Set the maximum packet size for receive, larger packets will be silently dropped. <span class="li-normal">type: int</span>
 <a id='label694' href="javascript:ContentClick('label695', 'label694');" onmouseover="ContentPreview('label695');" onmouseout="ContentUnpreview('label695');" title="click to collapse or expand..."> more... </a>
 <div id="label695" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">npu_tcam</span> <b>(Alias name: npu-tcam)</b>  Npu tcam. <span class="li-normal">type: list</span>
 <a id='label696' href="javascript:ContentClick('label697', 'label696');" onmouseover="ContentPreview('label697');" onmouseout="ContentUnpreview('label697');" title="click to collapse or expand..."> more... </a>
 <div id="label697" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">data</span> Data. <span class="li-normal">type: dict</span>
 <a id='label698' href="javascript:ContentClick('label699', 'label698');" onmouseover="ContentPreview('label699');" onmouseout="ContentUnpreview('label699');" title="click to collapse or expand..."> more... </a>
 <div id="label699" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">df</span> Tcam data ip flag df. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label700' href="javascript:ContentClick('label701', 'label700');" onmouseover="ContentPreview('label701');" onmouseout="ContentUnpreview('label701');" title="click to collapse or expand..."> more... </a>
 <div id="label701" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstip</span> Tcam data dst ipv4 address. <span class="li-normal">type: str</span>
 <a id='label702' href="javascript:ContentClick('label703', 'label702');" onmouseover="ContentPreview('label703');" onmouseout="ContentUnpreview('label703');" title="click to collapse or expand..."> more... </a>
 <div id="label703" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstipv6</span> Tcam data dst ipv6 address. <span class="li-normal">type: str</span>
 <a id='label704' href="javascript:ContentClick('label705', 'label704');" onmouseover="ContentPreview('label705');" onmouseout="ContentUnpreview('label705');" title="click to collapse or expand..."> more... </a>
 <div id="label705" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstmac</span> Tcam data dst macaddr. <span class="li-normal">type: str</span>
 <a id='label706' href="javascript:ContentClick('label707', 'label706');" onmouseover="ContentPreview('label707');" onmouseout="ContentUnpreview('label707');" title="click to collapse or expand..."> more... </a>
 <div id="label707" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstport</span> Tcam data l4 dst port. <span class="li-normal">type: int</span>
 <a id='label708' href="javascript:ContentClick('label709', 'label708');" onmouseover="ContentPreview('label709');" onmouseout="ContentUnpreview('label709');" title="click to collapse or expand..."> more... </a>
 <div id="label709" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ethertype</span> Tcam data ethertype. <span class="li-normal">type: str</span>
 <a id='label710' href="javascript:ContentClick('label711', 'label710');" onmouseover="ContentPreview('label711');" onmouseout="ContentUnpreview('label711');" title="click to collapse or expand..."> more... </a>
 <div id="label711" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ext_tag</span> <b>(Alias name: ext-tag)</b>  Tcam data extension tag. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label712' href="javascript:ContentClick('label713', 'label712');" onmouseover="ContentPreview('label713');" onmouseout="ContentUnpreview('label713');" title="click to collapse or expand..."> more... </a>
 <div id="label713" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_off</span> <b>(Alias name: frag-off)</b>  Tcam data ip flag fragment offset. <span class="li-normal">type: int</span>
 <a id='label714' href="javascript:ContentClick('label715', 'label714');" onmouseover="ContentPreview('label715');" onmouseout="ContentUnpreview('label715');" title="click to collapse or expand..."> more... </a>
 <div id="label715" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_buf_cnt</span> <b>(Alias name: gen-buf-cnt)</b>  Tcam data gen info buffer count. <span class="li-normal">type: int</span>
 <a id='label716' href="javascript:ContentClick('label717', 'label716');" onmouseover="ContentPreview('label717');" onmouseout="ContentUnpreview('label717');" title="click to collapse or expand..."> more... </a>
 <div id="label717" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_iv</span> <b>(Alias name: gen-iv)</b>  Tcam data gen info iv. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label718' href="javascript:ContentClick('label719', 'label718');" onmouseover="ContentPreview('label719');" onmouseout="ContentUnpreview('label719');" title="click to collapse or expand..."> more... </a>
 <div id="label719" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_l3_flags</span> <b>(Alias name: gen-l3-flags)</b>  Tcam data gen info l3 flags. <span class="li-normal">type: int</span>
 <a id='label720' href="javascript:ContentClick('label721', 'label720');" onmouseover="ContentPreview('label721');" onmouseout="ContentUnpreview('label721');" title="click to collapse or expand..."> more... </a>
 <div id="label721" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_l4_flags</span> <b>(Alias name: gen-l4-flags)</b>  Tcam data gen info l4 flags. <span class="li-normal">type: int</span>
 <a id='label722' href="javascript:ContentClick('label723', 'label722');" onmouseover="ContentPreview('label723');" onmouseout="ContentUnpreview('label723');" title="click to collapse or expand..."> more... </a>
 <div id="label723" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_pkt_ctrl</span> <b>(Alias name: gen-pkt-ctrl)</b>  Tcam data gen info packet control. <span class="li-normal">type: int</span>
 <a id='label724' href="javascript:ContentClick('label725', 'label724');" onmouseover="ContentPreview('label725');" onmouseout="ContentUnpreview('label725');" title="click to collapse or expand..."> more... </a>
 <div id="label725" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_pri</span> <b>(Alias name: gen-pri)</b>  Tcam data gen info priority. <span class="li-normal">type: int</span>
 <a id='label726' href="javascript:ContentClick('label727', 'label726');" onmouseover="ContentPreview('label727');" onmouseout="ContentUnpreview('label727');" title="click to collapse or expand..."> more... </a>
 <div id="label727" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_pri_v</span> <b>(Alias name: gen-pri-v)</b>  Tcam data gen info priority valid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label728' href="javascript:ContentClick('label729', 'label728');" onmouseover="ContentPreview('label729');" onmouseout="ContentUnpreview('label729');" title="click to collapse or expand..."> more... </a>
 <div id="label729" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_tv</span> <b>(Alias name: gen-tv)</b>  Tcam data gen info tv. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label730' href="javascript:ContentClick('label731', 'label730');" onmouseover="ContentPreview('label731');" onmouseout="ContentUnpreview('label731');" title="click to collapse or expand..."> more... </a>
 <div id="label731" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ihl</span> Tcam data ipv4 ihl. <span class="li-normal">type: int</span>
 <a id='label732' href="javascript:ContentClick('label733', 'label732');" onmouseover="ContentPreview('label733');" onmouseout="ContentUnpreview('label733');" title="click to collapse or expand..."> more... </a>
 <div id="label733" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip4_id</span> <b>(Alias name: ip4-id)</b>  Tcam data ipv4 id. <span class="li-normal">type: int</span>
 <a id='label734' href="javascript:ContentClick('label735', 'label734');" onmouseover="ContentPreview('label735');" onmouseout="ContentUnpreview('label735');" title="click to collapse or expand..."> more... </a>
 <div id="label735" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip6_fl</span> <b>(Alias name: ip6-fl)</b>  Tcam data ipv6 flow label. <span class="li-normal">type: int</span>
 <a id='label736' href="javascript:ContentClick('label737', 'label736');" onmouseover="ContentPreview('label737');" onmouseout="ContentUnpreview('label737');" title="click to collapse or expand..."> more... </a>
 <div id="label737" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipver</span> Tcam data ip header version. <span class="li-normal">type: int</span>
 <a id='label738' href="javascript:ContentClick('label739', 'label738');" onmouseover="ContentPreview('label739');" onmouseout="ContentUnpreview('label739');" title="click to collapse or expand..."> more... </a>
 <div id="label739" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd10</span> <b>(Alias name: l4-wd10)</b>  Tcam data l4 word10. <span class="li-normal">type: int</span>
 <a id='label740' href="javascript:ContentClick('label741', 'label740');" onmouseover="ContentPreview('label741');" onmouseout="ContentUnpreview('label741');" title="click to collapse or expand..."> more... </a>
 <div id="label741" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd11</span> <b>(Alias name: l4-wd11)</b>  Tcam data l4 word11. <span class="li-normal">type: int</span>
 <a id='label742' href="javascript:ContentClick('label743', 'label742');" onmouseover="ContentPreview('label743');" onmouseout="ContentUnpreview('label743');" title="click to collapse or expand..."> more... </a>
 <div id="label743" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd8</span> <b>(Alias name: l4-wd8)</b>  Tcam data l4 word8. <span class="li-normal">type: int</span>
 <a id='label744' href="javascript:ContentClick('label745', 'label744');" onmouseover="ContentPreview('label745');" onmouseout="ContentUnpreview('label745');" title="click to collapse or expand..."> more... </a>
 <div id="label745" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd9</span> <b>(Alias name: l4-wd9)</b>  Tcam data l4 word9. <span class="li-normal">type: int</span>
 <a id='label746' href="javascript:ContentClick('label747', 'label746');" onmouseover="ContentPreview('label747');" onmouseout="ContentUnpreview('label747');" title="click to collapse or expand..."> more... </a>
 <div id="label747" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mf</span> Tcam data ip flag mf. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label748' href="javascript:ContentClick('label749', 'label748');" onmouseover="ContentPreview('label749');" onmouseout="ContentUnpreview('label749');" title="click to collapse or expand..."> more... </a>
 <div id="label749" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protocol</span> Tcam data ip protocol. <span class="li-normal">type: int</span>
 <a id='label750' href="javascript:ContentClick('label751', 'label750');" onmouseover="ContentPreview('label751');" onmouseout="ContentUnpreview('label751');" title="click to collapse or expand..."> more... </a>
 <div id="label751" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">slink</span> Tcam data sublink. <span class="li-normal">type: int</span>
 <a id='label752' href="javascript:ContentClick('label753', 'label752');" onmouseover="ContentPreview('label753');" onmouseout="ContentUnpreview('label753');" title="click to collapse or expand..."> more... </a>
 <div id="label753" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">smac_change</span> <b>(Alias name: smac-change)</b>  Tcam data source mac change. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label754' href="javascript:ContentClick('label755', 'label754');" onmouseover="ContentPreview('label755');" onmouseout="ContentUnpreview('label755');" title="click to collapse or expand..."> more... </a>
 <div id="label755" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sp</span> Tcam data source port. <span class="li-normal">type: int</span>
 <a id='label756' href="javascript:ContentClick('label757', 'label756');" onmouseover="ContentPreview('label757');" onmouseout="ContentUnpreview('label757');" title="click to collapse or expand..."> more... </a>
 <div id="label757" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">src_cfi</span> <b>(Alias name: src-cfi)</b>  Tcam data source cfi. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label758' href="javascript:ContentClick('label759', 'label758');" onmouseover="ContentPreview('label759');" onmouseout="ContentUnpreview('label759');" title="click to collapse or expand..."> more... </a>
 <div id="label759" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">src_prio</span> <b>(Alias name: src-prio)</b>  Tcam data source priority. <span class="li-normal">type: int</span>
 <a id='label760' href="javascript:ContentClick('label761', 'label760');" onmouseover="ContentPreview('label761');" onmouseout="ContentUnpreview('label761');" title="click to collapse or expand..."> more... </a>
 <div id="label761" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">src_updt</span> <b>(Alias name: src-updt)</b>  Tcam data source update. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label762' href="javascript:ContentClick('label763', 'label762');" onmouseover="ContentPreview('label763');" onmouseout="ContentUnpreview('label763');" title="click to collapse or expand..."> more... </a>
 <div id="label763" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcip</span> Tcam data src ipv4 address. <span class="li-normal">type: str</span>
 <a id='label764' href="javascript:ContentClick('label765', 'label764');" onmouseover="ContentPreview('label765');" onmouseout="ContentUnpreview('label765');" title="click to collapse or expand..."> more... </a>
 <div id="label765" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcipv6</span> Tcam data src ipv6 address. <span class="li-normal">type: str</span>
 <a id='label766' href="javascript:ContentClick('label767', 'label766');" onmouseover="ContentPreview('label767');" onmouseout="ContentUnpreview('label767');" title="click to collapse or expand..."> more... </a>
 <div id="label767" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcmac</span> Tcam data src macaddr. <span class="li-normal">type: str</span>
 <a id='label768' href="javascript:ContentClick('label769', 'label768');" onmouseover="ContentPreview('label769');" onmouseout="ContentUnpreview('label769');" title="click to collapse or expand..."> more... </a>
 <div id="label769" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcport</span> Tcam data l4 src port. <span class="li-normal">type: int</span>
 <a id='label770' href="javascript:ContentClick('label771', 'label770');" onmouseover="ContentPreview('label771');" onmouseout="ContentUnpreview('label771');" title="click to collapse or expand..."> more... </a>
 <div id="label771" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">svid</span> Tcam data source vid. <span class="li-normal">type: int</span>
 <a id='label772' href="javascript:ContentClick('label773', 'label772');" onmouseover="ContentPreview('label773');" onmouseout="ContentUnpreview('label773');" title="click to collapse or expand..."> more... </a>
 <div id="label773" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_ack</span> <b>(Alias name: tcp-ack)</b>  Tcam data tcp flag ack. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label774' href="javascript:ContentClick('label775', 'label774');" onmouseover="ContentPreview('label775');" onmouseout="ContentUnpreview('label775');" title="click to collapse or expand..."> more... </a>
 <div id="label775" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_cwr</span> <b>(Alias name: tcp-cwr)</b>  Tcam data tcp flag cwr. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label776' href="javascript:ContentClick('label777', 'label776');" onmouseover="ContentPreview('label777');" onmouseout="ContentUnpreview('label777');" title="click to collapse or expand..."> more... </a>
 <div id="label777" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_ece</span> <b>(Alias name: tcp-ece)</b>  Tcam data tcp flag ece. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label778' href="javascript:ContentClick('label779', 'label778');" onmouseover="ContentPreview('label779');" onmouseout="ContentUnpreview('label779');" title="click to collapse or expand..."> more... </a>
 <div id="label779" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_fin</span> <b>(Alias name: tcp-fin)</b>  Tcam data tcp flag fin. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label780' href="javascript:ContentClick('label781', 'label780');" onmouseover="ContentPreview('label781');" onmouseout="ContentUnpreview('label781');" title="click to collapse or expand..."> more... </a>
 <div id="label781" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_push</span> <b>(Alias name: tcp-push)</b>  Tcam data tcp flag push. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label782' href="javascript:ContentClick('label783', 'label782');" onmouseover="ContentPreview('label783');" onmouseout="ContentUnpreview('label783');" title="click to collapse or expand..."> more... </a>
 <div id="label783" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_rst</span> <b>(Alias name: tcp-rst)</b>  Tcam data tcp flag rst. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label784' href="javascript:ContentClick('label785', 'label784');" onmouseover="ContentPreview('label785');" onmouseout="ContentUnpreview('label785');" title="click to collapse or expand..."> more... </a>
 <div id="label785" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_syn</span> <b>(Alias name: tcp-syn)</b>  Tcam data tcp flag syn. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label786' href="javascript:ContentClick('label787', 'label786');" onmouseover="ContentPreview('label787');" onmouseout="ContentUnpreview('label787');" title="click to collapse or expand..."> more... </a>
 <div id="label787" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_urg</span> <b>(Alias name: tcp-urg)</b>  Tcam data tcp flag urg. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label788' href="javascript:ContentClick('label789', 'label788');" onmouseover="ContentPreview('label789');" onmouseout="ContentUnpreview('label789');" title="click to collapse or expand..."> more... </a>
 <div id="label789" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_cfi</span> <b>(Alias name: tgt-cfi)</b>  Tcam data target cfi. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label790' href="javascript:ContentClick('label791', 'label790');" onmouseover="ContentPreview('label791');" onmouseout="ContentUnpreview('label791');" title="click to collapse or expand..."> more... </a>
 <div id="label791" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_prio</span> <b>(Alias name: tgt-prio)</b>  Tcam data target priority. <span class="li-normal">type: int</span>
 <a id='label792' href="javascript:ContentClick('label793', 'label792');" onmouseover="ContentPreview('label793');" onmouseout="ContentUnpreview('label793');" title="click to collapse or expand..."> more... </a>
 <div id="label793" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_updt</span> <b>(Alias name: tgt-updt)</b>  Tcam data target port update. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label794' href="javascript:ContentClick('label795', 'label794');" onmouseover="ContentPreview('label795');" onmouseout="ContentUnpreview('label795');" title="click to collapse or expand..."> more... </a>
 <div id="label795" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_v</span> <b>(Alias name: tgt-v)</b>  Tcam data target valid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label796' href="javascript:ContentClick('label797', 'label796');" onmouseover="ContentPreview('label797');" onmouseout="ContentUnpreview('label797');" title="click to collapse or expand..."> more... </a>
 <div id="label797" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tos</span> Tcam data ip tos. <span class="li-normal">type: int</span>
 <a id='label798' href="javascript:ContentClick('label799', 'label798');" onmouseover="ContentPreview('label799');" onmouseout="ContentUnpreview('label799');" title="click to collapse or expand..."> more... </a>
 <div id="label799" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tp</span> Tcam data target port. <span class="li-normal">type: int</span>
 <a id='label800' href="javascript:ContentClick('label801', 'label800');" onmouseover="ContentPreview('label801');" onmouseout="ContentUnpreview('label801');" title="click to collapse or expand..."> more... </a>
 <div id="label801" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ttl</span> Tcam data ip ttl. <span class="li-normal">type: int</span>
 <a id='label802' href="javascript:ContentClick('label803', 'label802');" onmouseover="ContentPreview('label803');" onmouseout="ContentUnpreview('label803');" title="click to collapse or expand..."> more... </a>
 <div id="label803" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tvid</span> Tcam data target vid. <span class="li-normal">type: int</span>
 <a id='label804' href="javascript:ContentClick('label805', 'label804');" onmouseover="ContentPreview('label805');" onmouseout="ContentUnpreview('label805');" title="click to collapse or expand..."> more... </a>
 <div id="label805" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vdid</span> Tcam data vdom id. <span class="li-normal">type: int</span>
 <a id='label806' href="javascript:ContentClick('label807', 'label806');" onmouseover="ContentPreview('label807');" onmouseout="ContentUnpreview('label807');" title="click to collapse or expand..."> more... </a>
 <div id="label807" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">dbg_dump</span> <b>(Alias name: dbg-dump)</b>  Debug driver dump data/mask pdq. <span class="li-normal">type: int</span>
 <a id='label808' href="javascript:ContentClick('label809', 'label808');" onmouseover="ContentPreview('label809');" onmouseout="ContentUnpreview('label809');" title="click to collapse or expand..."> more... </a>
 <div id="label809" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mask</span> Mask. <span class="li-normal">type: dict</span>
 <a id='label810' href="javascript:ContentClick('label811', 'label810');" onmouseover="ContentPreview('label811');" onmouseout="ContentUnpreview('label811');" title="click to collapse or expand..."> more... </a>
 <div id="label811" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">df</span> Tcam mask ip flag df. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label812' href="javascript:ContentClick('label813', 'label812');" onmouseover="ContentPreview('label813');" onmouseout="ContentUnpreview('label813');" title="click to collapse or expand..."> more... </a>
 <div id="label813" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstip</span> Tcam mask dst ipv4 address. <span class="li-normal">type: str</span>
 <a id='label814' href="javascript:ContentClick('label815', 'label814');" onmouseover="ContentPreview('label815');" onmouseout="ContentUnpreview('label815');" title="click to collapse or expand..."> more... </a>
 <div id="label815" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstipv6</span> Tcam mask dst ipv6 address. <span class="li-normal">type: str</span>
 <a id='label816' href="javascript:ContentClick('label817', 'label816');" onmouseover="ContentPreview('label817');" onmouseout="ContentUnpreview('label817');" title="click to collapse or expand..."> more... </a>
 <div id="label817" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstmac</span> Tcam mask dst macaddr. <span class="li-normal">type: str</span>
 <a id='label818' href="javascript:ContentClick('label819', 'label818');" onmouseover="ContentPreview('label819');" onmouseout="ContentUnpreview('label819');" title="click to collapse or expand..."> more... </a>
 <div id="label819" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dstport</span> Tcam mask l4 dst port. <span class="li-normal">type: int</span>
 <a id='label820' href="javascript:ContentClick('label821', 'label820');" onmouseover="ContentPreview('label821');" onmouseout="ContentUnpreview('label821');" title="click to collapse or expand..."> more... </a>
 <div id="label821" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ethertype</span> Tcam mask ethertype. <span class="li-normal">type: str</span>
 <a id='label822' href="javascript:ContentClick('label823', 'label822');" onmouseover="ContentPreview('label823');" onmouseout="ContentUnpreview('label823');" title="click to collapse or expand..."> more... </a>
 <div id="label823" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ext_tag</span> <b>(Alias name: ext-tag)</b>  Tcam mask extension tag. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label824' href="javascript:ContentClick('label825', 'label824');" onmouseover="ContentPreview('label825');" onmouseout="ContentUnpreview('label825');" title="click to collapse or expand..."> more... </a>
 <div id="label825" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_off</span> <b>(Alias name: frag-off)</b>  Tcam data ip flag fragment offset. <span class="li-normal">type: int</span>
 <a id='label826' href="javascript:ContentClick('label827', 'label826');" onmouseover="ContentPreview('label827');" onmouseout="ContentUnpreview('label827');" title="click to collapse or expand..."> more... </a>
 <div id="label827" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_buf_cnt</span> <b>(Alias name: gen-buf-cnt)</b>  Tcam mask gen info buffer count. <span class="li-normal">type: int</span>
 <a id='label828' href="javascript:ContentClick('label829', 'label828');" onmouseover="ContentPreview('label829');" onmouseout="ContentUnpreview('label829');" title="click to collapse or expand..."> more... </a>
 <div id="label829" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_iv</span> <b>(Alias name: gen-iv)</b>  Tcam mask gen info iv. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label830' href="javascript:ContentClick('label831', 'label830');" onmouseover="ContentPreview('label831');" onmouseout="ContentUnpreview('label831');" title="click to collapse or expand..."> more... </a>
 <div id="label831" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_l3_flags</span> <b>(Alias name: gen-l3-flags)</b>  Tcam mask gen info l3 flags. <span class="li-normal">type: int</span>
 <a id='label832' href="javascript:ContentClick('label833', 'label832');" onmouseover="ContentPreview('label833');" onmouseout="ContentUnpreview('label833');" title="click to collapse or expand..."> more... </a>
 <div id="label833" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_l4_flags</span> <b>(Alias name: gen-l4-flags)</b>  Tcam mask gen info l4 flags. <span class="li-normal">type: int</span>
 <a id='label834' href="javascript:ContentClick('label835', 'label834');" onmouseover="ContentPreview('label835');" onmouseout="ContentUnpreview('label835');" title="click to collapse or expand..."> more... </a>
 <div id="label835" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_pkt_ctrl</span> <b>(Alias name: gen-pkt-ctrl)</b>  Tcam mask gen info packet control. <span class="li-normal">type: int</span>
 <a id='label836' href="javascript:ContentClick('label837', 'label836');" onmouseover="ContentPreview('label837');" onmouseout="ContentUnpreview('label837');" title="click to collapse or expand..."> more... </a>
 <div id="label837" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_pri</span> <b>(Alias name: gen-pri)</b>  Tcam mask gen info priority. <span class="li-normal">type: int</span>
 <a id='label838' href="javascript:ContentClick('label839', 'label838');" onmouseover="ContentPreview('label839');" onmouseout="ContentUnpreview('label839');" title="click to collapse or expand..."> more... </a>
 <div id="label839" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_pri_v</span> <b>(Alias name: gen-pri-v)</b>  Tcam mask gen info priority valid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label840' href="javascript:ContentClick('label841', 'label840');" onmouseover="ContentPreview('label841');" onmouseout="ContentUnpreview('label841');" title="click to collapse or expand..."> more... </a>
 <div id="label841" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">gen_tv</span> <b>(Alias name: gen-tv)</b>  Tcam mask gen info tv. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label842' href="javascript:ContentClick('label843', 'label842');" onmouseover="ContentPreview('label843');" onmouseout="ContentUnpreview('label843');" title="click to collapse or expand..."> more... </a>
 <div id="label843" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ihl</span> Tcam mask ipv4 ihl. <span class="li-normal">type: int</span>
 <a id='label844' href="javascript:ContentClick('label845', 'label844');" onmouseover="ContentPreview('label845');" onmouseout="ContentUnpreview('label845');" title="click to collapse or expand..."> more... </a>
 <div id="label845" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip4_id</span> <b>(Alias name: ip4-id)</b>  Tcam mask ipv4 id. <span class="li-normal">type: int</span>
 <a id='label846' href="javascript:ContentClick('label847', 'label846');" onmouseover="ContentPreview('label847');" onmouseout="ContentUnpreview('label847');" title="click to collapse or expand..."> more... </a>
 <div id="label847" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip6_fl</span> <b>(Alias name: ip6-fl)</b>  Tcam mask ipv6 flow label. <span class="li-normal">type: int</span>
 <a id='label848' href="javascript:ContentClick('label849', 'label848');" onmouseover="ContentPreview('label849');" onmouseout="ContentUnpreview('label849');" title="click to collapse or expand..."> more... </a>
 <div id="label849" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipver</span> Tcam mask ip header version. <span class="li-normal">type: int</span>
 <a id='label850' href="javascript:ContentClick('label851', 'label850');" onmouseover="ContentPreview('label851');" onmouseout="ContentUnpreview('label851');" title="click to collapse or expand..."> more... </a>
 <div id="label851" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd10</span> <b>(Alias name: l4-wd10)</b>  Tcam mask l4 word10. <span class="li-normal">type: int</span>
 <a id='label852' href="javascript:ContentClick('label853', 'label852');" onmouseover="ContentPreview('label853');" onmouseout="ContentUnpreview('label853');" title="click to collapse or expand..."> more... </a>
 <div id="label853" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd11</span> <b>(Alias name: l4-wd11)</b>  Tcam mask l4 word11. <span class="li-normal">type: int</span>
 <a id='label854' href="javascript:ContentClick('label855', 'label854');" onmouseover="ContentPreview('label855');" onmouseout="ContentUnpreview('label855');" title="click to collapse or expand..."> more... </a>
 <div id="label855" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd8</span> <b>(Alias name: l4-wd8)</b>  Tcam mask l4 word8. <span class="li-normal">type: int</span>
 <a id='label856' href="javascript:ContentClick('label857', 'label856');" onmouseover="ContentPreview('label857');" onmouseout="ContentUnpreview('label857');" title="click to collapse or expand..."> more... </a>
 <div id="label857" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">l4_wd9</span> <b>(Alias name: l4-wd9)</b>  Tcam mask l4 word9. <span class="li-normal">type: int</span>
 <a id='label858' href="javascript:ContentClick('label859', 'label858');" onmouseover="ContentPreview('label859');" onmouseout="ContentUnpreview('label859');" title="click to collapse or expand..."> more... </a>
 <div id="label859" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mf</span> Tcam mask ip flag mf. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label860' href="javascript:ContentClick('label861', 'label860');" onmouseover="ContentPreview('label861');" onmouseout="ContentUnpreview('label861');" title="click to collapse or expand..."> more... </a>
 <div id="label861" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protocol</span> Tcam mask ip protocol. <span class="li-normal">type: int</span>
 <a id='label862' href="javascript:ContentClick('label863', 'label862');" onmouseover="ContentPreview('label863');" onmouseout="ContentUnpreview('label863');" title="click to collapse or expand..."> more... </a>
 <div id="label863" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">slink</span> Tcam mask sublink. <span class="li-normal">type: int</span>
 <a id='label864' href="javascript:ContentClick('label865', 'label864');" onmouseover="ContentPreview('label865');" onmouseout="ContentUnpreview('label865');" title="click to collapse or expand..."> more... </a>
 <div id="label865" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">smac_change</span> <b>(Alias name: smac-change)</b>  Tcam mask source mac change. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label866' href="javascript:ContentClick('label867', 'label866');" onmouseover="ContentPreview('label867');" onmouseout="ContentUnpreview('label867');" title="click to collapse or expand..."> more... </a>
 <div id="label867" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sp</span> Tcam mask source port. <span class="li-normal">type: int</span>
 <a id='label868' href="javascript:ContentClick('label869', 'label868');" onmouseover="ContentPreview('label869');" onmouseout="ContentUnpreview('label869');" title="click to collapse or expand..."> more... </a>
 <div id="label869" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">src_cfi</span> <b>(Alias name: src-cfi)</b>  Tcam mask source cfi. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label870' href="javascript:ContentClick('label871', 'label870');" onmouseover="ContentPreview('label871');" onmouseout="ContentUnpreview('label871');" title="click to collapse or expand..."> more... </a>
 <div id="label871" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">src_prio</span> <b>(Alias name: src-prio)</b>  Tcam mask source priority. <span class="li-normal">type: int</span>
 <a id='label872' href="javascript:ContentClick('label873', 'label872');" onmouseover="ContentPreview('label873');" onmouseout="ContentUnpreview('label873');" title="click to collapse or expand..."> more... </a>
 <div id="label873" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">src_updt</span> <b>(Alias name: src-updt)</b>  Tcam mask source update. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label874' href="javascript:ContentClick('label875', 'label874');" onmouseover="ContentPreview('label875');" onmouseout="ContentUnpreview('label875');" title="click to collapse or expand..."> more... </a>
 <div id="label875" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcip</span> Tcam mask src ipv4 address. <span class="li-normal">type: str</span>
 <a id='label876' href="javascript:ContentClick('label877', 'label876');" onmouseover="ContentPreview('label877');" onmouseout="ContentUnpreview('label877');" title="click to collapse or expand..."> more... </a>
 <div id="label877" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcipv6</span> Tcam mask src ipv6 address. <span class="li-normal">type: str</span>
 <a id='label878' href="javascript:ContentClick('label879', 'label878');" onmouseover="ContentPreview('label879');" onmouseout="ContentUnpreview('label879');" title="click to collapse or expand..."> more... </a>
 <div id="label879" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcmac</span> Tcam mask src macaddr. <span class="li-normal">type: str</span>
 <a id='label880' href="javascript:ContentClick('label881', 'label880');" onmouseover="ContentPreview('label881');" onmouseout="ContentUnpreview('label881');" title="click to collapse or expand..."> more... </a>
 <div id="label881" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">srcport</span> Tcam mask l4 src port. <span class="li-normal">type: int</span>
 <a id='label882' href="javascript:ContentClick('label883', 'label882');" onmouseover="ContentPreview('label883');" onmouseout="ContentUnpreview('label883');" title="click to collapse or expand..."> more... </a>
 <div id="label883" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">svid</span> Tcam mask source vid. <span class="li-normal">type: int</span>
 <a id='label884' href="javascript:ContentClick('label885', 'label884');" onmouseover="ContentPreview('label885');" onmouseout="ContentUnpreview('label885');" title="click to collapse or expand..."> more... </a>
 <div id="label885" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_ack</span> <b>(Alias name: tcp-ack)</b>  Tcam mask tcp flag ack. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label886' href="javascript:ContentClick('label887', 'label886');" onmouseover="ContentPreview('label887');" onmouseout="ContentUnpreview('label887');" title="click to collapse or expand..."> more... </a>
 <div id="label887" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_cwr</span> <b>(Alias name: tcp-cwr)</b>  Tcam mask tcp flag cwr. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label888' href="javascript:ContentClick('label889', 'label888');" onmouseover="ContentPreview('label889');" onmouseout="ContentUnpreview('label889');" title="click to collapse or expand..."> more... </a>
 <div id="label889" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_ece</span> <b>(Alias name: tcp-ece)</b>  Tcam mask tcp flag ece. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label890' href="javascript:ContentClick('label891', 'label890');" onmouseover="ContentPreview('label891');" onmouseout="ContentUnpreview('label891');" title="click to collapse or expand..."> more... </a>
 <div id="label891" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_fin</span> <b>(Alias name: tcp-fin)</b>  Tcam mask tcp flag fin. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label892' href="javascript:ContentClick('label893', 'label892');" onmouseover="ContentPreview('label893');" onmouseout="ContentUnpreview('label893');" title="click to collapse or expand..."> more... </a>
 <div id="label893" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_push</span> <b>(Alias name: tcp-push)</b>  Tcam mask tcp flag push. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label894' href="javascript:ContentClick('label895', 'label894');" onmouseover="ContentPreview('label895');" onmouseout="ContentUnpreview('label895');" title="click to collapse or expand..."> more... </a>
 <div id="label895" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_rst</span> <b>(Alias name: tcp-rst)</b>  Tcam mask tcp flag rst. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label896' href="javascript:ContentClick('label897', 'label896');" onmouseover="ContentPreview('label897');" onmouseout="ContentUnpreview('label897');" title="click to collapse or expand..."> more... </a>
 <div id="label897" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_syn</span> <b>(Alias name: tcp-syn)</b>  Tcam mask tcp flag syn. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label898' href="javascript:ContentClick('label899', 'label898');" onmouseover="ContentPreview('label899');" onmouseout="ContentUnpreview('label899');" title="click to collapse or expand..."> more... </a>
 <div id="label899" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tcp_urg</span> <b>(Alias name: tcp-urg)</b>  Tcam mask tcp flag urg. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label900' href="javascript:ContentClick('label901', 'label900');" onmouseover="ContentPreview('label901');" onmouseout="ContentUnpreview('label901');" title="click to collapse or expand..."> more... </a>
 <div id="label901" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_cfi</span> <b>(Alias name: tgt-cfi)</b>  Tcam mask target cfi. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label902' href="javascript:ContentClick('label903', 'label902');" onmouseover="ContentPreview('label903');" onmouseout="ContentUnpreview('label903');" title="click to collapse or expand..."> more... </a>
 <div id="label903" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_prio</span> <b>(Alias name: tgt-prio)</b>  Tcam mask target priority. <span class="li-normal">type: int</span>
 <a id='label904' href="javascript:ContentClick('label905', 'label904');" onmouseover="ContentPreview('label905');" onmouseout="ContentUnpreview('label905');" title="click to collapse or expand..."> more... </a>
 <div id="label905" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_updt</span> <b>(Alias name: tgt-updt)</b>  Tcam mask target port update. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label906' href="javascript:ContentClick('label907', 'label906');" onmouseover="ContentPreview('label907');" onmouseout="ContentUnpreview('label907');" title="click to collapse or expand..."> more... </a>
 <div id="label907" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgt_v</span> <b>(Alias name: tgt-v)</b>  Tcam mask target valid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [invalid, valid]</span> 
 <a id='label908' href="javascript:ContentClick('label909', 'label908');" onmouseover="ContentPreview('label909');" onmouseout="ContentUnpreview('label909');" title="click to collapse or expand..."> more... </a>
 <div id="label909" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tos</span> Tcam mask ip tos. <span class="li-normal">type: int</span>
 <a id='label910' href="javascript:ContentClick('label911', 'label910');" onmouseover="ContentPreview('label911');" onmouseout="ContentUnpreview('label911');" title="click to collapse or expand..."> more... </a>
 <div id="label911" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tp</span> Tcam mask target port. <span class="li-normal">type: int</span>
 <a id='label912' href="javascript:ContentClick('label913', 'label912');" onmouseover="ContentPreview('label913');" onmouseout="ContentUnpreview('label913');" title="click to collapse or expand..."> more... </a>
 <div id="label913" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ttl</span> Tcam mask ip ttl. <span class="li-normal">type: int</span>
 <a id='label914' href="javascript:ContentClick('label915', 'label914');" onmouseover="ContentPreview('label915');" onmouseout="ContentUnpreview('label915');" title="click to collapse or expand..."> more... </a>
 <div id="label915" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tvid</span> Tcam mask target vid. <span class="li-normal">type: int</span>
 <a id='label916' href="javascript:ContentClick('label917', 'label916');" onmouseover="ContentPreview('label917');" onmouseout="ContentUnpreview('label917');" title="click to collapse or expand..."> more... </a>
 <div id="label917" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vdid</span> Tcam mask vdom id. <span class="li-normal">type: int</span>
 <a id='label918' href="javascript:ContentClick('label919', 'label918');" onmouseover="ContentPreview('label919');" onmouseout="ContentUnpreview('label919');" title="click to collapse or expand..."> more... </a>
 <div id="label919" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">mir_act</span> <b>(Alias name: mir-act)</b>  Mir act. <span class="li-normal">type: dict</span>
 <a id='label920' href="javascript:ContentClick('label921', 'label920');" onmouseover="ContentPreview('label921');" onmouseout="ContentUnpreview('label921');" title="click to collapse or expand..."> more... </a>
 <div id="label921" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">vlif</span> Tcam mirror action vlif. <span class="li-normal">type: int</span>
 <a id='label922' href="javascript:ContentClick('label923', 'label922');" onmouseover="ContentPreview('label923');" onmouseout="ContentUnpreview('label923');" title="click to collapse or expand..."> more... </a>
 <div id="label923" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">name</span> Npu tcam policies name. <span class="li-normal">type: str</span>
 <a id='label924' href="javascript:ContentClick('label925', 'label924');" onmouseover="ContentPreview('label925');" onmouseout="ContentUnpreview('label925');" title="click to collapse or expand..."> more... </a>
 <div id="label925" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">oid</span> Npu tcam oid. <span class="li-normal">type: int</span>
 <a id='label926' href="javascript:ContentClick('label927', 'label926');" onmouseover="ContentPreview('label927');" onmouseout="ContentUnpreview('label927');" title="click to collapse or expand..."> more... </a>
 <div id="label927" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">pri_act</span> <b>(Alias name: pri-act)</b>  Pri act. <span class="li-normal">type: dict</span>
 <a id='label928' href="javascript:ContentClick('label929', 'label928');" onmouseover="ContentPreview('label929');" onmouseout="ContentUnpreview('label929');" title="click to collapse or expand..."> more... </a>
 <div id="label929" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">priority</span> Tcam priority action priority. <span class="li-normal">type: int</span>
 <a id='label930' href="javascript:ContentClick('label931', 'label930');" onmouseover="ContentPreview('label931');" onmouseout="ContentUnpreview('label931');" title="click to collapse or expand..."> more... </a>
 <div id="label931" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">weight</span> Tcam priority action weight. <span class="li-normal">type: int</span>
 <a id='label932' href="javascript:ContentClick('label933', 'label932');" onmouseover="ContentPreview('label933');" onmouseout="ContentUnpreview('label933');" title="click to collapse or expand..."> more... </a>
 <div id="label933" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">sact</span> Sact. <span class="li-normal">type: dict</span>
 <a id='label934' href="javascript:ContentClick('label935', 'label934');" onmouseover="ContentPreview('label935');" onmouseout="ContentUnpreview('label935');" title="click to collapse or expand..."> more... </a>
 <div id="label935" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">act</span> Tcam sact act. <span class="li-normal">type: int</span>
 <a id='label936' href="javascript:ContentClick('label937', 'label936');" onmouseover="ContentPreview('label937');" onmouseout="ContentUnpreview('label937');" title="click to collapse or expand..."> more... </a>
 <div id="label937" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">act_v</span> <b>(Alias name: act-v)</b>  Enable to set sact act. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label938' href="javascript:ContentClick('label939', 'label938');" onmouseover="ContentPreview('label939');" onmouseout="ContentUnpreview('label939');" title="click to collapse or expand..."> more... </a>
 <div id="label939" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bmproc</span> Tcam sact bmproc. <span class="li-normal">type: int</span>
 <a id='label940' href="javascript:ContentClick('label941', 'label940');" onmouseover="ContentPreview('label941');" onmouseout="ContentUnpreview('label941');" title="click to collapse or expand..."> more... </a>
 <div id="label941" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bmproc_v</span> <b>(Alias name: bmproc-v)</b>  Enable to set sact bmproc. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label942' href="javascript:ContentClick('label943', 'label942');" onmouseover="ContentPreview('label943');" onmouseout="ContentUnpreview('label943');" title="click to collapse or expand..."> more... </a>
 <div id="label943" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">df_lif</span> <b>(Alias name: df-lif)</b>  Tcam sact df-lif. <span class="li-normal">type: int</span>
 <a id='label944' href="javascript:ContentClick('label945', 'label944');" onmouseover="ContentPreview('label945');" onmouseout="ContentUnpreview('label945');" title="click to collapse or expand..."> more... </a>
 <div id="label945" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">df_lif_v</span> <b>(Alias name: df-lif-v)</b>  Enable to set sact df-lif. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label946' href="javascript:ContentClick('label947', 'label946');" onmouseover="ContentPreview('label947');" onmouseout="ContentUnpreview('label947');" title="click to collapse or expand..."> more... </a>
 <div id="label947" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dfr</span> Tcam sact dfr. <span class="li-normal">type: int</span>
 <a id='label948' href="javascript:ContentClick('label949', 'label948');" onmouseover="ContentPreview('label949');" onmouseout="ContentUnpreview('label949');" title="click to collapse or expand..."> more... </a>
 <div id="label949" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dfr_v</span> <b>(Alias name: dfr-v)</b>  Enable to set sact dfr. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label950' href="javascript:ContentClick('label951', 'label950');" onmouseover="ContentPreview('label951');" onmouseout="ContentUnpreview('label951');" title="click to collapse or expand..."> more... </a>
 <div id="label951" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dmac_skip</span> <b>(Alias name: dmac-skip)</b>  Tcam sact dmac-skip. <span class="li-normal">type: int</span>
 <a id='label952' href="javascript:ContentClick('label953', 'label952');" onmouseover="ContentPreview('label953');" onmouseout="ContentUnpreview('label953');" title="click to collapse or expand..."> more... </a>
 <div id="label953" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dmac_skip_v</span> <b>(Alias name: dmac-skip-v)</b>  Enable to set sact dmac-skip. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label954' href="javascript:ContentClick('label955', 'label954');" onmouseover="ContentPreview('label955');" onmouseout="ContentUnpreview('label955');" title="click to collapse or expand..."> more... </a>
 <div id="label955" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dosen</span> Tcam sact dosen. <span class="li-normal">type: int</span>
 <a id='label956' href="javascript:ContentClick('label957', 'label956');" onmouseover="ContentPreview('label957');" onmouseout="ContentUnpreview('label957');" title="click to collapse or expand..."> more... </a>
 <div id="label957" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dosen_v</span> <b>(Alias name: dosen-v)</b>  Enable to set sact dosen. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label958' href="javascript:ContentClick('label959', 'label958');" onmouseover="ContentPreview('label959');" onmouseout="ContentUnpreview('label959');" title="click to collapse or expand..."> more... </a>
 <div id="label959" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">espff_proc</span> <b>(Alias name: espff-proc)</b>  Tcam sact espff-proc. <span class="li-normal">type: int</span>
 <a id='label960' href="javascript:ContentClick('label961', 'label960');" onmouseover="ContentPreview('label961');" onmouseout="ContentUnpreview('label961');" title="click to collapse or expand..."> more... </a>
 <div id="label961" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">espff_proc_v</span> <b>(Alias name: espff-proc-v)</b>  Enable to set sact espff-proc. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label962' href="javascript:ContentClick('label963', 'label962');" onmouseover="ContentPreview('label963');" onmouseout="ContentUnpreview('label963');" title="click to collapse or expand..."> more... </a>
 <div id="label963" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">etype_pid</span> <b>(Alias name: etype-pid)</b>  Tcam sact etype-pid. <span class="li-normal">type: int</span>
 <a id='label964' href="javascript:ContentClick('label965', 'label964');" onmouseover="ContentPreview('label965');" onmouseout="ContentUnpreview('label965');" title="click to collapse or expand..."> more... </a>
 <div id="label965" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">etype_pid_v</span> <b>(Alias name: etype-pid-v)</b>  Enable to set sact etype-pid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label966' href="javascript:ContentClick('label967', 'label966');" onmouseover="ContentPreview('label967');" onmouseout="ContentUnpreview('label967');" title="click to collapse or expand..."> more... </a>
 <div id="label967" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_proc</span> <b>(Alias name: frag-proc)</b>  Tcam sact frag-proc. <span class="li-normal">type: int</span>
 <a id='label968' href="javascript:ContentClick('label969', 'label968');" onmouseover="ContentPreview('label969');" onmouseout="ContentUnpreview('label969');" title="click to collapse or expand..."> more... </a>
 <div id="label969" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_proc_v</span> <b>(Alias name: frag-proc-v)</b>  Enable to set sact frag-proc. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label970' href="javascript:ContentClick('label971', 'label970');" onmouseover="ContentPreview('label971');" onmouseout="ContentUnpreview('label971');" title="click to collapse or expand..."> more... </a>
 <div id="label971" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fwd</span> Tcam sact fwd. <span class="li-normal">type: int</span>
 <a id='label972' href="javascript:ContentClick('label973', 'label972');" onmouseover="ContentPreview('label973');" onmouseout="ContentUnpreview('label973');" title="click to collapse or expand..."> more... </a>
 <div id="label973" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fwd_lif</span> <b>(Alias name: fwd-lif)</b>  Tcam sact fwd-lif. <span class="li-normal">type: int</span>
 <a id='label974' href="javascript:ContentClick('label975', 'label974');" onmouseover="ContentPreview('label975');" onmouseout="ContentUnpreview('label975');" title="click to collapse or expand..."> more... </a>
 <div id="label975" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fwd_lif_v</span> <b>(Alias name: fwd-lif-v)</b>  Enable to set sact fwd-lif. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label976' href="javascript:ContentClick('label977', 'label976');" onmouseover="ContentPreview('label977');" onmouseout="ContentUnpreview('label977');" title="click to collapse or expand..."> more... </a>
 <div id="label977" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fwd_tvid</span> <b>(Alias name: fwd-tvid)</b>  Tcam sact fwd-tvid. <span class="li-normal">type: int</span>
 <a id='label978' href="javascript:ContentClick('label979', 'label978');" onmouseover="ContentPreview('label979');" onmouseout="ContentUnpreview('label979');" title="click to collapse or expand..."> more... </a>
 <div id="label979" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fwd_tvid_v</span> <b>(Alias name: fwd-tvid-v)</b>  Enable to set sact fwd-vid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label980' href="javascript:ContentClick('label981', 'label980');" onmouseover="ContentPreview('label981');" onmouseout="ContentUnpreview('label981');" title="click to collapse or expand..."> more... </a>
 <div id="label981" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fwd_v</span> <b>(Alias name: fwd-v)</b>  Enable to set sact fwd. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label982' href="javascript:ContentClick('label983', 'label982');" onmouseover="ContentPreview('label983');" onmouseout="ContentUnpreview('label983');" title="click to collapse or expand..."> more... </a>
 <div id="label983" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icpen</span> Tcam sact icpen. <span class="li-normal">type: int</span>
 <a id='label984' href="javascript:ContentClick('label985', 'label984');" onmouseover="ContentPreview('label985');" onmouseout="ContentUnpreview('label985');" title="click to collapse or expand..."> more... </a>
 <div id="label985" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icpen_v</span> <b>(Alias name: icpen-v)</b>  Enable to set sact icpen. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label986' href="javascript:ContentClick('label987', 'label986');" onmouseover="ContentPreview('label987');" onmouseout="ContentUnpreview('label987');" title="click to collapse or expand..."> more... </a>
 <div id="label987" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">igmp_mld_snp</span> <b>(Alias name: igmp-mld-snp)</b>  Tcam sact igmp-mld-snp. <span class="li-normal">type: int</span>
 <a id='label988' href="javascript:ContentClick('label989', 'label988');" onmouseover="ContentPreview('label989');" onmouseout="ContentUnpreview('label989');" title="click to collapse or expand..."> more... </a>
 <div id="label989" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">igmp_mld_snp_v</span> <b>(Alias name: igmp-mld-snp-v)</b>  Enable to set sact igmp-mld-snp. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label990' href="javascript:ContentClick('label991', 'label990');" onmouseover="ContentPreview('label991');" onmouseout="ContentUnpreview('label991');" title="click to collapse or expand..."> more... </a>
 <div id="label991" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">learn</span> Tcam sact learn. <span class="li-normal">type: int</span>
 <a id='label992' href="javascript:ContentClick('label993', 'label992');" onmouseover="ContentPreview('label993');" onmouseout="ContentUnpreview('label993');" title="click to collapse or expand..."> more... </a>
 <div id="label993" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">learn_v</span> <b>(Alias name: learn-v)</b>  Enable to set sact learn. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label994' href="javascript:ContentClick('label995', 'label994');" onmouseover="ContentPreview('label995');" onmouseout="ContentUnpreview('label995');" title="click to collapse or expand..."> more... </a>
 <div id="label995" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">m_srh_ctrl</span> <b>(Alias name: m-srh-ctrl)</b>  Tcam sact m-srh-ctrl. <span class="li-normal">type: int</span>
 <a id='label996' href="javascript:ContentClick('label997', 'label996');" onmouseover="ContentPreview('label997');" onmouseout="ContentUnpreview('label997');" title="click to collapse or expand..."> more... </a>
 <div id="label997" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">m_srh_ctrl_v</span> <b>(Alias name: m-srh-ctrl-v)</b>  Enable to set sact m-srh-ctrl. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label998' href="javascript:ContentClick('label999', 'label998');" onmouseover="ContentPreview('label999');" onmouseout="ContentUnpreview('label999');" title="click to collapse or expand..."> more... </a>
 <div id="label999" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mac_id</span> <b>(Alias name: mac-id)</b>  Tcam sact mac-id. <span class="li-normal">type: int</span>
 <a id='label1000' href="javascript:ContentClick('label1001', 'label1000');" onmouseover="ContentPreview('label1001');" onmouseout="ContentUnpreview('label1001');" title="click to collapse or expand..."> more... </a>
 <div id="label1001" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mac_id_v</span> <b>(Alias name: mac-id-v)</b>  Enable to set sact mac-id. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1002' href="javascript:ContentClick('label1003', 'label1002');" onmouseover="ContentPreview('label1003');" onmouseout="ContentUnpreview('label1003');" title="click to collapse or expand..."> more... </a>
 <div id="label1003" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mss</span> Tcam sact mss. <span class="li-normal">type: int</span>
 <a id='label1004' href="javascript:ContentClick('label1005', 'label1004');" onmouseover="ContentPreview('label1005');" onmouseout="ContentUnpreview('label1005');" title="click to collapse or expand..."> more... </a>
 <div id="label1005" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mss_v</span> <b>(Alias name: mss-v)</b>  Enable to set sact mss. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1006' href="javascript:ContentClick('label1007', 'label1006');" onmouseover="ContentPreview('label1007');" onmouseout="ContentUnpreview('label1007');" title="click to collapse or expand..."> more... </a>
 <div id="label1007" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">pleen</span> Tcam sact pleen. <span class="li-normal">type: int</span>
 <a id='label1008' href="javascript:ContentClick('label1009', 'label1008');" onmouseover="ContentPreview('label1009');" onmouseout="ContentUnpreview('label1009');" title="click to collapse or expand..."> more... </a>
 <div id="label1009" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">pleen_v</span> <b>(Alias name: pleen-v)</b>  Enable to set sact pleen. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1010' href="javascript:ContentClick('label1011', 'label1010');" onmouseover="ContentPreview('label1011');" onmouseout="ContentUnpreview('label1011');" title="click to collapse or expand..."> more... </a>
 <div id="label1011" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">prio_pid</span> <b>(Alias name: prio-pid)</b>  Tcam sact prio-pid. <span class="li-normal">type: int</span>
 <a id='label1012' href="javascript:ContentClick('label1013', 'label1012');" onmouseover="ContentPreview('label1013');" onmouseout="ContentUnpreview('label1013');" title="click to collapse or expand..."> more... </a>
 <div id="label1013" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">prio_pid_v</span> <b>(Alias name: prio-pid-v)</b>  Enable to set sact prio-pid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1014' href="javascript:ContentClick('label1015', 'label1014');" onmouseover="ContentPreview('label1015');" onmouseout="ContentUnpreview('label1015');" title="click to collapse or expand..."> more... </a>
 <div id="label1015" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">promis</span> Tcam sact promis. <span class="li-normal">type: int</span>
 <a id='label1016' href="javascript:ContentClick('label1017', 'label1016');" onmouseover="ContentPreview('label1017');" onmouseout="ContentUnpreview('label1017');" title="click to collapse or expand..."> more... </a>
 <div id="label1017" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">promis_v</span> <b>(Alias name: promis-v)</b>  Enable to set sact promis. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1018' href="javascript:ContentClick('label1019', 'label1018');" onmouseover="ContentPreview('label1019');" onmouseout="ContentUnpreview('label1019');" title="click to collapse or expand..."> more... </a>
 <div id="label1019" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rfsh</span> Tcam sact rfsh. <span class="li-normal">type: int</span>
 <a id='label1020' href="javascript:ContentClick('label1021', 'label1020');" onmouseover="ContentPreview('label1021');" onmouseout="ContentUnpreview('label1021');" title="click to collapse or expand..."> more... </a>
 <div id="label1021" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rfsh_v</span> <b>(Alias name: rfsh-v)</b>  Enable to set sact rfsh. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1022' href="javascript:ContentClick('label1023', 'label1022');" onmouseover="ContentPreview('label1023');" onmouseout="ContentUnpreview('label1023');" title="click to collapse or expand..."> more... </a>
 <div id="label1023" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">smac_skip</span> <b>(Alias name: smac-skip)</b>  Tcam sact smac-skip. <span class="li-normal">type: int</span>
 <a id='label1024' href="javascript:ContentClick('label1025', 'label1024');" onmouseover="ContentPreview('label1025');" onmouseout="ContentUnpreview('label1025');" title="click to collapse or expand..."> more... </a>
 <div id="label1025" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">smac_skip_v</span> <b>(Alias name: smac-skip-v)</b>  Enable to set sact smac-skip. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1026' href="javascript:ContentClick('label1027', 'label1026');" onmouseover="ContentPreview('label1027');" onmouseout="ContentUnpreview('label1027');" title="click to collapse or expand..."> more... </a>
 <div id="label1027" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tp_smchk_v</span> <b>(Alias name: tp-smchk-v)</b>  Enable to set sact tp mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1028' href="javascript:ContentClick('label1029', 'label1028');" onmouseover="ContentPreview('label1029');" onmouseout="ContentUnpreview('label1029');" title="click to collapse or expand..."> more... </a>
 <div id="label1029" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tp_smchk</span> Tcam sact tp mode. <span class="li-normal">type: int</span>
 <a id='label1030' href="javascript:ContentClick('label1031', 'label1030');" onmouseover="ContentPreview('label1031');" onmouseout="ContentUnpreview('label1031');" title="click to collapse or expand..."> more... </a>
 <div id="label1031" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tpe_id</span> <b>(Alias name: tpe-id)</b>  Tcam sact tpe-id. <span class="li-normal">type: int</span>
 <a id='label1032' href="javascript:ContentClick('label1033', 'label1032');" onmouseover="ContentPreview('label1033');" onmouseout="ContentUnpreview('label1033');" title="click to collapse or expand..."> more... </a>
 <div id="label1033" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tpe_id_v</span> <b>(Alias name: tpe-id-v)</b>  Enable to set sact tpe-id. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1034' href="javascript:ContentClick('label1035', 'label1034');" onmouseover="ContentPreview('label1035');" onmouseout="ContentUnpreview('label1035');" title="click to collapse or expand..."> more... </a>
 <div id="label1035" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vdm</span> Tcam sact vdm. <span class="li-normal">type: int</span>
 <a id='label1036' href="javascript:ContentClick('label1037', 'label1036');" onmouseover="ContentPreview('label1037');" onmouseout="ContentUnpreview('label1037');" title="click to collapse or expand..."> more... </a>
 <div id="label1037" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vdm_v</span> <b>(Alias name: vdm-v)</b>  Enable to set sact vdm. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1038' href="javascript:ContentClick('label1039', 'label1038');" onmouseover="ContentPreview('label1039');" onmouseout="ContentUnpreview('label1039');" title="click to collapse or expand..."> more... </a>
 <div id="label1039" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vdom_id</span> <b>(Alias name: vdom-id)</b>  Tcam sact vdom-id. <span class="li-normal">type: int</span>
 <a id='label1040' href="javascript:ContentClick('label1041', 'label1040');" onmouseover="ContentPreview('label1041');" onmouseout="ContentUnpreview('label1041');" title="click to collapse or expand..."> more... </a>
 <div id="label1041" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vdom_id_v</span> <b>(Alias name: vdom-id-v)</b>  Enable to set sact vdom-id. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1042' href="javascript:ContentClick('label1043', 'label1042');" onmouseover="ContentPreview('label1043');" onmouseout="ContentUnpreview('label1043');" title="click to collapse or expand..."> more... </a>
 <div id="label1043" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">x_mode</span> <b>(Alias name: x-mode)</b>  Tcam sact x-mode. <span class="li-normal">type: int</span>
 <a id='label1044' href="javascript:ContentClick('label1045', 'label1044');" onmouseover="ContentPreview('label1045');" onmouseout="ContentUnpreview('label1045');" title="click to collapse or expand..."> more... </a>
 <div id="label1045" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">x_mode_v</span> <b>(Alias name: x-mode-v)</b>  Enable to set sact x-mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1046' href="javascript:ContentClick('label1047', 'label1046');" onmouseover="ContentPreview('label1047');" onmouseout="ContentUnpreview('label1047');" title="click to collapse or expand..."> more... </a>
 <div id="label1047" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">tact</span> Tact. <span class="li-normal">type: dict</span>
 <a id='label1048' href="javascript:ContentClick('label1049', 'label1048');" onmouseover="ContentPreview('label1049');" onmouseout="ContentUnpreview('label1049');" title="click to collapse or expand..."> more... </a>
 <div id="label1049" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">act</span> Tcam tact act. <span class="li-normal">type: int</span>
 <a id='label1050' href="javascript:ContentClick('label1051', 'label1050');" onmouseover="ContentPreview('label1051');" onmouseout="ContentUnpreview('label1051');" title="click to collapse or expand..."> more... </a>
 <div id="label1051" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">act_v</span> <b>(Alias name: act-v)</b>  Enable to set tact act. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1052' href="javascript:ContentClick('label1053', 'label1052');" onmouseover="ContentPreview('label1053');" onmouseout="ContentUnpreview('label1053');" title="click to collapse or expand..."> more... </a>
 <div id="label1053" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fmtuv4_s</span> <b>(Alias name: fmtuv4-s)</b>  Tcam tact fmtuv4-s. <span class="li-normal">type: int</span>
 <a id='label1054' href="javascript:ContentClick('label1055', 'label1054');" onmouseover="ContentPreview('label1055');" onmouseout="ContentUnpreview('label1055');" title="click to collapse or expand..."> more... </a>
 <div id="label1055" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fmtuv4_s_v</span> <b>(Alias name: fmtuv4-s-v)</b>  Enable to set tact fmtuv4-s. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1056' href="javascript:ContentClick('label1057', 'label1056');" onmouseover="ContentPreview('label1057');" onmouseout="ContentUnpreview('label1057');" title="click to collapse or expand..."> more... </a>
 <div id="label1057" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fmtuv6_s</span> <b>(Alias name: fmtuv6-s)</b>  Tcam tact fmtuv6-s. <span class="li-normal">type: int</span>
 <a id='label1058' href="javascript:ContentClick('label1059', 'label1058');" onmouseover="ContentPreview('label1059');" onmouseout="ContentUnpreview('label1059');" title="click to collapse or expand..."> more... </a>
 <div id="label1059" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fmtuv6_s_v</span> <b>(Alias name: fmtuv6-s-v)</b>  Enable to set tact fmtuv6-s. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1060' href="javascript:ContentClick('label1061', 'label1060');" onmouseover="ContentPreview('label1061');" onmouseout="ContentUnpreview('label1061');" title="click to collapse or expand..."> more... </a>
 <div id="label1061" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">lnkid</span> Tcam tact lnkid. <span class="li-normal">type: int</span>
 <a id='label1062' href="javascript:ContentClick('label1063', 'label1062');" onmouseover="ContentPreview('label1063');" onmouseout="ContentUnpreview('label1063');" title="click to collapse or expand..."> more... </a>
 <div id="label1063" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">lnkid_v</span> <b>(Alias name: lnkid-v)</b>  Enable to set tact lnkid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1064' href="javascript:ContentClick('label1065', 'label1064');" onmouseover="ContentPreview('label1065');" onmouseout="ContentUnpreview('label1065');" title="click to collapse or expand..."> more... </a>
 <div id="label1065" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mac_id</span> <b>(Alias name: mac-id)</b>  Tcam tact mac-id. <span class="li-normal">type: int</span>
 <a id='label1066' href="javascript:ContentClick('label1067', 'label1066');" onmouseover="ContentPreview('label1067');" onmouseout="ContentUnpreview('label1067');" title="click to collapse or expand..."> more... </a>
 <div id="label1067" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mac_id_v</span> <b>(Alias name: mac-id-v)</b>  Enable to set tact mac-id. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1068' href="javascript:ContentClick('label1069', 'label1068');" onmouseover="ContentPreview('label1069');" onmouseout="ContentUnpreview('label1069');" title="click to collapse or expand..."> more... </a>
 <div id="label1069" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mss_t</span> <b>(Alias name: mss-t)</b>  Tcam tact mss. <span class="li-normal">type: int</span>
 <a id='label1070' href="javascript:ContentClick('label1071', 'label1070');" onmouseover="ContentPreview('label1071');" onmouseout="ContentUnpreview('label1071');" title="click to collapse or expand..."> more... </a>
 <div id="label1071" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mss_t_v</span> <b>(Alias name: mss-t-v)</b>  Enable to set tact mss. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1072' href="javascript:ContentClick('label1073', 'label1072');" onmouseover="ContentPreview('label1073');" onmouseout="ContentUnpreview('label1073');" title="click to collapse or expand..."> more... </a>
 <div id="label1073" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mtuv4</span> Tcam tact mtuv4. <span class="li-normal">type: int</span>
 <a id='label1074' href="javascript:ContentClick('label1075', 'label1074');" onmouseover="ContentPreview('label1075');" onmouseout="ContentUnpreview('label1075');" title="click to collapse or expand..."> more... </a>
 <div id="label1075" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mtuv4_v</span> <b>(Alias name: mtuv4-v)</b>  Enable to set tact mtuv4. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1076' href="javascript:ContentClick('label1077', 'label1076');" onmouseover="ContentPreview('label1077');" onmouseout="ContentUnpreview('label1077');" title="click to collapse or expand..."> more... </a>
 <div id="label1077" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mtuv6</span> Tcam tact mtuv6. <span class="li-normal">type: int</span>
 <a id='label1078' href="javascript:ContentClick('label1079', 'label1078');" onmouseover="ContentPreview('label1079');" onmouseout="ContentUnpreview('label1079');" title="click to collapse or expand..."> more... </a>
 <div id="label1079" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mtuv6_v</span> <b>(Alias name: mtuv6-v)</b>  Enable to set tact mtuv6. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1080' href="javascript:ContentClick('label1081', 'label1080');" onmouseover="ContentPreview('label1081');" onmouseout="ContentUnpreview('label1081');" title="click to collapse or expand..."> more... </a>
 <div id="label1081" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">slif_act</span> <b>(Alias name: slif-act)</b>  Tcam tact slif-act. <span class="li-normal">type: int</span>
 <a id='label1082' href="javascript:ContentClick('label1083', 'label1082');" onmouseover="ContentPreview('label1083');" onmouseout="ContentUnpreview('label1083');" title="click to collapse or expand..."> more... </a>
 <div id="label1083" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">slif_act_v</span> <b>(Alias name: slif-act-v)</b>  Enable to set tact slif-act. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1084' href="javascript:ContentClick('label1085', 'label1084');" onmouseover="ContentPreview('label1085');" onmouseout="ContentUnpreview('label1085');" title="click to collapse or expand..."> more... </a>
 <div id="label1085" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sublnkid</span> Tcam tact sublnkid. <span class="li-normal">type: int</span>
 <a id='label1086' href="javascript:ContentClick('label1087', 'label1086');" onmouseover="ContentPreview('label1087');" onmouseout="ContentUnpreview('label1087');" title="click to collapse or expand..."> more... </a>
 <div id="label1087" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sublnkid_v</span> <b>(Alias name: sublnkid-v)</b>  Enable to set tact sublnkid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1088' href="javascript:ContentClick('label1089', 'label1088');" onmouseover="ContentPreview('label1089');" onmouseout="ContentUnpreview('label1089');" title="click to collapse or expand..."> more... </a>
 <div id="label1089" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgtv_act</span> <b>(Alias name: tgtv-act)</b>  Tcam tact tgtv-act. <span class="li-normal">type: int</span>
 <a id='label1090' href="javascript:ContentClick('label1091', 'label1090');" onmouseover="ContentPreview('label1091');" onmouseout="ContentUnpreview('label1091');" title="click to collapse or expand..."> more... </a>
 <div id="label1091" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tgtv_act_v</span> <b>(Alias name: tgtv-act-v)</b>  Enable to set tact tgtv-act. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1092' href="javascript:ContentClick('label1093', 'label1092');" onmouseover="ContentPreview('label1093');" onmouseout="ContentUnpreview('label1093');" title="click to collapse or expand..."> more... </a>
 <div id="label1093" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tlif_act</span> <b>(Alias name: tlif-act)</b>  Tcam tact tlif-act. <span class="li-normal">type: int</span>
 <a id='label1094' href="javascript:ContentClick('label1095', 'label1094');" onmouseover="ContentPreview('label1095');" onmouseout="ContentUnpreview('label1095');" title="click to collapse or expand..."> more... </a>
 <div id="label1095" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tlif_act_v</span> <b>(Alias name: tlif-act-v)</b>  Enable to set tact tlif-act. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1096' href="javascript:ContentClick('label1097', 'label1096');" onmouseover="ContentPreview('label1097');" onmouseout="ContentUnpreview('label1097');" title="click to collapse or expand..."> more... </a>
 <div id="label1097" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tpeid</span> Tcam tact tpeid. <span class="li-normal">type: int</span>
 <a id='label1098' href="javascript:ContentClick('label1099', 'label1098');" onmouseover="ContentPreview('label1099');" onmouseout="ContentUnpreview('label1099');" title="click to collapse or expand..."> more... </a>
 <div id="label1099" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tpeid_v</span> <b>(Alias name: tpeid-v)</b>  Enable to set tact tpeid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1100' href="javascript:ContentClick('label1101', 'label1100');" onmouseover="ContentPreview('label1101');" onmouseout="ContentUnpreview('label1101');" title="click to collapse or expand..."> more... </a>
 <div id="label1101" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">v6fe</span> Tcam tact v6fe. <span class="li-normal">type: int</span>
 <a id='label1102' href="javascript:ContentClick('label1103', 'label1102');" onmouseover="ContentPreview('label1103');" onmouseout="ContentUnpreview('label1103');" title="click to collapse or expand..."> more... </a>
 <div id="label1103" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">v6fe_v</span> <b>(Alias name: v6fe-v)</b>  Enable to set tact v6fe. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1104' href="javascript:ContentClick('label1105', 'label1104');" onmouseover="ContentPreview('label1105');" onmouseout="ContentUnpreview('label1105');" title="click to collapse or expand..."> more... </a>
 <div id="label1105" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vep_en_v</span> <b>(Alias name: vep-en-v)</b>  Enable to set tact vep-en. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1106' href="javascript:ContentClick('label1107', 'label1106');" onmouseover="ContentPreview('label1107');" onmouseout="ContentUnpreview('label1107');" title="click to collapse or expand..."> more... </a>
 <div id="label1107" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vep_slid</span> <b>(Alias name: vep-slid)</b>  Tcam tact vep_slid. <span class="li-normal">type: int</span>
 <a id='label1108' href="javascript:ContentClick('label1109', 'label1108');" onmouseover="ContentPreview('label1109');" onmouseout="ContentUnpreview('label1109');" title="click to collapse or expand..."> more... </a>
 <div id="label1109" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vep_slid_v</span> <b>(Alias name: vep-slid-v)</b>  Enable to set tact vep-slid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1110' href="javascript:ContentClick('label1111', 'label1110');" onmouseover="ContentPreview('label1111');" onmouseout="ContentUnpreview('label1111');" title="click to collapse or expand..."> more... </a>
 <div id="label1111" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vep_en</span> Tcam tact vep_en. <span class="li-normal">type: int</span>
 <a id='label1112' href="javascript:ContentClick('label1113', 'label1112');" onmouseover="ContentPreview('label1113');" onmouseout="ContentUnpreview('label1113');" title="click to collapse or expand..."> more... </a>
 <div id="label1113" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">xlt_lif</span> <b>(Alias name: xlt-lif)</b>  Tcam tact xlt-lif. <span class="li-normal">type: int</span>
 <a id='label1114' href="javascript:ContentClick('label1115', 'label1114');" onmouseover="ContentPreview('label1115');" onmouseout="ContentUnpreview('label1115');" title="click to collapse or expand..."> more... </a>
 <div id="label1115" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">xlt_lif_v</span> <b>(Alias name: xlt-lif-v)</b>  Enable to set tact xlt-lif. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1116' href="javascript:ContentClick('label1117', 'label1116');" onmouseover="ContentPreview('label1117');" onmouseout="ContentUnpreview('label1117');" title="click to collapse or expand..."> more... </a>
 <div id="label1117" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">xlt_vid</span> <b>(Alias name: xlt-vid)</b>  Tcam tact xlt-vid. <span class="li-normal">type: int</span>
 <a id='label1118' href="javascript:ContentClick('label1119', 'label1118');" onmouseover="ContentPreview('label1119');" onmouseout="ContentUnpreview('label1119');" title="click to collapse or expand..."> more... </a>
 <div id="label1119" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">xlt_vid_v</span> <b>(Alias name: xlt-vid-v)</b>  Enable to set tact xlt-vid. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1120' href="javascript:ContentClick('label1121', 'label1120');" onmouseover="ContentPreview('label1121');" onmouseout="ContentUnpreview('label1121');" title="click to collapse or expand..."> more... </a>
 <div id="label1121" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">type</span> Tcam policy type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [L2_src_tc, L2_tgt_tc, L2_src_mir, L2_tgt_mir, L2_src_act, L2_tgt_act, IPv4_src_tc, IPv4_tgt_tc, IPv4_src_mir, IPv4_tgt_mir, IPv4_src_act, IPv4_tgt_act, IPv6_src_tc, IPv6_tgt_tc, IPv6_src_mir, IPv6_tgt_mir, IPv6_src_act, IPv6_tgt_act]</span> 
 <a id='label1122' href="javascript:ContentClick('label1123', 'label1122');" onmouseover="ContentPreview('label1123');" onmouseout="ContentUnpreview('label1123');" title="click to collapse or expand..."> more... </a>
 <div id="label1123" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vid</span> Npu tcam vid. <span class="li-normal">type: int</span>
 <a id='label1124' href="javascript:ContentClick('label1125', 'label1124');" onmouseover="ContentPreview('label1125');" onmouseout="ContentUnpreview('label1125');" title="click to collapse or expand..."> more... </a>
 <div id="label1125" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">icmp_rate_ctrl</span> <b>(Alias name: icmp-rate-ctrl)</b>  Icmp rate ctrl. <span class="li-normal">type: dict</span>
 <a id='label1126' href="javascript:ContentClick('label1127', 'label1126');" onmouseover="ContentPreview('label1127');" onmouseout="ContentUnpreview('label1127');" title="click to collapse or expand..."> more... </a>
 <div id="label1127" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">icmp_v4_bucket_size</span> <b>(Alias name: icmp-v4-bucket-size)</b>  Bucket size used in the token bucket algorithm for controlling the flow of icmpv4 packets (1 - 100, default = 10). <span class="li-normal">type: int</span>
 <a id='label1128' href="javascript:ContentClick('label1129', 'label1128');" onmouseover="ContentPreview('label1129');" onmouseout="ContentUnpreview('label1129');" title="click to collapse or expand..."> more... </a>
 <div id="label1129" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_v4_rate</span> <b>(Alias name: icmp-v4-rate)</b>  Average rate of icmpv4 packets that allowed to be generated per second (1 - 100, default = 1). <span class="li-normal">type: int</span>
 <a id='label1130' href="javascript:ContentClick('label1131', 'label1130');" onmouseover="ContentPreview('label1131');" onmouseout="ContentUnpreview('label1131');" title="click to collapse or expand..."> more... </a>
 <div id="label1131" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_v6_bucket_size</span> <b>(Alias name: icmp-v6-bucket-size)</b>  Bucket size used in the token bucket algorithm for controlling the flow of icmpv6 packets (1 - 100, default = 10). <span class="li-normal">type: int</span>
 <a id='label1132' href="javascript:ContentClick('label1133', 'label1132');" onmouseover="ContentPreview('label1133');" onmouseout="ContentUnpreview('label1133');" title="click to collapse or expand..."> more... </a>
 <div id="label1133" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_v6_rate</span> <b>(Alias name: icmp-v6-rate)</b>  Average rate of icmpv6 packets that allowed to be generated per second (1 - 100, default = 1). <span class="li-normal">type: int</span>
 <a id='label1134' href="javascript:ContentClick('label1135', 'label1134');" onmouseover="ContentPreview('label1135');" onmouseout="ContentUnpreview('label1135');" title="click to collapse or expand..."> more... </a>
 <div id="label1135" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">vxlan_offload</span> <b>(Alias name: vxlan-offload)</b>  Enable/disable offloading vxlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1136' href="javascript:ContentClick('label1137', 'label1136');" onmouseover="ContentPreview('label1137');" onmouseout="ContentUnpreview('label1137');" title="click to collapse or expand..."> more... </a>
 <div id="label1137" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmp_error_rate_ctrl</span> <b>(Alias name: icmp-error-rate-ctrl)</b>  Icmp error rate ctrl. <span class="li-normal">type: dict</span>
 <a id='label1138' href="javascript:ContentClick('label1139', 'label1138');" onmouseover="ContentPreview('label1139');" onmouseout="ContentUnpreview('label1139');" title="click to collapse or expand..."> more... </a>
 <div id="label1139" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">icmpv4_error_bucket_size</span> <b>(Alias name: icmpv4-error-bucket-size)</b>  Bucket size used in the token bucket algorithm for controlling the flow of icmpv4 error packets (1 - 100, default = 20). <span class="li-normal">type: int</span>
 <a id='label1140' href="javascript:ContentClick('label1141', 'label1140');" onmouseover="ContentPreview('label1141');" onmouseout="ContentUnpreview('label1141');" title="click to collapse or expand..."> more... </a>
 <div id="label1141" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmpv4_error_rate</span> <b>(Alias name: icmpv4-error-rate)</b>  Average rate of icmpv4 error packets that allowed to be generated per second (1 - 100, default = 1). <span class="li-normal">type: int</span>
 <a id='label1142' href="javascript:ContentClick('label1143', 'label1142');" onmouseover="ContentPreview('label1143');" onmouseout="ContentUnpreview('label1143');" title="click to collapse or expand..."> more... </a>
 <div id="label1143" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmpv4_error_rate_limit</span> <b>(Alias name: icmpv4-error-rate-limit)</b>  Enable to limit the icmpv4 error packets generated by this fortigate. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1144' href="javascript:ContentClick('label1145', 'label1144');" onmouseover="ContentPreview('label1145');" onmouseout="ContentUnpreview('label1145');" title="click to collapse or expand..."> more... </a>
 <div id="label1145" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmpv6_error_bucket_size</span> <b>(Alias name: icmpv6-error-bucket-size)</b>  Bucket size used in the token bucket algorithm for controlling the flow of icmpv6 error packets (1 - 100, default = 20). <span class="li-normal">type: int</span>
 <a id='label1146' href="javascript:ContentClick('label1147', 'label1146');" onmouseover="ContentPreview('label1147');" onmouseout="ContentUnpreview('label1147');" title="click to collapse or expand..."> more... </a>
 <div id="label1147" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmpv6_error_rate</span> <b>(Alias name: icmpv6-error-rate)</b>  Average rate of icmpv6 error packets that allowed to be generated per second (1 - 100, default = 1). <span class="li-normal">type: int</span>
 <a id='label1148' href="javascript:ContentClick('label1149', 'label1148');" onmouseover="ContentPreview('label1149');" onmouseout="ContentUnpreview('label1149');" title="click to collapse or expand..."> more... </a>
 <div id="label1149" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">icmpv6_error_rate_limit</span> <b>(Alias name: icmpv6-error-rate-limit)</b>  Enable to limit the icmpv6 error packets generated by this fortigate. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1150' href="javascript:ContentClick('label1151', 'label1150');" onmouseover="ContentPreview('label1151');" onmouseout="ContentUnpreview('label1151');" title="click to collapse or expand..."> more... </a>
 <div id="label1151" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">ipv4_session_quota</span> <b>(Alias name: ipv4-session-quota)</b>  Enable/disable nonat ipv4 session quota for hyperscale vdoms. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1152' href="javascript:ContentClick('label1153', 'label1152');" onmouseover="ContentPreview('label1153');" onmouseout="ContentUnpreview('label1153');" title="click to collapse or expand..."> more... </a>
 <div id="label1153" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_session_quota_high</span> <b>(Alias name: ipv4-session-quota-high)</b>  Configure nonat ipv4 session quota high threshold. <span class="li-normal">type: int</span>
 <a id='label1154' href="javascript:ContentClick('label1155', 'label1154');" onmouseover="ContentPreview('label1155');" onmouseout="ContentUnpreview('label1155');" title="click to collapse or expand..."> more... </a>
 <div id="label1155" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv4_session_quota_low</span> <b>(Alias name: ipv4-session-quota-low)</b>  Configure nonat ipv4 session quota low threshold. <span class="li-normal">type: int</span>
 <a id='label1156' href="javascript:ContentClick('label1157', 'label1156');" onmouseover="ContentPreview('label1157');" onmouseout="ContentUnpreview('label1157');" title="click to collapse or expand..."> more... </a>
 <div id="label1157" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_prefix_session_quota</span> <b>(Alias name: ipv6-prefix-session-quota)</b>  Enable/disable hardware ipv6 /64 prefix session quota for hyperscale vdoms. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1158' href="javascript:ContentClick('label1159', 'label1158');" onmouseover="ContentPreview('label1159');" onmouseout="ContentUnpreview('label1159');" title="click to collapse or expand..."> more... </a>
 <div id="label1159" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_prefix_session_quota_high</span> <b>(Alias name: ipv6-prefix-session-quota-high)</b>  Configure ipv6 prefix session quota high threshold. <span class="li-normal">type: int</span>
 <a id='label1160' href="javascript:ContentClick('label1161', 'label1160');" onmouseover="ContentPreview('label1161');" onmouseout="ContentUnpreview('label1161');" title="click to collapse or expand..."> more... </a>
 <div id="label1161" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipv6_prefix_session_quota_low</span> <b>(Alias name: ipv6-prefix-session-quota-low)</b>  Configure ipv6 prefix session quota low threshold. <span class="li-normal">type: int</span>
 <a id='label1162' href="javascript:ContentClick('label1163', 'label1162');" onmouseover="ContentPreview('label1163');" onmouseout="ContentUnpreview('label1163');" title="click to collapse or expand..."> more... </a>
 <div id="label1163" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dedicated_lacp_queue</span> <b>(Alias name: dedicated-lacp-queue)</b>  Enable to dedicate one hif queue for lacp. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1164' href="javascript:ContentClick('label1165', 'label1164');" onmouseover="ContentPreview('label1165');" onmouseout="ContentUnpreview('label1165');" title="click to collapse or expand..."> more... </a>
 <div id="label1165" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ipsec_ordering</span> <b>(Alias name: ipsec-ordering)</b>  Enable/disable ipsec ordering. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1166' href="javascript:ContentClick('label1167', 'label1166');" onmouseover="ContentPreview('label1167');" onmouseout="ContentUnpreview('label1167');" title="click to collapse or expand..."> more... </a>
 <div id="label1167" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.7 -> v7.4.7</code></p>
 </div>
 </li>
 <li><span class="li-head">sw_np_pause</span> <b>(Alias name: sw-np-pause)</b>  Enable sp5 tx pause and marvell rx receive pause, for sw uplink only. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1168' href="javascript:ContentClick('label1169', 'label1168');" onmouseover="ContentPreview('label1169');" onmouseout="ContentUnpreview('label1169');" title="click to collapse or expand..."> more... </a>
 <div id="label1169" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.7 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sw_np_rate</span> <b>(Alias name: sw-np-rate)</b>  Bandwidth from switch to np, for sw uplink port. <span class="li-normal">type: int</span>
 <a id='label1170' href="javascript:ContentClick('label1171', 'label1170');" onmouseover="ContentPreview('label1171');" onmouseout="ContentUnpreview('label1171');" title="click to collapse or expand..."> more... </a>
 <div id="label1171" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.7 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sw_np_rate_unit</span> <b>(Alias name: sw-np-rate-unit)</b>  Unit for bandwidth from switch to np, for sw uplink port. <span class="li-normal">type: str</span> <span class="li-normal">choices: [mbps, pps]</span> 
 <a id='label1172' href="javascript:ContentClick('label1173', 'label1172');" onmouseover="ContentPreview('label1173');" onmouseout="ContentUnpreview('label1173');" title="click to collapse or expand..."> more... </a>
 <div id="label1173" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.7 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.3 -> latest</code></p>
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
      - name: Configure NPU attributes.
        fortinet.fortimanager.fmgr_system_npu:
          # bypass_validation: false
          workspace_locking_adom: <value in [global, custom adom including root]>
          workspace_locking_timeout: 300
          # rc_succeeded: [0, -2, -3, ...]
          # rc_failed: [-2, -3, ...]
          adom: <your own value>
          system_npu:
            # capwap_offload: <value in [disable, enable]>
            # dedicated_management_affinity: <string>
            # dedicated_management_cpu: <value in [disable, enable]>
            # fastpath: <value in [disable, enable]>
            # fp_anomaly:
            #   esp_minlen_err: <value in [drop, trap-to-host]>
            #   icmp_csum_err: <value in [drop, trap-to-host]>
            #   icmp_minlen_err: <value in [drop, trap-to-host]>
            #   ipv4_csum_err: <value in [drop, trap-to-host]>
            #   ipv4_ihl_err: <value in [drop, trap-to-host]>
            #   ipv4_len_err: <value in [drop, trap-to-host]>
            #   ipv4_opt_err: <value in [drop, trap-to-host]>
            #   ipv4_ttlzero_err: <value in [drop, trap-to-host]>
            #   ipv4_ver_err: <value in [drop, trap-to-host]>
            #   ipv6_exthdr_len_err: <value in [drop, trap-to-host]>
            #   ipv6_exthdr_order_err: <value in [drop, trap-to-host]>
            #   ipv6_ihl_err: <value in [drop, trap-to-host]>
            #   ipv6_plen_zero: <value in [drop, trap-to-host]>
            #   ipv6_ver_err: <value in [drop, trap-to-host]>
            #   tcp_csum_err: <value in [drop, trap-to-host]>
            #   tcp_hlen_err: <value in [drop, trap-to-host]>
            #   tcp_plen_err: <value in [drop, trap-to-host]>
            #   udp_csum_err: <value in [drop, trap-to-host]>
            #   udp_hlen_err: <value in [drop, trap-to-host]>
            #   udp_len_err: <value in [drop, trap-to-host]>
            #   udp_plen_err: <value in [drop, trap-to-host]>
            #   udplite_cover_err: <value in [drop, trap-to-host]>
            #   udplite_csum_err: <value in [drop, trap-to-host, allow]>
            #   unknproto_minlen_err: <value in [drop, trap-to-host]>
            #   tcp_fin_only: <value in [allow, drop, trap-to-host]>
            #   ipv4_optsecurity: <value in [allow, drop, trap-to-host]>
            #   ipv6_optralert: <value in [allow, drop, trap-to-host]>
            #   tcp_syn_fin: <value in [allow, drop, trap-to-host]>
            #   ipv4_proto_err: <value in [allow, drop, trap-to-host]>
            #   ipv6_saddr_err: <value in [allow, drop, trap-to-host]>
            #   icmp_frag: <value in [allow, drop, trap-to-host]>
            #   ipv4_optssrr: <value in [allow, drop, trap-to-host]>
            #   ipv6_opthomeaddr: <value in [allow, drop, trap-to-host]>
            #   udp_land: <value in [allow, drop, trap-to-host]>
            #   ipv6_optinvld: <value in [allow, drop, trap-to-host]>
            #   tcp_fin_noack: <value in [allow, drop, trap-to-host]>
            #   ipv6_proto_err: <value in [allow, drop, trap-to-host]>
            #   tcp_land: <value in [allow, drop, trap-to-host]>
            #   ipv4_unknopt: <value in [allow, drop, trap-to-host]>
            #   ipv4_optstream: <value in [allow, drop, trap-to-host]>
            #   ipv6_optjumbo: <value in [allow, drop, trap-to-host]>
            #   icmp_land: <value in [allow, drop, trap-to-host]>
            #   tcp_winnuke: <value in [allow, drop, trap-to-host]>
            #   ipv6_daddr_err: <value in [allow, drop, trap-to-host]>
            #   ipv4_land: <value in [allow, drop, trap-to-host]>
            #   ipv6_opttunnel: <value in [allow, drop, trap-to-host]>
            #   tcp_no_flag: <value in [allow, drop, trap-to-host]>
            #   ipv6_land: <value in [allow, drop, trap-to-host]>
            #   ipv4_optlsrr: <value in [allow, drop, trap-to-host]>
            #   ipv4_opttimestamp: <value in [allow, drop, trap-to-host]>
            #   ipv4_optrr: <value in [allow, drop, trap-to-host]>
            #   ipv6_optnsap: <value in [allow, drop, trap-to-host]>
            #   ipv6_unknopt: <value in [allow, drop, trap-to-host]>
            #   tcp_syn_data: <value in [allow, drop, trap-to-host]>
            #   ipv6_optendpid: <value in [allow, drop, trap-to-host]>
            #   gtpu_plen_err: <value in [drop, trap-to-host]>
            #   vxlan_minlen_err: <value in [drop, trap-to-host]>
            #   capwap_minlen_err: <value in [drop, trap-to-host]>
            #   gre_csum_err: <value in [drop, trap-to-host, allow]>
            #   nvgre_minlen_err: <value in [drop, trap-to-host]>
            #   sctp_l4len_err: <value in [drop, trap-to-host]>
            #   tcp_hlenvsl4len_err: <value in [drop, trap-to-host]>
            #   sctp_crc_err: <value in [drop, trap-to-host]>
            #   sctp_clen_err: <value in [drop, trap-to-host]>
            #   uesp_minlen_err: <value in [drop, trap-to-host]>
            #   sctp_csum_err: <value in [allow, drop, trap-to-host]>
            # gtp_enhanced_cpu_range: <value in [0, 1, 2]>
            # gtp_enhanced_mode: <value in [disable, enable]>
            # host_shortcut_mode: <value in [bi-directional, host-shortcut]>
            # htx_gtse_quota: <value in [100Mbps, 200Mbps, 300Mbps, ...]>
            # intf_shaping_offload: <value in [disable, enable]>
            # iph_rsvd_re_cksum: <value in [disable, enable]>
            # ipsec_dec_subengine_mask: <string>
            # ipsec_enc_subengine_mask: <string>
            # ipsec_inbound_cache: <value in [disable, enable]>
            # ipsec_mtu_override: <value in [disable, enable]>
            # ipsec_over_vlink: <value in [disable, enable]>
            # isf_np_queues:
            #   cos0: <string>
            #   cos1: <string>
            #   cos2: <string>
            #   cos3: <string>
            #   cos4: <string>
            #   cos5: <string>
            #   cos6: <string>
            #   cos7: <string>
            # lag_out_port_select: <value in [disable, enable]>
            # mcast_session_accounting: <value in [disable, session-based, tpe-based]>
            # np6_cps_optimization_mode: <value in [disable, enable]>
            # per_session_accounting: <value in [enable, disable, enable-by-log, ...]>
            # port_cpu_map:
            #   - cpu_core: <string>
            #     interface: <string>
            # port_npu_map:
            #   - interface: <string>
            #     npu_group_index: <integer>
            # priority_protocol:
            #   bfd: <value in [disable, enable]>
            #   bgp: <value in [disable, enable]>
            #   slbc: <value in [disable, enable]>
            # qos_mode: <value in [disable, priority, round-robin]>
            # rdp_offload: <value in [disable, enable]>
            # recover_np6_link: <value in [disable, enable]>
            # session_denied_offload: <value in [disable, enable]>
            # sse_backpressure: <value in [disable, enable]>
            # strip_clear_text_padding: <value in [disable, enable]>
            # strip_esp_padding: <value in [disable, enable]>
            # sw_eh_hash:
            #   computation: <value in [xor16, xor8, xor4, ...]>
            #   destination_ip_lower_16: <value in [include, exclude]>
            #   destination_ip_upper_16: <value in [include, exclude]>
            #   destination_port: <value in [include, exclude]>
            #   ip_protocol: <value in [include, exclude]>
            #   netmask_length: <integer>
            #   source_ip_lower_16: <value in [include, exclude]>
            #   source_ip_upper_16: <value in [include, exclude]>
            #   source_port: <value in [include, exclude]>
            # sw_np_bandwidth: <value in [0G, 2G, 4G, ...]>
            # switch_np_hash: <value in [src-ip, dst-ip, src-dst-ip]>
            # uesp_offload: <value in [disable, enable]>
            # np_queues:
            #   ethernet_type:
            #     - name: <string>
            #       queue: <integer>
            #       type: <integer>
            #       weight: <integer>
            #   ip_protocol:
            #     - name: <string>
            #       protocol: <integer>
            #       queue: <integer>
            #       weight: <integer>
            #   ip_service:
            #     - dport: <integer>
            #       name: <string>
            #       protocol: <integer>
            #       queue: <integer>
            #       sport: <integer>
            #       weight: <integer>
            #   profile:
            #     - cos0: <value in [queue0, queue1, queue2, ...]>
            #       cos1: <value in [queue0, queue1, queue2, ...]>
            #       cos2: <value in [queue0, queue1, queue2, ...]>
            #       cos3: <value in [queue0, queue1, queue2, ...]>
            #       cos4: <value in [queue0, queue1, queue2, ...]>
            #       cos5: <value in [queue0, queue1, queue2, ...]>
            #       cos6: <value in [queue0, queue1, queue2, ...]>
            #       cos7: <value in [queue0, queue1, queue2, ...]>
            #       dscp0: <value in [queue0, queue1, queue2, ...]>
            #       dscp1: <value in [queue0, queue1, queue2, ...]>
            #       dscp10: <value in [queue0, queue1, queue2, ...]>
            #       dscp11: <value in [queue0, queue1, queue2, ...]>
            #       dscp12: <value in [queue0, queue1, queue2, ...]>
            #       dscp13: <value in [queue0, queue1, queue2, ...]>
            #       dscp14: <value in [queue0, queue1, queue2, ...]>
            #       dscp15: <value in [queue0, queue1, queue2, ...]>
            #       dscp16: <value in [queue0, queue1, queue2, ...]>
            #       dscp17: <value in [queue0, queue1, queue2, ...]>
            #       dscp18: <value in [queue0, queue1, queue2, ...]>
            #       dscp19: <value in [queue0, queue1, queue2, ...]>
            #       dscp2: <value in [queue0, queue1, queue2, ...]>
            #       dscp20: <value in [queue0, queue1, queue2, ...]>
            #       dscp21: <value in [queue0, queue1, queue2, ...]>
            #       dscp22: <value in [queue0, queue1, queue2, ...]>
            #       dscp23: <value in [queue0, queue1, queue2, ...]>
            #       dscp24: <value in [queue0, queue1, queue2, ...]>
            #       dscp25: <value in [queue0, queue1, queue2, ...]>
            #       dscp26: <value in [queue0, queue1, queue2, ...]>
            #       dscp27: <value in [queue0, queue1, queue2, ...]>
            #       dscp28: <value in [queue0, queue1, queue2, ...]>
            #       dscp29: <value in [queue0, queue1, queue2, ...]>
            #       dscp3: <value in [queue0, queue1, queue2, ...]>
            #       dscp30: <value in [queue0, queue1, queue2, ...]>
            #       dscp31: <value in [queue0, queue1, queue2, ...]>
            #       dscp32: <value in [queue0, queue1, queue2, ...]>
            #       dscp33: <value in [queue0, queue1, queue2, ...]>
            #       dscp34: <value in [queue0, queue1, queue2, ...]>
            #       dscp35: <value in [queue0, queue1, queue2, ...]>
            #       dscp36: <value in [queue0, queue1, queue2, ...]>
            #       dscp37: <value in [queue0, queue1, queue2, ...]>
            #       dscp38: <value in [queue0, queue1, queue2, ...]>
            #       dscp39: <value in [queue0, queue1, queue2, ...]>
            #       dscp4: <value in [queue0, queue1, queue2, ...]>
            #       dscp40: <value in [queue0, queue1, queue2, ...]>
            #       dscp41: <value in [queue0, queue1, queue2, ...]>
            #       dscp42: <value in [queue0, queue1, queue2, ...]>
            #       dscp43: <value in [queue0, queue1, queue2, ...]>
            #       dscp44: <value in [queue0, queue1, queue2, ...]>
            #       dscp45: <value in [queue0, queue1, queue2, ...]>
            #       dscp46: <value in [queue0, queue1, queue2, ...]>
            #       dscp47: <value in [queue0, queue1, queue2, ...]>
            #       dscp48: <value in [queue0, queue1, queue2, ...]>
            #       dscp49: <value in [queue0, queue1, queue2, ...]>
            #       dscp5: <value in [queue0, queue1, queue2, ...]>
            #       dscp50: <value in [queue0, queue1, queue2, ...]>
            #       dscp51: <value in [queue0, queue1, queue2, ...]>
            #       dscp52: <value in [queue0, queue1, queue2, ...]>
            #       dscp53: <value in [queue0, queue1, queue2, ...]>
            #       dscp54: <value in [queue0, queue1, queue2, ...]>
            #       dscp55: <value in [queue0, queue1, queue2, ...]>
            #       dscp56: <value in [queue0, queue1, queue2, ...]>
            #       dscp57: <value in [queue0, queue1, queue2, ...]>
            #       dscp58: <value in [queue0, queue1, queue2, ...]>
            #       dscp59: <value in [queue0, queue1, queue2, ...]>
            #       dscp6: <value in [queue0, queue1, queue2, ...]>
            #       dscp60: <value in [queue0, queue1, queue2, ...]>
            #       dscp61: <value in [queue0, queue1, queue2, ...]>
            #       dscp62: <value in [queue0, queue1, queue2, ...]>
            #       dscp63: <value in [queue0, queue1, queue2, ...]>
            #       dscp7: <value in [queue0, queue1, queue2, ...]>
            #       dscp8: <value in [queue0, queue1, queue2, ...]>
            #       dscp9: <value in [queue0, queue1, queue2, ...]>
            #       id: <integer>
            #       type: <value in [cos, dscp]>
            #       weight: <integer>
            #   scheduler:
            #     - mode: <value in [none, priority, round-robin]>
            #       name: <string>
            #   custom_etype_lookup: <value in [disable, enable]>
            # udp_timeout_profile:
            #   - id: <integer>
            #     udp_idle: <integer>
            # qtm_buf_mode: <value in [6ch, 4ch]>
            # default_qos_type: <value in [policing, shaping, policing-enhanced]>
            # tcp_rst_timeout: <integer>
            # ipsec_local_uesp_port: <integer>
            # htab_dedi_queue_nr: <integer>
            # double_level_mcast_offload: <value in [disable, enable]>
            # dse_timeout: <integer>
            # ippool_overload_low: <integer>
            # pba_eim: <value in [disallow, allow]>
            # policy_offload_level: <value in [disable, dos-offload, full-offload]>
            # max_session_timeout: <integer>
            # port_path_option:
            #   ports_using_npu: <list or string>
            # vlan_lookup_cache: <value in [disable, enable]>
            # dos_options:
            #   npu_dos_meter_mode: <value in [local, global]>
            #   npu_dos_synproxy_mode: <value in [synack2ack, pass-synack]>
            #   npu_dos_tpe_mode: <value in [disable, enable]>
            # hash_tbl_spread: <value in [disable, enable]>
            # tcp_timeout_profile:
            #   - close_wait: <integer>
            #     fin_wait: <integer>
            #     id: <integer>
            #     syn_sent: <integer>
            #     syn_wait: <integer>
            #     tcp_idle: <integer>
            #     time_wait: <integer>
            # ip_reassembly:
            #   max_timeout: <integer>
            #   min_timeout: <integer>
            #   status: <value in [disable, enable]>
            # gtp_support: <value in [disable, enable]>
            # htx_icmp_csum_chk: <value in [pass, drop]>
            # hpe:
            #   all_protocol: <integer>
            #   arp_max: <integer>
            #   enable_shaper: <value in [disable, enable]>
            #   esp_max: <integer>
            #   high_priority: <integer>
            #   icmp_max: <integer>
            #   ip_frag_max: <integer>
            #   ip_others_max: <integer>
            #   l2_others_max: <integer>
            #   pri_type_max: <integer>
            #   sctp_max: <integer>
            #   tcp_max: <integer>
            #   tcpfin_rst_max: <integer>
            #   tcpsyn_ack_max: <integer>
            #   tcpsyn_max: <integer>
            #   udp_max: <integer>
            #   enable_queue_shaper: <value in [disable, enable]>
            #   exception_code: <integer>
            #   fragment_with_sess: <integer>
            #   fragment_without_session: <integer>
            #   queue_shaper_max: <integer>
            # dsw_dts_profile:
            #   - action: <value in [wait, drop, drop_tmr_0, ...]>
            #     min_limit: <integer>
            #     profile_id: <integer>
            #     step: <integer>
            # hash_config: <value in [5-tuple, src-ip, src-dst-ip]>
            # ipsec_ob_np_sel: <value in [RR, rr, Packet, ...]>
            # napi_break_interval: <integer>
            # background_sse_scan:
            #   scan: <value in [disable, enable]>
            #   stats_update_interval: <integer>
            #   udp_keepalive_interval: <integer>
            #   scan_stale: <integer>
            #   scan_vt: <integer>
            #   stats_qual_access: <integer>
            #   stats_qual_duration: <integer>
            #   udp_qual_access: <integer>
            #   udp_qual_duration: <integer>
            # inbound_dscp_copy_port: <list or string>
            # session_acct_interval: <integer>
            # htab_msg_queue: <value in [idle, data, dedicated]>
            # dsw_queue_dts_profile:
            #   - iport: <value in [EIF0, eif0, EIF1, ...]>
            #     name: <string>
            #     oport: <value in [EIF0, eif0, EIF1, ...]>
            #     profile_id: <integer>
            #     queue_select: <integer>
            # hw_ha_scan_interval: <integer>
            # ippool_overload_high: <integer>
            # nat46_force_ipv4_packet_forwarding: <value in [disable, enable]>
            # prp_port_out: <list or string>
            # isf_np_rx_tr_distr: <value in [port-flow, round-robin, randomized]>
            # mcast_session_counting6: <value in [disable, enable, session-based, ...]>
            # prp_port_in: <list or string>
            # rps_mode: <value in [disable, enable]>
            # per_policy_accounting: <value in [disable, enable]>
            # mcast_session_counting: <value in [disable, enable, session-based, ...]>
            # inbound_dscp_copy: <value in [disable, enable]>
            # ipsec_host_dfclr: <value in [disable, enable]>
            # process_icmp_by_host: <value in [disable, enable]>
            # dedicated_tx_npu: <value in [disable, enable]>
            # ull_port_mode: <value in [10G, 25G]>
            # sse_ha_scan:
            #   gap: <integer>
            #   max_session_cnt: <integer>
            #   min_duration: <integer>
            # hash_ipv6_sel: <integer>
            # ip_fragment_offload: <value in [disable, enable]>
            # ple_non_syn_tcp_action: <value in [forward, drop]>
            # npu_group_effective_scope: <integer>
            # ipsec_STS_timeout: <value in [1, 2, 3, ...]>
            # ipsec_throughput_msg_frequency: <value in [disable, 32KB, 64KB, ...]>
            # ipt_STS_timeout: <value in [1, 2, 3, ...]>
            # ipt_throughput_msg_frequency: <value in [disable, 32KB, 64KB, ...]>
            # default_tcp_refresh_dir: <value in [both, outgoing, incoming]>
            # default_udp_refresh_dir: <value in [both, outgoing, incoming]>
            # nss_threads_option: <value in [4t-eif, 4t-noeif, 2t]>
            # prp_session_clear_mode: <value in [blocking, non-blocking, do-not-clear]>
            # shaping_stats: <value in [disable, enable]>
            # sw_tr_hash:
            #   draco15: <value in [disable, enable]>
            #   tcp_udp_port: <value in [include, exclude]>
            # pba_port_select_mode: <value in [random, direct]>
            # spa_port_select_mode: <value in [random, direct]>
            # split_ipsec_engines: <value in [disable, enable]>
            # tunnel_over_vlink: <value in [disable, enable]>
            # max_receive_unit: <integer>
            # npu_tcam:
            #   - data:
            #       df: <value in [disable, enable]>
            #       dstip: <string>
            #       dstipv6: <string>
            #       dstmac: <string>
            #       dstport: <integer>
            #       ethertype: <string>
            #       ext_tag: <value in [disable, enable]>
            #       frag_off: <integer>
            #       gen_buf_cnt: <integer>
            #       gen_iv: <value in [invalid, valid]>
            #       gen_l3_flags: <integer>
            #       gen_l4_flags: <integer>
            #       gen_pkt_ctrl: <integer>
            #       gen_pri: <integer>
            #       gen_pri_v: <value in [invalid, valid]>
            #       gen_tv: <value in [invalid, valid]>
            #       ihl: <integer>
            #       ip4_id: <integer>
            #       ip6_fl: <integer>
            #       ipver: <integer>
            #       l4_wd10: <integer>
            #       l4_wd11: <integer>
            #       l4_wd8: <integer>
            #       l4_wd9: <integer>
            #       mf: <value in [disable, enable]>
            #       protocol: <integer>
            #       slink: <integer>
            #       smac_change: <value in [disable, enable]>
            #       sp: <integer>
            #       src_cfi: <value in [disable, enable]>
            #       src_prio: <integer>
            #       src_updt: <value in [disable, enable]>
            #       srcip: <string>
            #       srcipv6: <string>
            #       srcmac: <string>
            #       srcport: <integer>
            #       svid: <integer>
            #       tcp_ack: <value in [disable, enable]>
            #       tcp_cwr: <value in [disable, enable]>
            #       tcp_ece: <value in [disable, enable]>
            #       tcp_fin: <value in [disable, enable]>
            #       tcp_push: <value in [disable, enable]>
            #       tcp_rst: <value in [disable, enable]>
            #       tcp_syn: <value in [disable, enable]>
            #       tcp_urg: <value in [disable, enable]>
            #       tgt_cfi: <value in [disable, enable]>
            #       tgt_prio: <integer>
            #       tgt_updt: <value in [disable, enable]>
            #       tgt_v: <value in [invalid, valid]>
            #       tos: <integer>
            #       tp: <integer>
            #       ttl: <integer>
            #       tvid: <integer>
            #       vdid: <integer>
            #     dbg_dump: <integer>
            #     mask:
            #       df: <value in [disable, enable]>
            #       dstip: <string>
            #       dstipv6: <string>
            #       dstmac: <string>
            #       dstport: <integer>
            #       ethertype: <string>
            #       ext_tag: <value in [disable, enable]>
            #       frag_off: <integer>
            #       gen_buf_cnt: <integer>
            #       gen_iv: <value in [invalid, valid]>
            #       gen_l3_flags: <integer>
            #       gen_l4_flags: <integer>
            #       gen_pkt_ctrl: <integer>
            #       gen_pri: <integer>
            #       gen_pri_v: <value in [invalid, valid]>
            #       gen_tv: <value in [invalid, valid]>
            #       ihl: <integer>
            #       ip4_id: <integer>
            #       ip6_fl: <integer>
            #       ipver: <integer>
            #       l4_wd10: <integer>
            #       l4_wd11: <integer>
            #       l4_wd8: <integer>
            #       l4_wd9: <integer>
            #       mf: <value in [disable, enable]>
            #       protocol: <integer>
            #       slink: <integer>
            #       smac_change: <value in [disable, enable]>
            #       sp: <integer>
            #       src_cfi: <value in [disable, enable]>
            #       src_prio: <integer>
            #       src_updt: <value in [disable, enable]>
            #       srcip: <string>
            #       srcipv6: <string>
            #       srcmac: <string>
            #       srcport: <integer>
            #       svid: <integer>
            #       tcp_ack: <value in [disable, enable]>
            #       tcp_cwr: <value in [disable, enable]>
            #       tcp_ece: <value in [disable, enable]>
            #       tcp_fin: <value in [disable, enable]>
            #       tcp_push: <value in [disable, enable]>
            #       tcp_rst: <value in [disable, enable]>
            #       tcp_syn: <value in [disable, enable]>
            #       tcp_urg: <value in [disable, enable]>
            #       tgt_cfi: <value in [disable, enable]>
            #       tgt_prio: <integer>
            #       tgt_updt: <value in [disable, enable]>
            #       tgt_v: <value in [invalid, valid]>
            #       tos: <integer>
            #       tp: <integer>
            #       ttl: <integer>
            #       tvid: <integer>
            #       vdid: <integer>
            #     mir_act:
            #       vlif: <integer>
            #     name: <string>
            #     oid: <integer>
            #     pri_act:
            #       priority: <integer>
            #       weight: <integer>
            #     sact:
            #       act: <integer>
            #       act_v: <value in [disable, enable]>
            #       bmproc: <integer>
            #       bmproc_v: <value in [disable, enable]>
            #       df_lif: <integer>
            #       df_lif_v: <value in [disable, enable]>
            #       dfr: <integer>
            #       dfr_v: <value in [disable, enable]>
            #       dmac_skip: <integer>
            #       dmac_skip_v: <value in [disable, enable]>
            #       dosen: <integer>
            #       dosen_v: <value in [disable, enable]>
            #       espff_proc: <integer>
            #       espff_proc_v: <value in [disable, enable]>
            #       etype_pid: <integer>
            #       etype_pid_v: <value in [disable, enable]>
            #       frag_proc: <integer>
            #       frag_proc_v: <value in [disable, enable]>
            #       fwd: <integer>
            #       fwd_lif: <integer>
            #       fwd_lif_v: <value in [disable, enable]>
            #       fwd_tvid: <integer>
            #       fwd_tvid_v: <value in [disable, enable]>
            #       fwd_v: <value in [disable, enable]>
            #       icpen: <integer>
            #       icpen_v: <value in [disable, enable]>
            #       igmp_mld_snp: <integer>
            #       igmp_mld_snp_v: <value in [disable, enable]>
            #       learn: <integer>
            #       learn_v: <value in [disable, enable]>
            #       m_srh_ctrl: <integer>
            #       m_srh_ctrl_v: <value in [disable, enable]>
            #       mac_id: <integer>
            #       mac_id_v: <value in [disable, enable]>
            #       mss: <integer>
            #       mss_v: <value in [disable, enable]>
            #       pleen: <integer>
            #       pleen_v: <value in [disable, enable]>
            #       prio_pid: <integer>
            #       prio_pid_v: <value in [disable, enable]>
            #       promis: <integer>
            #       promis_v: <value in [disable, enable]>
            #       rfsh: <integer>
            #       rfsh_v: <value in [disable, enable]>
            #       smac_skip: <integer>
            #       smac_skip_v: <value in [disable, enable]>
            #       tp_smchk_v: <value in [disable, enable]>
            #       tp_smchk: <integer>
            #       tpe_id: <integer>
            #       tpe_id_v: <value in [disable, enable]>
            #       vdm: <integer>
            #       vdm_v: <value in [disable, enable]>
            #       vdom_id: <integer>
            #       vdom_id_v: <value in [disable, enable]>
            #       x_mode: <integer>
            #       x_mode_v: <value in [disable, enable]>
            #     tact:
            #       act: <integer>
            #       act_v: <value in [disable, enable]>
            #       fmtuv4_s: <integer>
            #       fmtuv4_s_v: <value in [disable, enable]>
            #       fmtuv6_s: <integer>
            #       fmtuv6_s_v: <value in [disable, enable]>
            #       lnkid: <integer>
            #       lnkid_v: <value in [disable, enable]>
            #       mac_id: <integer>
            #       mac_id_v: <value in [disable, enable]>
            #       mss_t: <integer>
            #       mss_t_v: <value in [disable, enable]>
            #       mtuv4: <integer>
            #       mtuv4_v: <value in [disable, enable]>
            #       mtuv6: <integer>
            #       mtuv6_v: <value in [disable, enable]>
            #       slif_act: <integer>
            #       slif_act_v: <value in [disable, enable]>
            #       sublnkid: <integer>
            #       sublnkid_v: <value in [disable, enable]>
            #       tgtv_act: <integer>
            #       tgtv_act_v: <value in [disable, enable]>
            #       tlif_act: <integer>
            #       tlif_act_v: <value in [disable, enable]>
            #       tpeid: <integer>
            #       tpeid_v: <value in [disable, enable]>
            #       v6fe: <integer>
            #       v6fe_v: <value in [disable, enable]>
            #       vep_en_v: <value in [disable, enable]>
            #       vep_slid: <integer>
            #       vep_slid_v: <value in [disable, enable]>
            #       vep_en: <integer>
            #       xlt_lif: <integer>
            #       xlt_lif_v: <value in [disable, enable]>
            #       xlt_vid: <integer>
            #       xlt_vid_v: <value in [disable, enable]>
            #     type: <value in [L2_src_tc, L2_tgt_tc, L2_src_mir, ...]>
            #     vid: <integer>
            # icmp_rate_ctrl:
            #   icmp_v4_bucket_size: <integer>
            #   icmp_v4_rate: <integer>
            #   icmp_v6_bucket_size: <integer>
            #   icmp_v6_rate: <integer>
            # vxlan_offload: <value in [disable, enable]>
            # icmp_error_rate_ctrl:
            #   icmpv4_error_bucket_size: <integer>
            #   icmpv4_error_rate: <integer>
            #   icmpv4_error_rate_limit: <value in [disable, enable]>
            #   icmpv6_error_bucket_size: <integer>
            #   icmpv6_error_rate: <integer>
            #   icmpv6_error_rate_limit: <value in [disable, enable]>
            # ipv4_session_quota: <value in [disable, enable]>
            # ipv4_session_quota_high: <integer>
            # ipv4_session_quota_low: <integer>
            # ipv6_prefix_session_quota: <value in [disable, enable]>
            # ipv6_prefix_session_quota_high: <integer>
            # ipv6_prefix_session_quota_low: <integer>
            # dedicated_lacp_queue: <value in [disable, enable]>
            # ipsec_ordering: <value in [disable, enable]>
            # sw_np_pause: <value in [disable, enable]>
            # sw_np_rate: <integer>
            # sw_np_rate_unit: <value in [mbps, pps]>


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
