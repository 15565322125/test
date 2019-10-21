1.将两个字符利用字符串对象的方法变成一个字符,显示在页面id为h1的元素中
答:
        var str1 = 'he'
        var str2 = 'llo'
        var endStr = str1.concat(str2)
        h1.innerText = endStr

2.一个富豪想存87万,给理财顾问写了87w,请自动生成存储870000的方法,显示在页面id为h2的元素中
答:
        var writeMoney = '87w'
        var transMoney = (parseInt(writeMoney) + '').padEnd(6, 0)
        h2.innerText = transMoney

3.一个数字79387.348的工程款,保留两位小数存入,显示在页面id为h3的元素中
答:
        var money = 79387.348
        var savedMonth = money.toFixed(2)
        h3.innerText = savedMonth

4.一张图片是一个相对路径img/head/,icon/1.jpg,我只需要拿到它的文件夹目录后显示在页面id为h4的元素中
答:
        var picUrl = 'img/head/icon/1.jpg'
        var showUrl = picUrl.slice(0, picUrl.lastIndexOf('/') + 1)
        h4.innerText = showUrl

5.用户输入验证码,无论大小写输入都会正确的方法,显示在页面id为h1的元素中,显示在页面id为h4的元素中
答:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    验证码：
    <span id="h1">HeLLo</span>
    <h4 id="h4"></h4>
    <input type="text" id="txt" placeholder="请输入验证码">
    <button id="btn">验证</button>
    <script>
        txt.oninput = function(){
            h4.innerText = this.value
        }
        btn.onclick = function(){
            if(h1.innerText.toLowerCase() === txt.value.toLowerCase()){
                alert('验证成功')
            }else{
                alert('验证失败')
            }
        }
    </script>
</body>
</html>
