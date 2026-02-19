<!DOCTYPE html> <html lang="zh-CN"> <head> <meta charset="UTF-8"> <meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>双人对战：金币与枪</title> <style> body { margin: 0; padding: 0; background-color: #222; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 100vh; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; color: white; overflow: hidden; }
    #game-container {
        position: relative;
        box-shadow: 0 0 20px rgba(0,0,0,0.5);
    }

    canvas {
        background-color: #333;
        background-image: 
            linear-gradient(#444 1px, transparent 1px),
            linear-gradient(90deg, #444 1px, transparent 1px);
        background-size: 40px 40px;
        border: 4px solid #555;
        border-radius: 4px;
        display: block;
    }

    /* 玩法简介面板 */
    #game-rules {
        background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
        border: 2px solid #444;
        border-radius: 10px;
        padding: 15px 25px;
        margin-bottom: 10px;
        max-width: 800px;
        text-align: center;
    }

    #game-rules h3 {
        margin: 0 0 10px 0;
        color: #ffa502;
        font-size: 18px;
    }

    #game-rules p {
        margin: 5px 0;
        font-size: 13px;
        color: #aaa;
        line-height: 1.5;
    }

    .rule-highlight {
        color: #fff;
        font-weight: bold;
    }

    .rule-coin { color: #ffd32a; }
    .rule-gun { color: #ffa502; }
    .rule-mine { color: #ff6b81; }
    .rule-medkit { color: #2ed573; }
    .rule-pvp { color: #ff4757; }

    /* UI 覆盖层 */
    #ui-layer {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        padding: 10px 20px;
        box-sizing: border-box;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        pointer-events: none;
        z-index: 5;
    }

    .score-box {
        background: rgba(0, 0, 0, 0.6);
        padding: 10px 20px;
        border-radius: 8px;
        font-size: 20px;
        font-weight: bold;
        text-shadow: 1px 1px 2px black;
    }

    #p1-score { color: #ff4757; }
    #p2-score { color: #1e90ff; }

    #timer {
        background: rgba(0, 0, 0, 0.6);
        padding: 10px 20px;
        border-radius: 8px;
        font-size: 24px;
        font-weight: bold;
        color: #ffa502;
    }

    #pause-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.6);
        backdrop-filter: blur(2px);
        display: none;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 8;
        pointer-events: none;
    }

    #pause-overlay h2 {
        font-size: 60px;
        margin: 0;
        color: #fff;
        text-shadow: 0 0 10px #ffa502;
        letter-spacing: 5px;
    }
    
    #pause-overlay p {
        font-size: 18px;
        color: #ddd;
        margin-top: 10px;
    }

    #game-over-modal {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.85);
        display: none;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 10;
    }

    #game-over-modal h1 {
        font-size: 48px;
        margin-bottom: 10px;
        text-transform: uppercase;
    }

    #game-over-modal p {
        font-size: 24px;
        margin-bottom: 30px;
        color: #ccc;
    }

    button {
        padding: 15px 40px;
        font-size: 24px;
        background-color: #2ed573;
        color: white;
        border: none;
        border-radius: 50px;
        cursor: pointer;
        transition: transform 0.1s, background-color 0.2s;
        box-shadow: 0 4px 0 #26af61;
        z-index: 11;
        pointer-events: auto;
    }

    button:active {
        transform: translateY(4px);
        box-shadow: none;
    }

    button:hover {
        background-color: #3ae37f;
    }

    /* 操作提示 */
    .controls-hint {
        margin-top: 10px;
        font-size: 14px;
        color: #888;
        text-align: center;
        line-height: 1.8;
    }
    .key-highlight {
        color: #fff;
        font-weight: bold;
        background: #444;
        padding: 2px 8px;
        border-radius: 4px;
        margin: 0 3px;
    }
    .player-red { color: #ff4757; }
    .player-blue { color: #1e90ff; }

    /* 游戏设置面板 */
    #settings-panel {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
        border: 3px solid #ffa502;
        border-radius: 15px;
        padding: 30px 40px;
        z-index: 20;
        text-align: center;
        box-shadow: 0 0 30px rgba(255, 165, 2, 0.3);
    }

    #settings-panel h2 {
        margin: 0 0 20px 0;
        color: #ffa502;
        font-size: 28px;
        text-shadow: 0 0 10px rgba(255, 165, 2, 0.5);
    }

    .setting-row {
        margin: 15px 0;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 15px;
        flex-wrap: wrap;
    }

    .setting-row label {
        font-size: 16px;
        color: #ddd;
    }

    .setting-row input[type="number"] {
        width: 80px;
        padding: 8px 12px;
        font-size: 18px;
        border: 2px solid #444;
        border-radius: 8px;
        background: #222;
        color: #fff;
        text-align: center;
    }

    .setting-row input[type="number"]:focus {
        outline: none;
        border-color: #ffa502;
    }

    .time-presets, .map-presets {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        justify-content: center;
    }

    .time-presets button, .map-presets button {
        padding: 8px 16px;
        font-size: 14px;
        background-color: #444;
        box-shadow: 0 3px 0 #333;
        border-radius: 8px;
    }

    .time-presets button:hover, .map-presets button:hover {
        background-color: #555;
    }

    .time-presets button.active, .map-presets button.active {
        background-color: #ffa502;
        box-shadow: 0 3px 0 #cc8400;
    }

    #start-btn {
        margin-top: 25px;
        padding: 15px 60px;
        font-size: 22px;
        background: linear-gradient(135deg, #2ed573 0%, #26af61 100%);
        box-shadow: 0 5px 0 #1e8b4d;
        border-radius: 50px;
    }

    #start-btn:hover {
        background: linear-gradient(135deg, #3ae37f 0%, #2ed573 100%);
    }

    .setting-note {
        font-size: 12px;
        color: #666;
        margin-top: 15px;
    }

    .setting-section {
        margin: 20px 0;
        padding: 15px;
        background: rgba(0,0,0,0.3);
        border-radius: 10px;
    }

    .setting-section h3 {
        margin: 0 0 10px 0;
        color: #ffa502;
        font-size: 16px;
    }

    .map-preview {
        display: flex;
        gap: 10px;
        justify-content: center;
        margin-top: 10px;
    }

    .map-card {
        width: 120px;
        padding: 10px;
        background: #2a2a4a;
        border: 2px solid #444;
        border-radius: 8px;
        cursor: pointer;
        transition: all 0.2s;
    }

    .map-card:hover {
        border-color: #ffa502;
        transform: scale(1.05);
    }

    .map-card.active {
        border-color: #ffa502;
        background: #3a3a5a;
        box-shadow: 0 0 15px rgba(255, 165, 2, 0.3);
    }

    .map-card canvas {
        width: 100%;
        height: 60px;
        border: 1px solid #555;
        border-radius: 4px;
    }

    .map-card p {
        margin: 5px 0 0 0;
        font-size: 12px;
        color: #aaa;
    }
