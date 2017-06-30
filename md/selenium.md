- 利用selenium模拟登入，获取cookies
```
from selenium import webdriver
import requests
#模拟登陆
browse = webdriver.Chrome()
browse.get(url)

#获取cookie
def getCookies():
    cookie_arr = [item["name"] + "=" + item["value"] for item in browse.get_cookies()] 
    cookies = ';'.join(item for item in cookie_arr)
    return cookies
headers = {'Cookie':cookies}
requests.get("http://www.baidu.com", headers = headers)
```
- 爬取https链接，解决SSL证书错误问题：SSLError: bad handshake
```
requests.get("https://webvpn.ruijie.com.cn", headers = headers, verify=false)
```
- 解决warning问题
```
from requests.packages.urllib3.exceptions import InsecureRequestWarning
# 禁用安全请求警告
requests.packages.urllib3.disable_warnings(InsecureRequestWarning)
```
- 解决html中文乱码问题
```
html = requests.get(url)
html.encoding = "utf-8"
```
- xpath 用法
- 取消弹窗警告
```
browse.switch_to_alert.accept()
browse.switch_to_alert.dismiss()
```