> **使用 Android Studio 时，因为常用 grade 作为依赖管理，不得不说，用着挺方便的。**
>
> **但有时加载别人的工程，发现使用了不同的 gradle ，突然要临时去下载下，因为某些特殊的原因，感觉慢得难受（用了梯子也慢）。**

网上也有方案说，用本地的 gradle 版本，配置下路径，其实也没什么问题。

不过按照个人习惯，想着是多缓存几个常用的 gradle 版本，就算打开别人的工程也没什么问题，这样比较万能嘛，毕竟。

看到有热心的兄弟会在百度云这种上面存几个版本，突然觉得，好像没谁好好整理下这个版本，于是决定慢慢传一些常用的版本，方便大家下载。

附上了官网 sha256 校验码，如果需要校验的可以参考下。

**如果发现有错误的时候可以去官网查看，也希望及时反馈，予以修正。**

**Gradle Zip：https://services.gradle.org/distributions/**

---

然后简单说下使用方法，当然网上也有。

当你使用 Android Studio 打开工程时，发现下方提示框提示 downloading gradle xxx 版本字样时。

![](https://github.com/RamboPan/gradle_download/blob/master/Image/gradle_downloading.png)

从默认的 gradle 配置当中没有找到需要的 gradle 版本。
就会从一个地址下载，可以打开 

    /gradle/wrapper/gradle-wrapper.properties 文件，
  
可以看到 

    distributionUrl=https\://services.gradle.org/distributions/gradle-4.1-all.zip
  
![](https://github.com/RamboPan/gradle_download/blob/master/Image/gradle_check.png)

类似字样，就是从这个地址下载的，当然也可以自己访问，需要需要下载的版本。

    gradle 本地默认路径为: Users/xxx/.gradle (Mac OS)

![](https://github.com/RamboPan/gradle_download/blob/master/Image/gradle_home.png)

,打开后发现 wrapper、caches 与一些其他文件，那么这个地方就是默认的 gradle 文件夹了。进入 

    /wrapper/dists/ 
    
中能看到各种 gradle 版本文件夹，找到你需要的，比如 

    /gradle-4.4-all/9br9xq1tocpiv8o6njlyu5op1/ 中间有一个随机字符串的文件夹，
    
不用修改，点进去，能发现正在下载但未完成的压缩文件，退出 Android Studio ，然后把未完成压缩文件删除，把下载好的完整压缩文件放进去，但是不要解压，
重新打开该工程就可以正常使用了。

![](https://github.com/RamboPan/gradle_download/blob/master/Image/gradle_unfinish_zip.png)

需要注意的是，一定是完全退出 Android Studio 。如果你只是在之前下载 Gradle 时取消了，回到选择工程对话框时，此时并没有完全退出 Android Studio ,
你点击退出时，还能看到一个是否取消下载的提示，说明没有完全退出，所以没完全退出时再进入该工程，并不会生效，完全退出后再进入，重新加载就可以了。

![](https://github.com/RamboPan/gradle_download/blob/master/Image/gradle_exit.png)

---

#### gradle-2.10-all.zip
- 496d60c331f8666f99b66d08ff67a880697a7e85a9d9b76ff08814cf97f61a4c

#### gradle-2.11-all.zip
- a1242e4db8f979998796b1844e608c2acf8f8f54df518bbb3d5954e52253ba71

#### gradle-2.12-all.zip
- d8b1948a575dc9ec13e03db94502ce91815d73da023f611296c04b852164cb5f

#### gradle-2.13-all.zip
- fb126ed684150f9dc39a811cbcf4daada4292fd387ed998c151ff2cf2536d94d

#### gradle-2.14-all.zip
- 65bbc0ef9c48be86fb06522fc927d59dcc7c04266f2bb8156be76971f7c3fc4a

#### gradle-2.14.1-all.zip
- 88a910cdf2e03ebbb5fe90f7ecf534fc9ac22e12112dc9a2fee810c598a76091

#### gradle-3.0-all.zip
- 9c8b7564ea6a911b5b9fcadd60f3a6cea4238413c8b1e1dd14400a50954aab99

#### gradle-3.1-all.zip
- 43be380834a13e28e9504c21f67fe1a8895ab54f314a6596601896dca7213482

#### gradle-3.2-all.zip
- e25ff599ff268182b597c371ed94eb3c225496af5d4e7eb9dcbb08d30f93a9ec

#### gradle-3.2.1-all.zip
- 0209696f1723f607c475109cf3ed8b51c8a91bb0cda05af0d4bd980bdefe75cd

#### gradle-3.3-all.zip
- 71a787faed83c4ef21e8464cc8452b941b5fcd575043aa29d39d15d879be89f7

#### gradle-3.4-all.zip
- 37c2fdce55411e4c89b896c292cae1f8f437862c8433c8a74cfc3805d7670c0a

#### gradle-3.4.1-all.zip
- ed7e9c8bb41bd10d4c9339c95b2f8b122f5bf13188bd90504a26e0f00b123b0d

#### gradle-3.5-all.zip
- d84bf6b6113da081d0082bcb63bd8547824c6967fe68704d1e3a6fde822b7212

#### gradle-3.5.1-all.zip
- 69d99ade952de3727b65a88f3188ee72231ff4e28c2d00aacfc96a42c6d6f303

#### gradle-4.0-all.zip
- a0af75d3d35799a90f56255a24de69c53cd9aea90f0b532586c8f818668e1734

#### gradle-4.0.1-all.zip
- 8a8005633be0ca38a206f2590445685683452a0b98a5d8ffd5b8413be09bf998

#### gradle-4.0.2-all.zip
- b683cb9f8510f3ae9533871e6b244c24eb9398e8c5b432471f91f48dbc91e7a9

#### gradle-4.1-all.zip
- 5c07b3bac2209fbc98fb1fdf6fd831f72429cdf8c503807404eae03d8c8099e5

#### gradle-4.2-all.zip
- 05590c601cca25e75d6fd44e0eb5a5bdb1049a5cb8faec8b2f73cc3c96daeb52

#### gradle-4.2.1-all.zip
- 7897b59fb45148cd8a79f078e5e4cef3861a252dd1a1af729d0c6e8a0a8703a8

#### gradle-4.3-all.zip                
- b3afcc2d5aaf4d23eeab2409d64c54046147322d05acc7fb5a63f84d8a2b8bd7

#### gradle-4.3.1-all.zip
- c5b67330a8a211539d713852c56a6a80fdea365d8902df92d1759d913d18fa2d

#### gradle-4.4-all.zip
- 7a2c66d1a78f811d5f37d14630ad21cec5e77a2a4dc61e787e2257a6341016ce

#### gradle-4.5-all.zip
- 6ac2f8f9302f50241bf14cc5f4a3d88504ad20e61bb98c5fd048f7723b61397e