</style>
</head> <body>
<!-- 玩法简介 -->
<div id="game-rules">
    <h3>🎮 游戏玩法简介</h3>
    <p>
        <span class="rule-coin">💰 收集金币</span> - 触碰金色金币获得积分，金币会不断刷新
        &nbsp;&nbsp;|&nbsp;&nbsp;
        <span class="rule-gun">🔫 抢夺枪械</span> - 拾取枪械后 <span class="rule-highlight">15 秒内</span> 可发射子弹
        &nbsp;&nbsp;|&nbsp;&nbsp;
        <span class="rule-medkit">🏥 治疗包</span> - 触碰白色红十字恢复 <span class="rule-highlight">10% 血量</span>，最多4个
        &nbsp;&nbsp;|&nbsp;&nbsp;
        <span class="rule-mine">💣 躲避地雷</span> - 触碰红色地雷扣除 <span class="rule-highlight">20% 血量</span>，地雷消失
        &nbsp;&nbsp;|&nbsp;&nbsp;
        <span class="rule-pvp">⚔️ 击败对手</span> - 子弹击中对方扣除 <span class="rule-highlight">20% 血量</span>，4 次即淘汰
    </p>
    <p style="font-size: 12px; color: #666;">
        🏆 获胜条件：击败对手 或 时间结束时金币更多 | 🗺️ 多张地图可选
    </p>
</div>

<div id="game-container">
    <canvas id="gameCanvas" width="800" height="600"></canvas>
    
    <div id="ui-layer">
        <div id="p1-score" class="score-box">🔴 红方金币：<span id="score1">0</span></div>
        <div id="timer">02:00</div>
        <div id="p2-score" class="score-box">🔵 蓝方金币：<span id="score2">0</span></div>
    </div>

    <div id="pause-overlay">
        <h2>PAUSED</h2>
        <p>按 P 键继续游戏</p>
    </div>

    <div id="game-over-modal">
        <h1 id="winner-text">红方获胜!</h1>
        <p id="win-reason">通过击败对手获胜</p>
        <button onclick="showSettings()">再来一局</button>
    </div>

    <!-- 游戏设置面板 -->
    <div id="settings-panel">
        <h2>⚙️ 游戏设置</h2>
        
        <div class="setting-section">
            <h3>📍 选择地图</h3>
            <div class="map-presets" id="map-buttons">
                <button onclick="selectMap(0)" data-map="0" class="active">🏠 经典</button>
                <button onclick="selectMap(1)" data-map="1">🏰 城堡</button>
                <button onclick="selectMap(2)" data-map="2">🌀 迷宫</button>
                <button onclick="selectMap(3)" data-map="3">⚔️ 战场</button>
                <button onclick="selectMap(4)" data-map="4">🔷 四角</button>
            </div>
            <div class="map-preview" id="map-preview"></div>
        </div>
        
        <div class="setting-section">
            <h3>⏱️ 游戏时长 (分钟)</h3>
            <div class="setting-row">
                <input type="number" id="game-time" min="1" max="10" value="2">
            </div>
            <div class="time-presets">
                <button onclick="setTime(1)" data-time="1">1分钟</button>
                <button onclick="setTime(2)" data-time="2" class="active">2分钟</button>
                <button onclick="setTime(3)" data-time="3">3分钟</button>
                <button onclick="setTime(5)" data-time="5">5分钟</button>
            </div>
        </div>
        
        <p class="setting-note">⚠️ 时间范围：1-10 分钟 | 障碍物会阻挡玩家和子弹</p>
        <button id="start-btn" onclick="startGameWithSettings()">🎮 开始游戏</button>
    </div>
