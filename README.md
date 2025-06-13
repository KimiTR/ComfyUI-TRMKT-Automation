# ComfyUI-TRMKT-Automation

The ComfyUI dedicated plugin for TRMKT-AI data cloud platform is used to call content clouds. Combined with the For Loop plugin, it can automate the loop for batch content generation.

TRMKT-AI数据云平台的ComfyUI专用插件用于调用内容云。结合For Loop插件，它可以自动生成批量内容的循环。

# Install 安装

You only need to download and extract the plugin to the "\ ComfyUI \ custom_nodes" directory of ComfyUI to use it

你只需要把插件下载并解压到“ComfyUI的\ComfyUI\custom_nodes”目录即可使用

# Instructions 使用说明

## Field filling instructions（字段填写说明）:
API Key: You can register trmkt.top and apply under the "Open API" menu

API-Key：您可以通过注册trmkt.top，并在菜单“开放API”下进行申请即可

## Prompt（Txt） plugin usage instructions（Prompt（Txt）插件使用说明）:
The Txt plugin needs to select the corresponding field of the content ID of the TRMKT data cloud (content cloud), which can be called as the input source for the next node

Txt插件需要选择TRMKT数据云（内容云）的对应内容ID的对应字段，即可作为下一个节点的输入源进行调用

## Instructions for using the Image plugin（Image插件使用说明）:
The Image plugin calls the corresponding main image of the TRMKT data cloud (content cloud) corresponding to the content ID, which can be used as an input source for calling. When calling, specify the local location to automatically download from the cloud to the local, and then use it as the data input source for the next node for processing

Image插件是调用TRMKT数据云（内容云）的对应内容ID的对应主图，即可作为输入源进行调用。调用时，指定本地的位置，即可自动从云端下载到本地，然后作为下一个节点的数据输入源进行处理

## Instructions for using video plugin（video插件使用说明）:
The video plugin calls the corresponding main video of the TRMKT data cloud (content cloud) with the corresponding content ID, which can be used as the input source for calling. When calling, specify the local location to automatically download from the cloud to the local, and then use it as the data input source for the next node for processing

video插件是调用TRMKT数据云（内容云）的对应内容ID的对应主视频，即可作为输入源进行调用。调用时，指定本地的位置，即可自动从云端下载到本地，然后作为下一个节点的数据输入源进行处理

# Notes 备注
If you have any usage issues, please contact us:

如果有使用方面的问题，请联系我们：

WeChat（微信号）：trmktai

Email：36111762@qq.com

[![Stargazers repo roster for @TRMKT-AI/ComfyUI-TRMKT-Automation](https://reporoster.com/stars/dark/notext/TRMKT-AI/ComfyUI-TRMKT-Automation)](https://github.com/TRMKT-AI/ComfyUI-TRMKT-Automation/stargazers)
