<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>⚔️ RPG Online Game - Phiêu Lưu Hành Động</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- React CDN -->
    <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    
    <!-- Babel Standalone for JSX -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700;900&display=swap');
        
        * {
            font-family: 'Roboto', sans-serif;
        }
        
        body {
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }

        @keyframes ping {
            75%, 100% {
                transform: scale(2);
                opacity: 0;
            }
        }

        .animate-ping {
            animation: ping 0.6s cubic-bezier(0, 0, 0.2, 1);
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }

        .animate-bounce {
            animation: bounce 1s infinite;
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.5;
            }
        }

        .animate-pulse {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }

        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(0, 0, 0, 0.3);
        }

        ::-webkit-scrollbar-thumb {
            background: rgba(147, 51, 234, 0.5);
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: rgba(147, 51, 234, 0.8);
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const { useState, useEffect } = React;
        const { Sword, Shield, Heart, Zap, TrendingUp, ShoppingCart, Users, DollarSign, Gift, Star, Crown, Sparkles, Flame } = lucide;

        const RPGGame = () => {
            // Load/Save game state
            const loadGameState = () => {
                try {
                    const saved = localStorage.getItem('rpgGameState');
                    return saved ? JSON.parse(saved) : null;
                } catch {
                    return null;
                }
            };

            const [gameStarted, setGameStarted] = useState(false);
            const [playerName, setPlayerName] = useState('');
            const [nameError, setNameError] = useState('');
            
            // Player stats
            const [player, setPlayer] = useState({
                name: '',
                hp: 100,
                maxHp: 100,
                atk: 2,
                def: 0,
                crit: 5,
                gold: 0,
                level: 1,
                exp: 0,
                currentStage: 1,
                weapon: null,
                armor: null,
                pet: null,
                inventory: [],
                dailyBosses: 2,
                weeklyBosses: 3,
                lastDailyReset: Date.now(),
                lastWeeklyReset: Date.now(),
            });

            const [currentView, setCurrentView] = useState('game');
            const [battleLog, setBattleLog] = useState([]);
            const [monster, setMonster] = useState(null);
            const [isInBattle, setIsInBattle] = useState(false);
            const [canAttack, setCanAttack] = useState(true);
            const [clickEffect, setClickEffect] = useState([]);
            const [adBoosts, setAdBoosts] = useState({
                hp: { active: false, endTime: 0 },
                atk: { active: false, endTime: 0 },
                def: { active: false, endTime: 0 }
            });
            const [marketListings, setMarketListings] = useState([]);
            const [tradeTarget, setTradeTarget] = useState('');
            const [withdrawHistory, setWithdrawHistory] = useState([]);

            // Shops data
            const weaponShop = [
                { name: 'Kiếm Gỗ', atk: 20, price: 200, icon: '🪵' },
                { name: 'Kiếm Đá', atk: 35, price: 500, icon: '🪨' },
                { name: 'Kiếm Sắt', atk: 50, price: 1000, icon: '⚔️' },
                { name: 'Kiếm Vàng', atk: 75, price: 2000, icon: '💛' },
                { name: 'Kiếm Kim Cương', atk: 125, price: 3000, icon: '💎' },
                { name: 'Kiếm Cầu Vồng', atk: 180, price: 4500, icon: '🌈' },
                { name: 'Kiếm Thánh', atk: 300, price: 7000, icon: '✨' },
            ];

            const armorShop = [
                { name: 'Giáp Vải', def: 3, hp: 50, price: 500, icon: '👕' },
                { name: 'Giáp Đồng', def: 7, hp: 75, price: 1000, icon: '🥉' },
                { name: 'Giáp Sắt', def: 10, hp: 100, price: 1500, icon: '🛡️' },
                { name: 'Giáp Kim Cương', def: 15, hp: 150, price: 3000, icon: '💠' },
                { name: 'Giáp Thánh', def: 30, hp: 300, price: 5000, icon: '👑' },
            ];

            const petShop = [
                { name: 'Gà Con', atkBonus: 5, price: 500, icon: '🐔' },
                { name: 'Chó Con', atkBonus: 8, price: 1000, icon: '🐕' },
                { name: 'Sói Xám', atkBonus: 13, price: 1500, icon: '🐺' },
                { name: 'Voi Ma Mút', atkBonus: 20, price: 2300, icon: '🐘' },
                { name: 'Rồng Thần', atkBonus: 30, price: 3500, icon: '🐉' },
            ];

            // Load game on mount
            useEffect(() => {
                const savedState = loadGameState();
                if (savedState && savedState.name) {
                    setPlayer(savedState);
                    setGameStarted(true);
                }
            }, []);

            // Save game
            const saveGame = (newPlayerState) => {
                try {
                    localStorage.setItem('rpgGameState', JSON.stringify(newPlayerState));
                } catch (e) {
                    console.error('Could not save game', e);
                }
            };

            // Reset daily/weekly bosses
            useEffect(() => {
                const now = Date.now();
                const dayMs = 24 * 60 * 60 * 1000;
                const weekMs = 7 * dayMs;

                let updated = false;
                let newPlayer = { ...player };

                if (now - player.lastDailyReset > dayMs) {
                    newPlayer.dailyBosses = 2;
                    newPlayer.lastDailyReset = now;
                    updated = true;
                }

                if (now - player.lastWeeklyReset > weekMs) {
                    newPlayer.weeklyBosses = 3;
                    newPlayer.lastWeeklyReset = now;
                    updated = true;
                }

                if (updated) {
                    setPlayer(newPlayer);
                    saveGame(newPlayer);
                }
            }, [player]);

            // Character creation
            const handleCreateCharacter = () => {
                if (playerName.length < 5) {
                    setNameError('Tên phải có ít nhất 5 ký tự!');
                    return;
                }
                
                const hasNumber = /\d/.test(playerName);
                if (!hasNumber) {
                    setNameError('Tên phải có ít nhất 1 chữ số!');
                    return;
                }

                const newPlayer = {
                    ...player,
                    name: playerName,
                };
                
                setPlayer(newPlayer);
                setGameStarted(true);
                saveGame(newPlayer);
            };

            // Calculate total stats
            const getTotalStats = () => {
                let totalAtk = player.atk;
                let totalDef = player.def;
                let totalHp = player.maxHp;
                let totalCrit = player.crit;

                if (player.weapon) totalAtk += player.weapon.atk;
                if (player.armor) {
                    totalDef += player.armor.def;
                    totalHp += player.armor.hp;
                }
                if (player.pet) {
                    totalAtk += Math.floor(totalAtk * (player.pet.atkBonus / 100));
                }

                // Ad boosts
                if (adBoosts.hp.active && Date.now() < adBoosts.hp.endTime) totalHp += 100;
                if (adBoosts.atk.active && Date.now() < adBoosts.atk.endTime) totalAtk += 75;
                if (adBoosts.def.active && Date.now() < adBoosts.def.endTime) totalDef += 10;

                return { totalAtk, totalDef, totalHp, totalCrit };
            };

            // Generate monster
            const generateMonster = (stage, isBoss = false, bossType = 'normal') => {
                const baseHp = 30 + stage * 15;
                const baseAtk = 1 + stage * 0.5;
                
                let hp = baseHp;
                let atk = baseAtk;
                let goldReward = 10 + stage * 5;
                let expReward = 20 + stage * 10;
                let name = `Quái Vật Lv.${stage}`;
                let icon = '👾';

                if (isBoss) {
                    if (bossType === 'stage') {
                        hp = baseHp * 1.5;
                        atk = baseAtk * 1.2;
                        goldReward *= 2;
                        expReward *= 2;
                        name = `Boss Ải ${Math.floor(stage / 10) + 1}`;
                        icon = '👹';
                    } else if (bossType === 'daily') {
                        hp = baseHp * 3;
                        atk = baseAtk * 2;
                        goldReward *= 5;
                        expReward *= 3;
                        name = `Boss Ngày`;
                        icon = '🔥';
                    } else if (bossType === 'weekly') {
                        hp = baseHp * 5;
                        atk = baseAtk * 3;
                        goldReward *= 10;
                        expReward *= 5;
                        name = `Boss Tuần`;
                        icon = '⚡';
                    }
                }

                return {
                    name,
                    icon,
                    hp: Math.floor(hp),
                    maxHp: Math.floor(hp),
                    atk: Math.floor(atk),
                    goldReward: Math.floor(goldReward),
                    expReward: Math.floor(expReward),
                    stage,
                    isBoss,
                    bossType
                };
            };

            // Start battle
            const startBattle = (bossType = null) => {
                const isBoss = bossType !== null;
                let newMonster;

                if (bossType === 'daily') {
                    if (player.dailyBosses <= 0) {
                        addLog('⚠️ Bạn đã hết lượt đánh Boss Ngày!', 'error');
                        return;
                    }
                    newMonster = generateMonster(player.currentStage, true, 'daily');
                } else if (bossType === 'weekly') {
                    if (player.weeklyBosses <= 0) {
                        addLog('⚠️ Bạn đã hết lượt đánh Boss Tuần!', 'error');
                        return;
                    }
                    newMonster = generateMonster(player.currentStage, true, 'weekly');
                } else {
                    const isStageBoss = player.currentStage % 10 === 0;
                    newMonster = generateMonster(player.currentStage, isStageBoss, isStageBoss ? 'stage' : null);
                }

                setMonster(newMonster);
                setIsInBattle(true);
                setCanAttack(true);
                setBattleLog([]);
                addLog(`⚔️ Chiến đấu với ${newMonster.icon} ${newMonster.name}!`, 'info');
                addLog(`💡 Click vào quái để tấn công!`, 'info');
            };

            // Add log
            const addLog = (message, type = 'info') => {
                setBattleLog(prev => [...prev, { message, type, time: Date.now() }].slice(-10));
            };

            // Player attack
            const playerAttack = (e) => {
                if (!canAttack || !monster || !isInBattle) return;

                // Tạo hiệu ứng click
                const rect = e.currentTarget.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const newEffect = { id: Date.now(), x, y };
                setClickEffect(prev => [...prev, newEffect]);
                setTimeout(() => {
                    setClickEffect(prev => prev.filter(ef => ef.id !== newEffect.id));
                }, 600);

                const stats = getTotalStats();
                const isCrit = Math.random() * 100 < stats.totalCrit;
                let damage = stats.totalAtk;
                if (isCrit) damage *= 2;

                const newMonster = { ...monster, hp: Math.max(0, monster.hp - damage) };
                setMonster(newMonster);

                addLog(`💥 Bạn gây ${damage} sát thương${isCrit ? ' (CHÍ MẠNG!)' : ''}`, 'success');

                // Cooldown ngắn để tránh spam quá nhanh
                setCanAttack(false);
                setTimeout(() => setCanAttack(true), 200);

                if (newMonster.hp <= 0) {
                    handleVictory(newMonster);
                } else {
                    // Quái phản đòn sau 0.5s
                    setTimeout(() => monsterAttack(), 500);
                }
            };

            // Monster attack
            const monsterAttack = () => {
                if (!monster || !isInBattle) return;

                const stats = getTotalStats();
                const damage = Math.max(1, monster.atk - stats.totalDef);
                const newHp = Math.max(0, player.hp - damage);

                setPlayer(prev => ({ ...prev, hp: newHp }));
                addLog(`🔴 ${monster.name} gây ${damage} sát thương!`, 'error');

                if (newHp <= 0) {
                    handleDefeat();
                }
            };

            // Victory
            const handleVictory = (defeatedMonster) => {
                const newGold = player.gold + defeatedMonster.goldReward;
                const newExp = player.exp + defeatedMonster.expReward;
                const expToLevel = player.level * 100;
                
                let newLevel = player.level;
                let remainingExp = newExp;
                let newAtk = player.atk;
                let newMaxHp = player.maxHp;

                while (remainingExp >= expToLevel) {
                    remainingExp -= expToLevel;
                    newLevel++;
                    newAtk += 2;
                    newMaxHp += 10;
                }

                let updatedPlayer = {
                    ...player,
                    gold: newGold,
                    exp: remainingExp,
                    level: newLevel,
                    atk: newAtk,
                    maxHp: newMaxHp,
                    hp: player.maxHp, // Full heal after battle
                };

                // Boss specific updates
                if (defeatedMonster.bossType === 'daily') {
                    updatedPlayer.dailyBosses--;
                } else if (defeatedMonster.bossType === 'weekly') {
                    updatedPlayer.weeklyBosses--;
                } else if (!defeatedMonster.isBoss) {
                    updatedPlayer.currentStage++;
                }

                setPlayer(updatedPlayer);
                saveGame(updatedPlayer);

                addLog(`🎉 Chiến thắng! +${defeatedMonster.goldReward}💰 +${defeatedMonster.expReward}⭐`, 'success');
                if (newLevel > player.level) {
                    addLog(`🆙 Level Up! Lv.${newLevel}`, 'success');
                }

                setIsInBattle(false);
                setMonster(null);
            };

            // Defeat
            const handleDefeat = () => {
                addLog('💀 Bạn đã thua! -50% vàng', 'error');
                const newGold = Math.floor(player.gold * 0.5);
                const updatedPlayer = {
                    ...player,
                    gold: newGold,
                    hp: player.maxHp
                };
                setPlayer(updatedPlayer);
                saveGame(updatedPlayer);
                setIsInBattle(false);
                setMonster(null);
            };

            // Buy item
            const buyItem = (item, type) => {
                if (player.gold < item.price) {
                    addLog('⚠️ Không đủ vàng!', 'error');
                    return;
                }

                const updatedPlayer = { ...player, gold: player.gold - item.price };
                
                if (type === 'weapon') updatedPlayer.weapon = item;
                else if (type === 'armor') {
                    updatedPlayer.armor = item;
                    updatedPlayer.maxHp = player.maxHp + item.hp;
                    updatedPlayer.hp = updatedPlayer.maxHp;
                }
                else if (type === 'pet') updatedPlayer.pet = item;

                setPlayer(updatedPlayer);
                saveGame(updatedPlayer);
                addLog(`✅ Đã mua ${item.icon} ${item.name}!`, 'success');
            };

            // Upgrade stats
            const upgradeStats = (stat) => {
                const costs = {
                    atk: 100 + player.atk * 50,
                    hp: 150 + player.maxHp * 2,
                    crit: 200 + player.crit * 100
                };

                if (player.gold < costs[stat]) {
                    addLog('⚠️ Không đủ vàng để nâng cấp!', 'error');
                    return;
                }

                const updatedPlayer = { ...player, gold: player.gold - costs[stat] };
                
                if (stat === 'atk') updatedPlayer.atk += 5;
                else if (stat === 'hp') {
                    updatedPlayer.maxHp += 20;
                    updatedPlayer.hp = updatedPlayer.maxHp;
                }
                else if (stat === 'crit') updatedPlayer.crit += 2;

                setPlayer(updatedPlayer);
                saveGame(updatedPlayer);
                addLog(`⬆️ Đã nâng cấp ${stat.toUpperCase()}!`, 'success');
            };

            // Watch ad (placeholder)
            const watchAd = (type) => {
                // PLACEHOLDER: Tích hợp Adsterra.com ở đây
                addLog('📺 Đang xem quảng cáo... (Demo mode)', 'info');
                
                setTimeout(() => {
                    const endTime = Date.now() + 10 * 60 * 1000;
                    
                    if (type === 'hp' || type === 'atk' || type === 'def') {
                        setAdBoosts(prev => ({
                            ...prev,
                            [type]: { active: true, endTime }
                        }));
                        addLog(`✅ Buff ${type.toUpperCase()} trong 10 phút!`, 'success');
                    } else if (type === 'coin50' || type === 'coin100') {
                        const bonus = type === 'coin50' ? 50 : 100;
                        const updatedPlayer = { ...player, gold: player.gold + bonus };
                        setPlayer(updatedPlayer);
                        saveGame(updatedPlayer);
                        addLog(`💰 +${bonus} Vàng từ quảng cáo!`, 'success');
                    }
                }, 2000);
            };

            // Character creation screen
            if (!gameStarted) {
                return (
                    <div className="min-h-screen bg-gradient-to-br from-purple-900 via-blue-900 to-black text-white p-8 flex items-center justify-center">
                        <div className="max-w-md w-full bg-gradient-to-br from-purple-800/50 to-blue-800/50 backdrop-blur-lg rounded-3xl p-8 shadow-2xl border border-purple-500/30">
                            <div className="text-center mb-8">
                                <h1 className="text-5xl font-bold mb-2 bg-gradient-to-r from-yellow-400 to-pink-500 bg-clip-text text-transparent">
                                    ⚔️ RPG ONLINE ⚔️
                                </h1>
                                <p className="text-purple-300">Bắt đầu hành trình của bạn!</p>
                            </div>

                            <div className="space-y-4">
                                <div>
                                    <label className="block text-sm font-bold mb-2 text-purple-200">Tên Nhân Vật</label>
                                    <input
                                        type="text"
                                        value={playerName}
                                        onChange={(e) => {
                                            setPlayerName(e.target.value);
                                            setNameError('');
                                        }}
                                        placeholder="Tối thiểu 5 ký tự + số"
                                        className="w-full px-4 py-3 bg-black/30 border-2 border-purple-500/50 rounded-xl focus:border-pink-500 focus:outline-none text-white placeholder-purple-300"
                                    />
                                    {nameError && <p className="text-red-400 text-sm mt-2">⚠️ {nameError}</p>}
                                </div>

                                <div className="bg-black/30 rounded-xl p-4 border border-purple-500/30">
                                    <h3 className="font-bold mb-3 text-yellow-400">📊 Stats Bắt Đầu:</h3>
                                    <div className="grid grid-cols-2 gap-2 text-sm">
                                        <div className="flex items-center gap-2">
                                            <Heart size={16} className="text-red-500" />
                                            <span>HP: 100</span>
                                        </div>
                                        <div className="flex items-center gap-2">
                                            <Sword size={16} className="text-orange-500" />
                                            <span>ATK: 2</span>
                                        </div>
                                        <div className="flex items-center gap-2">
                                            <Shield size={16} className="text-blue-500" />
                                            <span>DEF: 0</span>
                                        </div>
                                        <div className="flex items-center gap-2">
                                            <Zap size={16} className="text-yellow-500" />
                                            <span>CRIT: 5%</span>
                                        </div>
                                    </div>
                                </div>

                                <button
                                    onClick={handleCreateCharacter}
                                    className="w-full py-4 bg-gradient-to-r from-pink-500 to-purple-600 hover:from-pink-600 hover:to-purple-700 rounded-xl font-bold text-lg shadow-lg transform hover:scale-105 transition-all duration-200"
                                >
                                    🎮 BẮT ĐẦU PHIÊU LƯU
                                </button>
                            </div>
                        </div>
                    </div>
                );
            }

            const stats = getTotalStats();

            // Main game UI
            return (
                <div className="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 text-white">
                    {/* Header */}
                    <div className="bg-gradient-to-r from-purple-900/80 to-blue-900/80 backdrop-blur-lg border-b-2 border-purple-500/30 shadow-xl">
                        <div className="max-w-7xl mx-auto px-4 py-4">
                            <div className="flex items-center justify-between flex-wrap gap-4">
                                <div>
                                    <h1 className="text-2xl font-bold bg-gradient-to-r from-yellow-400 to-pink-500 bg-clip-text text-transparent">
                                        👤 {player.name}
                                    </h1>
                                    <p className="text-sm text-purple-300">Level {player.level} • Ải {player.currentStage}</p>
                                </div>
                                
                                <div className="flex gap-4 flex-wrap">
                                    <div className="bg-black/30 px-4 py-2 rounded-lg border border-yellow-500/30">
                                        <div className="flex items-center gap-2">
                                            <span className="text-2xl">💰</span>
                                            <span className="font-bold text-yellow-400">{player.gold.toLocaleString()}</span>
                                        </div>
                                    </div>
                                    
                                    <div className="bg-black/30 px-4 py-2 rounded-lg border border-blue-500/30">
                                        <div className="flex items-center gap-2">
                                            <Star size={20} className="text-blue-400" />
                                            <span className="font-bold">{player.exp}/{player.level * 100}</span>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            {/* Stats Bar */}
                            <div className="mt-4 grid grid-cols-2 md:grid-cols-4 gap-2">
                                <div className="bg-red-900/30 px-3 py-2 rounded-lg border border-red-500/30">
                                    <div className="flex items-center justify-between text-sm">
                                        <Heart size={16} />
                                        <span className="font-bold">{player.hp}/{stats.totalHp}</span>
                                    </div>
                                </div>
                                <div className="bg-orange-900/30 px-3 py-2 rounded-lg border border-orange-500/30">
                                    <div className="flex items-center justify-between text-sm">
                                        <Sword size={16} />
                                        <span className="font-bold">ATK: {stats.totalAtk}</span>
                                    </div>
                                </div>
                                <div className="bg-blue-900/30 px-3 py-2 rounded-lg border border-blue-500/30">
                                    <div className="flex items-center justify-between text-sm">
                                        <Shield size={16} />
                                        <span className="font-bold">DEF: {stats.totalDef}</span>
                                    </div>
                                </div>
                                <div className="bg-yellow-900/30 px-3 py-2 rounded-lg border border-yellow-500/30">
                                    <div className="flex items-center justify-between text-sm">
                                        <Zap size={16} />
                                        <span className="font-bold">CRIT: {stats.totalCrit}%</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    {/* Navigation */}
                    <div className="bg-black/30 border-b border-purple-500/30">
                        <div className="max-w-7xl mx-auto px-4">
                            <div className="flex gap-2 overflow-x-auto py-2">
                                {[
                                    { id: 'game', label: '⚔️ Chiến Đấu' },
                                    { id: 'upgrade', label: '⬆️ Nâng Cấp' },
                                    { id: 'shop', label: '🛒 Cửa Hàng' },
                                    { id: 'boss', label: '👑 Boss' },
                                    { id: 'ads', label: '📺 Quảng Cáo' },
                                    { id: 'market', label: '🏪 Chợ' },
                                    { id: 'withdraw', label: '💵 Rút Tiền' },
                                ].map(nav => (
                                    <button
                                        key={nav.id}
                                        onClick={() => setCurrentView(nav.id)}
                                        className={`px-4 py-2 rounded-lg font-bold whitespace-nowrap transition-all ${
                                            currentView === nav.id
                                                ? 'bg-gradient-to-r from-pink-500 to-purple-600 shadow-lg'
                                                : 'bg-purple-800/30 hover:bg-purple-700/50'
                                        }`}
                                    >
                                        {nav.label}
                                    </button>
                                ))}
                            </div>
                        </div>
                    </div>

                    {/* Main Content */}
                    <div className="max-w-7xl mx-auto px-4 py-6">
                        {/* GAME VIEW */}
                        {currentView === 'game' && (
                            <div className="grid md:grid-cols-2 gap-6">
                                {/* Battle Arena */}
                                <div className="bg-gradient-to-br from-purple-900/50 to-blue-900/50 rounded-2xl p-6 border-2 border-purple-500/30 shadow-xl">
                                    <h2 className="text-2xl font-bold mb-4 text-center bg-gradient-to-r from-yellow-400 to-pink-500 bg-clip-text text-transparent">
                                        ⚔️ Chiến Trường
                                    </h2>
                                    
                                    {!isInBattle ? (
                                        <div className="text-center space-y-4">
                                            <div className="text-6xl mb-4 animate-bounce">🏰</div>
                                            <p className="text-purple-300 mb-4">Sẵn sàng chiến đấu?</p>
                                            <button
                                                onClick={() => startBattle()}
                                                className="w-full py-4 bg-gradient-to-r from-green-500 to-emerald-600 hover:from-green-600 hover:to-emerald-700 rounded-xl font-bold text-lg shadow-lg transform hover:scale-105 transition-all"
                                            >
                                                ⚔️ BẮT ĐẦU CHIẾN ĐẤU
                                            </button>
                                        </div>
                                    ) : (
                                        <div className="space-y-4">
                                            {/* Monster - Clickable */}
                                            <div 
                                                onClick={playerAttack}
                                                className="bg-red-900/30 rounded-xl p-6 border-2 border-red-500/50 cursor-pointer hover:bg-red-800/40 hover:border-red-400 hover:scale-105 transition-all duration-200 relative overflow-hidden active:scale-95"
                                                style={{ userSelect: 'none' }}
                                            >
                                                {/* Click Effects */}
                                                {clickEffect.map(effect => (
                                                    <div
                                                        key={effect.id}
                                                        className="absolute pointer-events-none text-4xl font-bold animate-ping"
                                                        style={{
                                                            left: effect.x,
                                                            top: effect.y,
                                                            color: '#ff6b6b'
                                                        }}
                                                    >
                                                        💥
                                                    </div>
                                                ))}
                                                
                                                <div className="text-center relative z-10">
                                                    <div className="text-7xl mb-3 animate-bounce">{monster.icon}</div>
                                                    <h3 className="font-bold text-2xl text-red-300 mb-2">{monster.name}</h3>
                                                    <div className="bg-black/50 rounded-lg p-3 inline-block">
                                                        <div className="flex items-center justify-center gap-2 mb-2">
                                                            <Heart size={20} className="text-red-500" />
                                                            <span className="font-bold text-xl">{monster.hp}/{monster.maxHp}</span>
                                                        </div>
                                                        <div className="w-64 bg-black/50 rounded-full h-4 overflow-hidden">
                                                            <div 
                                                                className="bg-gradient-to-r from-red-600 to-pink-500 h-full transition-all duration-300"
                                                                style={{ width: `${(monster.hp / monster.maxHp) * 100}%` }}
                                                            />
                                                        </div>
                                                    </div>
                                                    
                                                    {/* Click hint */}
                                                    <div className="mt-4 text-yellow-300 text-sm animate-pulse">
                                                        👆 CLICK ĐỂ TẤN CÔNG! 👆
                                                    </div>
                                                </div>
                                                
                                                {/* Glow effect */}
                                                <div className="absolute inset-0 bg-gradient-to-r from-red-500/20 to-orange-500/20 blur-xl opacity-50 pointer-events-none" />
                                            </div>

                                            {/* VS */}
                                            <div className="text-center">
                                                <span className="text-4xl font-bold bg-gradient-to-r from-yellow-400 to-red-500 bg-clip-text text-transparent">
                                                    ⚡ VS ⚡
                                                </span>
                                            </div>

                                            {/* Player in battle */}
                                            <div className="bg-blue-900/30 rounded-xl p-4 border-2 border-blue-500/50">
                                                <div className="text-center">
                                                    <div className="text-6xl mb-2">🛡️</div>
                                                    <h3 className="font-bold text-xl text-blue-300">{player.name}</h3>
                                                    <div className="mt-2">
                                                        <div className="flex items-center justify-center gap-2 mb-1">
                                                            <Heart size={16} className="text-red-500" />
                                                            <span className="font-bold">{player.hp}/{stats.totalHp}</span>
                                                        </div>
                                                        <div className="w-full bg-black/50 rounded-full h-3 overflow-hidden">
                                                            <div 
                                                                className="bg-gradient-to-r from-green-600 to-emerald-500 h-full transition-all duration-300"
                                                                style={{ width: `${(player.hp / stats.totalHp) * 100}%` }}
                                                            />
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>

                                            {/* Stats Info */}
                                            <div className="bg-black/30 rounded-lg p-3 text-center text-sm">
                                                <div className="flex justify-around">
                                                    <span>⚔️ ATK: <strong className="text-orange-400">{stats.totalAtk}</strong></span>
                                                    <span>🛡️ DEF: <strong className="text-blue-400">{stats.totalDef}</strong></span>
                                                    <span>⚡ CRIT: <strong className="text-yellow-400">{stats.totalCrit}%</strong></span>
                                                </div>
                                            </div>
                                        </div>
                                    )}
                                </div>

                                {/* Battle Log & Equipment */}
                                <div className="space-y-6">
                                    {/* Battle Log */}
                                    <div className="bg-black/50 rounded-2xl p-6 border-2 border-purple-500/30">
                                        <h3 className="text-xl font-bold mb-4 flex items-center gap-2">
                                            <Sparkles size={20} className="text-yellow-400" />
                                            Nhật Ký Chiến Đấu
                                        </h3>
                                        <div className="space-y-2 max-h-64 overflow-y-auto">
                                            {battleLog.length === 0 ? (
                                                <p className="text-purple-300 text-center py-4">Chưa có trận chiến nào...</p>
                                            ) : (
                                                battleLog.map((log, i) => (
                                                    <div
                                                        key={i}
                                                        className={`p-2 rounded-lg text-sm ${
                                                            log.type === 'success' ? 'bg-green-900/30 text-green-300' :
                                                            log.type === 'error' ? 'bg-red-900/30 text-red-300' :
                                                            'bg-blue-900/30 text-blue-300'
                                                        }`}
                                                    >
                                                        {log.message}
                                                    </div>
                                                ))
                                            )}
                                        </div>
                                    </div>

                                    {/* Equipment */}
                                    <div className="bg-gradient-to-br from-purple-900/50 to-pink-900/50 rounded-2xl p-6 border-2 border-purple-500/30">
                                        <h3 className="text-xl font-bold mb-4 flex items-center gap-2">
                                            <Crown size={20} className="text-yellow-400" />
                                            Trang Bị
                                        </h3>
                                        <div className="space-y-3">
                                            <div className="bg-black/30 p-3 rounded-lg">
                                                <div className="flex items-center justify-between">
                                                    <span className="text-purple-300">⚔️ Vũ Khí:</span>
                                                    <span className="font-bold">{player.weapon ? `${player.weapon.icon} ${player.weapon.name}` : 'Chưa có'}</span>
                                                </div>
                                            </div>
                                            <div className="bg-black/30 p-3 rounded-lg">
                                                <div className="flex items-center justify-between">
                                                    <span className="text-purple-300">🛡️ Giáp:</span>
                                                    <span className="font-bold">{player.armor ? `${player.armor.icon} ${player.armor.name}` : 'Chưa có'}</span>
                                                </div>
                                            </div>
                                            <div className="bg-black/30 p-3 rounded-lg">
                                                <div className="flex items-center justify-between">
                                                    <span className="text-purple-300">🐾 Pet:</span>
                                                    <span className="font-bold">{player.pet ? `${player.pet.icon} ${player.pet.name}` : 'Chưa có'}</span>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        )}

                        {/* UPGRADE VIEW */}
                        {currentView === 'upgrade' && (
                            <div className="max-w-3xl mx-auto">
                                <h2 className="text-3xl font-bold mb-6 text-center bg-gradient-to-r from-yellow-400 to-pink-500 bg-clip-text text-transparent">
                                    ⬆️ NÂNG CẤP NHÂN VẬT
                                </h2>
                                <div className="grid md:grid-cols-3 gap-4">
                                    {[
                                        { stat: 'atk', label: 'Sức Mạnh', icon: '⚔️', current: player.atk, bonus: '+5 ATK', color: 'from-orange-500 to-red-600' },
                                        { stat: 'hp', label: 'Máu', icon: '❤️', current: player.maxHp, bonus: '+20 HP', color: 'from-red-500 to-pink-600' },
                                        { stat: 'crit', label: 'Chí Mạng', icon: '⚡', current: player.crit, bonus: '+2% CRIT', color: 'from-yellow-500 to-orange-600' }
                                    ].map(item => (
                                        <div key={item.stat} className="bg-gradient-to-br from-purple-900/50 to-blue-900/50 rounded-2xl p-6 border-2 border-purple-500/30">
                                            <div className="text-center mb-4">
                                                <div className="text-5xl mb-2">{item.icon}</div>
                                                <h3 className="font-bold text-xl">{item.label}</h3>
                                                <p className="text-purple-300 text-sm mt-1">Hiện tại: {item.current}</p>
                                            </div>
                                            <button
                                                onClick={() => upgradeStats(item.stat)}
                                                className={`w-full py-3 bg-gradient-to-r ${item.color} hover:scale-105 rounded-xl font-bold shadow-lg transform transition-all`}
                                            >
                                                {item.bonus}
                                                <div className="text-sm mt-1">💰 {(100 + player[item.stat === 'hp' ? 'maxHp' : item.stat] * (item.stat === 'atk' ? 50 : item.stat === 'hp' ? 2 : 100)).toLocaleString()}</div>
                                            </button>
                                        </div>
                                    ))}
                                </div>
                            </div>
                        )}

                        {/* SHOP VIEW */}
                        {currentView === 'shop' && (
                            <div className="space-y-8">
                                {/* Weapon Shop */}
                                <div>
                                    <h2 className="text-3xl font-bold mb-4 text-center bg-gradient-to-r from-yellow-400 to-orange-500 bg-clip-text text-transparent">
                                        ⚔️ CỬA HÀNG VŨ KHÍ
                                    </h2>
                                    <div className="grid md:grid-cols-4 gap-4">
                                        {weaponShop.map(weapon => (
                                            <div key={weapon.name} className="bg-gradient-to-br from-orange-900/50 to-red-900/50 rounded-xl p-4 border-2 border-orange-500/30 hover:border-orange-400 transition-all hover:scale-105">
                                                <div className="text-center">
                                                    <div className="text-4xl mb-2">{weapon.icon}</div>
                                                    <h3 className="font-bold">{weapon.name}</h3>
                                                    <p className="text-orange-300 text-sm">+{weapon.atk} ATK</p>
                                                    <button
                                                        onClick={() => buyItem(weapon, 'weapon')}
                                                        disabled={player.weapon?.name === weapon.name}
                                                        className={`mt-3 w-full py-2 rounded-lg font-bold text-sm ${
                                                            player.weapon?.name === weapon.name
                                                                ? 'bg-gray-600 cursor-not-allowed'
                                                                : 'bg-gradient-to-r from-yellow-500 to-orange-600 hover:from-yellow-600 hover:to-orange-700'
                                                        }`}
                                                    >
                                                        {player.weapon?.name === weapon.name ? '✓ Đang dùng' : `💰 ${weapon.price}`}
                                                    </button>
                                                </div>
                                            </div>
                                        ))}
                                    </div>
                                </div>

                                {/* Armor Shop */}
                                <div>
                                    <h2 className="text-3xl font-bold mb-4 text-center bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
                                        🛡️ CỬA HÀNG GIÁP
                                    </h2>
                                    <div className="grid md:grid-cols-5 gap-4">
                                        {armorShop.map(armor => (
                                            <div key={armor.name} className="bg-gradient-to-br from-blue-900/50 to-purple-900/50 rounded-xl p-4 border-2 border-blue-500/30 hover:border-blue-400 transition-all hover:scale-105">
                                                <div className="text-center">
                                                    <div className="text-4xl mb-2">{armor.icon}</div>
                                                    <h3 className="font-bold text-sm">{armor.name}</h3>
                                                    <p className="text-blue-300 text-xs">+{armor.def} DEF</p>
                                                    <p className="text-red-300 text-xs">+{armor.hp} HP</p>
                                                    <button
                                                        onClick={() => buyItem(armor, 'armor')}
                                                        disabled={player.armor?.name === armor.name}
                                                        className={`mt-3 w-full py-2 rounded-lg font-bold text-sm ${
                                                            player.armor?.name === armor.name
                                                                ? 'bg-gray-600 cursor-not-allowed'
                                                                : 'bg-gradient-to-r from-blue-500 to-purple-600 hover:from-blue-600 hover:to-purple-700'
                                                        }`}
                                                    >
                                                        {player.armor?.name === armor.name ? '✓ Đang dùng' : `💰 ${armor.price}`}
                                                    </button>
                                                </div>
                                            </div>
                                        ))}
                                    </div>
                                </div>

                                {/* Pet Shop */}
                                <div>
                                    <h2 className="text-3xl font-bold mb-4 text-center bg-gradient-to-r from-green-400 to-emerald-500 bg-clip-text text-transparent">
                                        🐾 CỬA HÀNG PET
                                    </h2>
                                    <div className="grid md:grid-cols-5 gap-4">
                                        {petShop.map(pet => (
                                            <div key={pet.name} className="bg-gradient-to-br from-green-900/50 to-emerald-900/50 rounded-xl p-4 border-2 border-green-500/30 hover:border-green-400 transition-all hover:scale-105">
                                                <div className="text-center">
                                                    <div className="text-4xl mb-2">{pet.icon}</div>
                                                    <h3 className="font-bold text-sm">{pet.name}</h3>
                                                    <p className="text-green-300 text-xs">+{pet.atkBonus}% ATK</p>
                                                    <button
                                                        onClick={() => buyItem(pet, 'pet')}
                                                        disabled={player.pet?.name === pet.name}
                                                        className={`mt-3 w-full py-2 rounded-lg font-bold text-sm ${
                                                            player.pet?.name === pet.name
                                                                ? 'bg-gray-600 cursor-not-allowed'
                                                                : 'bg-gradient-to-r from-green-500 to-emerald-600 hover:from-green-600 hover:to-emerald-700'
                                                        }`}
                                                    >
                                                        {player.pet?.name === pet.name ? '✓ Đang dùng' : `💰 ${pet.price}`}
                                                    </button>
                                                </div>
                                            </div>
                                        ))}
                                    </div>
                                </div>
                            </div>
                        )}

                        {/* BOSS VIEW */}
                        {currentView === 'boss' && (
                            <div className="max-w-4xl mx-auto">
                                <h2 className="text-3xl font-bold mb-6 text-center bg-gradient-to-r from-red-400 to-orange-500 bg-clip-text text-transparent">
                                    👑 BOSS TỰ CHỌN
                                </h2>
                                <div className="grid md:grid-cols-2 gap-6">
                                    {/* Daily Boss */}
                                    <div className="bg-gradient-to-br from-red-900/50 to-orange-900/50 rounded-2xl p-6 border-2 border-red-500/30">
                                        <div className="text-center mb-4">
                                            <div className="text-6xl mb-2">🔥</div>
                                            <h3 className="text-2xl font-bold text-red-300">BOSS NGÀY</h3>
                                            <p className="text-sm text-orange-300 mt-2">Phần thưởng x5 Vàng!</p>
                                        </div>
                                        <div className="bg-black/30 rounded-lg p-3 mb-4">
                                            <p className="text-center">Lượt còn lại: <span className="font-bold text-yellow-400">{player.dailyBosses}/2</span></p>
                                        </div>
                                        <button
                                            onClick={() => startBattle('daily')}
                                            disabled={player.dailyBosses <= 0}
                                            className={`w-full py-4 rounded-xl font-bold text-lg shadow-lg transform transition-all ${
                                                player.dailyBosses > 0
                                                    ? 'bg-gradient-to-r from-red-500 to-orange-600 hover:from-red-600 hover:to-orange-700 hover:scale-105'
                                                    : 'bg-gray-600 cursor-not-allowed opacity-50'
                                            }`}
                                        >
                                            {player.dailyBosses > 0 ? '⚔️ THÁCH ĐẤU' : '❌ Hết lượt'}
                                        </button>
                                    </div>

                                    {/* Weekly Boss */}
                                    <div className="bg-gradient-to-br from-purple-900/50 to-pink-900/50 rounded-2xl p-6 border-2 border-purple-500/30">
                                        <div className="text-center mb-4">
                                            <div className="text-6xl mb-2">⚡</div>
                                            <h3 className="text-2xl font-bold text-purple-300">BOSS TUẦN</h3>
                                            <p className="text-sm text-pink-300 mt-2">Phần thưởng x10 Vàng!</p>
                                        </div>
                                        <div className="bg-black/30 rounded-lg p-3 mb-4">
                                            <p className="text-center">Lượt còn lại: <span className="font-bold text-yellow-400">{player.weeklyBosses}/3</span></p>
                                        </div>
                                        <button
                                            onClick={() => startBattle('weekly')}
                                            disabled={player.weeklyBosses <= 0}
                                            className={`w-full py-4 rounded-xl font-bold text-lg shadow-lg transform transition-all ${
                                                player.weeklyBosses > 0
                                                    ? 'bg-gradient-to-r from-purple-500 to-pink-600 hover:from-purple-600 hover:to-pink-700 hover:scale-105'
                                                    : 'bg-gray-600 cursor-not-allowed opacity-50'
                                            }`}
                                        >
                                            {player.weeklyBosses > 0 ? '⚔️ THÁCH ĐẤU' : '❌ Hết lượt'}
                                        </button>
                                    </div>
                                </div>
                            </div>
                        )}

                        {/* ADS VIEW */}
                        {currentView === 'ads' && (
                            <div className="max-w-4xl mx-auto">
                                <h2 className="text-3xl font-bold mb-6 text-center bg-gradient-to-r from-green-400 to-blue-500 bg-clip-text text-transparent">
                                    📺 XEM QUẢNG CÁO NHẬN THƯỞNG
                                </h2>
                                
                                <div className="bg-yellow-900/30 border-2 border-yellow-500/50 rounded-xl p-4 mb-6">
                                    <p className="text-center text-yellow-300">
                                        ⚠️ <strong>DEMO MODE:</strong> Tích hợp Adsterra.com cần backend server thật
                                    </p>
                                </div>

                                <div className="space-y-4">
                                    {/* Stat Boosts */}
                                    <div className="bg-gradient-to-br from-purple-900/50 to-blue-900/50 rounded-xl p-6 border-2 border-purple-500/30">
                                        <h3 className="text-xl font-bold mb-4">⚡ BUFF STATS (10 phút)</h3>
                                        <div className="grid md:grid-cols-3 gap-4">
                                            {[
                                                { type: 'hp', label: '+100 HP', icon: '❤️', color: 'from-red-500 to-pink-600' },
                                                { type: 'atk', label: '+75 ATK', icon: '⚔️', color: 'from-orange-500 to-red-600' },
                                                { type: 'def', label: '+10 DEF', icon: '🛡️', color: 'from-blue-500 to-purple-600' }
                                            ].map(boost => (
                                                <button
                                                    key={boost.type}
                                                    onClick={() => watchAd(boost.type)}
                                                    disabled={adBoosts[boost.type].active && Date.now() < adBoosts[boost.type].endTime}
                                                    className={`py-4 rounded-xl font-bold bg-gradient-to-r ${boost.color} hover:scale-105 transform transition-all ${
                                                        adBoosts[boost.type].active && Date.now() < adBoosts[boost.type].endTime ? 'opacity-50 cursor-not-allowed' : ''
                                                    }`}
                                                >
                                                    <div className="text-2xl mb-1">{boost.icon}</div>
                                                    <div>{boost.label}</div>
                                                    {adBoosts[boost.type].active && Date.now() < adBoosts[boost.type].endTime && (
                                                        <div className="text-xs mt-1">⏳ Đang hoạt động</div>
                                                    )}
                                                </button>
                                            ))}
                                        </div>
                                    </div>

                                    {/* Coin Rewards */}
                                    <div className="bg-gradient-to-br from-yellow-900/50 to-orange-900/50 rounded-xl p-6 border-2 border-yellow-500/30">
                                        <h3 className="text-xl font-bold mb-4">💰 NHẬN VÀNG</h3>
                                        <div className="grid md:grid-cols-2 gap-4">
                                            <button
                                                onClick={() => watchAd('coin50')}
                                                className="py-4 rounded-xl font-bold bg-gradient-to-r from-yellow-500 to-orange-600 hover:scale-105 transform transition-all"
                                            >
                                                <div className="text-2xl mb-1">💰</div>
                                                <div>+50 Vàng</div>
                                                <div className="text-xs mt-1">(1 QC)</div>
                                            </button>
                                            <button
                                                onClick={() => watchAd('coin100')}
                                                className="py-4 rounded-xl font-bold bg-gradient-to-r from-yellow-500 to-orange-600 hover:scale-105 transform transition-all"
                                            >
                                                <div className="text-2xl mb-1">💎</div>
                                                <div>+100 Vàng</div>
                                                <div className="text-xs mt-1">(2 QC)</div>
                                            </button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        )}

                        {/* MARKET VIEW */}
                        {currentView === 'market' && (
                            <div className="max-w-4xl mx-auto">
                                <h2 className="text-3xl font-bold mb-6 text-center bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
                                    🏪 CHỢ TRADE & GIAO DỊCH
                                </h2>
                                
                                <div className="bg-yellow-900/30 border-2 border-yellow-500/50 rounded-xl p-4 mb-6">
                                    <p className="text-center text-yellow-300">
                                        ⚠️ <strong>DEMO MODE:</strong> Chợ multiplayer thật cần backend server + database
                                    </p>
                                </div>

                                <div className="grid md:grid-cols-2 gap-6">
                                    {/* Market Listings */}
                                    <div className="bg-gradient-to-br from-purple-900/50 to-blue-900/50 rounded-xl p-6 border-2 border-purple-500/30">
                                        <h3 className="text-xl font-bold mb-4">📦 Hàng Đang Bán</h3>
                                        <div className="space-y-2">
                                            {marketListings.length === 0 ? (
                                                <p className="text-center text-purple-300 py-8">Chưa có hàng nào</p>
                                            ) : (
                                                marketListings.map((item, i) => (
                                                    <div key={i} className="bg-black/30 p-3 rounded-lg">
                                                        <div className="flex justify-between items-center">
                                                            <span>{item.name}</span>
                                                            <button className="px-3 py-1 bg-green-600 rounded-lg text-sm">
                                                                💰 {item.price}
                                                            </button>
                                                        </div>
                                                    </div>
                                                ))
                                            )}
                                        </div>
                                    </div>

                                    {/* Trade */}
                                    <div className="bg-gradient-to-br from-pink-900/50 to-purple-900/50 rounded-xl p-6 border-2 border-pink-500/30">
                                        <h3 className="text-xl font-bold mb-4">🤝 Trade Trực Tiếp</h3>
                                        <div className="space-y-4">
                                            <input
                                                type="text"
                                                value={tradeTarget}
                                                onChange={(e) => setTradeTarget(e.target.value)}
                                                placeholder="Nhập tên người chơi..."
                                                className="w-full px-4 py-3 bg-black/30 border-2 border-pink-500/50 rounded-xl focus:border-pink-400 focus:outline-none"
                                            />
                                            <button className="w-full py-3 bg-gradient-to-r from-pink-500 to-purple-600 hover:from-pink-600 hover:to-purple-700 rounded-xl font-bold">
                                                🔍 Tìm Người Chơi
                                            </button>
                                            <p className="text-sm text-purple-300 text-center">
                                                Cần backend để kết nối với người chơi khác
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        )}

                        {/* WITHDRAW VIEW */}
                        {currentView === 'withdraw' && (
                            <div className="max-w-4xl mx-auto">
                                <h2 className="text-3xl font-bold mb-6 text-center bg-gradient-to-r from-green-400 to-emerald-500 bg-clip-text text-transparent">
                                    💵 RÚT TIỀN
                                </h2>
                                
                                <div className="bg-red-900/30 border-2 border-red-500/50 rounded-xl p-4 mb-6">
                                    <p className="text-center text-red-300 font-bold">
                                        ⚠️ CẢNH BÁO: Tính năng này CHỈ LÀ GIAO DIỆN DEMO
                                    </p>
                                    <p className="text-center text-red-200 text-sm mt-2">
                                        Rút tiền thật cần: Giấy phép kinh doanh, Backend server bảo mật, Tích hợp Payment Gateway hợp pháp
                                    </p>
                                </div>

                                <div className="grid md:grid-cols-3 gap-4">
                                    {[
                                        { method: 'bank', label: 'Ngân Hàng', icon: '🏦', min: '20K' },
                                        { method: 'momo', label: 'MoMo', icon: '📱', min: '20K' },
                                        { method: 'card', label: 'Thẻ Cào', icon: '🎫', min: '10K' }
                                    ].map(item => (
                                        <button
                                            key={item.method}
                                            onClick={() => {
                                                alert(`DEMO: Chức năng rút ${item.label} cần backend thật. Min: ${item.min}`);
                                            }}
                                            className="bg-gradient-to-br from-green-900/50 to-emerald-900/50 rounded-xl p-6 border-2 border-green-500/30 hover:border-green-400 hover:scale-105 transition-all"
                                        >
                                            <div className="text-5xl mb-2">{item.icon}</div>
                                            <h3 className="font-bold">{item.label}</h3>
                                            <p className="text-sm text-green-300">Min: {item.min}</p>
                                        </button>
                                    ))}
                                </div>
                            </div>
                        )}
                    </div>

                    {/* Footer */}
                    <div className="bg-black/50 border-t border-purple-500/30 mt-8 py-4">
                        <p className="text-center text-purple-300 text-sm">
                            ⚔️ RPG Online Game • Made with ❤️ • Demo Version
                        </p>
                    </div>
                </div>
            );
        };

        // Initialize Lucide icons
        lucide.createIcons();

        // Render app
        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<RPGGame />);
    </script>
</body>
</html>
