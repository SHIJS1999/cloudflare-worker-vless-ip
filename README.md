#白奶酪

#通过ws路径自定义cf worker vless出站ip

1.原作者ED哥：GitHub Repository for https://github.com/zizifn/edgetunnel

2.当路径字符串为myIP时，出站IP和你自己选择的CF入站IP一致

3.当路径字符串为proxyIP=时，如proxyIP=11.11.11.11，你的出站IP为11.11.11.11。（proxyIP必须是CF的反代IP）

#模板
     
    type: vless
     
    name: www.123.com
   
    server: 12.34.56.78
    
    port: 443
    
    uuid: YouUserId
    
    network: ws
    
    tls: true 
    
    udp: false
    
    sni: www.123.com
    
    client-fingerprint: chrome
    
    ws-opts:
  
    path: "/proxyIP=11.11.11.11"
    
    headers:
    
    host: www.123.com
    
