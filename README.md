![img](./assets/npm-logo.png)

# Test publish a npm package

- 要想发布npm包没有npm账号怎么行？

  npm网站注册地址：https://www.npmjs.com/signup

- 编写你要发布的模块

  例如：
  ```javascript
    exports.cmdHello = function() {
        return 'Hello cmdHello!';
    };

    export function es6Hello() {
        return 'Hello es6Hello!';
    };
  ```
  之后发布到github，这样在package.json文件中可填写repository地址，可实现自动更新包

- 初始化发布的包的描述信息

  使用`npm init`命令生成package.json文件

- 登陆包仓库账号

  登录，使用`npm login`登录npm账号

- 正式发布npm包

  使用`npm publish`命令发布npm包
  注意包名将会与package.json中的name字段一致

- 安装npm包

  发布成功后他人就可以通过`npm install xxx`下载你的npm包了（记得编写测试用例以及完善文档）

- 更新npm包

  如果要更新npm包也很简单，修改好文件后更新下package.json中的`version`字段重新`npm publish`即可

- 删除npm包

  删除要用force强制删除。超过24小时就不能删除了。自己把握好时间。

  `npm --force unpublish xxx`

## 其他
如果想要在发布包对应的github仓库里面README加上类似这样的图片及链接

![img](https://nodei.co/npm/express.png)

可以在这里操作，网址：https://nodei.co/

![img](https://camo.githubusercontent.com/daa90383a04683ce3b210eaa01ade8ef3ae4d42e/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f72656c656173652f4c656163685a686f752f626c6f672e737667)

可以在这里操作，网址：https://shields.io/

![img](https://camo.githubusercontent.com/51cafcc775642bf9af6e729a5928ecd8521113c7/68747470733a2f2f7472617669732d63692e6f72672f4c656163685a686f752f626c6f672e7376673f6272616e63683d6d6173746572)

可以在这里操作，网址：https://travis-ci.org/
