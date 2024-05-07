# luatos-lib-dnsproxy

DNS代理转发

## 介绍

实现DNS请求的代理转发, 可与ulwip库搭配使用

## 安装

本协议库使用纯lua编写, 所以不需要编译, 直接将源码拷贝到项目即可

## 使用

```lua
local dnsproxy = require("dnsproxy")

sys.taskInit(function()
    sys.waitUntil("IP_READY")
    sys.wait(100)
    -- 监听AP所在的网络, 然后代理到4G网络
    dnsproxy.setup(socket.LWIP_AP, socket.LWIP_GP)
end)
```

## 变更日志

[changelog](changelog.md)

## LIcense

[MIT License](https://opensource.org/licenses/MIT)
