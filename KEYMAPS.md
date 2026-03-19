# 快捷键速查表

> Leader 键为 `Space`

## 通用

| 快捷键 | 模式 | 说明 |
|--------|------|------|
| `jk` | Insert | 退出插入模式 (等同 Esc) |
| `jk` | Terminal | 退出终端模式 |
| `Esc Esc` | Terminal | 退出终端模式 |
| `Esc` | Normal | 清除搜索高亮 |
| `;` | Normal | 进入命令模式 (等同 :) |
| `e` | Normal/Visual/Operator | Leap 跳转 |
| `E` | Normal | Leap 跨窗口跳转 |

## 标签页

| 快捷键 | 说明 |
|--------|------|
| `tn` | 新建标签页 |
| `tj` | 下一个标签页 |
| `tk` | 上一个标签页 |

## 窗口导航 (Tmux Navigator)

| 快捷键 | 说明 |
|--------|------|
| `Ctrl-h` | 导航到左侧窗口 |
| `Ctrl-j` | 导航到下方窗口 |
| `Ctrl-k` | 导航到上方窗口 |
| `Ctrl-l` | 导航到右侧窗口 |
| `Ctrl-\` | 导航到上一个窗口 |
| `Ctrl-w s` | 水平分屏 |
| `Ctrl-w v` | 垂直分屏 |
| `Ctrl-w q` | 关闭当前窗口 |
| `Ctrl-w o` | 只保留当前窗口，关闭其他 |
| `Ctrl-w =` | 等分所有窗口 |
| `Ctrl-w T` | 将当前窗口移到新标签页 |

## 文件浏览 (Neo-tree)

| 快捷键 | 说明 |
|--------|------|
| `Ctrl-e` | 打开/关闭文件树 |
| `o` | 打开文件/目录 |
| `z` | 在当前目录使用 grug-far 搜索替换 |
| `O` | 排序菜单 |
| `Oc/Od/Og/Om/On/Os/Ot` | 按创建时间/诊断/Git状态/修改时间/名称/大小/类型排序 |

## 搜索 (Telescope)

| 快捷键 | 说明 |
|--------|------|
| `Ctrl-p` | 搜索文件 |
| `<leader>sf` | 搜索文件 |
| `<leader>sg` | 全局文本搜索 (Grep) |
| `<leader>sw` | 搜索光标下的单词 |
| `<leader>sh` | 搜索帮助文档 |
| `<leader>sk` | 搜索快捷键 |
| `<leader>ss` | 选择 Telescope 搜索器 |
| `<leader>sd` | 搜索诊断信息 |
| `<leader>sr` | 恢复上次搜索 |
| `<leader>s.` | 搜索最近打开的文件 |
| `<leader>s/` | 在已打开的文件中搜索 |
| `<leader>sn` | 搜索 Neovim 配置文件 |
| `<leader>/` | 当前缓冲区模糊搜索 |
| `<leader><leader>` | 查找已打开的缓冲区 |

Telescope 内部快捷键:

| 快捷键 | 说明 |
|--------|------|
| `Ctrl-j` | 下一项 |
| `Ctrl-k` | 上一项 |
| `Ctrl-t` | 在新标签页打开 |
| `Esc` | 关闭 |

## 全局搜索替换 (grug-far)

| 快捷键 | 说明 |
|--------|------|
| `<leader>gs` | 打开全局搜索替换 |

## LSP

| 快捷键 | 说明 |
|--------|------|
| `grd` | 跳转到定义 |
| `grr` | 跳转到引用 |
| `gri` | 跳转到实现 |
| `grt` | 跳转到类型定义 |
| `grD` | 跳转到声明 |
| `grn` | 重命名符号 |
| `gra` | 代码操作 (Normal/Visual) |
| `gO` | 文档符号列表 |
| `gW` | 工作区符号搜索 |
| `L` | 显示当前行诊断浮窗 |
| `<leader>q` | 打开诊断 Quickfix 列表 |
| `<leader>yd` | 复制当前行诊断信息(含位置) |
| `<leader>th` | 切换 Inlay Hints |

## 格式化

| 快捷键 | 说明 |
|--------|------|
| `<leader>f` | 格式化当前缓冲区 |

## 补全 (blink.cmp)

| 快捷键 | 说明 |
|--------|------|
| `Ctrl-s` | 显示/切换签名帮助 |
| `Ctrl-l` | 显示/切换文档 |
| `Ctrl-e` | 隐藏/显示补全菜单 |
| `Ctrl-j` | 选择下一项 |
| `Ctrl-k` | 选择上一项 |

## Git

### Gitsigns

| 快捷键 | 模式 | 说明 |
|--------|------|------|
| `]c` | Normal | 跳转到下一个变更 |
| `[c` | Normal | 跳转到上一个变更 |
| `<leader>hs` | Normal/Visual | 暂存 hunk |
| `<leader>hr` | Normal/Visual | 重置 hunk |
| `<leader>hS` | Normal | 暂存整个缓冲区 |
| `<leader>hu` | Normal | 撤销暂存 hunk |
| `<leader>hR` | Normal | 重置整个缓冲区 |
| `<leader>hp` | Normal | 预览 hunk |
| `<leader>hb` | Normal | 显示当前行 blame |
| `<leader>hd` | Normal | 与 index 对比 diff |
| `<leader>hD` | Normal | 与上次提交对比 diff |
| `<leader>tb` | Normal | 切换行内 blame 显示 |
| `<leader>tD` | Normal | 切换行内删除预览 |

### Neogit

| 快捷键 | 说明 |
|--------|------|
| `<leader>ng` | 打开 Neogit 界面 |

## 调试 (DAP)

| 快捷键 | 说明 |
|--------|------|
| `F5` | 开始/继续调试 |
| `F1` | 单步进入 |
| `F2` | 单步跳过 |
| `F3` | 单步跳出 |
| `F7` | 切换调试 UI |
| `<leader>b` | 切换断点 |
| `<leader>B` | 设置条件断点 |

## 图片预览 (image.nvim)

| 快捷键 | 说明 |
|--------|------|
| `:edit <图片路径>` | 打开并预览图片 |
| `:q` 或 `:bd` | 关闭图片预览 |

## Claude Code

| 快捷键 | 说明 |
|--------|------|
| `<leader>cc` | 打开/关闭 Claude Code |
| `<leader>cf` | 聚焦 Claude 窗口 |
| `<leader>cr` | 恢复上次对话 |
| `<leader>cC` | 继续对话 |
| `<leader>cm` | 选择模型 |
| `<leader>cb` | 添加当前缓冲区到上下文 |
| `<leader>cs` | 发送选中内容到 Claude (Visual) / 在文件树中添加文件 |
| `<leader>ca` | 接受 diff |
| `<leader>cd` | 拒绝 diff |
