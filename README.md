# learn-file-storage-s3-golang-starter (Tubely)

This repo contains the starter code for the Tubely application - the #1 tool for engagement bait - for the "Learn File Servers and CDNs with S3 and CloudFront" [course](https://www.boot.dev/courses/learn-file-servers-s3-cloudfront-golang) on [boot.dev](https://www.boot.dev)

## Quickstart

*This is to be used as a *reference\* in case you need it, you should follow the instructions in the course rather than trying to do everything here.

## 1. Install dependencies

- [Go](https://golang.org/doc/install)
- `go mod download` to download all dependencies
- [FFMPEG](https://ffmpeg.org/download.html) - both `ffmpeg` and `ffprobe` are required to be in your `PATH`.

```bash
# linux
sudo apt update
sudo apt install ffmpeg

# mac
brew update
brew install ffmpeg
```

- [SQLite 3](https://www.sqlite.org/download.html) only required for you to manually inspect the database.

```bash
# linux
sudo apt update
sudo apt install sqlite3

# mac
brew update
brew install sqlite3
```

- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

## 2. Download sample images and videos

```bash
./samplesdownload.sh
# samples/ dir will be created
# with sample images and videos
```

## 3. Configure environment variables

Copy the `.env.example` file to `.env` and fill in the values.

```bash
cp .env.example .env
```

You'll need to update values in the `.env` file to match your configuration, but _you won't need to do anything here until the course tells you to_.

## 3. Run the server

```bash
go run .
```

- You should see a new database file `tubely.db` created in the root directory.
- You should see a new `assets` directory created in the root directory, this is where the images will be stored.
- You should see a link in your console to open the local web page.

# Leon Thomas Added

## JS前端 + Go后端 + AWS SDK + Sqlite3 搭建视频存储平台.      
### 模块：      
     Video Streaming : The native HTML5 <video> element. It streams video files by default as long as the server supports it.
     AWS S3 Bucket 云存储服务器      
     Sqlite3 本地存储 video metadata, UserID ,进行用户校验（视频所有权校验）            
     Go：             
        标准库：[os, net/http, log, crypto, context]       
        三方库：[aws-sdk-go-v2, godotenv(解析.env文件), ]         
        工具链：[Sqlc 数据库代码生成工具,      
                插入bash命令以使用ffmpeg视频处理工具进行视频横纵比解析]          

### 功能：注册，登录          
     创建视频(Video Title，Description)          
     支持存储 - 视频微缩图+视频源文件 > 网页显示        
     
### 草稿：    
    JWT uuid 验证User， 加密          
    AWS s3 bucket as cloud File-Storage             
    use ffmpeg               

