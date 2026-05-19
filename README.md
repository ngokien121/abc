<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>TỔNG HỢP KIẾN THỨC</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Segoe UI;
}

body{
    overflow-x:hidden;
    color:white;
    background:black;
}

/* BACKGROUND */

body::before{

    content:"";

    position:fixed;
    inset:0;

    background:
    linear-gradient(
    rgba(0,0,0,0.65),
    rgba(0,0,0,0.75)
    ),

    url("https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=2070&auto=format&fit=crop");

    background-size:cover;
    background-position:center;

    z-index:-2;
}

/* PARTICLES */

.particle{

    position:fixed;

    width:4px;
    height:4px;

    background:white;

    border-radius:50%;

    opacity:0.7;

    animation:float linear infinite;
}

@keyframes float{

    from{
        transform:translateY(100vh);
    }

    to{
        transform:translateY(-100vh);
    }

}

/* HEADER */

header{

    text-align:center;

    padding:100px 20px;
}

header h1{

    font-size:75px;

    font-weight:900;

    text-shadow:
    0 0 20px cyan,
    0 0 40px cyan;
}

header p{

    margin-top:25px;

    font-size:28px;

    color:#cbd5e1;
}

/* MENU */

.menu{

    display:flex;

    justify-content:center;

    flex-wrap:wrap;

    gap:20px;

    padding:20px;
}

.menu button{

    padding:18px 35px;

    border:none;

    border-radius:18px;

    font-size:18px;

    color:white;

    cursor:pointer;

    background:
    rgba(255,255,255,0.08);

    backdrop-filter:blur(12px);

    transition:0.3s;
}

.menu button:hover{

    transform:scale(1.08);

    background:cyan;

    color:black;

    box-shadow:0 0 25px cyan;
}

/* CONTENT */

.content{

    display:none;

    width:90%;
    max-width:1300px;

    margin:auto;
    margin-top:50px;
    margin-bottom:80px;

    padding:40px;

    border-radius:30px;

    background:
    rgba(0,0,0,0.45);

    border:
    1px solid rgba(255,255,255,0.15);

    backdrop-filter:blur(15px);

    animation:fade 0.5s;
}

