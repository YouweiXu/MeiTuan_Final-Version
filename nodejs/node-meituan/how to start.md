启动该项目前，需要先配置如下账号：

config文件下：
1.baidu.js：设置APPID/AK/SK
2.base.js：阿里云云数据库链接
3.dispose.js：配置你的微信支付商户号，配置你的实时通讯地址，你的appkey

短信验证码账号配置
config/smcode.js文件：
var client = new Core({
  accessKeyId: '你的阿里云账号',
  accessKeySecret: '你的阿里云账号',
  endpoint: 'https://dysmsapi.aliyuncs.com',
  apiVersion: '2017-05-25'
});

let params = {
	  "RegionId": "配置短信验证码相关",
	  "PhoneNumbers": iphone,
	  "SignName": "配置短信验证码相关",
	  "TemplateCode": "配置短信验证码相关",
	  "TemplateParam": `{"code":${codes}}`
}

oss/oss.js:
填写你的阿里云oss账号
accessKeyId: '',
accessKeySecret: '',

routes/wxuser/wxuser.js：
appid:'小程序appid',
secret:'小程序秘钥',


以上账号配置后在项目根目录下执行npm install或者cnpm install安装依赖
成功之后，再执行nodemon app.js启动



--------------------温馨提示：以看课程为主，切勿追求急于求成-----------------