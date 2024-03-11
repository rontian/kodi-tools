# KODI相关问题收集

## kodi源仓库

[https://github.com/xbmc/xbmc](https://github.com/xbmc/xbmc)

### 修改为清华源镜像

下载<https://github.com/xbmc/xbmc>，找到目录下<addons/repository.xbmc.org/addon.xml>

> 修改前

```xml
<extension point="xbmc.addon.repository">
    <!-- Do not forget to bump add-on version when changing paths to force a repo refresh -->
    <dir>
        <info>https://mirrors.kodi.tv/addons/omega/addons.xml.gz</info>
        <checksum verify="sha256">https://mirrors.kodi.tv/addons/omega/addons.xml.gz?sha256</checksum>
        <datadir>https://mirrors.kodi.tv/addons/omega</datadir>
        <artdir>https://mirrors.kodi.tv/addons/omega</artdir>
        <hashes>sha256</hashes>
    </dir>
</extension>
```

>修改后

```xml
<extension point="xbmc.addon.repository">
    <!-- Do not forget to bump add-on version when changing paths to force a repo refresh -->
    <dir>
        <info>https://mirrors4.tuna.tsinghua.edu.cn/kodi/addons/omega/addons.xml.gz</info>
        <checksum>https://mirrors4.tuna.tsinghua.edu.cn/kodi/addons/omega/addons.xml.gz</checksum>
        <datadir>https://mirrors4.tuna.tsinghua.edu.cn/kodi/addons/omega</datadir>
        <artdir>https://mirrors4.tuna.tsinghua.edu.cn/kodi/addons/omega</artdir>
        <hashes>false</hashes>
    </dir>
</extension>
```

## android hosts修改工具

[https://github.com/x-falcon/Virtual-Hosts](https://github.com/x-falcon/Virtual-Hosts)

## 修改hosts

### 从[https://tool.chinaz.com/dns](https://tool.chinaz.com/dns)查询`api.themoviedb.org`和`image.tmdb.org`在香港亚马逊云的ip进行修改

> hosts文件内容如下

```hosts
13.224.163.120  api.themoviedb.org
13.224.163.120  image.tmdb.org
```
