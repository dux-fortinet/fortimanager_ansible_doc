:source: fmgr_wtpprofile.py

:orphan:

.. _fmgr_wtpprofile:

fmgr_wtpprofile -- Configure WTP profiles or FortiAP profiles that define radio settings for manageable FortiAP platforms.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

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

 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>



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
 <li><span class="li-head">state</span> - The directive to create, update or delete an object <span class="li-normal">type: str</span> <span class="li-required">required: true</span> <span class="li-normal"> choices: present, absent</span> </li>
 <li><span class="li-head">workspace_locking_adom</span> - Acquire the workspace lock if FortiManager is running in workspace mode. <span class="li-normal">type: str</span> <span class="li-required">required: false</span> <span class="li-normal"> choices: global, custom adom including root</span> </li>
 <li><span class="li-head">workspace_locking_timeout</span> - The maximum time in seconds to wait for other users to release workspace lock. <span class="li-normal">type: integer</span> <span class="li-required">required: false</span>  <span class="li-normal">default: 300</span> </li>
 <li><span class="li-head">adom</span> - The parameter in requested url <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
 <li><span class="li-head">wtpprofile</span> - Configure WTP profiles or FortiAP profiles that define radio settings for manageable FortiAP platforms. <span class="li-normal">type: dict</span></li>
 <ul class="ul-self">
 <li><span class="li-head">allowaccess</span> Control management access to the managed wtp, fortiap, or ap. <span class="li-normal">type: list</span> <span class="li-normal">choices: [https, ssh, snmp, http, telnet]</span> 
 <a id='label0' href="javascript:ContentClick('label1', 'label0');" onmouseover="ContentPreview('label1');" onmouseout="ContentUnpreview('label1');" title="click to collapse or expand..."> more... </a>
 <div id="label1" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_country</span> <b>(Alias name: ap-country)</b>  Country in which this wtp, fortiap or ap will operate (default = na, automatically use the country configured for the current vdom). <span class="li-normal">type: str</span> <span class="li-normal">choices: [AL, DZ, AR, AM, AU, AT, AZ, BH, BD, BY, BE, BZ, BO, BA, BR, BN, BG, CA, CL, CN, CO, CR, HR, CY, CZ, DK, DO, EC, EG, SV, EE, FI, FR, GE, DE, GR, GT, HN, HK, HU, IS, IN, ID, IR, IE, IL, IT, JM, JP, JO, KZ, KE, KP, KR, KW, LV, LB, LI, LT, LU, MO, MK, MY, MT, MX, MC, MA, NP, NL, AN, NZ, NO, OM, PK, PA, PG, PE, PH, PL, PT, PR, QA, RO, RU, SA, SG, SK, SI, ZA, ES, LK, SE, CH, SY, TW, TH, TT, TN, TR, AE, UA, GB, US, PS, UY, UZ, VE, VN, YE, ZW, NA, KH, TZ, SD, AO, RW, MZ, RS, ME, BB, GD, GL, GU, PY, HT, AW, MM, ZB, CF, BS, VC, MV, SN, CI, GH, MW, UG, BF, KY, TC, TM, VU, FM, GY, KN, LC, CX, AF, CM, ML, BJ, MG, TD, BW, LY, LS, MU, SL, NE, TG, RE, MD, BM, VI, PM, MF, IM, FO, GI, LA, WF, MH, BT, PF, NI, GF, AS, MP, PW, GP, ET, SR, DM, MQ, YT, BL, ZM, CG, CD, MR, IQ, FJ, --, MN, NG, GA, GM, SO, SZ, LR, DJ, TL]</span> 
 <a id='label2' href="javascript:ContentClick('label3', 'label2');" onmouseover="ContentPreview('label3');" onmouseout="ContentUnpreview('label3');" title="click to collapse or expand..."> more... </a>
 <div id="label3" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_profile</span> <b>(Alias name: ble-profile)</b>  Bluetooth low energy profile name. <span class="li-normal">type: str</span>
 <a id='label4' href="javascript:ContentClick('label5', 'label4');" onmouseover="ContentPreview('label5');" onmouseout="ContentUnpreview('label5');" title="click to collapse or expand..."> more... </a>
 <div id="label5" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">comment</span> Comment. <span class="li-normal">type: str</span>
 <a id='label6' href="javascript:ContentClick('label7', 'label6');" onmouseover="ContentPreview('label7');" onmouseout="ContentUnpreview('label7');" title="click to collapse or expand..."> more... </a>
 <div id="label7" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">control_message_offload</span> <b>(Alias name: control-message-offload)</b>  Enable/disable capwap control message data channel offload. <span class="li-normal">type: list</span> <span class="li-normal">choices: [ebp-frame, aeroscout-tag, ap-list, sta-list, sta-cap-list, stats, aeroscout-mu, sta-health, spectral-analysis]</span> 
 <a id='label8' href="javascript:ContentClick('label9', 'label8');" onmouseover="ContentPreview('label9');" onmouseout="ContentUnpreview('label9');" title="click to collapse or expand..."> more... </a>
 <div id="label9" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">deny_mac_list</span> <b>(Alias name: deny-mac-list)</b>  Deny mac list. <span class="li-normal">type: list</span>
 <a id='label10' href="javascript:ContentClick('label11', 'label10');" onmouseover="ContentPreview('label11');" onmouseout="ContentUnpreview('label11');" title="click to collapse or expand..."> more... </a>
 <div id="label11" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">id</span> Id. <span class="li-normal">type: int</span>
 <a id='label12' href="javascript:ContentClick('label13', 'label12');" onmouseover="ContentPreview('label13');" onmouseout="ContentUnpreview('label13');" title="click to collapse or expand..."> more... </a>
 <div id="label13" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mac</span> A wifi device with this mac address is denied access to this wtp, fortiap or ap. <span class="li-normal">type: str</span>
 <a id='label14' href="javascript:ContentClick('label15', 'label14');" onmouseover="ContentPreview('label15');" onmouseout="ContentUnpreview('label15');" title="click to collapse or expand..."> more... </a>
 <div id="label15" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">dtls_in_kernel</span> <b>(Alias name: dtls-in-kernel)</b>  Enable/disable data channel dtls in kernel. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label16' href="javascript:ContentClick('label17', 'label16');" onmouseover="ContentPreview('label17');" onmouseout="ContentUnpreview('label17');" title="click to collapse or expand..."> more... </a>
 <div id="label17" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dtls_policy</span> <b>(Alias name: dtls-policy)</b>  Wtp data channel dtls policy (default = clear-text). <span class="li-normal">type: list</span> <span class="li-normal">choices: [clear-text, dtls-enabled, ipsec-vpn, ipsec-sn-vpn]</span> 
 <a id='label18' href="javascript:ContentClick('label19', 'label18');" onmouseover="ContentPreview('label19');" onmouseout="ContentUnpreview('label19');" title="click to collapse or expand..."> more... </a>
 <div id="label19" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">energy_efficient_ethernet</span> <b>(Alias name: energy-efficient-ethernet)</b>  Enable/disable use of energy efficient ethernet on wtp. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label20' href="javascript:ContentClick('label21', 'label20');" onmouseover="ContentPreview('label21');" onmouseout="ContentUnpreview('label21');" title="click to collapse or expand..."> more... </a>
 <div id="label21" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ext_info_enable</span> <b>(Alias name: ext-info-enable)</b>  Enable/disable station/vap/radio extension information. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label22' href="javascript:ContentClick('label23', 'label22');" onmouseover="ContentPreview('label23');" onmouseout="ContentUnpreview('label23');" title="click to collapse or expand..."> more... </a>
 <div id="label23" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">handoff_roaming</span> <b>(Alias name: handoff-roaming)</b>  Enable/disable client load balancing during roaming to avoid roaming delay (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label24' href="javascript:ContentClick('label25', 'label24');" onmouseover="ContentPreview('label25');" onmouseout="ContentUnpreview('label25');" title="click to collapse or expand..."> more... </a>
 <div id="label25" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">handoff_rssi</span> <b>(Alias name: handoff-rssi)</b>  Minimum received signal strength indicator (rssi) value for handoff (20 - 30, default = 25). <span class="li-normal">type: int</span>
 <a id='label26' href="javascript:ContentClick('label27', 'label26');" onmouseover="ContentPreview('label27');" onmouseout="ContentUnpreview('label27');" title="click to collapse or expand..."> more... </a>
 <div id="label27" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">handoff_sta_thresh</span> <b>(Alias name: handoff-sta-thresh)</b>  Threshold value for ap handoff. <span class="li-normal">type: int</span>
 <a id='label28' href="javascript:ContentClick('label29', 'label28');" onmouseover="ContentPreview('label29');" onmouseout="ContentUnpreview('label29');" title="click to collapse or expand..."> more... </a>
 <div id="label29" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ip_fragment_preventing</span> <b>(Alias name: ip-fragment-preventing)</b>  Select how to prevent ip fragmentation for capwap tunneled control and data packets (default = tcp-mss-adjust). <span class="li-normal">type: list</span> <span class="li-normal">choices: [tcp-mss-adjust, icmp-unreachable]</span> 
 <a id='label30' href="javascript:ContentClick('label31', 'label30');" onmouseover="ContentPreview('label31');" onmouseout="ContentUnpreview('label31');" title="click to collapse or expand..."> more... </a>
 <div id="label31" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">led_schedules</span> <b>(Alias name: led-schedules)</b>  Recurring firewall schedules for illuminating leds on the fortiap. <span class="li-normal">type: list or str</span>
 <a id='label32' href="javascript:ContentClick('label33', 'label32');" onmouseover="ContentPreview('label33');" onmouseout="ContentUnpreview('label33');" title="click to collapse or expand..."> more... </a>
 <div id="label33" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">led_state</span> <b>(Alias name: led-state)</b>  Enable/disable use of leds on wtp (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label34' href="javascript:ContentClick('label35', 'label34');" onmouseover="ContentPreview('label35');" onmouseout="ContentUnpreview('label35');" title="click to collapse or expand..."> more... </a>
 <div id="label35" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">lldp</span> Enable/disable link layer discovery protocol (lldp) for the wtp, fortiap, or ap (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label36' href="javascript:ContentClick('label37', 'label36');" onmouseover="ContentPreview('label37');" onmouseout="ContentUnpreview('label37');" title="click to collapse or expand..."> more... </a>
 <div id="label37" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">login_passwd</span> <b>(Alias name: login-passwd)</b>  Set the managed wtp, fortiap, or aps administrator password. <span class="li-normal">type: list</span>
 <a id='label38' href="javascript:ContentClick('label39', 'label38');" onmouseover="ContentPreview('label39');" onmouseout="ContentUnpreview('label39');" title="click to collapse or expand..."> more... </a>
 <div id="label39" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">login_passwd_change</span> <b>(Alias name: login-passwd-change)</b>  Change or reset the administrator password of a managed wtp, fortiap or ap (yes, default, or no, default = no). <span class="li-normal">type: str</span> <span class="li-normal">choices: [no, yes, default]</span> 
 <a id='label40' href="javascript:ContentClick('label41', 'label40');" onmouseover="ContentPreview('label41');" onmouseout="ContentUnpreview('label41');" title="click to collapse or expand..."> more... </a>
 <div id="label41" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_clients</span> <b>(Alias name: max-clients)</b>  Maximum number of stations (stas) supported by the wtp (default = 0, meaning no client limitation). <span class="li-normal">type: int</span>
 <a id='label42' href="javascript:ContentClick('label43', 'label42');" onmouseover="ContentPreview('label43');" onmouseout="ContentUnpreview('label43');" title="click to collapse or expand..."> more... </a>
 <div id="label43" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">name</span> Wtp (or fortiap or ap) profile name. <span class="li-normal">type: str</span>
 <a id='label44' href="javascript:ContentClick('label45', 'label44');" onmouseover="ContentPreview('label45');" onmouseout="ContentUnpreview('label45');" title="click to collapse or expand..."> more... </a>
 <div id="label45" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">poe_mode</span> <b>(Alias name: poe-mode)</b>  Set the wtp, fortiap, or aps poe mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [auto, 8023af, 8023at, power-adapter, full, high, low]</span> 
 <a id='label46' href="javascript:ContentClick('label47', 'label46');" onmouseover="ContentPreview('label47');" onmouseout="ContentUnpreview('label47');" title="click to collapse or expand..."> more... </a>
 <div id="label47" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">split_tunneling_acl</span> <b>(Alias name: split-tunneling-acl)</b>  Split tunneling acl. <span class="li-normal">type: list</span>
 <a id='label48' href="javascript:ContentClick('label49', 'label48');" onmouseover="ContentPreview('label49');" onmouseout="ContentUnpreview('label49');" title="click to collapse or expand..."> more... </a>
 <div id="label49" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">dest_ip</span> <b>(Alias name: dest-ip)</b>  Destination ip and mask for the split-tunneling subnet. <span class="li-normal">type: str</span>
 <a id='label50' href="javascript:ContentClick('label51', 'label50');" onmouseover="ContentPreview('label51');" onmouseout="ContentUnpreview('label51');" title="click to collapse or expand..."> more... </a>
 <div id="label51" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">id</span> Id. <span class="li-normal">type: int</span>
 <a id='label52' href="javascript:ContentClick('label53', 'label52');" onmouseover="ContentPreview('label53');" onmouseout="ContentUnpreview('label53');" title="click to collapse or expand..."> more... </a>
 <div id="label53" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">split_tunneling_acl_local_ap_subnet</span> <b>(Alias name: split-tunneling-acl-local-ap-subnet)</b>  Enable/disable automatically adding local subnetwork of fortiap to split-tunneling acl (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label54' href="javascript:ContentClick('label55', 'label54');" onmouseover="ContentPreview('label55');" onmouseout="ContentUnpreview('label55');" title="click to collapse or expand..."> more... </a>
 <div id="label55" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">split_tunneling_acl_path</span> <b>(Alias name: split-tunneling-acl-path)</b>  Split tunneling acl path is local/tunnel. <span class="li-normal">type: str</span> <span class="li-normal">choices: [tunnel, local]</span> 
 <a id='label56' href="javascript:ContentClick('label57', 'label56');" onmouseover="ContentPreview('label57');" onmouseout="ContentUnpreview('label57');" title="click to collapse or expand..."> more... </a>
 <div id="label57" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tun_mtu_downlink</span> <b>(Alias name: tun-mtu-downlink)</b>  Downlink capwap tunnel mtu (0, 576, or 1500 bytes, default = 0). <span class="li-normal">type: int</span>
 <a id='label58' href="javascript:ContentClick('label59', 'label58');" onmouseover="ContentPreview('label59');" onmouseout="ContentUnpreview('label59');" title="click to collapse or expand..."> more... </a>
 <div id="label59" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tun_mtu_uplink</span> <b>(Alias name: tun-mtu-uplink)</b>  Uplink capwap tunnel mtu (0, 576, or 1500 bytes, default = 0). <span class="li-normal">type: int</span>
 <a id='label60' href="javascript:ContentClick('label61', 'label60');" onmouseover="ContentPreview('label61');" onmouseout="ContentUnpreview('label61');" title="click to collapse or expand..."> more... </a>
 <div id="label61" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wan_port_mode</span> <b>(Alias name: wan-port-mode)</b>  Enable/disable using a wan port as a lan port. <span class="li-normal">type: str</span> <span class="li-normal">choices: [wan-lan, wan-only]</span> 
 <a id='label62' href="javascript:ContentClick('label63', 'label62');" onmouseover="ContentPreview('label63');" onmouseout="ContentUnpreview('label63');" title="click to collapse or expand..."> more... </a>
 <div id="label63" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">snmp</span> Enable/disable snmp for the wtp, fortiap, or ap (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label64' href="javascript:ContentClick('label65', 'label64');" onmouseover="ContentPreview('label65');" onmouseout="ContentUnpreview('label65');" title="click to collapse or expand..."> more... </a>
 <div id="label65" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.0 -> v7.2.0</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_handoff</span> <b>(Alias name: ap-handoff)</b>  Enable/disable ap handoff of clients to other aps (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label66' href="javascript:ContentClick('label67', 'label66');" onmouseover="ContentPreview('label67');" onmouseout="ContentUnpreview('label67');" title="click to collapse or expand..."> more... </a>
 <div id="label67" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">apcfg_profile</span> <b>(Alias name: apcfg-profile)</b>  Ap local configuration profile name. <span class="li-normal">type: str</span>
 <a id='label68' href="javascript:ContentClick('label69', 'label68');" onmouseover="ContentPreview('label69');" onmouseout="ContentUnpreview('label69');" title="click to collapse or expand..."> more... </a>
 <div id="label69" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frequency_handoff</span> <b>(Alias name: frequency-handoff)</b>  Enable/disable frequency handoff of clients to other channels (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label70' href="javascript:ContentClick('label71', 'label70');" onmouseover="ContentPreview('label71');" onmouseout="ContentUnpreview('label71');" title="click to collapse or expand..."> more... </a>
 <div id="label71" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">lan</span> Lan. <span class="li-normal">type: dict</span>
 <a id='label72' href="javascript:ContentClick('label73', 'label72');" onmouseover="ContentPreview('label73');" onmouseout="ContentUnpreview('label73');" title="click to collapse or expand..."> more... </a>
 <div id="label73" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">port_esl_mode</span> <b>(Alias name: port-esl-mode)</b>  Esl port mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label74' href="javascript:ContentClick('label75', 'label74');" onmouseover="ContentPreview('label75');" onmouseout="ContentUnpreview('label75');" title="click to collapse or expand..."> more... </a>
 <div id="label75" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port_esl_ssid</span> <b>(Alias name: port-esl-ssid)</b>  Bridge esl port to ssid. <span class="li-normal">type: str</span>
 <a id='label76' href="javascript:ContentClick('label77', 'label76');" onmouseover="ContentPreview('label77');" onmouseout="ContentUnpreview('label77');" title="click to collapse or expand..."> more... </a>
 <div id="label77" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port_mode</span> <b>(Alias name: port-mode)</b>  Lan port mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label78' href="javascript:ContentClick('label79', 'label78');" onmouseover="ContentPreview('label79');" onmouseout="ContentUnpreview('label79');" title="click to collapse or expand..."> more... </a>
 <div id="label79" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port_ssid</span> <b>(Alias name: port-ssid)</b>  Bridge lan port to ssid. <span class="li-normal">type: str</span>
 <a id='label80' href="javascript:ContentClick('label81', 'label80');" onmouseover="ContentPreview('label81');" onmouseout="ContentUnpreview('label81');" title="click to collapse or expand..."> more... </a>
 <div id="label81" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port1_mode</span> <b>(Alias name: port1-mode)</b>  Lan port 1 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label82' href="javascript:ContentClick('label83', 'label82');" onmouseover="ContentPreview('label83');" onmouseout="ContentUnpreview('label83');" title="click to collapse or expand..."> more... </a>
 <div id="label83" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port1_ssid</span> <b>(Alias name: port1-ssid)</b>  Bridge lan port 1 to ssid. <span class="li-normal">type: str</span>
 <a id='label84' href="javascript:ContentClick('label85', 'label84');" onmouseover="ContentPreview('label85');" onmouseout="ContentUnpreview('label85');" title="click to collapse or expand..."> more... </a>
 <div id="label85" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port2_mode</span> <b>(Alias name: port2-mode)</b>  Lan port 2 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label86' href="javascript:ContentClick('label87', 'label86');" onmouseover="ContentPreview('label87');" onmouseout="ContentUnpreview('label87');" title="click to collapse or expand..."> more... </a>
 <div id="label87" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port2_ssid</span> <b>(Alias name: port2-ssid)</b>  Bridge lan port 2 to ssid. <span class="li-normal">type: str</span>
 <a id='label88' href="javascript:ContentClick('label89', 'label88');" onmouseover="ContentPreview('label89');" onmouseout="ContentUnpreview('label89');" title="click to collapse or expand..."> more... </a>
 <div id="label89" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port3_mode</span> <b>(Alias name: port3-mode)</b>  Lan port 3 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label90' href="javascript:ContentClick('label91', 'label90');" onmouseover="ContentPreview('label91');" onmouseout="ContentUnpreview('label91');" title="click to collapse or expand..."> more... </a>
 <div id="label91" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port3_ssid</span> <b>(Alias name: port3-ssid)</b>  Bridge lan port 3 to ssid. <span class="li-normal">type: str</span>
 <a id='label92' href="javascript:ContentClick('label93', 'label92');" onmouseover="ContentPreview('label93');" onmouseout="ContentUnpreview('label93');" title="click to collapse or expand..."> more... </a>
 <div id="label93" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port4_mode</span> <b>(Alias name: port4-mode)</b>  Lan port 4 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label94' href="javascript:ContentClick('label95', 'label94');" onmouseover="ContentPreview('label95');" onmouseout="ContentUnpreview('label95');" title="click to collapse or expand..."> more... </a>
 <div id="label95" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port4_ssid</span> <b>(Alias name: port4-ssid)</b>  Bridge lan port 4 to ssid. <span class="li-normal">type: str</span>
 <a id='label96' href="javascript:ContentClick('label97', 'label96');" onmouseover="ContentPreview('label97');" onmouseout="ContentUnpreview('label97');" title="click to collapse or expand..."> more... </a>
 <div id="label97" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port5_mode</span> <b>(Alias name: port5-mode)</b>  Lan port 5 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label98' href="javascript:ContentClick('label99', 'label98');" onmouseover="ContentPreview('label99');" onmouseout="ContentUnpreview('label99');" title="click to collapse or expand..."> more... </a>
 <div id="label99" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port5_ssid</span> <b>(Alias name: port5-ssid)</b>  Bridge lan port 5 to ssid. <span class="li-normal">type: str</span>
 <a id='label100' href="javascript:ContentClick('label101', 'label100');" onmouseover="ContentPreview('label101');" onmouseout="ContentUnpreview('label101');" title="click to collapse or expand..."> more... </a>
 <div id="label101" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port6_mode</span> <b>(Alias name: port6-mode)</b>  Lan port 6 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label102' href="javascript:ContentClick('label103', 'label102');" onmouseover="ContentPreview('label103');" onmouseout="ContentUnpreview('label103');" title="click to collapse or expand..."> more... </a>
 <div id="label103" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port6_ssid</span> <b>(Alias name: port6-ssid)</b>  Bridge lan port 6 to ssid. <span class="li-normal">type: str</span>
 <a id='label104' href="javascript:ContentClick('label105', 'label104');" onmouseover="ContentPreview('label105');" onmouseout="ContentUnpreview('label105');" title="click to collapse or expand..."> more... </a>
 <div id="label105" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port7_mode</span> <b>(Alias name: port7-mode)</b>  Lan port 7 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label106' href="javascript:ContentClick('label107', 'label106');" onmouseover="ContentPreview('label107');" onmouseout="ContentUnpreview('label107');" title="click to collapse or expand..."> more... </a>
 <div id="label107" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port7_ssid</span> <b>(Alias name: port7-ssid)</b>  Bridge lan port 7 to ssid. <span class="li-normal">type: str</span>
 <a id='label108' href="javascript:ContentClick('label109', 'label108');" onmouseover="ContentPreview('label109');" onmouseout="ContentUnpreview('label109');" title="click to collapse or expand..."> more... </a>
 <div id="label109" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port8_mode</span> <b>(Alias name: port8-mode)</b>  Lan port 8 mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: [offline, bridge-to-wan, bridge-to-ssid, nat-to-wan]</span> 
 <a id='label110' href="javascript:ContentClick('label111', 'label110');" onmouseover="ContentPreview('label111');" onmouseout="ContentUnpreview('label111');" title="click to collapse or expand..."> more... </a>
 <div id="label111" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">port8_ssid</span> <b>(Alias name: port8-ssid)</b>  Bridge lan port 8 to ssid. <span class="li-normal">type: str</span>
 <a id='label112' href="javascript:ContentClick('label113', 'label112');" onmouseover="ContentPreview('label113');" onmouseout="ContentUnpreview('label113');" title="click to collapse or expand..."> more... </a>
 <div id="label113" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">lbs</span> Lbs. <span class="li-normal">type: dict</span>
 <a id='label114' href="javascript:ContentClick('label115', 'label114');" onmouseover="ContentPreview('label115');" onmouseout="ContentUnpreview('label115');" title="click to collapse or expand..."> more... </a>
 <div id="label115" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">aeroscout</span> Enable/disable aeroscout real time location service (rtls) support (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label116' href="javascript:ContentClick('label117', 'label116');" onmouseover="ContentPreview('label117');" onmouseout="ContentUnpreview('label117');" title="click to collapse or expand..."> more... </a>
 <div id="label117" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_ap_mac</span> <b>(Alias name: aeroscout-ap-mac)</b>  Use bssid or board mac address as ap mac address in aeroscout ap messages (default = bssid). <span class="li-normal">type: str</span> <span class="li-normal">choices: [bssid, board-mac]</span> 
 <a id='label118' href="javascript:ContentClick('label119', 'label118');" onmouseover="ContentPreview('label119');" onmouseout="ContentUnpreview('label119');" title="click to collapse or expand..."> more... </a>
 <div id="label119" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_mmu_report</span> <b>(Alias name: aeroscout-mmu-report)</b>  Enable/disable compounded aeroscout tag and mu report (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label120' href="javascript:ContentClick('label121', 'label120');" onmouseover="ContentPreview('label121');" onmouseout="ContentUnpreview('label121');" title="click to collapse or expand..."> more... </a>
 <div id="label121" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_mu</span> <b>(Alias name: aeroscout-mu)</b>  Enable/disable aeroscout mobile unit (mu) support (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label122' href="javascript:ContentClick('label123', 'label122');" onmouseover="ContentPreview('label123');" onmouseout="ContentUnpreview('label123');" title="click to collapse or expand..."> more... </a>
 <div id="label123" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_mu_factor</span> <b>(Alias name: aeroscout-mu-factor)</b>  Aeroscout mu mode dilution factor (default = 20). <span class="li-normal">type: int</span>
 <a id='label124' href="javascript:ContentClick('label125', 'label124');" onmouseover="ContentPreview('label125');" onmouseout="ContentUnpreview('label125');" title="click to collapse or expand..."> more... </a>
 <div id="label125" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_mu_timeout</span> <b>(Alias name: aeroscout-mu-timeout)</b>  Aeroscout mu mode timeout (0 - 65535 sec, default = 5). <span class="li-normal">type: int</span>
 <a id='label126' href="javascript:ContentClick('label127', 'label126');" onmouseover="ContentPreview('label127');" onmouseout="ContentUnpreview('label127');" title="click to collapse or expand..."> more... </a>
 <div id="label127" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_server_ip</span> <b>(Alias name: aeroscout-server-ip)</b>  Ip address of aeroscout server. <span class="li-normal">type: str</span>
 <a id='label128' href="javascript:ContentClick('label129', 'label128');" onmouseover="ContentPreview('label129');" onmouseout="ContentUnpreview('label129');" title="click to collapse or expand..."> more... </a>
 <div id="label129" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">aeroscout_server_port</span> <b>(Alias name: aeroscout-server-port)</b>  Aeroscout server udp listening port. <span class="li-normal">type: int</span>
 <a id='label130' href="javascript:ContentClick('label131', 'label130');" onmouseover="ContentPreview('label131');" onmouseout="ContentUnpreview('label131');" title="click to collapse or expand..."> more... </a>
 <div id="label131" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ekahau_blink_mode</span> <b>(Alias name: ekahau-blink-mode)</b>  Enable/disable ekahau blink mode (now known as airista flow) to track and locate wifi tags (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label132' href="javascript:ContentClick('label133', 'label132');" onmouseover="ContentPreview('label133');" onmouseout="ContentUnpreview('label133');" title="click to collapse or expand..."> more... </a>
 <div id="label133" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ekahau_tag</span> <b>(Alias name: ekahau-tag)</b>  Wifi frame mac address or wifi tag. <span class="li-normal">type: str</span>
 <a id='label134' href="javascript:ContentClick('label135', 'label134');" onmouseover="ContentPreview('label135');" onmouseout="ContentUnpreview('label135');" title="click to collapse or expand..."> more... </a>
 <div id="label135" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">erc_server_ip</span> <b>(Alias name: erc-server-ip)</b>  Ip address of ekahau rtls controller (erc). <span class="li-normal">type: str</span>
 <a id='label136' href="javascript:ContentClick('label137', 'label136');" onmouseover="ContentPreview('label137');" onmouseout="ContentUnpreview('label137');" title="click to collapse or expand..."> more... </a>
 <div id="label137" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">erc_server_port</span> <b>(Alias name: erc-server-port)</b>  Ekahau rtls controller (erc) udp listening port. <span class="li-normal">type: int</span>
 <a id='label138' href="javascript:ContentClick('label139', 'label138');" onmouseover="ContentPreview('label139');" onmouseout="ContentUnpreview('label139');" title="click to collapse or expand..."> more... </a>
 <div id="label139" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence</span> Enable/disable fortipresence to monitor the location and activity of wifi clients even if they dont connect to this wifi network (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, enable2, foreign, both]</span> 
 <a id='label140' href="javascript:ContentClick('label141', 'label140');" onmouseover="ContentPreview('label141');" onmouseout="ContentUnpreview('label141');" title="click to collapse or expand..."> more... </a>
 <div id="label141" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_ble</span> <b>(Alias name: fortipresence-ble)</b>  Enable/disable fortipresence finding and reporting ble devices. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label142' href="javascript:ContentClick('label143', 'label142');" onmouseover="ContentPreview('label143');" onmouseout="ContentUnpreview('label143');" title="click to collapse or expand..."> more... </a>
 <div id="label143" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_frequency</span> <b>(Alias name: fortipresence-frequency)</b>  Fortipresence report transmit frequency (5 - 65535 sec, default = 30). <span class="li-normal">type: int</span>
 <a id='label144' href="javascript:ContentClick('label145', 'label144');" onmouseover="ContentPreview('label145');" onmouseout="ContentUnpreview('label145');" title="click to collapse or expand..."> more... </a>
 <div id="label145" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_port</span> <b>(Alias name: fortipresence-port)</b>  Fortipresence server udp listening port (default = 3000). <span class="li-normal">type: int</span>
 <a id='label146' href="javascript:ContentClick('label147', 'label146');" onmouseover="ContentPreview('label147');" onmouseout="ContentUnpreview('label147');" title="click to collapse or expand..."> more... </a>
 <div id="label147" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_project</span> <b>(Alias name: fortipresence-project)</b>  Fortipresence project name (max. <span class="li-normal">type: str</span>
 <a id='label148' href="javascript:ContentClick('label149', 'label148');" onmouseover="ContentPreview('label149');" onmouseout="ContentUnpreview('label149');" title="click to collapse or expand..."> more... </a>
 <div id="label149" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_rogue</span> <b>(Alias name: fortipresence-rogue)</b>  Enable/disable fortipresence finding and reporting rogue aps. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label150' href="javascript:ContentClick('label151', 'label150');" onmouseover="ContentPreview('label151');" onmouseout="ContentUnpreview('label151');" title="click to collapse or expand..."> more... </a>
 <div id="label151" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_secret</span> <b>(Alias name: fortipresence-secret)</b>  Fortipresence secret password (max. <span class="li-normal">type: list</span>
 <a id='label152' href="javascript:ContentClick('label153', 'label152');" onmouseover="ContentPreview('label153');" onmouseout="ContentUnpreview('label153');" title="click to collapse or expand..."> more... </a>
 <div id="label153" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_server</span> <b>(Alias name: fortipresence-server)</b>  Fortipresence server ip address. <span class="li-normal">type: str</span>
 <a id='label154' href="javascript:ContentClick('label155', 'label154');" onmouseover="ContentPreview('label155');" onmouseout="ContentUnpreview('label155');" title="click to collapse or expand..."> more... </a>
 <div id="label155" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_unassoc</span> <b>(Alias name: fortipresence-unassoc)</b>  Enable/disable fortipresence finding and reporting unassociated stations. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label156' href="javascript:ContentClick('label157', 'label156');" onmouseover="ContentPreview('label157');" onmouseout="ContentUnpreview('label157');" title="click to collapse or expand..."> more... </a>
 <div id="label157" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">station_locate</span> <b>(Alias name: station-locate)</b>  Enable/disable client station locating services for all clients, whether associated or not (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label158' href="javascript:ContentClick('label159', 'label158');" onmouseover="ContentPreview('label159');" onmouseout="ContentUnpreview('label159');" title="click to collapse or expand..."> more... </a>
 <div id="label159" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_server_addr_type</span> <b>(Alias name: fortipresence-server-addr-type)</b>  Fortipresence server address type (default = ipv4). <span class="li-normal">type: str</span> <span class="li-normal">choices: [fqdn, ipv4]</span> 
 <a id='label160' href="javascript:ContentClick('label161', 'label160');" onmouseover="ContentPreview('label161');" onmouseout="ContentUnpreview('label161');" title="click to collapse or expand..."> more... </a>
 <div id="label161" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">fortipresence_server_fqdn</span> <b>(Alias name: fortipresence-server-fqdn)</b>  Fqdn of fortipresence server. <span class="li-normal">type: str</span>
 <a id='label162' href="javascript:ContentClick('label163', 'label162');" onmouseover="ContentPreview('label163');" onmouseout="ContentUnpreview('label163');" title="click to collapse or expand..."> more... </a>
 <div id="label163" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar</span> Enable/disable polestar ble nao track real time location service (rtls) support (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label164' href="javascript:ContentClick('label165', 'label164');" onmouseover="ContentPreview('label165');" onmouseout="ContentUnpreview('label165');" title="click to collapse or expand..."> more... </a>
 <div id="label165" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_accumulation_interval</span> <b>(Alias name: polestar-accumulation-interval)</b>  Time that measurements should be accumulated in seconds (default = 2). <span class="li-normal">type: int</span>
 <a id='label166' href="javascript:ContentClick('label167', 'label166');" onmouseover="ContentPreview('label167');" onmouseout="ContentUnpreview('label167');" title="click to collapse or expand..."> more... </a>
 <div id="label167" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_asset_addrgrp_list</span> <b>(Alias name: polestar-asset-addrgrp-list)</b>  Tags and asset addrgrp list to be reported. <span class="li-normal">type: str</span>
 <a id='label168' href="javascript:ContentClick('label169', 'label168');" onmouseover="ContentPreview('label169');" onmouseout="ContentUnpreview('label169');" title="click to collapse or expand..."> more... </a>
 <div id="label169" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_asset_uuid_list1</span> <b>(Alias name: polestar-asset-uuid-list1)</b>  Tags and asset uuid list 1 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label170' href="javascript:ContentClick('label171', 'label170');" onmouseover="ContentPreview('label171');" onmouseout="ContentUnpreview('label171');" title="click to collapse or expand..."> more... </a>
 <div id="label171" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_asset_uuid_list2</span> <b>(Alias name: polestar-asset-uuid-list2)</b>  Tags and asset uuid list 2 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label172' href="javascript:ContentClick('label173', 'label172');" onmouseover="ContentPreview('label173');" onmouseout="ContentUnpreview('label173');" title="click to collapse or expand..."> more... </a>
 <div id="label173" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_asset_uuid_list3</span> <b>(Alias name: polestar-asset-uuid-list3)</b>  Tags and asset uuid list 3 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label174' href="javascript:ContentClick('label175', 'label174');" onmouseover="ContentPreview('label175');" onmouseout="ContentUnpreview('label175');" title="click to collapse or expand..."> more... </a>
 <div id="label175" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_asset_uuid_list4</span> <b>(Alias name: polestar-asset-uuid-list4)</b>  Tags and asset uuid list 4 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label176' href="javascript:ContentClick('label177', 'label176');" onmouseover="ContentPreview('label177');" onmouseout="ContentUnpreview('label177');" title="click to collapse or expand..."> more... </a>
 <div id="label177" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_protocol</span> <b>(Alias name: polestar-protocol)</b>  Select the protocol to report measurements, advertising data, or location data to nao cloud. <span class="li-normal">type: str</span> <span class="li-normal">choices: [WSS]</span> 
 <a id='label178' href="javascript:ContentClick('label179', 'label178');" onmouseover="ContentPreview('label179');" onmouseout="ContentUnpreview('label179');" title="click to collapse or expand..."> more... </a>
 <div id="label179" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_reporting_interval</span> <b>(Alias name: polestar-reporting-interval)</b>  Time between reporting accumulated measurements in seconds (default = 2). <span class="li-normal">type: int</span>
 <a id='label180' href="javascript:ContentClick('label181', 'label180');" onmouseover="ContentPreview('label181');" onmouseout="ContentUnpreview('label181');" title="click to collapse or expand..."> more... </a>
 <div id="label181" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_server_fqdn</span> <b>(Alias name: polestar-server-fqdn)</b>  Fqdn of polestar nao track server (default = ws. <span class="li-normal">type: str</span>
 <a id='label182' href="javascript:ContentClick('label183', 'label182');" onmouseover="ContentPreview('label183');" onmouseout="ContentUnpreview('label183');" title="click to collapse or expand..."> more... </a>
 <div id="label183" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_server_path</span> <b>(Alias name: polestar-server-path)</b>  Path of polestar nao track server (default = /v1/token/<access_token>/pst-v2). <span class="li-normal">type: str</span>
 <a id='label184' href="javascript:ContentClick('label185', 'label184');" onmouseover="ContentPreview('label185');" onmouseout="ContentUnpreview('label185');" title="click to collapse or expand..."> more... </a>
 <div id="label185" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_server_port</span> <b>(Alias name: polestar-server-port)</b>  Port of polestar nao track server (default = 443). <span class="li-normal">type: int</span>
 <a id='label186' href="javascript:ContentClick('label187', 'label186');" onmouseover="ContentPreview('label187');" onmouseout="ContentUnpreview('label187');" title="click to collapse or expand..."> more... </a>
 <div id="label187" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">polestar_server_token</span> <b>(Alias name: polestar-server-token)</b>  Access token of polestar nao track server. <span class="li-normal">type: str</span>
 <a id='label188' href="javascript:ContentClick('label189', 'label188');" onmouseover="ContentPreview('label189');" onmouseout="ContentUnpreview('label189');" title="click to collapse or expand..."> more... </a>
 <div id="label189" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls</span> <b>(Alias name: ble-rtls)</b>  Set ble real time location service (rtls) support (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, polestar, evresys]</span> 
 <a id='label190' href="javascript:ContentClick('label191', 'label190');" onmouseover="ContentPreview('label191');" onmouseout="ContentUnpreview('label191');" title="click to collapse or expand..."> more... </a>
 <div id="label191" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_accumulation_interval</span> <b>(Alias name: ble-rtls-accumulation-interval)</b>  Time that measurements should be accumulated in seconds (default = 2). <span class="li-normal">type: int</span>
 <a id='label192' href="javascript:ContentClick('label193', 'label192');" onmouseover="ContentPreview('label193');" onmouseout="ContentUnpreview('label193');" title="click to collapse or expand..."> more... </a>
 <div id="label193" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_asset_addrgrp_list</span> <b>(Alias name: ble-rtls-asset-addrgrp-list)</b>  Tags and asset addrgrp list to be reported. <span class="li-normal">type: list</span>
 <a id='label194' href="javascript:ContentClick('label195', 'label194');" onmouseover="ContentPreview('label195');" onmouseout="ContentUnpreview('label195');" title="click to collapse or expand..."> more... </a>
 <div id="label195" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_asset_uuid_list1</span> <b>(Alias name: ble-rtls-asset-uuid-list1)</b>  Tags and asset uuid list 1 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label196' href="javascript:ContentClick('label197', 'label196');" onmouseover="ContentPreview('label197');" onmouseout="ContentUnpreview('label197');" title="click to collapse or expand..."> more... </a>
 <div id="label197" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_asset_uuid_list2</span> <b>(Alias name: ble-rtls-asset-uuid-list2)</b>  Tags and asset uuid list 2 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label198' href="javascript:ContentClick('label199', 'label198');" onmouseover="ContentPreview('label199');" onmouseout="ContentUnpreview('label199');" title="click to collapse or expand..."> more... </a>
 <div id="label199" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_asset_uuid_list3</span> <b>(Alias name: ble-rtls-asset-uuid-list3)</b>  Tags and asset uuid list 3 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label200' href="javascript:ContentClick('label201', 'label200');" onmouseover="ContentPreview('label201');" onmouseout="ContentUnpreview('label201');" title="click to collapse or expand..."> more... </a>
 <div id="label201" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_asset_uuid_list4</span> <b>(Alias name: ble-rtls-asset-uuid-list4)</b>  Tags and asset uuid list 4 to be reported (string in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx). <span class="li-normal">type: str</span>
 <a id='label202' href="javascript:ContentClick('label203', 'label202');" onmouseover="ContentPreview('label203');" onmouseout="ContentUnpreview('label203');" title="click to collapse or expand..."> more... </a>
 <div id="label203" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_protocol</span> <b>(Alias name: ble-rtls-protocol)</b>  Select the protocol to report measurements, advertising data, or location data to cloud server. <span class="li-normal">type: str</span> <span class="li-normal">choices: [WSS]</span> 
 <a id='label204' href="javascript:ContentClick('label205', 'label204');" onmouseover="ContentPreview('label205');" onmouseout="ContentUnpreview('label205');" title="click to collapse or expand..."> more... </a>
 <div id="label205" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_reporting_interval</span> <b>(Alias name: ble-rtls-reporting-interval)</b>  Time between reporting accumulated measurements in seconds (default = 2). <span class="li-normal">type: int</span>
 <a id='label206' href="javascript:ContentClick('label207', 'label206');" onmouseover="ContentPreview('label207');" onmouseout="ContentUnpreview('label207');" title="click to collapse or expand..."> more... </a>
 <div id="label207" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_server_fqdn</span> <b>(Alias name: ble-rtls-server-fqdn)</b>  Fqdn of ble real time location service (rtls) server. <span class="li-normal">type: str</span>
 <a id='label208' href="javascript:ContentClick('label209', 'label208');" onmouseover="ContentPreview('label209');" onmouseout="ContentUnpreview('label209');" title="click to collapse or expand..."> more... </a>
 <div id="label209" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_server_path</span> <b>(Alias name: ble-rtls-server-path)</b>  Path of ble real time location service (rtls) server. <span class="li-normal">type: str</span>
 <a id='label210' href="javascript:ContentClick('label211', 'label210');" onmouseover="ContentPreview('label211');" onmouseout="ContentUnpreview('label211');" title="click to collapse or expand..."> more... </a>
 <div id="label211" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_server_port</span> <b>(Alias name: ble-rtls-server-port)</b>  Port of ble real time location service (rtls) server (default = 443). <span class="li-normal">type: int</span>
 <a id='label212' href="javascript:ContentClick('label213', 'label212');" onmouseover="ContentPreview('label213');" onmouseout="ContentUnpreview('label213');" title="click to collapse or expand..."> more... </a>
 <div id="label213" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ble_rtls_server_token</span> <b>(Alias name: ble-rtls-server-token)</b>  Access token of ble real time location service (rtls) server. <span class="li-normal">type: str</span>
 <a id='label214' href="javascript:ContentClick('label215', 'label214');" onmouseover="ContentPreview('label215');" onmouseout="ContentUnpreview('label215');" title="click to collapse or expand..."> more... </a>
 <div id="label215" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> v7.4.7</code>, <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">platform</span> Platform. <span class="li-normal">type: dict</span>
 <a id='label216' href="javascript:ContentClick('label217', 'label216');" onmouseover="ContentPreview('label217');" onmouseout="ContentUnpreview('label217');" title="click to collapse or expand..."> more... </a>
 <div id="label217" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">ddscan</span> Enable/disable use of one radio for dedicated dual-band scanning to detect rf characterization and wireless threat management. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label218' href="javascript:ContentClick('label219', 'label218');" onmouseover="ContentPreview('label219');" onmouseout="ContentUnpreview('label219');" title="click to collapse or expand..."> more... </a>
 <div id="label219" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mode</span> Configure operation mode of 5g radios (default = single-5g). <span class="li-normal">type: str</span> <span class="li-normal">choices: [dual-5G, single-5G]</span> 
 <a id='label220' href="javascript:ContentClick('label221', 'label220');" onmouseover="ContentPreview('label221');" onmouseout="ContentUnpreview('label221');" title="click to collapse or expand..."> more... </a>
 <div id="label221" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">type</span> Wtp, fortiap or ap platform type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [30B-50B, 60B, 80CM-81CM, 220A, 220B, 210B, 60C, 222B, 112B, 320B, 11C, 14C, 223B, 28C, 320C, 221C, 25D, 222C, 224D, 214B, 21D, 24D, 112D, 223C, 321C, C220C, C225C, S321C, S323C, FWF, S311C, S313C, AP-11N, S322C, S321CR, S322CR, S323CR, S421E, S422E, S423E, 421E, 423E, C221E, C226E, C23JD, C24JE, C21D, U421E, U423E, 221E, 222E, 223E, S221E, S223E, U221EV, U223EV, U321EV, U323EV, 224E, U422EV, U24JEV, 321E, U431F, U433F, 231E, 431F, 433F, 231F, 432F, 234F, 23JF, U231F, 831F, U234F, U432F, 431FL, 432FR, 433FL, 231FL, 231G, 233G, 431G, 433G, U231G, U441G, 234G, 432G, 441K, 443K, 241K, 243K, 231K, 23JK]</span> 
 <a id='label222' href="javascript:ContentClick('label223', 'label222');" onmouseover="ContentPreview('label223');" onmouseout="ContentUnpreview('label223');" title="click to collapse or expand..."> more... </a>
 <div id="label223" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">_local_platform_str</span> Local platform str. <span class="li-normal">type: str</span>
 <a id='label224' href="javascript:ContentClick('label225', 'label224');" onmouseover="ContentPreview('label225');" onmouseout="ContentUnpreview('label225');" title="click to collapse or expand..."> more... </a>
 <div id="label225" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.6 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">radio_1</span> <b>(Alias name: radio-1)</b>  Radio 1. <span class="li-normal">type: dict</span>
 <a id='label226' href="javascript:ContentClick('label227', 'label226');" onmouseover="ContentPreview('label227');" onmouseout="ContentUnpreview('label227');" title="click to collapse or expand..."> more... </a>
 <div id="label227" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">airtime_fairness</span> <b>(Alias name: airtime-fairness)</b>  Enable/disable airtime fairness (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label228' href="javascript:ContentClick('label229', 'label228');" onmouseover="ContentPreview('label229');" onmouseout="ContentUnpreview('label229');" title="click to collapse or expand..."> more... </a>
 <div id="label229" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">amsdu</span> Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label230' href="javascript:ContentClick('label231', 'label230');" onmouseover="ContentPreview('label231');" onmouseout="ContentUnpreview('label231');" title="click to collapse or expand..."> more... </a>
 <div id="label231" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_addr</span> <b>(Alias name: ap-sniffer-addr)</b>  Mac address to monitor. <span class="li-normal">type: str</span>
 <a id='label232' href="javascript:ContentClick('label233', 'label232');" onmouseover="ContentPreview('label233');" onmouseout="ContentUnpreview('label233');" title="click to collapse or expand..."> more... </a>
 <div id="label233" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_bufsize</span> <b>(Alias name: ap-sniffer-bufsize)</b>  Sniffer buffer size (1 - 32 mb, default = 16). <span class="li-normal">type: int</span>
 <a id='label234' href="javascript:ContentClick('label235', 'label234');" onmouseover="ContentPreview('label235');" onmouseout="ContentUnpreview('label235');" title="click to collapse or expand..."> more... </a>
 <div id="label235" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan</span> <b>(Alias name: ap-sniffer-chan)</b>  Channel on which to operate the sniffer (default = 6). <span class="li-normal">type: int</span>
 <a id='label236' href="javascript:ContentClick('label237', 'label236');" onmouseover="ContentPreview('label237');" onmouseout="ContentUnpreview('label237');" title="click to collapse or expand..."> more... </a>
 <div id="label237" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_ctl</span> <b>(Alias name: ap-sniffer-ctl)</b>  Enable/disable sniffer on wifi control frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label238' href="javascript:ContentClick('label239', 'label238');" onmouseover="ContentPreview('label239');" onmouseout="ContentUnpreview('label239');" title="click to collapse or expand..."> more... </a>
 <div id="label239" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_data</span> <b>(Alias name: ap-sniffer-data)</b>  Enable/disable sniffer on wifi data frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label240' href="javascript:ContentClick('label241', 'label240');" onmouseover="ContentPreview('label241');" onmouseout="ContentUnpreview('label241');" title="click to collapse or expand..."> more... </a>
 <div id="label241" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_beacon</span> <b>(Alias name: ap-sniffer-mgmt-beacon)</b>  Enable/disable sniffer on wifi management beacon frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label242' href="javascript:ContentClick('label243', 'label242');" onmouseover="ContentPreview('label243');" onmouseout="ContentUnpreview('label243');" title="click to collapse or expand..."> more... </a>
 <div id="label243" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_other</span> <b>(Alias name: ap-sniffer-mgmt-other)</b>  Enable/disable sniffer on wifi management other frames  (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label244' href="javascript:ContentClick('label245', 'label244');" onmouseover="ContentPreview('label245');" onmouseout="ContentUnpreview('label245');" title="click to collapse or expand..."> more... </a>
 <div id="label245" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_probe</span> <b>(Alias name: ap-sniffer-mgmt-probe)</b>  Enable/disable sniffer on wifi management probe frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label246' href="javascript:ContentClick('label247', 'label246');" onmouseover="ContentPreview('label247');" onmouseout="ContentUnpreview('label247');" title="click to collapse or expand..."> more... </a>
 <div id="label247" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_high</span> <b>(Alias name: auto-power-high)</b>  The upper bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label248' href="javascript:ContentClick('label249', 'label248');" onmouseover="ContentPreview('label249');" onmouseout="ContentUnpreview('label249');" title="click to collapse or expand..."> more... </a>
 <div id="label249" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_level</span> <b>(Alias name: auto-power-level)</b>  Enable/disable automatic power-level adjustment to prevent co-channel interference (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label250' href="javascript:ContentClick('label251', 'label250');" onmouseover="ContentPreview('label251');" onmouseout="ContentUnpreview('label251');" title="click to collapse or expand..."> more... </a>
 <div id="label251" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_low</span> <b>(Alias name: auto-power-low)</b>  The lower bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label252' href="javascript:ContentClick('label253', 'label252');" onmouseover="ContentPreview('label253');" onmouseout="ContentUnpreview('label253');" title="click to collapse or expand..."> more... </a>
 <div id="label253" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_target</span> <b>(Alias name: auto-power-target)</b>  The target of automatic transmit power adjustment in dbm. <span class="li-normal">type: str</span>
 <a id='label254' href="javascript:ContentClick('label255', 'label254');" onmouseover="ContentPreview('label255');" onmouseout="ContentUnpreview('label255');" title="click to collapse or expand..."> more... </a>
 <div id="label255" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band</span> Wifi band that radio 1 operates on. <span class="li-normal">type: str</span> <span class="li-normal">choices: [802.11b, 802.11a, 802.11g, 802.11n, 802.11ac, 802.11n-5G, 802.11ax-5G, 802.11ax, 802.11ac-2G, 802.11g-only, 802.11n-only, 802.11n,g-only, 802.11ac-only, 802.11ac,n-only, 802.11n-5G-only, 802.11ax-5G-only, 802.11ax,ac-only, 802.11ax,ac,n-only, 802.11ax-only, 802.11ax,n-only, 802.11ax,n,g-only, 802.11ax-6G, 802.11n-2G, 802.11ac-5G, 802.11ax-2G, 802.11be-2G, 802.11be-5G, 802.11be-6G]</span> 
 <a id='label256' href="javascript:ContentClick('label257', 'label256');" onmouseover="ContentPreview('label257');" onmouseout="ContentUnpreview('label257');" title="click to collapse or expand..."> more... </a>
 <div id="label257" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band_5g_type</span> <b>(Alias name: band-5g-type)</b>  Wifi 5g band type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [5g-full, 5g-high, 5g-low]</span> 
 <a id='label258' href="javascript:ContentClick('label259', 'label258');" onmouseover="ContentPreview('label259');" onmouseout="ContentUnpreview('label259');" title="click to collapse or expand..."> more... </a>
 <div id="label259" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_admission_control</span> <b>(Alias name: bandwidth-admission-control)</b>  Enable/disable wifi multimedia (wmm) bandwidth admission control to optimize wifi bandwidth use. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label260' href="javascript:ContentClick('label261', 'label260');" onmouseover="ContentPreview('label261');" onmouseout="ContentUnpreview('label261');" title="click to collapse or expand..."> more... </a>
 <div id="label261" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_capacity</span> <b>(Alias name: bandwidth-capacity)</b>  Maximum bandwidth capacity allowed (1 - 600000 kbps, default = 2000). <span class="li-normal">type: int</span>
 <a id='label262' href="javascript:ContentClick('label263', 'label262');" onmouseover="ContentPreview('label263');" onmouseout="ContentUnpreview('label263');" title="click to collapse or expand..."> more... </a>
 <div id="label263" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">beacon_interval</span> <b>(Alias name: beacon-interval)</b>  Beacon interval. <span class="li-normal">type: int</span>
 <a id='label264' href="javascript:ContentClick('label265', 'label264');" onmouseover="ContentPreview('label265');" onmouseout="ContentUnpreview('label265');" title="click to collapse or expand..."> more... </a>
 <div id="label265" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color</span> <b>(Alias name: bss-color)</b>  Bss color value for this 11ax radio (0 - 63, 0 means disable. <span class="li-normal">type: int</span>
 <a id='label266' href="javascript:ContentClick('label267', 'label266');" onmouseover="ContentPreview('label267');" onmouseout="ContentUnpreview('label267');" title="click to collapse or expand..."> more... </a>
 <div id="label267" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_admission_control</span> <b>(Alias name: call-admission-control)</b>  Enable/disable wifi multimedia (wmm) call admission control to optimize wifi bandwidth use for voip calls. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label268' href="javascript:ContentClick('label269', 'label268');" onmouseover="ContentPreview('label269');" onmouseout="ContentUnpreview('label269');" title="click to collapse or expand..."> more... </a>
 <div id="label269" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_capacity</span> <b>(Alias name: call-capacity)</b>  Maximum number of voice over wlan (vowlan) phones supported by the radio (0 - 60, default = 10). <span class="li-normal">type: int</span>
 <a id='label270' href="javascript:ContentClick('label271', 'label270');" onmouseover="ContentPreview('label271');" onmouseout="ContentUnpreview('label271');" title="click to collapse or expand..."> more... </a>
 <div id="label271" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel</span> Selected list of wireless radio channels. <span class="li-normal">type: list</span>
 <a id='label272' href="javascript:ContentClick('label273', 'label272');" onmouseover="ContentPreview('label273');" onmouseout="ContentUnpreview('label273');" title="click to collapse or expand..."> more... </a>
 <div id="label273" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding</span> <b>(Alias name: channel-bonding)</b>  Channel bandwidth: 160,80, 40, or 20mhz. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, 80MHz, 40MHz, 20MHz, 160MHz, 320MHz, 240MHz]</span> 
 <a id='label274' href="javascript:ContentClick('label275', 'label274');" onmouseover="ContentPreview('label275');" onmouseout="ContentUnpreview('label275');" title="click to collapse or expand..."> more... </a>
 <div id="label275" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_utilization</span> <b>(Alias name: channel-utilization)</b>  Enable/disable measuring channel utilization. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label276' href="javascript:ContentClick('label277', 'label276');" onmouseover="ContentPreview('label277');" onmouseout="ContentUnpreview('label277');" title="click to collapse or expand..."> more... </a>
 <div id="label277" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">coexistence</span> Enable/disable allowing both ht20 and ht40 on the same radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label278' href="javascript:ContentClick('label279', 'label278');" onmouseover="ContentPreview('label279');" onmouseout="ContentUnpreview('label279');" title="click to collapse or expand..."> more... </a>
 <div id="label279" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">darrp</span> Enable/disable distributed automatic radio resource provisioning (darrp) to make sure the radio is always using the most optimal channel (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label280' href="javascript:ContentClick('label281', 'label280');" onmouseover="ContentPreview('label281');" onmouseout="ContentUnpreview('label281');" title="click to collapse or expand..."> more... </a>
 <div id="label281" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma</span> Enable/disable dynamic radio mode assignment (drma) (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label282' href="javascript:ContentClick('label283', 'label282');" onmouseover="ContentPreview('label283');" onmouseout="ContentUnpreview('label283');" title="click to collapse or expand..."> more... </a>
 <div id="label283" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma_sensitivity</span> <b>(Alias name: drma-sensitivity)</b>  Network coverage factor (ncf) percentage required to consider a radio as redundant (default = low). <span class="li-normal">type: str</span> <span class="li-normal">choices: [low, medium, high]</span> 
 <a id='label284' href="javascript:ContentClick('label285', 'label284');" onmouseover="ContentPreview('label285');" onmouseout="ContentUnpreview('label285');" title="click to collapse or expand..."> more... </a>
 <div id="label285" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dtim</span> Delivery traffic indication map (dtim) period (1 - 255, default = 1). <span class="li-normal">type: int</span>
 <a id='label286' href="javascript:ContentClick('label287', 'label286');" onmouseover="ContentPreview('label287');" onmouseout="ContentUnpreview('label287');" title="click to collapse or expand..."> more... </a>
 <div id="label287" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_threshold</span> <b>(Alias name: frag-threshold)</b>  Maximum packet size that can be sent without fragmentation (800 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label288' href="javascript:ContentClick('label289', 'label288');" onmouseover="ContentPreview('label289');" onmouseout="ContentUnpreview('label289');" title="click to collapse or expand..."> more... </a>
 <div id="label289" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_clients</span> <b>(Alias name: max-clients)</b>  Maximum number of stations (stas) or wifi clients supported by the radio. <span class="li-normal">type: int</span>
 <a id='label290' href="javascript:ContentClick('label291', 'label290');" onmouseover="ContentPreview('label291');" onmouseout="ContentUnpreview('label291');" title="click to collapse or expand..."> more... </a>
 <div id="label291" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_distance</span> <b>(Alias name: max-distance)</b>  Maximum expected distance between the ap and clients (0 - 54000 m, default = 0). <span class="li-normal">type: int</span>
 <a id='label292' href="javascript:ContentClick('label293', 'label292');" onmouseover="ContentPreview('label293');" onmouseout="ContentUnpreview('label293');" title="click to collapse or expand..."> more... </a>
 <div id="label293" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mode</span> Mode of radio 1. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disabled, ap, monitor, sniffer, sam]</span> 
 <a id='label294' href="javascript:ContentClick('label295', 'label294');" onmouseover="ContentPreview('label295');" onmouseout="ContentUnpreview('label295');" title="click to collapse or expand..."> more... </a>
 <div id="label295" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_level</span> <b>(Alias name: power-level)</b>  Radio power level as a percentage of the maximum transmit power (0 - 100, default = 100). <span class="li-normal">type: int</span>
 <a id='label296' href="javascript:ContentClick('label297', 'label296');" onmouseover="ContentPreview('label297');" onmouseout="ContentUnpreview('label297');" title="click to collapse or expand..."> more... </a>
 <div id="label297" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">powersave_optimize</span> <b>(Alias name: powersave-optimize)</b>  Enable client power-saving features such as tim, ac vo, and obss etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [tim, ac-vo, no-obss-scan, no-11b-rate, client-rate-follow]</span> 
 <a id='label298' href="javascript:ContentClick('label299', 'label298');" onmouseover="ContentPreview('label299');" onmouseout="ContentUnpreview('label299');" title="click to collapse or expand..."> more... </a>
 <div id="label299" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protection_mode</span> <b>(Alias name: protection-mode)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [rtscts, ctsonly, disable]</span> 
 <a id='label300' href="javascript:ContentClick('label301', 'label300');" onmouseover="ContentPreview('label301');" onmouseout="ContentUnpreview('label301');" title="click to collapse or expand..."> more... </a>
 <div id="label301" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">radio_id</span> <b>(Alias name: radio-id)</b>  Radio id. <span class="li-normal">type: int</span>
 <a id='label302' href="javascript:ContentClick('label303', 'label302');" onmouseover="ContentPreview('label303');" onmouseout="ContentUnpreview('label303');" title="click to collapse or expand..."> more... </a>
 <div id="label303" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rts_threshold</span> <b>(Alias name: rts-threshold)</b>  Maximum packet size for rts transmissions, specifying the maximum size of a data packet before rts/cts (256 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label304' href="javascript:ContentClick('label305', 'label304');" onmouseover="ContentPreview('label305');" onmouseout="ContentUnpreview('label305');" title="click to collapse or expand..."> more... </a>
 <div id="label305" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">short_guard_interval</span> <b>(Alias name: short-guard-interval)</b>  Use either the short guard interval (short gi) of 400 ns or the long guard interval (long gi) of 800 ns. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label306' href="javascript:ContentClick('label307', 'label306');" onmouseover="ContentPreview('label307');" onmouseout="ContentUnpreview('label307');" title="click to collapse or expand..."> more... </a>
 <div id="label307" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">spectrum_analysis</span> <b>(Alias name: spectrum-analysis)</b>  Enable/disable spectrum analysis to find interference that would negatively impact wireless performance. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, scan-only]</span> 
 <a id='label308' href="javascript:ContentClick('label309', 'label308');" onmouseover="ContentPreview('label309');" onmouseout="ContentUnpreview('label309');" title="click to collapse or expand..."> more... </a>
 <div id="label309" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">transmit_optimize</span> <b>(Alias name: transmit-optimize)</b>  Packet transmission optimization options including power saving, aggregation limiting, retry limiting, etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [disable, power-save, aggr-limit, retry-limit, send-bar]</span> 
 <a id='label310' href="javascript:ContentClick('label311', 'label310');" onmouseover="ContentPreview('label311');" onmouseout="ContentUnpreview('label311');" title="click to collapse or expand..."> more... </a>
 <div id="label311" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap_all</span> <b>(Alias name: vap-all)</b>  Configure method for assigning ssids to this fortiap (default = automatically assign tunnel ssids). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, tunnel, bridge, manual]</span> 
 <a id='label312' href="javascript:ContentClick('label313', 'label312');" onmouseover="ContentPreview('label313');" onmouseout="ContentUnpreview('label313');" title="click to collapse or expand..."> more... </a>
 <div id="label313" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap1</span> Virtual access point (vap) for wlan id 1 <span class="li-normal">type: str</span>
 <a id='label314' href="javascript:ContentClick('label315', 'label314');" onmouseover="ContentPreview('label315');" onmouseout="ContentUnpreview('label315');" title="click to collapse or expand..."> more... </a>
 <div id="label315" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap2</span> Virtual access point (vap) for wlan id 2 <span class="li-normal">type: str</span>
 <a id='label316' href="javascript:ContentClick('label317', 'label316');" onmouseover="ContentPreview('label317');" onmouseout="ContentUnpreview('label317');" title="click to collapse or expand..."> more... </a>
 <div id="label317" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap3</span> Virtual access point (vap) for wlan id 3 <span class="li-normal">type: str</span>
 <a id='label318' href="javascript:ContentClick('label319', 'label318');" onmouseover="ContentPreview('label319');" onmouseout="ContentUnpreview('label319');" title="click to collapse or expand..."> more... </a>
 <div id="label319" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap4</span> Virtual access point (vap) for wlan id 4 <span class="li-normal">type: str</span>
 <a id='label320' href="javascript:ContentClick('label321', 'label320');" onmouseover="ContentPreview('label321');" onmouseout="ContentUnpreview('label321');" title="click to collapse or expand..."> more... </a>
 <div id="label321" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap5</span> Virtual access point (vap) for wlan id 5 <span class="li-normal">type: str</span>
 <a id='label322' href="javascript:ContentClick('label323', 'label322');" onmouseover="ContentPreview('label323');" onmouseout="ContentUnpreview('label323');" title="click to collapse or expand..."> more... </a>
 <div id="label323" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap6</span> Virtual access point (vap) for wlan id 6 <span class="li-normal">type: str</span>
 <a id='label324' href="javascript:ContentClick('label325', 'label324');" onmouseover="ContentPreview('label325');" onmouseout="ContentUnpreview('label325');" title="click to collapse or expand..."> more... </a>
 <div id="label325" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap7</span> Virtual access point (vap) for wlan id 7 <span class="li-normal">type: str</span>
 <a id='label326' href="javascript:ContentClick('label327', 'label326');" onmouseover="ContentPreview('label327');" onmouseout="ContentUnpreview('label327');" title="click to collapse or expand..."> more... </a>
 <div id="label327" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap8</span> Virtual access point (vap) for wlan id 8 <span class="li-normal">type: str</span>
 <a id='label328' href="javascript:ContentClick('label329', 'label328');" onmouseover="ContentPreview('label329');" onmouseout="ContentUnpreview('label329');" title="click to collapse or expand..."> more... </a>
 <div id="label329" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vaps</span> Manually selected list of virtual access points (vaps). <span class="li-normal">type: list or str</span>
 <a id='label330' href="javascript:ContentClick('label331', 'label330');" onmouseover="ContentPreview('label331');" onmouseout="ContentUnpreview('label331');" title="click to collapse or expand..."> more... </a>
 <div id="label331" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wids_profile</span> <b>(Alias name: wids-profile)</b>  Wireless intrusion detection system (wids) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label332' href="javascript:ContentClick('label333', 'label332');" onmouseover="ContentPreview('label333');" onmouseout="ContentUnpreview('label333');" title="click to collapse or expand..."> more... </a>
 <div id="label333" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">zero_wait_dfs</span> <b>(Alias name: zero-wait-dfs)</b>  Enable/disable zero wait dfs on radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label334' href="javascript:ContentClick('label335', 'label334');" onmouseover="ContentPreview('label335');" onmouseout="ContentUnpreview('label335');" title="click to collapse or expand..."> more... </a>
 <div id="label335" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frequency_handoff</span> <b>(Alias name: frequency-handoff)</b>  Enable/disable frequency handoff of clients to other channels (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label336' href="javascript:ContentClick('label337', 'label336');" onmouseover="ContentPreview('label337');" onmouseout="ContentUnpreview('label337');" title="click to collapse or expand..."> more... </a>
 <div id="label337" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_handoff</span> <b>(Alias name: ap-handoff)</b>  Enable/disable ap handoff of clients to other aps (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label338' href="javascript:ContentClick('label339', 'label338');" onmouseover="ContentPreview('label339');" onmouseout="ContentUnpreview('label339');" title="click to collapse or expand..."> more... </a>
 <div id="label339" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_protocol</span> <b>(Alias name: iperf-protocol)</b>  Iperf test protocol (default = udp). <span class="li-normal">type: str</span> <span class="li-normal">choices: [udp, tcp]</span> 
 <a id='label340' href="javascript:ContentClick('label341', 'label340');" onmouseover="ContentPreview('label341');" onmouseout="ContentUnpreview('label341');" title="click to collapse or expand..."> more... </a>
 <div id="label341" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_server_port</span> <b>(Alias name: iperf-server-port)</b>  Iperf service port number. <span class="li-normal">type: int</span>
 <a id='label342' href="javascript:ContentClick('label343', 'label342');" onmouseover="ContentPreview('label343');" onmouseout="ContentUnpreview('label343');" title="click to collapse or expand..."> more... </a>
 <div id="label343" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_mode</span> <b>(Alias name: power-mode)</b>  Set radio effective isotropic radiated power (eirp) in dbm or by a percentage of the maximum eirp (default = percentage). <span class="li-normal">type: str</span> <span class="li-normal">choices: [dBm, percentage]</span> 
 <a id='label344' href="javascript:ContentClick('label345', 'label344');" onmouseover="ContentPreview('label345');" onmouseout="ContentUnpreview('label345');" title="click to collapse or expand..."> more... </a>
 <div id="label345" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_value</span> <b>(Alias name: power-value)</b>  Radio eirp power in dbm (1 - 33, default = 27). <span class="li-normal">type: int</span>
 <a id='label346' href="javascript:ContentClick('label347', 'label346');" onmouseover="ContentPreview('label347');" onmouseout="ContentUnpreview('label347');" title="click to collapse or expand..."> more... </a>
 <div id="label347" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_bssid</span> <b>(Alias name: sam-bssid)</b>  Bssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label348' href="javascript:ContentClick('label349', 'label348');" onmouseover="ContentPreview('label349');" onmouseout="ContentUnpreview('label349');" title="click to collapse or expand..."> more... </a>
 <div id="label349" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_captive_portal</span> <b>(Alias name: sam-captive-portal)</b>  Enable/disable captive portal authentication (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label350' href="javascript:ContentClick('label351', 'label350');" onmouseover="ContentPreview('label351');" onmouseout="ContentUnpreview('label351');" title="click to collapse or expand..."> more... </a>
 <div id="label351" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_password</span> <b>(Alias name: sam-password)</b>  Passphrase for wifi network connection. <span class="li-normal">type: list</span>
 <a id='label352' href="javascript:ContentClick('label353', 'label352');" onmouseover="ContentPreview('label353');" onmouseout="ContentUnpreview('label353');" title="click to collapse or expand..."> more... </a>
 <div id="label353" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_report_intv</span> <b>(Alias name: sam-report-intv)</b>  Sam report interval (sec), 0 for a one-time report. <span class="li-normal">type: int</span>
 <a id='label354' href="javascript:ContentClick('label355', 'label354');" onmouseover="ContentPreview('label355');" onmouseout="ContentUnpreview('label355');" title="click to collapse or expand..."> more... </a>
 <div id="label355" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_security_type</span> <b>(Alias name: sam-security-type)</b>  Select wifi network security type (default = wpa-personal). <span class="li-normal">type: str</span> <span class="li-normal">choices: [open, wpa-personal, wpa-enterprise, owe, wpa3-sae]</span> 
 <a id='label356' href="javascript:ContentClick('label357', 'label356');" onmouseover="ContentPreview('label357');" onmouseout="ContentUnpreview('label357');" title="click to collapse or expand..."> more... </a>
 <div id="label357" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server</span> <b>(Alias name: sam-server)</b>  Sam test server ip address or domain name. <span class="li-normal">type: str</span>
 <a id='label358' href="javascript:ContentClick('label359', 'label358');" onmouseover="ContentPreview('label359');" onmouseout="ContentUnpreview('label359');" title="click to collapse or expand..."> more... </a>
 <div id="label359" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ssid</span> <b>(Alias name: sam-ssid)</b>  Ssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label360' href="javascript:ContentClick('label361', 'label360');" onmouseover="ContentPreview('label361');" onmouseout="ContentUnpreview('label361');" title="click to collapse or expand..."> more... </a>
 <div id="label361" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_test</span> <b>(Alias name: sam-test)</b>  Select sam test type (default = ping). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ping, iperf]</span> 
 <a id='label362' href="javascript:ContentClick('label363', 'label362');" onmouseover="ContentPreview('label363');" onmouseout="ContentUnpreview('label363');" title="click to collapse or expand..."> more... </a>
 <div id="label363" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_username</span> <b>(Alias name: sam-username)</b>  Username for wifi network connection. <span class="li-normal">type: str</span>
 <a id='label364' href="javascript:ContentClick('label365', 'label364');" onmouseover="ContentPreview('label365');" onmouseout="ContentUnpreview('label365');" title="click to collapse or expand..."> more... </a>
 <div id="label365" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">arrp_profile</span> <b>(Alias name: arrp-profile)</b>  Distributed automatic radio resource provisioning (darrp) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label366' href="javascript:ContentClick('label367', 'label366');" onmouseover="ContentPreview('label367');" onmouseout="ContentUnpreview('label367');" title="click to collapse or expand..."> more... </a>
 <div id="label367" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color_mode</span> <b>(Alias name: bss-color-mode)</b>  Bss color mode for this 11ax radio (default = auto). <span class="li-normal">type: str</span> <span class="li-normal">choices: [auto, static]</span> 
 <a id='label368' href="javascript:ContentClick('label369', 'label368');" onmouseover="ContentPreview('label369');" onmouseout="ContentUnpreview('label369');" title="click to collapse or expand..."> more... </a>
 <div id="label369" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_failure_string</span> <b>(Alias name: sam-cwp-failure-string)</b>  Failure identification on the page after an incorrect login. <span class="li-normal">type: str</span>
 <a id='label370' href="javascript:ContentClick('label371', 'label370');" onmouseover="ContentPreview('label371');" onmouseout="ContentUnpreview('label371');" title="click to collapse or expand..."> more... </a>
 <div id="label371" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_match_string</span> <b>(Alias name: sam-cwp-match-string)</b>  Identification string from the captive portal login form. <span class="li-normal">type: str</span>
 <a id='label372' href="javascript:ContentClick('label373', 'label372');" onmouseover="ContentPreview('label373');" onmouseout="ContentUnpreview('label373');" title="click to collapse or expand..."> more... </a>
 <div id="label373" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_password</span> <b>(Alias name: sam-cwp-password)</b>  Password for captive portal authentication. <span class="li-normal">type: list</span>
 <a id='label374' href="javascript:ContentClick('label375', 'label374');" onmouseover="ContentPreview('label375');" onmouseout="ContentUnpreview('label375');" title="click to collapse or expand..."> more... </a>
 <div id="label375" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_success_string</span> <b>(Alias name: sam-cwp-success-string)</b>  Success identification on the page after a successful login. <span class="li-normal">type: str</span>
 <a id='label376' href="javascript:ContentClick('label377', 'label376');" onmouseover="ContentPreview('label377');" onmouseout="ContentUnpreview('label377');" title="click to collapse or expand..."> more... </a>
 <div id="label377" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_test_url</span> <b>(Alias name: sam-cwp-test-url)</b>  Website the client is trying to access. <span class="li-normal">type: str</span>
 <a id='label378' href="javascript:ContentClick('label379', 'label378');" onmouseover="ContentPreview('label379');" onmouseout="ContentUnpreview('label379');" title="click to collapse or expand..."> more... </a>
 <div id="label379" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_username</span> <b>(Alias name: sam-cwp-username)</b>  Username for captive portal authentication. <span class="li-normal">type: str</span>
 <a id='label380' href="javascript:ContentClick('label381', 'label380');" onmouseover="ContentPreview('label381');" onmouseout="ContentUnpreview('label381');" title="click to collapse or expand..."> more... </a>
 <div id="label381" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_fqdn</span> <b>(Alias name: sam-server-fqdn)</b>  Sam test server domain name. <span class="li-normal">type: str</span>
 <a id='label382' href="javascript:ContentClick('label383', 'label382');" onmouseover="ContentPreview('label383');" onmouseout="ContentUnpreview('label383');" title="click to collapse or expand..."> more... </a>
 <div id="label383" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_ip</span> <b>(Alias name: sam-server-ip)</b>  Sam test server ip address. <span class="li-normal">type: str</span>
 <a id='label384' href="javascript:ContentClick('label385', 'label384');" onmouseover="ContentPreview('label385');" onmouseout="ContentUnpreview('label385');" title="click to collapse or expand..."> more... </a>
 <div id="label385" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_type</span> <b>(Alias name: sam-server-type)</b>  Select sam server type (default = ip). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ip, fqdn]</span> 
 <a id='label386' href="javascript:ContentClick('label387', 'label386');" onmouseover="ContentPreview('label387');" onmouseout="ContentUnpreview('label387');" title="click to collapse or expand..."> more... </a>
 <div id="label387" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211d</span> <b>(Alias name: 80211d)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label388' href="javascript:ContentClick('label389', 'label388');" onmouseover="ContentPreview('label389');" onmouseout="ContentUnpreview('label389');" title="click to collapse or expand..."> more... </a>
 <div id="label389" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna</span> <b>(Alias name: optional-antenna)</b>  Optional antenna used on fap (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, FANT-04ABGN-8065-P-N, FANT-04ABGN-0606-O-R, FANT-04ABGN-0606-P-R, FANT-10ACAX-1213-D-N, FANT-08ABGN-1213-D-R, custom]</span> 
 <a id='label390' href="javascript:ContentClick('label391', 'label390');" onmouseover="ContentPreview('label391');" onmouseout="ContentUnpreview('label391');" title="click to collapse or expand..."> more... </a>
 <div id="label391" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mimo_mode</span> <b>(Alias name: mimo-mode)</b>  Configure radio mimo mode (default = default). <span class="li-normal">type: str</span> <span class="li-normal">choices: [default, 1x1, 2x2, 3x3, 4x4, 8x8]</span> 
 <a id='label392' href="javascript:ContentClick('label393', 'label392');" onmouseover="ContentPreview('label393');" onmouseout="ContentUnpreview('label393');" title="click to collapse or expand..."> more... </a>
 <div id="label393" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna_gain</span> <b>(Alias name: optional-antenna-gain)</b>  Optional antenna gain in dbi (0 to 20, default = 0). <span class="li-normal">type: str</span>
 <a id='label394' href="javascript:ContentClick('label395', 'label394');" onmouseover="ContentPreview('label395');" onmouseout="ContentUnpreview('label395');" title="click to collapse or expand..."> more... </a>
 <div id="label395" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ca_certificate</span> <b>(Alias name: sam-ca-certificate)</b>  Ca certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label396' href="javascript:ContentClick('label397', 'label396');" onmouseover="ContentPreview('label397');" onmouseout="ContentUnpreview('label397');" title="click to collapse or expand..."> more... </a>
 <div id="label397" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_client_certificate</span> <b>(Alias name: sam-client-certificate)</b>  Client certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label398' href="javascript:ContentClick('label399', 'label398');" onmouseover="ContentPreview('label399');" onmouseout="ContentUnpreview('label399');" title="click to collapse or expand..."> more... </a>
 <div id="label399" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_eap_method</span> <b>(Alias name: sam-eap-method)</b>  Select wpa2/wpa3-enterprise eap method (default = peap). <span class="li-normal">type: str</span> <span class="li-normal">choices: [tls, peap, both]</span> 
 <a id='label400' href="javascript:ContentClick('label401', 'label400');" onmouseover="ContentPreview('label401');" onmouseout="ContentUnpreview('label401');" title="click to collapse or expand..."> more... </a>
 <div id="label401" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key</span> <b>(Alias name: sam-private-key)</b>  Private key for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label402' href="javascript:ContentClick('label403', 'label402');" onmouseover="ContentPreview('label403');" onmouseout="ContentUnpreview('label403');" title="click to collapse or expand..."> more... </a>
 <div id="label403" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key_password</span> <b>(Alias name: sam-private-key-password)</b>  Password for private key file for wpa2/wpa3-enterprise. <span class="li-normal">type: list</span>
 <a id='label404' href="javascript:ContentClick('label405', 'label404');" onmouseover="ContentPreview('label405');" onmouseout="ContentUnpreview('label405');" title="click to collapse or expand..."> more... </a>
 <div id="label405" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding_ext</span> <b>(Alias name: channel-bonding-ext)</b>  Channel bandwidth extension: 320 mhz-1 and 320 mhz-2 (default = 320 mhz-2). <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz-1, 320MHz-2]</span> 
 <a id='label406' href="javascript:ContentClick('label407', 'label406');" onmouseover="ContentPreview('label407');" onmouseout="ContentUnpreview('label407');" title="click to collapse or expand..."> more... </a>
 <div id="label407" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211mc</span> <b>(Alias name: 80211mc)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label408' href="javascript:ContentClick('label409', 'label408');" onmouseover="ContentPreview('label409');" onmouseout="ContentUnpreview('label409');" title="click to collapse or expand..."> more... </a>
 <div id="label409" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan_width</span> <b>(Alias name: ap-sniffer-chan-width)</b>  Channel bandwidth for sniffer. <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz, 240MHz, 160MHz, 80MHz, 40MHz, 20MHz]</span> 
 <a id='label410' href="javascript:ContentClick('label411', 'label410');" onmouseover="ContentPreview('label411');" onmouseout="ContentUnpreview('label411');" title="click to collapse or expand..."> more... </a>
 <div id="label411" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">radio_2</span> <b>(Alias name: radio-2)</b>  Radio 2. <span class="li-normal">type: dict</span>
 <a id='label412' href="javascript:ContentClick('label413', 'label412');" onmouseover="ContentPreview('label413');" onmouseout="ContentUnpreview('label413');" title="click to collapse or expand..."> more... </a>
 <div id="label413" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">airtime_fairness</span> <b>(Alias name: airtime-fairness)</b>  Enable/disable airtime fairness (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label414' href="javascript:ContentClick('label415', 'label414');" onmouseover="ContentPreview('label415');" onmouseout="ContentUnpreview('label415');" title="click to collapse or expand..."> more... </a>
 <div id="label415" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">amsdu</span> Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label416' href="javascript:ContentClick('label417', 'label416');" onmouseover="ContentPreview('label417');" onmouseout="ContentUnpreview('label417');" title="click to collapse or expand..."> more... </a>
 <div id="label417" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_addr</span> <b>(Alias name: ap-sniffer-addr)</b>  Mac address to monitor. <span class="li-normal">type: str</span>
 <a id='label418' href="javascript:ContentClick('label419', 'label418');" onmouseover="ContentPreview('label419');" onmouseout="ContentUnpreview('label419');" title="click to collapse or expand..."> more... </a>
 <div id="label419" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_bufsize</span> <b>(Alias name: ap-sniffer-bufsize)</b>  Sniffer buffer size (1 - 32 mb, default = 16). <span class="li-normal">type: int</span>
 <a id='label420' href="javascript:ContentClick('label421', 'label420');" onmouseover="ContentPreview('label421');" onmouseout="ContentUnpreview('label421');" title="click to collapse or expand..."> more... </a>
 <div id="label421" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan</span> <b>(Alias name: ap-sniffer-chan)</b>  Channel on which to operate the sniffer (default = 6). <span class="li-normal">type: int</span>
 <a id='label422' href="javascript:ContentClick('label423', 'label422');" onmouseover="ContentPreview('label423');" onmouseout="ContentUnpreview('label423');" title="click to collapse or expand..."> more... </a>
 <div id="label423" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_ctl</span> <b>(Alias name: ap-sniffer-ctl)</b>  Enable/disable sniffer on wifi control frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label424' href="javascript:ContentClick('label425', 'label424');" onmouseover="ContentPreview('label425');" onmouseout="ContentUnpreview('label425');" title="click to collapse or expand..."> more... </a>
 <div id="label425" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_data</span> <b>(Alias name: ap-sniffer-data)</b>  Enable/disable sniffer on wifi data frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label426' href="javascript:ContentClick('label427', 'label426');" onmouseover="ContentPreview('label427');" onmouseout="ContentUnpreview('label427');" title="click to collapse or expand..."> more... </a>
 <div id="label427" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_beacon</span> <b>(Alias name: ap-sniffer-mgmt-beacon)</b>  Enable/disable sniffer on wifi management beacon frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label428' href="javascript:ContentClick('label429', 'label428');" onmouseover="ContentPreview('label429');" onmouseout="ContentUnpreview('label429');" title="click to collapse or expand..."> more... </a>
 <div id="label429" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_other</span> <b>(Alias name: ap-sniffer-mgmt-other)</b>  Enable/disable sniffer on wifi management other frames  (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label430' href="javascript:ContentClick('label431', 'label430');" onmouseover="ContentPreview('label431');" onmouseout="ContentUnpreview('label431');" title="click to collapse or expand..."> more... </a>
 <div id="label431" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_probe</span> <b>(Alias name: ap-sniffer-mgmt-probe)</b>  Enable/disable sniffer on wifi management probe frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label432' href="javascript:ContentClick('label433', 'label432');" onmouseover="ContentPreview('label433');" onmouseout="ContentUnpreview('label433');" title="click to collapse or expand..."> more... </a>
 <div id="label433" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_high</span> <b>(Alias name: auto-power-high)</b>  The upper bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label434' href="javascript:ContentClick('label435', 'label434');" onmouseover="ContentPreview('label435');" onmouseout="ContentUnpreview('label435');" title="click to collapse or expand..."> more... </a>
 <div id="label435" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_level</span> <b>(Alias name: auto-power-level)</b>  Enable/disable automatic power-level adjustment to prevent co-channel interference (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label436' href="javascript:ContentClick('label437', 'label436');" onmouseover="ContentPreview('label437');" onmouseout="ContentUnpreview('label437');" title="click to collapse or expand..."> more... </a>
 <div id="label437" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_low</span> <b>(Alias name: auto-power-low)</b>  The lower bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label438' href="javascript:ContentClick('label439', 'label438');" onmouseover="ContentPreview('label439');" onmouseout="ContentUnpreview('label439');" title="click to collapse or expand..."> more... </a>
 <div id="label439" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_target</span> <b>(Alias name: auto-power-target)</b>  The target of automatic transmit power adjustment in dbm. <span class="li-normal">type: str</span>
 <a id='label440' href="javascript:ContentClick('label441', 'label440');" onmouseover="ContentPreview('label441');" onmouseout="ContentUnpreview('label441');" title="click to collapse or expand..."> more... </a>
 <div id="label441" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band</span> Wifi band that radio 2 operates on. <span class="li-normal">type: str</span> <span class="li-normal">choices: [802.11b, 802.11a, 802.11g, 802.11n, 802.11ac, 802.11n-5G, 802.11ax-5G, 802.11ax, 802.11ac-2G, 802.11g-only, 802.11n-only, 802.11n,g-only, 802.11ac-only, 802.11ac,n-only, 802.11n-5G-only, 802.11ax-5G-only, 802.11ax,ac-only, 802.11ax,ac,n-only, 802.11ax-only, 802.11ax,n-only, 802.11ax,n,g-only, 802.11ax-6G, 802.11n-2G, 802.11ac-5G, 802.11ax-2G, 802.11be-2G, 802.11be-5G, 802.11be-6G]</span> 
 <a id='label442' href="javascript:ContentClick('label443', 'label442');" onmouseover="ContentPreview('label443');" onmouseout="ContentUnpreview('label443');" title="click to collapse or expand..."> more... </a>
 <div id="label443" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band_5g_type</span> <b>(Alias name: band-5g-type)</b>  Wifi 5g band type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [5g-full, 5g-high, 5g-low]</span> 
 <a id='label444' href="javascript:ContentClick('label445', 'label444');" onmouseover="ContentPreview('label445');" onmouseout="ContentUnpreview('label445');" title="click to collapse or expand..."> more... </a>
 <div id="label445" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_admission_control</span> <b>(Alias name: bandwidth-admission-control)</b>  Enable/disable wifi multimedia (wmm) bandwidth admission control to optimize wifi bandwidth use. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label446' href="javascript:ContentClick('label447', 'label446');" onmouseover="ContentPreview('label447');" onmouseout="ContentUnpreview('label447');" title="click to collapse or expand..."> more... </a>
 <div id="label447" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_capacity</span> <b>(Alias name: bandwidth-capacity)</b>  Maximum bandwidth capacity allowed (1 - 600000 kbps, default = 2000). <span class="li-normal">type: int</span>
 <a id='label448' href="javascript:ContentClick('label449', 'label448');" onmouseover="ContentPreview('label449');" onmouseout="ContentUnpreview('label449');" title="click to collapse or expand..."> more... </a>
 <div id="label449" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">beacon_interval</span> <b>(Alias name: beacon-interval)</b>  Beacon interval. <span class="li-normal">type: int</span>
 <a id='label450' href="javascript:ContentClick('label451', 'label450');" onmouseover="ContentPreview('label451');" onmouseout="ContentUnpreview('label451');" title="click to collapse or expand..."> more... </a>
 <div id="label451" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color</span> <b>(Alias name: bss-color)</b>  Bss color value for this 11ax radio (0 - 63, 0 means disable. <span class="li-normal">type: int</span>
 <a id='label452' href="javascript:ContentClick('label453', 'label452');" onmouseover="ContentPreview('label453');" onmouseout="ContentUnpreview('label453');" title="click to collapse or expand..."> more... </a>
 <div id="label453" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_admission_control</span> <b>(Alias name: call-admission-control)</b>  Enable/disable wifi multimedia (wmm) call admission control to optimize wifi bandwidth use for voip calls. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label454' href="javascript:ContentClick('label455', 'label454');" onmouseover="ContentPreview('label455');" onmouseout="ContentUnpreview('label455');" title="click to collapse or expand..."> more... </a>
 <div id="label455" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_capacity</span> <b>(Alias name: call-capacity)</b>  Maximum number of voice over wlan (vowlan) phones supported by the radio (0 - 60, default = 10). <span class="li-normal">type: int</span>
 <a id='label456' href="javascript:ContentClick('label457', 'label456');" onmouseover="ContentPreview('label457');" onmouseout="ContentUnpreview('label457');" title="click to collapse or expand..."> more... </a>
 <div id="label457" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel</span> Selected list of wireless radio channels. <span class="li-normal">type: list</span>
 <a id='label458' href="javascript:ContentClick('label459', 'label458');" onmouseover="ContentPreview('label459');" onmouseout="ContentUnpreview('label459');" title="click to collapse or expand..."> more... </a>
 <div id="label459" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding</span> <b>(Alias name: channel-bonding)</b>  Channel bandwidth: 160,80, 40, or 20mhz. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, 80MHz, 40MHz, 20MHz, 160MHz, 320MHz, 240MHz]</span> 
 <a id='label460' href="javascript:ContentClick('label461', 'label460');" onmouseover="ContentPreview('label461');" onmouseout="ContentUnpreview('label461');" title="click to collapse or expand..."> more... </a>
 <div id="label461" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_utilization</span> <b>(Alias name: channel-utilization)</b>  Enable/disable measuring channel utilization. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label462' href="javascript:ContentClick('label463', 'label462');" onmouseover="ContentPreview('label463');" onmouseout="ContentUnpreview('label463');" title="click to collapse or expand..."> more... </a>
 <div id="label463" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">coexistence</span> Enable/disable allowing both ht20 and ht40 on the same radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label464' href="javascript:ContentClick('label465', 'label464');" onmouseover="ContentPreview('label465');" onmouseout="ContentUnpreview('label465');" title="click to collapse or expand..."> more... </a>
 <div id="label465" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">darrp</span> Enable/disable distributed automatic radio resource provisioning (darrp) to make sure the radio is always using the most optimal channel (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label466' href="javascript:ContentClick('label467', 'label466');" onmouseover="ContentPreview('label467');" onmouseout="ContentUnpreview('label467');" title="click to collapse or expand..."> more... </a>
 <div id="label467" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma</span> Enable/disable dynamic radio mode assignment (drma) (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label468' href="javascript:ContentClick('label469', 'label468');" onmouseover="ContentPreview('label469');" onmouseout="ContentUnpreview('label469');" title="click to collapse or expand..."> more... </a>
 <div id="label469" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma_sensitivity</span> <b>(Alias name: drma-sensitivity)</b>  Network coverage factor (ncf) percentage required to consider a radio as redundant (default = low). <span class="li-normal">type: str</span> <span class="li-normal">choices: [low, medium, high]</span> 
 <a id='label470' href="javascript:ContentClick('label471', 'label470');" onmouseover="ContentPreview('label471');" onmouseout="ContentUnpreview('label471');" title="click to collapse or expand..."> more... </a>
 <div id="label471" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dtim</span> Delivery traffic indication map (dtim) period (1 - 255, default = 1). <span class="li-normal">type: int</span>
 <a id='label472' href="javascript:ContentClick('label473', 'label472');" onmouseover="ContentPreview('label473');" onmouseout="ContentUnpreview('label473');" title="click to collapse or expand..."> more... </a>
 <div id="label473" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_threshold</span> <b>(Alias name: frag-threshold)</b>  Maximum packet size that can be sent without fragmentation (800 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label474' href="javascript:ContentClick('label475', 'label474');" onmouseover="ContentPreview('label475');" onmouseout="ContentUnpreview('label475');" title="click to collapse or expand..."> more... </a>
 <div id="label475" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_clients</span> <b>(Alias name: max-clients)</b>  Maximum number of stations (stas) or wifi clients supported by the radio. <span class="li-normal">type: int</span>
 <a id='label476' href="javascript:ContentClick('label477', 'label476');" onmouseover="ContentPreview('label477');" onmouseout="ContentUnpreview('label477');" title="click to collapse or expand..."> more... </a>
 <div id="label477" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_distance</span> <b>(Alias name: max-distance)</b>  Maximum expected distance between the ap and clients (0 - 54000 m, default = 0). <span class="li-normal">type: int</span>
 <a id='label478' href="javascript:ContentClick('label479', 'label478');" onmouseover="ContentPreview('label479');" onmouseout="ContentUnpreview('label479');" title="click to collapse or expand..."> more... </a>
 <div id="label479" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mode</span> Mode of radio 2. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disabled, ap, monitor, sniffer, sam]</span> 
 <a id='label480' href="javascript:ContentClick('label481', 'label480');" onmouseover="ContentPreview('label481');" onmouseout="ContentUnpreview('label481');" title="click to collapse or expand..."> more... </a>
 <div id="label481" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_level</span> <b>(Alias name: power-level)</b>  Radio power level as a percentage of the maximum transmit power (0 - 100, default = 100). <span class="li-normal">type: int</span>
 <a id='label482' href="javascript:ContentClick('label483', 'label482');" onmouseover="ContentPreview('label483');" onmouseout="ContentUnpreview('label483');" title="click to collapse or expand..."> more... </a>
 <div id="label483" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">powersave_optimize</span> <b>(Alias name: powersave-optimize)</b>  Enable client power-saving features such as tim, ac vo, and obss etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [tim, ac-vo, no-obss-scan, no-11b-rate, client-rate-follow]</span> 
 <a id='label484' href="javascript:ContentClick('label485', 'label484');" onmouseover="ContentPreview('label485');" onmouseout="ContentUnpreview('label485');" title="click to collapse or expand..."> more... </a>
 <div id="label485" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protection_mode</span> <b>(Alias name: protection-mode)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [rtscts, ctsonly, disable]</span> 
 <a id='label486' href="javascript:ContentClick('label487', 'label486');" onmouseover="ContentPreview('label487');" onmouseout="ContentUnpreview('label487');" title="click to collapse or expand..."> more... </a>
 <div id="label487" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">radio_id</span> <b>(Alias name: radio-id)</b>  Radio id. <span class="li-normal">type: int</span>
 <a id='label488' href="javascript:ContentClick('label489', 'label488');" onmouseover="ContentPreview('label489');" onmouseout="ContentUnpreview('label489');" title="click to collapse or expand..."> more... </a>
 <div id="label489" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rts_threshold</span> <b>(Alias name: rts-threshold)</b>  Maximum packet size for rts transmissions, specifying the maximum size of a data packet before rts/cts (256 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label490' href="javascript:ContentClick('label491', 'label490');" onmouseover="ContentPreview('label491');" onmouseout="ContentUnpreview('label491');" title="click to collapse or expand..."> more... </a>
 <div id="label491" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">short_guard_interval</span> <b>(Alias name: short-guard-interval)</b>  Use either the short guard interval (short gi) of 400 ns or the long guard interval (long gi) of 800 ns. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label492' href="javascript:ContentClick('label493', 'label492');" onmouseover="ContentPreview('label493');" onmouseout="ContentUnpreview('label493');" title="click to collapse or expand..."> more... </a>
 <div id="label493" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">spectrum_analysis</span> <b>(Alias name: spectrum-analysis)</b>  Enable/disable spectrum analysis to find interference that would negatively impact wireless performance. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, scan-only]</span> 
 <a id='label494' href="javascript:ContentClick('label495', 'label494');" onmouseover="ContentPreview('label495');" onmouseout="ContentUnpreview('label495');" title="click to collapse or expand..."> more... </a>
 <div id="label495" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">transmit_optimize</span> <b>(Alias name: transmit-optimize)</b>  Packet transmission optimization options including power saving, aggregation limiting, retry limiting, etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [disable, power-save, aggr-limit, retry-limit, send-bar]</span> 
 <a id='label496' href="javascript:ContentClick('label497', 'label496');" onmouseover="ContentPreview('label497');" onmouseout="ContentUnpreview('label497');" title="click to collapse or expand..."> more... </a>
 <div id="label497" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap_all</span> <b>(Alias name: vap-all)</b>  Configure method for assigning ssids to this fortiap (default = automatically assign tunnel ssids). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, tunnel, bridge, manual]</span> 
 <a id='label498' href="javascript:ContentClick('label499', 'label498');" onmouseover="ContentPreview('label499');" onmouseout="ContentUnpreview('label499');" title="click to collapse or expand..."> more... </a>
 <div id="label499" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap1</span> Virtual access point (vap) for wlan id 1 <span class="li-normal">type: str</span>
 <a id='label500' href="javascript:ContentClick('label501', 'label500');" onmouseover="ContentPreview('label501');" onmouseout="ContentUnpreview('label501');" title="click to collapse or expand..."> more... </a>
 <div id="label501" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap2</span> Virtual access point (vap) for wlan id 2 <span class="li-normal">type: str</span>
 <a id='label502' href="javascript:ContentClick('label503', 'label502');" onmouseover="ContentPreview('label503');" onmouseout="ContentUnpreview('label503');" title="click to collapse or expand..."> more... </a>
 <div id="label503" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap3</span> Virtual access point (vap) for wlan id 3 <span class="li-normal">type: str</span>
 <a id='label504' href="javascript:ContentClick('label505', 'label504');" onmouseover="ContentPreview('label505');" onmouseout="ContentUnpreview('label505');" title="click to collapse or expand..."> more... </a>
 <div id="label505" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap4</span> Virtual access point (vap) for wlan id 4 <span class="li-normal">type: str</span>
 <a id='label506' href="javascript:ContentClick('label507', 'label506');" onmouseover="ContentPreview('label507');" onmouseout="ContentUnpreview('label507');" title="click to collapse or expand..."> more... </a>
 <div id="label507" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap5</span> Virtual access point (vap) for wlan id 5 <span class="li-normal">type: str</span>
 <a id='label508' href="javascript:ContentClick('label509', 'label508');" onmouseover="ContentPreview('label509');" onmouseout="ContentUnpreview('label509');" title="click to collapse or expand..."> more... </a>
 <div id="label509" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap6</span> Virtual access point (vap) for wlan id 6 <span class="li-normal">type: str</span>
 <a id='label510' href="javascript:ContentClick('label511', 'label510');" onmouseover="ContentPreview('label511');" onmouseout="ContentUnpreview('label511');" title="click to collapse or expand..."> more... </a>
 <div id="label511" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap7</span> Virtual access point (vap) for wlan id 7 <span class="li-normal">type: str</span>
 <a id='label512' href="javascript:ContentClick('label513', 'label512');" onmouseover="ContentPreview('label513');" onmouseout="ContentUnpreview('label513');" title="click to collapse or expand..."> more... </a>
 <div id="label513" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap8</span> Virtual access point (vap) for wlan id 8 <span class="li-normal">type: str</span>
 <a id='label514' href="javascript:ContentClick('label515', 'label514');" onmouseover="ContentPreview('label515');" onmouseout="ContentUnpreview('label515');" title="click to collapse or expand..."> more... </a>
 <div id="label515" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vaps</span> Manually selected list of virtual access points (vaps). <span class="li-normal">type: list or str</span>
 <a id='label516' href="javascript:ContentClick('label517', 'label516');" onmouseover="ContentPreview('label517');" onmouseout="ContentUnpreview('label517');" title="click to collapse or expand..."> more... </a>
 <div id="label517" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wids_profile</span> <b>(Alias name: wids-profile)</b>  Wireless intrusion detection system (wids) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label518' href="javascript:ContentClick('label519', 'label518');" onmouseover="ContentPreview('label519');" onmouseout="ContentUnpreview('label519');" title="click to collapse or expand..."> more... </a>
 <div id="label519" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">zero_wait_dfs</span> <b>(Alias name: zero-wait-dfs)</b>  Enable/disable zero wait dfs on radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label520' href="javascript:ContentClick('label521', 'label520');" onmouseover="ContentPreview('label521');" onmouseout="ContentUnpreview('label521');" title="click to collapse or expand..."> more... </a>
 <div id="label521" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frequency_handoff</span> <b>(Alias name: frequency-handoff)</b>  Enable/disable frequency handoff of clients to other channels (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label522' href="javascript:ContentClick('label523', 'label522');" onmouseover="ContentPreview('label523');" onmouseout="ContentUnpreview('label523');" title="click to collapse or expand..."> more... </a>
 <div id="label523" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_handoff</span> <b>(Alias name: ap-handoff)</b>  Enable/disable ap handoff of clients to other aps (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label524' href="javascript:ContentClick('label525', 'label524');" onmouseover="ContentPreview('label525');" onmouseout="ContentUnpreview('label525');" title="click to collapse or expand..."> more... </a>
 <div id="label525" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_protocol</span> <b>(Alias name: iperf-protocol)</b>  Iperf test protocol (default = udp). <span class="li-normal">type: str</span> <span class="li-normal">choices: [udp, tcp]</span> 
 <a id='label526' href="javascript:ContentClick('label527', 'label526');" onmouseover="ContentPreview('label527');" onmouseout="ContentUnpreview('label527');" title="click to collapse or expand..."> more... </a>
 <div id="label527" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_server_port</span> <b>(Alias name: iperf-server-port)</b>  Iperf service port number. <span class="li-normal">type: int</span>
 <a id='label528' href="javascript:ContentClick('label529', 'label528');" onmouseover="ContentPreview('label529');" onmouseout="ContentUnpreview('label529');" title="click to collapse or expand..."> more... </a>
 <div id="label529" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_mode</span> <b>(Alias name: power-mode)</b>  Set radio effective isotropic radiated power (eirp) in dbm or by a percentage of the maximum eirp (default = percentage). <span class="li-normal">type: str</span> <span class="li-normal">choices: [dBm, percentage]</span> 
 <a id='label530' href="javascript:ContentClick('label531', 'label530');" onmouseover="ContentPreview('label531');" onmouseout="ContentUnpreview('label531');" title="click to collapse or expand..."> more... </a>
 <div id="label531" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_value</span> <b>(Alias name: power-value)</b>  Radio eirp power in dbm (1 - 33, default = 27). <span class="li-normal">type: int</span>
 <a id='label532' href="javascript:ContentClick('label533', 'label532');" onmouseover="ContentPreview('label533');" onmouseout="ContentUnpreview('label533');" title="click to collapse or expand..."> more... </a>
 <div id="label533" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_bssid</span> <b>(Alias name: sam-bssid)</b>  Bssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label534' href="javascript:ContentClick('label535', 'label534');" onmouseover="ContentPreview('label535');" onmouseout="ContentUnpreview('label535');" title="click to collapse or expand..."> more... </a>
 <div id="label535" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_captive_portal</span> <b>(Alias name: sam-captive-portal)</b>  Enable/disable captive portal authentication (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label536' href="javascript:ContentClick('label537', 'label536');" onmouseover="ContentPreview('label537');" onmouseout="ContentUnpreview('label537');" title="click to collapse or expand..."> more... </a>
 <div id="label537" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_password</span> <b>(Alias name: sam-password)</b>  Passphrase for wifi network connection. <span class="li-normal">type: list</span>
 <a id='label538' href="javascript:ContentClick('label539', 'label538');" onmouseover="ContentPreview('label539');" onmouseout="ContentUnpreview('label539');" title="click to collapse or expand..."> more... </a>
 <div id="label539" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_report_intv</span> <b>(Alias name: sam-report-intv)</b>  Sam report interval (sec), 0 for a one-time report. <span class="li-normal">type: int</span>
 <a id='label540' href="javascript:ContentClick('label541', 'label540');" onmouseover="ContentPreview('label541');" onmouseout="ContentUnpreview('label541');" title="click to collapse or expand..."> more... </a>
 <div id="label541" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_security_type</span> <b>(Alias name: sam-security-type)</b>  Select wifi network security type (default = wpa-personal). <span class="li-normal">type: str</span> <span class="li-normal">choices: [open, wpa-personal, wpa-enterprise, owe, wpa3-sae]</span> 
 <a id='label542' href="javascript:ContentClick('label543', 'label542');" onmouseover="ContentPreview('label543');" onmouseout="ContentUnpreview('label543');" title="click to collapse or expand..."> more... </a>
 <div id="label543" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server</span> <b>(Alias name: sam-server)</b>  Sam test server ip address or domain name. <span class="li-normal">type: str</span>
 <a id='label544' href="javascript:ContentClick('label545', 'label544');" onmouseover="ContentPreview('label545');" onmouseout="ContentUnpreview('label545');" title="click to collapse or expand..."> more... </a>
 <div id="label545" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ssid</span> <b>(Alias name: sam-ssid)</b>  Ssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label546' href="javascript:ContentClick('label547', 'label546');" onmouseover="ContentPreview('label547');" onmouseout="ContentUnpreview('label547');" title="click to collapse or expand..."> more... </a>
 <div id="label547" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_test</span> <b>(Alias name: sam-test)</b>  Select sam test type (default = ping). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ping, iperf]</span> 
 <a id='label548' href="javascript:ContentClick('label549', 'label548');" onmouseover="ContentPreview('label549');" onmouseout="ContentUnpreview('label549');" title="click to collapse or expand..."> more... </a>
 <div id="label549" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_username</span> <b>(Alias name: sam-username)</b>  Username for wifi network connection. <span class="li-normal">type: str</span>
 <a id='label550' href="javascript:ContentClick('label551', 'label550');" onmouseover="ContentPreview('label551');" onmouseout="ContentUnpreview('label551');" title="click to collapse or expand..."> more... </a>
 <div id="label551" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">arrp_profile</span> <b>(Alias name: arrp-profile)</b>  Distributed automatic radio resource provisioning (darrp) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label552' href="javascript:ContentClick('label553', 'label552');" onmouseover="ContentPreview('label553');" onmouseout="ContentUnpreview('label553');" title="click to collapse or expand..."> more... </a>
 <div id="label553" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color_mode</span> <b>(Alias name: bss-color-mode)</b>  Bss color mode for this 11ax radio (default = auto). <span class="li-normal">type: str</span> <span class="li-normal">choices: [auto, static]</span> 
 <a id='label554' href="javascript:ContentClick('label555', 'label554');" onmouseover="ContentPreview('label555');" onmouseout="ContentUnpreview('label555');" title="click to collapse or expand..."> more... </a>
 <div id="label555" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_failure_string</span> <b>(Alias name: sam-cwp-failure-string)</b>  Failure identification on the page after an incorrect login. <span class="li-normal">type: str</span>
 <a id='label556' href="javascript:ContentClick('label557', 'label556');" onmouseover="ContentPreview('label557');" onmouseout="ContentUnpreview('label557');" title="click to collapse or expand..."> more... </a>
 <div id="label557" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_match_string</span> <b>(Alias name: sam-cwp-match-string)</b>  Identification string from the captive portal login form. <span class="li-normal">type: str</span>
 <a id='label558' href="javascript:ContentClick('label559', 'label558');" onmouseover="ContentPreview('label559');" onmouseout="ContentUnpreview('label559');" title="click to collapse or expand..."> more... </a>
 <div id="label559" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_password</span> <b>(Alias name: sam-cwp-password)</b>  Password for captive portal authentication. <span class="li-normal">type: list</span>
 <a id='label560' href="javascript:ContentClick('label561', 'label560');" onmouseover="ContentPreview('label561');" onmouseout="ContentUnpreview('label561');" title="click to collapse or expand..."> more... </a>
 <div id="label561" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_success_string</span> <b>(Alias name: sam-cwp-success-string)</b>  Success identification on the page after a successful login. <span class="li-normal">type: str</span>
 <a id='label562' href="javascript:ContentClick('label563', 'label562');" onmouseover="ContentPreview('label563');" onmouseout="ContentUnpreview('label563');" title="click to collapse or expand..."> more... </a>
 <div id="label563" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_test_url</span> <b>(Alias name: sam-cwp-test-url)</b>  Website the client is trying to access. <span class="li-normal">type: str</span>
 <a id='label564' href="javascript:ContentClick('label565', 'label564');" onmouseover="ContentPreview('label565');" onmouseout="ContentUnpreview('label565');" title="click to collapse or expand..."> more... </a>
 <div id="label565" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_username</span> <b>(Alias name: sam-cwp-username)</b>  Username for captive portal authentication. <span class="li-normal">type: str</span>
 <a id='label566' href="javascript:ContentClick('label567', 'label566');" onmouseover="ContentPreview('label567');" onmouseout="ContentUnpreview('label567');" title="click to collapse or expand..."> more... </a>
 <div id="label567" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_fqdn</span> <b>(Alias name: sam-server-fqdn)</b>  Sam test server domain name. <span class="li-normal">type: str</span>
 <a id='label568' href="javascript:ContentClick('label569', 'label568');" onmouseover="ContentPreview('label569');" onmouseout="ContentUnpreview('label569');" title="click to collapse or expand..."> more... </a>
 <div id="label569" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_ip</span> <b>(Alias name: sam-server-ip)</b>  Sam test server ip address. <span class="li-normal">type: str</span>
 <a id='label570' href="javascript:ContentClick('label571', 'label570');" onmouseover="ContentPreview('label571');" onmouseout="ContentUnpreview('label571');" title="click to collapse or expand..."> more... </a>
 <div id="label571" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_type</span> <b>(Alias name: sam-server-type)</b>  Select sam server type (default = ip). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ip, fqdn]</span> 
 <a id='label572' href="javascript:ContentClick('label573', 'label572');" onmouseover="ContentPreview('label573');" onmouseout="ContentUnpreview('label573');" title="click to collapse or expand..."> more... </a>
 <div id="label573" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211d</span> <b>(Alias name: 80211d)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label574' href="javascript:ContentClick('label575', 'label574');" onmouseover="ContentPreview('label575');" onmouseout="ContentUnpreview('label575');" title="click to collapse or expand..."> more... </a>
 <div id="label575" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna</span> <b>(Alias name: optional-antenna)</b>  Optional antenna used on fap (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, FANT-04ABGN-8065-P-N, FANT-04ABGN-0606-O-R, FANT-04ABGN-0606-P-R, FANT-10ACAX-1213-D-N, FANT-08ABGN-1213-D-R, custom]</span> 
 <a id='label576' href="javascript:ContentClick('label577', 'label576');" onmouseover="ContentPreview('label577');" onmouseout="ContentUnpreview('label577');" title="click to collapse or expand..."> more... </a>
 <div id="label577" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mimo_mode</span> <b>(Alias name: mimo-mode)</b>  Configure radio mimo mode (default = default). <span class="li-normal">type: str</span> <span class="li-normal">choices: [default, 1x1, 2x2, 3x3, 4x4, 8x8]</span> 
 <a id='label578' href="javascript:ContentClick('label579', 'label578');" onmouseover="ContentPreview('label579');" onmouseout="ContentUnpreview('label579');" title="click to collapse or expand..."> more... </a>
 <div id="label579" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna_gain</span> <b>(Alias name: optional-antenna-gain)</b>  Optional antenna gain in dbi (0 to 20, default = 0). <span class="li-normal">type: str</span>
 <a id='label580' href="javascript:ContentClick('label581', 'label580');" onmouseover="ContentPreview('label581');" onmouseout="ContentUnpreview('label581');" title="click to collapse or expand..."> more... </a>
 <div id="label581" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ca_certificate</span> <b>(Alias name: sam-ca-certificate)</b>  Ca certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label582' href="javascript:ContentClick('label583', 'label582');" onmouseover="ContentPreview('label583');" onmouseout="ContentUnpreview('label583');" title="click to collapse or expand..."> more... </a>
 <div id="label583" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_client_certificate</span> <b>(Alias name: sam-client-certificate)</b>  Client certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label584' href="javascript:ContentClick('label585', 'label584');" onmouseover="ContentPreview('label585');" onmouseout="ContentUnpreview('label585');" title="click to collapse or expand..."> more... </a>
 <div id="label585" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_eap_method</span> <b>(Alias name: sam-eap-method)</b>  Select wpa2/wpa3-enterprise eap method (default = peap). <span class="li-normal">type: str</span> <span class="li-normal">choices: [tls, peap, both]</span> 
 <a id='label586' href="javascript:ContentClick('label587', 'label586');" onmouseover="ContentPreview('label587');" onmouseout="ContentUnpreview('label587');" title="click to collapse or expand..."> more... </a>
 <div id="label587" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key</span> <b>(Alias name: sam-private-key)</b>  Private key for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label588' href="javascript:ContentClick('label589', 'label588');" onmouseover="ContentPreview('label589');" onmouseout="ContentUnpreview('label589');" title="click to collapse or expand..."> more... </a>
 <div id="label589" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key_password</span> <b>(Alias name: sam-private-key-password)</b>  Password for private key file for wpa2/wpa3-enterprise. <span class="li-normal">type: list</span>
 <a id='label590' href="javascript:ContentClick('label591', 'label590');" onmouseover="ContentPreview('label591');" onmouseout="ContentUnpreview('label591');" title="click to collapse or expand..."> more... </a>
 <div id="label591" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding_ext</span> <b>(Alias name: channel-bonding-ext)</b>  Channel bandwidth extension: 320 mhz-1 and 320 mhz-2 (default = 320 mhz-2). <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz-1, 320MHz-2]</span> 
 <a id='label592' href="javascript:ContentClick('label593', 'label592');" onmouseover="ContentPreview('label593');" onmouseout="ContentUnpreview('label593');" title="click to collapse or expand..."> more... </a>
 <div id="label593" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211mc</span> <b>(Alias name: 80211mc)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label594' href="javascript:ContentClick('label595', 'label594');" onmouseover="ContentPreview('label595');" onmouseout="ContentUnpreview('label595');" title="click to collapse or expand..."> more... </a>
 <div id="label595" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan_width</span> <b>(Alias name: ap-sniffer-chan-width)</b>  Channel bandwidth for sniffer. <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz, 240MHz, 160MHz, 80MHz, 40MHz, 20MHz]</span> 
 <a id='label596' href="javascript:ContentClick('label597', 'label596');" onmouseover="ContentPreview('label597');" onmouseout="ContentUnpreview('label597');" title="click to collapse or expand..."> more... </a>
 <div id="label597" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">radio_3</span> <b>(Alias name: radio-3)</b>  Radio 3. <span class="li-normal">type: dict</span>
 <a id='label598' href="javascript:ContentClick('label599', 'label598');" onmouseover="ContentPreview('label599');" onmouseout="ContentUnpreview('label599');" title="click to collapse or expand..."> more... </a>
 <div id="label599" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">airtime_fairness</span> <b>(Alias name: airtime-fairness)</b>  Enable/disable airtime fairness (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label600' href="javascript:ContentClick('label601', 'label600');" onmouseover="ContentPreview('label601');" onmouseout="ContentUnpreview('label601');" title="click to collapse or expand..."> more... </a>
 <div id="label601" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">amsdu</span> Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label602' href="javascript:ContentClick('label603', 'label602');" onmouseover="ContentPreview('label603');" onmouseout="ContentUnpreview('label603');" title="click to collapse or expand..."> more... </a>
 <div id="label603" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_addr</span> <b>(Alias name: ap-sniffer-addr)</b>  Mac address to monitor. <span class="li-normal">type: str</span>
 <a id='label604' href="javascript:ContentClick('label605', 'label604');" onmouseover="ContentPreview('label605');" onmouseout="ContentUnpreview('label605');" title="click to collapse or expand..."> more... </a>
 <div id="label605" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_bufsize</span> <b>(Alias name: ap-sniffer-bufsize)</b>  Sniffer buffer size (1 - 32 mb, default = 16). <span class="li-normal">type: int</span>
 <a id='label606' href="javascript:ContentClick('label607', 'label606');" onmouseover="ContentPreview('label607');" onmouseout="ContentUnpreview('label607');" title="click to collapse or expand..."> more... </a>
 <div id="label607" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan</span> <b>(Alias name: ap-sniffer-chan)</b>  Channel on which to operate the sniffer (default = 6). <span class="li-normal">type: int</span>
 <a id='label608' href="javascript:ContentClick('label609', 'label608');" onmouseover="ContentPreview('label609');" onmouseout="ContentUnpreview('label609');" title="click to collapse or expand..."> more... </a>
 <div id="label609" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_ctl</span> <b>(Alias name: ap-sniffer-ctl)</b>  Enable/disable sniffer on wifi control frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label610' href="javascript:ContentClick('label611', 'label610');" onmouseover="ContentPreview('label611');" onmouseout="ContentUnpreview('label611');" title="click to collapse or expand..."> more... </a>
 <div id="label611" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_data</span> <b>(Alias name: ap-sniffer-data)</b>  Enable/disable sniffer on wifi data frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label612' href="javascript:ContentClick('label613', 'label612');" onmouseover="ContentPreview('label613');" onmouseout="ContentUnpreview('label613');" title="click to collapse or expand..."> more... </a>
 <div id="label613" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_beacon</span> <b>(Alias name: ap-sniffer-mgmt-beacon)</b>  Enable/disable sniffer on wifi management beacon frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label614' href="javascript:ContentClick('label615', 'label614');" onmouseover="ContentPreview('label615');" onmouseout="ContentUnpreview('label615');" title="click to collapse or expand..."> more... </a>
 <div id="label615" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_other</span> <b>(Alias name: ap-sniffer-mgmt-other)</b>  Enable/disable sniffer on wifi management other frames  (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label616' href="javascript:ContentClick('label617', 'label616');" onmouseover="ContentPreview('label617');" onmouseout="ContentUnpreview('label617');" title="click to collapse or expand..."> more... </a>
 <div id="label617" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_probe</span> <b>(Alias name: ap-sniffer-mgmt-probe)</b>  Enable/disable sniffer on wifi management probe frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label618' href="javascript:ContentClick('label619', 'label618');" onmouseover="ContentPreview('label619');" onmouseout="ContentUnpreview('label619');" title="click to collapse or expand..."> more... </a>
 <div id="label619" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_high</span> <b>(Alias name: auto-power-high)</b>  The upper bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label620' href="javascript:ContentClick('label621', 'label620');" onmouseover="ContentPreview('label621');" onmouseout="ContentUnpreview('label621');" title="click to collapse or expand..."> more... </a>
 <div id="label621" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_level</span> <b>(Alias name: auto-power-level)</b>  Enable/disable automatic power-level adjustment to prevent co-channel interference (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label622' href="javascript:ContentClick('label623', 'label622');" onmouseover="ContentPreview('label623');" onmouseout="ContentUnpreview('label623');" title="click to collapse or expand..."> more... </a>
 <div id="label623" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_low</span> <b>(Alias name: auto-power-low)</b>  The lower bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label624' href="javascript:ContentClick('label625', 'label624');" onmouseover="ContentPreview('label625');" onmouseout="ContentUnpreview('label625');" title="click to collapse or expand..."> more... </a>
 <div id="label625" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_target</span> <b>(Alias name: auto-power-target)</b>  The target of automatic transmit power adjustment in dbm. <span class="li-normal">type: str</span>
 <a id='label626' href="javascript:ContentClick('label627', 'label626');" onmouseover="ContentPreview('label627');" onmouseout="ContentUnpreview('label627');" title="click to collapse or expand..."> more... </a>
 <div id="label627" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band</span> Wifi band that radio 3 operates on. <span class="li-normal">type: str</span> <span class="li-normal">choices: [802.11b, 802.11a, 802.11g, 802.11n, 802.11ac, 802.11n-5G, 802.11ax-5G, 802.11ax, 802.11ac-2G, 802.11g-only, 802.11n-only, 802.11n,g-only, 802.11ac-only, 802.11ac,n-only, 802.11n-5G-only, 802.11ax-5G-only, 802.11ax,ac-only, 802.11ax,ac,n-only, 802.11ax-only, 802.11ax,n-only, 802.11ax,n,g-only, 802.11ax-6G, 802.11n-2G, 802.11ac-5G, 802.11ax-2G, 802.11be-2G, 802.11be-5G, 802.11be-6G]</span> 
 <a id='label628' href="javascript:ContentClick('label629', 'label628');" onmouseover="ContentPreview('label629');" onmouseout="ContentUnpreview('label629');" title="click to collapse or expand..."> more... </a>
 <div id="label629" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band_5g_type</span> <b>(Alias name: band-5g-type)</b>  Wifi 5g band type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [5g-full, 5g-high, 5g-low]</span> 
 <a id='label630' href="javascript:ContentClick('label631', 'label630');" onmouseover="ContentPreview('label631');" onmouseout="ContentUnpreview('label631');" title="click to collapse or expand..."> more... </a>
 <div id="label631" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_admission_control</span> <b>(Alias name: bandwidth-admission-control)</b>  Enable/disable wifi multimedia (wmm) bandwidth admission control to optimize wifi bandwidth use. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label632' href="javascript:ContentClick('label633', 'label632');" onmouseover="ContentPreview('label633');" onmouseout="ContentUnpreview('label633');" title="click to collapse or expand..."> more... </a>
 <div id="label633" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_capacity</span> <b>(Alias name: bandwidth-capacity)</b>  Maximum bandwidth capacity allowed (1 - 600000 kbps, default = 2000). <span class="li-normal">type: int</span>
 <a id='label634' href="javascript:ContentClick('label635', 'label634');" onmouseover="ContentPreview('label635');" onmouseout="ContentUnpreview('label635');" title="click to collapse or expand..."> more... </a>
 <div id="label635" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">beacon_interval</span> <b>(Alias name: beacon-interval)</b>  Beacon interval. <span class="li-normal">type: int</span>
 <a id='label636' href="javascript:ContentClick('label637', 'label636');" onmouseover="ContentPreview('label637');" onmouseout="ContentUnpreview('label637');" title="click to collapse or expand..."> more... </a>
 <div id="label637" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color</span> <b>(Alias name: bss-color)</b>  Bss color value for this 11ax radio (0 - 63, 0 means disable. <span class="li-normal">type: int</span>
 <a id='label638' href="javascript:ContentClick('label639', 'label638');" onmouseover="ContentPreview('label639');" onmouseout="ContentUnpreview('label639');" title="click to collapse or expand..."> more... </a>
 <div id="label639" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_admission_control</span> <b>(Alias name: call-admission-control)</b>  Enable/disable wifi multimedia (wmm) call admission control to optimize wifi bandwidth use for voip calls. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label640' href="javascript:ContentClick('label641', 'label640');" onmouseover="ContentPreview('label641');" onmouseout="ContentUnpreview('label641');" title="click to collapse or expand..."> more... </a>
 <div id="label641" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_capacity</span> <b>(Alias name: call-capacity)</b>  Maximum number of voice over wlan (vowlan) phones supported by the radio (0 - 60, default = 10). <span class="li-normal">type: int</span>
 <a id='label642' href="javascript:ContentClick('label643', 'label642');" onmouseover="ContentPreview('label643');" onmouseout="ContentUnpreview('label643');" title="click to collapse or expand..."> more... </a>
 <div id="label643" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel</span> Selected list of wireless radio channels. <span class="li-normal">type: list</span>
 <a id='label644' href="javascript:ContentClick('label645', 'label644');" onmouseover="ContentPreview('label645');" onmouseout="ContentUnpreview('label645');" title="click to collapse or expand..."> more... </a>
 <div id="label645" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding</span> <b>(Alias name: channel-bonding)</b>  Channel bandwidth: 160,80, 40, or 20mhz. <span class="li-normal">type: str</span> <span class="li-normal">choices: [80MHz, 40MHz, 20MHz, 160MHz, 320MHz, 240MHz]</span> 
 <a id='label646' href="javascript:ContentClick('label647', 'label646');" onmouseover="ContentPreview('label647');" onmouseout="ContentUnpreview('label647');" title="click to collapse or expand..."> more... </a>
 <div id="label647" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_utilization</span> <b>(Alias name: channel-utilization)</b>  Enable/disable measuring channel utilization. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label648' href="javascript:ContentClick('label649', 'label648');" onmouseover="ContentPreview('label649');" onmouseout="ContentUnpreview('label649');" title="click to collapse or expand..."> more... </a>
 <div id="label649" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">coexistence</span> Enable/disable allowing both ht20 and ht40 on the same radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label650' href="javascript:ContentClick('label651', 'label650');" onmouseover="ContentPreview('label651');" onmouseout="ContentUnpreview('label651');" title="click to collapse or expand..."> more... </a>
 <div id="label651" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">darrp</span> Enable/disable distributed automatic radio resource provisioning (darrp) to make sure the radio is always using the most optimal channel (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label652' href="javascript:ContentClick('label653', 'label652');" onmouseover="ContentPreview('label653');" onmouseout="ContentUnpreview('label653');" title="click to collapse or expand..."> more... </a>
 <div id="label653" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma</span> Enable/disable dynamic radio mode assignment (drma) (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label654' href="javascript:ContentClick('label655', 'label654');" onmouseover="ContentPreview('label655');" onmouseout="ContentUnpreview('label655');" title="click to collapse or expand..."> more... </a>
 <div id="label655" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma_sensitivity</span> <b>(Alias name: drma-sensitivity)</b>  Network coverage factor (ncf) percentage required to consider a radio as redundant (default = low). <span class="li-normal">type: str</span> <span class="li-normal">choices: [low, medium, high]</span> 
 <a id='label656' href="javascript:ContentClick('label657', 'label656');" onmouseover="ContentPreview('label657');" onmouseout="ContentUnpreview('label657');" title="click to collapse or expand..."> more... </a>
 <div id="label657" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dtim</span> Delivery traffic indication map (dtim) period (1 - 255, default = 1). <span class="li-normal">type: int</span>
 <a id='label658' href="javascript:ContentClick('label659', 'label658');" onmouseover="ContentPreview('label659');" onmouseout="ContentUnpreview('label659');" title="click to collapse or expand..."> more... </a>
 <div id="label659" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_threshold</span> <b>(Alias name: frag-threshold)</b>  Maximum packet size that can be sent without fragmentation (800 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label660' href="javascript:ContentClick('label661', 'label660');" onmouseover="ContentPreview('label661');" onmouseout="ContentUnpreview('label661');" title="click to collapse or expand..."> more... </a>
 <div id="label661" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_clients</span> <b>(Alias name: max-clients)</b>  Maximum number of stations (stas) or wifi clients supported by the radio. <span class="li-normal">type: int</span>
 <a id='label662' href="javascript:ContentClick('label663', 'label662');" onmouseover="ContentPreview('label663');" onmouseout="ContentUnpreview('label663');" title="click to collapse or expand..."> more... </a>
 <div id="label663" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_distance</span> <b>(Alias name: max-distance)</b>  Maximum expected distance between the ap and clients (0 - 54000 m, default = 0). <span class="li-normal">type: int</span>
 <a id='label664' href="javascript:ContentClick('label665', 'label664');" onmouseover="ContentPreview('label665');" onmouseout="ContentUnpreview('label665');" title="click to collapse or expand..."> more... </a>
 <div id="label665" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mode</span> Mode of radio 3. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disabled, ap, monitor, sniffer, sam]</span> 
 <a id='label666' href="javascript:ContentClick('label667', 'label666');" onmouseover="ContentPreview('label667');" onmouseout="ContentUnpreview('label667');" title="click to collapse or expand..."> more... </a>
 <div id="label667" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_level</span> <b>(Alias name: power-level)</b>  Radio power level as a percentage of the maximum transmit power (0 - 100, default = 100). <span class="li-normal">type: int</span>
 <a id='label668' href="javascript:ContentClick('label669', 'label668');" onmouseover="ContentPreview('label669');" onmouseout="ContentUnpreview('label669');" title="click to collapse or expand..."> more... </a>
 <div id="label669" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">powersave_optimize</span> <b>(Alias name: powersave-optimize)</b>  Enable client power-saving features such as tim, ac vo, and obss etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [tim, ac-vo, no-obss-scan, no-11b-rate, client-rate-follow]</span> 
 <a id='label670' href="javascript:ContentClick('label671', 'label670');" onmouseover="ContentPreview('label671');" onmouseout="ContentUnpreview('label671');" title="click to collapse or expand..."> more... </a>
 <div id="label671" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protection_mode</span> <b>(Alias name: protection-mode)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [rtscts, ctsonly, disable]</span> 
 <a id='label672' href="javascript:ContentClick('label673', 'label672');" onmouseover="ContentPreview('label673');" onmouseout="ContentUnpreview('label673');" title="click to collapse or expand..."> more... </a>
 <div id="label673" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">radio_id</span> <b>(Alias name: radio-id)</b>  Radio id. <span class="li-normal">type: int</span>
 <a id='label674' href="javascript:ContentClick('label675', 'label674');" onmouseover="ContentPreview('label675');" onmouseout="ContentUnpreview('label675');" title="click to collapse or expand..."> more... </a>
 <div id="label675" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rts_threshold</span> <b>(Alias name: rts-threshold)</b>  Maximum packet size for rts transmissions, specifying the maximum size of a data packet before rts/cts (256 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label676' href="javascript:ContentClick('label677', 'label676');" onmouseover="ContentPreview('label677');" onmouseout="ContentUnpreview('label677');" title="click to collapse or expand..."> more... </a>
 <div id="label677" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">short_guard_interval</span> <b>(Alias name: short-guard-interval)</b>  Use either the short guard interval (short gi) of 400 ns or the long guard interval (long gi) of 800 ns. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label678' href="javascript:ContentClick('label679', 'label678');" onmouseover="ContentPreview('label679');" onmouseout="ContentUnpreview('label679');" title="click to collapse or expand..."> more... </a>
 <div id="label679" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">spectrum_analysis</span> <b>(Alias name: spectrum-analysis)</b>  Enable/disable spectrum analysis to find interference that would negatively impact wireless performance. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, scan-only]</span> 
 <a id='label680' href="javascript:ContentClick('label681', 'label680');" onmouseover="ContentPreview('label681');" onmouseout="ContentUnpreview('label681');" title="click to collapse or expand..."> more... </a>
 <div id="label681" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">transmit_optimize</span> <b>(Alias name: transmit-optimize)</b>  Packet transmission optimization options including power saving, aggregation limiting, retry limiting, etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [disable, power-save, aggr-limit, retry-limit, send-bar]</span> 
 <a id='label682' href="javascript:ContentClick('label683', 'label682');" onmouseover="ContentPreview('label683');" onmouseout="ContentUnpreview('label683');" title="click to collapse or expand..."> more... </a>
 <div id="label683" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap_all</span> <b>(Alias name: vap-all)</b>  Configure method for assigning ssids to this fortiap (default = automatically assign tunnel ssids). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, tunnel, bridge, manual]</span> 
 <a id='label684' href="javascript:ContentClick('label685', 'label684');" onmouseover="ContentPreview('label685');" onmouseout="ContentUnpreview('label685');" title="click to collapse or expand..."> more... </a>
 <div id="label685" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap1</span> Virtual access point (vap) for wlan id 1 <span class="li-normal">type: str</span>
 <a id='label686' href="javascript:ContentClick('label687', 'label686');" onmouseover="ContentPreview('label687');" onmouseout="ContentUnpreview('label687');" title="click to collapse or expand..."> more... </a>
 <div id="label687" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap2</span> Virtual access point (vap) for wlan id 2 <span class="li-normal">type: str</span>
 <a id='label688' href="javascript:ContentClick('label689', 'label688');" onmouseover="ContentPreview('label689');" onmouseout="ContentUnpreview('label689');" title="click to collapse or expand..."> more... </a>
 <div id="label689" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap3</span> Virtual access point (vap) for wlan id 3 <span class="li-normal">type: str</span>
 <a id='label690' href="javascript:ContentClick('label691', 'label690');" onmouseover="ContentPreview('label691');" onmouseout="ContentUnpreview('label691');" title="click to collapse or expand..."> more... </a>
 <div id="label691" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap4</span> Virtual access point (vap) for wlan id 4 <span class="li-normal">type: str</span>
 <a id='label692' href="javascript:ContentClick('label693', 'label692');" onmouseover="ContentPreview('label693');" onmouseout="ContentUnpreview('label693');" title="click to collapse or expand..."> more... </a>
 <div id="label693" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap5</span> Virtual access point (vap) for wlan id 5 <span class="li-normal">type: str</span>
 <a id='label694' href="javascript:ContentClick('label695', 'label694');" onmouseover="ContentPreview('label695');" onmouseout="ContentUnpreview('label695');" title="click to collapse or expand..."> more... </a>
 <div id="label695" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap6</span> Virtual access point (vap) for wlan id 6 <span class="li-normal">type: str</span>
 <a id='label696' href="javascript:ContentClick('label697', 'label696');" onmouseover="ContentPreview('label697');" onmouseout="ContentUnpreview('label697');" title="click to collapse or expand..."> more... </a>
 <div id="label697" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap7</span> Virtual access point (vap) for wlan id 7 <span class="li-normal">type: str</span>
 <a id='label698' href="javascript:ContentClick('label699', 'label698');" onmouseover="ContentPreview('label699');" onmouseout="ContentUnpreview('label699');" title="click to collapse or expand..."> more... </a>
 <div id="label699" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap8</span> Virtual access point (vap) for wlan id 8 <span class="li-normal">type: str</span>
 <a id='label700' href="javascript:ContentClick('label701', 'label700');" onmouseover="ContentPreview('label701');" onmouseout="ContentUnpreview('label701');" title="click to collapse or expand..."> more... </a>
 <div id="label701" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vaps</span> Manually selected list of virtual access points (vaps). <span class="li-normal">type: list or str</span>
 <a id='label702' href="javascript:ContentClick('label703', 'label702');" onmouseover="ContentPreview('label703');" onmouseout="ContentUnpreview('label703');" title="click to collapse or expand..."> more... </a>
 <div id="label703" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wids_profile</span> <b>(Alias name: wids-profile)</b>  Wireless intrusion detection system (wids) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label704' href="javascript:ContentClick('label705', 'label704');" onmouseover="ContentPreview('label705');" onmouseout="ContentUnpreview('label705');" title="click to collapse or expand..."> more... </a>
 <div id="label705" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">zero_wait_dfs</span> <b>(Alias name: zero-wait-dfs)</b>  Enable/disable zero wait dfs on radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label706' href="javascript:ContentClick('label707', 'label706');" onmouseover="ContentPreview('label707');" onmouseout="ContentUnpreview('label707');" title="click to collapse or expand..."> more... </a>
 <div id="label707" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frequency_handoff</span> <b>(Alias name: frequency-handoff)</b>  Enable/disable frequency handoff of clients to other channels (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label708' href="javascript:ContentClick('label709', 'label708');" onmouseover="ContentPreview('label709');" onmouseout="ContentUnpreview('label709');" title="click to collapse or expand..."> more... </a>
 <div id="label709" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_handoff</span> <b>(Alias name: ap-handoff)</b>  Enable/disable ap handoff of clients to other aps (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label710' href="javascript:ContentClick('label711', 'label710');" onmouseover="ContentPreview('label711');" onmouseout="ContentUnpreview('label711');" title="click to collapse or expand..."> more... </a>
 <div id="label711" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_protocol</span> <b>(Alias name: iperf-protocol)</b>  Iperf test protocol (default = udp). <span class="li-normal">type: str</span> <span class="li-normal">choices: [udp, tcp]</span> 
 <a id='label712' href="javascript:ContentClick('label713', 'label712');" onmouseover="ContentPreview('label713');" onmouseout="ContentUnpreview('label713');" title="click to collapse or expand..."> more... </a>
 <div id="label713" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_server_port</span> <b>(Alias name: iperf-server-port)</b>  Iperf service port number. <span class="li-normal">type: int</span>
 <a id='label714' href="javascript:ContentClick('label715', 'label714');" onmouseover="ContentPreview('label715');" onmouseout="ContentUnpreview('label715');" title="click to collapse or expand..."> more... </a>
 <div id="label715" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_mode</span> <b>(Alias name: power-mode)</b>  Set radio effective isotropic radiated power (eirp) in dbm or by a percentage of the maximum eirp (default = percentage). <span class="li-normal">type: str</span> <span class="li-normal">choices: [dBm, percentage]</span> 
 <a id='label716' href="javascript:ContentClick('label717', 'label716');" onmouseover="ContentPreview('label717');" onmouseout="ContentUnpreview('label717');" title="click to collapse or expand..."> more... </a>
 <div id="label717" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_value</span> <b>(Alias name: power-value)</b>  Radio eirp power in dbm (1 - 33, default = 27). <span class="li-normal">type: int</span>
 <a id='label718' href="javascript:ContentClick('label719', 'label718');" onmouseover="ContentPreview('label719');" onmouseout="ContentUnpreview('label719');" title="click to collapse or expand..."> more... </a>
 <div id="label719" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_bssid</span> <b>(Alias name: sam-bssid)</b>  Bssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label720' href="javascript:ContentClick('label721', 'label720');" onmouseover="ContentPreview('label721');" onmouseout="ContentUnpreview('label721');" title="click to collapse or expand..."> more... </a>
 <div id="label721" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_captive_portal</span> <b>(Alias name: sam-captive-portal)</b>  Enable/disable captive portal authentication (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label722' href="javascript:ContentClick('label723', 'label722');" onmouseover="ContentPreview('label723');" onmouseout="ContentUnpreview('label723');" title="click to collapse or expand..."> more... </a>
 <div id="label723" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_password</span> <b>(Alias name: sam-password)</b>  Passphrase for wifi network connection. <span class="li-normal">type: list</span>
 <a id='label724' href="javascript:ContentClick('label725', 'label724');" onmouseover="ContentPreview('label725');" onmouseout="ContentUnpreview('label725');" title="click to collapse or expand..."> more... </a>
 <div id="label725" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_report_intv</span> <b>(Alias name: sam-report-intv)</b>  Sam report interval (sec), 0 for a one-time report. <span class="li-normal">type: int</span>
 <a id='label726' href="javascript:ContentClick('label727', 'label726');" onmouseover="ContentPreview('label727');" onmouseout="ContentUnpreview('label727');" title="click to collapse or expand..."> more... </a>
 <div id="label727" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_security_type</span> <b>(Alias name: sam-security-type)</b>  Select wifi network security type (default = wpa-personal). <span class="li-normal">type: str</span> <span class="li-normal">choices: [open, wpa-personal, wpa-enterprise, owe, wpa3-sae]</span> 
 <a id='label728' href="javascript:ContentClick('label729', 'label728');" onmouseover="ContentPreview('label729');" onmouseout="ContentUnpreview('label729');" title="click to collapse or expand..."> more... </a>
 <div id="label729" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server</span> <b>(Alias name: sam-server)</b>  Sam test server ip address or domain name. <span class="li-normal">type: str</span>
 <a id='label730' href="javascript:ContentClick('label731', 'label730');" onmouseover="ContentPreview('label731');" onmouseout="ContentUnpreview('label731');" title="click to collapse or expand..."> more... </a>
 <div id="label731" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ssid</span> <b>(Alias name: sam-ssid)</b>  Ssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label732' href="javascript:ContentClick('label733', 'label732');" onmouseover="ContentPreview('label733');" onmouseout="ContentUnpreview('label733');" title="click to collapse or expand..."> more... </a>
 <div id="label733" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_test</span> <b>(Alias name: sam-test)</b>  Select sam test type (default = ping). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ping, iperf]</span> 
 <a id='label734' href="javascript:ContentClick('label735', 'label734');" onmouseover="ContentPreview('label735');" onmouseout="ContentUnpreview('label735');" title="click to collapse or expand..."> more... </a>
 <div id="label735" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_username</span> <b>(Alias name: sam-username)</b>  Username for wifi network connection. <span class="li-normal">type: str</span>
 <a id='label736' href="javascript:ContentClick('label737', 'label736');" onmouseover="ContentPreview('label737');" onmouseout="ContentUnpreview('label737');" title="click to collapse or expand..."> more... </a>
 <div id="label737" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">arrp_profile</span> <b>(Alias name: arrp-profile)</b>  Distributed automatic radio resource provisioning (darrp) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label738' href="javascript:ContentClick('label739', 'label738');" onmouseover="ContentPreview('label739');" onmouseout="ContentUnpreview('label739');" title="click to collapse or expand..."> more... </a>
 <div id="label739" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color_mode</span> <b>(Alias name: bss-color-mode)</b>  Bss color mode for this 11ax radio (default = auto). <span class="li-normal">type: str</span> <span class="li-normal">choices: [auto, static]</span> 
 <a id='label740' href="javascript:ContentClick('label741', 'label740');" onmouseover="ContentPreview('label741');" onmouseout="ContentUnpreview('label741');" title="click to collapse or expand..."> more... </a>
 <div id="label741" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_failure_string</span> <b>(Alias name: sam-cwp-failure-string)</b>  Failure identification on the page after an incorrect login. <span class="li-normal">type: str</span>
 <a id='label742' href="javascript:ContentClick('label743', 'label742');" onmouseover="ContentPreview('label743');" onmouseout="ContentUnpreview('label743');" title="click to collapse or expand..."> more... </a>
 <div id="label743" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_match_string</span> <b>(Alias name: sam-cwp-match-string)</b>  Identification string from the captive portal login form. <span class="li-normal">type: str</span>
 <a id='label744' href="javascript:ContentClick('label745', 'label744');" onmouseover="ContentPreview('label745');" onmouseout="ContentUnpreview('label745');" title="click to collapse or expand..."> more... </a>
 <div id="label745" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_password</span> <b>(Alias name: sam-cwp-password)</b>  Password for captive portal authentication. <span class="li-normal">type: list</span>
 <a id='label746' href="javascript:ContentClick('label747', 'label746');" onmouseover="ContentPreview('label747');" onmouseout="ContentUnpreview('label747');" title="click to collapse or expand..."> more... </a>
 <div id="label747" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_success_string</span> <b>(Alias name: sam-cwp-success-string)</b>  Success identification on the page after a successful login. <span class="li-normal">type: str</span>
 <a id='label748' href="javascript:ContentClick('label749', 'label748');" onmouseover="ContentPreview('label749');" onmouseout="ContentUnpreview('label749');" title="click to collapse or expand..."> more... </a>
 <div id="label749" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_test_url</span> <b>(Alias name: sam-cwp-test-url)</b>  Website the client is trying to access. <span class="li-normal">type: str</span>
 <a id='label750' href="javascript:ContentClick('label751', 'label750');" onmouseover="ContentPreview('label751');" onmouseout="ContentUnpreview('label751');" title="click to collapse or expand..."> more... </a>
 <div id="label751" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_username</span> <b>(Alias name: sam-cwp-username)</b>  Username for captive portal authentication. <span class="li-normal">type: str</span>
 <a id='label752' href="javascript:ContentClick('label753', 'label752');" onmouseover="ContentPreview('label753');" onmouseout="ContentUnpreview('label753');" title="click to collapse or expand..."> more... </a>
 <div id="label753" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_fqdn</span> <b>(Alias name: sam-server-fqdn)</b>  Sam test server domain name. <span class="li-normal">type: str</span>
 <a id='label754' href="javascript:ContentClick('label755', 'label754');" onmouseover="ContentPreview('label755');" onmouseout="ContentUnpreview('label755');" title="click to collapse or expand..."> more... </a>
 <div id="label755" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_ip</span> <b>(Alias name: sam-server-ip)</b>  Sam test server ip address. <span class="li-normal">type: str</span>
 <a id='label756' href="javascript:ContentClick('label757', 'label756');" onmouseover="ContentPreview('label757');" onmouseout="ContentUnpreview('label757');" title="click to collapse or expand..."> more... </a>
 <div id="label757" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_type</span> <b>(Alias name: sam-server-type)</b>  Select sam server type (default = ip). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ip, fqdn]</span> 
 <a id='label758' href="javascript:ContentClick('label759', 'label758');" onmouseover="ContentPreview('label759');" onmouseout="ContentUnpreview('label759');" title="click to collapse or expand..."> more... </a>
 <div id="label759" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211d</span> <b>(Alias name: 80211d)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label760' href="javascript:ContentClick('label761', 'label760');" onmouseover="ContentPreview('label761');" onmouseout="ContentUnpreview('label761');" title="click to collapse or expand..."> more... </a>
 <div id="label761" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna</span> <b>(Alias name: optional-antenna)</b>  Optional antenna used on fap (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, FANT-04ABGN-8065-P-N, FANT-04ABGN-0606-O-R, FANT-04ABGN-0606-P-R, FANT-10ACAX-1213-D-N, FANT-08ABGN-1213-D-R, custom]</span> 
 <a id='label762' href="javascript:ContentClick('label763', 'label762');" onmouseover="ContentPreview('label763');" onmouseout="ContentUnpreview('label763');" title="click to collapse or expand..."> more... </a>
 <div id="label763" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mimo_mode</span> <b>(Alias name: mimo-mode)</b>  Configure radio mimo mode (default = default). <span class="li-normal">type: str</span> <span class="li-normal">choices: [default, 1x1, 2x2, 3x3, 4x4, 8x8]</span> 
 <a id='label764' href="javascript:ContentClick('label765', 'label764');" onmouseover="ContentPreview('label765');" onmouseout="ContentUnpreview('label765');" title="click to collapse or expand..."> more... </a>
 <div id="label765" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna_gain</span> <b>(Alias name: optional-antenna-gain)</b>  Optional antenna gain in dbi (0 to 20, default = 0). <span class="li-normal">type: str</span>
 <a id='label766' href="javascript:ContentClick('label767', 'label766');" onmouseover="ContentPreview('label767');" onmouseout="ContentUnpreview('label767');" title="click to collapse or expand..."> more... </a>
 <div id="label767" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ca_certificate</span> <b>(Alias name: sam-ca-certificate)</b>  Ca certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label768' href="javascript:ContentClick('label769', 'label768');" onmouseover="ContentPreview('label769');" onmouseout="ContentUnpreview('label769');" title="click to collapse or expand..."> more... </a>
 <div id="label769" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_client_certificate</span> <b>(Alias name: sam-client-certificate)</b>  Client certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label770' href="javascript:ContentClick('label771', 'label770');" onmouseover="ContentPreview('label771');" onmouseout="ContentUnpreview('label771');" title="click to collapse or expand..."> more... </a>
 <div id="label771" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_eap_method</span> <b>(Alias name: sam-eap-method)</b>  Select wpa2/wpa3-enterprise eap method (default = peap). <span class="li-normal">type: str</span> <span class="li-normal">choices: [tls, peap, both]</span> 
 <a id='label772' href="javascript:ContentClick('label773', 'label772');" onmouseover="ContentPreview('label773');" onmouseout="ContentUnpreview('label773');" title="click to collapse or expand..."> more... </a>
 <div id="label773" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key</span> <b>(Alias name: sam-private-key)</b>  Private key for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label774' href="javascript:ContentClick('label775', 'label774');" onmouseover="ContentPreview('label775');" onmouseout="ContentUnpreview('label775');" title="click to collapse or expand..."> more... </a>
 <div id="label775" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key_password</span> <b>(Alias name: sam-private-key-password)</b>  Password for private key file for wpa2/wpa3-enterprise. <span class="li-normal">type: list</span>
 <a id='label776' href="javascript:ContentClick('label777', 'label776');" onmouseover="ContentPreview('label777');" onmouseout="ContentUnpreview('label777');" title="click to collapse or expand..."> more... </a>
 <div id="label777" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding_ext</span> <b>(Alias name: channel-bonding-ext)</b>  Channel bandwidth extension: 320 mhz-1 and 320 mhz-2 (default = 320 mhz-2). <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz-1, 320MHz-2]</span> 
 <a id='label778' href="javascript:ContentClick('label779', 'label778');" onmouseover="ContentPreview('label779');" onmouseout="ContentUnpreview('label779');" title="click to collapse or expand..."> more... </a>
 <div id="label779" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211mc</span> <b>(Alias name: 80211mc)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label780' href="javascript:ContentClick('label781', 'label780');" onmouseover="ContentPreview('label781');" onmouseout="ContentUnpreview('label781');" title="click to collapse or expand..."> more... </a>
 <div id="label781" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan_width</span> <b>(Alias name: ap-sniffer-chan-width)</b>  Channel bandwidth for sniffer. <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz, 240MHz, 160MHz, 80MHz, 40MHz, 20MHz]</span> 
 <a id='label782' href="javascript:ContentClick('label783', 'label782');" onmouseover="ContentPreview('label783');" onmouseout="ContentUnpreview('label783');" title="click to collapse or expand..."> more... </a>
 <div id="label783" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">radio_4</span> <b>(Alias name: radio-4)</b>  Radio 4. <span class="li-normal">type: dict</span>
 <a id='label784' href="javascript:ContentClick('label785', 'label784');" onmouseover="ContentPreview('label785');" onmouseout="ContentUnpreview('label785');" title="click to collapse or expand..."> more... </a>
 <div id="label785" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">airtime_fairness</span> <b>(Alias name: airtime-fairness)</b>  Enable/disable airtime fairness (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label786' href="javascript:ContentClick('label787', 'label786');" onmouseover="ContentPreview('label787');" onmouseout="ContentUnpreview('label787');" title="click to collapse or expand..."> more... </a>
 <div id="label787" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">amsdu</span> Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label788' href="javascript:ContentClick('label789', 'label788');" onmouseover="ContentPreview('label789');" onmouseout="ContentUnpreview('label789');" title="click to collapse or expand..."> more... </a>
 <div id="label789" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_addr</span> <b>(Alias name: ap-sniffer-addr)</b>  Mac address to monitor. <span class="li-normal">type: str</span>
 <a id='label790' href="javascript:ContentClick('label791', 'label790');" onmouseover="ContentPreview('label791');" onmouseout="ContentUnpreview('label791');" title="click to collapse or expand..."> more... </a>
 <div id="label791" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_bufsize</span> <b>(Alias name: ap-sniffer-bufsize)</b>  Sniffer buffer size (1 - 32 mb, default = 16). <span class="li-normal">type: int</span>
 <a id='label792' href="javascript:ContentClick('label793', 'label792');" onmouseover="ContentPreview('label793');" onmouseout="ContentUnpreview('label793');" title="click to collapse or expand..."> more... </a>
 <div id="label793" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan</span> <b>(Alias name: ap-sniffer-chan)</b>  Channel on which to operate the sniffer (default = 6). <span class="li-normal">type: int</span>
 <a id='label794' href="javascript:ContentClick('label795', 'label794');" onmouseover="ContentPreview('label795');" onmouseout="ContentUnpreview('label795');" title="click to collapse or expand..."> more... </a>
 <div id="label795" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_ctl</span> <b>(Alias name: ap-sniffer-ctl)</b>  Enable/disable sniffer on wifi control frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label796' href="javascript:ContentClick('label797', 'label796');" onmouseover="ContentPreview('label797');" onmouseout="ContentUnpreview('label797');" title="click to collapse or expand..."> more... </a>
 <div id="label797" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_data</span> <b>(Alias name: ap-sniffer-data)</b>  Enable/disable sniffer on wifi data frame (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label798' href="javascript:ContentClick('label799', 'label798');" onmouseover="ContentPreview('label799');" onmouseout="ContentUnpreview('label799');" title="click to collapse or expand..."> more... </a>
 <div id="label799" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_beacon</span> <b>(Alias name: ap-sniffer-mgmt-beacon)</b>  Enable/disable sniffer on wifi management beacon frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label800' href="javascript:ContentClick('label801', 'label800');" onmouseover="ContentPreview('label801');" onmouseout="ContentUnpreview('label801');" title="click to collapse or expand..."> more... </a>
 <div id="label801" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_other</span> <b>(Alias name: ap-sniffer-mgmt-other)</b>  Enable/disable sniffer on wifi management other frames  (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label802' href="javascript:ContentClick('label803', 'label802');" onmouseover="ContentPreview('label803');" onmouseout="ContentUnpreview('label803');" title="click to collapse or expand..."> more... </a>
 <div id="label803" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_mgmt_probe</span> <b>(Alias name: ap-sniffer-mgmt-probe)</b>  Enable/disable sniffer on wifi management probe frames (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label804' href="javascript:ContentClick('label805', 'label804');" onmouseover="ContentPreview('label805');" onmouseout="ContentUnpreview('label805');" title="click to collapse or expand..."> more... </a>
 <div id="label805" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_high</span> <b>(Alias name: auto-power-high)</b>  The upper bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label806' href="javascript:ContentClick('label807', 'label806');" onmouseover="ContentPreview('label807');" onmouseout="ContentUnpreview('label807');" title="click to collapse or expand..."> more... </a>
 <div id="label807" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_level</span> <b>(Alias name: auto-power-level)</b>  Enable/disable automatic power-level adjustment to prevent co-channel interference (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label808' href="javascript:ContentClick('label809', 'label808');" onmouseover="ContentPreview('label809');" onmouseout="ContentUnpreview('label809');" title="click to collapse or expand..."> more... </a>
 <div id="label809" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_low</span> <b>(Alias name: auto-power-low)</b>  The lower bound of automatic transmit power adjustment in dbm (the actual range of transmit power depends on the ap platform type). <span class="li-normal">type: int</span>
 <a id='label810' href="javascript:ContentClick('label811', 'label810');" onmouseover="ContentPreview('label811');" onmouseout="ContentUnpreview('label811');" title="click to collapse or expand..."> more... </a>
 <div id="label811" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">auto_power_target</span> <b>(Alias name: auto-power-target)</b>  The target of automatic transmit power adjustment in dbm. <span class="li-normal">type: str</span>
 <a id='label812' href="javascript:ContentClick('label813', 'label812');" onmouseover="ContentPreview('label813');" onmouseout="ContentUnpreview('label813');" title="click to collapse or expand..."> more... </a>
 <div id="label813" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band</span> Wifi band that radio 3 operates on. <span class="li-normal">type: str</span> <span class="li-normal">choices: [802.11b, 802.11a, 802.11g, 802.11n, 802.11ac, 802.11n-5G, 802.11ax-5G, 802.11ax, 802.11ac-2G, 802.11g-only, 802.11n-only, 802.11n,g-only, 802.11ac-only, 802.11ac,n-only, 802.11n-5G-only, 802.11ax-5G-only, 802.11ax,ac-only, 802.11ax,ac,n-only, 802.11ax-only, 802.11ax,n-only, 802.11ax,n,g-only, 802.11ax-6G, 802.11n-2G, 802.11ac-5G, 802.11ax-2G, 802.11be-2G, 802.11be-5G, 802.11be-6G]</span> 
 <a id='label814' href="javascript:ContentClick('label815', 'label814');" onmouseover="ContentPreview('label815');" onmouseout="ContentUnpreview('label815');" title="click to collapse or expand..."> more... </a>
 <div id="label815" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">band_5g_type</span> <b>(Alias name: band-5g-type)</b>  Wifi 5g band type. <span class="li-normal">type: str</span> <span class="li-normal">choices: [5g-full, 5g-high, 5g-low]</span> 
 <a id='label816' href="javascript:ContentClick('label817', 'label816');" onmouseover="ContentPreview('label817');" onmouseout="ContentUnpreview('label817');" title="click to collapse or expand..."> more... </a>
 <div id="label817" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_admission_control</span> <b>(Alias name: bandwidth-admission-control)</b>  Enable/disable wifi multimedia (wmm) bandwidth admission control to optimize wifi bandwidth use. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label818' href="javascript:ContentClick('label819', 'label818');" onmouseover="ContentPreview('label819');" onmouseout="ContentUnpreview('label819');" title="click to collapse or expand..."> more... </a>
 <div id="label819" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bandwidth_capacity</span> <b>(Alias name: bandwidth-capacity)</b>  Maximum bandwidth capacity allowed (1 - 600000 kbps, default = 2000). <span class="li-normal">type: int</span>
 <a id='label820' href="javascript:ContentClick('label821', 'label820');" onmouseover="ContentPreview('label821');" onmouseout="ContentUnpreview('label821');" title="click to collapse or expand..."> more... </a>
 <div id="label821" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">beacon_interval</span> <b>(Alias name: beacon-interval)</b>  Beacon interval. <span class="li-normal">type: int</span>
 <a id='label822' href="javascript:ContentClick('label823', 'label822');" onmouseover="ContentPreview('label823');" onmouseout="ContentUnpreview('label823');" title="click to collapse or expand..."> more... </a>
 <div id="label823" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color</span> <b>(Alias name: bss-color)</b>  Bss color value for this 11ax radio (0 - 63, 0 means disable. <span class="li-normal">type: int</span>
 <a id='label824' href="javascript:ContentClick('label825', 'label824');" onmouseover="ContentPreview('label825');" onmouseout="ContentUnpreview('label825');" title="click to collapse or expand..."> more... </a>
 <div id="label825" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_admission_control</span> <b>(Alias name: call-admission-control)</b>  Enable/disable wifi multimedia (wmm) call admission control to optimize wifi bandwidth use for voip calls. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label826' href="javascript:ContentClick('label827', 'label826');" onmouseover="ContentPreview('label827');" onmouseout="ContentUnpreview('label827');" title="click to collapse or expand..."> more... </a>
 <div id="label827" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">call_capacity</span> <b>(Alias name: call-capacity)</b>  Maximum number of voice over wlan (vowlan) phones supported by the radio (0 - 60, default = 10). <span class="li-normal">type: int</span>
 <a id='label828' href="javascript:ContentClick('label829', 'label828');" onmouseover="ContentPreview('label829');" onmouseout="ContentUnpreview('label829');" title="click to collapse or expand..."> more... </a>
 <div id="label829" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel</span> Selected list of wireless radio channels. <span class="li-normal">type: list</span>
 <a id='label830' href="javascript:ContentClick('label831', 'label830');" onmouseover="ContentPreview('label831');" onmouseout="ContentUnpreview('label831');" title="click to collapse or expand..."> more... </a>
 <div id="label831" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding</span> <b>(Alias name: channel-bonding)</b>  Channel bandwidth: 160,80, 40, or 20mhz. <span class="li-normal">type: str</span> <span class="li-normal">choices: [80MHz, 40MHz, 20MHz, 160MHz, 320MHz, 240MHz]</span> 
 <a id='label832' href="javascript:ContentClick('label833', 'label832');" onmouseover="ContentPreview('label833');" onmouseout="ContentUnpreview('label833');" title="click to collapse or expand..."> more... </a>
 <div id="label833" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_utilization</span> <b>(Alias name: channel-utilization)</b>  Enable/disable measuring channel utilization. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label834' href="javascript:ContentClick('label835', 'label834');" onmouseover="ContentPreview('label835');" onmouseout="ContentUnpreview('label835');" title="click to collapse or expand..."> more... </a>
 <div id="label835" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">coexistence</span> Enable/disable allowing both ht20 and ht40 on the same radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label836' href="javascript:ContentClick('label837', 'label836');" onmouseover="ContentPreview('label837');" onmouseout="ContentUnpreview('label837');" title="click to collapse or expand..."> more... </a>
 <div id="label837" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">darrp</span> Enable/disable distributed automatic radio resource provisioning (darrp) to make sure the radio is always using the most optimal channel (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label838' href="javascript:ContentClick('label839', 'label838');" onmouseover="ContentPreview('label839');" onmouseout="ContentUnpreview('label839');" title="click to collapse or expand..."> more... </a>
 <div id="label839" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma</span> Enable/disable dynamic radio mode assignment (drma) (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label840' href="javascript:ContentClick('label841', 'label840');" onmouseover="ContentPreview('label841');" onmouseout="ContentUnpreview('label841');" title="click to collapse or expand..."> more... </a>
 <div id="label841" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">drma_sensitivity</span> <b>(Alias name: drma-sensitivity)</b>  Network coverage factor (ncf) percentage required to consider a radio as redundant (default = low). <span class="li-normal">type: str</span> <span class="li-normal">choices: [low, medium, high]</span> 
 <a id='label842' href="javascript:ContentClick('label843', 'label842');" onmouseover="ContentPreview('label843');" onmouseout="ContentUnpreview('label843');" title="click to collapse or expand..."> more... </a>
 <div id="label843" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">dtim</span> Delivery traffic indication map (dtim) period (1 - 255, default = 1). <span class="li-normal">type: int</span>
 <a id='label844' href="javascript:ContentClick('label845', 'label844');" onmouseover="ContentPreview('label845');" onmouseout="ContentUnpreview('label845');" title="click to collapse or expand..."> more... </a>
 <div id="label845" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frag_threshold</span> <b>(Alias name: frag-threshold)</b>  Maximum packet size that can be sent without fragmentation (800 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label846' href="javascript:ContentClick('label847', 'label846');" onmouseover="ContentPreview('label847');" onmouseout="ContentUnpreview('label847');" title="click to collapse or expand..."> more... </a>
 <div id="label847" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_clients</span> <b>(Alias name: max-clients)</b>  Maximum number of stations (stas) or wifi clients supported by the radio. <span class="li-normal">type: int</span>
 <a id='label848' href="javascript:ContentClick('label849', 'label848');" onmouseover="ContentPreview('label849');" onmouseout="ContentUnpreview('label849');" title="click to collapse or expand..."> more... </a>
 <div id="label849" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">max_distance</span> <b>(Alias name: max-distance)</b>  Maximum expected distance between the ap and clients (0 - 54000 m, default = 0). <span class="li-normal">type: int</span>
 <a id='label850' href="javascript:ContentClick('label851', 'label850');" onmouseover="ContentPreview('label851');" onmouseout="ContentUnpreview('label851');" title="click to collapse or expand..."> more... </a>
 <div id="label851" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mode</span> Mode of radio 3. <span class="li-normal">type: str</span> <span class="li-normal">choices: [ap, monitor, sniffer, disabled, sam]</span> 
 <a id='label852' href="javascript:ContentClick('label853', 'label852');" onmouseover="ContentPreview('label853');" onmouseout="ContentUnpreview('label853');" title="click to collapse or expand..."> more... </a>
 <div id="label853" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_level</span> <b>(Alias name: power-level)</b>  Radio power level as a percentage of the maximum transmit power (0 - 100, default = 100). <span class="li-normal">type: int</span>
 <a id='label854' href="javascript:ContentClick('label855', 'label854');" onmouseover="ContentPreview('label855');" onmouseout="ContentUnpreview('label855');" title="click to collapse or expand..."> more... </a>
 <div id="label855" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">powersave_optimize</span> <b>(Alias name: powersave-optimize)</b>  Enable client power-saving features such as tim, ac vo, and obss etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [tim, ac-vo, no-obss-scan, no-11b-rate, client-rate-follow]</span> 
 <a id='label856' href="javascript:ContentClick('label857', 'label856');" onmouseover="ContentPreview('label857');" onmouseout="ContentUnpreview('label857');" title="click to collapse or expand..."> more... </a>
 <div id="label857" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">protection_mode</span> <b>(Alias name: protection-mode)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [rtscts, ctsonly, disable]</span> 
 <a id='label858' href="javascript:ContentClick('label859', 'label858');" onmouseover="ContentPreview('label859');" onmouseout="ContentUnpreview('label859');" title="click to collapse or expand..."> more... </a>
 <div id="label859" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">radio_id</span> <b>(Alias name: radio-id)</b>  Radio id. <span class="li-normal">type: int</span>
 <a id='label860' href="javascript:ContentClick('label861', 'label860');" onmouseover="ContentPreview('label861');" onmouseout="ContentUnpreview('label861');" title="click to collapse or expand..."> more... </a>
 <div id="label861" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">rts_threshold</span> <b>(Alias name: rts-threshold)</b>  Maximum packet size for rts transmissions, specifying the maximum size of a data packet before rts/cts (256 - 2346 bytes, default = 2346). <span class="li-normal">type: int</span>
 <a id='label862' href="javascript:ContentClick('label863', 'label862');" onmouseover="ContentPreview('label863');" onmouseout="ContentUnpreview('label863');" title="click to collapse or expand..."> more... </a>
 <div id="label863" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">short_guard_interval</span> <b>(Alias name: short-guard-interval)</b>  Use either the short guard interval (short gi) of 400 ns or the long guard interval (long gi) of 800 ns. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label864' href="javascript:ContentClick('label865', 'label864');" onmouseover="ContentPreview('label865');" onmouseout="ContentUnpreview('label865');" title="click to collapse or expand..."> more... </a>
 <div id="label865" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">spectrum_analysis</span> <b>(Alias name: spectrum-analysis)</b>  Enable/disable spectrum analysis to find interference that would negatively impact wireless performance. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, scan-only]</span> 
 <a id='label866' href="javascript:ContentClick('label867', 'label866');" onmouseover="ContentPreview('label867');" onmouseout="ContentUnpreview('label867');" title="click to collapse or expand..."> more... </a>
 <div id="label867" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">transmit_optimize</span> <b>(Alias name: transmit-optimize)</b>  Packet transmission optimization options including power saving, aggregation limiting, retry limiting, etc. <span class="li-normal">type: list</span> <span class="li-normal">choices: [disable, power-save, aggr-limit, retry-limit, send-bar]</span> 
 <a id='label868' href="javascript:ContentClick('label869', 'label868');" onmouseover="ContentPreview('label869');" onmouseout="ContentUnpreview('label869');" title="click to collapse or expand..."> more... </a>
 <div id="label869" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap_all</span> <b>(Alias name: vap-all)</b>  Configure method for assigning ssids to this fortiap (default = automatically assign tunnel ssids). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, tunnel, bridge, manual]</span> 
 <a id='label870' href="javascript:ContentClick('label871', 'label870');" onmouseover="ContentPreview('label871');" onmouseout="ContentUnpreview('label871');" title="click to collapse or expand..."> more... </a>
 <div id="label871" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap1</span> Virtual access point (vap) for wlan id 1 <span class="li-normal">type: str</span>
 <a id='label872' href="javascript:ContentClick('label873', 'label872');" onmouseover="ContentPreview('label873');" onmouseout="ContentUnpreview('label873');" title="click to collapse or expand..."> more... </a>
 <div id="label873" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap2</span> Virtual access point (vap) for wlan id 2 <span class="li-normal">type: str</span>
 <a id='label874' href="javascript:ContentClick('label875', 'label874');" onmouseover="ContentPreview('label875');" onmouseout="ContentUnpreview('label875');" title="click to collapse or expand..."> more... </a>
 <div id="label875" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap3</span> Virtual access point (vap) for wlan id 3 <span class="li-normal">type: str</span>
 <a id='label876' href="javascript:ContentClick('label877', 'label876');" onmouseover="ContentPreview('label877');" onmouseout="ContentUnpreview('label877');" title="click to collapse or expand..."> more... </a>
 <div id="label877" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap4</span> Virtual access point (vap) for wlan id 4 <span class="li-normal">type: str</span>
 <a id='label878' href="javascript:ContentClick('label879', 'label878');" onmouseover="ContentPreview('label879');" onmouseout="ContentUnpreview('label879');" title="click to collapse or expand..."> more... </a>
 <div id="label879" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap5</span> Virtual access point (vap) for wlan id 5 <span class="li-normal">type: str</span>
 <a id='label880' href="javascript:ContentClick('label881', 'label880');" onmouseover="ContentPreview('label881');" onmouseout="ContentUnpreview('label881');" title="click to collapse or expand..."> more... </a>
 <div id="label881" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap6</span> Virtual access point (vap) for wlan id 6 <span class="li-normal">type: str</span>
 <a id='label882' href="javascript:ContentClick('label883', 'label882');" onmouseover="ContentPreview('label883');" onmouseout="ContentUnpreview('label883');" title="click to collapse or expand..."> more... </a>
 <div id="label883" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap7</span> Virtual access point (vap) for wlan id 7 <span class="li-normal">type: str</span>
 <a id='label884' href="javascript:ContentClick('label885', 'label884');" onmouseover="ContentPreview('label885');" onmouseout="ContentUnpreview('label885');" title="click to collapse or expand..."> more... </a>
 <div id="label885" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vap8</span> Virtual access point (vap) for wlan id 8 <span class="li-normal">type: str</span>
 <a id='label886' href="javascript:ContentClick('label887', 'label886');" onmouseover="ContentPreview('label887');" onmouseout="ContentUnpreview('label887');" title="click to collapse or expand..."> more... </a>
 <div id="label887" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">vaps</span> Manually selected list of virtual access points (vaps). <span class="li-normal">type: list or str</span>
 <a id='label888' href="javascript:ContentClick('label889', 'label888');" onmouseover="ContentPreview('label889');" onmouseout="ContentUnpreview('label889');" title="click to collapse or expand..."> more... </a>
 <div id="label889" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wids_profile</span> <b>(Alias name: wids-profile)</b>  Wireless intrusion detection system (wids) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label890' href="javascript:ContentClick('label891', 'label890');" onmouseover="ContentPreview('label891');" onmouseout="ContentUnpreview('label891');" title="click to collapse or expand..."> more... </a>
 <div id="label891" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">zero_wait_dfs</span> <b>(Alias name: zero-wait-dfs)</b>  Enable/disable zero wait dfs on radio (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label892' href="javascript:ContentClick('label893', 'label892');" onmouseover="ContentPreview('label893');" onmouseout="ContentUnpreview('label893');" title="click to collapse or expand..."> more... </a>
 <div id="label893" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">frequency_handoff</span> <b>(Alias name: frequency-handoff)</b>  Enable/disable frequency handoff of clients to other channels (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label894' href="javascript:ContentClick('label895', 'label894');" onmouseover="ContentPreview('label895');" onmouseout="ContentUnpreview('label895');" title="click to collapse or expand..."> more... </a>
 <div id="label895" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_handoff</span> <b>(Alias name: ap-handoff)</b>  Enable/disable ap handoff of clients to other aps (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label896' href="javascript:ContentClick('label897', 'label896');" onmouseover="ContentPreview('label897');" onmouseout="ContentUnpreview('label897');" title="click to collapse or expand..."> more... </a>
 <div id="label897" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.8 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.5 -> v7.6.2</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_protocol</span> <b>(Alias name: iperf-protocol)</b>  Iperf test protocol (default = udp). <span class="li-normal">type: str</span> <span class="li-normal">choices: [udp, tcp]</span> 
 <a id='label898' href="javascript:ContentClick('label899', 'label898');" onmouseover="ContentPreview('label899');" onmouseout="ContentUnpreview('label899');" title="click to collapse or expand..."> more... </a>
 <div id="label899" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">iperf_server_port</span> <b>(Alias name: iperf-server-port)</b>  Iperf service port number. <span class="li-normal">type: int</span>
 <a id='label900' href="javascript:ContentClick('label901', 'label900');" onmouseover="ContentPreview('label901');" onmouseout="ContentUnpreview('label901');" title="click to collapse or expand..."> more... </a>
 <div id="label901" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_mode</span> <b>(Alias name: power-mode)</b>  Set radio effective isotropic radiated power (eirp) in dbm or by a percentage of the maximum eirp (default = percentage). <span class="li-normal">type: str</span> <span class="li-normal">choices: [dBm, percentage]</span> 
 <a id='label902' href="javascript:ContentClick('label903', 'label902');" onmouseover="ContentPreview('label903');" onmouseout="ContentUnpreview('label903');" title="click to collapse or expand..."> more... </a>
 <div id="label903" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">power_value</span> <b>(Alias name: power-value)</b>  Radio eirp power in dbm (1 - 33, default = 27). <span class="li-normal">type: int</span>
 <a id='label904' href="javascript:ContentClick('label905', 'label904');" onmouseover="ContentPreview('label905');" onmouseout="ContentUnpreview('label905');" title="click to collapse or expand..."> more... </a>
 <div id="label905" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_bssid</span> <b>(Alias name: sam-bssid)</b>  Bssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label906' href="javascript:ContentClick('label907', 'label906');" onmouseover="ContentPreview('label907');" onmouseout="ContentUnpreview('label907');" title="click to collapse or expand..."> more... </a>
 <div id="label907" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_captive_portal</span> <b>(Alias name: sam-captive-portal)</b>  Enable/disable captive portal authentication (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label908' href="javascript:ContentClick('label909', 'label908');" onmouseover="ContentPreview('label909');" onmouseout="ContentUnpreview('label909');" title="click to collapse or expand..."> more... </a>
 <div id="label909" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_password</span> <b>(Alias name: sam-password)</b>  Passphrase for wifi network connection. <span class="li-normal">type: list</span>
 <a id='label910' href="javascript:ContentClick('label911', 'label910');" onmouseover="ContentPreview('label911');" onmouseout="ContentUnpreview('label911');" title="click to collapse or expand..."> more... </a>
 <div id="label911" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_report_intv</span> <b>(Alias name: sam-report-intv)</b>  Sam report interval (sec), 0 for a one-time report. <span class="li-normal">type: int</span>
 <a id='label912' href="javascript:ContentClick('label913', 'label912');" onmouseover="ContentPreview('label913');" onmouseout="ContentUnpreview('label913');" title="click to collapse or expand..."> more... </a>
 <div id="label913" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_security_type</span> <b>(Alias name: sam-security-type)</b>  Select wifi network security type (default = wpa-personal). <span class="li-normal">type: str</span> <span class="li-normal">choices: [open, wpa-personal, wpa-enterprise, owe, wpa3-sae]</span> 
 <a id='label914' href="javascript:ContentClick('label915', 'label914');" onmouseover="ContentPreview('label915');" onmouseout="ContentUnpreview('label915');" title="click to collapse or expand..."> more... </a>
 <div id="label915" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server</span> <b>(Alias name: sam-server)</b>  Sam test server ip address or domain name. <span class="li-normal">type: str</span>
 <a id='label916' href="javascript:ContentClick('label917', 'label916');" onmouseover="ContentPreview('label917');" onmouseout="ContentUnpreview('label917');" title="click to collapse or expand..."> more... </a>
 <div id="label917" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ssid</span> <b>(Alias name: sam-ssid)</b>  Ssid for wifi network. <span class="li-normal">type: str</span>
 <a id='label918' href="javascript:ContentClick('label919', 'label918');" onmouseover="ContentPreview('label919');" onmouseout="ContentUnpreview('label919');" title="click to collapse or expand..."> more... </a>
 <div id="label919" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_test</span> <b>(Alias name: sam-test)</b>  Select sam test type (default = ping). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ping, iperf]</span> 
 <a id='label920' href="javascript:ContentClick('label921', 'label920');" onmouseover="ContentPreview('label921');" onmouseout="ContentUnpreview('label921');" title="click to collapse or expand..."> more... </a>
 <div id="label921" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_username</span> <b>(Alias name: sam-username)</b>  Username for wifi network connection. <span class="li-normal">type: str</span>
 <a id='label922' href="javascript:ContentClick('label923', 'label922');" onmouseover="ContentPreview('label923');" onmouseout="ContentUnpreview('label923');" title="click to collapse or expand..."> more... </a>
 <div id="label923" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">arrp_profile</span> <b>(Alias name: arrp-profile)</b>  Distributed automatic radio resource provisioning (darrp) profile name to assign to the radio. <span class="li-normal">type: str</span>
 <a id='label924' href="javascript:ContentClick('label925', 'label924');" onmouseover="ContentPreview('label925');" onmouseout="ContentUnpreview('label925');" title="click to collapse or expand..."> more... </a>
 <div id="label925" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bss_color_mode</span> <b>(Alias name: bss-color-mode)</b>  Bss color mode for this 11ax radio (default = auto). <span class="li-normal">type: str</span> <span class="li-normal">choices: [auto, static]</span> 
 <a id='label926' href="javascript:ContentClick('label927', 'label926');" onmouseover="ContentPreview('label927');" onmouseout="ContentUnpreview('label927');" title="click to collapse or expand..."> more... </a>
 <div id="label927" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_failure_string</span> <b>(Alias name: sam-cwp-failure-string)</b>  Failure identification on the page after an incorrect login. <span class="li-normal">type: str</span>
 <a id='label928' href="javascript:ContentClick('label929', 'label928');" onmouseover="ContentPreview('label929');" onmouseout="ContentUnpreview('label929');" title="click to collapse or expand..."> more... </a>
 <div id="label929" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_match_string</span> <b>(Alias name: sam-cwp-match-string)</b>  Identification string from the captive portal login form. <span class="li-normal">type: str</span>
 <a id='label930' href="javascript:ContentClick('label931', 'label930');" onmouseover="ContentPreview('label931');" onmouseout="ContentUnpreview('label931');" title="click to collapse or expand..."> more... </a>
 <div id="label931" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_password</span> <b>(Alias name: sam-cwp-password)</b>  Password for captive portal authentication. <span class="li-normal">type: list</span>
 <a id='label932' href="javascript:ContentClick('label933', 'label932');" onmouseover="ContentPreview('label933');" onmouseout="ContentUnpreview('label933');" title="click to collapse or expand..."> more... </a>
 <div id="label933" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_success_string</span> <b>(Alias name: sam-cwp-success-string)</b>  Success identification on the page after a successful login. <span class="li-normal">type: str</span>
 <a id='label934' href="javascript:ContentClick('label935', 'label934');" onmouseover="ContentPreview('label935');" onmouseout="ContentUnpreview('label935');" title="click to collapse or expand..."> more... </a>
 <div id="label935" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_test_url</span> <b>(Alias name: sam-cwp-test-url)</b>  Website the client is trying to access. <span class="li-normal">type: str</span>
 <a id='label936' href="javascript:ContentClick('label937', 'label936');" onmouseover="ContentPreview('label937');" onmouseout="ContentUnpreview('label937');" title="click to collapse or expand..."> more... </a>
 <div id="label937" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_cwp_username</span> <b>(Alias name: sam-cwp-username)</b>  Username for captive portal authentication. <span class="li-normal">type: str</span>
 <a id='label938' href="javascript:ContentClick('label939', 'label938');" onmouseover="ContentPreview('label939');" onmouseout="ContentUnpreview('label939');" title="click to collapse or expand..."> more... </a>
 <div id="label939" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_fqdn</span> <b>(Alias name: sam-server-fqdn)</b>  Sam test server domain name. <span class="li-normal">type: str</span>
 <a id='label940' href="javascript:ContentClick('label941', 'label940');" onmouseover="ContentPreview('label941');" onmouseout="ContentUnpreview('label941');" title="click to collapse or expand..."> more... </a>
 <div id="label941" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_ip</span> <b>(Alias name: sam-server-ip)</b>  Sam test server ip address. <span class="li-normal">type: str</span>
 <a id='label942' href="javascript:ContentClick('label943', 'label942');" onmouseover="ContentPreview('label943');" onmouseout="ContentUnpreview('label943');" title="click to collapse or expand..."> more... </a>
 <div id="label943" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_server_type</span> <b>(Alias name: sam-server-type)</b>  Select sam server type (default = ip). <span class="li-normal">type: str</span> <span class="li-normal">choices: [ip, fqdn]</span> 
 <a id='label944' href="javascript:ContentClick('label945', 'label944');" onmouseover="ContentPreview('label945');" onmouseout="ContentUnpreview('label945');" title="click to collapse or expand..."> more... </a>
 <div id="label945" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211d</span> <b>(Alias name: 80211d)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label946' href="javascript:ContentClick('label947', 'label946');" onmouseover="ContentPreview('label947');" onmouseout="ContentUnpreview('label947');" title="click to collapse or expand..."> more... </a>
 <div id="label947" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna</span> <b>(Alias name: optional-antenna)</b>  Optional antenna used on fap (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, FANT-04ABGN-8065-P-N, FANT-04ABGN-0606-O-R, FANT-04ABGN-0606-P-R, FANT-10ACAX-1213-D-N, FANT-08ABGN-1213-D-R, custom]</span> 
 <a id='label948' href="javascript:ContentClick('label949', 'label948');" onmouseover="ContentPreview('label949');" onmouseout="ContentUnpreview('label949');" title="click to collapse or expand..."> more... </a>
 <div id="label949" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.2.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">mimo_mode</span> <b>(Alias name: mimo-mode)</b>  Configure radio mimo mode (default = default). <span class="li-normal">type: str</span> <span class="li-normal">choices: [default, 1x1, 2x2, 3x3, 4x4, 8x8]</span> 
 <a id='label950' href="javascript:ContentClick('label951', 'label950');" onmouseover="ContentPreview('label951');" onmouseout="ContentUnpreview('label951');" title="click to collapse or expand..."> more... </a>
 <div id="label951" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">optional_antenna_gain</span> <b>(Alias name: optional-antenna-gain)</b>  Optional antenna gain in dbi (0 to 20, default = 0). <span class="li-normal">type: str</span>
 <a id='label952' href="javascript:ContentClick('label953', 'label952');" onmouseover="ContentPreview('label953');" onmouseout="ContentUnpreview('label953');" title="click to collapse or expand..."> more... </a>
 <div id="label953" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_ca_certificate</span> <b>(Alias name: sam-ca-certificate)</b>  Ca certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label954' href="javascript:ContentClick('label955', 'label954');" onmouseover="ContentPreview('label955');" onmouseout="ContentUnpreview('label955');" title="click to collapse or expand..."> more... </a>
 <div id="label955" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_client_certificate</span> <b>(Alias name: sam-client-certificate)</b>  Client certificate for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label956' href="javascript:ContentClick('label957', 'label956');" onmouseover="ContentPreview('label957');" onmouseout="ContentUnpreview('label957');" title="click to collapse or expand..."> more... </a>
 <div id="label957" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_eap_method</span> <b>(Alias name: sam-eap-method)</b>  Select wpa2/wpa3-enterprise eap method (default = peap). <span class="li-normal">type: str</span> <span class="li-normal">choices: [tls, peap, both]</span> 
 <a id='label958' href="javascript:ContentClick('label959', 'label958');" onmouseover="ContentPreview('label959');" onmouseout="ContentUnpreview('label959');" title="click to collapse or expand..."> more... </a>
 <div id="label959" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key</span> <b>(Alias name: sam-private-key)</b>  Private key for wpa2/wpa3-enterprise. <span class="li-normal">type: str</span>
 <a id='label960' href="javascript:ContentClick('label961', 'label960');" onmouseover="ContentPreview('label961');" onmouseout="ContentUnpreview('label961');" title="click to collapse or expand..."> more... </a>
 <div id="label961" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">sam_private_key_password</span> <b>(Alias name: sam-private-key-password)</b>  Password for private key file for wpa2/wpa3-enterprise. <span class="li-normal">type: list</span>
 <a id='label962' href="javascript:ContentClick('label963', 'label962');" onmouseover="ContentPreview('label963');" onmouseout="ContentUnpreview('label963');" title="click to collapse or expand..."> more... </a>
 <div id="label963" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">channel_bonding_ext</span> <b>(Alias name: channel-bonding-ext)</b>  Channel bandwidth extension: 320 mhz-1 and 320 mhz-2 (default = 320 mhz-2). <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz-1, 320MHz-2]</span> 
 <a id='label964' href="javascript:ContentClick('label965', 'label964');" onmouseover="ContentPreview('label965');" onmouseout="ContentUnpreview('label965');" title="click to collapse or expand..."> more... </a>
 <div id="label965" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">d80211mc</span> <b>(Alias name: 80211mc)</b>  Enable/disable 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label966' href="javascript:ContentClick('label967', 'label966');" onmouseover="ContentPreview('label967');" onmouseout="ContentUnpreview('label967');" title="click to collapse or expand..."> more... </a>
 <div id="label967" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">ap_sniffer_chan_width</span> <b>(Alias name: ap-sniffer-chan-width)</b>  Channel bandwidth for sniffer. <span class="li-normal">type: str</span> <span class="li-normal">choices: [320MHz, 240MHz, 160MHz, 80MHz, 40MHz, 20MHz]</span> 
 <a id='label968' href="javascript:ContentClick('label969', 'label968');" onmouseover="ContentPreview('label969');" onmouseout="ContentUnpreview('label969');" title="click to collapse or expand..."> more... </a>
 <div id="label969" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.4 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">console_login</span> <b>(Alias name: console-login)</b>  Enable/disable fortiap console login access (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label970' href="javascript:ContentClick('label971', 'label970');" onmouseover="ContentPreview('label971');" onmouseout="ContentUnpreview('label971');" title="click to collapse or expand..."> more... </a>
 <div id="label971" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v6.2.9 -> v6.2.13</code>, <code class="docutils literal notranslate">v6.4.8 -> v6.4.15</code>, <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">esl_ses_dongle</span> <b>(Alias name: esl-ses-dongle)</b>  Esl ses dongle. <span class="li-normal">type: dict</span>
 <a id='label972' href="javascript:ContentClick('label973', 'label972');" onmouseover="ContentPreview('label973');" onmouseout="ContentUnpreview('label973');" title="click to collapse or expand..."> more... </a>
 <div id="label973" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 <ul class="ul-self">
 <li><span class="li-head">apc_addr_type</span> <b>(Alias name: apc-addr-type)</b>  Esl ses-imagotag apc address type (default = fqdn). <span class="li-normal">type: str</span> <span class="li-normal">choices: [fqdn, ip]</span> 
 <a id='label974' href="javascript:ContentClick('label975', 'label974');" onmouseover="ContentPreview('label975');" onmouseout="ContentUnpreview('label975');" title="click to collapse or expand..."> more... </a>
 <div id="label975" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">apc_fqdn</span> <b>(Alias name: apc-fqdn)</b>  Fqdn of esl ses-imagotag access point controller (apc). <span class="li-normal">type: str</span>
 <a id='label976' href="javascript:ContentClick('label977', 'label976');" onmouseover="ContentPreview('label977');" onmouseout="ContentUnpreview('label977');" title="click to collapse or expand..."> more... </a>
 <div id="label977" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">apc_ip</span> <b>(Alias name: apc-ip)</b>  Ip address of esl ses-imagotag access point controller (apc). <span class="li-normal">type: str</span>
 <a id='label978' href="javascript:ContentClick('label979', 'label978');" onmouseover="ContentPreview('label979');" onmouseout="ContentUnpreview('label979');" title="click to collapse or expand..."> more... </a>
 <div id="label979" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">apc_port</span> <b>(Alias name: apc-port)</b>  Port of esl ses-imagotag access point controller (apc). <span class="li-normal">type: int</span>
 <a id='label980' href="javascript:ContentClick('label981', 'label980');" onmouseover="ContentPreview('label981');" onmouseout="ContentUnpreview('label981');" title="click to collapse or expand..."> more... </a>
 <div id="label981" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">coex_level</span> <b>(Alias name: coex-level)</b>  Esl ses-imagotag dongle coexistence level (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none]</span> 
 <a id='label982' href="javascript:ContentClick('label983', 'label982');" onmouseover="ContentPreview('label983');" onmouseout="ContentUnpreview('label983');" title="click to collapse or expand..."> more... </a>
 <div id="label983" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">compliance_level</span> <b>(Alias name: compliance-level)</b>  Compliance levels for the esl solution integration (default = compliance-level-2). <span class="li-normal">type: str</span> <span class="li-normal">choices: [compliance-level-2]</span> 
 <a id='label984' href="javascript:ContentClick('label985', 'label984');" onmouseover="ContentPreview('label985');" onmouseout="ContentUnpreview('label985');" title="click to collapse or expand..."> more... </a>
 <div id="label985" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">esl_channel</span> <b>(Alias name: esl-channel)</b>  Esl ses-imagotag dongle channel (default = 127). <span class="li-normal">type: str</span> <span class="li-normal">choices: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 127, -1]</span> 
 <a id='label986' href="javascript:ContentClick('label987', 'label986');" onmouseover="ContentPreview('label987');" onmouseout="ContentUnpreview('label987');" title="click to collapse or expand..."> more... </a>
 <div id="label987" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">output_power</span> <b>(Alias name: output-power)</b>  Esl ses-imagotag dongle output power (default = a). <span class="li-normal">type: str</span> <span class="li-normal">choices: [a, b, c, d, e, f, g, h]</span> 
 <a id='label988' href="javascript:ContentClick('label989', 'label988');" onmouseover="ContentPreview('label989');" onmouseout="ContentUnpreview('label989');" title="click to collapse or expand..."> more... </a>
 <div id="label989" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">scd_enable</span> <b>(Alias name: scd-enable)</b>  Enable/disable esl ses-imagotag serial communication daemon (scd) (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label990' href="javascript:ContentClick('label991', 'label990');" onmouseover="ContentPreview('label991');" onmouseout="ContentUnpreview('label991');" title="click to collapse or expand..."> more... </a>
 <div id="label991" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tls_cert_verification</span> <b>(Alias name: tls-cert-verification)</b>  Enable/disable tls certificate verification (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label992' href="javascript:ContentClick('label993', 'label992');" onmouseover="ContentPreview('label993');" onmouseout="ContentUnpreview('label993');" title="click to collapse or expand..."> more... </a>
 <div id="label993" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">tls_fqdn_verification</span> <b>(Alias name: tls-fqdn-verification)</b>  Enable/disable tls certificate verification (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label994' href="javascript:ContentClick('label995', 'label994');" onmouseover="ContentPreview('label995');" onmouseout="ContentUnpreview('label995');" title="click to collapse or expand..."> more... </a>
 <div id="label995" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 </ul>
 </li>
 <li><span class="li-head">indoor_outdoor_deployment</span> <b>(Alias name: indoor-outdoor-deployment)</b>  Set to allow indoor/outdoor-only channels under regulatory rules (default = platform-determined). <span class="li-normal">type: str</span> <span class="li-normal">choices: [platform-determined, outdoor, indoor]</span> 
 <a id='label996' href="javascript:ContentClick('label997', 'label996');" onmouseover="ContentPreview('label997');" onmouseout="ContentUnpreview('label997');" title="click to collapse or expand..."> more... </a>
 <div id="label997" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.1 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">syslog_profile</span> <b>(Alias name: syslog-profile)</b>  System log server configuration profile name. <span class="li-normal">type: str</span>
 <a id='label998' href="javascript:ContentClick('label999', 'label998');" onmouseover="ContentPreview('label999');" onmouseout="ContentUnpreview('label999');" title="click to collapse or expand..."> more... </a>
 <div id="label999" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wan_port_auth</span> <b>(Alias name: wan-port-auth)</b>  Set wan port authentication mode (default = none). <span class="li-normal">type: str</span> <span class="li-normal">choices: [none, 802.1x]</span> 
 <a id='label1000' href="javascript:ContentClick('label1001', 'label1000');" onmouseover="ContentPreview('label1001');" onmouseout="ContentUnpreview('label1001');" title="click to collapse or expand..."> more... </a>
 <div id="label1001" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wan_port_auth_methods</span> <b>(Alias name: wan-port-auth-methods)</b>  Wan port 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [all, EAP-FAST, EAP-TLS, EAP-PEAP]</span> 
 <a id='label1002' href="javascript:ContentClick('label1003', 'label1002');" onmouseover="ContentPreview('label1003');" onmouseout="ContentUnpreview('label1003');" title="click to collapse or expand..."> more... </a>
 <div id="label1003" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wan_port_auth_password</span> <b>(Alias name: wan-port-auth-password)</b>  Set wan port 802. <span class="li-normal">type: list</span>
 <a id='label1004' href="javascript:ContentClick('label1005', 'label1004');" onmouseover="ContentPreview('label1005');" onmouseout="ContentUnpreview('label1005');" title="click to collapse or expand..."> more... </a>
 <div id="label1005" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wan_port_auth_usrname</span> <b>(Alias name: wan-port-auth-usrname)</b>  Set wan port 802. <span class="li-normal">type: str</span>
 <a id='label1006' href="javascript:ContentClick('label1007', 'label1006');" onmouseover="ContentPreview('label1007');" onmouseout="ContentUnpreview('label1007');" title="click to collapse or expand..."> more... </a>
 <div id="label1007" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.0.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">_is_factory_setting</span> Is factory setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable, ext]</span>  <span class="li-normal">default: disable</span> 
 <a id='label1008' href="javascript:ContentClick('label1009', 'label1008');" onmouseover="ContentPreview('label1009');" onmouseout="ContentUnpreview('label1009');" title="click to collapse or expand..."> more... </a>
 <div id="label1009" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">unii_4_5ghz_band</span> <b>(Alias name: unii-4-5ghz-band)</b>  Enable/disable unii-4 5ghz band channels (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1010' href="javascript:ContentClick('label1011', 'label1010');" onmouseover="ContentPreview('label1011');" onmouseout="ContentUnpreview('label1011');" title="click to collapse or expand..."> more... </a>
 <div id="label1011" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.0 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">bonjour_profile</span> <b>(Alias name: bonjour-profile)</b>  Bonjour profile name. <span class="li-normal">type: str</span>
 <a id='label1012' href="javascript:ContentClick('label1013', 'label1012');" onmouseover="ContentPreview('label1013');" onmouseout="ContentUnpreview('label1013');" title="click to collapse or expand..."> more... </a>
 <div id="label1013" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">wan_port_auth_macsec</span> <b>(Alias name: wan-port-auth-macsec)</b>  Enable/disable wan port 802. <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1014' href="javascript:ContentClick('label1015', 'label1014');" onmouseover="ContentPreview('label1015');" onmouseout="ContentUnpreview('label1015');" title="click to collapse or expand..."> more... </a>
 <div id="label1015" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">usb_port</span> <b>(Alias name: usb-port)</b>  Enable/disable usb port of the wtp (default = enable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1016' href="javascript:ContentClick('label1017', 'label1016');" onmouseover="ContentPreview('label1017');" onmouseout="ContentUnpreview('label1017');" title="click to collapse or expand..."> more... </a>
 <div id="label1017" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.4.3 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">admin_auth_tacacs_</span> <b>(Alias name: admin-auth-tacacs+)</b>  Remote authentication server for admin user. <span class="li-normal">type: list</span>
 <a id='label1018' href="javascript:ContentClick('label1019', 'label1018');" onmouseover="ContentPreview('label1019');" onmouseout="ContentUnpreview('label1019');" title="click to collapse or expand..."> more... </a>
 <div id="label1019" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
 </div>
 </li>
 <li><span class="li-head">admin_restrict_local</span> <b>(Alias name: admin-restrict-local)</b>  Enable/disable local admin authentication restriction when remote authenticator is up and running (default = disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: [disable, enable]</span> 
 <a id='label1020' href="javascript:ContentClick('label1021', 'label1020');" onmouseover="ContentPreview('label1021');" onmouseout="ContentUnpreview('label1021');" title="click to collapse or expand..."> more... </a>
 <div id="label1021" style="display:none">
 <p>Supported Version Ranges: <code class="docutils literal notranslate">v7.6.2 -> latest</code></p>
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
      - name: Configure WTP profiles or FortiAP profiles that define radio settings for manageable FortiAP platforms.
        fortinet.fortimanager.fmgr_wtpprofile:
          # bypass_validation: false
          workspace_locking_adom: <value in [global, custom adom including root]>
          workspace_locking_timeout: 300
          # rc_succeeded: [0, -2, -3, ...]
          # rc_failed: [-2, -3, ...]
          adom: <your own value>
          state: present # <value in [present, absent]>
          wtpprofile:
            name: "your value" # Required variable, string
            # allowaccess:
            #   - "https"
            #   - "ssh"
            #   - "snmp"
            #   - "http"
            #   - "telnet"
            # ap_country: <value in [AL, DZ, AR, ...]>
            # ble_profile: <string>
            # comment: <string>
            # control_message_offload:
            #   - "ebp-frame"
            #   - "aeroscout-tag"
            #   - "ap-list"
            #   - "sta-list"
            #   - "sta-cap-list"
            #   - "stats"
            #   - "aeroscout-mu"
            #   - "sta-health"
            #   - "spectral-analysis"
            # deny_mac_list:
            #   - id: <integer>
            #     mac: <string>
            # dtls_in_kernel: <value in [disable, enable]>
            # dtls_policy:
            #   - "clear-text"
            #   - "dtls-enabled"
            #   - "ipsec-vpn"
            #   - "ipsec-sn-vpn"
            # energy_efficient_ethernet: <value in [disable, enable]>
            # ext_info_enable: <value in [disable, enable]>
            # handoff_roaming: <value in [disable, enable]>
            # handoff_rssi: <integer>
            # handoff_sta_thresh: <integer>
            # ip_fragment_preventing:
            #   - "tcp-mss-adjust"
            #   - "icmp-unreachable"
            # led_schedules: <list or string>
            # led_state: <value in [disable, enable]>
            # lldp: <value in [disable, enable]>
            # login_passwd: <list or string>
            # login_passwd_change: <value in [no, yes, default]>
            # max_clients: <integer>
            # poe_mode: <value in [auto, 8023af, 8023at, ...]>
            # split_tunneling_acl:
            #   - dest_ip: <string>
            #     id: <integer>
            # split_tunneling_acl_local_ap_subnet: <value in [disable, enable]>
            # split_tunneling_acl_path: <value in [tunnel, local]>
            # tun_mtu_downlink: <integer>
            # tun_mtu_uplink: <integer>
            # wan_port_mode: <value in [wan-lan, wan-only]>
            # snmp: <value in [disable, enable]>
            # ap_handoff: <value in [disable, enable]>
            # apcfg_profile: <string>
            # frequency_handoff: <value in [disable, enable]>
            # lan:
            #   port_esl_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port_esl_ssid: <string>
            #   port_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port_ssid: <string>
            #   port1_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port1_ssid: <string>
            #   port2_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port2_ssid: <string>
            #   port3_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port3_ssid: <string>
            #   port4_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port4_ssid: <string>
            #   port5_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port5_ssid: <string>
            #   port6_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port6_ssid: <string>
            #   port7_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port7_ssid: <string>
            #   port8_mode: <value in [offline, bridge-to-wan, bridge-to-ssid, ...]>
            #   port8_ssid: <string>
            # lbs:
            #   aeroscout: <value in [disable, enable]>
            #   aeroscout_ap_mac: <value in [bssid, board-mac]>
            #   aeroscout_mmu_report: <value in [disable, enable]>
            #   aeroscout_mu: <value in [disable, enable]>
            #   aeroscout_mu_factor: <integer>
            #   aeroscout_mu_timeout: <integer>
            #   aeroscout_server_ip: <string>
            #   aeroscout_server_port: <integer>
            #   ekahau_blink_mode: <value in [disable, enable]>
            #   ekahau_tag: <string>
            #   erc_server_ip: <string>
            #   erc_server_port: <integer>
            #   fortipresence: <value in [disable, enable, enable2, ...]>
            #   fortipresence_ble: <value in [disable, enable]>
            #   fortipresence_frequency: <integer>
            #   fortipresence_port: <integer>
            #   fortipresence_project: <string>
            #   fortipresence_rogue: <value in [disable, enable]>
            #   fortipresence_secret: <list or string>
            #   fortipresence_server: <string>
            #   fortipresence_unassoc: <value in [disable, enable]>
            #   station_locate: <value in [disable, enable]>
            #   fortipresence_server_addr_type: <value in [fqdn, ipv4]>
            #   fortipresence_server_fqdn: <string>
            #   polestar: <value in [disable, enable]>
            #   polestar_accumulation_interval: <integer>
            #   polestar_asset_addrgrp_list: <string>
            #   polestar_asset_uuid_list1: <string>
            #   polestar_asset_uuid_list2: <string>
            #   polestar_asset_uuid_list3: <string>
            #   polestar_asset_uuid_list4: <string>
            #   polestar_protocol: <value in [WSS]>
            #   polestar_reporting_interval: <integer>
            #   polestar_server_fqdn: <string>
            #   polestar_server_path: <string>
            #   polestar_server_port: <integer>
            #   polestar_server_token: <string>
            #   ble_rtls: <value in [none, polestar, evresys]>
            #   ble_rtls_accumulation_interval: <integer>
            #   ble_rtls_asset_addrgrp_list: <list or string>
            #   ble_rtls_asset_uuid_list1: <string>
            #   ble_rtls_asset_uuid_list2: <string>
            #   ble_rtls_asset_uuid_list3: <string>
            #   ble_rtls_asset_uuid_list4: <string>
            #   ble_rtls_protocol: <value in [WSS]>
            #   ble_rtls_reporting_interval: <integer>
            #   ble_rtls_server_fqdn: <string>
            #   ble_rtls_server_path: <string>
            #   ble_rtls_server_port: <integer>
            #   ble_rtls_server_token: <string>
            # platform:
            #   ddscan: <value in [disable, enable]>
            #   mode: <value in [dual-5G, single-5G]>
            #   type: <value in [30B-50B, 60B, 80CM-81CM, ...]>
            #   _local_platform_str: <string>
            # radio_1:
            #   airtime_fairness: <value in [disable, enable]>
            #   amsdu: <value in [disable, enable]>
            #   ap_sniffer_addr: <string>
            #   ap_sniffer_bufsize: <integer>
            #   ap_sniffer_chan: <integer>
            #   ap_sniffer_ctl: <value in [disable, enable]>
            #   ap_sniffer_data: <value in [disable, enable]>
            #   ap_sniffer_mgmt_beacon: <value in [disable, enable]>
            #   ap_sniffer_mgmt_other: <value in [disable, enable]>
            #   ap_sniffer_mgmt_probe: <value in [disable, enable]>
            #   auto_power_high: <integer>
            #   auto_power_level: <value in [disable, enable]>
            #   auto_power_low: <integer>
            #   auto_power_target: <string>
            #   band: <value in [802.11b, 802.11a, 802.11g, ...]>
            #   band_5g_type: <value in [5g-full, 5g-high, 5g-low]>
            #   bandwidth_admission_control: <value in [disable, enable]>
            #   bandwidth_capacity: <integer>
            #   beacon_interval: <integer>
            #   bss_color: <integer>
            #   call_admission_control: <value in [disable, enable]>
            #   call_capacity: <integer>
            #   channel: <list or string>
            #   channel_bonding: <value in [disable, enable, 80MHz, ...]>
            #   channel_utilization: <value in [disable, enable]>
            #   coexistence: <value in [disable, enable]>
            #   darrp: <value in [disable, enable]>
            #   drma: <value in [disable, enable]>
            #   drma_sensitivity: <value in [low, medium, high]>
            #   dtim: <integer>
            #   frag_threshold: <integer>
            #   max_clients: <integer>
            #   max_distance: <integer>
            #   mode: <value in [disabled, ap, monitor, ...]>
            #   power_level: <integer>
            #   powersave_optimize:
            #     - "tim"
            #     - "ac-vo"
            #     - "no-obss-scan"
            #     - "no-11b-rate"
            #     - "client-rate-follow"
            #   protection_mode: <value in [rtscts, ctsonly, disable]>
            #   radio_id: <integer>
            #   rts_threshold: <integer>
            #   short_guard_interval: <value in [disable, enable]>
            #   spectrum_analysis: <value in [disable, enable, scan-only]>
            #   transmit_optimize:
            #     - "disable"
            #     - "power-save"
            #     - "aggr-limit"
            #     - "retry-limit"
            #     - "send-bar"
            #   vap_all: <value in [disable, enable, tunnel, ...]>
            #   vap1: <string>
            #   vap2: <string>
            #   vap3: <string>
            #   vap4: <string>
            #   vap5: <string>
            #   vap6: <string>
            #   vap7: <string>
            #   vap8: <string>
            #   vaps: <list or string>
            #   wids_profile: <string>
            #   zero_wait_dfs: <value in [disable, enable]>
            #   frequency_handoff: <value in [disable, enable]>
            #   ap_handoff: <value in [disable, enable]>
            #   iperf_protocol: <value in [udp, tcp]>
            #   iperf_server_port: <integer>
            #   power_mode: <value in [dBm, percentage]>
            #   power_value: <integer>
            #   sam_bssid: <string>
            #   sam_captive_portal: <value in [disable, enable]>
            #   sam_password: <list or string>
            #   sam_report_intv: <integer>
            #   sam_security_type: <value in [open, wpa-personal, wpa-enterprise, ...]>
            #   sam_server: <string>
            #   sam_ssid: <string>
            #   sam_test: <value in [ping, iperf]>
            #   sam_username: <string>
            #   arrp_profile: <string>
            #   bss_color_mode: <value in [auto, static]>
            #   sam_cwp_failure_string: <string>
            #   sam_cwp_match_string: <string>
            #   sam_cwp_password: <list or string>
            #   sam_cwp_success_string: <string>
            #   sam_cwp_test_url: <string>
            #   sam_cwp_username: <string>
            #   sam_server_fqdn: <string>
            #   sam_server_ip: <string>
            #   sam_server_type: <value in [ip, fqdn]>
            #   d80211d: <value in [disable, enable]>
            #   optional_antenna: <value in [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, ...]>
            #   mimo_mode: <value in [default, 1x1, 2x2, ...]>
            #   optional_antenna_gain: <string>
            #   sam_ca_certificate: <string>
            #   sam_client_certificate: <string>
            #   sam_eap_method: <value in [tls, peap, both]>
            #   sam_private_key: <string>
            #   sam_private_key_password: <list or string>
            #   channel_bonding_ext: <value in [320MHz-1, 320MHz-2]>
            #   d80211mc: <value in [disable, enable]>
            #   ap_sniffer_chan_width: <value in [320MHz, 240MHz, 160MHz, ...]>
            # radio_2:
            #   airtime_fairness: <value in [disable, enable]>
            #   amsdu: <value in [disable, enable]>
            #   ap_sniffer_addr: <string>
            #   ap_sniffer_bufsize: <integer>
            #   ap_sniffer_chan: <integer>
            #   ap_sniffer_ctl: <value in [disable, enable]>
            #   ap_sniffer_data: <value in [disable, enable]>
            #   ap_sniffer_mgmt_beacon: <value in [disable, enable]>
            #   ap_sniffer_mgmt_other: <value in [disable, enable]>
            #   ap_sniffer_mgmt_probe: <value in [disable, enable]>
            #   auto_power_high: <integer>
            #   auto_power_level: <value in [disable, enable]>
            #   auto_power_low: <integer>
            #   auto_power_target: <string>
            #   band: <value in [802.11b, 802.11a, 802.11g, ...]>
            #   band_5g_type: <value in [5g-full, 5g-high, 5g-low]>
            #   bandwidth_admission_control: <value in [disable, enable]>
            #   bandwidth_capacity: <integer>
            #   beacon_interval: <integer>
            #   bss_color: <integer>
            #   call_admission_control: <value in [disable, enable]>
            #   call_capacity: <integer>
            #   channel: <list or string>
            #   channel_bonding: <value in [disable, enable, 80MHz, ...]>
            #   channel_utilization: <value in [disable, enable]>
            #   coexistence: <value in [disable, enable]>
            #   darrp: <value in [disable, enable]>
            #   drma: <value in [disable, enable]>
            #   drma_sensitivity: <value in [low, medium, high]>
            #   dtim: <integer>
            #   frag_threshold: <integer>
            #   max_clients: <integer>
            #   max_distance: <integer>
            #   mode: <value in [disabled, ap, monitor, ...]>
            #   power_level: <integer>
            #   powersave_optimize:
            #     - "tim"
            #     - "ac-vo"
            #     - "no-obss-scan"
            #     - "no-11b-rate"
            #     - "client-rate-follow"
            #   protection_mode: <value in [rtscts, ctsonly, disable]>
            #   radio_id: <integer>
            #   rts_threshold: <integer>
            #   short_guard_interval: <value in [disable, enable]>
            #   spectrum_analysis: <value in [disable, enable, scan-only]>
            #   transmit_optimize:
            #     - "disable"
            #     - "power-save"
            #     - "aggr-limit"
            #     - "retry-limit"
            #     - "send-bar"
            #   vap_all: <value in [disable, enable, tunnel, ...]>
            #   vap1: <string>
            #   vap2: <string>
            #   vap3: <string>
            #   vap4: <string>
            #   vap5: <string>
            #   vap6: <string>
            #   vap7: <string>
            #   vap8: <string>
            #   vaps: <list or string>
            #   wids_profile: <string>
            #   zero_wait_dfs: <value in [disable, enable]>
            #   frequency_handoff: <value in [disable, enable]>
            #   ap_handoff: <value in [disable, enable]>
            #   iperf_protocol: <value in [udp, tcp]>
            #   iperf_server_port: <integer>
            #   power_mode: <value in [dBm, percentage]>
            #   power_value: <integer>
            #   sam_bssid: <string>
            #   sam_captive_portal: <value in [disable, enable]>
            #   sam_password: <list or string>
            #   sam_report_intv: <integer>
            #   sam_security_type: <value in [open, wpa-personal, wpa-enterprise, ...]>
            #   sam_server: <string>
            #   sam_ssid: <string>
            #   sam_test: <value in [ping, iperf]>
            #   sam_username: <string>
            #   arrp_profile: <string>
            #   bss_color_mode: <value in [auto, static]>
            #   sam_cwp_failure_string: <string>
            #   sam_cwp_match_string: <string>
            #   sam_cwp_password: <list or string>
            #   sam_cwp_success_string: <string>
            #   sam_cwp_test_url: <string>
            #   sam_cwp_username: <string>
            #   sam_server_fqdn: <string>
            #   sam_server_ip: <string>
            #   sam_server_type: <value in [ip, fqdn]>
            #   d80211d: <value in [disable, enable]>
            #   optional_antenna: <value in [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, ...]>
            #   mimo_mode: <value in [default, 1x1, 2x2, ...]>
            #   optional_antenna_gain: <string>
            #   sam_ca_certificate: <string>
            #   sam_client_certificate: <string>
            #   sam_eap_method: <value in [tls, peap, both]>
            #   sam_private_key: <string>
            #   sam_private_key_password: <list or string>
            #   channel_bonding_ext: <value in [320MHz-1, 320MHz-2]>
            #   d80211mc: <value in [disable, enable]>
            #   ap_sniffer_chan_width: <value in [320MHz, 240MHz, 160MHz, ...]>
            # radio_3:
            #   airtime_fairness: <value in [disable, enable]>
            #   amsdu: <value in [disable, enable]>
            #   ap_sniffer_addr: <string>
            #   ap_sniffer_bufsize: <integer>
            #   ap_sniffer_chan: <integer>
            #   ap_sniffer_ctl: <value in [disable, enable]>
            #   ap_sniffer_data: <value in [disable, enable]>
            #   ap_sniffer_mgmt_beacon: <value in [disable, enable]>
            #   ap_sniffer_mgmt_other: <value in [disable, enable]>
            #   ap_sniffer_mgmt_probe: <value in [disable, enable]>
            #   auto_power_high: <integer>
            #   auto_power_level: <value in [disable, enable]>
            #   auto_power_low: <integer>
            #   auto_power_target: <string>
            #   band: <value in [802.11b, 802.11a, 802.11g, ...]>
            #   band_5g_type: <value in [5g-full, 5g-high, 5g-low]>
            #   bandwidth_admission_control: <value in [disable, enable]>
            #   bandwidth_capacity: <integer>
            #   beacon_interval: <integer>
            #   bss_color: <integer>
            #   call_admission_control: <value in [disable, enable]>
            #   call_capacity: <integer>
            #   channel: <list or string>
            #   channel_bonding: <value in [80MHz, 40MHz, 20MHz, ...]>
            #   channel_utilization: <value in [disable, enable]>
            #   coexistence: <value in [disable, enable]>
            #   darrp: <value in [disable, enable]>
            #   drma: <value in [disable, enable]>
            #   drma_sensitivity: <value in [low, medium, high]>
            #   dtim: <integer>
            #   frag_threshold: <integer>
            #   max_clients: <integer>
            #   max_distance: <integer>
            #   mode: <value in [disabled, ap, monitor, ...]>
            #   power_level: <integer>
            #   powersave_optimize:
            #     - "tim"
            #     - "ac-vo"
            #     - "no-obss-scan"
            #     - "no-11b-rate"
            #     - "client-rate-follow"
            #   protection_mode: <value in [rtscts, ctsonly, disable]>
            #   radio_id: <integer>
            #   rts_threshold: <integer>
            #   short_guard_interval: <value in [disable, enable]>
            #   spectrum_analysis: <value in [disable, enable, scan-only]>
            #   transmit_optimize:
            #     - "disable"
            #     - "power-save"
            #     - "aggr-limit"
            #     - "retry-limit"
            #     - "send-bar"
            #   vap_all: <value in [disable, enable, tunnel, ...]>
            #   vap1: <string>
            #   vap2: <string>
            #   vap3: <string>
            #   vap4: <string>
            #   vap5: <string>
            #   vap6: <string>
            #   vap7: <string>
            #   vap8: <string>
            #   vaps: <list or string>
            #   wids_profile: <string>
            #   zero_wait_dfs: <value in [disable, enable]>
            #   frequency_handoff: <value in [disable, enable]>
            #   ap_handoff: <value in [disable, enable]>
            #   iperf_protocol: <value in [udp, tcp]>
            #   iperf_server_port: <integer>
            #   power_mode: <value in [dBm, percentage]>
            #   power_value: <integer>
            #   sam_bssid: <string>
            #   sam_captive_portal: <value in [disable, enable]>
            #   sam_password: <list or string>
            #   sam_report_intv: <integer>
            #   sam_security_type: <value in [open, wpa-personal, wpa-enterprise, ...]>
            #   sam_server: <string>
            #   sam_ssid: <string>
            #   sam_test: <value in [ping, iperf]>
            #   sam_username: <string>
            #   arrp_profile: <string>
            #   bss_color_mode: <value in [auto, static]>
            #   sam_cwp_failure_string: <string>
            #   sam_cwp_match_string: <string>
            #   sam_cwp_password: <list or string>
            #   sam_cwp_success_string: <string>
            #   sam_cwp_test_url: <string>
            #   sam_cwp_username: <string>
            #   sam_server_fqdn: <string>
            #   sam_server_ip: <string>
            #   sam_server_type: <value in [ip, fqdn]>
            #   d80211d: <value in [disable, enable]>
            #   optional_antenna: <value in [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, ...]>
            #   mimo_mode: <value in [default, 1x1, 2x2, ...]>
            #   optional_antenna_gain: <string>
            #   sam_ca_certificate: <string>
            #   sam_client_certificate: <string>
            #   sam_eap_method: <value in [tls, peap, both]>
            #   sam_private_key: <string>
            #   sam_private_key_password: <list or string>
            #   channel_bonding_ext: <value in [320MHz-1, 320MHz-2]>
            #   d80211mc: <value in [disable, enable]>
            #   ap_sniffer_chan_width: <value in [320MHz, 240MHz, 160MHz, ...]>
            # radio_4:
            #   airtime_fairness: <value in [disable, enable]>
            #   amsdu: <value in [disable, enable]>
            #   ap_sniffer_addr: <string>
            #   ap_sniffer_bufsize: <integer>
            #   ap_sniffer_chan: <integer>
            #   ap_sniffer_ctl: <value in [disable, enable]>
            #   ap_sniffer_data: <value in [disable, enable]>
            #   ap_sniffer_mgmt_beacon: <value in [disable, enable]>
            #   ap_sniffer_mgmt_other: <value in [disable, enable]>
            #   ap_sniffer_mgmt_probe: <value in [disable, enable]>
            #   auto_power_high: <integer>
            #   auto_power_level: <value in [disable, enable]>
            #   auto_power_low: <integer>
            #   auto_power_target: <string>
            #   band: <value in [802.11b, 802.11a, 802.11g, ...]>
            #   band_5g_type: <value in [5g-full, 5g-high, 5g-low]>
            #   bandwidth_admission_control: <value in [disable, enable]>
            #   bandwidth_capacity: <integer>
            #   beacon_interval: <integer>
            #   bss_color: <integer>
            #   call_admission_control: <value in [disable, enable]>
            #   call_capacity: <integer>
            #   channel: <list or string>
            #   channel_bonding: <value in [80MHz, 40MHz, 20MHz, ...]>
            #   channel_utilization: <value in [disable, enable]>
            #   coexistence: <value in [disable, enable]>
            #   darrp: <value in [disable, enable]>
            #   drma: <value in [disable, enable]>
            #   drma_sensitivity: <value in [low, medium, high]>
            #   dtim: <integer>
            #   frag_threshold: <integer>
            #   max_clients: <integer>
            #   max_distance: <integer>
            #   mode: <value in [ap, monitor, sniffer, ...]>
            #   power_level: <integer>
            #   powersave_optimize:
            #     - "tim"
            #     - "ac-vo"
            #     - "no-obss-scan"
            #     - "no-11b-rate"
            #     - "client-rate-follow"
            #   protection_mode: <value in [rtscts, ctsonly, disable]>
            #   radio_id: <integer>
            #   rts_threshold: <integer>
            #   short_guard_interval: <value in [disable, enable]>
            #   spectrum_analysis: <value in [disable, enable, scan-only]>
            #   transmit_optimize:
            #     - "disable"
            #     - "power-save"
            #     - "aggr-limit"
            #     - "retry-limit"
            #     - "send-bar"
            #   vap_all: <value in [disable, enable, tunnel, ...]>
            #   vap1: <string>
            #   vap2: <string>
            #   vap3: <string>
            #   vap4: <string>
            #   vap5: <string>
            #   vap6: <string>
            #   vap7: <string>
            #   vap8: <string>
            #   vaps: <list or string>
            #   wids_profile: <string>
            #   zero_wait_dfs: <value in [disable, enable]>
            #   frequency_handoff: <value in [disable, enable]>
            #   ap_handoff: <value in [disable, enable]>
            #   iperf_protocol: <value in [udp, tcp]>
            #   iperf_server_port: <integer>
            #   power_mode: <value in [dBm, percentage]>
            #   power_value: <integer>
            #   sam_bssid: <string>
            #   sam_captive_portal: <value in [disable, enable]>
            #   sam_password: <list or string>
            #   sam_report_intv: <integer>
            #   sam_security_type: <value in [open, wpa-personal, wpa-enterprise, ...]>
            #   sam_server: <string>
            #   sam_ssid: <string>
            #   sam_test: <value in [ping, iperf]>
            #   sam_username: <string>
            #   arrp_profile: <string>
            #   bss_color_mode: <value in [auto, static]>
            #   sam_cwp_failure_string: <string>
            #   sam_cwp_match_string: <string>
            #   sam_cwp_password: <list or string>
            #   sam_cwp_success_string: <string>
            #   sam_cwp_test_url: <string>
            #   sam_cwp_username: <string>
            #   sam_server_fqdn: <string>
            #   sam_server_ip: <string>
            #   sam_server_type: <value in [ip, fqdn]>
            #   d80211d: <value in [disable, enable]>
            #   optional_antenna: <value in [none, FANT-04ABGN-0606-O-N, FANT-04ABGN-1414-P-N, ...]>
            #   mimo_mode: <value in [default, 1x1, 2x2, ...]>
            #   optional_antenna_gain: <string>
            #   sam_ca_certificate: <string>
            #   sam_client_certificate: <string>
            #   sam_eap_method: <value in [tls, peap, both]>
            #   sam_private_key: <string>
            #   sam_private_key_password: <list or string>
            #   channel_bonding_ext: <value in [320MHz-1, 320MHz-2]>
            #   d80211mc: <value in [disable, enable]>
            #   ap_sniffer_chan_width: <value in [320MHz, 240MHz, 160MHz, ...]>
            # console_login: <value in [disable, enable]>
            # esl_ses_dongle:
            #   apc_addr_type: <value in [fqdn, ip]>
            #   apc_fqdn: <string>
            #   apc_ip: <string>
            #   apc_port: <integer>
            #   coex_level: <value in [none]>
            #   compliance_level: <value in [compliance-level-2]>
            #   esl_channel: <value in [0, 1, 2, ...]>
            #   output_power: <value in [a, b, c, ...]>
            #   scd_enable: <value in [disable, enable]>
            #   tls_cert_verification: <value in [disable, enable]>
            #   tls_fqdn_verification: <value in [disable, enable]>
            # indoor_outdoor_deployment: <value in [platform-determined, outdoor, indoor]>
            # syslog_profile: <string>
            # wan_port_auth: <value in [none, 802.1x]>
            # wan_port_auth_methods: <value in [all, EAP-FAST, EAP-TLS, ...]>
            # wan_port_auth_password: <list or string>
            # wan_port_auth_usrname: <string>
            # _is_factory_setting: <value in [disable, enable, ext]>
            # unii_4_5ghz_band: <value in [disable, enable]>
            # bonjour_profile: <string>
            # wan_port_auth_macsec: <value in [disable, enable]>
            # usb_port: <value in [disable, enable]>
            # admin_auth_tacacs_: <list or string>
            # admin_restrict_local: <value in [disable, enable]>


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