</div>

<div class="controls-hint">
    <span class="player-red">🔴 红方玩家</span>：
    <span class="key-highlight">W</span><span class="key-highlight">A</span><span class="key-highlight">S</span><span class="key-highlight">D</span> 移动 
    <span class="key-highlight">空格</span> 射击
    &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <span class="player-blue">🔵 蓝方玩家</span>：
    <span class="key-highlight">↑</span><span class="key-highlight">↓</span><span class="key-highlight">←</span><span class="key-highlight">→</span> 移动 
    <span class="key-highlight">M</span> 射击
    &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
    <span style="color:#aaa">⏸️ 暂停</span>：<span class="key-highlight">P</span>
</div>
<script>
// --- 游戏配置与状态 ---
const canvas = document.getElementById('gameCanvas');
const ctx = canvas.getContext('2d');

// 游戏常量
const PLAYER_RADIUS = 20;
const PLAYER_SPEED = 5;
const BULLET_SPEED = 10;
const BULLET_RADIUS = 5;
const GUN_DURATION = 900;
const COOLDOWN_TIME = 30;
const MAX_HP = 100;
const DAMAGE = 20;
const MINE_DAMAGE = 20;
const MEDKIT_HEAL = 10;
const ITEM_RADIUS = 12;
const MAX_MINES = 3;
const MAX_MEDKITS = 4;
const COIN_PICKUP_RADIUS = PLAYER_RADIUS + ITEM_RADIUS + 5;

let GAME_DURATION = 120;
let selectedMapIndex = 0;

// --- 地图定义 ---
const MAPS = [
    {
        name: "经典",
        icon: "🏠",
        obstacles: []  // 无障碍物
    },
    {
        name: "城堡",
        icon: "🏰",
        obstacles: [
            // 中央城堡结构
            { x: 350, y: 250, w: 100, h: 100 },
            // 四个角楼
            { x: 150, y: 100, w: 60, h: 60 },
            { x: 590, y: 100, w: 60, h: 60 },
            { x: 150, y: 440, w: 60, h: 60 },
            { x: 590, y: 440, w: 60, h: 60 }
        ]
    },
    {
        name: "迷宫",
        icon: "🌀",
        obstacles: [
            // 横向墙壁
            { x: 100, y: 150, w: 200, h: 30 },
            { x: 500, y: 150, w: 200, h: 30 },
            { x: 100, y: 300, w: 150, h: 30 },
            { x: 350, y: 300, w: 300, h: 30 },
            { x: 100, y: 450, w: 200, h: 30 },
            { x: 500, y: 450, w: 200, h: 30 },
            // 纵向墙壁
            { x: 300, y: 100, w: 30, h: 100 },
            { x: 470, y: 400, w: 30, h: 100 }
        ]
    },
    {
        name: "战场",
        icon: "⚔️",
        obstacles: [
            // 中央掩体
            { x: 200, y: 280, w: 40, h: 40 },
            { x: 380, y: 280, w: 40, h: 40 },
            { x: 560, y: 280, w: 40, h: 40 },
            // 上下掩体
            { x: 300, y: 100, w: 200, h: 30 },
            { x: 300, y: 470, w: 200, h: 30 },
            // 两侧掩体
            { x: 50, y: 250, w: 30, h: 100 },
            { x: 720, y: 250, w: 30, h: 100 }
        ]
    },
    {
        name: "四角",
        icon: "🔷",
        obstacles: [
            // 四个大障碍物
            { x: 100, y: 100, w: 120, h: 120 },
            { x: 580, y: 100, w: 120, h: 120 },
            { x: 100, y: 380, w: 120, h: 120 },
            { x: 580, y: 380, w: 120, h: 120 },
            // 中央小障碍
            { x: 370, y: 270, w: 60, h: 60 }
        ]
    }
];

let gameState = {
    isRunning: false,
    isPaused: false,
    timeLeft: GAME_DURATION,
    timerInterval: null
};

const keys = {};
let players = [];
let bullets = [];
let items = [];
let coinEffects = [];
let obstacles = [];
let mineSpawnInterval = null;
let medkitSpawnInterval = null;

