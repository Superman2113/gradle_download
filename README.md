> **使用 Android Studio 时，因为常用 grade 作为依赖管理，不得不说，用着挺方便的。**
>
> **但有时加载别人的工程，发现使用了不同的 gradle ，突然要临时去下载下，因为某些特殊的原因，感觉慢得难受（用了梯子也慢）。**

网上也有方案说，用本地的 gradle 版本，配置下路径，其实也没什么问题。

不过按照个人习惯，想着是多缓存几个常用的 gradle 版本，就算打开别人的工程也没什么问题，这样比较万能嘛，毕竟。

看到有热心的兄弟会在百度云这种上面存几个版本，突然觉得，好像没谁好好整理下这个版本，于是决定慢慢传一些常用的版本，方便大家下载。

附上了官网 sha256 校验码，如果需要校验的可以参考下。

**如果发现有错误的时候可以去官网查看，也希望及时反馈，予以改正。**

**Gradle Zip：https://services.gradle.org/distributions/**

---

然后简单说下使用方法，当然网上也有。

当你使用 Android Studio 打开工程时，发现下方提示框提示 downloading gradle xxx 版本字样时，
从默认的 gradle 配置当中没有找到需要的 gradle 版本。
就会从一个地址下载，可以打开 /gradle/wrapper/gradle-wrapper.properties 文件，
可以看到 distributionUrl=https\://services.gradle.org/distributions/gradle-4.1-all.zip 
类似字样，就是从这个地址下载的，当然也可以自己访问，需要需要下载的版本。

gradle 本地默认路径为: Users/xxx/.gradle (Mac OS),打开后发现 wrapper、caches 与一些其他文件，那么这个地方就是默认的 gradle 文件夹了。
进入 /wrapper/dists/ 中能看到各种 gradle 版本文件夹，找到你需要的，
比如 /gradle-4.4-all/9br9xq1tocpiv8o6njlyu5op1/ 中间有一个随机字符串的文件夹，
，不用修改，点进去，能发现正在下载但未完成的压缩文件，退出 Android Studio ，然后把未完成压缩文件删除，把下载好的完整压缩文件放进去，但是不要解压，
重新打开该工程就可以正常使用了。

需要注意的是，一定是完全退出 Android Studio 。如果你只是在之前下载 Gradle 时取消了，回到选择工程对话框时，此时并没有完全退出 Android Studio ,
你点击退出时，还能看到一个是否取消下载的提示，说明没有完全退出，所以没完全退出时再进入该工程，并不会生效。

---

#### gradle-2.14.1-all.zip
- 88a910cdf2e03ebbb5fe90f7ecf534fc9ac22e12112dc9a2fee810c598a76091

#### gradle-3.3-all.zip
- 71a787faed83c4ef21e8464cc8452b941b5fcd575043aa29d39d15d879be89f7

#### gradle-4.1-all.zip
- 5c07b3bac2209fbc98fb1fdf6fd831f72429cdf8c503807404eae03d8c8099e5

#### gradle-4.4-all.zip
- 7a2c66d1a78f811d5f37d14630ad21cec5e77a2a4dc61e787e2257a6341016ce

