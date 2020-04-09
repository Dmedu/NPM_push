# NPM_push

> 创建一个RN第三方包

1. create-react-native-module --package-identifier [id] --platforms [ios] [package_name]

```
Usage: create-react-native-module [options] <name>

Options:

  -V, --version                             output the version number
  --prefix <prefix>                         The prefix of the library module object to be exported by both JavaScript and native code (Default: ``)
  --module-name <moduleName>                The module library package name to be used in package.json. Default: react-native-(name in param-case)
  --module-prefix <modulePrefix>            The prefix of the library module object, ignored if --module-name is specified (Default: `react-native`)
  --package-identifier <packageIdentifier>  [Android] The Java package identifier used by the Android module (Default: `com.reactlibrary`)
  --platforms <platforms>                   Platforms the library module will be created for - comma separated (Default: `ios,android`)
  --tvos-enabled                            Generate the module with tvOS build enabled (requires react-native-tvos fork, with minimum version of 0.60, and iOS platform to be enabled)
  --github-account <githubAccount>          The github account where the library module is hosted (Default: `github_account`)
  --author-name <authorName>                The author's name (Default: `Your Name`)
  --author-email <authorEmail>              The author's email (Default: `yourname@email.com`)
  --license <license>                       The license type (Default: `MIT`)
  --view                                    Generate the module as a very simple native view component
  --use-apple-networking                    [iOS] Use `AFNetworking` dependency as a sample in the podspec & use it from the iOS code
  --generate-example                        Generate an example project and add the library module to it with symlink by defult, with overwrite of example metro.config.js to add workaround for Metro symlink issue - requires both react-native-cli and yarn to be installed globally
  --example-file-linkage                    DEPRECATED: do `yarn add file:../` instead of `yarn add link:../` in a generated example project, and add a postinstall workaround script, with no overwrite of example metro.config.js
  --example-name <exampleName>              Name for the example project (default: `example`)
  --example-react-native-version <version>  React Native version for the generated example project (default: `react-native@latest`)
  --write-example-podfile                   [iOS] EXPERIMENTAL FEATURE NOT SUPPORTED: write (or overwrite) example ios/Podfile
  -h, --help                                output usage information

```

2. 重命名 : mv [old_package_name] [new_package_name]

> 发布npm包。

1. npm config get registry # 查看当前镜像源
2. npm config set registry=http://registry.npmjs.org # 更改回官方镜像源
3. npm adduser # 创建 NPM 账号
4. npm login # 如果已经在官网有账号，可以直接登录
5. npm whoami # 查看登录状态
6. npm publish # 发布
7. npm config set registry http://registry.npm.taobao.org # 切回国内镜像
