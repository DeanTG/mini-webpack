# webpack
![image](https://github.com/DeanTG/mini-webpack/assets/16485611/c434fbde-4c12-4f4a-8cb3-ee70d63e1db4)

## Webpack 构建过程可以简单划分为 Init、Make、Seal 三个阶段；
* Init 阶段负责初始化 Webpack 内部若干插件与状态，逻辑比较简单；
* Make 阶段解决资源读入问题，这个阶段会从 Entry —— 入口模块开始，递归读入、解析所有模块内容，并根据模块之间的依赖关系构建 ModuleGraph —— 模块关系图对象；
* Seal 阶段更复杂：
一方面，根据 ModuleGraph 构建 ChunkGraph；
另一方面，开始遍历 ChunkGraph，转译每一个模块代码；
最后，将所有模块与模块运行时依赖合并为最终输出的 Bundle —— 资产文件。
