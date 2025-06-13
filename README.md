# ComfyUI-TRMKT-Nodes

The ComfyUI dedicated plugin of TRMKT-AI data cloud platform is used to call the content cloud. Combined with the For Loop plugin, it can automatically generate loops for batch content. The plugin is implemented in Python and communicates with the server through APIs. It supports calling various AI models such as video, image, and audio uploads (Maskkct, MimicMotion, FluxGGUF, etc.)

TRMKT-AI数据云平台的ComfyUI专用插件用于调用内容云。结合For Loop插件，它可以自动生成批量内容的循环。插件基于Python实现，通过API与服务端通信，支持以下功能：视频、图片、音频上传等多种AI模型的调用（Maskgct、MimicMotion、FluxGGUF等）

# Install 安装

You only need to download and extract the plugin to the "\ ComfyUI \ custom_nodes" directory of ComfyUI to use it

你只需要把插件下载并解压到“ComfyUI的\ComfyUI\custom_nodes”目录即可使用

## Detail steps 详细步骤

Ensure that ComfyUI is installed. Please place this plugin in the custom_nodes directory of ComfyUI: ComfyUI/custom_nodes/ComfyUI_Trmket_nodes/(Remember to change the name of the downloaded code package)

Installation dependency: "pip install -r requirements.txt"

Configure the API address in Config. py, which defaults to the local test address, to ensure that the API service is started.

确保已安装ComfyUI。请将此插件放置在ComfyUI的custom_nodes目录下: ComfyUI/custom_nodes/ComfyUI_Trmket_Nodes/(记得下载的代码包要记得改名字)

安装依赖: pip install -r requirements.txt

配置Config.py中的API地址，默认为本地测试地址，确保API服务已启动。


# Instructions 使用说明

## Field filling instructions（字段填写说明）:
API Key: You can register trmkt.top and apply under the "Open API" menu

API-Key：您可以通过注册trmkt.top，并在菜单“开放API”下进行申请即可

## How to use it（安装后如何使用）:

Step 1: https://www.trmkt.top/cn/ Log in or register as a user, apply for API Key under "Open API", and fill in the usage information

Step 2: Open Content Cloud, create a new content library, configure the content, and then copy the content ID to be executed

Step 3: Install the ComfyUI_Trmkt_nodes plugin. Remember to configure the environment through the command line "pip install -r requirements.txt" in the ComfyUI_Trmkt_nodes directory, and restart ComfyUI after installation is complete

Step 4: Introduce plugins (prompt words are description fields for content data in the content cloud, image: main image set in the content cloud, video: main video set in the content cloud)

第一步：https://www.trmkt.top/cn/ 登录或注册用户，并在“开放API”下进行申请API-Key，并填入使用

第二步：打开内容云，新建内容库，配置内容，然后复制要执行的内容id

第三步：安装ComfyUI_Trmkt_Nodes插件，记得在ComfyUI_Trmkt_Nodes目录下，通过命令行pip install -r requirements.txt配置环境，安装完成后重启ComfyUI

第四步：引入插件（提示词是内容云中的内容数据的描述字段，图片：内容云设置的主图，视频为:内容云设置的主视频）

## Prompt（Txt） plugin usage instructions（Prompt（Txt）插件使用说明）:
The Txt plugin needs to select the corresponding field of the content ID of the TRMKT data cloud (content cloud), which can be called as the input source for the next node

Txt插件需要选择TRMKT数据云（内容云）的对应内容ID的对应字段，即可作为下一个节点的输入源进行调用

## Instructions for using the Image plugin（Image插件使用说明）:
The Image plugin calls the corresponding main image of the TRMKT data cloud (content cloud) corresponding to the content ID, which can be used as an input source for calling. When calling, specify the local location to automatically download from the cloud to the local, and then use it as the data input source for the next node for processing

Image插件是调用TRMKT数据云（内容云）的对应内容ID的对应主图，即可作为输入源进行调用。调用时，指定本地的位置，即可自动从云端下载到本地，然后作为下一个节点的数据输入源进行处理

## Instructions for using video plugin（video插件使用说明）:
The video plugin calls the corresponding main video of the TRMKT data cloud (content cloud) with the corresponding content ID, which can be used as the input source for calling. When calling, specify the local location to automatically download from the cloud to the local, and then use it as the data input source for the next node for processing

video插件是调用TRMKT数据云（内容云）的对应内容ID的对应主视频，即可作为输入源进行调用。调用时，指定本地的位置，即可自动从云端下载到本地，然后作为下一个节点的数据输入源进行处理

# Use parameter settings（使用参数设置）:

Please download the example workflow from the plugin code. Please note that when using it, it is necessary to use it in conjunction with the ComfyUI Easy Use plugin's For loop

示例工作流，请在插件代码中下载。注意使用时需要配合ComfyUI-Easy-Use插件的For循环使用

## Platform Content Cloud Settings（平台内容云设置）:

Please upload your content to the Content Cloud first,

1. To use the Prompt (TXT) plugin, it is necessary to update the description
   
2. To use the Video and Image plugins, you need to upload Video and Image, and set the main image and main video. The plugin call will only call the main image and main video.

请先在内容云上传内容：

1. 用Prompt（TXT）插件，需要更新描述
   
2. 用Video和Image插件，需要上传Video和Image，并设置主图和主视频。插件调用只会调用主图和主视频。
   
![image](https://github.com/user-attachments/assets/88c1c73b-2148-4f23-bda6-f1aad83df1e3)


## Plugin parameter settings（插件参数设置）:

The total amount of the loop needs to be consistent with the input Content_id

For循环总量需要与输入的Content_id一致

video plugin：

![image](https://github.com/user-attachments/assets/5cec0297-171e-4012-8f31-e25b6ababcab)

Image plugin：

![image](https://github.com/user-attachments/assets/6fe1a5bb-4826-4011-ac82-cd74dba00c3b)


Prompt（Txt） plugin：

![image](https://github.com/user-attachments/assets/be6a4794-1879-479f-a2cf-8e1ae85f1d36)




# Q&A 常见问题

Launch ComfyUI and find all nodes under the trmktNodes category in the node list. Before uploading files, ensure that the API service is started. All nodes need to provide api_key in order to function properly. If the node is not displayed, check if the directory structure is correct
Confirm that all dependencies have been installed correctly. Check if ComfyUI has loaded the plugin properly. Ensure that the API service is started and accessible.

启动ComfyUI，在节点列表中的trmktNodes分类下可找到所有节点。上传文件前需确保API服务已启动。所有节点都需要提供api_key才能正常使用。如果节点未显示，检查目录结构是否正确。确认所有依赖已正确安装。检查ComfyUI是否正常加载了插件。确保API服务已启动并可访问。

# Notes 备注
If you have any usage issues, please contact us:

如果有使用方面的问题，请联系我们：

WeChat（微信号）：trmktai

Email：36111762@qq.com
