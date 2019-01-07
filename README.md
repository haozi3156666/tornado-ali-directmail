# tornado-ali-directmail
阿里云邮件推送包，适配 tornado 框架，异步 API 调用

## 使用示例
```python
from tornado-ali-directmail.client import AliMail

access_id = 'xxxxxx'
access_secret = 'xxxxxx'
from_address = 'test@xxx.com'
from_alias = '小白'
ali_client = AliMail(access_id, access_secret, from_address, from_alias)
resp = yield ali_client.send('xiaoming@qq.com', '主题', '内容', is_html=False) # 默认为纯文本内容
print(resp)
```