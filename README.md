# minislims

The absolute minimal SLiMS 9 Bulian setup with FrankenPHP - one command to rule them all.

**Created by:** muzub  
**Date:** 2025-05-16 04:25:12  
**Purpose:** For full stack developers building AI applications

## ⚡ One Command Setup (Windows)

```powershell
# Copy and paste this SINGLE command in PowerShell (run as Administrator)
mkdir minislims; cd minislims; Invoke-WebRequest -Uri "https://github.com/slims/slims9_bulian/archive/refs/heads/master.zip" -OutFile "slims.zip"; Expand-Archive -Path "slims.zip" -DestinationPath "."; mkdir slims; Move-Item -Path "slims9_bulian-master\*" -Destination "slims\" -Force; Remove-Item -Path "slims9_bulian-master" -Recurse -Force; Remove-Item -Path "slims.zip" -Force; Invoke-WebRequest -Uri "https://raw.githubusercontent.com/muzub/minislims/main/docker-compose.yml" -OutFile "docker-compose.yml"; docker compose up -d
```

## 📋 Repository Contents

```
minislims/
├── README.md           # This file - minimal instructions
└── docker-compose.yml  # All-in-one Docker configuration
```

## 🚀 Installation

That's it! Just run the one command above and access:
- SLiMS: http://127.0.0.1:8080
- Admin: http://127.0.0.1:8080/admin/ (admin/admin)

## 🛠️ DB Connection Parameters

Database parameters for your AI applications:
- Host: `localhost` 
- Port: `3306`
- User: `slims`
- Password: `slims`
- Database: `slims`

---

**Note:** Security-sensitive values like passwords are kept simple for development. Change these in production environments.
