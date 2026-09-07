# Remote Feedback WPS

一个可在 WPS Office 中运行的网页评审工作簿。

在表格中填写公开网页 URL 和可选 Prompt，点击按钮后，工作簿会调用远程反馈服务，并把结果写入「运行记录」。

## 使用

1. 下载 [`artifacts/Remote_Feedback_Playground_WPS.xlsm`](./artifacts/Remote_Feedback_Playground_WPS.xlsm)。
2. 用 WPS Office 打开。
3. 点击黄色安全提示中的「启用宏」。
4. 在「真实反馈台」填写 URL 和 Prompt。
5. 点击「获取真实反馈」。

## 安全说明

公开仓库版本已移除原工作簿密钥。它不会直接可用，除非你把自己的 `X-Workbook-Key` 写入宏并让服务端使用同一密钥。不要把真实密钥提交到 Git。

工作簿只应访问你有权评审的公开网页。不要输入内网地址、登录页、个人数据或机密内容。

## 当前边界

仓库包含最终 WPS 客户端产物。原会话创建的临时 Vercel 服务源码已被清理，因此没有把不存在的源码伪造成项目源码。工作簿默认指向原部署地址；若部署自己的服务，请在宏中替换服务 URL 和密钥。
