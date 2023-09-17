# smartirmqtt  
将smartir改的，原来的smartir支持设备大部分是博联的协议，对mqtt支持非常不友好。    
在github上发现了irgen。可以将博联的红外码转成raw码，  
于是配合一下，就有了这个项目  
需要配合  配置文件里面的irmqttesp32.yaml用来生成ESPHOME固件
原理是将smartir里面的博联的base64码转换成raw码，
然后将raw码用mqtt发送给esphome。esphome将收到的raw码作为红外发送出去  

smartir.yaml放homeassistant里面
将插件放到custom_components目录下面，重启hass就能看到固件了  