// --- 类定义 ---
class Player {
    constructor(id, x, y, color, controls) {
        this.id = id;
        this.x = x;
        this.y = y;
        this.color = color;
        this.controls = controls;
        this.vx = 0;
        this.vy = 0;
        this.lastDirX = 1;
        this.lastDirY = 0;
        this.hp = MAX_HP;
        this.score = 0;
        this.hasGun = false;
        this.gunTimer = 0;
        this.shootCooldown = 0;
        this.invulnerable = 0;
    }

    update() {
        this.vx = 0;
        this.vy = 0;
        if (keys[this.controls.up]) this.vy = -PLAYER_SPEED;
        if (keys[this.controls.down]) this.vy = PLAYER_SPEED;
        if (keys[this.controls.left]) this.vx = -PLAYER_SPEED;
        if (keys[this.controls.right]) this.vx = PLAYER_SPEED;

        if (this.vx !== 0 || this.vy !== 0) {
            const len = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
            this.lastDirX = this.vx / len;
            this.lastDirY = this.vy / len;
        }

        // 【新增】尝试移动并检测障碍物碰撞
        let newX = this.x + this.vx;
        let newY = this.y + this.vy;

        // X轴碰撞检测
        if (this.checkObstacleCollision(newX, this.y)) {
            newX = this.x;
        }
        // Y轴碰撞检测
        if (this.checkObstacleCollision(this.x, newY)) {
            newY = this.y;
        }

        this.x = newX;
        this.y = newY;

        // 边界检测
        if (this.x - PLAYER_RADIUS < 0) this.x = PLAYER_RADIUS;
        if (this.x + PLAYER_RADIUS > canvas.width) this.x = canvas.width - PLAYER_RADIUS;
        if (this.y - PLAYER_RADIUS < 0) this.y = PLAYER_RADIUS;
        if (this.y + PLAYER_RADIUS > canvas.height) this.y = canvas.height - PLAYER_RADIUS;

        if (this.hasGun) {
            this.gunTimer--;
            if (this.gunTimer <= 0) this.hasGun = false;
        }

        if (this.shootCooldown > 0) this.shootCooldown--;
        
        if (this.invulnerable > 0) this.invulnerable--;

        if (this.hasGun && keys[this.controls.shoot] && this.shootCooldown <= 0) {
            this.shoot();
        }
    }

    // 【新增】检测玩家与障碍物碰撞
    checkObstacleCollision(x, y) {
        for (let obs of obstacles) {
            // 圆形玩家与矩形障碍物碰撞检测
            const closestX = Math.max(obs.x, Math.min(x, obs.x + obs.w));
            const closestY = Math.max(obs.y, Math.min(y, obs.y + obs.h));
            const distX = x - closestX;
            const distY = y - closestY;
            const distance = Math.sqrt(distX * distX + distY * distY);
            
            if (distance < PLAYER_RADIUS) {
                return true;
            }
        }
        return false;
    }

    shoot() {
        bullets.push(new Bullet(
            this.x + this.lastDirX * (PLAYER_RADIUS + 5),
            this.y + this.lastDirY * (PLAYER_RADIUS + 5),
            this.lastDirX * BULLET_SPEED,
            this.lastDirY * BULLET_SPEED,
            this.id
        ));
        this.shootCooldown = COOLDOWN_TIME;
    }

    draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, PLAYER_RADIUS, 0, Math.PI * 2);
        
        if (this.invulnerable > 0 && Math.floor(Date.now() / 100) % 2 === 0) {
            ctx.fillStyle = 'rgba(255, 255, 255, 0.5)';
        } else {
            ctx.fillStyle = this.color;
        }
        ctx.fill();
        ctx.lineWidth = 3;
        ctx.strokeStyle = '#fff';
        ctx.stroke();

        ctx.beginPath();
        ctx.arc(this.x + this.lastDirX * 10, this.y + this.lastDirY * 10, 5, 0, Math.PI * 2);
        ctx.fillStyle = 'white';
        ctx.fill();

        const hpPercent = this.hp / MAX_HP;
        ctx.fillStyle = 'red';
        ctx.fillRect(this.x - 20, this.y - 35, 40, 5);
        ctx.fillStyle = '#2ed573';
        ctx.fillRect(this.x - 20, this.y - 35, 40 * hpPercent, 5);

        if (this.hasGun) {
            const ringPercent = this.gunTimer / GUN_DURATION;
            ctx.beginPath();
            ctx.arc(this.x, this.y, PLAYER_RADIUS + 8, -Math.PI/2, -Math.PI/2 + (ringPercent * Math.PI * 2));
            ctx.strokeStyle = '#ffa502';
            ctx.lineWidth = 3;
            ctx.stroke();
        }
    }
}

class Bullet {
    constructor(x, y, vx, vy, ownerId) {
        this.x = x;
        this.y = y;
        this.vx = vx;
        this.vy = vy;
        this.ownerId = ownerId;
        this.active = true;
    }

