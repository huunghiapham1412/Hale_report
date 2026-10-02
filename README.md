# Hale_report

NVCC → Virginia Tech Transfer & Graduation Dashboard
📌 Giới thiệu
NVCC → Virginia Tech Transfer & Graduation Dashboard là một web dashboard tương tác được xây dựng để theo dõi tiến độ học tập, kiểm tra các yêu cầu tốt nghiệp và mô phỏng lộ trình chuyển tiếp từ Northern Virginia Community College (NVCC) sang Virginia Tech (VT) ngành B.S. Computer Science.
Project được thiết kế theo hướng trực quan, giúp người dùng nhanh chóng xem:
• Tiến độ hoàn thành các chương trình A.S.
• GPA và số tín chỉ đã hoàn thành.
• Các môn còn thiếu để tốt nghiệp.
• Lộ trình transfer sang Virginia Tech.
• Đối chiếu môn học giữa NVCC và Virginia Tech.
• Lịch sử học tập theo từng học kỳ.
• Mô phỏng việc đăng ký các môn học trong học kỳ tiếp theo.
Lưu ý: Dữ liệu học tập và lộ trình trong dashboard là dữ liệu được hard-code trong project nhằm phục vụ mục đích trình bày/mô phỏng. Người dùng nên đối chiếu với Degree Audit, catalog và thông tin chính thức của trường trước khi sử dụng cho quyết định học tập thực tế.
—————
✨ Tính năng chính

1. Student Overview
   Dashboard hiển thị thông tin tổng quan ngay trên trang chính:
   • GPA tích lũy.
   • Tổng số tín chỉ đã hoàn thành.
   • Chương trình đang theo học.
   • Mục tiêu transfer.
   • Phần trăm tiến độ của từng major.
   Hai chương trình A.S. được theo dõi gồm:
   • Science / Mathematics (880-02)
   • Computer Science (2460)
   —————
2. Virginia Tech Transfer Roadmap
   Tab Virginia Tech CS (Fall 2027) cung cấp một roadmap chuyển tiếp gồm:
   • Thông tin chương trình B.S. Computer Science.
   • Kiểm tra các điều kiện GPA.
   • Tình trạng bằng cấp NVCC.
   • Kiểm tra các môn học bắt buộc.
   • Bảng đối chiếu môn học NVCC ↔ Virginia Tech.
   • Các môn đang học và các môn dự kiến đăng ký.
   • Timeline chuẩn bị hồ sơ transfer.
   Project hiện mô phỏng lộ trình:
   NVCC → Virginia Tech → B.S. Computer Science → Fall 2027
   —————
3. Degree Audit – Science / Mathematics
   Tab Science / Mathematics (880-02) chia yêu cầu chương trình thành nhiều nhóm:
   • Core Requirements.
   • Mathematics Core & Electives.
   • Physical / Life Science có lab.
   • General Education Electives.
   Mỗi môn được hiển thị trạng thái như:
   • ✅ Completed
   • ⏳ In Progress
   • ❌ Required / Missing
   Dashboard cũng hiển thị số tín chỉ còn thiếu để hoàn thành chương trình.
   —————
4. Degree Audit – Computer Science
   Tab Computer Science (2460) tập trung vào các yêu cầu của chương trình A.S. Computer Science.
   Các nhóm chính gồm:
   • Computer Science Core.
   • Science & Mathematics Requirements.
   • Humanities & Social Sciences.
   Một trong những môn được đánh dấu quan trọng trong roadmap là:
   CSC 223 – Data Structures and Analysis of Algorithms
   —————
5. Interactive Graduation Planner
   Tab Interactive Planner cho phép người dùng chọn các môn dự kiến đăng ký và xem dashboard cập nhật tiến độ.
   Hai lựa chọn chính trong simulation:
   • CSC 223 – Data Structures and Analysis of Algorithms
   • CHM 112 – General Chemistry II hoặc lựa chọn Science tương đương được dashboard mô phỏng.
   Khi checkbox được thay đổi, JavaScript sẽ tự động:
6. Tính lại số tín chỉ.
7. Tính phần trăm hoàn thành.
8. Cập nhật progress bar.
9. Cập nhật trạng thái còn thiếu.
10. Hiển thị thông báo khi đạt trạng thái mô phỏng hoàn thành.
    —————
11. Course History
    Tab Course History hiển thị lịch sử các môn học dưới dạng bảng.
    Các cột bao gồm:
    Trường
    Mô tả

Term
Học kỳ

Course Code
Mã môn

Course Title
Tên môn

Credits
Số tín chỉ

Grade
Điểm

