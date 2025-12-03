<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Cá Nhân - Wireframe</title>
    <style>
        /* Reset và font chữ cơ bản */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f5f5;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header */
        header {
            background-color: #fff;
            border-bottom: 2px solid #ddd;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
            padding: 5px;
            border: 2px solid #333;
            display: inline-block;
        }
        
        /* Menu Desktop */
        .desktop-menu {
            display: flex;
            list-style: none;
        }
        
        .desktop-menu li {
            margin-left: 25px;
        }
        
        .desktop-menu a {
            text-decoration: none;
            color: #333;
            font-weight: bold;
            padding: 5px 10px;
            border: 1px solid transparent;
        }
        
        .desktop-menu a:hover {
            border: 1px solid #333;
        }
        
        /* Hamburger Menu (Mobile) */
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            width: 30px;
            height: 20px;
            justify-content: space-between;
        }
        
        .hamburger-line {
            width: 100%;
            height: 3px;
            background-color: #333;
        }
        
        .mobile-menu {
            display: none;
            position: absolute;
            top: 70px;
            left: 0;
            width: 100%;
            background-color: #fff;
            border-top: 1px solid #ddd;
            box-shadow: 0 5px 10px rgba(0,0,0,0.1);
        }
        
        .mobile-menu.active {
            display: block;
        }
        
        .mobile-menu ul {
            list-style: none;
        }
        
        .mobile-menu li {
            border-bottom: 1px solid #eee;
        }
        
        .mobile-menu a {
            display: block;
            padding: 15px;
            text-decoration: none;
            color: #333;
            font-weight: bold;
        }
        
        /* Hero Section */
        .hero {
            background-color: #fff;
            padding: 60px 0;
            text-align: center;
            border-bottom: 2px solid #ddd;
            margin-bottom: 40px;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            padding: 10px;
            border: 2px solid #333;
            display: inline-block;
        }
        
        .hero p {
            max-width: 600px;
            margin: 0 auto 30px;
            padding: 10px;
        }
        
        .cta-button {
            display: inline-block;
            padding: 12px 30px;
            background-color: #fff;
            border: 2px solid #333;
            text-decoration: none;
            color: #333;
            font-weight: bold;
            margin-top: 10px;
        }
        
        /* Main Content */
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        /* Introduction Section */
        .intro {
            flex: 1;
            min-width: 300px;
            background-color: #fff;
            padding: 30px;
            border: 2px solid #ddd;
        }
        
        .intro h2 {
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ddd;
        }
        
        .content-columns {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 20px;
        }
        
        .column {
            flex: 1;
            min-width: 200px;
            padding: 15px;
            border: 1px solid #ddd;
            background-color: #f9f9f9;
        }
        
        .column h3 {
            margin-bottom: 10px;
        }
        
        /* Sidebar (for inner pages) */
        .sidebar {
            width: 300px;
            background-color: #fff;
            padding: 30px;
            border: 2px solid #ddd;
        }
        
        .sidebar h2 {
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ddd;
        }
        
        .sidebar ul {
            list-style: none;
        }
        
        .sidebar li {
            margin-bottom: 15px;
            padding: 10px;
            border: 1px solid #eee;
        }
        
        /* Footer */
        footer {
            background-color: #fff;
            border-top: 2px solid #ddd;
            padding: 40px 0;
            margin-top: 40px;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ddd;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-link {
            display: inline-block;
            width: 40px;
            height: 40px;
            border: 1px solid #333;
            text-align: center;
            line-height: 40px;
            text-decoration: none;
            color: #333;
            font-weight: bold;
        }
        
        /* Utility Classes */
        .placeholder {
            background-color: #eee;
            border: 1px dashed #aaa;
            padding: 15px;
            text-align: center;
            color: #666;
            margin: 10px 0;
        }
        
        .divider {
            height: 2px;
            background-color: #ddd;
            margin: 30px 0;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .main-content {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                order: 2;
            }
            
            .intro {
                order: 1;
            }
        }
        
        @media (max-width: 768px) {
            /* Ẩn menu desktop, hiện hamburger */
            .desktop-menu {
                display: none;
            }
            
            .hamburger {
                display: flex;
            }
            
            /* Điều chỉnh hero cho mobile */
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .hero {
                padding: 40px 0;
            }
            
            /* Chuyển các cột thành chồng lên nhau */
            .content-columns {
                flex-direction: column;
            }
            
            /* Điều chỉnh footer */
            .footer-content {
                flex-direction: column;
            }
            
            /* Tăng kích thước nút cho dễ chạm */
            .cta-button {
                padding: 15px 35px;
                min-width: 200px;
            }
            
            .mobile-menu a {
                padding: 18px 15px;
            }
        }
        
        /* View Toggle (for demonstration) */
        .view-toggle {
            text-align: center;
            margin: 20px 0;
            padding: 10px;
            background-color: #fff;
            border: 2px solid #ddd;
        }
        
        .toggle-button {
            padding: 8px 16px;
            margin: 0 5px;
            background-color: #fff;
            border: 1px solid #333;
            cursor: pointer;
            font-weight: bold;
        }
        
        .toggle-button.active {
            background-color: #333;
            color: #fff;
        }
        
        .mobile-view {
            display: none;
            max-width: 400px;
            margin: 0 auto;
            border: 3px solid #333;
            min-height: 600px;
            position: relative;
            overflow: hidden;
        }
        
        .desktop-view {
            display: block;
        }
    </style>
</head>
<body>
    <!-- View Toggle (Chỉ để demo) -->
    <div class="view-toggle">
        <button class="toggle-button active" onclick="showView('desktop')">Desktop View</button>
        <button class="toggle-button" onclick="showView('mobile')">Mobile View</button>
        <p><small><em>(Chức năng này chỉ để minh họa. Trong thực tế, responsive CSS sẽ tự động điều chỉnh)</em></small></p>
    </div>
    
    <!-- Desktop View -->
    <div id="desktop-view" class="desktop-view">
        <!-- Header -->
        <header>
            <div class="container header-content">
                <div class="logo">LOGO</div>
                <nav>
                    <ul class="desktop-menu">
                        <li><a href="#">Trang Chủ</a></li>
                        <li><a href="#">Giới Thiệu</a></li>
                        <li><a href="#">Dự Án</a></li>
                        <li><a href="#">Bài Viết</a></li>
                        <li><a href="#">Liên Hệ</a></li>
                    </ul>
                    <div class="hamburger" onclick="toggleMobileMenu()">
                        <div class="hamburger-line"></div>
                        <div class="hamburger-line"></div>
                        <div class="hamburger-line"></div>
                    </div>
                </nav>
                <div class="mobile-menu" id="mobileMenu">
                    <ul>
                        <li><a href="#">Trang Chủ</a></li>
                        <li><a href="#">Giới Thiệu</a></li>
                        <li><a href="#">Dự Án</a></li>
                        <li><a href="#">Bài Viết</a></li>
                        <li><a href="#">Liên Hệ</a></li>
                    </ul>
                </div>
            </div>
        </header>

        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <h1>TIÊU ĐỀ TRANG CHỦ</h1>
                <p class="placeholder">Đây là khu vực hero với mô tả ngắn về trang web. Nội dung này thu hút sự chú ý của người dùng và giới thiệu tổng quan.</p>
                <a href="#" class="cta-button">NÚT KÊU GỌI HÀNH ĐỘNG</a>
            </div>
        </section>

        <!-- Main Content -->
        <div class="container">
            <div class="main-content">
                <!-- Introduction Section -->
                <section class="intro">
                    <h2>GIỚI THIỆU</h2>
                    <p class="placeholder">Phần giới thiệu về trang web, dịch vụ hoặc cá nhân. Nội dung mô tả chi tiết hơn về mục đích của trang web.</p>
                    
                    <div class="content-columns">
                        <div class="column">
                            <h3>Tính Năng 1</h3>
                            <p class="placeholder">Mô tả ngắn về tính năng hoặc nội dung đầu tiên.</p>
                        </div>
                        <div class="column">
                            <h3>Tính Năng 2</h3>
                            <p class="placeholder">Mô tả ngắn về tính năng hoặc nội dung thứ hai.</p>
                        </div>
                        <div class="column">
                            <h3>Tính Năng 3</h3>
                            <p class="placeholder">Mô tả ngắn về tính năng hoặc nội dung thứ ba.</p>
                        </div>
                    </div>
                </section>

                <!-- Sidebar (for inner pages - optional) -->
                <aside class="sidebar">
                    <h2>THANH BÊN</h2>
                    <p class="placeholder">Đây là sidebar, thường chứa điều hướng phụ, bài viết liên quan, hoặc widget.</p>
                    <ul>
                        <li>Liên kết phụ 1</li>
                        <li>Liên kết phụ 2</li>
                        <li>Liên kết phụ 3</li>
                        <li>Liên kết phụ 4</li>
                    </ul>
                </aside>
            </div>
            
            <div class="divider"></div>
            
            <!-- Additional section to show different layout -->
            <section class="intro">
                <h2>TRANG CON MẪU (Desktop View)</h2>
                <p class="placeholder">Đây là wireframe cho một trang con. Lưu ý cách sidebar được đặt cạnh nội dung chính trên desktop.</p>
                
                <div class="content-columns">
                    <div class="column" style="flex: 2;">
                        <h3>Nội Dung Chính</h3>
                        <p class="placeholder">Khu vực nội dung chính rộng rãi cho trang con. Ở chế độ desktop, sidebar nằm bên cạnh.</p>
                    </div>
                    <div class="column" style="flex: 1;">
                        <h3>Sidebar</h3>
                        <p class="placeholder">Trên desktop, sidebar nằm cạnh nội dung chính.</p>
                    </div>
                </div>
            </section>
        </div>

        <!-- Footer -->
        <footer>
            <div class="container">
                <div class="footer-content">
                    <div class="footer-section">
                        <h3>THÔNG TIN LIÊN HỆ</h3>
                        <p class="placeholder">Địa chỉ: 123 Đường ABC, Quận XYZ</p>
                        <p class="placeholder">Email: contact@example.com</p>
                        <p class="placeholder">Điện thoại: (012) 345-6789</p>
                    </div>
                    <div class="footer-section">
                        <h3>LIÊN KẾT NHANH</h3>
                        <p class="placeholder">Trang Chủ</p>
                        <p class="placeholder">Giới Thiệu</p>
                        <p class="placeholder">Dịch Vụ</p>
                        <p class="placeholder">Liên Hệ</p>
                    </div>
                    <div class="footer-section">
                        <h3>MẠNG XÃ HỘI</h3>
                        <div class="social-links">
                            <a href="#" class="social-link">FB</a>
                            <a href="#" class="social-link">TW</a>
                            <a href="#" class="social-link">IG</a>
                            <a href="#" class="social-link">IN</a>
                        </div>
                    </div>
                </div>
            </div>
        </footer>
    </div>
    
    <!-- Mobile View (Chỉ để minh họa) -->
    <div id="mobile-view" class="mobile-view">
        <div style="padding: 15px;">
            <!-- Mobile Header -->
            <div style="display: flex; justify-content: space-between; align-items: center; padding: 10px 0; border-bottom: 2px solid #333;">
                <div style="font-size: 20px; font-weight: bold; padding: 5px; border: 2px solid #333;">LOGO</div>
                <div onclick="toggleMobileMenuDemo()" style="display: flex; flex-direction: column; cursor: pointer; width: 30px; height: 20px; justify-content: space-between;">
                    <div style="width: 100%; height: 3px; background-color: #333;"></div>
                    <div style="width: 100%; height: 3px; background-color: #333;"></div>
                    <div style="width: 100%; height: 3px; background-color: #333;"></div>
                </div>
            </div>
            
            <!-- Mobile Menu (hidden by default) -->
            <div id="mobileMenuDemo" style="display: none; background-color: #fff; margin-top: 10px; border: 1px solid #ddd;">
                <div style="padding: 15px; border-bottom: 1px solid #eee;">Trang Chủ</div>
                <div style="padding: 15px; border-bottom: 1px solid #eee;">Giới Thiệu</div>
                <div style="padding: 15px; border-bottom: 1px solid #eee;">Dự Án</div>
                <div style="padding: 15px; border-bottom: 1px solid #eee;">Bài Viết</div>
                <div style="padding: 15px;">Liên Hệ</div>
            </div>
            
            <!-- Mobile Hero -->
            <div style="text-align: center; padding: 30px 0; border-bottom: 1px solid #ddd;">
                <div style="font-size: 1.5rem; font-weight: bold; margin-bottom: 15px; padding: 10px; border: 2px solid #333;">TIÊU ĐỀ TRANG CHỦ</div>
                <div style="background-color: #eee; padding: 15px; margin-bottom: 20px; border: 1px dashed #aaa;">
                    Khu vực hero cho mobile. Nội dung được xếp chồng lên nhau.
                </div>
                <div style="padding: 15px 30px; border: 2px solid #333; display: inline-block; font-weight: bold; margin-top: 10px;">
                    NÚT LỚN CHO MOBILE
                </div>
            </div>
            
            <!-- Mobile Content -->
            <div style="padding: 20px 0;">
                <div style="font-size: 1.3rem; font-weight: bold; margin-bottom: 15px; padding-bottom: 10px; border-bottom: 1px solid #ddd;">
                    NỘI DUNG CHÍNH
                </div>
                
                <div style="background-color: #f9f9f9; padding: 15px; margin-bottom: 15px; border: 1px solid #ddd;">
                    <div style="font-weight: bold; margin-bottom: 10px;">Phần 1</div>
                    <div style="background-color: #eee; padding: 10px; border: 1px dashed #aaa;">Nội dung xếp chồng trên mobile</div>
                </div>
                
                <div style="background-color: #f9f9f9; padding: 15px; margin-bottom: 15px; border: 1px solid #ddd;">
                    <div style="font-weight: bold; margin-bottom: 10px;">Phần 2</div>
                    <div style="background-color: #eee; padding: 10px; border: 1px dashed #aaa;">Tất cả nội dung đều xếp dọc</div>
                </div>
                
                <div style="background-color: #f9f9f9; padding: 15px; margin-bottom: 15px; border: 1px solid #ddd;">
                    <div style="font-weight: bold; margin-bottom: 10px;">Phần 3</div>
                    <div style="background-color: #eee; padding: 10px; border: 1px dashed #aaa;">Không có cột cạnh nhau</div>
                </div>
                
                <div style="margin-top: 30px; padding: 15px; background-color: #fff; border: 1px solid #ddd;">
                    <div style="font-weight: bold; margin-bottom: 10px;">TRANG CON (Mobile View)</div>
                    <div style="background-color: #eee; padding: 10px; border: 1px dashed #aaa; margin-bottom: 15px;">
                        Trên mobile, sidebar thường chuyển xuống dưới cùng hoặc vào menu ẩn.
                    </div>
                </div>
            </div>
            
            <!-- Mobile Footer -->
            <div style="background-color: #fff; border-top: 2px solid #ddd; padding: 20px; margin-top: 20px;">
                <div style="text-align: center; font-weight: bold; margin-bottom: 15px;">FOOTER MOBILE</div>
                <div style="background-color: #eee; padding: 15px; border: 1px dashed #aaa; text-align: center;">
                    Thông tin liên hệ và liên kết xã hội
                </div>
            </div>
        </div>
    </div>

    <script>
        // JavaScript để chuyển đổi giữa desktop và mobile view (chỉ để demo)
        function showView(view) {
            const desktopView = document.getElementById('desktop-view');
            const mobileView = document.getElementById('mobile-view');
            const desktopBtn = document.querySelectorAll('.toggle-button')[0];
            const mobileBtn = document.querySelectorAll('.toggle-button')[1];
            
            if (view === 'desktop') {
                desktopView.style.display = 'block';
                mobileView.style.display = 'none';
                desktopBtn.classList.add('active');
                mobileBtn.classList.remove('active');
            } else {
                desktopView.style.display = 'none';
                mobileView.style.display = 'block';
                desktopBtn.classList.remove('active');
                mobileBtn.classList.add('active');
            }
        }
        
        // JavaScript cho menu mobile (trong desktop view)
        function toggleMobileMenu() {
            const mobileMenu = document.getElementById('mobileMenu');
            mobileMenu.classList.toggle('active');
        }
        
        // JavaScript cho menu mobile (trong mobile view demo)
        function toggleMobileMenuDemo() {
            const mobileMenuDemo = document.getElementById('mobileMenuDemo');
            if (mobileMenuDemo.style.display === 'none' || mobileMenuDemo.style.display === '') {
                mobileMenuDemo.style.display = 'block';
            } else {
                mobileMenuDemo.style.display = 'none';
            }
        }
        
        // Đóng menu mobile khi click bên ngoài (cho desktop view)
        document.addEventListener('click', function(event) {
            const mobileMenu = document.getElementById('mobileMenu');
            const hamburger = document.querySelector('.hamburger');
            
            if (mobileMenu && hamburger) {
                if (!mobileMenu.contains(event.target) && !hamburger.contains(event.target)) {
                    mobileMenu.classList.remove('active');
                }
            }
        });
        
        // Mặc định hiển thị desktop view
        window.onload = function() {
            showView('desktop');
        };
    </script>
</body>
</html>
