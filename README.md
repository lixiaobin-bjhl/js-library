## js-library
js-library 是一个js common库，为了前期与js-common共存，所以取名js-library。

## 使用说明

* 执行npm install 下载安装js-library依赖的nodejs 模块。
* 执行npm start 启用web服务，用于自己联调。
* 执行npm test 运行单元测试。前提是pc上需安装chrome浏览器。所有单元测试用例都存放在test/unit目录下。
* 执行npm run protractor 运行端到端测试。所有端到端测试用例都存放在test/e2e目录下。

## 规范说明

* 所有function或util中已实现的功能请直接使用，不重复造轮子。
* 所有的依懒（dep目录）都使用bower进行统一管理（更新、卸载、更新）。
* 项目下有jshint 配置文件.jshintrc，所有提交的代码都必须jshint检测通过后才能提交。
* dep中的文件禁止改动。
* 禁止把项目无关的文件（如.DS_Store）提代到仓库中，把不需要提交的文件增加到.gitignore文件中。
* ngDirective、ngFilter、ngService先在widget或util中实现，再用angularJs语法封装。这样非angularJs项目也能使用js-library的服务。
* 原则上所有src下的js代码都需要有单元测试、并且保证测试用例通过（如图1所示），且覆盖率90%及以上（如图2所示）。
* dep里面有ng-bootStrap源码，建议在项目中选择性的引用。
* 每个功能都尽量写一个demo页面供参考，demo页面放在demo对应的目录下。
* 交互性较强的功能建议写e2e测试用例，并保证测试用例通过（如图3所示）。
* 所有提交的代码，严格使用gerrit走评审流程，并且于少2人评审。

## 目录介绍
* dep 第三方依赖，如jquery、angularjs。
* biz 公共业务处理。如room、cas。
* demo demo展示示例。
* ngDirective 公共angularJs指令 如regionSelector、subjectSelector。
* ngService 公共angularJs服务。如urlUtil、storage。
* ngFilter 公共的angularJs filter，比如货币filter。（内置的filter负数展示有问题）
* ngAnimation 公共的动画。
* function 公共的function。比使生成一个唯一的guid函数。目前function的文件copy了凤巢和cobble中的function。
* uitl 公共的uitl。比如时间处理工具、flag控制。
* widget 公共的小组件。比如regionSelector、subjectSelector。
* test 所有端到端测试和单元测试用列,并且保证测试用例通过。

![单元测试](http://sucimg.itc.cn/sblog/j66fdd6aae1e57439a2bd348b77c8bf13 '单元测试')

（图1）

![覆盖率](http://sucimg.itc.cn/sblog/ja25e87bc4954ddba122e402f77888787 '覆盖率')

（图2）

![e2e测试](http://sucimg.itc.cn/sblog/jb7ba5e7ebaa361a9a96405b859ab7bd6 'e2e测试')

（图3）


