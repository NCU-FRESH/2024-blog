---
title: "開發測試空間"
tags: ["Blog"]
date: 2024-07-22
---
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

<div class="container text-center">
<div class="row">
<h4 class="text-3xl font-bold mb-4">上課大樓名稱查詢</h4>
</div>

<div class="row align-items-start">
<div class="col-8">
<input class="form-control mb-4" type="text" style="border-color: rgb(180 83 9); border-width: 0.15rem;" id="buildingCode" placeholder="輸入大樓代碼">
</div>
<div class="col-4">
<button class="btn text-white d-block col-12" style="background-color: #9e6b59;" onclick="
var isAppleDevice = /iPad|iPhone|iPod|Macintosh/.test(navigator.userAgent || navigator.vendor || window.opera);
var buildings = [
{code: 'A', name: '文學一館', g_map: 'https://goo.gl/maps/dmBrr4xnK1JeytGB8', a_map: 'https://maps.apple.com/?address=320317台灣桃園市中壢區&auid=8164453128013662295&ll=24.969378,121.194551&lsp=9902&q=國立中央大學文學一館&t=r'},
{code: 'C2', name: '文學二館', g_map: 'https://goo.gl/maps/LAnvszz6ZfMrTFEM6', a_map: 'https://maps.apple.com/?address=320台灣桃園市中壢區中大路300號&auid=9829456620230881551&ll=24.968771,121.194613&lsp=9902&q=文學二館&t=r'},
{code: 'E', name: '工程一館', g_map: 'https://goo.gl/maps/u5o81ZpRuXcqcgWTA', a_map: 'https://maps.apple.com/?address=320317台灣桃園市中壢區中大路300號&auid=5523926844627740521&ll=24.967091,121.192698&lsp=9902&q=工程一館&t=r'},
{code: 'E1', name: '工程二館(資電學院辦公室)', g_map: 'https://goo.gl/maps/AGSD5vLvzPScE44s9', a_map: 'https://maps.apple.com/?address=320台灣桃園市中壢區中大路300號&auid=6122627498224294796&ll=24.967375,121.191875&lsp=9902&q=工程二館&t=r'},
{code: 'E2', name: '機械館(工程三館)', g_map: 'https://goo.gl/maps/nVEe2kNxa8waVxx49', a_map: 'https://maps.apple.com/?address=國立中央大學324台灣桃園市平鎮區雙連里&auid=7243484797072291443&ll=24.967978,121.188737&lsp=9902&q=機械館&t=r'},
{code: 'E3', name: '環工化工館', g_map: 'https://goo.gl/maps/ChtrH8B9tM7phi6W9', a_map: 'https://maps.apple.com/?address=國立中央大學320台灣桃園市平鎮區雙連里&auid=14195489125104946467&ll=24.968329,121.187686&lsp=9902&q=環工化工館&t=r'},
{code: 'E4', name: '機電實驗室', g_map: 'https://goo.gl/maps/8Dx9stdKYXNXmkDu8', a_map: ''},
{code: 'E5', name: '大型力學實驗室', g_map: 'https://goo.gl/maps/6etywwTHiAtr1sEX6', a_map: 'https://maps.apple.com/?address=320317台灣桃園市中壢區中大路300號&auid=9415511250769958399&ll=24.968757,121.188555&lsp=9902&q=大型力學實驗室&t=r'},
{code: 'E6', name: '工程五館大樓(工學院辦公室)', g_map: 'https://goo.gl/maps/8jDtoAht8tX9chLR7', a_map: 'https://maps.apple.com/?address=國立中央大學324台灣桃園市平鎮區雙連里&auid=12009543488106939736&ll=24.967138,121.187682&lsp=9902&q=國立中央大學工程五館&t=r'},
{code: 'H2', name: '理學院教學館(原普化實驗大樓)', g_map: 'https://goo.gl/maps/vLByMzVArpChbsJY7', a_map: ''},
{code: 'HK', name: '客家學院大樓(客家學院辦公室)', g_map: 'https://goo.gl/maps/utfxMNFvBgn3DXDb7', a_map: 'https://maps.apple.com/?address=320台灣桃園市中壢區中大路300號&auid=1387615647684134107&ll=24.970848,121.190336&lsp=9902&q=國立中央大學客家學院大樓&t=r'},
{code: 'I', name: '志希館(管理學院辦公室)', g_map: 'https://goo.gl/maps/zr62NusULfHfjFXG8', a_map: 'https://maps.apple.com/?address=國立中央大學320台灣桃園市中壢區五權里&auid=18339168732871101213&ll=24.970216,121.193812&lsp=9902&q=志希館&t=r'},
{code: 'I1', name: '管理二館', g_map: 'https://goo.gl/maps/EBum6jS2MmY6KFZ57', a_map: 'https://maps.apple.com/?address=國立中央大學320台灣桃園市中壢區五權里&auid=11339571079636042899&ll=24.970690,121.193502&lsp=9902&q=管理二館&t=r'},
{code: 'IL', name: '國鼎光電大樓', g_map: 'https://goo.gl/maps/2KM5SHr7AMwScByKA', a_map: 'https://maps.apple.com/?address=國立中央大學320台灣桃園市平鎮區雙連里&auid=14616547687819694150&ll=24.970322,121.190389&lsp=9902&q=國鼎光電大樓&t=r'},
{code: 'L3', name: '國鼎圖書資料館', g_map: 'https://goo.gl/maps/PagQexZyk9eixE567', a_map: ''},
{code: 'LS', name: '人文社會科學大樓(文學院辦公室)', g_map: 'https://goo.gl/maps/Qmw1d2TtE6G1HDLq5', a_map: 'https://maps.apple.com/?address=320台灣桃園市中壢區中大路300號&auid=10666553622271177631&ll=24.969330,121.195185&lsp=9902&q=人文社會科學大樓&t=r'},
{code: 'M', name: '鴻經館', g_map: 'https://goo.gl/maps/5pg7urBkkxFekNvp6', a_map: 'https://maps.apple.com/?address=320011台灣桃園市中壢區&auid=11521147528526283842&ll=24.970795,121.192651&lsp=9902&q=中央大學鴻經館&t=r'},
{code: 'O', name: '綜教館(語言中心)', g_map: 'https://goo.gl/maps/NgBDQ13zUMdHGpLn7', a_map: 'https://maps.apple.com/?address=320台灣桃園市中壢區中大路300號&auid=17318161590537731525&ll=24.970628,121.195376&lsp=9902&q=國立中央大學綜合教學館&t=r'},
{code: 'T', name: '科學二館', g_map: 'https://goo.gl/maps/ExWuCGMWbTBrzF3m8', a_map: 'https://maps.apple.com/?address=320台灣桃園市中壢區中大路300號&auid=14361994485291521330&ll=24.968229,121.193134&lsp=9902&q=國立中央大學科學二館&t=r'}
];
var code = document.getElementById('buildingCode').value.trim().toUpperCase();
var result = buildings.find(building => building.code === code);
if (result) {
document.getElementById('result').innerHTML = `
<div class='card mx-auto' style='width: 90%; background-color:#e6d5cf;border-color: rgb(180 83 9); border-width: 0.15rem;'>
<a href='${isAppleDevice ? result.a_map : result.g_map}' class='btn btn-white  text-start' target='_blank'>
<div class='card-body'>
<span class='badge rounded-pill text-bg-info text-light fs-5'>${result.code}</span>
<h5 class='card-title fs-4 d-inline'>${result.name}</h5>
<div class='text-end col-12'>
<span class='text-end mx-2'>在地圖中開啟</span><svg class='d-inline fs-1' xmlns='http://www.w3.org/2000/svg' width='16' height='16' fill='currentColor' class='bi bi-box-arrow-up-right' viewBox='0 0 16 16'>
<path fill-rule='evenodd' d='M8.636 3.5a.5.5 0 0 0-.5-.5H1.5A1.5 1.5 0 0 0 0 4.5v10A1.5 1.5 0 0 0 1.5 16h10a1.5 1.5 0 0 0 1.5-1.5V7.864a.5.5 0 0 0-1 0V14.5a.5.5 0 0 1-.5.5h-10a.5.5 0 0 1-.5-.5v-10a.5.5 0 0 1 .5-.5h6.636a.5.5 0 0 0 .5-.5'/>
<path fill-rule='evenodd' d='M16 .5a.5.5 0 0 0-.5-.5h-5a.5.5 0 0 0 0 1h3.793L6.146 9.146a.5.5 0 1 0 .708.708L15 1.707V5.5a.5.5 0 0 0 1 0z'/>
</svg>
</div>

</div>
</a>
</div>
`;
} else {
document.getElementById('result').innerHTML = '找不到相應的大樓';
}">
查詢
</button>
</div>
</div>

<div class="row">
<div class="col-12" id="result"></div>
</div>
</div>