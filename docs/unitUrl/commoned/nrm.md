[[toc]]
## nrm命令
nrm(npm registry manager )是npm的镜像源管理工具。
### nrm 管理下载使用镜像
```
#查看镜像资源
nrm ls
#使用某个资源
nrm use 资源名
```
### nrm 安装

#### window:
npm install nrm -g

#### mac: 
sudo npm install nrm -g

### nrm 命令

#### nrm有自带默认配置，*为当前的配置
nrm ls
```js
  npm -------- https://registry.npmjs.org/

  yarn ------- https://registry.yarnpkg.com/

  cnpm ------- http://r.cnpmjs.org/

* taobao ----- https://registry.npm.taobao.org/

  nj --------- https://registry.nodejitsu.com/

  npmMirror -- https://skimdb.npmjs.com/registry/
```

#### 切换当前源地址

nrm use taobao

#### 删除源地址

nrm del taobao

#### 添加源地址

nrm add *** https://****.***/

#### 测试时间

nrm test npm 



#### 直接安装cnpm 

npm install cnpm -g --registry=https://registry.npm.taobao.org

#### 直接更改源地址

npm set registry https://registry.npm.taobao.org/

#### 查看npm源地址

npm config list

#### 删除源地址

npm config rm registry


## nvm命令
[nvm](https://github.com/nvm-sh/nvm)
### nvm 管理node版本
```
#查看node版本
nvm ls
#使用某个node版本
nvm use node版本
```
### 安装流程：
#### 环境安装:安装nvm管理node版本：12.17.0（不要安装node）
1. <https://github.com/coreybutler/nvm-windows/releases> 下载nvm-setup.zip<br/>
2. 安装nvm-setup.zip，安装路径：D:\sofeware\nvm 下nvm和nodejs文件夹<br/>
<img :src="$withBase('/images/nvm/1.png')" alt="foo">
<img :src="$withBase('/images/nvm/2.png')" alt="foo">
 
#### cmd执行：
- nvm查看nvm命令
- nvm install 12.17.0
- nvm use 12.17.0

#### 注意：node和npm丢失问题
- 如果找不node 查看 D:\sofeware\nvm\nvm 中setting.txt 文件下内容是否和环境变量一致<br/>
setting.txt<br/>
<img :src="$withBase('/images/nvm/3.png')" alt="foo">

系统环境变量
<img :src="$withBase('/images/nvm/4.png')" alt="foo">
 
path都要有 %NVM_HOME%  %NVM_SYMLINK% 
- npm找不到，执行nvm install node其他版本号生成npm包：这里使用的是12.10.10


### 常用命令

#### 所有安装node列表
nvm list 

#### 查看网络可以安装的版本
nvm list available 

#### 使用指定node
nvm use node版本

#### 下载最新node
nvm install

#### 下载指定版本node
nvm install node版本

#### 卸载node
nvm uninstall node版本

#### 当前使用的node版本
nvm current

#### 打开nodejs控制
nvm on

#### 关闭nodejs控制
nvm off

#### 查看设置与代理
nvm proxy

#### 设置和查看root路径
nvm root

#### name给不同版本号添加别名
nvm alias <name> <version>

#### name删除已定义的别名
nvm unalias <name> 

#### 设置setting.text
nvm node_mirror [url] 设置或者查看setting.txt中的node_mirror，如果不设置的默认是 https://nodejs.org/dist/
nvm npm_mirror [url] 设置或者查看setting.txt中的npm_mirror,如果不设置的话默认的是： https://github.com/npm/npm/archive/.