Status
Trạng thái

Danh sách môn được lưu trong JavaScript dưới dạng array object.
————— 7. Course Search / Filter
Course History có ô tìm kiếm cho phép lọc theo:
• Course code.
• Course name.
• Term.
Bộ lọc được xử lý hoàn toàn bằng JavaScript ở phía client, không cần backend.
—————
🛠️ Công nghệ sử dụng
Project hiện được xây dựng chủ yếu bằng front-end technologies:
HTML5
HTML được sử dụng để xây dựng cấu trúc của dashboard, các card, bảng dữ liệu, navigation tabs và các section nội dung.
Tailwind CSS
Project sử dụng Tailwind CSS CDN để xây dựng giao diện responsive và utility-based styling.
JavaScript
JavaScript xử lý các chức năng tương tác như:
• Tab switching.
• Course table rendering.
• Course search.
• Interactive graduation simulation.
• Dynamic progress calculation.
• Checkbox-based updates.
Font Awesome
Font Awesome được sử dụng để cung cấp icon cho:
• Education.
• Computer Science.
• Mathematics.
• Science.
• Search.
• Status indicators.
• Navigation.
Chart.js
Project có tích hợp Chart.js để hỗ trợ visualization trong giao diện.
Google Fonts
Project sử dụng font Inter cho typography.
—————
📂 Cấu trúc project
Project hiện có thể chạy dưới dạng một single-page application đơn giản:
project/
│
└── index.html
Toàn bộ:
• HTML
• CSS configuration
• JavaScript
• Course dataset
• Interactive functions
được đặt trong index.html.
—————
🚀 Cách chạy project
Cách 1 – Mở trực tiếp
Download hoặc clone project về máy, sau đó mở:
index.html
bằng trình duyệt web.
Cách 2 – VS Code + Live Server
Nếu sử dụng Visual Studio Code:

1. Mở folder project.
2. Mở index.html.
3. Cài extension Live Server nếu chưa có.
4. Click chuột phải vào index.html.
5. Chọn Open with Live Server.
   Project sẽ chạy trực tiếp trên trình duyệt.
   —————
   💻 Không cần backend
   Project hiện không sử dụng:
   • Database.
   • Node.js server.
   • REST API.
   • Authentication.
   • Backend framework.
   Dữ liệu course history và các thông số degree audit được lưu trực tiếp trong JavaScript.
   Điều này giúp project:
   • Dễ chạy.
   • Dễ demo.
   • Không cần cấu hình server.
   • Phù hợp cho portfolio hoặc academic project.
   —————
   🎨 Thiết kế giao diện
   Giao diện sử dụng phong cách dashboard hiện đại với:
   • Responsive layout.
   • Card-based UI.
   • Progress bars.
   • Status badges.
   • Gradient headers.
   • Sticky navigation.
   • Tables.
   • Interactive tabs.
   • Mobile-friendly layout.
   Màu sắc được tùy chỉnh để tạo sự liên kết trực quan giữa NVCC và Virginia Tech.
   —————
   📊 Logic mô phỏng tiến độ
   Dashboard sử dụng các giá trị tín chỉ cơ sở và cộng thêm tín chỉ dựa trên lựa chọn của người dùng.
   Ví dụ, logic JavaScript mô phỏng:
   let mathCredits = 54;

if (csc223) mathCredits += 3;
if (chm112) mathCredits += 4;

let mathPercent = Math.min(
100,
(mathCredits / 60) \* 100
);
Tương tự, tiến độ Computer Science được tính lại dựa trên các môn được chọn.
Đây là simulation logic, không phải hệ thống Degree Audit chính thức của trường.
—————
🔍 Data Model
Course history được lưu theo cấu trúc object:
{
term: '2026 Fall',
code: 'CHM 111',
name: 'General Chemistry I',
credits: 4.0,
grade: 'IP',
status: 'In Progress'
}
Các field chính:
• term
• code
• name
• credits
• grade
• status
Cách tổ chức này giúp việc filter và render bảng bằng JavaScript đơn giản hơn.
—————
🔄 Các hàm JavaScript chính
renderCourseTable(courses)
Render danh sách course vào HTML table.
filterCourses()
Lọc course history dựa trên nội dung người dùng nhập vào search box.
switchTab(tabId)
Ẩn/hiện các tab và cập nhật trạng thái active của navigation.
updateSimulation()
Tính toán lại tiến độ Science/Math và Computer Science dựa trên các môn người dùng chọn.
—————
📅 Transfer Timeline
Dashboard mô phỏng timeline cho mục tiêu Fall 2027, bao gồm:

