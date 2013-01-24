GET请求
$http = new HttpClient();
$http->set_header('User-Agent','Mozilla/5.0 (Windows NT 5.1; rv:13.0) Gecko/20100101 Firefox/13.0.1');
$http->get('http://www.example.com/');
echo $http->get_body();

POST请求
$http = new HttpClient();
$http->set_header('User-Agent','Mozilla/5.0 (Windows NT 5.1; rv:13.0) Gecko/20100101 Firefox/13.0.1');
$data = array(
	'id'=>1,
	'name'=>'example'
);
$file = array(
	'photo'=>'/data/patch/file.jpg'
);
$http->get('http://www.example.com/',array($data)[,$file]);
echo $http->get_body();

Cookie支持
$http->set_cookies($cookie);

代理支持
$http->set_proxy('socks5.example.com:1080',HttpClient::PROXY_SOCKS5,'user','password');