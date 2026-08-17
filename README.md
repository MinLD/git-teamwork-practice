# Git Teamwork Practice

Mini Vue 3 + Vite project dùng để thực hành Git teamwork.

## Chạy project

```bash
npm install
npm run dev
```

## Bài tập Git đề xuất

Giả lập team có các branch chung:

- `main`: branch ổn định, không code trực tiếp.
- `FE`: branch tích hợp của frontend.
- Branch cá nhân/task: tạo từ `FE`.

### Task 1 — Status filter

Tạo branch:

```bash
git switch FE
git pull origin FE
git switch -c <ten-ban>/feat-status-filter
```

Yêu cầu: thêm select lọc `TODO`, `IN_PROGRESS`, `DONE`.

### Task 2 — Stats cards

Tạo branch riêng từ `FE`.

Yêu cầu: hiển thị tổng project, số TODO, IN_PROGRESS và DONE.

### Task 3 — Add project modal

Tạo branch riêng từ `FE`.

Yêu cầu: nút `+ New Project` mở modal và thêm project mới vào list.

### Task 4 — Dark mode

Tạo branch riêng từ `FE`.

Yêu cầu: thêm nút bật/tắt dark mode.

### Task 5 — Conflict exercise

Hai người/2 branch cùng sửa dòng tiêu đề `Mini Project Board` thành hai nội dung khác nhau, sau đó merge để cố tình tạo conflict và giải quyết conflict.

## Commit convention gợi ý

```text
feat: add status filter
fix: fix empty state
style: improve project card spacing
refactor: extract project toolbar
```

Test protected main branch.
