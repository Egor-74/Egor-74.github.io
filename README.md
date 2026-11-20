[index.html](https://github.com/user-attachments/files/35186571/index.html)
<!doctype html>
<html lang="ru" class="no-js">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Bodrero: французская кондитерская, предзаказ эклеров и тортов</title>
<meta name="description" content="Кондитерская-пекарня Bodrero на Маросейке, Петровке, Рождественке и Сретенке. Соберите предзаказ эклеров или торта и отправьте готовый текст заявки.">
<link rel="preload" href="assets/fonts/marck-script-cyrillic.woff2" as="font" type="font/woff2" crossorigin>
<style>
@font-face{font-family:"Onest";font-weight:400 700;font-display:swap;src:url(assets/fonts/onest-cyrillic.woff2) format("woff2");unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}
@font-face{font-family:"Onest";font-weight:400 700;font-display:swap;src:url(assets/fonts/onest-latin.woff2) format("woff2");unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}
@font-face{font-family:"Marck";font-weight:400;font-display:swap;src:url(assets/fonts/marck-script-cyrillic.woff2) format("woff2");unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}
@font-face{font-family:"Marck";font-weight:400;font-display:swap;src:url(assets/fonts/marck-script-latin.woff2) format("woff2");unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}

:root{
  --fuchsia:#C4155F; --ink:#141214; --chalk:#1F2423; --chalk-2:#2A302F;
  --cream:#EEEDEA;--h2:clamp(40px,5vw,72px); --oak:#C99A62; --mint:#BFE3D3;
  --pad:clamp(20px,4vw,56px);
  --ease:cubic-bezier(.2,.8,.2,1);
  --script:"Marck","Onest",cursive; --sans:"Onest",system-ui,sans-serif;
}
*{box-sizing:border-box;margin:0;border-radius:0}
html{scroll-behavior:smooth}
body{font:400 18px/1.55 var(--sans);color:var(--ink);background:var(--cream);-webkit-font-smoothing:antialiased}
img{display:block;width:100%;height:100%;object-fit:cover}
a{color:inherit}
::selection{background:var(--fuchsia);color:var(--cream)}
:focus-visible{outline:3px solid var(--oak);outline-offset:3px}
h1,h2,h3{font-family:var(--script);font-weight:400;line-height:.98;letter-spacing:-.01em;text-wrap:balance}
h2{font-size:var(--h2)}
p{max-width:62ch}

.btn{display:inline-flex;align-items:center;justify-content:center;min-height:52px;padding:0 28px;background:var(--fuchsia);color:var(--cream);font:600 18px/1 var(--sans);text-decoration:none;border:0;cursor:pointer;transition:transform 140ms var(--ease),background-color 140ms var(--ease)}
.btn:active{transform:scale(.97)}
.btn[aria-disabled="true"]{background:var(--chalk-2);color:#B9B3A8;cursor:not-allowed}
.btn.quiet{background:var(--chalk-2)}
@media (hover:hover) and (pointer:fine){.btn:not([aria-disabled="true"]):hover{background:#A9104F}.btn.quiet:hover{background:#38403F!important}}

/* 1. первый экран */
.hero{position:relative;min-height:100svh;display:grid;grid-template-rows:auto 1fr;color:var(--cream);isolation:isolate}
.hero>picture,.hero>img{position:absolute;inset:0;z-index:-2}
.hero img{object-position:35% 45%}
.hero::after{content:"";position:absolute;inset:0;background:rgba(20,18,20,.4);z-index:-1}
.nav{display:flex;justify-content:space-between;align-items:center;padding:22px var(--pad)}
.nav .mark{font:400 28px/1 var(--script);text-decoration:none}
.nav a.l{font:600 18px/1 var(--sans);text-decoration:none;padding:12px 0}
.hero .copy{align-self:end;padding:0 var(--pad) clamp(40px,8vh,88px)}
.hero h1{font-size:clamp(40px,10vw,160px);line-height:.95;max-width:11em;animation:rise 560ms var(--ease) both}
.hero .lead{font-size:20px;margin:28px 0 32px;max-width:34em;animation:rise 560ms 90ms var(--ease) both}
.hero .btn{animation:rise 560ms 180ms var(--ease) both}
@keyframes rise{from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:none}}

/* 2. витрина */
.showcase{padding:0 0 clamp(88px,13vw,200px);display:grid;grid-template-columns:repeat(12,1fr);column-gap:clamp(16px,2vw,32px);row-gap:48px}
.showcase header{grid-column:1/-1;display:grid;grid-template-columns:repeat(12,1fr);column-gap:inherit;align-items:end}
.showcase h2{grid-column:1/-1;padding:0 var(--pad);font-size:clamp(48px,7vw,104px);color:var(--fuchsia)}
.f-wide{grid-column:1/-1;margin:0}
.f-wide .ph{aspect-ratio:21/9;overflow:hidden}
.f-wide figcaption{padding:0 var(--pad)}
.lede{grid-column:1/8;margin-left:var(--pad);font-size:28px;line-height:1.4}
.showcase figure{position:relative;margin:0}
.showcase figcaption{font-size:16px;margin-top:12px}
.f-main{grid-column:1/9;aspect-ratio:3/2}
.f-main .ph{aspect-ratio:4/3;overflow:hidden}
.showcase .f-tall{grid-column:8/-1;margin:12vh var(--pad) 0 0}
.showcase{align-items:start}
.f-tall .ph{aspect-ratio:4/5;overflow:hidden}
.showcase .f-small{grid-column:1/8;margin-left:var(--pad)}
.f-small .ph{aspect-ratio:4/5;overflow:hidden}
.showcase figcaption{margin-top:12px}
.f-main{aspect-ratio:auto}

/* 3. конструктор */
.order{background:var(--ink);color:var(--cream);padding:clamp(88px,12vw,180px) var(--pad)}
.order>h2{max-width:14em;margin-bottom:20px}
.order .sub{font-size:20px;margin-bottom:56px}
.order-grid{display:grid;grid-template-columns:7fr 5fr;gap:clamp(24px,4vw,64px);align-items:start}
.board{background:var(--chalk);border:16px solid var(--oak);padding:clamp(20px,3vw,40px)}
.row{display:grid;grid-template-columns:150px 1fr;gap:12px 24px;padding:18px 0;align-items:start}
.row+.row{margin-top:2px}
.row>.lab{font:400 28px/1.3 var(--script);padding-top:6px}
.opts{display:flex;flex-wrap:wrap;gap:6px 8px}
.word{position:relative;background:transparent;color:var(--cream);font:500 18px/1.3 var(--sans);padding:10px 14px 12px;border:0;cursor:pointer;transition:background-color 140ms var(--ease),transform 120ms var(--ease)}
.word::after{content:"";position:absolute;left:14px;right:14px;bottom:3px;height:4px;background:var(--fuchsia);transform:scaleX(0);transform-origin:left;transition:transform 200ms var(--ease)}
.word[aria-pressed="true"]::after{transform:scaleX(1)}
.word[aria-pressed="true"]{font-weight:600}
.word:active{transform:scale(.97)}
@media (hover:hover) and (pointer:fine){.word:hover{background:var(--chalk-2)}}
.opts.big .word{font:400 48px/1.3 var(--script);padding:6px 14px 14px}
.opts.big .word::after{height:6px;bottom:4px}
.field{width:100%;background:var(--chalk-2);color:var(--cream);font:400 18px/1.4 var(--sans);padding:14px 16px;border:0;min-height:52px;color-scheme:dark}
.field::placeholder{color:#B9B3A8}
textarea.field{min-height:96px;resize:vertical}
.flavors{display:grid;gap:4px;width:100%}
.fl{display:flex;justify-content:space-between;align-items:center;background:var(--chalk-2);padding:6px 6px 6px 16px;font-size:18px}
.step{display:flex;align-items:center;gap:4px}
.step button{width:44px;height:44px;background:var(--chalk);color:var(--cream);font:600 20px/1 var(--sans);border:0;cursor:pointer;transition:transform 120ms var(--ease)}
.step button:active{transform:scale(.94)}
.step output{min-width:34px;text-align:center;font-weight:600;font-variant-numeric:tabular-nums}
.total{font-size:16px;margin-top:8px}
[hidden]{display:none!important}
.sr{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap}

.side{position:sticky;top:12vh}
.side .ph{aspect-ratio:4/3;overflow:hidden;background:var(--chalk)}
.side .ph img{transition:opacity 220ms var(--ease)}
.side figcaption{font-size:16px;margin-top:12px}

.note{background:#FBF7EE;color:var(--ink);margin-top:-4px;padding:28px clamp(20px,3vw,40px) 32px;position:relative;grid-column:1/2;clip-path:inset(0)}
.note.in{animation:slip 280ms var(--ease) both}
@keyframes slip{from{clip-path:inset(0 0 100% 0);transform:translateY(-8px)}to{clip-path:inset(0);transform:none}}
.note .tag{display:inline-block;background:var(--fuchsia);color:var(--cream);font:600 16px/1.3 var(--sans);padding:8px 12px;margin-bottom:16px}
.note pre{font:400 18px/1.55 var(--sans);white-space:pre-wrap;max-width:60ch}
.note .acts{display:flex;flex-wrap:wrap;gap:10px;margin-top:24px}
.note .btn.quiet{background:var(--ink);color:var(--cream)}
.note .hint{font-size:16px;margin-top:18px;max-width:56ch}

/* 4. шторка */
.shutter{position:relative}
.shutter .ph{position:sticky;top:0;height:100svh}
.shutter .band{position:relative;z-index:1;background:var(--ink);color:var(--cream);padding:clamp(56px,10vw,120px) var(--pad)}
.shutter .band p{font-size:28px;line-height:1.4;max-width:30em}

/* 5. улицы */
.streets{background:var(--mint);padding:clamp(88px,12vw,180px) var(--pad)}
.streets>h2{margin-bottom:clamp(40px,6vw,88px)}
.st{display:grid;grid-template-columns:1fr 1fr;gap:clamp(20px,4vw,64px);align-items:center;padding:clamp(24px,3.5vw,48px) 0}
.st:nth-of-type(even)>:first-child{order:2}
.st h3{font-size:clamp(48px,7vw,104px)}
.st address{font-style:normal;font-size:20px;margin:14px 0 4px}
.st .metro,.st .hrs{font-size:18px}
.st .acts{display:flex;flex-wrap:wrap;gap:10px;margin-top:22px}
.st .btn.quiet{background:var(--ink);color:var(--cream)}
.st .ph{aspect-ratio:4/5;overflow:hidden}
.st .tel{aspect-ratio:4/5;background:var(--fuchsia);color:var(--cream);display:flex;align-items:end;padding:clamp(20px,3vw,36px);font:400 var(--h2)/1.1 var(--script);text-decoration:none}

/* 6. финал */
.final{position:relative;isolation:isolate;background:var(--chalk);color:var(--cream);min-height:90svh;display:grid}
.final .bg{position:absolute;inset:0;z-index:-2}
.final::after{content:"";position:absolute;inset:0;background:rgba(20,18,18,.55);z-index:-1}
.final .t{padding:clamp(56px,9vw,140px) var(--pad);display:flex;flex-direction:column;justify-content:center;align-items:flex-start;gap:32px}
.final h2{font-size:clamp(64px,10vw,144px);line-height:.95}

footer{background:var(--ink);color:var(--cream);padding:28px var(--pad);font-size:16px;display:flex;flex-wrap:wrap;gap:8px 32px;justify-content:space-between}
footer p{max-width:none}


/* появление: только когда скрипт включён */
.js .rv{opacity:0;transform:translateY(24px);transition:opacity 700ms var(--ease),transform 700ms var(--ease)}
.js .rv.on{opacity:1;transform:none}
.js .rp img{clip-path:inset(0 0 100% 0);transition:clip-path 800ms var(--ease)}
.js .rp.on img{clip-path:inset(0)}
.hero img{animation:drift 1800ms var(--ease) both}
@keyframes drift{from{transform:scale(1.06)}to{transform:none}}
@media (prefers-reduced-motion:reduce){.js .rv,.js .rp img{opacity:1;transform:none;clip-path:none;transition:none}.hero img{animation:none}}
@media (max-width:860px){
  .showcase{grid-template-columns:1fr;row-gap:40px}
  .showcase h2,.showcase .lede,.showcase .f-wide,.showcase .f-tall,.showcase .f-small{grid-column:1/-1;margin-left:0;margin-right:0;margin-top:0}
  .showcase figure:not(.f-wide),.showcase .lede,.showcase h2{margin-left:var(--pad)!important;margin-right:var(--pad)!important}
  .f-wide .ph{aspect-ratio:4/3}
  .lede{font-size:24px}
  .showcase h2{font-size:48px;padding:0}
  .f-wide figcaption{padding:0}
  .order-grid,.st{grid-template-columns:1fr}
  .note{grid-column:auto}
  .side{position:static;order:-1}
  .side .ph{aspect-ratio:4/3}
  .row{grid-template-columns:1fr;gap:4px}
  
  .opts.big .word{font-size:48px}
  .board{border-width:10px}
  .st .tel{order:-1}
  .st:nth-of-type(even)>:first-child{order:0}
  .st .ph,.st .tel{aspect-ratio:4/3}
  .shutter .band p{font-size:24px}
}
@media (prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}
  .hero h1,.hero .lead,.hero .btn{animation:none}
  .note.in{animation:none}
  .word::after,.word,.btn,.side .ph img{transition:none}
}
</style>
</head>
<body>

<header class="hero">
  <picture>
    <img src="assets/img/ya-01.jpg" alt="Витрина кондитерской Bodrero вечером: розовые двери, неон «Пейте хороший кофе»" fetchpriority="high">
  </picture>
  <nav class="nav" aria-label="Основное">
    <a class="mark" href="#top">Bodrero</a>
    <a class="l" href="#ulitsy">Адреса</a>
  </nav>
  <div class="copy" id="top">
    <h1>Эклеры и торты на заказ</h1>
    <p class="lead">Французская кондитерская на Маросейке, Петровке, Рождественке и Сретенке.</p>
    <a class="btn" href="#zakaz">Собрать заказ</a>
  </div>
</header>

<main>
<section class="showcase" aria-labelledby="h-vitrina">
  <figure class="f-wide"><div class="ph rp"><img src="assets/img/ya-16.jpg" alt="Витрина с медовиком, пирожными «Мон амур», тарталетками и эклерами" loading="lazy" style="object-position:50% 55%"></div></figure>
  <h2 id="h-vitrina" class="rv">Что лежит на витрине</h2>
  <figure class="f-small"><div class="ph rp"><img src="assets/img/ya-17.jpg" alt="Витрина с киш, слойками и сэндвичами" loading="lazy" style="object-position:50% 45%"></div><figcaption>Киш, слойки и сэндвичи</figcaption></figure>
  <figure class="f-tall"><div class="ph rp" data-d="120"><img src="assets/img/ya-18.jpg" alt="Эспрессо и эклер на столе из светлого дерева" loading="lazy" style="object-position:55% 60%"></div><figcaption>Эспрессо и эклер</figcaption></figure>
  <p class="lede rv">Пирожные, эклеры, киш и сэндвичи. Кто-то берёт эклер к утреннему кофе, кто-то приходит вечером за десертом, а коробку эклеров или торт можно заказать заранее.</p>
</section>

<section class="order" id="zakaz" aria-labelledby="h-zakaz">
  <h2 id="h-zakaz" class="rv">Напишите заказ на доске</h2>
  <p class="sub rv" data-d="90">Выберите, что нужно, и внизу появится готовая записка. Скопируйте её и отправьте в кондитерскую.</p>
  <div class="order-grid">
    <div class="board" id="board">
      <div class="row">
        <div class="lab" id="l-what">Что</div>
        <div class="opts big" role="group" aria-labelledby="l-what">
          <button type="button" class="word" data-type="eclairs" aria-pressed="false">Набор эклеров</button>
          <button type="button" class="word" data-type="cake" aria-pressed="false">Торт</button>
        </div>
      </div>

      <div class="row" id="eclairs-row" hidden>
        <div class="lab">Вкусы</div>
        <div>
          <div class="flavors" id="flavors"></div>
          <p class="total" id="total">Выбрано: 0</p>
        </div>
      </div>

      <div class="row" id="cake-row" hidden>
        <div class="lab">Гостей</div>
        <div class="step" role="group" aria-label="Количество гостей">
          <button type="button" data-g="-1" aria-label="Меньше гостей">−</button>
          <output id="guests" aria-live="polite">8</output>
          <button type="button" data-g="1" aria-label="Больше гостей">+</button>
        </div>
      </div>

      <div class="row">
        <div class="lab" id="l-occ">Повод</div>
        <div class="opts" role="group" aria-labelledby="l-occ" id="occ"></div>
      </div>
      <div class="row">
        <div class="lab" id="l-pt">Точка</div>
        <div class="opts" role="group" aria-labelledby="l-pt" id="pt"></div>
      </div>
      <div class="row">
        <label class="lab" for="date">Когда</label>
        <input class="field" type="date" id="date">
      </div>
      <div class="row">
        <label class="lab" for="name">Имя</label>
        <input class="field" type="text" id="name" autocomplete="given-name" placeholder="Как к вам обращаться">
      </div>
      <div class="row">
        <label class="lab" for="wish">Пожелания</label>
        <textarea class="field" id="wish" maxlength="300" placeholder="Надпись, начинка, аллергии"></textarea>
      </div>
    </div>

    <figure class="side">
      <div class="ph"><img id="side-img" style="object-position:50% 90%" src="assets/img/ya-31.jpg" alt="Эклеры из Bodrero в коробке"></div>
      <figcaption id="side-cap">Эклеры в коробке</figcaption>
    </figure>

    <div class="note" id="note">
      <span class="tag" id="tag">Записка заказа</span>
      <pre id="text">Выберите, что заказываем, и точку. Здесь появится текст заявки.</pre>
      <p class="hint" id="status" role="status"></p>
      <div class="acts">
        <button type="button" class="btn" id="copy" aria-disabled="true">Скопировать текст</button>
        <a class="btn quiet" href="https://vk.me/konditer_francois" target="_blank" rel="noopener">ВКонтакте</a>
        <a class="btn quiet" href="tel:+74951991998">Позвонить</a>
      </div>
      <p class="hint">Сайт ничего не отправляет: вы копируете текст и отправляете его сами. Сроки и сумму подтвердит кондитерская.</p>
      <noscript><p class="hint">Без скриптов позвоните: +7 (495) 199-19-98.</p></noscript>
    </div>
  </div>
</section>

<section class="shutter" aria-labelledby="h-int">
  <h2 id="h-int" class="sr">Интерьер Bodrero</h2>
  <div class="ph">
    <picture>
      <source media="(max-width:860px)" srcset="assets/img/ya-25.jpg">
      <img src="assets/img/ya-12.jpg" alt="Интерьер Bodrero: деревянная стойка со скалками и меловые доски" loading="lazy">
    </picture>
  </div>
  <div class="band"><p class="rv">Дерево, меловые доски и стойка из скалок. Приходите выбирать глазами.</p></div>
</section>

<section class="streets" id="ulitsy" aria-labelledby="h-ul">
  <h2 id="h-ul" class="rv">Четыре улицы</h2>

  <article class="st">
    <div class="rv">
      <h3>Маросейка</h3>
      <address>ул. Маросейка, 10/1, стр. 1</address>
      <p class="metro">м. Китай-город</p>
      <div class="acts"><a class="btn" href="https://yandex.ru/maps/?text=Bodrero%20Маросейка%2010%2F1" target="_blank" rel="noopener">Маршрут</a><a class="btn quiet" href="tel:+74951991998">Позвонить</a></div>
    </div>
    <div class="ph rp"><img src="assets/img/ya-11.jpg" alt="Угловой фасад кондитерской Bodrero на Маросейке" loading="lazy"></div>
  </article>

  <article class="st">
    <div class="rv">
      <h3>Петровка</h3>
      <address>ул. Петровка, 19, стр. 1</address>
      <p class="metro">м. Трубная</p>
      <div class="acts"><a class="btn" href="https://yandex.ru/maps/?text=Bodrero%20Петровка%2019" target="_blank" rel="noopener">Маршрут</a><a class="btn quiet" href="tel:+74951991998">Позвонить</a></div>
    </div>
    <div class="ph rp"><img src="assets/img/ya-05.jpg" alt="Дверь и неоновая вывеска Bodrero на Петровке" loading="lazy"></div>
  </article>

  <article class="st">
    <div class="rv">
      <h3>Рождественка</h3>
      <address>ул. Рождественка, 5/7, стр. 2</address>
      <p class="metro">м. Кузнецкий мост</p>
      <div class="acts"><a class="btn" href="https://yandex.ru/maps/?text=Bodrero%20Рождественка%205%2F7" target="_blank" rel="noopener">Маршрут</a><a class="btn quiet" href="tel:+74951991998">Позвонить</a></div>
    </div>
    <div class="ph rp"><img src="assets/img/ya-24.jpg" alt="Фасад Bodrero с розовыми рамами и вывеской «Кондитерская»" loading="lazy"></div>
  </article>

  <article class="st">
    <div class="rv">
      <h3>Сретенка</h3>
      <address>ул. Сретенка, 9</address>
      <p class="metro">м. Сретенский бульвар</p>
      <div class="acts"><a class="btn" href="https://yandex.ru/maps/?text=Bodrero%20Сретенка%209" target="_blank" rel="noopener">Маршрут</a></div>
    </div>
    <a class="tel rv" href="tel:+74951991998">+7 (495) 199-19-98</a>
  </article>
</section>

<section class="final" aria-labelledby="h-fin">
  <div class="ph bg rp"><img src="assets/img/ya-32.jpg" alt="Белая лепная рама с рельефными круассанами на тёмной стене кафе" loading="lazy" style="object-position:50% 8%"></div>
  <div class="t">
    <h2 id="h-fin" class="rv">До встречи в Bodrero</h2>
    <a class="btn" href="#zakaz">Собрать заказ</a>
  </div>
</section>
</main>

<footer>
  <p>Фото: Яндекс Карты, гости и кафе.</p>
  <p>Демонстрационная страница. Заявки сайт не отправляет.</p>
</footer>

<script>
(function(){
  document.documentElement.className="js";
  var io=("IntersectionObserver" in window)?new IntersectionObserver(function(es){es.forEach(function(e){if(e.isIntersecting){var d=Number(e.target.dataset.d||0);setTimeout(function(){e.target.classList.add("on")},d);io.unobserve(e.target)}})},{rootMargin:"0px 0px -12% 0px"}):null;
  document.querySelectorAll(".rv,.rp").forEach(function(el){if(io)io.observe(el);else el.classList.add("on")});
  var tk=0;function sweep(){tk=0;document.querySelectorAll(".rv:not(.on),.rp:not(.on)").forEach(function(el){if(el.getBoundingClientRect().top<innerHeight*0.95)el.classList.add("on")})}
  addEventListener("scroll",function(){if(!tk)tk=requestAnimationFrame(sweep)},{passive:true});
  var FLAVORS=["Чёрный лес","Маракуйя – малина","Ваниль","Миндаль","Лаванда"];
  var OCC=["День рождения","К чаю в офис","Подарок","Праздник","Без повода"];
  var PTS=[["Маросейка","Маросейка, 10/1"],["Петровка","Петровка, 19"],["Рождественка","Рождественка, 5/7"],["Сретенка","Сретенка, 9"]];
  var $=function(i){return document.getElementById(i)};
  var s={type:"",occ:"",pt:"",qty:FLAVORS.map(function(){return 0}),guests:8};

  function chips(box,list,key,labelFn){
    list.forEach(function(it){
      var v=Array.isArray(it)?it[0]:it;
      var b=document.createElement("button");b.type="button";b.className="word";b.textContent=v;b.setAttribute("aria-pressed","false");
      b.addEventListener("click",function(){
        s[key]=(s[key]===v)?"":v;
        [].forEach.call(box.children,function(c){c.setAttribute("aria-pressed",c.textContent===s[key]?"true":"false")});
        render();
      });
      box.appendChild(b);
    });
  }
  chips($("occ"),OCC,"occ");chips($("pt"),PTS,"pt");

  var fl=$("flavors");
  FLAVORS.forEach(function(f,i){
    var d=document.createElement("div");d.className="fl";
    d.innerHTML='<span>'+f+'</span><span class="step"><button type="button" aria-label="Убрать: '+f+'">−</button><output aria-live="polite">0</output><button type="button" aria-label="Добавить: '+f+'">+</button></span>';
    var out=d.querySelector("output"),bs=d.querySelectorAll("button");
    bs[0].addEventListener("click",function(){s.qty[i]=Math.max(0,s.qty[i]-1);out.textContent=s.qty[i];render()});
    bs[1].addEventListener("click",function(){s.qty[i]=Math.min(12,s.qty[i]+1);out.textContent=s.qty[i];render()});
    fl.appendChild(d);
  });
  document.querySelectorAll(".word[data-type]").forEach(function(b){
    b.addEventListener("click",function(){
      s.type=b.dataset.type;
      document.querySelectorAll(".word[data-type]").forEach(function(x){x.setAttribute("aria-pressed",x===b?"true":"false")});
      render();
    });
  });
  document.querySelectorAll("[data-g]").forEach(function(b){
    b.addEventListener("click",function(){s.guests=Math.max(2,Math.min(40,s.guests+Number(b.dataset.g)));$("guests").textContent=s.guests;render()});
  });
  ["date","name","wish"].forEach(function(id){$(id).addEventListener("input",render)});
  var dt=$("date"),n=new Date();dt.min=n.getFullYear()+"-"+String(n.getMonth()+1).padStart(2,"0")+"-"+String(n.getDate()).padStart(2,"0");

  var ready=false,lastText="";
  function plural(n){var a=n%100,b=n%10;if(a>10&&a<15)return "гостей";if(b===1)return "гость";if(b>1&&b<5)return "гостя";return "гостей"}
  function what(){
    if(s.type==="cake")return "Торт на "+s.guests+" "+plural(s.guests);
    var parts=[],tot=0;
    FLAVORS.forEach(function(f,i){if(s.qty[i]){parts.push(f+" × "+s.qty[i]);tot+=s.qty[i]}});
    return "Набор эклеров"+(tot?": "+parts.join(", ")+" (всего "+tot+")":"");
  }
  function render(){
    var ecl=s.type==="eclairs",cake=s.type==="cake";
    $("eclairs-row").hidden=!ecl;$("cake-row").hidden=!cake;
    var tot=s.qty.reduce(function(a,b){return a+b},0);$("total").textContent="Выбрано: "+tot;
    var img=$("side-img"),cap=$("side-cap");
    var want=cake?"assets/img/ya-14.jpg":"assets/img/ya-31.jpg";
    if(img.getAttribute("src")!==want){img.style.opacity=0;setTimeout(function(){img.src=want;img.style.objectPosition=cake?"50% 35%":"50% 90%";cap.textContent=cake?"Пирожные-сердца из витрины":"Эклеры в коробке";img.alt=cake?"Красные глазированные пирожные-сердца в витрине Bodrero":"Эклеры из Bodrero в коробке";img.style.opacity=1},160)}
    var past=dt.value&&dt.value<dt.min;var ok=!!s.type&&!!s.pt&&(!ecl||tot>0)&&!past;var hint=!s.type?"Выберите, что заказываем.":(ecl&&!tot)?"Добавьте хотя бы один эклер.":!s.pt?"Выберите точку.":past?"Выберите дату не раньше сегодняшней.":"";
    var pt=PTS.filter(function(p){return p[0]===s.pt})[0];
    $("tag").textContent=pt?pt[1]:"Записка заказа";
    var text=(hint?hint+" ":"")+"Здесь появится текст заявки.";
    if(ok){
      var lines=["Здравствуйте! Хочу сделать предзаказ в Bodrero.","Что: "+what()];
      if(s.occ)lines.push("Повод: "+s.occ.toLowerCase());
      lines.push("Точка: "+pt[1]);
      if(dt.value){var d=new Date(dt.value+"T12:00:00");lines.push("Когда: "+d.toLocaleDateString("ru-RU",{weekday:"long",day:"numeric",month:"long"}))}
      var nm=$("name").value.trim();if(nm)lines.push("Имя: "+nm);
      var w=$("wish").value.trim();if(w)lines.push("Пожелания: "+w);
      lines.push("Подскажите, пожалуйста, получится ли и какая будет сумма.");
      text=lines.join("\n");
    }
    $("text").textContent=text;$("status").textContent=ok?"":"Кнопка копирования заработает, когда заявка будет готова.";
    var cp=$("copy");cp.setAttribute("aria-disabled",ok?"false":"true");
    if(ok&&!ready){var nt=$("note");nt.classList.remove("in");void nt.offsetWidth;nt.classList.add("in")}
    ready=ok;lastText=ok?text:"";
  }
  $("copy").addEventListener("click",function(e){
    if(!lastText){e.preventDefault();return}
    var b=this,done=function(){var o=b.textContent;b.textContent="Скопировано";$("status").textContent="Текст скопирован.";setTimeout(function(){b.textContent="Скопировать текст"},1800)};
    if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(lastText).then(done,function(){fallback()})}else fallback();
    function fallback(){var r=document.createRange();r.selectNodeContents($("text"));var sel=getSelection();sel.removeAllRanges();sel.addRange(r);try{document.execCommand("copy");done()}catch(x){}}
  });
  render();
})();
</script>
</body>
</html>
