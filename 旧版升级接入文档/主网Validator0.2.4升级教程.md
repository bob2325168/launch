# 主网Validator 0.2.4 升级教程

### 1. 下载安装包并解压
`创建目录并进入`
```
mkdir -p ~/LambdaIM && cd ~/LambdaIM  
```
如已有~/LambdaIM目录则直接进入目录：`cd ~/LambdaIM` 

`下载安装包`
```
wget https://github.com/LambdaIM/launch/releases/download/v0.2.4/lambda-0.2.4-release.tar.gz
```

`解压安装包`
```
tar zxvf lambda-0.2.4-release.tar.gz && cd lambda-0.2.4-release
```
### 2. 停止节点服务

```
kill -9 `ps aux | grep lambda |grep -v grep| awk '{print $2}'`
```

### 3. 启动节点  
```
nohup ./lambda start --p2p.laddr tcp://0.0.0.0:26656 --rpc.laddr tcp://0.0.0.0:26657 >> /tmp/lambda.log 2>&1 &
```
