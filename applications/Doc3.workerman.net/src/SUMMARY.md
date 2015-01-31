# Summary

* [版权信息](license/README.md)
* [序言](preface/README.md)
* [入门指引](getting-started/README.md)
   * [特性](getting-started/feature.md)
   * [简单的开发实例](getting-started/simple-example.md)
* [安装配置](install/README)
   * [环境要求](install/requirement.md)
   * [下载安装](install/install.md)
   * [启动与停止](install/start-and-stop.md)
* [开发流程](development/README.md)
   * [开发前必读](development/before-development.md)
   * [目录结构](development/directory-structure.md)
   * [开发规范](development/standard.md)
   * [基本流程](development/process.md)
* [定制通讯协议](protocols/README.md)
   * [通讯协议的作用](protocols/why-protocols.md)
   * [如何定制协议](protocols/how-protocols.md)
   * [一些例子](protocols/example.md)
* [基于Worker开发](worker-development/README.md)
   * [Worker开发适用范围](worker-development/worker-development.md)
   * [Worker类的回调接口](worker-development/worker-functions.md)
       * [onWorkerStart](worker-development/on_worker_start.md)
       * [onWorkerStop](worker-development/on-worker-stop.md)
       * [onConnect](worker-development/on-connect.md)
       * [onMessage](worker-development/on-message.md)
       * [onClose](worker-development/on-close.md)
   * [Connection类提供的接口](worker-development/connection-functions)
       * [send](worker-development/send.md)
       * [getRemoteIp](worker-development/get-remote-ip.md)
       * [getRemotePort](worker-development/get-remote-port.md)
       * [close](worker-development/close.md)
