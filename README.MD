# VAP Preview Tool

## 项目简介

VAP Preview Tool 是一个专业的VAP视频预览工具，支持本地和远程VAP资源的预览和播放。专注于提供流畅的VAP播放体验和便捷的资源管理功能。

## 项目截图

![VAP Preview Demo](https://raw.githubusercontent.com/YalongYan/vap-preview/refs/heads/master/assets/demo.png)

![VAP Preview Demo](https://github.com/YalongYan/vap-preview/blob/master/assets/demo2.png?raw=true)

## 主要功能

### 🎯 核心特性
- **双模式支持**: 支持URL输入和本地文件选择两种方式
- **实时预览**: 流畅的VAP视频播放体验
- **播放控制**: 完整的播放器控制功能
- **文件信息**: 详细的VAP文件信息展示

### 📁 输入方式

#### URL方式
- 输入MP4文件和JSON配置文件的远程URL
- 支持在线VAP资源的直接预览
- 适合测试和生产环境使用
- 实时网络资源加载

#### 本地文件方式
- 选择本地的MP4和JSON配置文件
- 支持拖拽和文件选择器
- 适合开发和调试环境使用
- 本地文件快速加载

### 🎮 播放控制
- **播放/暂停/恢复**: 完整的播放控制
- **循环播放**: 可配置的循环播放选项
- **实时状态**: 播放状态实时显示
- **文件信息**: 显示视频尺寸、FPS等详细信息

### 🔧 技术特性
- 基于VAP.js引擎
- 异步文件加载，避免UI阻塞
- 智能错误处理和用户提示
- 响应式设计，支持多种屏幕尺寸

## 使用场景

- **前端开发**: VAP动画效果预览和调试
- **设计师**: 动画效果展示和分享
- **测试人员**: VAP资源质量验证
- **产品经理**: 动画效果演示和评审
- **内容创作者**: VAP资源预览和检查


## 使用方法

### 1. URL方式播放
1. 在"URL方式"卡片中输入MP4和JSON文件的URL
2. 选择是否循环播放
3. 点击"播放"按钮
4. 等待资源加载完成后开始播放

### 2. 本地文件播放
1. 在"本地文件方式"卡片中选择MP4和JSON文件
2. 选择是否循环播放
3. 点击"播放"按钮
4. 文件读取完成后开始播放

### 3. 播放控制
- 使用播放器下方的控制按钮进行播放控制
- 查看实时播放状态和文件信息
- 支持播放、暂停、恢复和销毁操作

## 开发经验分享

### Git Push 小插曲

在项目开发过程中，遇到了一个有趣的Git push问题：

```bash
fatal: unable to access 'https://github.com/YalongYan/vap-preview.git/': Failure when receiving data from the peer
```

**问题分析**: 这是由于网络连接不稳定导致的传输失败，Git缓冲区过小无法处理网络波动。

**解决方案**: 增大Git缓冲区大小
```bash
git config --global http.postBuffer 524288000  # 500MB
```

**经验总结**: 
- 公司内网GitLab通常网络稳定，不需要特殊配置
- GitHub等公网服务可能受到网络环境影响，需要适当调整缓冲区
- 这是一个常见的"网络环境差异"问题，增大缓冲区是有效的解决方案