    update() {
        this.x += this.vx;
        this.y += this.vy;
        
        // 边界检测
        if (this.x < 0 || this.x > canvas.width || this.y < 0 || this.y > canvas.height) {
            this.active = false;
            return;
        }
        
        // 【新增】检测子弹与障碍物碰撞
        for (let obs of obstacles) {
            if (this.x > obs.x && this.x < obs.x + obs.w &&
                this.y > obs.y && this.y < obs.y + obs.h) {
                this.active = false;
                return;
            }
        }
    }

    draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, BULLET_RADIUS, 0, Math.PI * 2);
        ctx.fillStyle = '#fff';
        ctx.fill();
        ctx.beginPath();
        ctx.arc(this.x, this.y, BULLET_RADIUS + 3, 0, Math.PI * 2);
        ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
        ctx.fill();
    }
}

class CoinEffect {
    constructor(x, y, text, color) {
        this.x = x;
        this.y = y;
        this.text = text;
        this.color = color || '#ffd32a';
        this.life = 30;
        this.vy = -2;
    }
    
    update() {
        this.y += this.vy;
        this.life--;
    }
    
    draw() {
        ctx.fillStyle = `rgba(255, 255, 255, ${this.life / 30})`;
        ctx.strokeStyle = this.color;
        ctx.lineWidth = 2;
        ctx.font = 'bold 16px Arial';
        ctx.strokeText(this.text, this.x - 15, this.y);
        ctx.fillText(this.text, this.x - 15, this.y);
    }
}

// --- 游戏设置功能 ---
function setTime(minutes) {
    GAME_DURATION = minutes * 60;
    document.getElementById('game-time').value = minutes;
    
    document.querySelectorAll('.time-presets button').forEach(btn => {
        btn.classList.remove('active');
        if (parseInt(btn.dataset.time) === minutes) {
            btn.classList.add('active');
        }
    });
}

function selectMap(index) {
    selectedMapIndex = index;
    
    document.querySelectorAll('.map-presets button').forEach(btn => {
        btn.classList.remove('active');
        if (parseInt(btn.dataset.map) === index) {
            btn.classList.add('active');
        }
    });
    
    // 更新地图预览
    renderMapPreview();
}

function renderMapPreview() {
    const container = document.getElementById('map-preview');
    container.innerHTML = '';
    
    const map = MAPS[selectedMapIndex];
    const previewCanvas = document.createElement('canvas');
    previewCanvas.width = 120;
    previewCanvas.height = 60;
    const pCtx = previewCanvas.getContext('2d');
    
    // 绘制背景
    pCtx.fillStyle = '#1a1a2e';
    pCtx.fillRect(0, 0, 120, 60);
    
    // 绘制障碍物预览
    pCtx.fillStyle = '#666';
    map.obstacles.forEach(obs => {
        const scale = 0.15;
        pCtx.fillRect(
            obs.x * scale,
            obs.y * scale,
            obs.w * scale,
            obs.h * scale
        );
    });
    
    // 绘制玩家起始位置
    pCtx.fillStyle = '#ff4757';
    pCtx.beginPath();
    pCtx.arc(15, 30, 4, 0, Math.PI * 2);
    pCtx.fill();
    
    pCtx.fillStyle = '#1e90ff';
    pCtx.beginPath();
    pCtx.arc(105, 30, 4, 0, Math.PI * 2);
    pCtx.fill();
    
    const card = document.createElement('div');
    card.className = 'map-card active';
    card.innerHTML = '';
    card.appendChild(previewCanvas);
    const nameP = document.createElement('p');
    nameP.textContent = `${map.icon} ${map.name} (${map.obstacles.length}个障碍)`;
    card.appendChild(nameP);
    
    container.appendChild(card);
}

function startGameWithSettings() {
    const input = document.getElementById('game-time');
    let minutes = parseInt(input.value);
    
    if (isNaN(minutes) || minutes < 1) minutes = 1;
    if (minutes > 10) minutes = 10;
    
    GAME_DURATION = minutes * 60;
    
    document.getElementById('settings-panel').style.display = 'none';
    
    initGame();
}

function showSettings() {
    document.getElementById('game-over-modal').style.display = 'none';
    document.getElementById('settings-panel').style.display = 'block';
    
    const currentMinutes = Math.round(GAME_DURATION / 60);
    document.getElementById('game-time').value = currentMinutes;
    
    document.querySelectorAll('.time-presets button').forEach(btn => {
        btn.classList.remove('active');
        if (parseInt(btn.dataset.time) === currentMinutes) {
            btn.classList.add('active');
        }
    });
    
    renderMapPreview();
}

