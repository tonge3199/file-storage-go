Here's a revised `README.md` that reflects your ownership of the project while keeping the original structure and useful info. I've updated the intro, clarified your role, and made it more suitable for showcasing your project to others:

---

# Tubely - Video Storage Platform with Go + AWS S3 + SQLite

Tubely is a simple but powerful video storage and streaming platform built using **Go**, **AWS S3**, and **SQLite**. It supports video upload, metadata storage, thumbnail generation, and playback – all wrapped in a clean and modern stack.

> 💡 Originally inspired by the Boot.dev course ["Learn File Servers and CDNs with S3 and CloudFront"](https://www.boot.dev/courses/learn-file-servers-s3-cloudfront-golang), this project has been fully adapted, expanded, and maintained by **Leon Thomas**.

---

## Features

- 📦 Upload and store videos with thumbnails
- 🧾 SQLite-based video metadata and user management
- 🌐 Simple front-end using native HTML5 `<video>` tag
- 🔐 JWT-based user authentication (WIP)
- ☁️ Cloud file storage with AWS S3
- 🎞️ Video processing with `ffmpeg` (aspect ratio, thumbnails)
- 🛠️ Built with Go and the AWS SDK (v2)

---

## Tech Stack

- **Frontend:** Basic HTML/CSS + JS
- **Backend:** Go
  - Standard Libraries: `net/http`, `os`, `log`, `crypto`, `context`
  - Third-Party: `aws-sdk-go-v2`, `godotenv`
- **Storage:**
  - Local: SQLite3 (for metadata, users, auth)
  - Cloud: AWS S3 Bucket (video + thumbnail storage)
- **Tools:**
  - `ffmpeg`, `ffprobe` for video parsing & thumbnail generation
  - `sqlc` for type-safe database queries

---

## Quickstart

> ⚠️ While this README gives you a fast overview, **follow the course or setup guide** for in-depth instructions.

### 1. Install dependencies

- [Go](https://golang.org/doc/install)
- Run:  
  ```bash
  go mod download
  ```

- [SQLite3](https://www.sqlite.org/download.html)
  ```bash
  # Linux
  sudo apt update && sudo apt install sqlite3

  # macOS
  brew update && brew install sqlite3
  ```

- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

---

### 2. Download Sample Videos

```bash
./samplesdownload.sh
```

Creates a `/samples` folder containing demo videos and images.

---

### 3. Configure Environment

Copy and configure the environment variables:

```bash
cp .env.example .env
```

Fill in your AWS credentials, S3 bucket name, etc. Follow prompts in the app or course instructions.

---

### 4. Run the Server

```bash
go run .
```

This will:

- Create a `tubely.db` file (SQLite database)
- Create an `assets/` folder for storing thumbnails
- Start a local server with a link to access the site

---

## Roadmap

- [x] Video upload to S3
- [x] Metadata storage in SQLite
- [x] Basic UI with video player
- [ ] JWT user auth system
- [ ] User dashboard to manage uploads
- [ ] S3 file expiration / cleanup

---

## License

MIT

---
