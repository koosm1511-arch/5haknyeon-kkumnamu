<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>꿈나무 공부방</title>

<style>
*{box-sizing:border-box}
body{
  margin:0;font-family:Arial,"Malgun Gothic",sans-serif;
  background:#f4f7ff;color:#203354
}
header{
  background:white;padding:18px;text-align:center;
  font-size:24px;font-weight:bold;color:#2869e8
}
.hero{
  padding:35px 15px;text-align:center;
  background:linear-gradient(120deg,#dceaff,#e9f8ff)
}
.hero h1{font-size:clamp(27px,5vw,42px)}
main{max-width:1000px;margin:auto;padding:20px}
.panel{
  background:white;border:1px solid #e0e8f5;
  border-radius:18px;padding:20px;margin-bottom:18px
}
.subjects,.answers,.characters{
  display:grid;grid-template-columns:repeat(2,minmax(0,1fr));
  gap:12px
}
button{font:inherit;cursor:pointer}
.subject,.answer,.character{
  padding:14px;background:white;border:1px solid #d8e2f1;
  border-radius:13px;color:#203354
}
.subject.active{border:2px solid #4382fa;background:#f0f6ff}
.subject .emoji,.character .emoji{font-size:35px;display:block}
.answer{text-align:left}
.answer.correct{background:#e1f8e9;border-color:#37a56b}
.answer.wrong{background:#fff0ed;border-color:#e57b70}
button:disabled{opacity:.6;cursor:default}
.progress,.levelbar{
  background:#e8edf6;border-radius:30px;overflow:hidden;height:10px;
  margin:14px 0
}
.progress div,.levelbar div{
  height:100%;width:0;background:#3478f6;transition:width .2s
}
#question{font-size:21px;font-weight:bold;line-height:1.6;margin:22px 0}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.stat{background:#f3f7ff;border-radius:13px;padding:13px;text-align:center}
.stat strong{display:block;font-size:22px;margin:5px}
.muted{font-size:13px;color:#71819b}
.actions{display:flex;justify-content:space-between;gap:10px;margin-top:16px}
.action{border:0;padding:12px 17px;border-radius:11px;font-weight:bold}
.primary{background:#3478f6;color:white}
.secondary{background:#edf1f8;color:#304665}
.feedback{display:none;padding:13px;border-radius:12px;line-height:1.7;margin-top:12px}
.feedback.show{display:block}
.good{background:#e5f8ed;color:#176340}
.bad{background:#fff0ed;color:#9b382e}
#character-section{display:none}
#character-section.show{display:block}
.characters{grid-template-columns:repeat(5,minmax(0,1fr))}
.character{text-align:center;overflow:hidden}
.character img{width:76px;height:76px;object-fit:contain;display:block;margin:5px auto}
.character:hover,.character.selected{border:2px solid #4382fa;background:#eef5ff}
#chosen-character{text-align:center;display:none;margin-top:24px}
#chosen-character img{width:180px;height:180px;object-fit:contain}
#chosen-character.show{display:block}
#chosen-character h3{font-size:25px;color:#2869e8}
.attribution{font-size:12px;color:#71819b;line-height:1.6}
footer{background:#203554;color:white;text-align:center;padding:22px}
@media(max-width:650px){
  .characters{grid-template-columns:repeat(2,minmax(0,1fr))}
  main{padding:12px}
  .stats{gap:5px}
  .stat{padding:8px 3px}
  .stat strong{font-size:18px}
}
</style>
</head>

<body>
<header>✏️ 꿈나무 공부방</header>

<section class="hero">
  <h1>공부하면 실력이 쑥쑥! 🌱</h1>
  <p>퀴즈를 모두 맞히고 좋아하는 캐릭터를 만나 보자!</p>
</section>

<main>
  <section class="panel">
    <h2>🏆 나의 공부 기록</h2>
    <div class="stats">
      <div class="stat">✅<strong id="total">0</strong><span class="muted">누적 정답</span></div>
      <div class="stat">✨<strong id="xp">0 XP</strong><span class="muted">경험치</span></div>
      <div class="stat">🎖️<strong id="level">레벨 1</strong><span class="muted">나의 레벨</span></div>
    </div>
    <div class="levelbar"><div id="level-progress"></div></div>
    <p id="level-message" class="muted">100 XP를 모으면 다음 레벨!</p>
  </section>

  <section class="panel">
    <h2>📚 과목 선택</h2>
    <div class="subjects">
      <button class="subject active" data-subject="수학"><span class="emoji">➗</span>수학</button>
      <button class="subject" data-subject="국어"><span class="emoji">✍️</span>국어</button>
      <button class="subject" data-subject="과학"><span class="emoji">🔬</span>과학</button>
      <button class="subject" data-subject="사회"><span class="emoji">🌏</span>사회</button>
    </div>
  </section>

  <section class="panel">
    <h2>🧠 퀴즈 도전</h2>
    <span id="subject-label">수학</span>
    <span id="number" style="float:right">1번 문제</span>
    <div class="progress"><div id="progress"></div></div>
    <div id="question">문제를 불러오는 중...</div>
    <div class="answers" id="answers"></div>
    <div class="feedback" id="feedback" aria-live="polite"></div>
    <div class="actions">
      <button class="action secondary" id="restart">다시 시작</button>
      <button class="action primary" id="next" disabled>다음 문제 →</button>
    </div>
  </section>

  <!-- 모든 문제를 맞힌 경우에만 나타나는 캐릭터 선택 화면 -->
  <section class="panel" id="character-section">
    <h2>🎉 축하해! 모든 문제를 맞혔어!</h2>
    <p>친구들이 좋아하는 캐릭터를 골라 봐!</p>

    <div class="characters" id="character-list"></div>

    <div id="chosen-character">
      <h3 id="chosen-name"></h3>
      <img id="chosen-image" alt="내가 고른 캐릭터">
      <p id="chosen-message"></p>
      <p>🏆 퀴즈 올 클리어 성공!</p>
    </div>

    <p class="attribution">
      캐릭터 그림: OpenMoji
      (<a href="https://openmoji.org/" target="_blank" rel="noopener">사이트</a>),
      CC BY-SA 4.0
    </p>
  </section>
</main>

<footer>🌱 꿈나무 공부방 · 오늘도 멋지게 성장하기!</footer>

<script>
const bank = {
  수학: [
    {q:"1/2와 크기가 같은 분수는?",a:["2/3","2/4","3/4","1/3"],c:1,e:"분자와 분모에 2를 곱하면 2/4야."},
    {q:"1.25 + 0.5는?",a:["1.30","1.70","1.75","2.25"],c:2,e:"1.25 + 0.50 = 1.75야."},
    {q:"가로 8cm, 세로 3cm인 직사각형의 넓이는?",a:["11㎠","22㎠","24㎠","48㎠"],c:2,e:"8 × 3 = 24㎠야."},
    {q:"36의 약수가 아닌 것은?",a:["2","4","6","5"],c:3,e:"36은 5로 나누어떨어지지 않아."},
    {q:"삼각형 세 내각의 합은?",a:["90도","180도","270도","360도"],c:1,e:"삼각형 세 내각의 합은 180도야."}
  ],
  국어: [
    {q:"‘마음이 넓다’와 뜻이 가까운 말은?",a:["키가 크다","너그럽다","멀리 있다","좁다"],c:1,e:"다른 사람을 잘 이해하고 너그럽다는 뜻이야."},
    {q:"원인과 결과가 드러난 문장은?",a:["하늘은 파랗다","비가 와서 길이 젖었다","꽃이 예쁘다","나는 걸었다"],c:1,e:"비가 온 것이 원인, 길이 젖은 것이 결과야."},
    {q:"‘성실하다’의 뜻은?",a:["맡은 일을 정성껏 하다","쉽게 포기하다","크게 말하다","빨리 달리다"],c:0,e:"꾸준하고 정성껏 일을 한다는 뜻이야."},
    {q:"대화할 때 좋은 태도는?",a:["말 끊기","딴짓하기","끝까지 듣기","소리 지르기"],c:2,e:"상대방의 말을 끝까지 듣는 것이 좋아."},
    {q:"‘즐겁다’와 뜻이 가까운 말은?",a:["기쁘다","슬프다","무섭다","화나다"],c:0,e:"기쁘다와 즐겁다는 뜻이 비슷해."}
  ],
  과학: [
    {q:"식물이 햇빛을 이용해 양분을 만드는 작용은?",a:["증발","광합성","응결","침식"],c:1,e:"식물은 빛에너지를 이용해 광합성을 해."},
    {q:"물이 얼음으로 변하는 것은?",a:["융해","기화","응고","용해"],c:2,e:"액체가 고체로 변하는 것을 응고라고 해."},
    {q:"우리가 사는 행성은?",a:["화성","지구","목성","금성"],c:1,e:"우리가 사는 행성은 지구야."},
    {q:"자석에 잘 붙는 물질은?",a:["나무","종이","철","유리"],c:2,e:"철은 자석에 잘 붙어."},
    {q:"낮과 밤이 생기는 주된 까닭은?",a:["지구의 자전","구름의 움직임","계절 변화","달의 모양"],c:0,e:"지구가 자전하면서 낮과 밤이 바뀌어."}
  ],
  사회: [
    {q:"지도에서 실제 거리를 줄여 나타낸 정도는?",a:["범례","축척","방위","기호"],c:1,e:"축척은 지도 거리와 실제 거리의 비율이야."},
    {q:"동서남북을 확인하는 데 사용하는 것은?",a:["축척","방위표","그래프","시간표"],c:1,e:"방위표는 방향을 알려 줘."},
    {q:"규칙이 필요한 까닭은?",a:["다툼을 늘리려고","안전하게 생활하려고","약속을 없애려고","한 사람만 편하려고"],c:1,e:"규칙은 모두가 질서 있고 안전하게 지내도록 도와줘."},
    {q:"물건을 사고파는 활동은?",a:["경제 활동","날씨 관측","식물 성장","지구 자전"],c:0,e:"물건을 사고파는 것은 경제 활동이야."},
    {q:"우리나라의 수도는?",a:["부산","서울","대전","제주"],c:1,e:"대한민국의 수도는 서울이야."}
  ]
};

// 캐릭터 그림은 온라인에서 불러와.
const characters = [
  {
    name:"고양이",
    emoji:"🐱",
    image:"https://openmoji.org/data/color/svg/1F431.svg",
    message:"야옹! 정말 잘했어! 🐾"
  },
  {
    name:"강아지",
    emoji:"🐶",
    image:"https://openmoji.org/data/color/svg/1F436.svg",
    message:"멍멍! 넌 최고의 공부 친구야!"
  },
  {
    name:"공룡",
    emoji:"🦖",
    image:"https://openmoji.org/data/color/svg/1F996.svg",
    message:"우와! 공룡처럼 힘차게 성장하자!"
  },
  {
    name:"토끼",
    emoji:"🐰",
    image:"https://openmoji.org/data/color/svg/1F430.svg",
    message:"깡충! 오늘 정말 멋지게 해냈어!"
  },
  {
    name:"로봇",
    emoji:"🤖",
    image:"https://openmoji.org/data/color/svg/1F916.svg",
    message:"임무 성공! 너의 실력이 업그레이드됐어!"
  }
];

const $ = id => document.getElementById(id);
const today = new Date();
const todayKey = `${today.getFullYear()}-${today.getMonth()+1}-${today.getDate()}`;

function getSaved(key){
  try{return Math.max(0,Number(localStorage.getItem(key))||0)}
  catch{return 0}
}

let total = getSaved("study_total");
let xp = getSaved("study_xp");
let todayCorrect = localStorage.getItem("study_date")===todayKey
  ? getSaved("study_today") : 0;

let subject = "수학";
let questions = [];
let position = 0;
let answered = false;
let correctThisRound = 0;

function shuffle(list){
  return [...list].sort(()=>Math.random()-0.5);
}

function save(){
  try{
    localStorage.setItem("study_total",total);
    localStorage.setItem("study_xp",xp);
    localStorage.setItem("study_today",todayCorrect);
    localStorage.setItem("study_date",todayKey);
  }catch{}
}

function updateStats(){
  const level=Math.floor(xp/100)+1;
  $("total").textContent=total;
  $("xp").textContent=xp+" XP";
  $("level").textContent="레벨 "+level;
  $("level-progress").style.width=(xp%100)+"%";
  $("level-message").textContent=
    `다음 레벨까지 ${100-(xp%100)} XP 남았어!`;
}

function startRound(){
  questions=shuffle(bank[subject]);
  position=0;
  correctThisRound=0;
  $("character-section").classList.remove("show");
  $("chosen-character").classList.remove("show");
  $("restart").textContent="다시 시작";
  renderQuestion();
}

function renderQuestion(){
  answered=false;
  const item=questions[position];

  $("subject-label").textContent=subject;
  $("number").textContent=`${position+1}/${questions.length} 문제`;
  $("progress").style.width=(position/questions.length*100)+"%";
  $("question").textContent=item.q;
  $("feedback").className="feedback";
  $("feedback").textContent="";
  $("next").disabled=true;
  $("next").textContent=position===questions.length-1
    ?"결과 보기 🎉":"다음 문제 →";
  $("answers").innerHTML="";

  item.a.forEach((answer,index)=>{
    const b=document.createElement("button");
    b.className="answer";
    b.textContent=["① ","② ","③ ","④ "][index]+answer;
    b.onclick=()=>chooseAnswer(index);
    $("answers").appendChild(b);
  });
}

function chooseAnswer(index){
  if(answered)return;
  answered=true;

  const item=questions[position];
  const buttons=[...$("answers").children];
  const correct=index===item.c;

  buttons.forEach((b,i)=>{
    b.disabled=true;
    if(i===item.c)b.classList.add("correct");
    if(i===index&&!correct)b.classList.add("wrong");
  });

  if(correct){
    correctThisRound++;
    total++;
    todayCorrect++;
    xp+=10;
    save();
    $("feedback").className="feedback show good";
    $("feedback").innerHTML="✅ 정답! +10 XP<br>"+item.e;
  }else{
    $("feedback").className="feedback show bad";
    $("feedback").textContent="괜찮아! 정답은 "+item.a[item.c]+"야. "+item.e;
  }

  $("progress").style.width=((position+1)/questions.length*100)+"%";
  $("next").disabled=false;
  updateStats();
}

function showCharacters(){
  $("question").textContent="모든 문제를 맞혔어! 정말 대단해! 🎉";
  $("answers").innerHTML="";
  $("feedback").className="feedback show good";
  $("feedback").textContent="이제 좋아하는 캐릭터를 선택해 봐!";
  $("progress").style.width="100%";
  $("number").textContent="클리어!";
  $("next").disabled=true;

  $("character-section").classList.add("show");
  $("character-section").scrollIntoView({behavior:"smooth",block:"start"});
}

function chooseCharacter(character){
  document.querySelectorAll(".character").forEach(b=>{
    b.classList.toggle("selected",b.dataset.name===character.name);
  });

  $("chosen-name").textContent="내가 고른 캐릭터: "+character.name;
  $("chosen-image").src=character.image;
  $("chosen-image").alt=character.name+" 그림";
  $("chosen-image").onerror=()=>{
    $("chosen-image").style.display="none";
    $("chosen-name").textContent+= " "+character.emoji;
  };
  $("chosen-image").onload=()=>{
    $("chosen-image").style.display="inline-block";
  };
  $("chosen-message").textContent=character.message;
  $("chosen-character").classList.add("show");
}

function buildCharacterPicker(){
  $("character-list").innerHTML="";

  characters.forEach(character=>{
    const button=document.createElement("button");
    button.className="character";
    button.dataset.name=character.name;
    button.innerHTML=`
      <img src="${character.image}" alt="${character.name}"
           onerror="this.style.display='none';this.nextElementSibling.style.display='block'">
      <span class="emoji" style="display:none">${character.emoji}</span>
      <b>${character.name}</b>
    `;
    button.onclick=()=>chooseCharacter(character);
    $("character-list").appendChild(button);
  });
}

document.querySelectorAll(".subject").forEach(button=>{
  button.onclick=()=>{
    subject=button.dataset.subject;
    document.querySelectorAll(".subject").forEach(b=>
      b.classList.toggle("active",b===button)
    );
    startRound();
  };
});

$("next").onclick=()=>{
  if(!answered)return;

  if(position<questions.length-1){
    position++;
    renderQuestion();
  }else if(correctThisRound===questions.length){
    // 이번 과목의 모든 문제를 맞혀야 캐릭터 선택 가능!
    showCharacters();
  }else{
    $("question").textContent=
      `${questions.length}문제 중 ${correctThisRound}문제를 맞혔어.`;
    $("answers").innerHTML="";
    $("feedback").className="feedback show bad";
    $("feedback").textContent=
      "캐릭터를 만나려면 이번 퀴즈를 전부 맞혀야 해! 다시 도전해 보자.";
    $("next").disabled=true;
    $("restart").textContent="다시 도전하기";
    $("restart").scrollIntoView({behavior:"smooth",block:"center"});
  }
};

$("restart").onclick=startRound;

buildCharacterPicker();
updateStats();
startRound();
</script>
</body>
</html>