@keyframes fade{

    from{
        opacity:0;
        transform:translateY(30px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }

}

.content h2{

    font-size:50px;

    color:cyan;

    margin-bottom:30px;
}

.content h3{

    margin-top:35px;
    margin-bottom:20px;

    color:#38bdf8;

    font-size:30px;
}

.code{

    background:#020617;

    padding:25px;

    border-radius:20px;

    border-left:5px solid cyan;

    line-height:2.2;

    font-size:20px;
}

/* FOOTER */

footer{

    text-align:center;

    padding:40px;

    color:#cbd5e1;

    font-size:18px;
}

/* SCROLL */

::-webkit-scrollbar{
    width:10px;
}

::-webkit-scrollbar-thumb{

    background:cyan;

    border-radius:20px;
}

/* MOBILE */

@media(max-width:768px){

    header h1{
        font-size:42px;
    }

    header p{
        font-size:18px;
    }

    .menu button{
        width:90%;
    }

    .content{
        width:95%;
        padding:20px;
    }

    .content h2{
        font-size:35px;
    }

    .code{
        font-size:16px;
    }

}

</style>
</head>

<body>

<header>

    <h1>TỔNG HỢP KIẾN THỨC</h1>

    <p>
        AutoCAD • Excel • Điện Tự Động Hóa • Quy Trình Làm Việc
    </p>

</header>

<!-- MENU -->

<div class="menu">

    <button onclick="showContent('cad')">
        LỆNH AUTOCAD
    </button>

    <button onclick="showContent('excel')">
        EXCEL
    </button>

    <button onclick="showContent('work')">
        QUY TRÌNH
    </button>

    <button onclick="showContent('auto')">
        ĐIỆN TỰ ĐỘNG HÓA
    </button>

</div>

<!-- AUTOCAD -->

<div class="content" id="cad">

<h2>TỔNG HỢP LỆNH AUTOCAD</h2>

<h3>NHÓM LỆNH VẼ</h3>

<div class="code">

L : Line → Vẽ đoạn thẳng <br><br>

PL : Pline → Vẽ đa tuyến <br><br>

C : Circle → Vẽ hình tròn <br><br>

REC : Rectangle → Hình chữ nhật <br><br>

POL : Polygon → Đa giác <br><br>

A : Arc → Cung tròn <br><br>

EL : Ellipse → Hình ellipse <br><br>

SPL : Spline → Đường cong <br><br>

DO : Donut → Vòng tròn đặc

    </div>

    <h3>II. NHÓM LỆNH CHỈNH SỬA (CHI TIẾT)</h3>

    <div class="code">

E : Erase → Xóa <br><br>

M : Move → Di chuyển <br><br>

CO : Copy → Sao chép <br><br>

RO : Rotate → Xoay <br><br>

SC : Scale → Thu phóng <br><br>

MI : Mirror → Đối xứng <br><br>

O : Offset → Tạo song song <br><br>

TR : Trim → Cắt <br><br>

EX : Extend → Nối dài <br><br>

F : Fillet → Bo góc

    </div>

    <h3>III. NHÓM LỆNH DIM (KÍCH THƯỚC)</h3>

    <div class="code">

DIM : Ghi kích thước <br><br>

DLI : Dim Linear <br><br>

DAL : Dim Align <br><br>

DAN : Dim Angular <br><br>

DDI : Đường kính <br><br>

DRA : Bán kính <br><br>

MT : Mtext <br><br>

T : Text

    </div>

    <h3>IV. NHÓM LAYER</h3>

    <div class="code">

LA : Quản lý layer <br><br>

LAYISO : Cô lập layer <br><br>

LAYOFF : Tắt layer <br><br>

LAYON : Bật layer <br><br>

LAYFRZ : Đóng băng layer

    </div>

    <h3>V. NHÓM 3D</h3>

    <div class="code">

BOX : Tạo khối hộp <br><br>

SPHERE : Hình cầu <br><br>

CYLINDER : Hình trụ <br><br>

EXTRUDE : Đùn khối <br><br>

REVOLVE : Xoay tạo khối <br><br>

UNION : Gộp khối <br><br>

SUBTRACT : Trừ khối

</div>

</div>

<!-- EXCEL -->

<div class="content" id="excel">

<h2>VŨ ĐỨC NGUYÊN CÓ YÊU TRÂM KHÔNG</h2>

<div class="choice-box">
    
    <label for="love">Chọn một đáp án 💖</label>

    <select id="love">
        <option>-- CHỌN Ở ĐÂY --</option>
        <option>YÊU TRÂM</option>
        <option>Rất yêu Trâm </option>
        <option>KHÔNG YÊU </option>
    <select id="love" onchange="changeScene()">

</div>



</div>

</div>

<!-- WORK -->

<div class="content" id="work">

<h2>QUY TRÌNH LÀM VIỆC</h2>

<div class="code">

1. Màn hình chính>phụ kiện>motor valve>van( cấp nước, nóng mát, tuần hoàn) <br><br>

2. Tắt cấp nước (rinse), tuần hoàn, gia nhiệt(pump) <br><br>

3. Chuyển tất cả trạng thái về off <br><br>

4. *(các bể hoá chất bơm tuần hoàn ở chế độ auto chuyển về manual và khi chuyển về manual thì chuyển trạng thái về open để mở van xả đáy) <br><br>

5. Xả hoá chất  <br><br>

6. Tiến hành di chuyển lên line và mở những ống có chữ ACHW có label màu xanh chữ vàng có hình mũi tên và mở van thủ công  <br><br>

7. quay trở lại màn hình chính <br>
Phụ kiện>motor valve>van(drain) Open full valve và để ở chế độ manual  (nếu ở chế độ auto reset máy và chỉnh về manual) <br><br>

8. **LƯU Ý MỞ VAN CÓ CHỮ ACHW** <br><br>

9. Đóng tất cả các van ACHW và đóng van điện vừa mở <br><br>
Mở van tay đường CPW Để rửa tự động <br><br>

10. Chạy Chương Trình
Màn hình chính>hoá chất/bể lưu chữ>tự động làm sạch>cleaner cleaning <br><br>

11. Kiểm tra các bước và số lần lặp lại<br>

-Auto cleaning on để vận hành<br>
-Kiểm tra tránh bị đầy tràn<br>
-chonh mục cleaning tự động bước tiếp theo để chương trình tự động chuyển bước tiếp theo<br>

+ Thay fillter<br><br>
-Mở van xả đáy của housing filter<br>
-Mở lắp gousing filter<br>
-Thay thế filter<br>
-Lấy filter đã sữ dụng<br><br>
*xịt rửa housing bằng vòi tăng áp trước khi cho filter mới*<br><br>
-kiểm tra các cọc cố định filter<br>
-Thay thế filter mới <br>
-đóng nắp giữ cố định filter<br>
*dùng máy khoan ở chế độ khoan với lực siết là 10*<br>
Đóng van xả đáy<br><br>
Thay fillter line pd strip<br>
Fillter nước 500 1um chịu nhiệt<br>
Fillter hoá chất axit naoh, acitdip, bd strip 500 1um chịu nhiệt<br>
Duy nhất Predip 750 1um chịu nhiệt<br><br>
4 bể hoá chất<br>
-acitdip<br>
-predip<br>
-pd strip<br>
-naoh<br><br>

  QUY TRÌNH PM LINE<br><br>
Cleanner<br>
Màn hình chính>phụ kiện>motor valve>van( cấp nước, nóng mát, tuần hoàn)<br>
Tắt cấp nước (rinse)<br>
Tắt bơm tuần hoàn, gia nhiệt(pump)<br>
Chuyển tất cả trạng thái về off<br>
Thời gian tối thiểu 1p<br>
*(các bể hoá chất bơm tuần hoàn ở chế độ auto chuyển về manual và khi chuyển về manual thì chuyển trạng thái về open để mở van xả đáy)<br>

Xả hoá chất 
-Tiến hành di chuyển lên line và mở những ống có chữ ACHW có label màu xanh chữ vàng có hình mũi tên và mở van thủ công <br>
-quay trở lại màn hình chính <br>
Phụ kiện>motor valve>van(drain) Open full valve và để ở chế độ manual  (nếu ở chế độ auto reset máy và chỉnh về manual)<br>
-LƯU Ý MỞ VAN CÓ CHỮ ACHW<br>
 Timer 30s

Đóng tất cả các van ACHW và đóng van điện vừa mở<br>
Mở van tay đường CPW Để rửa tự động<br>

Chạy Chương Trình<br>
Màn hình chính>hoá chất/bể lưu chữ>tự động làm sạch>cleaner cleaning<br>

Kiểm tra các bước và số lần lặp lại<br>

-Auto cleaning on để vận hành<br>
-Kiểm tra tránh bị đầy tràn<br>
-chonh mục cleaning tự động bước tiếp theo để chương trình tự động chuyển bước tiếp theo<br><br>




Vệ sinh bể<br>
-Sử dụng máy rửa cao áo vệ sinh dị vật và bẩn ở đáy bể<br>
-soi và kiểm tra nozzle<br>
Điều chỉnh góc gương với khoản 45 độ để có góc ngoại quan tốt nhất, loại bỏ nếu phát sinh<br>
-kiểm tra nozzle<br>
Tháo thanh nozzle ra bên ngoài, xoáy ngược chiều kim đồng hồ để tháo<br>
- dùng nhíp để loại bỏ dị vật phát sinh<br>
- Sau khi Thay Xong Fillter kiểm tra lại CÁC VAN XẢ ĐÁY HOUSING VÀ XẢ BỂ để chuẩn bị make up mới hoá chất<br>
MAKE UP MỚI HOÁ CHẤT<br>
-di chuyển về màn hình>hoá chất/bể lưu trữ<br>
+Bật Lại hết tất cả thành ON(rinse)<br>
+Bật Bơm tuần hoàn Thành ON/OPEN(Pump)<br>
Bật Gia Nhiệt OFF->ON<br>
<br>
Vệ Sinh Acid Dip<br>
<br>
Off bơm và gia nhiệt<br>
Tắt cấp nước(rinse)<br>
Tắt tuần hoàn(pump)<br>
Tắt gia nhiệt ON->OFF<br>
THỰC HIỆN XẢ HOÁ CHẤT<br>
di chuyển lên line tiến hành xả van thủ công(van tay)<br>
KÍ HIỆU ACHW<br>
du chuyển ra màn hình mở ban xả đáy<br>
BẬT CHƯƠNG TRÌNH VỆ SINH TỰ ĐỘNG<br>
Màn hình chính>hoá chất/bể lưu chữ/tự động làm sạch/cleaner cleaning<br>
Kieemr tra các bước vệ sinh tự động và số lần lặp lại<br>
STEP BẰNG 0 thì lặp lại 1 lần( n+1)<br>
Chọn AUTO CLEANING ON để vận hành<br>
Chọn mục cleaning tự động bước tiếp theo để chương trình tự động chuyển tiếp các bước<br>
<br><BR>

Vệ sinh bể<br>
-Sử dụng máy rửa cao áo vệ sinh dị vật và bẩn ở đáy bể<br>
-soi và kiểm tra nozzle<br>
Điều chỉnh góc gương với khoản 45 độ để có góc ngoại quan tốt nhất, loại bỏ nếu phát sinh<br>
-kiểm tra nozzle<br>
Tháo thanh nozzle ra bên ngoài, xoáy ngược chiều kim đồng hồ để tháo<br>
- dùng nhíp để loại bỏ dị vật phát sinh<br> <BR>
+ Thay fillter<br>
-Mở van xả đáy của housing filter<br>
-Mở lắp gousing filter<br>
-Thay thế filter<br>
-Lấy filter đã sữ dụng<br>
*xịt rửa housing bằng vòi tăng áp trước khi cho filter mới*<br>
-kiểm tra các cọc cố định filter<br>
-Thay thế filter mới <br>
-đóng nắp giữ cố định filter<br>
*dùng máy khoan ở chế độ khoan với lực siết là 10*<br>
Đóng van xả đáy<br>
<br>
- Sau khi Thay Xong Fillter kiểm tra lại CÁC VAN XẢ ĐÁY HOUSING VÀ XẢ BỂ để chuẩn bị make up mới hoá chất<br>
MAKE UP MỚI HOÁ CHẤT<br>
-di chuyển về màn hình>hoá chất/bể lưu trữ<br>
+Bật Lại hết tất cả thành ON(rinse)<br>
+Bật Bơm tuần hoàn Thành ON/OPEN(Pump)<br>
Bật Gia Nhiệt OFF->ON<br>
<br>
<br>
chi tiết các line cần fillter<br><br>
mạ ngang: <br>
-line mài:<br>
fillter không chịu nhiệt 10um 12 cái 250, 8 cái 500<br>
-line destmear<br>
fillter chịu nhiệt 5um 50 cái <br>
line mạ<br>
fillter chịu nhiệt 195 cái 5um 250, 64 con 1um 250<br>
<br>
line fill<br>
fillter chịu nhiệt 1um: <br>
18 con 750<br>
13 con 250<br>
94 con 500<br>

</div>

</div>

<!-- AUTO -->

<div class="content" id="auto">



</div>

</div>

<footer>

DESIGN BY TRUNG KIÊN ⚡

</footer>

<script>

/* SHOW CONTENT */

function showContent(id){

    let contents =
    document.querySelectorAll(".content");

    contents.forEach(box=>{

        box.style.display="none";

    });

    document.getElementById(id)
    .style.display="block";
}

/* PARTICLES */

for(let i=0;i<100;i++){

    let p =
    document.createElement("div");

    p.classList.add("particle");

    p.style.left =
    Math.random()*100 + "vw";

    p.style.animationDuration =
    (5 + Math.random()*10) + "s";

    p.style.opacity =
    Math.random();

    document.body.appendChild(p);
}

</script>

</body>
</html>
<script>

function changeScene(){

    let value = document.getElementById("love").value;

    if(value === "KHÔNG YÊU VÀ ĐÒI LẠI BÁNH MỲ"){

        document.body.innerHTML = `

        <video autoplay loop controls
        style="
        position:fixed;
        width:100%;
        height:100%;
        object-fit:cover;
        top:0;
        left:0;
        ">

            <source src="video.mp4" type="video/mp4">

        </video>

        <div style="
        position:absolute;
        top:50%;
        left:50%;
        transform:translate(-50%,-50%);
        color:white;
        font-size:55px;
        font-weight:bold;
        text-shadow:0 0 20px black;
        ">

        😭 BỊ ĐÒI LẠI BÁNH MỲ 😭

        </div>

        `;

    }

}

</script># abc
