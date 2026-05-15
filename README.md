<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>测测你的专属功夫茶 · 潮汕工夫茶礼仪位次</title>
    <style>
        *{margin:0;padding:0;box-sizing:border-box;font-family: "PingFang SC","微软雅黑","宋体",serif;}
        body{
            background: #f5efe6;
            color: #3a2e23;
            line-height: 1.6;
            min-height: 100vh;
            padding-bottom: 30px;
        }
        .container{
            max-width: 650px;
            margin: 0 auto;
            padding: 0 20px;
        }
        .box{
            background: rgba(255,255,255,0.92);
            border-radius: 18px;
            padding: 35px;
            margin: 25px 0;
            box-shadow: 0 6px 20px rgba(0,0,0,0.08);
            border: 1px solid #e2d6c7;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .box:hover{
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        /* 首页背景样式 */
        #home{
            background: url("https://picsum.photos/id/225/1200/800") center center / cover no-repeat;
            min-height: 650px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            border-radius: 18px;
            position: relative;
            overflow: hidden;
            margin-top: 30px;
        }
        #home::before{
            content: "";
            position: absolute;
            top:0;left:0;right:0;bottom:0;
            background: linear-gradient(to bottom, rgba(0,0,0,0.3), rgba(0,0,0,0.5));
            z-index: 1;
        }
        #home > *{
            position: relative;
            z-index: 2;
        }
        #home h1{
            color: #fff;
            font-size: 36px;
            margin-bottom: 30px;
            letter-spacing: 2px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }
        #home .desc{
            color: rgba(255,255,255,0.95);
            font-size: 18px;
            line-height: 2;
            margin-bottom: 40px;
        }
        h1{
            text-align: center;
            color: #8c5e31;
            margin-bottom: 20px;
            font-weight: normal;
            font-size: 26px;
        }
        .subtitle{
            text-align: center;
            color: #7a5837;
            margin-bottom: 25px;
            font-size: 15px;
        }
        .desc{
            text-align: center;
            margin-bottom: 25px;
            color: #555;
            line-height: 1.7;
        }
        .btn{
            display: block;
            width: 100%;
            background: linear-gradient(135deg, #8c5e31, #a67c4a);
            color: #fff;
            border: none;
            padding: 15px;
            font-size: 18px;
            border-radius: 12px;
            cursor: pointer;
            margin-top: 25px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(140, 94, 49, 0.3);
        }
        .btn:hover{
            background: linear-gradient(135deg, #704a26, #8c5e31);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(140, 94, 49, 0.4);
        }
        .btn:active{
            transform: translateY(0);
        }
        .question{display: none;}
        .question.active{display: block;
            animation: fadeIn 0.4s ease;
        }
        @keyframes fadeIn{
            from{opacity:0;transform:translateY(10px);}
            to{opacity:1;transform:translateY(0);}
        }
        .q-title{
            font-size: 18px;
            margin-bottom: 18px;
            font-weight: bold;
            color: #3a2e23;
        }
        .option{
            padding: 14px 18px;
            border: 1px solid #dcd0c2;
            border-radius: 10px;
            margin: 10px 0;
            cursor: pointer;
            transition: all 0.3s ease;
            background: #fff;
        }
        .option:hover{
            border-color: #8c5e31;
            background: #fdf6ee;
            transform: translateX(5px);
        }
        .result{display: none;text-align: center;
            animation: fadeIn 0.5s ease;
        }
        .result h2{
            color: #8c5e31;
            margin: 12px 0;
            font-size: 20px;
        }
        .result h1{
            font-size: 24px;
            margin: 10px 0;
        }
        .result-text{
            margin: 22px 0;
            text-align: left;
            line-height: 1.8;
            color: #333;
            background: #f8f3eb;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #8c5e31;
        }
        .progress{
            text-align: center;
            color: #999;
            margin-bottom: 12px;
            font-size: 14px;
        }
        .progress-bar{
            width: 100%;
            height: 6px;
            background: #eee;
            border-radius: 3px;
            margin-bottom: 20px;
            overflow: hidden;
        }
        .progress-fill{
            height: 100%;
            background: linear-gradient(90deg, #8c5e31, #a67c4a);
            border-radius: 3px;
            transition: width 0.3s ease;
        }
        .age-select{
            margin: 20px 0;
            text-align: center;
        }
        .age-select select{
            padding: 12px 20px;
            font-size: 16px;
            border-radius: 10px;
            border: 1px solid #dcd0c2;
            width: 80%;
            outline: none;
            color: #3a2e23;
            background: #fff;
            cursor: pointer;
            transition: border-color 0.3s ease;
        }
        .age-select select:focus{
            border-color: #8c5e31;
        }
        .order-box{
            background: #f8f3eb;
            border-left: 4px solid #8c5e31;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: left;
        }
        .order-title{
            font-weight: bold;
            color: #8c5e31;
            margin-bottom: 10px;
            font-size: 17px;
        }
        .order-num{
            font-size: 22px;
            font-weight: bold;
            color: #8c5e31;
            margin: 5px 0;
        }
        .rule-text{
            font-size: 14px;
            color: #666;
            margin-top: 8px;
        }
        .cup-img{
            width: 80%;
            max-width: 300px;
            height: 220px;
            object-fit: cover;
            display: block;
            margin: 20px auto;
            border-radius: 12px;
            background: #fff;
            border:1px solid #eee;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        .cup-img:hover{
            transform: scale(1.02);
        }
        .cup-text{
            text-align: center;
            font-size: 18px;
            color: #8c5e31;
            font-weight: bold;
            margin-top: 10px;
        }
        .tea-img{
            width: 100%;
            max-width: 400px;
            height: 250px;
            object-fit: cover;
            border-radius: 12px;
            margin: 20px auto;
            display: block;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        .share-btn{
            background: linear-gradient(135deg, #4CAF50, #66BB6A);
            margin-top: 15px;
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
        }
        .share-btn:hover{
            background: linear-gradient(135deg, #388E3C, #4CAF50);
            box-shadow: 0 6px 20px rgba(76, 175, 80, 0.4);
        }
        .culture-note{
            background: #fdf6ee;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            font-size: 14px;
            color: #666;
            text-align: left;
        }
        .culture-note h4{
            color: #8c5e31;
            margin-bottom: 8px;
            font-size: 15px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 首页 -->
        <div class="box" id="home">
            <h1>测测你的专属功夫茶</h1>
            <p class="desc">
                偷得浮生半日闲<br>
                一品茶香心自舒<br>
                先选年龄 → 完成性格测试<br>
                解锁你的专属茶杯与本命功夫茶
            </p>
            <button class="btn" onclick="goToAgePage()">开始测试</button>
        </div>

        <!-- 年龄选择页 -->
        <div class="box" id="agePage" style="display:none;">
            <h1>请选择你的年龄档位</h1>
            <p class="desc">将按照潮汕工夫茶正统礼仪<br>纯按年龄长幼，确定你的接杯顺序</p>
            <div class="age-select">
                <select id="ageSelect">
                    <option value="0">—— 请选择 ——</option>
                    <option value="1">55岁以上（长辈/最尊位）</option>
                    <option value="2">40～54岁（次尊位）</option>
                    <option value="3">30～39岁（中位次）</option>
                    <option value="4">24～29岁（青年位次）</option>
                    <option value="5">18～23岁（晚辈位次）</option>
                    <option value="6">18岁以下（最末位）</option>
                </select>
            </div>
            <button class="btn" onclick="goToQuiz()">确认，进入性格测试</button>
        </div>

        <!-- 答题区域 -->
        <div id="quiz"></div>

        <!-- 独立茶杯位次页 -->
        <div class="box" id="orderPage" style="display:none;">
            <h1>潮汕工夫茶·接杯位次</h1>
            <div class="order-box">
                <div class="order-title">你是第 <span id="orderNum" style="font-size:26px;">1</span> 个拿到茶杯</div>
                <p class="rule-text">排序规则：严格遵循潮汕工夫茶传统礼仪，纯按年龄长幼排序，长辈优先、年幼居后。</p>
            </div>

            <img id="cupImage" class="cup-img" src="" alt="专属茶杯">
            <p class="cup-text">你的专属茶杯是……</p>

            <button class="btn" onclick="goToTeaResult()">查看专属功夫茶结果</button>
            
            <div class="culture-note">
                <h4>潮汕工夫茶小知识</h4>
                <p>潮汕工夫茶讲究"先尊后卑，先老后少"，主人冲茶后，第一杯必须先敬最年长的长辈，这是潮汕地区流传千年的待客之道和礼仪文化。</p>
            </div>
        </div>

        <!-- 最终茶叶结果页 -->
        <div class="box result" id="result">
            <h2>测试完成 · 本命功夫茶</h2>
            <img id="teaImage" class="tea-img" src="" alt="本命功夫茶">
            <h1>你最适合的茶叶是：<span id="teaName"></span></h1>
            <div class="result-text" id="teaDesc"></div>
            
            <div class="culture-note">
                <h4>品茶小贴士</h4>
                <p>潮汕工夫茶讲究"高冲低洒，关公巡城，韩信点兵"，每一道工序都蕴含着潮汕人对生活的热爱和对客人的尊重。</p>
            </div>
            
            <button class="btn" onclick="restartTest()">重新测试</button>
            <button class="btn share-btn" onclick="shareResult()">分享给好友</button>
        </div>
    </div>

    <script>
        // 在线茶杯图片
        const cupImages = [
            "https://picsum.photos/id/30/600/400",
            "https://picsum.photos/id/31/600/400",
            "https://picsum.photos/id/32/600/400",
            "https://picsum.photos/id/33/600/400",
            "https://picsum.photos/id/34/600/400"
        ];

        // 在线茶叶图片
        const teaImages = [
            "https://picsum.photos/id/226/800/500", // 凤凰单丛
            "https://picsum.photos/id/227/800/500", // 安溪铁观音
            "https://picsum.photos/id/228/800/500", // 陈年普洱
            "https://picsum.photos/id/229/800/500", // 武夷大红袍
            "https://picsum.photos/id/230/800/500", // 鸭屎香单丛
            "https://picsum.photos/id/231/800/500"  // 正岩肉桂
        ];

        const questions = [
            {q:"1. 周末你更偏爱哪种状态？",opt:["A 安静独处，享受慢时光","B 约知己小聚，闲谈小叙","C 随性出门，自在放空","D 专注投入一件热爱的事"]},
            {q:"2. 旁人对你的印象更偏向？",opt:["A 温润内敛，心思细腻","B 爽朗通透，直爽真诚","C 平和佛系，从容淡定","D 清醒独立，自有风骨"]},
            {q:"3. 你更偏爱哪种茶汤口感？",opt:["A 清香淡雅，回甘悠长","B 香气高扬，层次丰富","C 温润柔和，醇厚顺滑","D 厚重沉稳，岩韵十足"]},
            {q:"4. 遇到烦心事你会？",opt:["A 自我消化，慢慢自愈","B 倾诉分享，释放情绪","C 看淡随缘，不困于心","D 理性面对，从容解决"]},
            {q:"5. 你向往的生活节奏是？",opt:["A 慢煮时光，安稳自在","B 张弛有度，鲜活有趣","C 随遇而安，平静知足","D 清醒笃定，稳步前行"]},
            {q:"6. 你更贴合哪种气质？",opt:["A 清雅文艺，温柔干净","B 灵动鲜活，自在洒脱","C 温润平和，治愈包容","D 沉稳大气，内敛有力量"]},
            {q:"7. 交友时你最看重？",opt:["A 相处舒服，三观契合","B 性格合拍，真诚有趣","C 人品踏实，低调靠谱","D 清醒同频，互相成长"]},
            {q:"8. 面对选择时你通常？",opt:["A 细腻谨慎，周全考量","B 遵从直觉，果断决定","C 顺其自然，不强求不纠结","D 理性分析，清醒笃定"]},
            {q:"9. 你喜欢的空间氛围是？",opt:["A 简约素雅，干净安静","B 温暖有烟火气，轻松自在","C 古朴温润，治愈安心","D 沉静高级，简约有质感"]},
            {q:"10. 你的性格底色更接近？",opt:["A 感性温柔，共情力强","B 乐观通透，不拧巴","C 温和包容，情绪稳定","D 冷静内敛，内心强大"]},
            {q:"11. 你的做事风格更像？",opt:["A 细致用心，慢工出细活","B 灵活随性，不拘小节","C 稳妥踏实，不冒进","D 利落有章法，沉稳靠谱"]},
            {q:"12. 你心中理想的人生状态是？",opt:["A 平淡安稳，岁月静好","B 自在随性，热烈生活","C 从容温润，知足常乐","D 沉淀自我，内心丰盈"]}
        ];

        const teaType = [
            {name:"凤凰单丛",desc:"你清雅通透、自带灵气，性格温柔细腻，不喜喧闹却自有风骨。如同凤凰单丛，香韵高雅、层次丰富，外表温润内敛，内心有自己的坚持与格调，是自带氛围感、让人相处舒服的温柔型人格。"},
            {name:"安溪铁观音",desc:"你随和温润、待人真诚，性格柔和无棱角，处事低调从容。像口感纯正的铁观音，顺滑回甘、不苦不涩，不张扬、不尖锐，情绪稳定、包容力强，是身边人都愿意亲近的治愈系人格。"},
            {name:"陈年普洱",desc:"你沉稳内敛、通透成熟，拥有远超同龄人的格局与包容心。如同陈年普洱，岁月沉淀、越品越香，性格醇厚安定，遇事冷静不慌乱，自带让人安心的沉稳气场。"},
            {name:"武夷大红袍",desc:"你气场鲜明、有主见有风骨，待人爽朗大方，做事干脆利落。像大红袍岩韵十足，气质独特不随波逐流，既有烟火气又有高级感，是人群中自带辨识度的清醒人格。"},
            {name:"鸭屎香单丛",desc:"你外表随性洒脱，内心细腻敏感，性格灵动有趣、从不呆板。如同鸭屎香，清香别致、回味清甜，温柔中带着小个性，不被世俗束缚，活得自在又通透。"},
            {name:"正岩肉桂",desc:"你冷静自持、内心坚定，有原则有底线，从不轻易被外界左右。像正岩肉桂，韵味厚重、气场沉稳，性格独立清醒，做事有分寸，自带低调又高级的强大气场。"}
        ];

        let currentQ = 0;
        let score = [0,0,0,0,0,0];
        let ageLevel = 0;

        // 首页→年龄页
        function goToAgePage(){
            document.getElementById('home').style.display = 'none';
            document.getElementById('agePage').style.display = 'block';
        }

        // 年龄页→答题页
        function goToQuiz(){
            ageLevel = parseInt(document.getElementById('ageSelect').value);
            if(ageLevel == 0){
                alert("请选择你的年龄档位");
                return;
            }
            document.getElementById('agePage').style.display = 'none';
            currentQ = 0;
            score = [0,0,0,0,0,0];
            renderQ();
        }

        // 渲染题目
        function renderQ(){
            const quizBox = document.getElementById('quiz');
            const q = questions[currentQ];
            const progress = ((currentQ + 1) / questions.length) * 100;
            
            let html = `
                <div class="box question active">
                    <div class="progress">${currentQ+1} / ${questions.length}</div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: ${progress}%"></div>
                    </div>
                    <div class="q-title">${q.q}</div>
            `;
            q.opt.forEach((item,idx)=>{
                html += `<div class="option" onclick="choose(${idx})">${item}</div>`;
            });
            html += `</div>`;
            quizBox.innerHTML = html;
        }

        // 选选项计分
        function choose(idx){
            score[idx]++;
            currentQ++;
            if(currentQ >= questions.length){
                // 答题完毕 跳茶杯位次页
                showCupOrderPage();
            }else{
                renderQ();
            }
        }

        // 答题结束 → 独立茶杯位次页
        function showCupOrderPage(){
            document.getElementById('quiz').innerHTML = '';
            // 随机茶杯图
            let randomIdx = Math.floor(Math.random() * cupImages.length);
            document.getElementById('cupImage').src = cupImages[randomIdx];
            document.getElementById('orderNum').innerText = ageLevel;

            document.getElementById('orderPage').style.display = 'block';
            // 滚动到顶部
            window.scrollTo({top: 0, behavior: 'smooth'});
        }

        // 茶杯页 → 茶叶最终结果页
        function goToTeaResult(){
            document.getElementById('orderPage').style.display = 'none';
            let maxIndex = score.indexOf(Math.max(...score));
            let tea = teaType[maxIndex];
            document.getElementById('teaName').innerText = tea.name;
            document.getElementById('teaDesc').innerText = tea.desc;
            document.getElementById('teaImage').src = teaImages[maxIndex];
            document.getElementById('result').style.display = 'block';
            // 滚动到顶部
            window.scrollTo({top: 0, behavior: 'smooth'});
        }

        // 重新测试
        function restartTest(){
            document.getElementById('result').style.display = 'none';
            document.getElementById('orderPage').style.display = 'none';
            document.getElementById('agePage').style.display = 'none';
            document.getElementById('quiz').innerHTML = '';
            document.getElementById('home').style.display = 'block';
            // 滚动到顶部
            window.scrollTo({top: 0, behavior: 'smooth'});
        }

        // 分享功能
        function shareResult(){
            let teaName = document.getElementById('teaName').innerText;
            let shareText = `我测出来的本命功夫茶是${teaName}！快来测测你的专属功夫茶和潮汕工夫茶接杯位次吧~`;
            
            if(navigator.share){
                navigator.share({
                    title: '测测你的专属功夫茶',
                    text: shareText,
                    url: window.location.href
                }).catch(console.error);
            }else{
                // 复制到剪贴板
                navigator.clipboard.writeText(shareText + ' ' + window.location.href)
                    .then(() => {
                        alert('分享链接已复制到剪贴板！');
                    })
                    .catch(() => {
                        alert('复制失败，请手动分享');
                    });
            }
        }
    </script>
</body>
</html>
