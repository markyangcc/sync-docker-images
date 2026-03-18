# DockerHub 镜像同步到阿里云 ACR

将 Docker Hub 镜像自动同步至阿里云容器镜像服务（ACR）

## 使用方式

### 手动触发单个镜像

- **amd64**：GitHub → Actions → `Sync Docker Images to Aliyun ACR (amd64/x86_64)` → Run workflow → 填入 `nginx:1.27`
- **arm64**：GitHub → Actions → `Sync Docker Images to Aliyun ACR (ARM64)` → Run workflow → 填入 `nginx:1.27`

### 自动同步

每次修改对应的镜像列表文件并推送到 main 分支后，GitHub Actions 会自动触发，将列表中所有镜像同步到阿里云 ACR。

| 架构 | 镜像列表文件 |
|------|-------------|
| amd64 | `images.txt` |
| arm64 | `images_arm64.txt` |

> arm64 镜像推送到ACR时 tag 会自动添加 `-arm64` 后缀，例如 `nginx:1.27` → `nginx:1.27-arm64`