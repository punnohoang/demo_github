# demo_github
I-II.Sử dụng git command line, commitlint
1.	Tải, Clone Git, khởi tạo, kiểm tra trạng thái
-	Tải git, cấu hình global: …
git config --global user.name "Phong"
git config --global user.email "mailgit@email.com"
-	Xem version : git –version
-	Clone : git clone https://link repository
-	Khởi tạo file .git: git init
-	Trạng thái: git status
-	.gitignore để bỏ qua tệp, ko theo dõi sự thay đổi của nó ( không đưa lên git)
2.	Nhánh, git branch
-	Xem nhánh: git branch
-	Tạo nhánh: git checkout -b tên_nhánh
-	Chuyển nhánh: git checkout tên_nhánh
3.	Thêm file
-	Thêm file: git add file1.txt file2.txt img_001.jpg
-	Thêm tất file: git add .
-	Quay lại: git reset HEAD – file1.txt
4.	Git commit ( theo commitlint, conventional)
<type>: <short message>

Type	Ý nghĩa
feat	Thêm tính năng mới
fix	Sửa bug
docs	Tài liệu
style	Format, không đổi logic
refactor	Refactor code
test	Thêm test
chore	Việc lặt vặt, update config

style: cap nhat noi dung in ra cua file hello.py
docs: cap nhat vi du trong hello.py
5.	Xem lịch sử các lần commit 
-	Tất cả: git log
-	Xem tóm gọn trên 1 dòng: git log –oneline
-	Xem n lần gần nhất: git log -số ( vd git log -2)
6.	Push
-	Lần đầu: git push -u origin main
-	Các lần sau: git push
7.	Quay lại commit trước
-	git log --oneline ( để xem lịch suẻ commit)
-	giữ nguyên thay đổi: git reset --soft mã_commit
-	xóa sạch thay đổi sau nó: git reset –hard mã_commit
8.	xử lý khi bị conflict
Xử lý xung đột (Conflicts)
Nếu git rebase gặp xung đột, nó sẽ dừng lại và yêu cầu bạn giải quyết.
•	Sửa các file bị xung đột.
•	Sử dụng git add <file> để đánh dấu là đã giải quyết.
•	Tiếp tục quá trình rebase: git rebase --continue
•	Nếu bạn muốn bỏ rebase và quay lại trạng thái ban đầu: git rebase --abort

III. Sử dụng GitHub: pull request, comments, reviews, approvals

Branch → Commit → Push → Pull Request → Review → Approve → Merge
1.	Khi tạo nhánh làm việc và hoàn thiện xong phần push code lên github, trên git hub sẽ có Pull Request (Compare & Pull Request)
-	Pull request Title ( viết theo yêu cầu)
-	Decription: Đã làm gì, để làm gì?
2.	Người review sẽ thấy và yêu cầu sửa lỗi nếu có, người làm sửa và push lại đến khi được chấp nhận mới gộp vào main 
