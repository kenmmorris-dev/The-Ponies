<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Ponies</title>
<link href="https://fonts.googleapis.com/css2?family=Rye&family=Nunito:wght@700;900&display=swap" rel="stylesheet">
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'Nunito', sans-serif;
  background: linear-gradient(160deg, #1a5c2a 0%, #3aaa55 60%, #87ceeb 100%);
  min-height: 100vh;
}

/* ── SCREENS ── */
.screen {
  display: none;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  padding: 24px 16px;
}
.screen.active { display: flex; }

/* ── TITLE ── */
.title {
  font-family: 'Rye', cursive;
  font-size: 2.8rem;
  color: #f5c842;
  text-shadow: 3px 3px 0 #5c3d11;
  text-align: center;
  margin-bottom: 6px;
}
.subtitle {
  color: #c8f5d0;
  font-size: 0.9rem;
  font-weight: 700;
  letter-spacing: 2px;
  margin-bottom: 24px;
  text-align: center;
}

/* ── CARD ── */
.card {
  background: #fdf6e3;
  border-radius: 20px;
  padding: 24px;
  width: 100%;
  max-width: 420px;
  box-shadow: 0 8px 32px rgba(0,0,0,0.3);
  border: 3px solid #f5c842;
}
.card h2 {
  font-family: 'Rye', cursive;
  color: #1a5c2a;
  font-size: 1.1rem;
  margin-bottom: 16px;
  text-align: center;
}