1. Chuẩn bị hồ sơ.
2. Chuẩn bị và nộp application.
3. Theo dõi kết quả admission.
4. Hoàn thành NVCC.
5. Gửi final transcript.
6. Chuẩn bị nhập học Virginia Tech.
   Các mốc thời gian được hard-code trong giao diện và cần được xác minh lại với lịch chính thức khi sử dụng thực tế.
   —————
   📱 Responsive Design
   Giao diện được xây dựng theo hướng responsive và sử dụng các breakpoint của Tailwind CSS.
   Project hỗ trợ:
   • Desktop.
   • Laptop.
   • Tablet.
   • Mobile.
   Các bảng lớn sử dụng horizontal scrolling trên màn hình nhỏ để tránh làm vỡ layout.
   —————
   🔐 Privacy & Security
   Project hiện chứa dữ liệu học tập được hard-code trực tiếp trong index.html.
   Nếu publish project public trên GitHub, nên cân nhắc:
   • Xóa Student ID.
   • Xóa thông tin cá nhân không cần thiết.
   • Không commit transcript thật.
   • Không đưa thông tin đăng nhập vào source code.
   • Không đưa API key hoặc secret vào JavaScript.
   Đối với portfolio public, nên sử dụng dữ liệu demo/anonymized data.
   —————
   ⚠️ Limitations
   Project hiện tại là một client-side dashboard / simulation, vì vậy có một số giới hạn:
7. Dữ liệu không tự động cập nhật từ NVCC.
8. Không kết nối trực tiếp với Virginia Tech.
9. Không có database.
10. Không có user authentication.
11. Degree requirements được lưu dưới dạng static data.
12. Transfer requirements cần được xác minh lại với nguồn chính thức.
13. Progress calculation chỉ phản ánh logic được lập trình trong project.
14. Các deadline trong dashboard có thể thay đổi theo từng admission cycle.
    —————
    🔮 Future Improvements
    Một số hướng phát triển tiếp theo:
    Backend
    • Node.js / Express.
    • Database PostgreSQL hoặc MongoDB.
    • REST API.
    Authentication
    • Student login.
    • Admin dashboard.
    • Role-based access control.
    Data Management
    • Import transcript từ CSV/PDF.
    • CRUD courses.
    • Dynamic degree requirements.
    • Automatic GPA calculation.
    Advanced Transfer Planning
    • Transfer equivalency database.
    • Degree requirement checker.
    • Prerequisite validation.
    • Semester-by-semester planning.
    • Graduation date estimation.
    Visualization
    • GPA chart.
    • Credits completed vs. remaining.
    • Semester workload chart.
    • Transfer requirement progress chart.
    Deployment
    Có thể deploy project bằng:
    • GitHub Pages.
    • Netlify.
    • Vercel.
    • Cloudflare Pages.
    —————
    🧪 Testing Checklist
    Trước khi deploy, nên kiểm tra:
    • ☐ Tất cả tabs chuyển đổi chính xác.
    • ☐ Course search hoạt động.
    • ☐ Course table render đúng.
    • ☐ Checkbox planner cập nhật progress.
    • ☐ Responsive layout trên mobile.
    • ☐ Không có lỗi JavaScript trong Console.
    • ☐ CDN resources load bình thường.
    • ☐ Không còn dữ liệu cá nhân trước khi public repository.
    —————
    📌 Project Status
    Status: Active / Prototype
    Project hiện phù hợp cho:
    • Academic project.
    • Portfolio.
    • Personal academic planning.
    • Front-end JavaScript demonstration.
    • Interactive dashboard demonstration.
    —————
    👨‍💻 Author
    Thi Thu Ha Le
    Academic Planning Dashboard
    Northern Virginia Community College → Virginia Tech
    —————
    📄 License
    Nếu project được public trên GitHub, nên thêm một license rõ ràng, ví dụ:
    • MIT License – nếu muốn người khác có thể sử dụng và sửa đổi project.
    • Apache 2.0 – nếu muốn license rõ ràng hơn về patent và redistribution.
    • Proprietary / All Rights Reserved – nếu không muốn người khác sử dụng source code.
    Hiện tại project chưa xác định license chính thức, vì vậy không nên tự động tuyên bố một license cụ thể nếu chưa có quyết định của author.
    —————
    🙏 Acknowledgments
    Project sử dụng các thư viện/CDN bên thứ ba được khai báo trong index.html, bao gồm:
    • Tailwind CSS
    • Font Awesome
    • Chart.js
    • Google Fonts (Inter)
    Các thư viện này được sử dụng để hỗ trợ styling, icons, visualization và typography của giao diện.
