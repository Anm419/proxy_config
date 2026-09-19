# `China_All.list`和 `ChinaMedia.list`规则

## 包含了那些规则

- 包含了`AliPay.list`
- 包含了`DouYin.list`
- 包含了`Pinduoduo.list`
- 包含了`Youku.list`
- 包含了`115.list`
- 包含了`BiliBili.list`
- 包含了`iQIYI.list`
- 包含了`TencentVideo.list`

## 对比规则缺失

- `AliPay.list`对比`China_All.list`和`ChinaMedia.list`将`DOMAIN-SUFFIX,luohanacademy.com`合并到`China_All.list`
- `DouYin.list`对比`China_All.list`和`ChinaMedia.list`将`DOMAIN-SUFFIX,idouyinvod.com`合并到`China_All.list`
- `iQIYI.list`中的`USER-AGENT,iQIYI*`已被`ChinaMedia.list`中的`USER-AGENT,*QIYI*`覆盖，不需要补充 Surge 的`PROCESS-NAME,com.qiyi.video`
- `DingTalk.list`对比`Alibaba_All.list`、`China_All.list`和`ChinaMedia.list`将`DOMAIN-SUFFIX,realapp.xin`合并到`Alibaba_All.list`

# 规则合并

- `CCB.list`合并到了`Bank.list`中
- `CMB.list`合并到了`Bank.list`中
- `ABC.list`合并到了`Bank.list`中
- `BOC.list`合并到了`Bank.list`中
- `BOCOM.list`合并到了`Bank.list`中
- `CGB.list`合并到了`Bank.list`中
- `UnionPay.list`合并到了`Bank.list`中
- `ICBC.list`合并到了`Bank.list`中
- `Alibaba.list`和`Alibaba_Domain.list`合并到了`Alibaba_All.list`中
- `China.list`和`China_Domain.list`合并到了`China_All.list`中
- `Tencent.list`和`Tencent_Domain.list`合并到了`Tencent_All.list`中
- `Apple.list`和`Apple_Domain.list`合并到了`Apple_All.list`中
- `GlobalMedia.list`和`GlobalMedia_Domain.list`合并到了`GlobalMedia_All.list`中
- `Proxy.list`和`Proxy_Domain.list`合并到了`Proxy_All.list`中

# 个人规则补充

- `DOMAIN-SUFFIX,openai.azure.com`合并到了`OpenAI.list`中
- `DOMAIN-SUFFIX,oai.azure.com`合并到了`OpenAI.list`中

# Loon 规则说明

- 规则从`rule/Loon/`整理，分类和文件名参考`Anm/Surge/`，合并规则的位置、分组顺序和备注与 Surge 对应文件保持一致
- `_Domain.list`中的点开头域名转换为`DOMAIN-SUFFIX`，普通域名转换为`DOMAIN`，合并后不需要单独订阅`_Domain.list`
- 保留 Loon 上游的`no-resolve`参数，每个文件内部去重，分类之间保留重叠
- 使用 Loon 上游规则，不迁入 Surge 的`PROCESS-NAME`条目；`WeChat.list`使用 Loon 上游的 33 条规则
- 现有`Loon.lcf`引用`Anm419/proxy_config`仓库下的`Loon/`目录，发布后远程订阅才会更新；若使用当前仓库，需调整仓库、分支及`Anm/Loon/`路径
- 本次整理已通过本地检查，尚未在 Loon 客户端实测
