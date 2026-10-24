# 发行包 · 桌面图标布局管理器

本目录存放 **桌面图标布局管理器** 的 Windows x64 可运行包体（由桌面快捷方式实际指向的安装/发布目录整理而来）。

| 项目 | 内容 |
| --- | --- |
| 版本 | `1.0.0` |
| 平台 | Windows x64 |
| 包体路径 | `release/1.0.0/desktop-icon-manager-1.0.0-win-x64/` |
| 文件数 | 1 |
| 体积 | 约 13.1 MB |

## 运行方式

双击 `DesktopIconManager.exe`

## 校验完整性

```bash
cd release
sha256sum -c SHA256SUMS.txt
```

Windows PowerShell：

```powershell
Get-Content release\SHA256SUMS.txt | ForEach-Object {
  $h, $p = $_ -split '  ', 2
  if ((Get-FileHash $p -Algorithm SHA256).Hash -ne $h.ToUpper()) { "MISMATCH $p" }
}
```

## 关于 桌面图标布局管理器

保存与还原 Windows 桌面图标布局。

## 未纳入的内容

无（单文件发行）。

以上目录属于开发环境、运行期缓存或大体积模型权重，不影响程序本体运行。
