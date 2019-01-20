

### gost 2.6.1 修改版，用于openshift v3 docker部署  


#### 修改项  

目标：规避openshift代理检查等  
基准：官方 2.6 20181103 commit c66751b  
- 版本号 d20190120 tls13 docker 20190120  
- 测试服务端和客户端使用go1.12beta2编译，测试http2 tls13  
- 增加-N选项，服务端彻底关闭log，规避用  
- 增加环境变量TSOG_USER 和 TSOG_PASS,仅当命令行有env:env时，环境变量优先替换生效  
- 同步至官方c66751b 2.6 阶段版  
- 同步至官方8390640 2.6.1 阶段版  

#### docker  
<https://hub.docker.com/r/devcodewak/tsog_openshift/>

#### Thanks : ginuerzh  
<https://github.com/ginuerzh/gost>  
  
  
  

