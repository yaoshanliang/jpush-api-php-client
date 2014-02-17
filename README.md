<<<<<<< HEAD
JPush API client library for Java
API 协议文档： http://docs.jpush.cn/pages/viewpage.action?pageId=2621796

其他语言的开发包： http://docs.jpush.cn/pages/viewpage.action?pageId=2228302

JPush Change List: http://docs.jpush.cn/pages/viewpage.action?pageId=3309737
=======
# JPush API client library for PHP

## 姒傝堪
杩欐槸 JPush REST API 鐨� PHP 鐗堟湰灏佽寮�鍙戝寘锛屾槸鐢辨瀬鍏夋帹閫佸畼鏂规彁渚涚殑锛屼竴鑸敮鎸佹渶鏂扮殑 API 鍔熻兘銆�

瀵瑰簲鐨� REST API 鏂囨。锛�<http://docs.jpush.cn/display/dev/REST+API>

## 鐜閰嶇疆

### PHP 閰嶇疆鏀寔 SSL

#### Windows 绯荤粺涓厤缃�
* 鍦� php.ini 涓� extension=php_openssl.dll 鍘绘帀鍓嶉潰鐨勬敞閲娿�傦紙鍙弬鑰� examples/ 鐩綍涓嬬殑 php.ini 鏂囦欢锛夈��
* 澶嶅埗 php 瀹夎鐩綍涓殑 libeay32.dll, ssleay32.dll 鑷� Windows 鏈哄櫒鐨� c:\windows\system32 鐩綍銆�
* 澶嶅埗 php 瀹夎鐩綍鐨別xt瀛愮洰褰曚腑 php_openssl.dll 鑷� Windows 鏈哄櫒鐨� c:\windows\system32 鐩綍銆�
* 閲嶅惎鏈嶅姟鍣� IIS 鎴栬�� Apache銆�

#### Linux 绯荤粺涓厤缃�
* 瀹夎 openssl銆�
* 濡傛灉褰撳墠鐨� PHP 鐗堟湰鏈敮鎸� SSL锛岄渶瑕侀噸鏂扮紪璇戝畨瑁� PHP 浠ユ敮鎸併�傝 Google 鏂囨。浜嗚В銆�
* 閲嶅惎 Apache銆�

## 浣跨敤鏍蜂緥

### 鎺ㄩ�佹牱渚�
```

$client = new JPushClient($app_key,$master_secret);
$extras = array();
$params = array("receiver_type" => 2,
                "receiver_value" => "tag_api",
                "sendno" => 1,
                "send_description" => "",
                "override_msg_id" => "");
//鍙戦�侀�氱煡
$msgResult1 = $client->sendNotification("tag notify content", $params, $extras);

//鍙戦�佽嚜瀹氫箟淇℃伅
$msgResult2 = $client->sendCustomMessage("tag title","tag notify content", $params, $extras);

```

### 缁熻鑾峰彇鏍蜂緥

```
$client = new JPushClient($app_key,$master_secret);
$msg_ids = "123, 12345, ";
$msgstr = $client->getReportReceiveds($msg_ids);
```


## 鐗堟湰鏇存柊
[Release椤甸潰](https://github.com/jpush/jpush-api-php-client/releases/) 鏈夎缁嗙殑鐗堟湰鍙戝竷璁板綍涓庝笅杞姐��
>>>>>>> dev
