# elmiafi-books
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>متجر الكتب المـعافي</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Tahoma,sans-serif}
body{background:#f6f8fc;color:#333;scroll-behavior:smooth}
header{background:linear-gradient(90deg,#1e3c72,#2a5298);color:#fff;text-align:center;padding:50px}
header h1{font-size:44px;letter-spacing:2px}
header p{margin-top:10px;font-size:18px;color:#e0e0e0}
nav{margin-top:15px}
nav a{color:#ffd700;text-decoration:none;margin:0 15px;font-weight:bold;font-size:16px}
nav a:hover{text-decoration:underline}

/* ===== SLIDER ===== */
.slider{display:flex;overflow-x:auto;scroll-behavior:smooth;padding:20px 0;gap:20px}
.slider::-webkit-scrollbar{display:none}
.slide{min-width:200px;background:#fff;border-radius:12px;box-shadow:0 8px 20px rgba(0,0,0,.15);text-align:center;transition:transform 0.3s}
.slide img{width:100%;height:280px;object-fit:cover;border-radius:12px}
.slide h3{color:#1e3c72;margin:10px 0;font-size:16px}
.slide p{font-size:14px;color:#555;margin:5px 0}
.slide button{margin-top:8px;padding:8px 15px;background:#2a5298;color:white;border:none;border-radius:20px;cursor:pointer;transition:0.3s}
.slide button:hover{background:#1e3c72;transform:scale(1.05)}

/* ===== BOOKS GRID ===== */
.products{display:flex;flex-wrap:wrap;gap:25px;justify-content:center;padding:50px}
.card{background:#fff;width:220px;padding:15px;border-radius:12px;text-align:center;box-shadow:0 12px 25px rgba(0,0,0,.15);transition:transform 0.4s,box-shadow 0.4s}
.card:hover{transform:translateY(-10px);box-shadow:0 20px 35px rgba(0,0,0,.25)}
.card img{width:100%;height:280px;object-fit:cover;border-radius:10px}
.card h3{color:#1e3c72;margin:15px 0 8px;font-size:16px}
.card p{font-size:14px;color:#555;margin-bottom:5px}
.card button{margin-top:8px;padding:8px 18px;background:#2a5298;color:white;border:none;border-radius:20px;cursor:pointer;font-size:14px;transition:background 0.3s,transform 0.3s}
.card button:hover{background:#1e3c72;transform:scale(1.05)}

/* ===== ABOUT ===== */
section.about{padding:60px 15%;line-height:1.8}
h2{color:#1e3c72;margin-bottom:15px}

/* ===== CART ===== */
#cart{position:fixed;top:80px;right:20px;width:300px;background:#fff;border-radius:12px;box-shadow:0 12px 25px rgba(0,0,0,.25);padding:15px;z-index:100}
#cart h3{margin-bottom:10px;color:#1e3c72}
#cart ul{list-style:none;max-height:400px;overflow-y:auto;margin-bottom:10px}
#cart ul li{margin-bottom:8px;display:flex;justify-content:space-between}
#cart button.remove{background:#dc3545;margin:0;padding:2px 8px;border-radius:5px;font-size:12px}
#cart p.total{font-weight:bold}

/* ===== FOOTER ===== */
footer{text-align:center;padding:25px;background:#eaeef6}
footer a{color:#2a5298;text-decoration:none;font-weight:bold}
footer a:hover{text-decoration:underline}
</style>
</head>
<body>

<header>
<h1>متجر الكتب المـعافي</h1>
<p>المعرفة • الثقافة • الإلهام</p>
<nav>
<a href="#slider">الرئيسية</a>
<a href="#books">الكتب</a>
<a href="#about">من نحن</a>
</nav>
</header>

<!-- ===== SLIDER ===== -->
<section id="slider" class="slider">
<!-- Slider 5 كتب مميزة -->
<div class="slide"><img src="https://images-na.ssl-images-amazon.com/images/I/81eB+7+CkUL.jpg" alt="العادات الذرية"><h3>العادات الذرية</h3><p>تحسين العادات وبناء حياة أفضل.</p><button onclick="window.open('https://www.paypal.me/username/120','_blank')">اشترِ عبر PayPal</button></div>
<div class="slide"><img src="https://images-na.ssl-images-amazon.com/images/I/71aFt4+OTOL.jpg" alt="الأب الغني والأب الفقير"><h3>الأب الغني والأب الفقير</h3><p>تعلم إدارة المال وتطوير العقلية المالية.</p><button onclick="window.open('https://www.paypal.me/username/100','_blank')">اشترِ عبر PayPal</button></div>
<div class="slide"><img src="https://images-na.ssl-images-amazon.com/images/I/81bsw6fnUiL.jpg" alt="الخيميائي"><h3>الخيميائي</h3><p>رواية عن الأحلام والسعي لتحقيق الحياة.</p><button onclick="window.open('https://www.paypal.me/username/90','_blank')">اشترِ عبر PayPal</button></div>
<div class="slide"><img src="https://images-na.ssl-images-amazon.com/images/I/91r+2PbCKwL.jpg" alt="قوة الآن"><h3>قوة الآن</h3><p>العيش في اللحظة الحالية والتخلص من القلق.</p><button onclick="window.open('https://www.paypal.me/username/110','_blank')">اشترِ عبر PayPal</button></div>
<div class="slide"><img src="https://images-na.ssl-images-amazon.com/images/I/81a4kCNuH+L.jpg" alt="فن اللامبالاة"><h3>فن اللامبالاة</h3><p>عيش حياة أكثر راحة وواقعية.</p><button onclick="window.open('https://www.paypal.me/username/95','_blank')">اشترِ عبر PayPal</button></div>
</section>

<!-- ===== ALL BOOKS ===== -->
<section id="books" class="products">
<script>
const books=[];
for(let i=1;i<=50;i++){
  books.push({
    title:"كتاب عربي "+i,
    desc:"وصف الكتاب "+i+" لتوضيح محتواه وفائدته.",
    price:Math.floor(Math.random()*100)+50,
    img:"https://picsum.photos/200/280?random="+i,
    link:"https://www.paypal.me/username/"+(50+i)
  });
}
const booksSection=document.getElementById("books");
books.forEach(book=>{
  const div=document.createElement("div");
  div.classList.add("card");
  div.innerHTML=`<img src="${book.img}" alt="${book.title}"><h3>${book.title}</h3><p>${book.desc}</p><p><strong>السعر:</strong> ${book.price} درهم</p><button onclick="window.open('${book.link}','_blank')">اشترِ عبر PayPal</button>`;
  booksSection.appendChild(div);
});
</script>
</section>

<!-- ===== ABOUT ===== -->
<section id="about" class="about">
<h2>من نحن</h2>
<p>متجر الكتب المـعافي يهدف إلى نشر الثقافة والمعرفة وإتاحة أفضل الكتب لجميع القراء العرب. نحرص على تقديم محتوى متنوع وعالي الجودة بأسعار مناسبة.</p>
<h2>لماذا تختارنا</h2>
<ul>
<li>اختيار دقيق للكتب</li>
<li>جودة مضمونة</li>
<li>شغف للثقافة</li>
<li>خدمة احترافية</li>
</ul>
</section>

<!-- ===== CART ===== -->
<div id="cart">
<h3>سلة المشتريات</h3>
<ul id="cart-items"></ul>
<p class="total">المجموع: 0 درهم</p>
</div>

<script>
// Cart متفاعل
const cartItems=document.getElementById("cart-items");
const totalP=document.querySelector("#cart p.total");
let total=0;
document.addEventListener("click",function(e){
  if(e.target.tagName==="BUTTON" && e.target.innerText.includes("اشترِ")){
    const card=e.target.closest(".card") || e.target.closest(".slide");
    const title=card.querySelector("h3").innerText;
    const price=parseInt(card.querySelector("p strong").nextSibling.textContent.replace("درهم","").trim());
    const li=document.createElement("li");
    li.innerHTML=`${title} - ${price} درهم <button class="remove">حذف</button>`;
    cartItems.appendChild(li);
    total+=price;
    totalP.innerText=`المجموع: ${total} درهم`;
    li.querySelector(".remove").addEventListener("click",()=>{
      total-=price;
      li.remove();
      totalP.innerText=`المجموع: ${total} درهم`;
    });
  }
});
</script>

<footer>
<p>تواصل معنا: <a href="http://www.elmiafibooks.com">www.elmiafibooks.com</a> | <a href="http://www.elmiafibooks.ma">www.elmiafibooks.ma</a></p>
<p>© 2026 متجر الكتب المـعافي – جميع الحقوق محفوظة</p>
</footer>

</body>
</html>
