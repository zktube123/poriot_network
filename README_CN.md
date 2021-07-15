- 系统推荐配置

- Core 8

- RAM 32G

- ESSD 300GB

- CentOS 7.6

- 前提准备go环境

- ```shell
  wget https://studygolang.com/dl/golang/go1.15.3.linux-amd64.tar.gz
  
  tar -zxvf go1.15.3.linux-amd64.tar.gz
  ```

- 添加环境变量/etc/profile

- ```shell
  - export PATH=$PATH:/usr/local/go/bin
  
  - export GOPATH=/usr/local/go
  
    export PATH=$GOPATH/bin:$PATH
  ```

  保存退出刷新配置

  ```shell
  source /etc/profile
  ```

- 检查是否成功，显示版本号即为成功

  

  ```shell
  go version
  ```

- 下载poriot-network.git

- ```shell
  git clonet https://github.com/zktube123/poriot_network.git
  ```

- 进入目录编译  poriot chain

- ```shell
  cd poriot_network && make gho
  ```

  

- 创建节点目录同步数据

  - ```shell
    mkdir data 
    ```

    - 初始化目录。(创始文件在源码包. genesis.json )

      - ```shell
        gho init --datadir data/ genesis.json
        ```

        

启动 节点

```shell
gho --networkid "52716" --datadir /root/data --port "22022" --http --http.addr "0.0.0.0" --http.corsdomain "*" --http.vhosts "*"  --ws --ws.addr "0.0.0.0" --ws.origins "*" 
```

端口默认 rpc.http 8545 	ws.rpc  8546

