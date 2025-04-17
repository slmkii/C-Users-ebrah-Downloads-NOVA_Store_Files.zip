<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>NOVA | متجر إلكتروني</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>🛍️ NOVA | متجرك الإلكتروني في الخليج</h1>
    <p>📞 خدمة العملاء: <strong>94011884</strong></p>
  </header>

  <nav>
    <a href="#products">المنتجات</a>
    <a href="#order">طلب جديد</a>
  </nav>

  <main class="container">
    <section id="products">
      <h2>📦 المنتجات</h2>

      <!-- منتج علي إكسبرس -->
      <div class="product">
        <img src="https://ae01.alicdn.com/kf/abc123.jpg" alt="منتج" width="100%">
        <h3>ساعة ذكية</h3>
        <p>السعر الأصلي: <span class="original-price">2</span> ريال</p>
        <p>سعر NOVA: <span class="nova-price"></span> ريال</p>
        <button>اطلب الآن</button>
      </div>
    </section>

    <section id="order" class="form-section">
      <h2>📝 نموذج الطلب</h2>
      <form>
        <label>الاسم الكامل</label>
        <input type="text" required />

        <label>رقم الهاتف</label>
        <input type="tel" required />

        <label>رقم البطاقة / جواز السفر</label>
        <input type="text" required />

        <label>الدولة</label>
        <select id="country" required>
          <option value="OM">عُمان</option>
          <option value="SA">السعودية</option>
          <option value="AE">الإمارات</option>
          <option value="QA">قطر</option>
          <option value="KW">الكويت</option>
          <option value="BH">البحرين</option>
        </select>

        <label>الموقع بالتفصيل</label>
        <input type="text" placeholder="اكتب عنوانك الكامل" required />

        <button type="submit">إرسال الطلب</button>
      </form>
    </section>
  </main>

  <footer>
    <p>© 2025 NOVA. جميع الحقوق محفوظة.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
<div class="product">
    <img src="https://ae01.alicdn.com/kf/abc123.jpg" width="100%">
    <h3>ساعة ذكية</h3>
    <p>السعر الأصلي: <span class="original-price" data-price="10">10</span> ريال</p>
    <p>سعر NOVA: <span class="nova-price"></span> ريال</p>
    <a href="https://www.aliexpress.com/item/123456.html" target="_blank">
      <button>عرض المنتج واطلبه</button>
    </a>
  </div>
  رbody {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background: #f4f4f4;
  }
  header, footer {
    background: #1e1e2f;
    color: white;
    padding: 20px;
    text-align: center;
  }
  nav {
    background: #333;
    text-align: center;
    padding: 10px;
  }
  nav a {
    color: white;
    margin: 0 10px;
    text-decoration: none;
  }
  .container {
    padding: 20px;
  }
  .product {
    background: white;
    padding: 15px;
    margin-bottom: 20px;
    border-radius: 10px;
  }
  .form-section {
    background: white;
    padding: 20px;
    margin-top: 30px;
    border-radius: 10px;
  }
  // رفع السعر الأصلي (×2 + 2 ريال شحن)
document.querySelectorAll('.product').forEach(product => {
    const originalPrice = parseFloat(product.querySelector('.original-price').textContent);
    const novaPrice = (originalPrice * 2) + 2;
    product.querySelector('.nova-price').textContent = novaPrice.toFixed(2);
  });
  // زيادة السعر لكل منتج (ثابت: 2 ريال)
document.querySelectorAll('.product').forEach(product => {
    const priceSpan = product.querySelector('.original-price');
    const basePrice = parseFloat(priceSpan.dataset.price);
    const novaPrice = basePrice + 2; // زيادة ريالين
    product.querySelector('.nova-price').textContent = novaPrice.toFixed(2);
  });
