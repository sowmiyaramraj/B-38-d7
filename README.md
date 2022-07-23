# B-38-d7


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
  <script src="script.js"></script>
</body>
</html>

Get all the countries from the Asia continent /region using the Filter function
```````````````````````````````````````````````````````````````````````````````
var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function()
{
    var result=JSON.parse(request.response);
   // console.log(result[0]);
var reg=result.filter((ele)=>ele.region=="Asia")
var nm=reg.map((ele)=>ele.name)
console.log(nm);

}

POPULATION LESS THAN 200000
````````````````````````````
var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function()
{
    var result=JSON.parse(request.response);
    console.log(result[0]);
var reg=result.filter((ele)=>ele.population<200000)
var nm=reg.map((ele)=>ele.name)
console.log(nm);

}

TO GET THE TOTAL POPULATION 
```````````````````````````

var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function()
{
    var result=JSON.parse(request.response);
   // console.log(result[122].currency);
   
   var nm=result.map((ele)=>ele.population)

var res=nm.reduce((acc,ele)=>acc+ele,0);
console.log(res);

}

var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function()
{
    var result=JSON.parse(request.response);
   // console.log(result[122].currency);
   var nm=result.map((ele)=>ele.name)
   nm.forEach(element => console.log(element));


}

flag
````
var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function()
{
    var result=JSON.parse(request.response);
   // console.log(result[122].currency);
   var nm=result.map((ele)=>ele.flag)
   nm.forEach(element => console.log(element));


}

capital
`````````

var request=new XMLHttpRequest();
request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
request.send();
request.onload=function()
{
    var result=JSON.parse(request.response);
   // console.log(result[122].currency);
   var nm=result.map((ele)=>ele.capital)
   nm.forEach(element => console.log(element));


}