// --- 游戏逻辑函数 ---
function initGame() {
    // 【新增】加载选定地图的障碍物
    const selectedMap = MAPS[selectedMapIndex];
    obstacles = selectedMap.obstacles.map(obs => ({...obs}));  // 深拷贝
    
    players = [
        new Player(1, 100, 300, '#ff4757', { up: 'w', down: 's', left: 'a', right: 'd', shoot: ' ' }),
        new Player(2, 700, 300, '#1e90ff', { up: 'ArrowUp', down: 'ArrowDown', left: 'ArrowLeft', right: 'ArrowRight', shoot: 'm' })
    ];
    bullets = [];
    items = [];
    coinEffects = [];
    gameState.timeLeft = GAME_DURATION;
    gameState.isRunning = true;
    gameState.isPaused = false;

    spawnItem('coin');
    spawnItem('coin');
    spawnItem('coin');
    spawnItem('gun');
    
    for (let i = 0; i < MAX_MINES; i++) {
        spawnItem('mine');
    }
    
    for (let i = 0; i < MAX_MEDKITS; i++) {
        spawnItem('medkit');
    }

    if (gameState.timerInterval) clearInterval(gameState.timerInterval);
    if (mineSpawnInterval) clearInterval(mineSpawnInterval);
    if (medkitSpawnInterval) clearInterval(medkitSpawnInterval);

    gameState.timerInterval = setInterval(() => {
        if (gameState.isRunning && !gameState.isPaused) {
            gameState.timeLeft--;
            updateTimerUI();
            if (gameState.timeLeft <= 0) endGame('time');
        }
    }, 1000);

    mineSpawnInterval = setInterval(() => {
        if (gameState.isRunning && !gameState.isPaused) {
            const currentMines = getCurrentItemCount('mine');
            if (currentMines < MAX_MINES) {
                spawnItem('mine');
            }
        }
    }, 5000);
    
    medkitSpawnInterval = setInterval(() => {
        if (gameState.isRunning && !gameState.isPaused) {
            const currentMedkits = getCurrentItemCount('medkit');
            if (currentMedkits < MAX_MEDKITS) {
                spawnItem('medkit');
            }
        }
    }, 8000);

    document.getElementById('game-over-modal').style.display = 'none';
    document.getElementById('pause-overlay').style.display = 'none';
    updateUI();
    updateTimerUI();
    requestAnimationFrame(gameLoop);
}

function getCurrentItemCount(type) {
    return items.filter(item => item.type === type && !item.collected).length;
}

function spawnItem(type) {
    if (type === 'mine' && getCurrentItemCount('mine') >= MAX_MINES) {
        return;
    }
    if (type === 'medkit' && getCurrentItemCount('medkit') >= MAX_MEDKITS) {
        return;
    }

    let valid = false, x, y, attempts = 0;
    while (!valid && attempts < 150) {  // 增加尝试次数
        x = 60 + Math.random() * (canvas.width - 120);
        y = 60 + Math.random() * (canvas.height - 120);
        valid = true;
        
        // 检查与玩家距离
        for (let p of players) {
            const dist = Math.hypot(p.x - x, p.y - y);
            if (dist < PLAYER_RADIUS + ITEM_RADIUS + 50) {
                valid = false;
                break;
            }
        }
        
        // 【新增】检查是否在障碍物内部
        for (let obs of obstacles) {
            if (x > obs.x - ITEM_RADIUS && x < obs.x + obs.w + ITEM_RADIUS &&
                y > obs.y - ITEM_RADIUS && y < obs.y + obs.h + ITEM_RADIUS) {
                valid = false;
                break;
            }
        }
        
        // 检查与其他物品距离
        for (let item of items) {
            if (item.collected) continue;
            if (Math.hypot(item.x - x, item.y - y) < ITEM_RADIUS * 3) {
                valid = false;
                break;
            }
        }
        
        attempts++;
    }
    if (valid) {
        items.push({ x, y, type, collected: false });
    }
}

