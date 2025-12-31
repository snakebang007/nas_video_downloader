# 📥 视频下载助手 | Video Downloader

[English](#english) | [中文](#中文)

---

<a name="中文"></a>
## 🇨🇳 中文

一个 Docker 容器化的视频/图集下载工具，支持抖音、小红书、B站、YouTube 等主流平台。专为 NAS 用户设计，也可部署在任何支持 Docker 的环境中。

### ✨ 功能特点

- 🎬 **多平台支持**: 抖音、小红书、哔哩哔哩
- 📷 **视频+图集**: 同时支持视频下载和图集提取
- 🔗 **智能解析**: 自动识别分享文本中的链接，自动处理短链重定向
- 📱 **移动端优化**: 响应式设计，手机浏览器完美适配
- 🖥️ **NAS 下载**: 支持直接下载到服务器存储
- 🔐 **用户认证**: 内置登录系统，支持两步验证(2FA)
- 🐳 **多架构支持**: 同时支持 amd64 和 arm64

### 📦 快速开始

#### Docker 运行

```bash
# 拉取镜像
docker pull snakebang007/video-downloader:latest

# 运行容器
docker run -d \
  --name video-downloader \
  -p 5000:5000 \
  -v /your/data/path:/app/data/downloads \
  snakebang007/video-downloader:latest
```

#### Docker Compose

```yaml
version: '3'
services:
  video-downloader:
    image: snakebang007/video-downloader:latest
    container_name: video-downloader
    ports:
      - "5000:5000"
    volumes:
      - ./data:/app/data/downloads
    restart: unless-stopped
```

### 🔧 配置说明

| 环境变量 | 默认值 | 说明 |
|---------|--------|------|
| `PORT` | 5000 | 服务端口 |

| 挂载目录 | 说明 |
|---------|------|
| `/app/data/downloads` | 数据目录（下载文件） |

### 🚀 首次使用

1. 访问 `http://your-server:5000`
2. 默认管理员账号: `admin` / `admin`
3. **首次登录后请立即修改密码**

### 📱 使用方式

1. **解析模式**: 粘贴链接 → 解析 → 在线预览/下载到手机
2. **下载模式**: 粘贴链接 → 下载到服务器 → 通过 NAS 访问

### 🛠️ 本地开发


### 📝 支持的平台

| 平台 | 视频 | 图集 | 状态 |
|------|:----:|:----:|:----:|
| 抖音 | ✅ | ✅ | 已完成 |
| 小红书 | ✅ | ✅ | 已完成 |
| 哔哩哔哩 | ✅ | ✅ | 已支持 |

### 📄 许可证

MIT License

---

<a name="english"></a>
## 🇺🇸 English

A Docker-based video/image downloader supporting Douyin (TikTok China), Xiaohongshu (RedNote), Bilibili, YouTube, and more. Designed for NAS users but works in any Docker environment.

### ✨ Features

- 🎬 **Multi-platform**: Douyin, Xiaohongshu, Bilibili
- 📷 **Video + Images**: Support both video download and image gallery extraction
- 🔗 **Smart Parsing**: Auto-detect links from share text, handle short URL redirects
- 📱 **Mobile Optimized**: Responsive design, perfect for mobile browsers
- 🖥️ **NAS Download**: Download directly to server storage
- 🔐 **Authentication**: Built-in login system with 2FA support
- 🐳 **Multi-arch**: Supports both amd64 and arm64

### 📦 Quick Start

#### Docker Run

```bash
# Pull image
docker pull snakebang007/video-downloader:latest

# Run container
docker run -d \
  --name video-downloader \
  -p 5000:5000 \
  -v /your/data/path:/app/data/downloads \
  snakebang007/video-downloader:latest
```

#### Docker Compose

```yaml
version: '3'
services:
  video-downloader:
    image: snakebang007/video-downloader:latest
    container_name: video-downloader
    ports:
      - "5000:5000"
    volumes:
      - ./data:/app/data/downloads
    restart: unless-stopped
```

### 🔧 Configuration

| Environment Variable | Default | Description |
|---------------------|---------|-------------|
| `PORT` | 5000 | Service port |

| Volume | Description |
|--------|-------------|
| `/app/data/downloads` | Data directory (database + downloads) |

### 🚀 First Time Setup

1. Visit `http://your-server:5000`
2. Default admin account: `admin` / `admin`
3. **Change password immediately after first login**

### 📱 Usage

1. **Parse Mode**: Paste link → Parse → Preview online / Download to phone
2. **Download Mode**: Paste link → Download to server → Access via NAS

### 🛠️ Local Development

```bash
# Clone repository
git clone https://github.com/snakebang007/docker_app_downloader.git
cd docker_app_downloader

# Install dependencies
pip install -r requirements.txt

# Run
python run.py
```

### 📝 Supported Platforms

| Platform | Video | Images | Status |
|----------|:-----:|:------:|:------:|
| Douyin | ✅ | ✅ | Complete |
| Xiaohongshu | ✅ | ✅ | Complete |
| Bilibili | ✅ | ✅ | Supported |

### 📄 License

MIT License

---

## 🔗 Links

- **GitHub**: [https://github.com/snakebang007/nas_video_downloader.git](https://github.com/snakebang007/nas_video_downloader.git)
- **Docker Hub**: [https://hub.docker.com/r/snakebang007/video-downloader](https://hub.docker.com/r/snakebang007/video-downloader)

---

Made with ❤️ by 一晌贪欢
