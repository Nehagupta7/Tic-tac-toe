<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1, user-scalable=no">
<title>Three in a Row</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@500;600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0f0b1e;
    --panel:#171227;
    --panel-2:#1e1836;
    --line:#2c2547;
    --cyan:#48f0d1;
    --cyan-glow:rgba(72,240,209,0.55);
    --coral:#ff6f91;
    --coral-glow:rgba(255,111,145,0.55);
    --gold:#ffd166;
    --text:#f1edfb;
    --text-dim:#948da9;
  }
  *{ box-sizing:border-box; }
  @media (prefers-reduced-motion: reduce){
    *{ animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important; }
  }
  html,body{
    margin:0; padding:0; min-height:100%;
    background:var(--bg);
    color:var(--text);
    font-family:'Inter', sans-serif;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
    position:relative;
  }
  .aurora{
    position:fixed; inset:0; z-index:0; pointer-events:none; overflow:hidden;
  }
  .aurora span{
    position:absolute;
    width:46vw; height:46vw;
    border-radius:50%;
    filter:blur(90px);
    opacity:0.28;
  }
  .aurora span:nth-child(1){ background:var(--cyan); top:-15%; left:-10%; animation:drift1 22s ease-in-out infinite; }
  .aurora span:nth-child(2){ background:var(--coral); bottom:-20%; right:-10%; animation:drift2 26s ease-in-out infinite; }
  .aurora span:nth-child(3){ background:var(--gold); top:30%; right:20%; opacity:0.14; animation:drift3 30s ease-in-out infinite; }
  @keyframes drift1{ 0%,100%{ transform:translate(0,0); } 50%{ transform:translate(6vw,8vh); } }
  @keyframes drift2{ 0%,100%{ transform:translate(0,0); } 50%{ transform:translate(-7vw,-6vh); } }
  @keyframes drift3{ 0%,100%{ transform:translate(0,0) scale(1); } 50%{ transform:translate(-4vw,5vh) scale(1.1); } }

  .wrap{ position:relative; z-index:1; max-width:560px; margin:0 auto; padding:32px 18px 50px; }

  header.top{ text-align:center; margin-bottom:22px; }
  .brand{ font-family:'Outfit', sans-serif; font-weight:800; font-size:1.9rem; letter-spacing:-0.01em; }
  .brand .x{ color:var(--cyan); }
  .brand .o{ color:var(--coral); }
  .tagline{ font-size:0.82rem; color:var(--text-dim); margin-top:4px; }

  .seg-label{ font-size:0.62rem; letter-spacing:0.14em; text-transform:uppercase; color:var(--text-dim); margin:14px 0 6px; text-align:center; }
  .seg{
    display:flex; justify-content:center;
    background:var(--panel); border:1px solid var(--line);
    border-radius:12px; padding:4px; gap:2px;
  }
  .seg button{
    font-family:'Inter', sans-serif; font-size:0.8rem; font-weight:600;
    color:var(--text-dim); background:transparent; border:none;
    padding:9px 14px; border-radius:9px; cursor:pointer; flex:1;
    transition:background .15s ease, color .15s ease;
  }
  .seg button.active{ background:var(--panel-2); color:var(--text); box-shadow:inset 0 0 0 1px var(--line); }
  .seg button:hover:not(.active){ color:var(--text); }
  .seg button:focus-visible{ outline:2px solid var(--cyan); outline-offset:2px; }
  #diffSeg{ display:none; }

  /* ---- Scoreboard ---- */
  .scoreboard{
    display:grid; grid-template-columns:1fr 0.8fr 1fr;
    gap:10px; margin:18px 0;
  }
  .score-box{
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:14px;
    padding:12px;
    text-align:center;
    transition:box-shadow .2s ease;
  }
  .score-box .lbl{ font-size:0.66rem; letter-spacing:0.08em; text-transform:uppercase; color:var(--text-dim); margin-bottom:5px; }
  .score-box .val{ font-family:'Outfit', sans-serif; font-weight:800; font-size:1.7rem; }
  .score-box.x .val{ color:var(--cyan); }
  .score-box.o .val{ color:var(--coral); }
  .score-box.draw .val{ color:var(--gold); }
  .score-box.bump{ animation:scoreBump 420ms ease; }
  @keyframes scoreBump{
    0%{ transform:scale(1); }
    30%{ transform:scale(1.12); }
    100%{ transform:scale(1); }
  }
  .score-box.x.bump{ box-shadow:0 0 0 1px var(--cyan), 0 0 20px -4px var(--cyan-glow); }
  .score-box.o.bump{ box-shadow:0 0 0 1px var(--coral), 0 0 20px -4px var(--coral-glow); }
  .score-box.draw.bump{ box-shadow:0 0 0 1px var(--gold), 0 0 20px -4px rgba(255,209,102,0.55); }

  /* ---- Turn pill ---- */
  .turn-pill{
    display:flex; align-items:center; justify-content:center; gap:8px;
    font-family:'Outfit', sans-serif; font-weight:600; font-size:0.92rem;
    margin-bottom:14px; color:var(--text-dim);
  }
  .turn-pill .dot{
    width:10px; height:10px; border-radius:50%;
    background:var(--cyan);
    box-shadow:0 0 0 4px rgba(72,240,209,0.18);
    transition:background .2s ease, box-shadow .2s ease;
  }
  .turn-pill.o .dot{ background:var(--coral); box-shadow:0 0 0 4px rgba(255,111,145,0.18); }
  .turn-pill .who{ color:var(--text); }

  /* ---- Board ---- */
  .board-shell{
    position:relative;
    background:linear-gradient(160deg, rgba(30,24,54,0.75), rgba(23,18,39,0.75));
    backdrop-filter:blur(14px);
    border:1px solid var(--line);
    border-radius:22px;
    padding:16px;
    box-shadow:0 30px 60px -30px rgba(0,0,0,0.7);
  }
  .board-shell.shake{ animation:boardShake 420ms ease-in-out; }
  @keyframes boardShake{
    0%,100%{ transform:translateX(0); }
    20%{ transform:translateX(-6px) rotate(-0.4deg); }
    40%{ transform:translateX(5px) rotate(0.4deg); }
    60%{ transform:translateX(-4px); }
    80%{ transform:translateX(3px); }
  }
  .board{
    position:relative;
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    grid-template-rows:repeat(3, 1fr);
    gap:10px;
    aspect-ratio:1/1;
  }
  .cell{
    position:relative;
    background:var(--panel);
    border:1px solid var(--line);
    border-radius:16px;
    cursor:pointer;
    display:flex; align-items:center; justify-content:center;
    transition:border-color .15s ease, transform .1s ease, background .15s ease;
    opacity:0;
    transform:scale(0.7);
    animation:cellIn 320ms cubic-bezier(.2,.9,.3,1.2) forwards;
  }
  .cell:nth-child(1){ animation-delay:0ms; }
  .cell:nth-child(2){ animation-delay:30ms; }
  .cell:nth-child(3){ animation-delay:60ms; }
  .cell:nth-child(4){ animation-delay:90ms; }
  .cell:nth-child(5){ animation-delay:120ms; }
  .cell:nth-child(6){ animation-delay:150ms; }
  .cell:nth-child(7){ animation-delay:180ms; }
  .cell:nth-child(8){ animation-delay:210ms; }
  .cell:nth-child(9){ animation-delay:240ms; }
  @keyframes cellIn{
    to{ opacity:1; transform:scale(1); }
  }
  .cell:hover{ border-color:var(--line); background:var(--panel-2); }
  .cell.playable:hover{ transform:translateY(-2px); }
  .cell:active.playable{ transform:scale(0.96); }
  .cell.win-cell{ border-color:var(--gold); box-shadow:0 0 0 1px var(--gold), 0 0 22px -6px rgba(255,209,102,0.7); }

  .cell .ghost{
    position:absolute; inset:0;
    display:flex; align-items:center; justify-content:center;
    opacity:0;
    transition:opacity .12s ease;
    pointer-events:none;
  }
  .cell.playable:hover .ghost{ opacity:0.22; }
  .cell .ghost svg{ width:46%; height:46%; }

  .mark-svg{ width:56%; height:56%; overflow:visible; }
  .mark-x line{ stroke:var(--cyan); stroke-width:11; stroke-linecap:round; }
  .mark-o circle{ stroke:var(--coral); stroke-width:10; fill:none; stroke-linecap:round; }

  #winLineSvg{
    position:absolute; inset:0;
    width:100%; height:100%;
    pointer-events:none;
    z-index:5;
  }
  #winLineSvg line{
    stroke:var(--gold);
    stroke-width:7;
    stroke-linecap:round;
    filter:drop-shadow(0 0 8px var(--gold));
  }

  .confetti-layer{ position:absolute; inset:0; overflow:visible; pointer-events:none; z-index:6; }
  .confetto{
    position:absolute;
    width:8px; height:8px;
    top:50%; left:50%;
    border-radius:2px;
    animation:confettoFly 900ms cubic-bezier(.15,.75,.35,1) forwards;
  }
  @keyframes confettoFly{
    0%{ transform:translate(-50%,-50%) translate(0,0) rotate(0deg); opacity:1; }
    100%{ transform:translate(-50%,-50%) translate(var(--tx), var(--ty)) rotate(var(--rot)); opacity:0; }
  }

  /* ---- Result banner ---- */
  .result-banner{
    position:absolute;
    left:16px; right:16px; bottom:16px;
    background:rgba(15,11,30,0.92);
    border:1px solid var(--line);
    border-radius:16px;
    padding:16px;
    text-align:center;
    z-index:10;
    opacity:0;
    transform:translateY(10px);
    animation:bannerIn 260ms ease forwards;
  }
  .result-banner[hidden]{ display:none; }
  @keyframes bannerIn{ to{ opacity:1; transform:translateY(0); } }
  .result-text{ font-family:'Outfit', sans-serif; font-weight:700; font-size:1.15rem; margin-bottom:12px; }
  .result-text.x{ color:var(--cyan); }
  .result-text.o{ color:var(--coral); }
  .result-text.draw{ color:var(--gold); }

  .btn{
    font-family:'Inter', sans-serif; font-size:0.82rem; font-weight:600;
    color:var(--text); background:var(--panel-2);
    border:1px solid var(--line); padding:10px 16px;
    border-radius:10px; cursor:pointer;
    transition:border-color .15s ease, transform .1s ease;
  }
  .btn:hover{ border-color:var(--cyan); }
  .btn:active{ transform:translateY(1px); }
  .btn.primary{ background:var(--cyan); border-color:var(--cyan); color:#062421; font-weight:700; }
  .btn.primary:hover{ border-color:var(--gold); }
  .btn:focus-visible{ outline:2px solid var(--cyan); outline-offset:2px; }

  .controls-row{
    display:flex; align-items:center; justify-content:space-between;
    margin-top:16px; gap:10px; flex-wrap:wrap;
  }
  .hint{ font-size:0.72rem; color:var(--text-dim); }

  footer.note{ margin-top:24px; text-align:center; font-size:0.72rem; color:var(--text-dim); }
</style>
</head>
<body>

<div class="aurora"><span></span><span></span><span></span></div>

<div class="wrap">
  <header class="top">
    <div class="brand"><span class="x">X</span> · <span class="o">O</span> Three in a Row</div>
    <div class="tagline">First to line up three wins the round.</div>
  </header>

  <div class="seg-label">Mode</div>
  <div class="seg" id="modeSeg">
    <button data-mode="two" class="active">Two Player</button>
    <button data-mode="ai">Vs Computer</button>
  </div>

  <div id="diffSeg" class="seg" style="margin-top:8px;">
    <button data-diff="easy" class="active">Easy</button>
    <button data-diff="medium">Medium</button>
    <button data-diff="unbeatable">Unbeatable</button>
  </div>

  <div class="scoreboard">
    <div class="score-box x" id="scoreBoxX">
      <div class="lbl" id="labelX">Player X</div>
      <div class="val" id="scoreX">0</div>
    </div>
    <div class="score-box draw" id="scoreBoxDraw">
      <div class="lbl">Draws</div>
      <div class="val" id="scoreD">0</div>
    </div>
    <div class="score-box o" id="scoreBoxO">
      <div class="lbl" id="labelO">Player O</div>
      <div class="val" id="scoreO">0</div>
    </div>
  </div>

  <div class="turn-pill" id="turnPill">
    <span class="dot"></span>
    <span class="who" id="turnText">X's turn</span>
  </div>

  <div class="board-shell" id="boardShell">
    <div class="board" id="board"></div>
    <svg id="winLineSvg"><line x1="0" y1="0" x2="0" y2="0"></line></svg>
    <div class="confetti-layer" id="confettiLayer"></div>

    <div class="result-banner" id="resultBanner" hidden>
      <div class="result-text" id="resultText"></div>
      <button class="btn primary" id="nextRoundBtn">Next Round ▶</button>
    </div>
  </div>

  <div class="controls-row">
    <div class="hint" id="controlsHint">Click a square to place your mark.</div>
    <button class="btn" id="resetMatchBtn">Reset Match</button>
  </div>

  <footer class="note">Starting player alternates each round to keep things fair.</footer>
</div>

<script>
(function(){
  var boardEl = document.getElementById('board');
  var boardShell = document.getElementById('boardShell');
  var winLineSvg = document.getElementById('winLineSvg');
  var winLine = winLineSvg.querySelector('line');
  var confettiLayer = document.getElementById('confettiLayer');
  var turnPill = document.getElementById('turnPill');
  var turnText = document.getElementById('turnText');
  var resultBanner = document.getElementById('resultBanner');
  var resultText = document.getElementById('resultText');
  var labelX = document.getElementById('labelX');
  var labelO = document.getElementById('labelO');
  var scoreXEl = document.getElementById('scoreX');
  var scoreOEl = document.getElementById('scoreO');
  var scoreDEl = document.getElementById('scoreD');
  var scoreBoxX = document.getElementById('scoreBoxX');
  var scoreBoxO = document.getElementById('scoreBoxO');
  var scoreBoxDraw = document.getElementById('scoreBoxDraw');

  var WINS = [
    [0,1,2],[3,4,5],[6,7,8],
    [0,3,6],[1,4,7],[2,5,8],
    [0,4,8],[2,4,6]
  ];

  var mode = 'two';
  var difficulty = 'easy';
  var board = Array(9).fill(null);
  var current = 'X';
  var starter = 'X';
  var roundOver = false;
  var scores = { X:0, O:0, D:0 };
  var aiThinking = false;

  function xLabel(){ return mode === 'ai' ? 'You (X)' : 'Player X'; }
  function oLabel(){ return mode === 'ai' ? 'Computer' : 'Player O'; }

  function buildBoard(){
    boardEl.innerHTML = '';
    for (var i=0;i<9;i++){
      var cell = document.createElement('div');
      cell.className = 'cell playable';
      cell.dataset.index = i;
      cell.innerHTML = '<div class="ghost" data-ghost></div>';
      cell.addEventListener('click', onCellClick);
      boardEl.appendChild(cell);
    }
    updateGhosts();
  }

  function updateGhosts(){
    var ghostSvg = current === 'X' ? xSvgMarkup(false) : oSvgMarkup(false);
    boardEl.querySelectorAll('[data-ghost]').forEach(function(g){
      g.innerHTML = ghostSvg;
    });
  }

  function xSvgMarkup(animate){
    var cls = animate ? 'mark-svg mark-x drawing' : 'mark-svg mark-x';
    return '<svg class="'+cls+'" viewBox="0 0 100 100"><line x1="22" y1="22" x2="78" y2="78"></line><line x1="78" y1="22" x2="22" y2="78"></line></svg>';
  }
  function oSvgMarkup(animate){
    var cls = animate ? 'mark-svg mark-o drawing' : 'mark-svg mark-o';
    return '<svg class="'+cls+'" viewBox="0 0 100 100"><circle cx="50" cy="50" r="32"></circle></svg>';
  }

  function labels(){
    labelX.textContent = xLabel();
    labelO.textContent = oLabel();
  }

  function setTurnUI(){
    turnPill.classList.toggle('o', current === 'O');
    if (mode === 'ai' && current === 'O'){
      turnText.textContent = 'Computer thinking…';
    } else if (mode === 'ai' && current === 'X'){
      turnText.textContent = 'Your turn';
    } else {
      turnText.textContent = current + '\u2019s turn';
    }
  }

  function checkResult(b){
    for (var i=0;i<WINS.length;i++){
      var line = WINS[i];
      var a = b[line[0]], c = b[line[1]], d = b[line[2]];
      if (a && a === c && a === d){
        return { winner:a, line:line };
      }
    }
    if (b.every(function(v){ return v; })) return { winner:'draw' };
    return null;
  }

  function onCellClick(e){
    if (roundOver || aiThinking) return;
    if (mode === 'ai' && current !== 'X') return;
    var idx = parseInt(e.currentTarget.dataset.index, 10);
    if (board[idx]) return;
    placeMark(idx, current);
  }

  function placeMark(idx, player){
    board[idx] = player;
    var cell = boardEl.children[idx];
    cell.classList.remove('playable');
    var ghost = cell.querySelector('[data-ghost]');
    if (ghost) ghost.remove();
    cell.insertAdjacentHTML('beforeend', player === 'X' ? xSvgMarkup(true) : oSvgMarkup(true));
    var svg = cell.querySelector('.mark-svg');
    prepareDraw(svg);

    var result = checkResult(board);
    if (result){
      roundOver = true;
      boardEl.querySelectorAll('.cell').forEach(function(c){ c.classList.remove('playable'); });
      setTimeout(function(){ handleRoundEnd(result); }, 260);
      return;
    }

    current = current === 'X' ? 'O' : 'X';
    setTurnUI();
    updateGhosts();

    if (mode === 'ai' && current === 'O' && !roundOver){
      aiThinking = true;
      setTimeout(computerMove, 450);
    }
  }

  function prepareDraw(svg){
    if (!svg) return;
    if (svg.classList.contains('mark-x')){
      svg.querySelectorAll('line').forEach(function(line){
        var len = 80; // approx diagonal length for the 22..78 segment
        line.style.strokeDasharray = len;
        line.style.strokeDashoffset = len;
        line.style.transition = 'stroke-dashoffset 260ms ease-out';
      });
      requestAnimationFrame(function(){
        requestAnimationFrame(function(){
          svg.querySelectorAll('line').forEach(function(line, i){
            setTimeout(function(){ line.style.strokeDashoffset = '0'; }, i * 90);
          });
        });
      });
    } else {
      var circle = svg.querySelector('circle');
      var len = 202; // ~ circumference of r=32 circle
      circle.style.strokeDasharray = len;
      circle.style.strokeDashoffset = len;
      circle.style.transition = 'stroke-dashoffset 320ms ease-out';
      requestAnimationFrame(function(){
        requestAnimationFrame(function(){
          circle.style.strokeDashoffset = '0';
        });
      });
    }
  }

  function handleRoundEnd(result){
    if (result.winner === 'draw'){
      scores.D++;
      bumpScore(scoreBoxDraw, scoreDEl, scores.D);
      shakeBoard();
      resultText.className = 'result-text draw';
      resultText.textContent = 'It\u2019s a draw!';
    } else {
      scores[result.winner]++;
      bumpScore(result.winner === 'X' ? scoreBoxX : scoreBoxO, result.winner === 'X' ? scoreXEl : scoreOEl, scores[result.winner]);
      drawWinLine(result.line);
      markWinCells(result.line);
      launchConfetti(result.winner);
      resultText.className = 'result-text ' + (result.winner === 'X' ? 'x' : 'o');
      var who = result.winner === 'X' ? xLabel() : oLabel();
      resultText.textContent = who + ' wins!';
    }
    turnText.textContent = 'Round over';
    resultBanner.hidden = false;
  }

  function markWinCells(line){
    line.forEach(function(i){ boardEl.children[i].classList.add('win-cell'); });
  }

  function drawWinLine(line){
    var boardRect = boardEl.getBoundingClientRect();
    var a = boardEl.children[line[0]].getBoundingClientRect();
    var c = boardEl.children[line[2]].getBoundingClientRect();
    var x1 = a.left - boardRect.left + a.width/2;
    var y1 = a.top - boardRect.top + a.height/2;
    var x2 = c.left - boardRect.left + c.width/2;
    var y2 = c.top - boardRect.top + c.height/2;

    winLineSvg.setAttribute('width', boardRect.width);
    winLineSvg.setAttribute('height', boardRect.height);
    winLine.setAttribute('x1', x1);
    winLine.setAttribute('y1', y1);
    winLine.setAttribute('x2', x1);
    winLine.setAttribute('y2', y1);

    var len = Math.hypot(x2-x1, y2-y1);
    winLine.style.strokeDasharray = len;
    winLine.style.strokeDashoffset = len;
    winLine.style.transition = 'stroke-dashoffset 280ms ease-out';

    requestAnimationFrame(function(){
      requestAnimationFrame(function(){
        winLine.setAttribute('x2', x2);
        winLine.setAttribute('y2', y2);
        winLine.style.strokeDashoffset = '0';
      });
    });
  }

  function launchConfetti(winner){
    var colors = winner === 'X' ? ['#48f0d1', '#8ff5e1', '#ffd166'] : ['#ff6f91', '#ffb0c3', '#ffd166'];
    for (var i=0;i<28;i++){
      var p = document.createElement('div');
      p.className = 'confetto';
      var angle = Math.random() * Math.PI * 2;
      var dist = 60 + Math.random() * 90;
      var tx = Math.cos(angle) * dist;
      var ty = Math.sin(angle) * dist - 20;
      p.style.setProperty('--tx', tx + 'px');
      p.style.setProperty('--ty', ty + 'px');
      p.style.setProperty('--rot', (Math.random()*360) + 'deg');
      p.style.background = colors[Math.floor(Math.random()*colors.length)];
      p.style.borderRadius = Math.random() > 0.5 ? '2px' : '50%';
      p.style.animationDelay = (Math.random()*80) + 'ms';
      confettiLayer.appendChild(p);
      (function(el){ setTimeout(function(){ if (el.parentNode) el.remove(); }, 1100); })(p);
    }
  }

  function bumpScore(box, valEl, value){
    valEl.textContent = value;
    box.classList.remove('bump');
    void box.offsetWidth;
    box.classList.add('bump');
    setTimeout(function(){ box.classList.remove('bump'); }, 440);
  }

  function shakeBoard(){
    boardShell.classList.remove('shake');
    void boardShell.offsetWidth;
    boardShell.classList.add('shake');
  }

  /* ---------------- Computer AI ---------------- */

  function emptyIndices(b){
    var out = [];
    b.forEach(function(v,i){ if(!v) out.push(i); });
    return out;
  }

  function minimax(b, player){
    var result = checkResult(b);
    if (result){
      if (result.winner === 'O') return { score: 1 };
      if (result.winner === 'X') return { score: -1 };
      return { score: 0 };
    }
    var moves = emptyIndices(b).map(function(i){
      var nb = b.slice();
      nb[i] = player;
      var r = minimax(nb, player === 'O' ? 'X' : 'O');
      return { index:i, score:r.score };
    });
    if (player === 'O'){
      return moves.reduce(function(best, m){ return m.score > best.score ? m : best; });
    }
    return moves.reduce(function(best, m){ return m.score < best.score ? m : best; });
  }

  function computerMove(){
    if (roundOver){ aiThinking = false; return; }
    var empties = emptyIndices(board);
    var idx;
    var useSmart = difficulty === 'unbeatable' || (difficulty === 'medium' && Math.random() < 0.6);
    if (useSmart){
      idx = minimax(board.slice(), 'O').index;
    } else {
      idx = empties[Math.floor(Math.random() * empties.length)];
    }
    aiThinking = false;
    placeMark(idx, 'O');
  }

  /* ---------------- Round / match flow ---------------- */

  function newRound(){
    board = Array(9).fill(null);
    roundOver = false;
    starter = starter === 'X' ? 'O' : 'X';
    current = starter;
    resultBanner.hidden = true;
    winLine.style.transition = 'none';
    winLine.setAttribute('x1',0); winLine.setAttribute('y1',0);
    winLine.setAttribute('x2',0); winLine.setAttribute('y2',0);
    confettiLayer.innerHTML = '';
    buildBoard();
    setTurnUI();

    if (mode === 'ai' && current === 'O'){
      aiThinking = true;
      setTimeout(computerMove, 500);
    }
  }

  function resetMatch(){
    scores = { X:0, O:0, D:0 };
    scoreXEl.textContent = '0';
    scoreOEl.textContent = '0';
    scoreDEl.textContent = '0';
    starter = 'X';
    newRound();
  }

  document.getElementById('nextRoundBtn').addEventListener('click', newRound);
  document.getElementById('resetMatchBtn').addEventListener('click', resetMatch);

  document.getElementById('modeSeg').addEventListener('click', function(e){
    var btn = e.target.closest('button');
    if (!btn) return;
    mode = btn.dataset.mode;
    Array.from(this.children).forEach(function(b){ b.classList.toggle('active', b === btn); });
    document.getElementById('diffSeg').style.display = mode === 'ai' ? 'flex' : 'none';
    document.getElementById('controlsHint').textContent = mode === 'ai'
      ? 'You\u2019re X. Click a square to place your mark.'
      : 'Click a square to place your mark.';
    labels();
    resetMatch();
  });

  document.getElementById('diffSeg').addEventListener('click', function(e){
    var btn = e.target.closest('button');
    if (!btn) return;
    difficulty = btn.dataset.diff;
    Array.from(this.children).forEach(function(b){ b.classList.toggle('active', b === btn); });
    resetMatch();
  });

  labels();
  newRound();
})();
</script>
</body>
</html>
