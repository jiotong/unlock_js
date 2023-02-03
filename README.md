<br/>脚本1：<br/>
</p><pre><code>[Script]
unlock_emby = type=http-response,script-path=https://raw.githubusercontent.com/nikleechan/eb1-script/master/unlock_emby.js,pattern=^http(s?):\/\/(www\.|)mb3admin\.com\/.*$,max-size=131072,requires-body=true,timeout=10,debug=false,enable=true
[MITM]
hostname = mb3admin.com,www.mb3admin.com</code></pre>

<br/>脚本2：<br/>
</p><pre><code>[Script]
EmbyPremiere = type=http-response,script-path=https://raw.githubusercontent.com/nikleechan/eb1-script/master/EmbyPremiere.js,pattern=^https?:\/\/mb3admin.com\/admin\/service\/registration\/validateDevice,max-size=131072,requires-body=true,timeout=10,enable=true

[MITM]
hostname = mb3admin.com</code></pre>
<br/>脚本2若打不开，则换备用地址：<br/>
</p><pre><code>[Script]
EmbyPremiere = type=http-response,script-path=https://gitlab.com/iptv-org/embypublic/-/raw/master/Script/EmbyPremiere.js,pattern=^https?:\/\/mb3admin.com\/admin\/service\/registration\/validateDevice,max-size=131072,requires-body=true,timeout=10,enable=true

[MITM]
hostname = mb3admin.com</code></pre>
