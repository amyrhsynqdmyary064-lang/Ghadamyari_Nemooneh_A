
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#101426">
<meta name="description" content="من قهرمانم؛ برنامه‌ریزی، پیشرفت و رقابت در مسیر موفقیت تحصیلی">
<title>من قهرمانم | مسیر پیشرفت من</title>

<style>
:root {
  --bg:#101426;
  --panel:#191f35;
  --panel2:#202943;
  --text:#f4f5ff;
  --muted:#9ba6c2;
  --primary:#8b7cff;
  --cyan:#38d9d0;
  --border:rgba(255,255,255,.09);
  --shadow:0 15px 40px rgba(0,0,0,.2);
}
body.light {
  --bg:#f2f4fb;
  --panel:#fff;
  --panel2:#edf0fa;
  --text:#20243a;
  --muted:#727b95;
  --border:rgba(20,30,60,.1);
  --shadow:0 12px 35px rgba(40,50,90,.08);
}
*{box-sizing:border-box}
body{
  margin:0;
  font-family:Tahoma,Arial,sans-serif;
  background:var(--bg);
  color:var(--text);
  transition:.3s;
}
button,input{font-family:inherit}
button{cursor:pointer}
.app{display:flex;min-height:100vh}
.sidebar{
  width:245px;
  background:var(--panel);
  border-left:1px solid var(--border);
  padding:25px 17px;
  position:fixed;
  top:0;bottom:0;right:0;
  z-index:10;
  display:flex;
  flex-direction:column;
}
.logo{
  font-size:22px;
  font-weight:bold;
  margin:5px 8px 35px;
}
.logo span{color:var(--primary)}
.logo small{
  display:block;
  color:var(--muted);
  font-size:10px;
  margin-top:8px;
  font-weight:normal;
}
.nav-title{
  color:var(--muted);
  font-size:11px;
  margin:15px 10px 10px;
}
.nav-btn{
  border:0;
  background:transparent;
  color:var(--muted);
  padding:14px;
  border-radius:13px;
  text-align:right;
  width:100%;
  margin:3px 0;
  font-size:13px;
  transition:.25s;
}
.nav-btn:hover,.nav-btn.active{
  background:linear-gradient(110deg,rgba(139,124,255,.23),rgba(56,217,208,.08));
  color:var(--text);
  transform:translateX(-3px);
}
.sidebar-bottom{margin-top:auto}
.main{
  width:calc(100% - 245px);
  margin-right:245px;
  padding:30px;
  max-width:1600px;
}
.topbar{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:15px;
  margin-bottom:30px;
}
.welcome h1{font-size:23px;margin:0 0 9px}
.welcome p{color:var(--muted);font-size:12px;margin:0}
.actions{display:flex;gap:10px}
.icon-btn{
  background:var(--panel);
  border:1px solid var(--border);
  color:var(--text);
  border-radius:12px;
  width:43px;height:43px;
  font-size:18px;
}
.hero{
  background:linear-gradient(115deg,#6556d9,#373a91 58%,#147e87);
  padding:27px;
  border-radius:22px;
  position:relative;
  overflow:hidden;
  box-shadow:var(--shadow);
  margin-bottom:22px;
  animation:rise .7s ease;
}
.hero:after{
  content:"";
  position:absolute;
  width:220px;height:220px;
  border:35px solid rgba(255,255,255,.08);
  border-radius:50%;
  left:-45px;top:-100px;
}
.hero h2{font-size:22px;margin:0 0 12px}
.hero p{font-size:12px;line-height:2;color:#eee}
.hero strong{color:#fff}
.hero .hero-btn{
  border:0;background:white;color:#423a9a;
  padding:12px 18px;border-radius:10px;
  font-weight:bold;margin-top:8px;
}
.stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:15px;
  margin-bottom:22px;
}
.stat,.card{
  background:var(--panel);
  border:1px solid var(--border);
  border-radius:18px;
  padding:20px;
  box-shadow:var(--shadow);
}
.stat-label{font-size:12px;color:var(--muted)}
.stat-value{font-size:26px;font-weight:bold;margin:13px 0 7px}
.stat-note{font-size:10px;color:var(--cyan)}
.content-grid{
  display:grid;
  grid-template-columns:1.35fr .85fr;
  gap:18px;
}
.card{margin-bottom:18px;min-width:0}
.card-head{
  display:flex;justify-content:space-between;
  align-items:center;margin-bottom:20px;gap:10px;
}
.card-head h3{font-size:15px;margin:0}
.card-head span{font-size:11px;color:var(--muted)}
.task-form{display:flex;gap:8px;margin-bottom:18px}
.task-form input{
  min-width:0;flex:1;
  background:var(--panel2);
  border:1px solid var(--border);
  color:var(--text);
  border-radius:10px;padding:13px;
  outline:none;
}
.primary-btn{
  border:0;border-radius:10px;
  padding:12px 16px;
  background:var(--primary);
  color:white;font-weight:bold;
}
.task{
  display:flex;align-items:center;
  gap:10px;padding:13px 5px;
  border-bottom:1px solid var(--border);
  font-size:12px;
}
.task:last-child{border-bottom:0}
.task input{accent-color:var(--primary);width:17px;height:17px}
.task.done .task-name{
  text-decoration:line-through;color:var(--muted);
}
.task-name{flex:1;overflow-wrap:anywhere}
.delete-btn{
  border:0;background:transparent;color:#ff7185;
  font-size:17px;
}
.empty{font-size:12px;color:var(--muted);text-align:center;padding:20px}
.timer-box{text-align:center;padding:12px 0}
.timer{
  font-size:45px;font-weight:bold;
  letter-spacing:2px;margin:15px 0;
  color:var(--cyan);
}
.timer-controls{display:flex;justify-content:center;gap:9px}
.timer-controls button{
  border:0;border-radius:10px;
  padding:11px 17px;background:var(--primary);
  color:white;font-weight:bold;
}
.timer-controls .secondary{
  background:var(--panel2);color:var(--text);
}
.progress-track{
  height:9px;background:var(--panel2);
  border-radius:20px;overflow:hidden;margin-top:12px;
}
.progress-fill{
  height:100%;width:0;
  background:linear-gradient(90deg,var(--primary),var(--cyan));
  border-radius:20px;transition:.4s;
}
.league-item{
  display:flex;align-items:center;
  gap:12px;padding:13px 0;
  border-bottom:1px solid var(--border);
  font-size:12px;
}
.league-item:last-child{border:0}
.rank{
  width:30px;height:30px;
  display:grid;place-items:center;
  background:var(--panel2);border-radius:9px;
}
.league-item strong{margin-right:auto}
.page{display:none;animation:rise .35s ease}
.page.active{display:block}
.section-title{font-size:22px;margin:5px 0 20px}
.info-box{
  padding:18px;border-radius:13px;
  background:var(--panel2);
  color:var(--muted);font-size:12px;line-height:2;
}
.profile-card{text-align:center}
.avatar{
  width:75px;height:75px;border-radius:24px;
  background:linear-gradient(135deg,var(--primary),var(--cyan));
  display:grid;place-items:center;
  font-size:32px;margin:5px auto 15px;
}
.mobile-title{display:none}
footer{
  text-align:center;color:var(--muted);
  font-size:10px;padding:20px;
}
@keyframes rise{
  from{opacity:0;transform:translateY(12px)}
  to{opacity:1;transform:translateY(0)}
}
@media(max-width:950px){
  .stats{grid-template-columns:repeat(2,1fr)}
  .content-grid{grid-template-columns:1fr}
}
@media(max-width:650px){
  .sidebar{
    top:auto;bottom:0;right:0;left:0;
    width:100%;height:68px;
    padding:5px 4px;
    border-left:0;border-top:1px solid var(--border);
    flex-direction:row;justify-content:space-around;
  }
  .logo,.nav-title,.sidebar-bottom{display:none}
  .nav-btn{
    width:auto;flex:1;text-align:center;
    padding:10px 2px;font-size:10px;
    margin:0;white-space:nowrap;
  }
  .main{
    width:100%;margin:0;padding:20px 13px 85px;
  }
  .topbar{margin-bottom:20px}
  .welcome h1{font-size:18px}
  .welcome p{font-size:10px}
  .hero{padding:22px}
  .hero h2{font-size:18px}
  .stat{padding:15px}
  .stat-value{font-size:22px}
  .card{padding:16px}
  .mobile-title{display:block}
}
</style>
</head>

<body>
<div class="app">

<aside class="sidebar">
  <div class="logo">🏆 من <span>قهرمانم</span>
    <small>هر روز، یک قدم به جلو</small>
  </div>

  <div class="nav-title">منوی اصلی</div>
  <button class="nav-btn active" data-page="dashboard">🏠 داشبورد</button>
  <button class="nav-btn" data-page="tasks">📝 برنامه و وظایف</button>
  <button class="nav-btn" data-page="timer">⏱️ زمان مطالعه</button>
  <button class="nav-btn" data-page="league">🏅 رقابت و لیگ</button>
  <button class="nav-btn" data-page="profile">👤 پروفایل من</button>

  <div class="sidebar-bottom">
    <button class="nav-btn" id="themeButton">🌗 تغییر پوسته</button>
  </div>
</aside>

<main class="main">

<header class="topbar">
  <div class="welcome">
    <h1>مسیر قهرمانی تو شروع شده! 🚀</h1>
    <p id="todayDate">امروز، روز ساختن آینده است.</p>
  </div>
  <div class="actions">
    <button class="icon-btn" id="themeButtonTop" title="تغییر پوسته">🌗</button>
  </div>
</header>

<section class="page active" id="dashboard">

  <div class="hero">
    <h2>قهرمان شدن اتفاقی نیست!</h2>
    <p>هر هدفی که امروز انجام می‌دهی، تو را به نسخه قوی‌تری از خودت نزدیک می‌کند.</p>
    <strong>از همین امروز شروع کن.</strong><br>
    <button class="hero-btn" onclick="showPage('tasks')">برنامه امروز من ←</button>
  </div>

  <div class="stats">
    <div class="stat">
      <div class="stat-label">📚 وظایف انجام‌شده</div>
      <div class="stat-value" id="completedStat">۰</div>
      <div class="stat-note">تعداد کارهای تکمیل‌شده</div>
    </div>
    <div class="stat">
      <div class="stat-label">🎯 وظایف باقی‌مانده</div>
      <div class="stat-value" id="remainingStat">۰</div>
      <div class="stat-note">قدم‌های بعدی تو</div>
    </div>
    <div class="stat">
      <div class="stat-label">⏱️ زمان مطالعه</div>
      <div class="stat-value" id="studyStat">۰</div>
      <div class="stat-note">دقیقه ثبت‌شده</div>
    </div>
    <div class="stat">
      <div class="stat-label">⭐ امتیاز تو</div>
      <div class="stat-value" id="pointsStat">۰</div>
      <div class="stat-note">با انجام وظایف امتیاز بگیر</div>
    </div>
  </div>

  <div class="content-grid">
    <div class="card">
      <div class="card-head">
        <h3>📝 برنامه امروز</h3>
        <span id="taskCount">۰ وظیفه</span>
      </div>
      <form class="task-form" id="taskForm">
        <input id="taskInput" placeholder="وظیفه جدید را بنویس..." maxlength="100" required>
        <button class="primary-btn" type="submit">افزودن +</button>
      </form>
      <div id="taskList"></div>
      <div class="progress-track">
        <div class="progress-fill" id="progressFill"></div>
      </div>
      <p class="stat-label" id="progressText">۰٪ پیشرفت امروز</p>
    </div>

    <div>
      <div class="card">
        <div class="card-head">
          <h3>⏱️ تمرکز سریع</h3>
          <span>تایمر مطالعه</span>
        </div>
        <div class="timer-box">
          <div class="timer" id="timerDisplay">25:00</div>
          <div class="timer-controls">
            <button id="startTimer">شروع</button>
            <button class="secondary" id="resetTimer">بازنشانی</button>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-head">
          <h3>🏆 مسیر قهرمانی</h3>
          <span>هدف تو</span>
        </div>
        <div class="info-box">
          با انجام وظایف و ثبت زمان مطالعه، امتیاز جمع کن و پیشرفتت را دنبال کن.
        </div>
      </div>
    </div>
  </div>
</section>

<section class="page" id="tasks">
  <h2 class="section-title">📝 برنامه و وظایف</h2>
  <div class="card">
    <div class="card-head"><h3>وظایف من</h3></div>
    <form class="task-form" id="taskForm2">
      <input id="taskInput2" placeholder="وظیفه جدید..." maxlength="100" required>
      <button class="primary-btn">افزودن +</button>
    </form>
    <div id="taskList2"></div>
  </div>
</section>

<section class="page" id="timer">
  <h2 class="section-title">⏱️ مرکز تمرکز</h2>
  <div class="card">
    <div class="timer-box">
      <p class="stat-label">زمان باقی‌مانده</p>
      <div class="timer" id="timerDisplay2">25:00</div>
      <div class="timer-controls">
        <button id="startTimer2">شروع مطالعه</button>
        <button class="secondary" id="resetTimer2">بازنشانی</button>
      </div>
      <p class="stat-label">هر جلسه تمرکز، یک قدم به موفقیت نزدیک‌ترت می‌کند.</p>
    </div>
  </div>
</section>

<section class="page" id="league">
  <h2 class="section-title">🏅 رقابت و لیگ</h2>
  <div class="card">
    <h3>لیگ قهرمانان</h3>
    <div class="info-box">
      بخش رقابت فردی و گروهی در حال آماده‌سازی اتصال به سرور است.
      برای رقابت واقعی، ثبت‌نام کاربران، گروه‌ها و جدول رتبه‌بندی باید به پایگاه داده متصل شوند.
    </div>
    <div class="league-item"><div class="rank">🥇</div> رتبه اول <strong>---</strong></div>
    <div class="league-item"><div class="rank">🥈</div> رتبه دوم <strong>---</strong></div>
    <div class="league-item"><div class="rank">🥉</div> رتبه سوم <strong>---</strong></div>
  </div>
</section>

<section class="page" id="profile">
  <h2 class="section-title">👤 پروفایل من</h2>
  <div class="card profile-card">
    <div class="avatar">🏆</div>
    <h3>قهرمان آینده</h3>
    <p class="stat-label">عضو باشگاه من قهرمانم</p>
    <div class="info-box">
      امتیاز: <strong id="profilePoints">۰</strong><br>
      وظایف تکمیل‌شده: <strong id="profileTasks">۰</strong><br>
      زمان مطالعه: <strong id="profileStudy">۰ دقیقه</strong>
    </div>
  </div>
</section>

<footer>من قهرمانم | مسیر پیشرفت از امروز آغاز می‌شود ✨</footer>

</main>
</div>

<script>
const $ = id => document.getElementById(id);

let data;
try {
  data = JSON.parse(localStorage.getItem("championData")) || {
    tasks:[],
    studyMinutes:0,
    points:0
  };
} catch {
  data = {tasks:[],studyMinutes:0,points:0};
}

function save(){
  localStorage.setItem("championData",JSON.stringify(data));
}

function fa(number){
  return Number(number).toLocaleString("fa-IR");
}

function addTask(value){
  const name=value.trim();
  if(!name)return;
  data.tasks.push({
    id:Date.now()+Math.random(),
    name,
    done:false
  });
  save();
  render();
}

function toggleTask(id){
  const task=data.tasks.find(t=>t.id===id);
  if(!task)return;
  task.done=!task.done;
  data.points=Math.max(0,data.points+(task.done?10:-10));
  save();
  render();
}

function deleteTask(id){
  data.tasks=data.tasks.filter(t=>t.id!==id);
  save();
  render();
}

function taskHTML(){
  if(!data.tasks.length){
    return '<div class="empty">هنوز وظیفه‌ای ثبت نکرده‌ای. اولین قدم را بردار! 🚀</div>';
  }

  return data.tasks.map(t=>`
    <div class="task ${t.done?'done':''}">
      <input type="checkbox" ${t.done?'checked':''}
        onchange="toggleTask(${t.id})">
      <span class="task-name">${escapeHTML(t.name)}</span>
      <button class="delete-btn" onclick="deleteTask(${t.id})" aria-label="حذف">×</button>
    </div>
  `).join("");
}

function escapeHTML(value){
  return value.replace(/[&<>"']/g, char => ({
    "&":"&amp;",
    "<":"&lt;",
    ">":"&gt;",
    '"':"&quot;",
    "'":"&#039;"
  })[char]);
}

function render(){
  const completed=data.tasks.filter(t=>t.done).length;
  const remaining=data.tasks.length-completed;
  const percent=data.tasks.length?
    Math.round(completed/data.tasks.length*100):0;

  $("taskList").innerHTML=taskHTML();
  $("taskList2").innerHTML=taskHTML();
  $("completedStat").textContent=fa(completed);
  $("remainingStat").textContent=fa(remaining);
  $("studyStat").textContent=fa(data.studyMinutes);
  $("pointsStat").textContent=fa(data.points);
  $("taskCount").textContent=fa(data.tasks.length)+" وظیفه";
  $("progressFill").style.width=percent+"%";
  $("progressText").textContent=fa(percent)+"٪ پیشرفت امروز";
  $("profilePoints").textContent=fa(data.points);
  $("profileTasks").textContent=fa(completed);
  $("profileStudy").textContent=fa(data.studyMinutes)+" دقیقه";
}

function bindForm(formId,inputId){
  $(formId).addEventListener("submit",e=>{
    e.preventDefault();
    addTask($(inputId).value);
    $(inputId).value="";
  });
}
bindForm("taskForm","taskInput");
bindForm("taskForm2","taskInput2");

function showPage(page){
  document.querySelectorAll(".page").forEach(p=>
    p.classList.toggle("active",p.id===page)
  );
  document.querySelectorAll(".nav-btn[data-page]").forEach(b=>
    b.classList.toggle("active",b.dataset.page===page)
  );
  window.scrollTo({top:0,behavior:"smooth"});
}

document.querySelectorAll(".nav-btn[data-page]").forEach(btn=>{
  btn.addEventListener("click",()=>showPage(btn.dataset.page));
});

function toggleTheme(){
  document.body.classList.toggle("light");
  localStorage.setItem(
    "championTheme",
    document.body.classList.contains("light")?"light":"dark"
  );
}
$("themeButton").onclick=toggleTheme;
$("themeButtonTop").onclick=toggleTheme;

if(localStorage.getItem("championTheme")==="light"){
  document.body.classList.add("light");
}

let seconds=1500;
let timerInterval=null;

function updateTimer(){
  const text=
    String(Math.floor(seconds/60)).padStart(2,"0")+":"+
    String(seconds%60).padStart(2,"0");
  $("timerDisplay").textContent=text;
  $("timerDisplay2").textContent=text;
}

function startTimer(){
  if(timerInterval){
    clearInterval(timerInterval);
    timerInterval=null;
    $("startTimer").textContent="ادامه";
    $("startTimer2").textContent="ادامه";
    return;
  }

  $("startTimer").textContent="توقف";
  $("startTimer2").textContent="توقف";

  timerInterval=setInterval(()=>{
    if(seconds>0){
      seconds--;
      updateTimer();
    }else{
      clearInterval(timerInterval);
      timerInterval=null;
      data.studyMinutes+=25;
      data.points+=15;
      save();
      render();
      alert("آفرین! یک جلسه تمرکز کامل شد 🏆");
      resetTimer();
    }
  },1000);
}

function resetTimer(){
  if(timerInterval)clearInterval(timerInterval);
  timerInterval=null;
  seconds=1500;
  $("startTimer").textContent="شروع";
  $("startTimer2").textContent="شروع مطالعه";
  updateTimer();
}

$("startTimer").onclick=startTimer;
$("startTimer2").onclick=startTimer;
$("resetTimer").onclick=resetTimer;
$("resetTimer2").onclick=resetTimer;

const now=new Date();
$("todayDate").textContent=
  "امروز "+now.toLocaleDateString("fa-IR")+"؛ یک فرصت تازه برای پیشرفت.";

render();
updateTimer();
</script>
</body>
</html>