function checkCollisions() {
    players.forEach(p => {
        for (let i = items.length - 1; i >= 0; i--) {
            const item = items[i];
            if (item.collected) continue;
            
            const dist = Math.hypot(p.x - item.x, p.y - item.y);
            
            if (dist < COIN_PICKUP_RADIUS) {
                if (item.type === 'coin') {
                    item.collected = true;
                    p.score++;
                    coinEffects.push(new CoinEffect(item.x, item.y, '+1', '#ffd32a'));
                    items.splice(i, 1);
                    updateUI();
                    setTimeout(() => {
                        if (gameState.isRunning && !gameState.isPaused) {
                            spawnItem('coin');
                        }
                    }, 500);
                    
                } else if (item.type === 'gun') {
                    item.collected = true;
                    p.hasGun = true;
                    p.gunTimer = GUN_DURATION;
                    items.splice(i, 1);
                    spawnItem('gun');
                    
                } else if (item.type === 'mine') {
                    if (p.invulnerable <= 0) {
                        item.collected = true;
                        p.hp -= MINE_DAMAGE;
                        p.invulnerable = 60;
                        coinEffects.push(new CoinEffect(item.x, item.y, '-20%', '#ff4757'));
                        if (p.hp <= 0) {
                            p.hp = 0;
                            const winner = players.find(pl => pl.id !== p.id);
                            endGame('kill', winner ? winner.id : p.id);
                        }
                        items.splice(i, 1);
                        updateUI();
                    }
                    
                } else if (item.type === 'medkit') {
                    if (p.hp < MAX_HP) {
                        item.collected = true;
                        p.hp = Math.min(p.hp + MEDKIT_HEAL, MAX_HP);
                        coinEffects.push(new CoinEffect(item.x, item.y, '+10%', '#2ed573'));
                        items.splice(i, 1);
                        updateUI();
                    }
                }
            }
        }
    });

    bullets.forEach(b => {
        if (!b.active) return;
        players.forEach(p => {
            if (p.id !== b.ownerId && Math.hypot(p.x - b.x, p.y - b.y) < PLAYER_RADIUS + BULLET_RADIUS) {
                b.active = false;
                p.hp -= DAMAGE;
                if (p.hp <= 0) {
                    p.hp = 0;
                    endGame('kill', b.ownerId);
                }
                updateUI();
            }
        });
    });
}

function updateUI() {
    const score1El = document.getElementById('score1');
    const score2El = document.getElementById('score2');
    if (score1El) score1El.innerText = players[0].score;
    if (score2El) score2El.innerText = players[1].score;
}

function updateTimerUI() {
    const m = Math.floor(gameState.timeLeft / 60);
    const s = gameState.timeLeft % 60;
    const timerEl = document.getElementById('timer');
    if (timerEl) {
        timerEl.innerText = `${m.toString().padStart(2, '0')}:${s.toString().padStart(2, '0')}`;
        if (gameState.timeLeft <= 30) {
            timerEl.style.color = '#ff4757';
            timerEl.style.textShadow = '0 0 10px rgba(255, 71, 87, 0.8)';
        } else {
            timerEl.style.color = '#ffa502';
            timerEl.style.textShadow = 'none';
        }
    }
}

function togglePause() {
    if (!gameState.isRunning) return;
    gameState.isPaused = !gameState.isPaused;
    document.getElementById('pause-overlay').style.display = gameState.isPaused ? 'flex' : 'none';
}

function endGame(reason, winnerId = null) {
    gameState.isRunning = false;
    gameState.isPaused = false;
    clearInterval(gameState.timerInterval);
    clearInterval(mineSpawnInterval);
    clearInterval(medkitSpawnInterval);
    document.getElementById('pause-overlay').style.display = 'none';
    
    const modal = document.getElementById('game-over-modal');
    const title = document.getElementById('winner-text');
    const reasonText = document.getElementById('win-reason');
    modal.style.display = 'flex';

    if (reason === 'kill') {
        const winnerName = winnerId === 1 ? "红方" : "蓝方";
        title.innerText = `${winnerName} 获胜!`;
        title.style.color = winnerId === 1 ? "#ff4757" : "#1e90ff";
        reasonText.innerText = "通过击败对手获胜";
    } else {
        const s1 = players[0].score, s2 = players[1].score;
        if (s1 > s2) {
            title.innerText = "红方 获胜!";
            title.style.color = "#ff4757";
            reasonText.innerText = `时间到！红方以 ${s1} : ${s2} 的金币优势获胜`;
        } else if (s2 > s1) {
            title.innerText = "蓝方 获胜!";
            title.style.color = "#1e90ff";
            reasonText.innerText = `时间到！蓝方以 ${s2} : ${s1} 的金币优势获胜`;
        } else {
            title.innerText = "平局!";
            title.style.color = "#fff";
            reasonText.innerText = `时间到！双方金币数相同 (${s1} : ${s2})`;
        }
    }
}

function resetGame() {
    initGame();
}

function drawGunIcon(x, y, rotation = 0) {
    ctx.save();
    ctx.translate(x, y);
    ctx.rotate(rotation);
    
    ctx.fillStyle = '#2d3436';
    ctx.fillRect(-12, -6, 24, 12);
    
    ctx.fillStyle = '#636e72';
    ctx.fillRect(8, -4, 10, 8);
    
    ctx.fillStyle = '#8b4513';
    ctx.fillRect(-14, -2, 8, 10);
    
    ctx.strokeStyle = '#2d3436';
    ctx.lineWidth = 2;
    ctx.beginPath();
    ctx.arc(-6, 4, 4, 0, Math.PI, false);
    ctx.stroke();
    
    ctx.fillStyle = '#e74c3c';
    ctx.fillRect(-2, -8, 4, 3);
    
    ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
    ctx.fillRect(-10, -5, 20, 3);
    
    ctx.restore();
}

