Happy 步骤：

1. 先运行ssl目录生成内网域名证书
2. 将证书拷贝到 traefik 目录下的 certs 目录，再运行 traefik 进行反向代理
3. 此时修改 hosts 文件，方便查看配置
4. 启动 dns-server，将本机 dns 指向 127.0.0.1，就可以把原先的 hosts 配置删掉了
5. 剩下的，想玩什么，到哪个目录下 `docker-compose up` 一下

备注：
- 默认内网域名是 *.dev.io，如果要切换，注意在每个目录下进行修改
- 如果存在 .env.sample 文件的，就先 `mv .env.sample .env`，再执行 `docker-compose up`