资源准备
准备好下面的文件，可以直接下载我的小火箭(Shadoerocket)在线安装仓库修改一下对应文件

准备好APP的IPA文件（ Shadowrocket.ipa ）
静态页面 index.html
ipa.plist 文件
准备好仓库并开启 Github Pages （https://github.com/52bp/shadowrocket ）
修改资源文件
下面我以我的仓库文件为例，教大家自己安装的时候需要修改哪些地方

1.替换IPA文件
把我我的Shdowrocket.ipa替换成你自己要在线安装的应用的ipa文件


2.修改 ipa.plist 文件
打开ipa.plist内容如下，修改里面的ipa地址以及版本号之类的信息

<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
    <dict>
        <key>items</key>
        <array>
            <dict>
                <key>assets</key>
                <array>
                    <dict>
                        <key>kind</key>
                        <string>software-package</string>
                        <key>url</key>
             <string>https://52bp.github.io/shadowrocket/Shadowrocket.ipa</string>
                    </dict>
                </array>
                <key>metadata</key>
                <dict>
                    <key>bundle-identifier</key>
                     <string>live.yremp.Shadowrocket</string>
                     <key>bundle-version</key>
                    <string>2.1.12</string>
                    <key>kind</key>
                    <string>software</string>
                    <key>title</key>
                    <string>Shadowrocket</string>
                </dict>
            </dict>
        </array>
    </dict>
</plist>
3.修改index.html
在index.html里面找到下面的代码

 <span id="checkinfo">
     <a href="itms-services://?action=download-manifest&url=https://52bp.github.io/shadowrocket/ipa.plist" class="btn btn-success btn-lg btn-circle" id="uaApp">在线安装</a>
          <div class="uatip" id="uaTip">
                <span class="uatip-icon"></span>
                         <p class="uatip-txt">点击右上角<br />选择在Safari中打开</p>
           </div>
  </span>
修改https://52bp.github.io/shadowrocket/ipa.plist为你自己的 ipa.plist URL即可，剩下的html内容就是前端展示相关，自己修改，修改完推送到Github仓库即可。
