<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<title>ที่เที่ยวอำเภอเดชอุดม</title>

<style>
body{
    margin:0;
    font-family:sans-serif;
    background:#eef2e6;
    text-align:center;
}

header{
    background:#2e7d32;
    color:white;
    padding:15px;
    font-size:22px;
    font-weight:bold;
}

.container{
    padding:20px;
}

img{
    width:90%;
    max-width:750px;
    height:420px;
    object-fit:cover;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.2);
}

h2{
    margin:15px 0 5px;
}

p{
    color:#444;
    font-size:16px;
}

.btn{
    margin-top:15px;
}

button{
    padding:10px 18px;
    margin:5px;
    border:none;
    border-radius:8px;
    cursor:pointer;
    background:#333;
    color:white;
    font-size:14px;
}

button:hover{
    background:#555;
}
</style>
</head>

<body>

<header>🌿 ที่เที่ยวอำเภอเดชอุดม จังหวัดอุบลราชธานี</header>

<div class="container">

    <h2 id="title">วัดสำราญนิเวศ</h2>

    <img id="img" src="https://source.unsplash.com/800x500/?temple,thailand">

    <p id="desc">วัดสำคัญในพื้นที่เดชอุดม บรรยากาศสงบ เหมาะแก่การทำบุญ</p>

    <div class="btn">
        <button onclick="prev()">⬅️ ก่อนหน้า</button>
        <button onclick="next()">➡️ ถัดไป</button>
    </div>

</div>

<script>
let page = 1;

const data = [
    {
        title:"วัดสำราญนิเวศ",
        img:"temple thailand rural",
        desc:"วัดในอำเภอเดชอุดม เป็นศูนย์รวมจิตใจของชาวบ้าน"
    },
    {
        title:"วัดบ้านนา",
        img:"temple village thailand",
        desc:"วัดท้องถิ่น บรรยากาศเรียบง่ายแบบอีสาน"
    },
    {
        title:"วัดป่าธรรมชาติ",
        img:"forest temple thailand",
        desc:"วัดป่าร่มรื่น เหมาะสำหรับนั่งสมาธิและพักใจ"
    },
    {
        title:"ตลาดสดเดชอุดม",
        img:"thai market street",
        desc:"ศูนย์รวมอาหารพื้นบ้าน ของกินอร่อยราคาถูก"
    },
    {
        title:"ถนนคนเดินชุมชน",
        img:"night market thailand",
        desc:"ตลาดเย็น วิถีชุมชนและของกินหลากหลาย"
    },
    {
        title:"ทุ่งนาเดชอุดม",
        img:"rice field thailand sunset",
        desc:"วิวทุ่งนาเขียวขจี สวยช่วงหน้าฝน"
    },
    {
        title:"ลำห้วยธรรมชาติ",
        img:"river nature thailand",
        desc:"แหล่งน้ำธรรมชาติของชุมชน บรรยากาศเย็นสบาย"
    },
    {
        title:"สะพานไม้ชุมชน",
        img:"wood bridge rural thailand",
        desc:"จุดถ่ายรูปยอดนิยมของคนในพื้นที่"
    },
    {
        title:"สวนสาธารณะเดชอุดม",
        img:"park thailand green",
        desc:"สถานที่พักผ่อนและออกกำลังกาย"
    },
    {
        title:"จุดชมพระอาทิตย์ตก",
        img:"sunset thailand field",
        desc:"วิวพระอาทิตย์ตกสวยงาม เหมาะถ่ายรูปมาก"
    }
];

function show(){
    document.getElementById("title").innerText = data[page-1].title;
    document.getElementById("desc").innerText = data[page-1].desc;
    document.getElementById("img").src =
        "https://source.unsplash.com/800x500/?" + data[page-1].img;
}

function next(){
    if(page < 10){
        page++;
        show();
    }
}

function prev(){
    if(page > 1){
        page--;
        show();
    }
}

</script>

</body>
</html>
