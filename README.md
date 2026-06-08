<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<title>ที่เที่ยวอำเภอเดชอุดม</title>

<style>
body{
    font-family: sans-serif;
    text-align: center;
    background: #f3f3f3;
    margin: 0;
}

h1{
    background: #2e7d32;
    color: white;
    margin: 0;
    padding: 15px;
}

.card{
    padding: 20px;
}

img{
    width: 90%;
    max-width: 750px;
    border-radius: 12px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.2);
}

button{
    padding: 10px 18px;
    margin: 10px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    background: #333;
    color: white;
}

button:hover{
    background: #555;
}

.place{
    font-size: 22px;
    margin-top: 10px;
}
</style>
</head>

<body>

<h1>🌿 ที่เที่ยวอำเภอเดชอุดม</h1>

<div class="card">

    <h2 id="title">วัดสำราญนิเวศ</h2>

    <img id="img"
    src="https://source.unsplash.com/800x500/?temple,thailand">

    <p class="place" id="desc">วัดสำคัญของอำเภอเดชอุดม บรรยากาศสงบ</p>

    <br>

    <button onclick="prev()">⬅️ ก่อนหน้า</button>
    <button onclick="next()">➡️ ถัดไป</button>

</div>

<script>
let page = 1;

const data = [
    {
        title:"วัดสำราญนิเวศ",
        img:"temple,thai,ubon",
        desc:"วัดดังในอำเภอเดชอุดม บรรยากาศเงียบสงบ เหมาะแก่การทำบุญ"
    },
    {
        title:"วัดบ้านทุ่งนางโอก",
        img:"temple,village,ubon",
        desc:"วัดท้องถิ่นในชุมชน วิถีชีวิตเรียบง่าย"
    },
    {
        title:"วัดป่าบ้านนา",
        img:"forest temple,thailand",
        desc:"วัดป่าร่มรื่น เหมาะสำหรับปฏิบัติธรรม"
    },
    {
        title:"ตลาดสดเดชอุดม",
        img:"thai market,ubon",
        desc:"แหล่งอาหารและของกินพื้นบ้าน"
    },
    {
        title:"แม่น้ำมูล (โซนใกล้เดชอุดม)",
        img:"river thailand sunset",
        desc:"จุดพักผ่อนริมแม่น้ำ บรรยากาศเย็นสบาย"
    },
    {
        title:"ทุ่งนาเดชอุดม",
        img:"rice field thailand ubon",
        desc:"วิวทุ่งนาเขียวขจี สวยมากช่วงฤดูฝน"
    },
    {
        title:"สะพานท้องถิ่น",
        img:"wood bridge thailand rural",
        desc:"จุดถ่ายรูปธรรมชาติในชุมชน"
    },
    {
        title:"สวนสาธารณะเดชอุดม",
        img:"park thailand rural",
        desc:"สวนพักผ่อน ออกกำลังกายของคนในพื้นที่"
    },
    {
        title:"หมู่บ้านเกษตรกรรม",
        img:"village thailand farming",
        desc:"เรียนรู้วิถีชีวิตชาวบ้านและเกษตรกร"
    },
    {
        title:"จุดชมพระอาทิตย์ตกเดชอุดม",
        img:"sunset thailand field",
        desc:"วิวพระอาทิตย์ตกสวยมาก เหมาะถ่ายรูป"
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