function gameLoop() {
    if (!gameState.isRunning) return;
    
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    
    if (!gameState.isPaused) {
        players.forEach(p => p.update());
        bullets.forEach(b => b.update());
        bullets = bullets.filter(b => b.active);
        checkCollisions();
        
        coinEffects.forEach(effect => effect.update());
        coinEffects = coinEffects.filter(effect => effect.life > 0);
    }

    // 【新增】绘制障碍物
    obstacles.forEach(obs => {
        // 障碍物主体
        ctx.fillStyle = '#4a4a6a';
        ctx.fillRect(obs.x, obs.y, obs.w, obs.h);
        
        // 边框
        ctx.strokeStyle = '#6a6a8a';
        ctx.lineWidth = 3;
        ctx.strokeRect(obs.x, obs.y, obs.w, obs.h);
        
        // 顶部高光
        ctx.fillStyle = 'rgba(255, 255, 255, 0.1)';
        ctx.fillRect(obs.x, obs.y, obs.w, 5);
        
        // 纹理效果
        ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
        ctx.lineWidth = 1;
        for (let i = 0; i < obs.w; i += 15) {
            ctx.beginPath();
            ctx.moveTo(obs.x + i, obs.y);
            ctx.lineTo(obs.x + i, obs.y + obs.h);
            ctx.stroke();
        }
        for (let i = 0; i < obs.h; i += 15) {
            ctx.beginPath();
            ctx.moveTo(obs.x, obs.y + i);
            ctx.lineTo(obs.x + obs.w, obs.y + i);
            ctx.stroke();
        }
    });

    // 绘制物品
    items.forEach(item => {
        if (item.collected) return;
        
        ctx.beginPath();
        if (item.type === 'coin') {
            const glow = 5 + Math.sin(Date.now() / 200) * 3;
            ctx.arc(item.x, item.y, ITEM_RADIUS + glow, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(255, 211, 42, 0.3)';
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(item.x, item.y, ITEM_RADIUS, 0, Math.PI * 2);
            ctx.fillStyle = '#ffd32a';
            ctx.fill();
            ctx.strokeStyle = '#e1b12c';
            ctx.lineWidth = 2;
            ctx.stroke();
            ctx.fillStyle = '#fff';
            ctx.font = 'bold 14px Arial';
            ctx.fillText("$", item.x - 4, item.y + 5);
            
        } else if (item.type === 'gun') {
            ctx.beginPath();
            ctx.arc(item.x, item.y, ITEM_RADIUS + 8, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(255, 165, 2, 0.2)';
            ctx.fill();
            
            drawGunIcon(item.x, item.y, 0);
            
            const pulse = 3 + Math.sin(Date.now() / 150) * 2;
            ctx.beginPath();
            ctx.arc(item.x, item.y, ITEM_RADIUS + 8 + pulse, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(255, 165, 2, 0.4)';
            ctx.lineWidth = 1;
            ctx.stroke();
            
        } else if (item.type === 'mine') {
            ctx.arc(item.x, item.y, ITEM_RADIUS, 0, Math.PI * 2);
            ctx.fillStyle = '#ff4757';
            ctx.fill();
            ctx.strokeStyle = '#c0392b';
            ctx.lineWidth = 2;
            ctx.stroke();
            ctx.beginPath();
            ctx.arc(item.x, item.y, 5, 0, Math.PI * 2);
            ctx.fillStyle = '#2d3436';
            ctx.fill();
            const pulse = 3 + Math.sin(Date.now() / 150) * 2;
            ctx.beginPath();
            ctx.arc(item.x, item.y, ITEM_RADIUS + pulse, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(255, 71, 87, 0.4)';
            ctx.lineWidth = 1;
            ctx.stroke();
            
        } else if (item.type === 'medkit') {
            ctx.beginPath();
            ctx.arc(item.x, item.y, ITEM_RADIUS, 0, Math.PI * 2);
            ctx.fillStyle = '#ffffff';
            ctx.fill();
            ctx.strokeStyle = '#dfe6e9';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            ctx.fillStyle = '#e74c3c';
            ctx.fillRect(item.x - 3, item.y - 8, 6, 16);
            ctx.fillRect(item.x - 8, item.y - 3, 16, 6);
            
            const pulse = 3 + Math.sin(Date.now() / 200) * 2;
            ctx.beginPath();
            ctx.arc(item.x, item.y, ITEM_RADIUS + pulse, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(46, 213, 115, 0.4)';
            ctx.lineWidth = 1;
            ctx.stroke();
        }
    });

    coinEffects.forEach(effect => effect.draw());

    players.forEach(p => p.draw());
    bullets.forEach(b => b.draw());
    
    requestAnimationFrame(gameLoop);
}

// --- 事件监听 ---
window.addEventListener('keydown', e => {
    if (e.key.toLowerCase() === 'p') {
        togglePause();
        return;
    }
    keys[e.key] = true;
    if(e.key === ' ') e.preventDefault();
});

window.addEventListener('keyup', e => {
    keys[e.key] = false;
});

// 初始化时显示设置面板
showSettings();
</script> </body> </html>
