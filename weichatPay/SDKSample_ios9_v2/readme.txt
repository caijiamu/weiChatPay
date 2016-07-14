Demo说明：
注意：
	1.本Demo只是做一个体验和演示,发起支付的流程;
	2.下单和签名、查单和支付通知均在服务器后台实现，请参考后台SDK代码。
	3.本Demo是64位的SDK
	4.直接运行可体验
	5.API详见：https://pay.weixin.qq.com/wiki/doc/api/app.php?chapter=8_1

开发步骤：
	1.开发微信APP支付，需要先去微信开放平台申请移动应用，并开通微信支付功能，通过审核后方可进行开发；
	2.用XCode打开项目，【项目属性】-【Info】-【URL Schemes】设置微信开放平台申请的应用APPID，如图文件夹下"设置appid.jpg"所示。如果这的APPID设置不正确将无法调起微信支付；
	3.需要调用代码注册APPID：[WXApi registerApp:APP_ID withDescription:@"demo 2.0”];项目该APPID需与步骤2中APPID保持一致；
	4.支付请求：WXApiRequestHandler.m中的jumpToBizPay方法实现了唤起微信支付；
	5.支付完成回调：WXApiManager.m中的onResp方法中接收返回支付状态。