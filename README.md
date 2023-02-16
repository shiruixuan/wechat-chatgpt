<h1 align="center">欢迎使用 wechat-chatgpt 👋</h1>

> 在微信上迅速接入 ChatGPT，让它成为你最好的助手！  

&nbsp;

### 下载配置文件模板
```sh
mkdir -p ~/wechat-chatgpt/ && wget https://raw.githubusercontent.com/fuergaosi233/wechat-chatgpt/main/config.yaml.example -O ~/wechat-chatgpt/config.yaml && touch ~/wechat-chatgpt/wechat-assistant.memory-card.json
```
在当前目录创建并修改config.yaml

&nbsp;

### 部署
```sh
docker run -d --name wechat-chatgpt -v ~/wechat-chatgpt/config.yaml:/app/config.yaml -v ~/wechat-chatgpt/wechat-assistant.memory-card.json:/app/wechat-assistant.memory-card.json shiruixuan/wechat-chatgpt:latest
```

&nbsp;

### 使用二维码登陆
```sh
docker logs -f wechat-chatgpt
```