/* ── FORM ── */
.row {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 12px;
}
.row label {
  font-weight: 900;
  color: #5c3d11;
  font-size: 0.9rem;
  white-space: nowrap;
  min-width: 90px;
}
.row input {
  flex: 1;
  padding: 10px 12px;
  border-radius: 10px;
  border: 2px solid #c8b89a;
  font-family: 'Nunito', sans-serif;
  font-size: 1rem;
  font-weight: 700;
  color: #5c3d11;
  background: white;
}
.row input:focus { outline: none; border-color: #2d8a44; }

.player-entry {
  display: flex;
  align-items: center;
  gap: 8px;
  background: white;
  border-radius: 12px;
  padding: 8px 12px;
  margin-bottom: 8px;
  border: 2px solid #e0d5c0;
}
.player-entry input {
  flex: 1;
  border: none;
  font-family: 'Nunito', sans-serif;
  font-size: 1rem;
  font-weight: 700;
  color: #5c3d11;
  background: transparent;
}
.player-entry input:focus { outline: none; }
.pony-em { font-size: 1.4rem; }
.del-btn {
  background: none;
  border: none;
  color: #e74c3c;
  font-size: 1.2rem;
  cursor: pointer;
  padding: 2px 6px;
  border-radius: 6px;
}

.add-btn {
  width: 100%;
  padding: 10px;
  border-radius: 12px;
  border: 2px dashed #2d8a44;
  background: none;
  color: #1a5c2a;
  font-family: 'Nunito', sans-serif;
  font-size: 0.95rem;
  font-weight: 900;
  cursor: pointer;
  margin-bottom: 4px;
}

.rules {
  background: #fff8e1;
  border-radius: 10px;
  padding: 12px 14px;
  margin-top: 14px;
  border-left: 4px solid #f5c842;
  font-size: 0.82rem;
  color: #5a4020;
  font-weight: 700;
  line-height: 1.7;
}
.rules b { color: #1a5c2a; }

.go-btn {
  width: 100%;
  margin-top: 18px;
  padding: 15px;
  background: linear-gradient(135deg, #1a5c2a, #2d8a44);
  color: white;
  font-family: 'Rye', cursive;
  font-size: 1.3rem;
  border: none;
  border-radius: 14px;
  cursor: pointer;
  box-shadow: 0 4px 16px rgba(0,0,0,0.25);
}

/* ── GAME SCREEN ── */
#game { padding: 0; align-items: stretch; background: none; }

.game-header {
  background: #1a5c2a;
  padding: 12px 16px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 3px 12px rgba(0,0,0,0.3);
  position: sticky;
  top: 0;
  z-index: 50;
}
.game-title {
  font-family: 'Rye', cursive;
  color: #f5c842;
  font-size: 1.3rem;
  text-shadow: 1px 1px 0 #5c3d11;
}
.header-btns { display: flex; gap: 8px; align-items: center; }
.hbtn {
  background: rgba(255,255,255,0.2);
  border: 1px solid rgba(255,255,255,0.4);
  color: white;
  padding: 5px 12px;
  border-radius: 20px;
  font-weight: 900;
  font-size: 0.82rem;
  cursor: pointer;
  font-family: 'Nunito', sans-serif;
}
.hole-pill {
  background: #f5c842;
  color: #5c3d11;
  font-weight: 900;
  font-size: 0.9rem;
  padding: 5px 14px;
  border-radius: 20px;
}

/* ── TRACKS ── */
.tracks {
  padding: 14px;
  background: linear-gradient(180deg, #2d8a44, #3aaa55);
}
.track-card {
  background: rgba(255,255,255,0.18);
  border-radius: 14px;
  margin-bottom: 12px;
  padding: 11px 13px;
  border: 2px solid rgba(255,255,255,0.3);
}
.track-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 8px;
}
.track-name {
  color: white;
  font-weight: 900;
  font-size: 0.95rem;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.4);
}
.money-badge {
  background: #e74c3c;
  color: white;
  font-weight: 900;
  font-size: 0.8rem;
  padding: 3px 10px;
  border-radius: 20px;
}
.money-badge.up { background: #27ae60; }

.track-bar {
  position: relative;
  height: 34px;
  background: #8B6914;
  border-radius: 18px;
  overflow: hidden;
  border: 3px solid #5c3d11;
  margin-bottom: 6px;
}
.track-fill {
  position: absolute;
  left: 0; top: 0; bottom: 0;
  background: linear-gradient(90deg, #8B6914, #c49a2a);
  border-radius: 18px;
  transition: width 0.5s ease;
}
.track-marks {
  position: absolute;
  inset: 0;
  pointer-events: none;
}
.mark {
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 2px;
  height: 20px;
  background: rgba(255,255,255,0.4);
  border-radius: 1px;
}
.pony-dot {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 1.5rem;
  transition: left 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
  z-index: 5;
  filter: drop-shadow(1px 2px 3px rgba(0,0,0,0.4));
  line-height: 1;
}
.pony-dot.rear { animation: rear 0.8s ease forwards; }
@keyframes rear {
  0%   { transform: translateY(-50%) rotate(0deg) scale(1); }
  25%  { transform: translateY(-80%) rotate(-20deg) scale(1.3); }
  50%  { transform: translateY(-100%) rotate(-30deg) scale(1.4); }
  75%  { transform: translateY(-60%) rotate(-10deg) scale(1.2); }
  100% { transform: translateY(-50%) rotate(0deg) scale(1); }
}
.finish-flag {
  position: absolute;
  right: 4px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 1rem;
}
.track-status {
  font-size: 0.75rem;
  color: rgba(255,255,255,0.85);
  font-weight: 700;
  text-align: right;
}
.winner-tape {
  background: repeating-linear-gradient(45deg, #f5c842, #f5c842 8px, #1a5c2a 8px, #1a5c2a 16px);
  height: 6px;
  border-radius: 3px;
  margin-top: 5px;
  display: none;
}
.track-card.won .winner-tape { display: block; }

/* ── SCORING ── */
.scoring {
  padding: 16px;
  background: #fdf6e3;
  border-radius: 22px 22px 0 0;
  margin-top: 0;
}
.scoring h2 {
  font-family: 'Rye', cursive;
  color: #1a5c2a;
  font-size: 1rem;
  margin-bottom: 14px;
  text-align: center;
}
.score-card {
  background: white;
  border-radius: 14px;
  padding: 12px 14px;
  margin-bottom: 12px;
  border: 2px solid #e8dcc8;
  box-shadow: 0 2px 8px rgba(0,0,0,0.06);
}
.score-card-name {
  font-weight: 900;
  color: #5c3d11;
  font-size: 0.95rem;
  margin-bottom: 10px;
}
.score-btns {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 5px;
}
.sb {
  padding: 9px 0;
  border-radius: 9px;
  border: 2px solid;
  font-family: 'Nunito', sans-serif;
  font-weight: 900;
  font-size: 0.75rem;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2px;
  line-height: 1.1;
  transition: transform 0.1s;
}
.sb:active { transform: scale(0.92); }
.sb span { font-size: 0.65rem; font-weight: 700; opacity: 0.85; }
.sb-eagle  { background: #fff3b0; border-color: #d4a017; color: #7a5c00; }
.sb-birdie { background: #d4f5e0; border-color: #27ae60; color: #1a5c2a; }
.sb-par    { background: #e0f0ff; border-color: #2980b9; color: #1a3d6e; }
.sb-bogey  { background: #fff0e0; border-color: #e67e22; color: #7a3b00; }
.sb-double { background: #ffe0e0; border-color: #e74c3c; color: #7a0000; }
.sb-triple { background: #f0d0f0; border-color: #8e44ad; color: #4a005a; }
.sb.selected { outline: 3px solid #333; transform: scale(1.07); }

.next-btn {
  width: 100%;
  margin-top: 6px;
  padding: 14px;
  background: linear-gradient(135deg, #1a5c2a, #2d8a44);
  color: white;
  font-family: 'Rye', cursive;
  font-size: 1.2rem;
  border: none;
  border-radius: 13px;
  cursor: pointer;
  box-shadow: 0 4px 14px rgba(0,0,0,0.2);
}

/* ── OVERLAY ── */
.overlay {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.88);
  z-index: 200;
  align-items: flex-start;
  justify-content: center;
  overflow-y: auto;
  padding: 16px;
}
.overlay.open { display: flex; }
.overlay-box {
  background: #fdf6e3;
  border-radius: 20px;
  padding: 22px 18px;
  width: 100%;
  max-width: 460px;
  border: 3px solid #f5c842;
  margin: auto;
}
.overlay-box h2 {
  font-family: 'Rye', cursive;
  color: #1a5c2a;
  font-size: 1.15rem;
  margin-bottom: 14px;
  text-align: center;
}
.close-btn {
  float: right;
  background: none;
  border: none;
  font-size: 1.4rem;
  cursor: pointer;
  color: #888;
  margin-top: -4px;
}

/* ── SCORECARD TABLE ── */
.sc-wrap { overflow-x: auto; -webkit-overflow-scrolling: touch; }
table.sc {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.78rem;
}
table.sc th {
  background: #1a5c2a;
  color: #f5c842;
  padding: 6px 4px;
  text-align: center;
  font-family: 'Rye', cursive;
  font-size: 0.7rem;
}
table.sc th:first-child { text-align: left; padding-left: 8px; min-width: 80px; }
table.sc td {
  padding: 5px 3px;
  text-align: center;
  border-bottom: 1px solid #f0e8d8;
  color: #5c3d11;
  font-weight: 700;
}
table.sc td:first-child { text-align: left; padding-left: 8px; font-weight: 900; }
table.sc tr:nth-child(even) td { background: #fff8ee; }
.sc-cell {
  display: inline-block;
  border-radius: 5px;
  padding: 1px 4px;
  font-weight: 900;
  font-size: 0.7rem;
  min-width: 20px;
  text-align: center;
}
.sc-eagle  { background: #fff3b0; color: #7a5c00; }
.sc-birdie { background: #d4f5e0; color: #1a5c2a; }
.sc-par    { background: #e0f0ff; color: #1a3d6e; }
.sc-bogey  { background: #fff0e0; color: #7a3b00; }
.sc-double { background: #ffe0e0; color: #7a0000; }
.sc-triple { background: #f0d0f0; color: #4a005a; }

/* ── WIN OVERLAY ── */
.win-card {
  background: #fdf6e3;
  border-radius: 22px;
  padding: 28px 22px;
  text-align: center;
  max-width: 360px;
  width: 90%;
  border: 4px solid #f5c842;
  box-shadow: 0 0 60px rgba(245,200,66,0.5);
}
.win-card h1 {
  font-family: 'Rye', cursive;
  color: #1a5c2a;
  font-size: 1.9rem;
  margin: 8px 0 6px;
}
.win-card p { color: #5c3d11; font-weight: 700; margin-bottom: 18px; white-space: pre-line; }
.win-btn {
  width: 100%;
  padding: 13px;
  background: linear-gradient(135deg, #1a5c2a, #2d8a44);
  color: white;
  font-family: 'Rye', cursive;
  font-size: 1.1rem;
  border: none;
  border-radius: 13px;
  cursor: pointer;
  margin-bottom: 8px;
}
.win-btn.grey { background: #888; font-size: 1rem; }

/* ── FINAL SCREEN ── */
.final-section { margin-bottom: 16px; }
.final-section h3 {
  font-family: 'Rye', cursive;
  color: #1a5c2a;
  font-size: 0.9rem;
  margin-bottom: 8px;
}
.final-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: white;
  border-radius: 10px;
  padding: 10px 13px;
  margin-bottom: 6px;
  border: 2px solid #e8dcc8;
}
.final-row .pname { font-weight: 900; color: #5c3d11; font-size: 0.9rem; }
.final-row .pdetail { font-size: 0.72rem; color: #aaa; font-weight: 700; margin-top: 2px; }
.final-row .pnet {
  font-family: 'Rye', cursive;
  font-size: 1.2rem;
}
.green { color: #27ae60; }
.red   { color: #e74c3c; }
.settle-box {
  background: #1a5c2a;
  border-radius: 13px;
  padding: 14px 15px;
  margin-top: 14px;
}
.settle-box h3 { color: #c8f5d0; font-family: 'Rye', cursive; font-size: 0.85rem; margin-bottom: 10px; }
.settle-row {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 8px;
}
.settle-row .sname { color: white; font-weight: 900; font-size: 0.88rem; flex: 1; }
.settle-amt {
  background: #f5c842;
  color: #5c3d11;
  font-family: 'Rye', cursive;
  font-size: 0.9rem;
  padding: 3px 12px;
  border-radius: 18px;
}

/* ── TOAST ── */
#toast {
  position: fixed;
  bottom: 80px;
  left: 50%;
  transform: translateX(-50%) translateY(16px);
  background: #5c3d11;
  color: white;
  padding: 10px 20px;
  border-radius: 28px;
  font-weight: 900;
  font-size: 0.95rem;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.25s, transform 0.25s;
  z-index: 400;
  white-space: nowrap;
  box-shadow: 0 4px 14px rgba(0,0,0,0.4);
}
#toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

@keyframes confetti-fall {
  0%   { transform: translateY(0) rotate(0deg); opacity: 1; }
  100% { transform: translateY(110vh) rotate(720deg); opacity: 0.2; }
}
</style>
</head>
<body>

<!-- ══ SETUP ══ -->
<div id="setup" class="screen active">
  <div class="title">🐴 The Ponies</div>
  <div class="subtitle">A HORSE RACE GOLF GAME</div>
  <div class="card">
    <h2>Game Setup</h2>
    <div class="row">
      <label>💰 Buy-In $</label>
      <input type="number" id="buyin" value="5" min="1" max="100">
    </div>
    <h2 style="margin-top:14px">Players</h2>
    <div id="player-list"></div>
    <button class="add-btn" onclick="addPlayer('')">+ Add Player</button>
    <div class="rules">
      <b>Win a race by getting:</b><br>
      6 Pars &nbsp;·&nbsp; 2 Birdies &nbsp;·&nbsp; 1 Eagle<br>
      <b>Eagle beats Birdie beats Par in a tie</b><br><br>
      <b>Penalties:</b> Bogey -$1 &nbsp;·&nbsp; Double -$5 &nbsp;·&nbsp; Triple -$10<br>
      <b>Winner</b> collects the pot + all losers' penalties
    </div>
    <button class="go-btn" onclick="startGame()">🏇 Start The Race!</button>
  </div>
</div>

<!-- ══ GAME ══ -->
<div id="game" class="screen">
  <div class="game-header">
    <div class="game-title">🐴 Ponies</div>
    <div class="header-btns">
      <button class="hbtn" onclick="openScorecard()">📋 Card</button>
      <div class="hole-pill" id="hole-pill">Hole 1</div>
    </div>
  </div>
  <div class="tracks" id="tracks"></div>
  <div class="scoring">
    <h2>Enter Scores — Hole <span id="hole-num">1</span></h2>
    <div id="score-cards"></div>
    <button class="next-btn" id="next-btn" onclick="nextHole()">Next Hole →</button>
  </div>
</div>

<!-- ══ WIN OVERLAY ══ -->
<div id="win-overlay" class="overlay">
  <div class="win-card">
    <div style="font-size:2.5rem">🎉🐴🏆</div>
    <h1 id="win-title">Winner!</h1>
    <p id="win-msg"></p>
    <button class="win-btn" id="continue-btn" onclick="continueRace()">🏇 Continue Race</button>
    <button class="win-btn grey" onclick="openFinal()">📋 End &amp; See Results</button>
  </div>
</div>

<!-- ══ SCORECARD OVERLAY ══ -->
<div id="sc-overlay" class="overlay">
  <div class="overlay-box">
    <button class="close-btn" onclick="closeOverlay('sc-overlay')">✕</button>
    <h2>📋 Scorecard</h2>
    <div class="sc-wrap">
      <table class="sc" id="sc-table">
        <thead id="sc-head"></thead>
        <tbody id="sc-body"></tbody>
      </table>
    </div>
    <div style="margin-top:12px;display:flex;flex-wrap:wrap;gap:5px;justify-content:center;">
      <span class="sc-cell sc-eagle">E</span><span style="font-size:.72rem;font-weight:700;color:#888;margin-right:6px">Eagle</span>
      <span class="sc-cell sc-birdie">B</span><span style="font-size:.72rem;font-weight:700;color:#888;margin-right:6px">Birdie</span>
      <span class="sc-cell sc-par">P</span><span style="font-size:.72rem;font-weight:700;color:#888;margin-right:6px">Par</span>
      <span class="sc-cell sc-bogey">+1</span><span style="font-size:.72rem;font-weight:700;color:#888;margin-right:6px">Bogey</span>
      <span class="sc-cell sc-double">+2</span><span style="font-size:.72rem;font-weight:700;color:#888;margin-right:6px">Double</span>
      <span class="sc-cell sc-triple">+3</span><span style="font-size:.72rem;font-weight:700;color:#888">Triple</span>
    </div>
  </div>
</div>

<!-- ══ FINAL OVERLAY ══ -->
<div id="final-overlay" class="overlay">
  <div class="overlay-box">
    <button class="close-btn" onclick="closeOverlay('final-overlay')">✕</button>
    <h2>🏁 Final Results</h2>
    <div id="final-content"></div>
    <button class="go-btn" onclick="newGame()" style="margin-top:16px">🔄 New Game</button>
  </div>
</div>

<div id="toast"></div>

<script>
// ── CONSTANTS ──
var PONIES   = ['🐴','🏇','🦄','🐎'];
var PRIORITY = { eagle: 0, birdie: 1, par: 2 };
var SC_CLASS = { eagle:'sc-eagle', birdie:'sc-birdie', par:'sc-par', bogey:'sc-bogey', double:'sc-double', triple:'sc-triple' };
var SC_LABEL = { eagle:'E', birdie:'B', par:'P', bogey:'+1', double:'+2', triple:'+3' };
var PEN_AMT  = { bogey: 1, double: 5, triple: 10 };

// ── STATE ──
var G = {};

function resetState(players, buyin) {
  G = {
    buyin:        buyin,
    hole:         1,
    players:      players,
    pending:      {},
    races:        [],          // completed races with winners
    currentPens:  {},          // penalty accumulation this race
    scoreLog:     []           // [{hole, scores:{pid:type}}] — every hole ever played
  };
  players.forEach(function(p) {
    G.currentPens[p.id] = 0;
  });
}

// ── SETUP ──
var playerCount = 0;
function addPlayer(name) {
  var list = document.getElementById('player-list');
  var idx  = list.children.length;
  var id   = 'p' + (++playerCount);
  var div  = document.createElement('div');
  div.className = 'player-entry';
  div.setAttribute('data-id', id);
  div.innerHTML =
    '<span class="pony-em">' + PONIES[idx % 4] + '</span>' +
    '<input type="text" placeholder="Player ' + (idx + 1) + '" value="' + name + '">' +
    '<button class="del-btn" onclick="this.parentElement.remove()">&#x2715;</button>';
  list.appendChild(div);
}

addPlayer('Player 1');
addPlayer('Player 2');

function startGame() {
  var entries = document.querySelectorAll('#player-list .player-entry');
  if (entries.length < 1) { toast('Add at least one player!'); return; }
  var buyin = parseFloat(document.getElementById('buyin').value) || 5;
  var players = [];
  for (var i = 0; i < entries.length; i++) {
    var inp  = entries[i].querySelector('input');
    var name = inp ? inp.value.trim() : '';
    if (!name) name = 'Player ' + (i + 1);
    players.push({
      id:      entries[i].getAttribute('data-id'),
      name:    name,
      pony:    PONIES[i % 4],
      pars:    0,
      birdies: 0,
      eagles:  0,
      won:     false
    });
  }
  resetState(players, buyin);
  show('game');
  render();
}

// ── RENDER ──
function render() {
  document.getElementById('hole-pill').textContent = 'Hole ' + G.hole;
  document.getElementById('hole-num').textContent  = G.hole;
  renderTracks();
  renderScoreCards();
}

function progress(p) {
  return Math.max(
    Math.min(p.pars    / 6, 1),
    Math.min(p.birdies / 2, 1),
    Math.min(p.eagles  / 1, 1)
  );
}

function statusLabel(p) {
  if (p.won) return '🏆 WINNER!';
  var parts = [];
  if (p.pars    > 0) parts.push(p.pars    + '/6 pars');
  if (p.birdies > 0) parts.push(p.birdies + '/2 birdies');
  if (p.eagles  > 0) parts.push(p.eagles  + '/1 eagle');
  return parts.length ? parts.join(' · ') : 'No progress yet';
}

function renderTracks() {
  var el = document.getElementById('tracks');
  el.innerHTML = '';
  G.players.forEach(function(p, i) {
    var pct  = progress(p) * 100;
    var left = Math.max(4, pct - 5);
    var pen  = G.currentPens[p.id] || 0;
    var net  = -pen;
    var badgeClass = net >= 0 ? 'money-badge up' : 'money-badge';
    var badgeText  = net >= 0 ? '+$' + net.toFixed(0) : '-$' + Math.abs(net).toFixed(0);

    var div = document.createElement('div');
    div.className = 'track-card' + (p.won ? ' won' : '');
    div.id = 'tc-' + p.id;
    div.innerHTML =
      '<div class="track-top">' +
        '<span class="track-name">' + p.pony + ' ' + p.name + '</span>' +
        '<span class="' + badgeClass + '">' + badgeText + '</span>' +
      '</div>' +
      '<div class="track-bar">' +
        '<div class="track-fill" style="width:' + pct + '%"></div>' +
        '<div class="track-marks">' +
          '<div class="mark" style="left:16.6%"></div>' +
          '<div class="mark" style="left:33.3%"></div>' +
          '<div class="mark" style="left:50%"></div>' +
          '<div class="mark" style="left:66.6%"></div>' +
          '<div class="mark" style="left:83.3%"></div>' +
        '</div>' +
        '<div class="pony-dot" id="pd-' + p.id + '" style="left:' + left + '%">' + p.pony + '</div>' +
        '<span class="finish-flag">🏁</span>' +
      '</div>' +
      '<div class="winner-tape"></div>' +
      '<div class="track-status">' + statusLabel(p) + '</div>';
    el.appendChild(div);
  });
}

function renderScoreCards() {
  var el  = document.getElementById('score-cards');
  el.innerHTML = '';
  var anyActive = false;
  G.players.forEach(function(p, i) {
    if (p.won) return;
    anyActive = true;
    var sel  = G.pending[p.id];
    var card = document.createElement('div');
    card.className = 'score-card';
    var btns = [
      ['eagle','sb-eagle','🦅','Eagle'],
      ['birdie','sb-birdie','🐦','Birdie'],
      ['par','sb-par','⛳','Par'],
      ['bogey','sb-bogey','😬','Bogey'],
      ['double','sb-double','😱','Double'],
      ['triple','sb-triple','💀','Triple']
    ];
    var bHtml = '';
    btns.forEach(function(b) {
      var selClass = sel === b[0] ? ' selected' : '';
      bHtml += '<button class="sb ' + b[1] + selClass + '" onclick="pickScore(\'' + p.id + '\',\'' + b[0] + '\')">' +
               b[2] + '<span>' + b[3] + '</span></button>';
    });
    card.innerHTML =
      '<div class="score-card-name">' + p.pony + ' ' + p.name + ' ' + (sel ? '✅' : '⬜') + '</div>' +
      '<div class="score-btns">' + bHtml + '</div>';
    el.appendChild(card);
  });
  if (!anyActive) {
    el.innerHTML = '<p style="text-align:center;color:#888;padding:16px;font-weight:700">All players finished this race!</p>';
  }
}

// ── SCORING ──
function pickScore(pid, type) {
  G.pending[pid] = type;
  // update penalty display immediately
  if (PEN_AMT[type] !== undefined) {
    // find player
    var base = 0;
    G.players.forEach(function(p) {
      if (p.id === pid && !p.won) {
        // recalc from scratch using log + this pending
      }
    });
  }
  renderScoreCards();
  var p = playerById(pid);
  var labels = { eagle:'Eagle 🦅', birdie:'Birdie 🐦', par:'Par ⛳', bogey:'Bogey -$1', double:'Double -$5', triple:'Triple -$10' };
  toast(p.name + ': ' + labels[type]);
}

function playerById(id) {
  for (var i = 0; i < G.players.length; i++) {
    if (G.players[i].id === id) return G.players[i];
  }
  return null;
}

// ── NEXT HOLE ──
function nextHole() {
  // 1. Apply pending scores
  var keys = Object.keys(G.pending);
  keys.forEach(function(pid) {
    var type = G.pending[pid];
    var p    = playerById(pid);
    if (!p || p.won) return;

    if      (type === 'eagle')  { p.eagles++;  }
    else if (type === 'birdie') { p.birdies++; }
    else if (type === 'par')    { p.pars++;    }
    else if (PEN_AMT[type])     { G.currentPens[p.id] = (G.currentPens[p.id] || 0) + PEN_AMT[type]; }
  });

  // 2. Log this hole's scores
  var holeScores = {};
  keys.forEach(function(pid) { holeScores[pid] = G.pending[pid]; });
  G.scoreLog.push({ hole: G.hole, scores: holeScores });

  // 3. Check for winners
  var finishers = [];
  G.players.forEach(function(p) {
    var type = G.pending[p.id];
    if (p.won || !type) return;
    if (p.eagles >= 1 || p.birdies >= 2 || p.pars >= 6) {
      finishers.push({ p: p, type: type });
    }
  });

  // 4. Clear pending
  G.pending = {};

  if (finishers.length > 0) {
    // Tiebreaker
    finishers.sort(function(a, b) {
      var pa = PRIORITY[a.type] !== undefined ? PRIORITY[a.type] : 99;
      var pb = PRIORITY[b.type] !== undefined ? PRIORITY[b.type] : 99;
      return pa - pb;
    });
    var bestRank = PRIORITY[finishers[0].type] !== undefined ? PRIORITY[finishers[0].type] : 99;
    var winners  = finishers.filter(function(f) {
      return (PRIORITY[f.type] !== undefined ? PRIORITY[f.type] : 99) === bestRank;
    });

    // Payout: pot (all buy-ins) + all non-winner penalties
    var loserPen = 0;
    G.players.forEach(function(p) {
      var isWinner = winners.some(function(w) { return w.p === p; });
      if (!isWinner) loserPen += (G.currentPens[p.id] || 0);
    });
    var pot   = G.players.length * G.buyin;
    var gross = pot + loserPen;
    var share = gross / winners.length;

    // Record race result
    var raceResult = {
      raceNum:  G.races.length + 1,
      winHole:  G.hole,
      winners:  winners.map(function(w) { return w.p.id; }),
      winShare: share,
      pens:     {}
    };
    G.players.forEach(function(p) {
      var isWinner = winners.some(function(w) { return w.p === p; });
      raceResult.pens[p.id] = isWinner ? 0 : (G.currentPens[p.id] || 0);
    });
    G.races.push(raceResult);

    // Mark winners
    winners.forEach(function(w) { w.p.won = true; });

    render();
    // Animate
    winners.forEach(function(w) { animatePony(w.p.id); });

    // Show win screen
    setTimeout(function() {
      var wNames = winners.map(function(w) { return w.p.pony + ' ' + w.p.name; }).join(' & ');
      var how    = finishers[0].type === 'eagle' ? 'with an Eagle! 🦅' :
                   finishers[0].type === 'birdie' ? 'with 2 Birdies! 🐦' : 'with 6 Pars! ⛳';
      document.getElementById('win-title').textContent = wNames + ' Win!';
      document.getElementById('win-msg').textContent   =
        'Won the pot ' + how + '\nPot: $' + share.toFixed(0) + (winners.length > 1 ? ' each' : '');
      // Update continue button label
      document.getElementById('continue-btn').textContent = '🏇 Start Hole ' + (G.hole + 1);
      openOverlay('win-overlay');
      launchConfetti();
    }, 700);

  } else {
    // No winner — just advance hole
    G.hole++;
    render();
    window.scrollTo({ top: 0, behavior: 'smooth' });
    toast('Hole ' + G.hole + ' ⛳');
  }
}

// ── CONTINUE RACE ──
function continueRace() {
  closeOverlay('win-overlay');
  G.hole++;
  // Reset race progress but keep score log and race history
  G.players.forEach(function(p) {
    p.pars = 0; p.birdies = 0; p.eagles = 0; p.won = false;
  });
  G.players.forEach(function(p) { G.currentPens[p.id] = 0; });
  G.pending = {};
  render();
  window.scrollTo({ top: 0, behavior: 'smooth' });
  toast('🏇 Hole ' + G.hole + ' — New Race!');
}

// ── ANIMATE PONY ──
function animatePony(pid) {
  var el = document.getElementById('pd-' + pid);
  if (!el) return;
  el.classList.remove('rear');
  void el.offsetWidth;
  el.classList.add('rear');
  setTimeout(function() { el.classList.remove('rear'); }, 900);
}

// ── SCORECARD ──
function openScorecard() {
  var holes   = G.hole;
  var players = G.players;

  // Build header
  var hh = '<tr>';
  hh += '<th>Player</th>';
  for (var h = 1; h <= holes; h++) hh += '<th>H' + h + '</th>';
  hh += '</tr>';
  document.getElementById('sc-head').innerHTML = hh;

  // Build rows
  var bh = '';
  players.forEach(function(p) {
    bh += '<tr><td>' + p.pony + ' ' + p.name + '</td>';
    for (var h = 1; h <= holes; h++) {
      var entry = null;
      G.scoreLog.forEach(function(log) {
        if (log.hole === h) entry = log.scores[p.id];
      });
      if (entry) {
        bh += '<td><span class="sc-cell ' + (SC_CLASS[entry] || '') + '">' + (SC_LABEL[entry] || '?') + '</span></td>';
      } else {
        bh += '<td style="color:#ccc">—</td>';
      }
    }
    bh += '</tr>';
  });
  document.getElementById('sc-body').innerHTML = bh;

  openOverlay('sc-overlay');
}

// ── FINAL RESULTS ──
function openFinal() {
  closeOverlay('win-overlay');
  buildFinal();
  openOverlay('final-overlay');
}

function buildFinal() {
  var el   = document.getElementById('final-content');
  var html = '';

  if (G.races.length === 0) {
    html = '<p style="text-align:center;color:#888;font-weight:700;padding:20px">No completed races yet.</p>';
    el.innerHTML = html;
    return;
  }

  // Per-race breakdown
  G.races.forEach(function(race) {
    html += '<div class="final-section">';
    html += '<h3>🏇 Race ' + race.raceNum + ' — Won on Hole ' + race.winHole + '</h3>';
    G.players.forEach(function(p) {
      var isWinner = race.winners.indexOf(p.id) !== -1;
      var pen      = race.pens[p.id] || 0;
      var net      = isWinner ? race.winShare - G.buyin : -(G.buyin + pen);
      var netClass = net >= 0 ? 'pnet green' : 'pnet red';
      var ns       = net >= 0 ? '+' : '';
      var detail   = isWinner
        ? 'Buy-in: -$' + G.buyin.toFixed(0) + ' · Won pot: +$' + race.winShare.toFixed(0)
        : 'Buy-in: -$' + G.buyin.toFixed(0) + (pen > 0 ? ' · Penalties: -$' + pen.toFixed(0) : '');
      html +=
        '<div class="final-row">' +
          '<div>' +
            '<div class="pname">' + p.pony + ' ' + p.name + (isWinner ? ' 🏆' : '') + '</div>' +
            '<div class="pdetail">' + detail + '</div>' +
          '</div>' +
          '<div class="' + netClass + '">' + ns + '$' + Math.abs(net).toFixed(0) + '</div>' +
        '</div>';
    });
    html += '</div>';
  });

  // Overall totals (only counting completed races)
  html += '<div class="final-section"><h3>💰 Overall Total</h3>';
  var totals = {};
  G.players.forEach(function(p) { totals[p.id] = 0; });
  G.races.forEach(function(race) {
    G.players.forEach(function(p) {
      var isWinner = race.winners.indexOf(p.id) !== -1;
      var pen      = race.pens[p.id] || 0;
      var net      = isWinner ? race.winShare - G.buyin : -(G.buyin + pen);
      totals[p.id] += net;
    });
  });
  G.players.forEach(function(p) {
    var overall  = totals[p.id];
    var nc       = overall >= 0 ? 'pnet green' : 'pnet red';
    var ns       = overall >= 0 ? '+' : '';
    var border   = overall >= 0 ? '#a8dfc0' : '#f5c0ba';
    html +=
      '<div class="final-row" style="border-color:' + border + ';border-width:3px">' +
        '<div class="pname">' + p.pony + ' ' + p.name + '</div>' +
        '<div class="' + nc + '" style="font-size:1.3rem">' + ns + '$' + Math.abs(overall).toFixed(0) + '</div>' +
      '</div>';
  });
  html += '</div>';

  // Settle-up
  var nets = G.players.map(function(p) { return { name: p.name, pony: p.pony, net: totals[p.id] }; });
  var payers     = nets.filter(function(x) { return x.net < 0; }).map(function(x) { return { name:x.name, pony:x.pony, rem: -x.net }; });
  var collectors = nets.filter(function(x) { return x.net > 0; }).map(function(x) { return { name:x.name, pony:x.pony, rem:  x.net }; });
  var txns = [];
  var pi = 0, ci = 0;
  while (pi < payers.length && ci < collectors.length) {
    var pay = payers[pi], col = collectors[ci];
    var amt = Math.min(pay.rem, col.rem);
    if (amt > 0.01) txns.push({ from: pay.pony + ' ' + pay.name, to: col.pony + ' ' + col.name, amt: amt });
    pay.rem -= amt; col.rem -= amt;
    if (pay.rem < 0.01) pi++;
    if (col.rem < 0.01) ci++;
  }

  html += '<div class="settle-box"><h3>Settle Up</h3>';
  if (txns.length === 0) {
    html += '<div style="color:#c8f5d0;font-weight:700;font-size:.9rem">All square! No payments needed 🤝</div>';
  } else {
    txns.forEach(function(t) {
      html +=
        '<div class="settle-row">' +
          '<span class="sname">' + t.from + ' pays ' + t.to + '</span>' +
          '<span class="settle-amt">$' + t.amt.toFixed(0) + '</span>' +
        '</div>';
    });
  }
  html += '</div>';

  el.innerHTML = html;
}

// ── NEW GAME ──
function newGame() {
  closeOverlay('final-overlay');
  closeOverlay('win-overlay');
  document.getElementById('player-list').innerHTML = '';
  playerCount = 0;
  addPlayer('Player 1');
  addPlayer('Player 2');
  show('setup');
}

// ── HELPERS ──
function show(id) {
  document.querySelectorAll('.screen').forEach(function(s) {
    s.classList.remove('active');
  });
  document.getElementById(id).classList.add('active');
}

function openOverlay(id) {
  document.getElementById(id).classList.add('open');
}

function closeOverlay(id) {
  document.getElementById(id).classList.remove('open');
}

var toastTimer;
function toast(msg) {
  var el = document.getElementById('toast');
  el.textContent = msg;
  el.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(function() { el.classList.remove('show'); }, 2200);
}

function launchConfetti() {
  var emojis = ['🐴','🏆','⭐','🎉','🌟','💰','🦅'];
  for (var i = 0; i < 28; i++) {
    (function(delay) {
      setTimeout(function() {
        var el  = document.createElement('div');
        var dur = 2 + Math.random() * 2;
        el.textContent = emojis[Math.floor(Math.random() * emojis.length)];
        el.style.cssText = 'position:fixed;top:-40px;left:' + (Math.random()*100) + 'vw;' +
          'font-size:' + (1.1 + Math.random()*0.8) + 'rem;z-index:250;pointer-events:none;' +
          'animation:confetti-fall ' + dur + 's ease-in forwards;';
        document.body.appendChild(el);
        setTimeout(function() {
          if (el && el.parentNode) el.parentNode.removeChild(el);
        }, dur * 1000 + 200);
      }, delay);
    })(i * 80);
  }
}
</script>
</body>
</html>
