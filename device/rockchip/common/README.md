# RK3506 Linux SDK

YJH-RK3506G2 MiniPDA Linux 6.1 SDK

## 首次拉取

```bash
git clone --recurse-submodules git@github.com:xmprocat/RK3506_LINUX_SDK.git
cd RK3506_LINUX_SDK
```

## 已有仓库更新

```bash
# 拉取主仓库
git pull

# 更新所有子模块
git submodule update --init --recursive
```

## 子模块

| 目录 | 仓库 | 分支 |
|------|------|------|
| kernel-6.1 | rk_kernel | RK3506_6.1 |
| u-boot | rk_uboot | RK3506_6.1 |
| buildroot | rk_buildroot | RK3506_6.1 |

## 编译

```bash
# 选择板级配置
source envsetup.sh rk3506 YJH-RK3506G2_MiniPDA_NAND

# 完整构建
./build.sh

# 或分步构建
./build.sh kernel
./build.sh rootfs
./build.sh updateimg
```

## 烧录

```bash
# 进入 loader 模式后
rkflash.sh
```
