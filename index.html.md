<!DOCTYPE html>  
<html lang="vi">  
<head>  
    <meta charset="UTF-8">  
    <title>Báo Tường 12/6</title>  
  
    <style>  
        body {  
            font-family: Arial;  
            margin: 0;  
            background-color: #fdf6f0;  
        }  
  
        header {  
            background: linear-gradient(to right, #ff9a9e, #fad0c4);  
            color: white;  
            text-align: center;  
            padding: 20px;  
        }  
  
        nav {  
            background-color: #333;  
            padding: 10px;  
            text-align: center;  
        }  
  
        nav a {  
            color: white;  
            margin: 10px;  
            text-decoration: none;  
            font-weight: bold;  
        }  
  
        nav a:hover {  
            color: #ff9a9e;  
        }  
  
        .content {  
            padding: 20px;  
        }  
  
        .gallery {  
            display: flex;  
            gap: 10px;  
            flex-wrap: wrap;  
        }  
  
        .gallery img {  
            width: 45%;  
            border-radius: 10px;  
        }  
  
        /* FORM BÌNH LUẬN */  
        .comment-box {  
            margin-top: 30px;  
            padding: 15px;  
            background: #fff;  
            border-radius: 10px;  
        }  
  
        input, textarea {  
            width: 100%;  
            padding: 10px;  
            margin-top: 10px;  
            border-radius: 8px;  
            border: 1px solid #ccc;  
        }  
  
        button {  
            margin-top: 10px;  
            padding: 10px 15px;  
            background: #ff9a9e;  
            border: none;  
            color: white;  
            border-radius: 8px;  
            cursor: pointer;  
        }  
  
        button:hover {  
            background: #ff6f91;  
        }  
  
        .comments {  
            margin-top: 20px;  
        }  
  
        .comment {  
            background: #ffe0e6;  
            padding: 10px;  
            border-radius: 10px;  
            margin-top: 10px;  
        }  
  
        footer {  
            background-color: #333;  
            color: white;  
            text-align: center;  
            padding: 10px;  
        }  
    </style>  
</head>  
  
<body>  
  
<header>  
    <h1>🚆 Chuyến Tàu Thanh Xuân - Lớp 12/6</h1>  
    <p>Nơi lưu giữ những kỷ niệm đẹp nhất ❤️</p>  
</header>  
  
<nav>  
    <a href="#">Trang chủ</a>  
    <a href="#">Giới thiệu</a>  
    <a href="#">Hình ảnh</a>  
    <a href="#">Cảm nghĩ</a>  
</nav>  
  
<section class="content">  
  
    <h2>📖 Giới thiệu</h2>  
    <p>  
        Thanh xuân giống như một chuyến tàu. Lớp 12/6 chính là nơi   
        ghi lại những ký ức đẹp nhất: những giờ học vui vẻ, những lần   
        quậy phá và cả những khoảnh khắc chia xa.  
    </p>  
  
    <h2>📸 Khoảnh khắc đáng nhớ</h2>  
    <div class="gallery">  
        <img src="IMG_3999.jpg">  
        <img src="IMG_4001.jpg">  
        <img src="IMG_4002.jpg">  
        <img src="IMG_4005.jpg">  
        <img src="IMG_4004.jpg">  
        <img src="IMG_4003.jpg">  
  
    </div>  
  
    <h2>💌 Góc cảm nghĩ</h2>  
    <p>  
        Ba năm cấp 3 trôi qua nhanh như một cái chớp mắt.   
        Chuyến tàu thanh xuân rồi sẽ dừng lại, nhưng tình bạn   
        và kỷ niệm sẽ còn mãi trong tim mỗi người.  
    </p>  
  
    <!-- FORM BÌNH LUẬN -->  
    <div class="comment-box">  
        <h2>📝 Bình luận</h2>  
  
        <input type="text" id="name" placeholder="Tên của bạn">  
        <textarea id="message" placeholder="Viết cảm nghĩ..."></textarea>  
        <button onclick="addComment()">Gửi</button>  
  
        <div class="comments" id="commentList"></div>  
    </div>  
  
</section>  
  
<footer>  
    <p>Thiết kế bởi tập thể lớp 12/6 💙</p>  
</footer>  
  
<script>  
function addComment() {  
    let name = document.getElementById("name").value;  
    let message = document.getElementById("message").value;  
  
    if(name === "" || message === "") {  
        alert("Vui lòng nhập đầy đủ!");  
        return;  
    }  
  
    let commentBox = document.getElementById("commentList");  
  
    let newComment = document.createElement("div");  
    newComment.classList.add("comment");  
  
    newComment.innerHTML = "<b>" + name + ":</b> " + message;  
  
    commentBox.appendChild(newComment);  
  
    document.getElementById("name").value = "";  
    document.getElementById("message").value = "";  
}  
</script>  
  
</body>  
</html>  
