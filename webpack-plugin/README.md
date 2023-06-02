# webpack-plugin
> 深度介入 Webpack 构建过程，重塑 构建逻辑

Webpack Plugin 其实就是一个普通的函数，在该函数中需要我们定制一个 apply 方法。当 Webpack 内部进行插件挂载时会执行 apply 函数。我们可以在 apply 方法中订阅各种生命周期钩子，当到达对应的时间点时就会执行。