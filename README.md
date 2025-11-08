<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Thư viện ảnh đáp ứng</title>
<style>
/* Mobile-first: 1 cột */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #fff;
  color: #000;
}

header {
  text-align: center;
  padding: 20px 0;
}

.gallery {
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
  padding: 10px;
}

.item img {
  width: 100%;
  display: block;
  border-radius: 0;
}

/* Tablet: 2 cột từ 772px */
@media (min-width: 772px) {
  .gallery {
    grid-template-columns: 1fr 1fr;
  }
  .item img {
    border-radius: 50%;
  }
  .gallery .item:last-child {
    grid-column: span 2;
  }
}

/* Desktop: 3 cột từ 992px */
@media (min-width: 992px) {
  .gallery {
    grid-template-columns: repeat(3, 1fr);
  }
  .item img {
    border-radius: 0;
  }
  .gallery .item:nth-child(3n) {
    grid-column: span 2;
  }
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  body {
    background-color: #222;
    color: #f0e68c;
  }
  .item img {
    border: 2px solid black;
  }
}
</style>
</head>
<body>
<header>
  <h1>Thư viện ảnh của tôi</h1>
</header>
<main class="gallery">
  <div class="item"><img src="image1.jpg" alt="Mô tả hình 1"><p>Chú thích 1</p></div>
  <div class="item"><img src="image2.jpg" alt="Mô tả hình 2"><p>Chú thích 2</p></div>
  <div class="item"><img src="image3.jpg" alt="Mô tả hình 3"><p>Chú thích 3</p></div>
  <div class="item"><img src="image4.jpg" alt="Mô tả hình 4"><p>Chú thích 4</p></div>
  <div class="item"><img src="image5.jpg" alt="Mô tả hình 5"><p>Chú thích 5</p></div>
  <div class="item"><img src="image6.jpg" alt="Mô tả hình 6"><p>Chú thích 6</p></div>
</main>
</body>
</html>
