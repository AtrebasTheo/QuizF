<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Quiz</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap');

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg:      #0f1117;
      --surface: #1a1d27;
      --border:  #2a2e3f;
      --text:    #e8eaf0;
      --muted:   #7880a0;
      --accent:  #6c63ff;
      --correct: #22c97a;
      --wrong:   #f04a6a;
      --radius:  14px;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 24px;
    }

    /* ── Lang switcher ── */
    .lang-bar {
      width: 100%;
      max-width: 640px;
      display: flex;
      justify-content: flex-end;
      gap: 8px;
      margin-bottom: 16px;
    }
    .lang-btn {
      background: var(--surface);
      border: 1.5px solid var(--border);
      color: var(--muted);
      font-family: inherit;
      font-size: 12px;
      font-weight: 700;
      letter-spacing: .06em;
      padding: 6px 14px;
      border-radius: 99px;
      cursor: pointer;
      transition: border-color .15s, color .15s;
    }
    .lang-btn.active {
      border-color: var(--accent);
      color: var(--accent);
    }
    .lang-btn:hover:not(.active) {
      border-color: var(--muted);
      color: var(--text);
    }

    /* ── Progress bar ── */
    .progress-wrap {
      width: 100%;
      max-width: 640px;
      margin-bottom: 28px;
    }
    .progress-meta {
      display: flex;
      justify-content: space-between;
      font-size: 13px;
      color: var(--muted);
      margin-bottom: 8px;
      font-weight: 600;
      letter-spacing: .04em;
      text-transform: uppercase;
    }
    .progress-track {
      height: 6px;
      background: var(--border);
      border-radius: 99px;
      overflow: hidden;
    }
    .progress-fill {
      height: 100%;
      background: var(--accent);
      border-radius: 99px;
      transition: width .4s cubic-bezier(.4,0,.2,1);
    }

    /* ── Card ── */
    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 40px 44px;
      width: 100%;
      max-width: 640px;
    }

    .question-label {
      font-size: 11px;
      font-weight: 700;
      letter-spacing: .12em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 14px;
    }
    .question-text {
      font-size: 22px;
      font-weight: 700;
      line-height: 1.4;
      margin-bottom: 32px;
    }

    /* ── Answers ── */
    .answers { display: flex; flex-direction: column; gap: 12px; }

    .answer-btn {
      background: var(--bg);
      border: 1.5px solid var(--border);
      border-radius: var(--radius);
      color: var(--text);
      font-family: inherit;
      font-size: 15px;
      font-weight: 600;
      padding: 16px 20px;
      text-align: left;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 14px;
      transition: border-color .15s, background .15s, transform .1s;
      position: relative;
      overflow: hidden;
    }
    .answer-btn:hover:not(:disabled) { border-color: var(--accent); background: #1f2236; }
    .answer-btn:active:not(:disabled) { transform: scale(.98); }

    .answer-key {
      width: 30px; height: 30px;
      border-radius: 8px;
      background: var(--border);
      display: grid; place-items: center;
      font-size: 12px; font-weight: 800;
      flex-shrink: 0;
      transition: background .2s;
    }

    .answer-btn.correct { border-color: var(--correct); background: rgba(34,201,122,.08); animation: pulse-correct .35s ease; }
    .answer-btn.correct .answer-key { background: var(--correct); color: #fff; }
    .answer-btn.wrong   { border-color: var(--wrong);   background: rgba(240,74,106,.08);  animation: pulse-wrong   .35s ease; }
    .answer-btn.wrong   .answer-key { background: var(--wrong);   color: #fff; }
    .answer-btn:disabled { cursor: default; }

    @keyframes pulse-correct {
      0%   { transform: scale(1); }
      40%  { transform: scale(1.025); }
      100% { transform: scale(1); }
    }
    @keyframes pulse-wrong {
      0%,100% { transform: translateX(0); }
      25%     { transform: translateX(-6px); }
      75%     { transform: translateX(6px); }
    }

    /* ── Feedback ── */
    .feedback { margin-top: 20px; padding: 14px 18px; border-radius: 10px; font-size: 14px; font-weight: 600; display: none; }
    .feedback.show    { display: block; }
    .feedback.correct { background: rgba(34,201,122,.1); color: var(--correct); border: 1px solid rgba(34,201,122,.25); }
    .feedback.wrong   { background: rgba(240,74,106,.1);  color: var(--wrong);   border: 1px solid rgba(240,74,106,.25); }

    /* ── Next btn ── */
    .next-btn {
      margin-top: 28px; width: 100%; padding: 16px;
      background: var(--accent); color: #fff; border: none;
      border-radius: var(--radius); font-family: inherit;
      font-size: 15px; font-weight: 700; letter-spacing: .02em;
      cursor: pointer; display: none;
      transition: filter .15s, transform .1s;
    }
    .next-btn.show  { display: block; }
    .next-btn:hover { filter: brightness(1.1); }
    .next-btn:active { transform: scale(.98); }

    /* ── Result ── */
    .result { text-align: center; display: none; }
    .result.show { display: block; }
    .result-icon  { font-size: 64px; margin-bottom: 16px; }
    .result-title { font-size: 28px; font-weight: 900; margin-bottom: 10px; }
    .result-sub   { color: var(--muted); font-size: 15px; margin-bottom: 32px; }
    .score-badge  {
      display: inline-block; background: var(--accent); color: #fff;
      font-size: 36px; font-weight: 900; padding: 18px 40px;
      border-radius: var(--radius); margin-bottom: 0;
    }
    .result-quote {
      font-size: 15px; color: var(--muted); font-style: italic;
      margin: 20px 0 28px; line-height: 1.5;
    }
    .restart-btn {
      padding: 16px 40px; background: transparent; color: var(--accent);
      border: 2px solid var(--accent); border-radius: var(--radius);
      font-family: inherit; font-size: 15px; font-weight: 700;
      cursor: pointer; transition: background .15s;
    }
    .restart-btn:hover { background: rgba(108,99,255,.12); }

    @media (max-width: 480px) {
      .card { padding: 28px 20px; }
      .question-text { font-size: 18px; }
    }
  </style>
</head>
<body>

<div class="lang-bar">
  <button class="lang-btn" id="btn-en" onclick="setLang('en')">EN</button>
  <button class="lang-btn" id="btn-de" onclick="setLang('de')">DE</button>
</div>

<div class="progress-wrap">
  <div class="progress-meta">
    <span id="q-label"></span>
    <span id="score-live"></span>
  </div>
  <div class="progress-track">
    <div class="progress-fill" id="progress-fill" style="width:0%"></div>
  </div>
</div>

<div class="card">
  <div id="quiz-screen">
    <div class="question-label" id="q-counter"></div>
    <div class="question-text" id="q-text"></div>
    <div class="answers" id="answers"></div>
    <div class="feedback" id="feedback"></div>
    <button class="next-btn" id="next-btn"></button>
  </div>

  <div class="result" id="result-screen">
    <div class="result-icon"  id="result-icon"></div>
    <div class="result-title" id="result-title"></div>
    <div class="result-sub"   id="result-sub"></div>
    <div class="score-badge"  id="score-badge"></div>
    <div class="result-quote" id="result-quote"></div>
    <button class="restart-btn" id="restart-btn" onclick="restart()"></button>
  </div>
</div>

<script>
  // ─────────────────────────────────────────────────────────────
  //  TRANSLATIONS
  // ─────────────────────────────────────────────────────────────
  const i18n = {
    en: {
      questionOf:   (i, t) => 'Question ' + i + ' of ' + t,
      questionLabel:(i)    => 'Question ' + i,
      points:       (n)    => n + ' Point' + (n !== 1 ? 's' : ''),
      next:               'Next →',
      showResult:         'Show Result',
      correct:      (exp) => '✓ Correct! ' + exp,
      wrong:        (exp) => '✗ Wrong. ' + exp,
      resultSub:    (s,t) => 'You answered ' + s + ' out of ' + t + ' questions correctly.',
      restart:            'Play Again',
      results: {
        perfect:  { title: 'Perfect!',       quote: 'You\'re a real Finn expert—absolutely flawless! Maybe you\'re even Finn himself!??' },
        great:    { title: 'Well done!',      quote: 'Great job! With a little more Finn stalking, it\'ll get even better.' },
        okay:     { title: 'Not bad!',        quote: 'You already know quite a bit—but there\'s still room for improvement. Get even more out of Finn.' },
        poor:     { title: 'Keep practising!',quote: 'You can do even better than that! Grab a listening device and hang out at Finn\'s window.' }
      }
    },
    de: {
      questionOf:   (i, t) => 'Frage ' + i + ' von ' + t,
      questionLabel:(i)    => 'Frage ' + i,
      points:       (n)    => n + ' Punkt' + (n !== 1 ? 'e' : ''),
      next:               'Weiter →',
      showResult:         'Ergebnis anzeigen',
      correct:      (exp) => '✓ Richtig! ' + exp,
      wrong:        (exp) => '✗ Falsch. ' + exp,
      resultSub:    (s,t) => 'Du hast ' + s + ' von ' + t + ' Fragen richtig beantwortet.',
      restart:            'Nochmal spielen',
      results: {
        perfect:  { title: 'Perfekt!',        quote: 'Du bist ein wahrer Finn-Experte – absolut makellos! Vieleicht bist du ja sogar Finn persönlich!??' },
        great:    { title: 'Gut gemacht!',    quote: 'Starke Leistung! Mit ein bisschen mehr Finn Stalking wird das noch besser.' },
        okay:     { title: 'Nicht schlecht!', quote: 'Du weißt schon einiges – aber da ist noch Luft nach oben. Quetsche Finn noch mehr aus.' },
        poor:     { title: 'Weiter üben!',    quote: 'Du kannst das noch viel besser! Schnapp dir ein Abhörgerät und lungere vor Finn\'s Fenster' }
      }
    }
  };

  // ─────────────────────────────────────────────────────────────
  //  QUESTIONS  (add/edit here)
  //  correct: zero-based index of the right answer
  // ─────────────────────────────────────────────────────────────
  const questions = {
    en: [
      {
        text: 'What is Finn\'s last name?',
        answers: ['Gianjogologocomolo', 'Sperle', 'Binchiling', 'Frankfurt'],
        correct: 0,
        explanation: 'Finn\'s family tree shows a connection to famous inventor Luigi Gianjogologocomolo'
      },
      {
        text: 'How many children does Finn have?',
        answers: ['0', '1', '2', 'More than 10'],
        correct: 0,
        explanation: 'Finn will probably have a nice family in the future, but as of now, he is childless'
      },
      { text: 'Where does Finn live?',
        answers: ['Duisburg', 'Wasserburger Landstraße 81b', 'South Sudan', 'Loch Ness'],
        correct: 1,
        explanation: 'I know where you live'
      },
      {
        text: 'Which plant sounds similar to Finn\'s GF?',
        answers: [ 'Bread','Vanilla', 'Lavender', 'Orchid'],
        correct: 1,
        explanation: 'No explanation'
      },
      {
        text: 'Why is Finn so cute?',
        answers: ['He\'s not', 'disposition', 'That is unknown', 'He learned it in elementary school', 'He imitates puppies'],
        correct: 2,
        explanation: 'No one really knows where he got his inexplicable charm'
      }
    ],
    de: [
      {
        text: 'Was ist Finn\'s Nachname?',
        answers: ['Gianjogologocomolo', 'Sperle', 'Binchiling', 'Frankfurt'],
        correct: 0,
        explanation: 'Finns Stammbaum zeigt eine Verbindung zu dem berühmten Erfinder Luigi Gianjogologocomolo'
      },
      {
        text: 'Wie viele Kinder hat Finn?',
        answers: ['0', '1', '2', 'Mehr als 10'],
        correct: 0,
        explanation: 'Finn wird sicher irgendwann eine nette Familie haben, aber momentan ist er kinderlos'
      },
      { text: 'Wo wohnt Finn?',
        answers: ['Duisburg', 'Wasserburger Landstraße 81b', 'Südsudan', 'Lochness'],
        correct: 1,
        explanation: 'Ich weiß wo du wohnst'
      },
      {
        text: 'Welche Pflanze hört sich ähnlich an wie Finn\'s GF?',
        answers: ['Brot', 'Vanille', 'Lavendel', 'Orchidee'],
        correct: 1,
        explanation: 'Keine Erklärung'
      },
      {
        text: 'Warum ist Finn so süss?',
        answers: ['Ist er nicht', 'Veranlagung', 'Das ist unbekannt', 'In der Grundschule erlernt', 'Er imitiert Hundewelpen'],
        correct: 2,
        explanation: 'Niemand weiß wirklich woher er seinen unerklärlichen Charm hat'
      }
    ]
  };

  // ─────────────────────────────────────────────────────────────
  //  STATE
  // ─────────────────────────────────────────────────────────────
  const KEYS = ['A','B','C','D','E','F'];
  let lang     = 'en';
  let current  = 0;
  let score    = 0;
  let answered = false;
  let inResult = false;

  // ─────────────────────────────────────────────────────────────
  //  LANGUAGE DETECTION & SWITCH
  // ─────────────────────────────────────────────────────────────
  function detectLang() {
    const pref = (navigator.language || navigator.userLanguage || 'en').toLowerCase();
    return pref.startsWith('de') ? 'de' : 'en';
  }

  function setLang(newLang) {
    lang = newLang;
    document.getElementById('btn-en').classList.toggle('active', lang === 'en');
    document.getElementById('btn-de').classList.toggle('active', lang === 'de');
    document.documentElement.lang = lang;

    if (inResult) {
      // re-render result screen in new language (keep score)
      showResult(true);
    } else {
      // re-render current question in new language (keep answered state)
      renderQuestion(current);
    }
    // update live score label
    document.getElementById('score-live').textContent = i18n[lang].points(score);
  }

  // ─────────────────────────────────────────────────────────────
  //  RENDER
  // ─────────────────────────────────────────────────────────────
  function renderQuestion(index) {
    const t   = i18n[lang];
    const qs  = questions[lang];
    const q   = qs[index];
    const total = qs.length;

    document.getElementById('q-label').textContent   = t.questionOf(index + 1, total);
    document.getElementById('q-counter').textContent = t.questionLabel(index + 1);
    document.getElementById('q-text').textContent    = q.text;
    document.getElementById('progress-fill').style.width = ((index / total) * 100) + '%';

    const nb = document.getElementById('next-btn');
    nb.textContent = index < total - 1 ? t.next : t.showResult;

    const container = document.getElementById('answers');
    container.innerHTML = '';
    q.answers.forEach((ans, i) => {
      const btn = document.createElement('button');
      btn.className = 'answer-btn';
      btn.innerHTML = '<span class="answer-key">' + KEYS[i] + '</span><span>' + ans + '</span>';
      btn.addEventListener('click', () => handleAnswer(i));
      container.appendChild(btn);
    });

    // re-apply answered state if switching lang mid-question
    if (answered) {
      const btns = container.querySelectorAll('.answer-btn');
      btns.forEach(b => b.disabled = true);
      btns[q.correct].classList.add('correct');
      // we stored the last chosen index globally
      if (lastChosen !== null && lastChosen !== q.correct) {
        btns[lastChosen].classList.add('wrong');
      }
      const fb = document.getElementById('feedback');
      fb.className = 'feedback ' + (lastChosen === q.correct ? 'correct' : 'wrong') + ' show';
      fb.textContent = lastChosen === q.correct ? t.correct(q.explanation) : t.wrong(q.explanation);
      nb.classList.add('show');
    }
  }

  function load(index) {
    answered  = false;
    lastChosen = null;
    inResult  = false;
    document.getElementById('feedback').className = 'feedback';
    document.getElementById('feedback').textContent = '';
    document.getElementById('next-btn').className = 'next-btn';
    document.getElementById('score-live').textContent = i18n[lang].points(score);
    renderQuestion(index);
  }

  // ─────────────────────────────────────────────────────────────
  //  INTERACTION
  // ─────────────────────────────────────────────────────────────
  let lastChosen = null;

  function handleAnswer(chosen) {
    if (answered) return;
    answered   = true;
    lastChosen = chosen;

    const q    = questions[lang][current];
    const t    = i18n[lang];
    const btns = document.querySelectorAll('.answer-btn');
    btns.forEach(b => b.disabled = true);

    const fb = document.getElementById('feedback');

    if (chosen === q.correct) {
      score++;
      btns[chosen].classList.add('correct');
      fb.textContent = t.correct(q.explanation);
      fb.className   = 'feedback correct show';
    } else {
      btns[chosen].classList.add('wrong');
      btns[q.correct].classList.add('correct');
      fb.textContent = t.wrong(q.explanation);
      fb.className   = 'feedback wrong show';
    }

    document.getElementById('score-live').textContent = i18n[lang].points(score);
    document.getElementById('next-btn').classList.add('show');
  }

  document.getElementById('next-btn').addEventListener('click', () => {
    current++;
    if (current < questions[lang].length) {
      load(current);
    } else {
      showResult(false);
    }
  });

  // ─────────────────────────────────────────────────────────────
  //  RESULT
  // ─────────────────────────────────────────────────────────────
  function showResult(langSwitch) {
    inResult = true;
    if (!langSwitch) {
      document.getElementById('quiz-screen').style.display = 'none';
      document.getElementById('progress-fill').style.width = '100%';
    }

    const t     = i18n[lang];
    const total = questions[lang].length;
    const pct   = Math.round((score / total) * 100);

    let icon, bucket;
    if (pct === 100)     { icon = '🏆'; bucket = 'perfect'; }
    else if (pct >= 67)  { icon = '🎉'; bucket = 'great';   }
    else if (pct >= 34)  { icon = '🤔'; bucket = 'okay';    }
    else                 { icon = '📚'; bucket = 'poor';     }

    document.getElementById('result-icon').textContent  = icon;
    document.getElementById('result-title').textContent = t.results[bucket].title;
    document.getElementById('result-sub').textContent   = t.resultSub(score, total);
    document.getElementById('score-badge').textContent  = score + ' / ' + total;
    document.getElementById('result-quote').textContent = t.results[bucket].quote;
    document.getElementById('restart-btn').textContent  = t.restart;
    document.getElementById('result-screen').className  = 'result show';
  }

  function restart() {
    current = 0; score = 0; inResult = false;
    document.getElementById('result-screen').className = 'result';
    document.getElementById('quiz-screen').style.display = 'block';
    load(0);
  }

  // ─────────────────────────────────────────────────────────────
  //  INIT
  // ─────────────────────────────────────────────────────────────
  lang = detectLang();
  document.getElementById('btn-en').classList.toggle('active', lang === 'en');
  document.getElementById('btn-de').classList.toggle('active', lang === 'de');
  document.documentElement.lang = lang;
  load(0);
</script>
</body>
</html>
