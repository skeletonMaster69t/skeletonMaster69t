# Hướng dẫn GIT and GITHUB

* [Hướng dẫn tải và cài Git](#hướng-dẫn-tải-và-cài-git)
* [Kết nối Git với GitHub cá nhân qua SSH key](#kết-nối-git-với-github-cá-nhân-qua-ssh-key)
* [Xây dựng trang cá nhân và thử git, github](#xây-dựng-trang-cá-nhân-và-thử-git-github)
* [Clone dự án Guide_Git_and_Github](#clone-dự-án-httpsgithubcomktlt1-bkguide_git_and_github)


**Git** là **hệ thống quản lý phiên bản** giúp theo dõi thay đổi mã nguồn, làm việc offline và quay lại các phiên bản cũ.

**GitHub** là **nền tảng lưu trữ và chia sẻ mã nguồn** trên internet, xây dựng trên Git, hỗ trợ làm việc nhóm và quản lý dự án.

<img src="https://techvccloud.mediacdn.vn/280518386289090560/2021/3/2/023-1614681588418717257234-0-0-767-1366-crop-16146815915111444794187.png" width="300">

--- 

## Hướng dẫn tải và cài Git

### Nếu cài không được các hướng dẫn dưới thì xem hướng dẫn https://www.youtube.com/watch?v=4FjgUp0zgcM

### 🪟 Windows

1. Vào **[https://git-scm.com](https://git-scm.com)**
2. Chọn **Download for Windows**
3. Cài đặt → **Next liên tục**

### 🍎 macOS (MacBook)

1. Mở **Terminal**
2. Gõ:
```bash
git --version
```
→ Chọn **Install** nếu được hỏi

### Kết quả kiểm tra

```bash
git --version
```

![](../images/git_version.png)

## Kết nối Git với GitHub cá nhân qua SSH key

### Nếu cài không được các hướng dẫn dưới thì xem hướng dẫn https://www.youtube.com/watch?v=2zFbhj7Fykc

### 1. Tạo SSH key

Mở **Terminal / Git Bash**, gõ:

```bash
ssh-keygen -t ed25519 -C "email_github_cua_ban"
```

Nhấn **Enter liên tục** để dùng cấu hình mặc định.

---

### 2. Thêm SSH key vào ssh-agent

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

---

### 3. Copy SSH public key

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy toàn bộ nội dung hiển thị.

---

### 4. Thêm SSH key vào GitHub

Vào GitHub → Settings → SSH and GPG keys → New SSH key → dán key → Save.

https://github.com/settings/ssh/new

<img src="./images/git_ssh_new.png" width="600">

---

### 5. Kiểm tra kết nối

```bash
ssh -T git@github.com
```

![alt text](./images/git_ssh_key.png)

---

## Xây dựng trang cá nhân và thử git, github 

### Xem hướng dẫn `create_profile_instructions.mp4`

### Tạo Profile Repository

1. Đăng nhập vào [GitHub](https://github.com).  
2. Nhấn nút **New Repository**.  
3. **Tên repository phải trùng với username của bạn**.  
   - Ví dụ: username của bạn là `votienbku` → repo tên là **`votienbku`**.  
4. Chọn **Public**.  
5. Tick vào **Add a README file**.  
6. Nhấn **Create repository**.  

---

### Clone dự án từ GitHub về máy bằng Git

1. Mở **Terminal / Git Bash**.
2. Copy link SSH của repository trên GitHub (nút **Code → SSH**).
3. Chạy lệnh:

```bash
git clone git@github.com:username/username.git
```

Ví dụ:

```bash
git clone git@github.com:votienbku/votienbku.git
```

4. Di chuyển vào thư mục project:

```bash
cd username
```

### Chỉnh sửa và push code lên GitHub

1. Mở thư mục repository vừa clone bằng **VS Code** hoặc editor bất kỳ.
2. Chỉnh sửa file `README.md` (ghi thông tin cá nhân, mô tả ngắn…).
3. Kiểm tra trạng thái thay đổi:

```bash
git status
```

4. Thêm các file đã chỉnh sửa vào stage:

```bash
git add .
```

5. Commit thay đổi:

```bash
git commit -m "Update profile README"
```

6. Push code lên GitHub:

```bash
git push origin main
```

<img src="./images/github_profile.png" width="600">

--- 

## Clone dự án [https://github.com/KTLT1-BK/Guide_Git_and_Github](https://github.com/KTLT1-BK/Guide_Git_and_Github)

### Xem hướng dẫn `clone_Guide_Git_and_Github.mp4`

1. Mở **Terminal / Git Bash**.

2. Chạy lệnh clone:

```bash
git clone git@github.com:KTLT1-BK/Guide_Git_and_Github.git
```

3. Di chuyển vào thư mục project:

```bash
cd Guide_Git_and_Github
```

4. Mở vscode :

```bash
code .
```

5. Mở git graph lênh xem (Các dự án sau thì cũng clone như này)

![alt text](./images/git_graph.png)



---
<p align="center">
  <a href="https://www.facebook.com/Shiba.Vo.Tien">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook"/>
  </a>
  <a href="https://www.tiktok.com/@votien_shiba">
    <img src="https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white" alt="TikTok"/>
  </a>
  <a href="https://www.facebook.com/groups/khmt.ktmt.cse.bku?locale=vi_VN">
    <img src="https://img.shields.io/badge/Facebook%20Group-4267B2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook Group"/>
  </a>
  <a href="https://www.facebook.com/CODE.MT.BK">
    <img src="https://img.shields.io/badge/Page%20CODE.MT.BK-0057FF?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook Page"/>
  </a>
  <a href="https://github.com/VoTienBKU">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>
