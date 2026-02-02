<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Static Lab - Grade 5 Science</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Quicksand:wght@400;600&display=swap');

        :root {
            --primary: #4f46e5;
            --secondary: #f59e0b;
            --accent: #10b981;
            --bg: #f3f4f6;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background-color: var(--bg);
            overflow-x: hidden;
            touch-action: manipulation;
        }

        h1, h2, .font-title {
            font-family: 'Fredoka One', cursive;
        }

        .lab-bench {
            background: linear-gradient(to bottom, #d1d5db 0%, #9ca3af 100%);
            border-top: 8px solid #4b5563;
        }

        .object-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
            aspect-ratio: 1 / 1;
        }

        .electron {
            width: 10px;
            height: 10px;
            background-color: #3b82f6;
            border-radius: 50%;
            position: absolute;
            transition: all 0.5s ease-in-out;
            pointer-events: none;
            z-index: 50;
        }

        .spark {
            position: absolute;
            pointer-events: none;
            animation: flash 0.2s ease-out forwards;
        }

        @keyframes flash {
            0% { transform: scale(0); opacity: 1; }
            100% { transform: scale(2); opacity: 0; }
        }

        .floating {
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        #micro-view {
            background: radial-gradient(circle, #2d3748 0%, #1a202c 100%);
            border: 4px solid #4a5568;
            border-radius: 20px;
            position: relative;
            overflow: hidden;
        }

        #inventory::-webkit-scrollbar {
            width: 6px;
        }
        #inventory::-webkit-scrollbar-thumb {
            background-color: #cbd5e1;
            border-radius: 10px;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Header -->
    <header class="bg-indigo-600 text-white p-4 shadow-lg flex justify-between items-center">
        <div class="flex items-center gap-3">
            <div class="bg-yellow-400 p-2 rounded-full text-indigo-900 shadow-inner">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 24 24" fill="currentColor"><path d="M13 10V3L4 14H11V21L20 10H13Z"/></svg>
            </div>
            <div>
                <h1 class="text-xl md:text-2xl tracking-wide leading-none uppercase">THE STATIC LAB</h1>
                <p class="text-[10px] sm:text-xs font-semibold opacity-90 mt-1 uppercase tracking-wider">Created by: Sir Angelo Medez, LPT</p>
            </div>
        </div>
        <div class="flex gap-2 md:gap-4 items-center">
            <div class="bg-indigo-800 px-3 md:px-4 py-1 rounded-full font-bold text-sm md:text-base">Score: <span id="score">0</span></div>
            <button onclick="showInstructions()" class="bg-indigo-500 hover:bg-indigo-400 px-3 py-1 rounded-md text-xs md:text-sm transition shadow-sm">Help</button>
        </div>
    </header>

    <!-- Main Game Area -->
    <main class="flex-grow flex flex-col md:flex-row p-4 gap-4 overflow-hidden">
        
        <!-- Left Panel: The Experiment Zone -->
        <div class="flex-grow flex flex-col gap-4">
            
            <div id="status-bar" class="bg-white p-4 rounded-xl shadow-md border-b-4 border-indigo-200 text-center">
                <p class="text-lg font-semibold text-gray-700" id="hint-text">Select two materials to rub together!</p>
            </div>

            <!-- Interaction Stage -->
            <div class="flex-grow relative flex items-center justify-around bg-blue-50 rounded-3xl border-2 border-dashed border-blue-200 p-8 overflow-hidden">
                
                <div id="slot-1" class="w-32 h-32 md:w-48 md:h-48 flex items-center justify-center bg-white/50 rounded-2xl border-2 border-gray-300 relative transition-all">
                    <span class="text-gray-400 absolute pointer-events-none text-xs uppercase font-bold">Item 1</span>
                    <div id="obj-container-1" class="z-10"></div>
                </div>

                <div class="flex flex-col items-center justify-center gap-4 z-20">
                    <div id="rubbing-area" class="w-24 h-24 rounded-full bg-indigo-100 flex items-center justify-center hidden">
                        <div class="animate-ping absolute w-20 h-20 rounded-full bg-indigo-300 opacity-75"></div>
                        <span class="text-3xl">✨</span>
                    </div>
                    <button id="rub-btn" onclick="startRubbing()" class="hidden bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 px-8 rounded-full shadow-lg transform hover:scale-105 active:scale-95 transition">RUB THEM!</button>
                    <button id="reset-btn" onclick="resetLab()" class="hidden bg-gray-500 hover:bg-gray-600 text-white font-bold py-2 px-6 rounded-full shadow-md transition">Reset Lab</button>
                </div>

                <div id="slot-2" class="w-32 h-32 md:w-48 md:h-48 flex items-center justify-center bg-white/50 rounded-2xl border-2 border-gray-300 relative transition-all">
                    <span class="text-gray-400 absolute pointer-events-none text-xs uppercase font-bold">Item 2</span>
                    <div id="obj-container-2" class="z-10"></div>
                </div>

                <div id="particle-field" class="absolute inset-0 pointer-events-none"></div>
            </div>

            <!-- Micro View -->
            <div id="micro-view-container" class="h-32 md:h-40 hidden flex flex-col">
                <p class="text-xs font-bold text-indigo-900 mb-1 ml-2 uppercase tracking-tighter">Microscope: Electron Flow</p>
                <div id="micro-view" class="flex-grow flex items-center justify-around">
                    <div class="text-center">
                        <div id="micro-atom-1" class="relative w-12 h-12 md:w-16 md:h-16 bg-red-400 rounded-full flex items-center justify-center text-white font-bold text-xl border-4 border-red-200">+</div>
                        <p class="text-white text-[10px] mt-1" id="micro-label-1"></p>
                    </div>
                    <div id="transfer-path" class="w-1/2 h-1 bg-white/20 relative"></div>
                    <div class="text-center">
                        <div id="micro-atom-2" class="relative w-12 h-12 md:w-16 md:h-16 bg-blue-400 rounded-full flex items-center justify-center text-white font-bold text-xl border-4 border-blue-200">-</div>
                        <p class="text-white text-[10px] mt-1" id="micro-label-2"></p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Right Panel: Inventory Grid -->
        <div class="w-full md:w-80 flex flex-col gap-4 h-full">
            <div class="bg-white p-4 rounded-xl shadow-md flex-grow overflow-hidden flex flex-col">
                <h3 class="font-title text-indigo-600 border-b-2 border-indigo-100 pb-2 mb-4 uppercase text-sm tracking-widest text-center">Material Inventory</h3>
                <div id="inventory" class="grid grid-cols-2 md:grid-cols-2 gap-3 overflow-y-auto p-1">
                    <!-- JS generated items as grid cells -->
                </div>
            </div>

            <div class="bg-indigo-900 text-white p-4 rounded-xl shadow-md">
                <h3 class="font-title text-yellow-400 text-sm mb-2 uppercase">Did you know?</h3>
                <p id="fact-box" class="text-xs md:text-sm leading-relaxed opacity-90">Static electricity comes from the Greek word "elektron," which means amber!</p>
            </div>
        </div>
    </main>

    <div class="lab-bench h-12 w-full"></div>

    <div id="toast" class="fixed bottom-16 left-1/2 -translate-x-1/2 bg-gray-800 text-white px-6 py-2 rounded-full text-sm font-bold shadow-xl opacity-0 transition-opacity pointer-events-none z-[200]">
        Copied to clipboard!
    </div>

    <div id="overlay" class="fixed inset-0 bg-black/70 z-[100] hidden items-center justify-center p-4 backdrop-blur-sm">
        <div id="modal-content" class="bg-white rounded-3xl p-6 md:p-8 max-w-md w-full shadow-2xl transform transition-all text-center">
        </div>
    </div>

    <script>
        const MATERIALS = {
            balloon: { name: "Rubber Balloon", icon: "🎈", affinity: -3, color: "bg-pink-400", border: "border-pink-500", fact: "Rubber is an insulator that loves to steal electrons!" },
            wool: { name: "Wool Sweater", icon: "🧶", affinity: 3, color: "bg-orange-200", border: "border-orange-300", fact: "Wool gives away electrons easily, making it positive." },
            glass: { name: "Glass Rod", icon: "🧪", affinity: 5, color: "bg-blue-100", border: "border-blue-200", fact: "Glass rod is very high on the series; it loses electrons easily." },
            silk: { name: "Silk Cloth", icon: "🧣", affinity: -1, color: "bg-purple-200", border: "border-purple-300", fact: "Silk grabs electrons from glass but gives them to rubber." },
            plastic: { name: "Plastic Comb", icon: "🪮", affinity: -4, color: "bg-gray-400", border: "border-gray-500", fact: "Plastic holds onto its electrons very tightly." },
            hair: { name: "Human Hair", icon: "🧑", affinity: 4, color: "bg-yellow-800", border: "border-yellow-900", fact: "Hair loses electrons quickly. That's why it stands up!" }
        };

        const STATE = {
            selected: [],
            score: 0,
            isRubbing: false,
            discoveredPairs: new Set()
        };

        function init() {
            const inv = document.getElementById('inventory');
            Object.keys(MATERIALS).forEach(key => {
                const m = MATERIALS[key];
                const div = document.createElement('div');
                div.className = `object-card ${m.color} p-2 rounded-xl shadow-sm border-b-4 border-black/10 flex flex-col items-center justify-center hover:scale-105 active:scale-95 transition-transform text-center`;
                div.innerHTML = `
                    <span class="text-3xl md:text-4xl mb-1">${m.icon}</span>
                    <span class="text-[9px] md:text-[10px] font-bold uppercase leading-tight">${m.name}</span>
                `;
                div.onclick = () => selectMaterial(key);
                inv.appendChild(div);
            });
            showInstructions();
        }

        function selectMaterial(key) {
            if (STATE.isRubbing || STATE.selected.length >= 2) return;
            if (STATE.selected.includes(key)) return;
            STATE.selected.push(key);
            const slotIdx = STATE.selected.length;
            const container = document.getElementById(`obj-container-${slotIdx}`);
            const slot = document.getElementById(`slot-${slotIdx}`);
            container.innerHTML = `<div class="text-6xl md:text-8xl floating">${MATERIALS[key].icon}</div>`;
            slot.classList.add('border-indigo-500', 'bg-indigo-50', 'shadow-inner');
            if (STATE.selected.length === 2) {
                document.getElementById('rub-btn').classList.remove('hidden');
                document.getElementById('hint-text').innerText = "Click RUB THEM to start the reaction!";
            } else {
                document.getElementById('hint-text').innerText = "Now select Item 2 to compare.";
            }
        }

        async function startRubbing() {
            if (STATE.isRubbing) return;
            STATE.isRubbing = true;
            document.getElementById('rub-btn').classList.add('hidden');
            document.getElementById('rubbing-area').classList.remove('hidden');
            document.getElementById('micro-view-container').classList.remove('hidden');
            const m1 = MATERIALS[STATE.selected[0]];
            const m2 = MATERIALS[STATE.selected[1]];
            document.getElementById('micro-label-1').innerText = m1.name;
            document.getElementById('micro-label-2').innerText = m2.name;
            const giver = m1.affinity > m2.affinity ? 1 : 2;
            const receiver = giver === 1 ? 2 : 1;
            for (let i = 0; i < 12; i++) {
                createElectron(giver, receiver);
                await new Promise(r => setTimeout(r, 150));
                if (i % 4 === 0) createSpark();
            }
            setTimeout(() => finishExperiment(STATE.selected[giver-1], STATE.selected[receiver-1]), 600);
        }

        function createElectron(fromIdx, toIdx) {
            const field = document.getElementById('particle-field');
            const startEl = document.getElementById(`slot-${fromIdx}`);
            const endEl = document.getElementById(`slot-${toIdx}`);
            const startRect = startEl.getBoundingClientRect();
            const endRect = endEl.getBoundingClientRect();
            const fieldRect = field.getBoundingClientRect();
            const e = document.createElement('div');
            e.className = 'electron';
            e.style.left = (startRect.left - fieldRect.left + startRect.width/2) + 'px';
            e.style.top = (startRect.top - fieldRect.top + startRect.height/2) + 'px';
            field.appendChild(e);
            e.offsetHeight;
            e.style.left = (endRect.left - fieldRect.left + endRect.width/2) + 'px';
            e.style.top = (endRect.top - fieldRect.top + endRect.height/2) + 'px';
            e.style.opacity = '0';
            setTimeout(() => e.remove(), 600);
            const microPath = document.getElementById('transfer-path');
            const me = document.createElement('div');
            me.className = 'electron';
            me.style.top = '-4px';
            me.style.left = fromIdx === 1 ? '0%' : '100%';
            microPath.appendChild(me);
            setTimeout(() => me.style.left = fromIdx === 1 ? '100%' : '0%', 10);
            setTimeout(() => me.remove(), 500);
        }

        function createSpark() {
            const area = document.getElementById('rubbing-area');
            const s = document.createElement('div');
            s.className = 'spark text-xl';
            s.innerHTML = '⚡';
            s.style.left = (Math.random() * 60 + 20) + '%';
            s.style.top = (Math.random() * 60 + 20) + '%';
            area.appendChild(s);
            setTimeout(() => s.remove(), 300);
        }

        function finishExperiment(giverKey, receiverKey) {
            const giver = MATERIALS[giverKey];
            const receiver = MATERIALS[receiverKey];
            const pairId = [giverKey, receiverKey].sort().join('-');
            let bonus = 0;
            if (!STATE.discoveredPairs.has(pairId)) {
                STATE.discoveredPairs.add(pairId);
                bonus = 50;
                STATE.score += bonus;
                document.getElementById('score').innerText = STATE.score;
            }
            document.getElementById('rubbing-area').classList.add('hidden');
            document.getElementById('reset-btn').classList.remove('hidden');
            const resultHtml = `
                <h2 class="text-2xl font-title text-indigo-600 mb-2 uppercase">Discovery!</h2>
                <div class="space-y-4 text-left bg-gray-50 p-4 rounded-xl border border-indigo-100">
                    <p class="text-sm">When rubbed, <b>electrons</b> move from the ${giver.name} to the ${receiver.name}.</p>
                    <div class="flex justify-around items-center py-4 bg-white rounded-lg shadow-inner border border-gray-100">
                        <div class="text-center">
                            <span class="text-4xl">${giver.icon}</span>
                            <div class="text-[10px] text-red-600 font-bold">+ POSITIVE</div>
                        </div>
                        <div class="text-lg text-gray-300">➡</div>
                        <div class="text-center">
                            <span class="text-4xl">${receiver.icon}</span>
                            <div class="text-[10px] text-blue-600 font-bold">- NEGATIVE</div>
                        </div>
                    </div>
                    <p class="text-xs text-gray-500 italic">Fact: ${receiver.fact}</p>
                </div>
                <div class="flex flex-col gap-2 mt-6">
                    <button onclick="closeModal()" class="w-full bg-indigo-600 text-white font-bold py-3 rounded-xl shadow-md">Continue Lab</button>
                    <button onclick="shareResult('${giver.name}', '${receiver.name}')" class="w-full bg-indigo-100 text-indigo-700 font-bold py-2 rounded-xl text-sm border border-indigo-200">Share Result</button>
                </div>`;
            showModal(resultHtml);
        }

        function shareResult(giver, receiver) {
            const text = `I discovered that in Sir Angelo Medez's Static Lab, electrons move from ${giver} to ${receiver}! My score is ${STATE.score}! ⚡🔬`;
            const dummy = document.createElement("textarea");
            document.body.appendChild(dummy);
            dummy.value = text;
            dummy.select();
            document.execCommand("copy");
            document.body.removeChild(dummy);
            const toast = document.getElementById('toast');
            toast.style.opacity = '1';
            setTimeout(() => toast.style.opacity = '0', 2000);
        }

        function resetLab() {
            STATE.selected = [];
            STATE.isRubbing = false;
            ['1','2'].forEach(id => {
                document.getElementById(`obj-container-${id}`).innerHTML = '';
                document.getElementById(`slot-${id}`).classList.remove('border-indigo-500', 'bg-indigo-50', 'shadow-inner');
            });
            document.getElementById('rub-btn').classList.add('hidden');
            document.getElementById('reset-btn').classList.add('hidden');
            document.getElementById('micro-view-container').classList.add('hidden');
            document.getElementById('hint-text').innerText = "Select two materials to rub together!";
        }

        function showModal(content) {
            const overlay = document.getElementById('overlay');
            const inner = document.getElementById('modal-content');
            inner.innerHTML = content;
            overlay.classList.remove('hidden');
            overlay.classList.add('flex');
        }

        function closeModal() {
            document.getElementById('overlay').classList.add('hidden');
            document.getElementById('overlay').classList.remove('flex');
        }

        function showInstructions() {
            showModal(`
                <h2 class="text-2xl font-title text-indigo-600 mb-4 uppercase">How to Play</h2>
                <div class="text-left space-y-4 text-sm text-gray-700">
                    <div class="flex gap-3"><span class="bg-indigo-100 w-6 h-6 rounded-full flex items-center justify-center font-bold text-indigo-600 shrink-0">1</span> <p>Select 2 different items from the grid.</p></div>
                    <div class="flex gap-3"><span class="bg-indigo-100 w-6 h-6 rounded-full flex items-center justify-center font-bold text-indigo-600 shrink-0">2</span> <p>Click <b>RUB THEM</b> to watch electrons move between atoms.</p></div>
                    <div class="flex gap-3"><span class="bg-indigo-100 w-6 h-6 rounded-full flex items-center justify-center font-bold text-indigo-600 shrink-0">3</span> <p>Discover all the <b>positive</b> and <b>negative</b> combinations!</p></div>
                </div>
                <button onclick="closeModal()" class="mt-8 w-full bg-indigo-600 text-white font-bold py-3 rounded-xl shadow-lg">Start Experiment</button>
            `);
        }

        window.onload = init;
    </script>
</body>
</html>
