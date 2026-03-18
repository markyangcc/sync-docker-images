# DockerHUb 镜像同步到阿里云 ACR

将 Docker Hub 镜像自动同步至阿里云容器镜像服务（ACR）

## 使用方式

### 手动触发单个镜像

GitHub → Actions → `Sync Docker Images to Aliyun ACR` → Run workflow → 填入 `nginx:1.27`

### 自动同步

每次修改 `image.txt` 并推送到 main 分支后，GitHub Actions 会自动触发，将列表中所有镜像同步到阿里云 ACR。

