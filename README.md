# my_etc-
个人自用的配置文件


## 结构  
### 发行版相关 -> dd

例：
```
dd  
├── distro1
│   └── pkg1.conf
└── distro2
    ├── pkg1
    │   └── pkg1.cfg
    └── rc.local
```
distro 的实际名称从 `sh -c '. /etc/os-release; echo $ID'` 获得  
~~我不关心没有 `/etc/os-release` 的 Linux 发行版~~

### 发行版独立 -> di

例:
```
di
├── pkg1
│   └── pkg1.conf
└── pkg2
    └── config.d
        └── default.conf
```
必须是大多数发行版打包软件包时约定好的位置，否则放在 dd
