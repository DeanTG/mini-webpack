# webpack-loader

* Loader 主要负责将资源内容转译为 Webpack 能够理解、处理的标准 JavaScript 形式，所以通常需要做 Loader 内通过 return/this.callback 方式返回翻译结果；
* Loader Context 提供了许多实用接口，我们可以借助这些接口读取上下文信息，或改变 Webpack 运行状态(相当于产生 Side Effect，例如通过 emitFile 接口)；
* 假若我们开发的 Loader 需要对外提供配置选项，建议使用 schema-utils 校验配置参数是否合法；
* 假若 Loader 需要生成额外的资源文件，建议使用 loader-utils 拼接产物路径；
* 执行时，Webpack 会按照 use 定义的顺序从前到后执行 Pitch Loader，从后到前执行 Normal Loader，我们可以将一些预处理逻辑放在 Pitch 中(如 vue-loader)；