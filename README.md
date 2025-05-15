<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini City RP - AutoFarm Gari</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .glow {
            text-shadow: 0 0 10px rgba(59, 130, 246, 0.8);
        }
        .btn-hack {
            background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
            transition: all 0.3s ease;
        }
        .btn-hack:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(59, 130, 246, 0.3);
        }
        .terminal {
            background-color: #0f172a;
            font-family: 'Courier New', monospace;
        }
        .progress-bar {
            height: 6px;
            background: linear-gradient(90deg, #3b82f6 0%, #10b981 100%);
            animation: progress 2s ease-in-out infinite;
        }
        @keyframes progress {
            0% { width: 0%; }
            50% { width: 100%; }
            100% { width: 0%; }
        }
    </style>
</head>
<body class="bg-gray-900 text-white min-h-screen">
    <div class="container mx-auto px-4 py-8">
        <!-- Header -->
        <header class="flex justify-between items-center mb-8 border-b border-blue-500 pb-4">
            <div class="flex items-center">
                <i class="fas fa-city text-blue-400 text-3xl mr-3"></i>
                <h1 class="text-2xl font-bold glow">Mini City RP <span class="text-blue-400">AutoFarm Gari</span></h1>
            </div>
            <div class="flex items-center space-x-4">
                <div class="bg-blue-900/50 px-3 py-1 rounded-full text-sm flex items-center">
                    <div class="w-2 h-2 bg-green-400 rounded-full mr-2"></div>
                    <span>Conectado</span>
                </div>
                <button class="bg-red-500 hover:bg-red-600 px-3 py-1 rounded text-sm transition">
                    Sair
                </button>
            </div>
        </header>

        <!-- Main Content -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
            <!-- Left Panel -->
            <div class="lg:col-span-2 space-y-6">
                <!-- Status Panel -->
                <div class="bg-gray-800 rounded-lg p-6 shadow-lg">
                    <h2 class="text-xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-chart-line text-blue-400 mr-2"></i>
                        Status do AutoFarm
                    </h2>
                    
                    <div class="grid grid-cols-2 gap-4 mb-6">
                        <div class="bg-gray-700/50 p-4 rounded-lg">
                            <div class="text-gray-400 text-sm mb-1">Tempo Ativo</div>
                            <div class="text-xl font-mono">02:45:18</div>
                        </div>
                        <div class="bg-gray-700/50 p-4 rounded-lg">
                            <div class="text-gray-400 text-sm mb-1">Gari Coletado</div>
                            <div class="text-xl font-mono">$ 12,450</div>
                        </div>
                        <div class="bg-gray-700/50 p-4 rounded-lg">
                            <div class="text-gray-400 text-sm mb-1">Trabalhos Concluídos</div>
                            <div class="text-xl font-mono">37</div>
                        </div>
                        <div class="bg-gray-700/50 p-4 rounded-lg">
                            <div class="text-gray-400 text-sm mb-1">Velocidade</div>
                            <div class="text-xl font-mono">3.5x</div>
                        </div>
                    </div>

                    <div class="mt-4">
                        <div class="flex justify-between text-sm mb-1">
                            <span>Progresso Atual</span>
                            <span>78%</span>
                        </div>
                        <div class="w-full bg-gray-700 rounded-full h-2.5">
                            <div class="bg-blue-500 h-2.5 rounded-full" style="width: 78%"></div>
                        </div>
                    </div>
                </div>

                <!-- Terminal -->
                <div class="terminal rounded-lg p-6 shadow-lg">
                    <div class="flex justify-between items-center mb-4">
                        <h2 class="text-xl font-semibold flex items-center">
                            <i class="fas fa-terminal text-green-400 mr-2"></i>
                            Log de Atividades
                        </h2>
                        <div class="flex space-x-2">
                            <button class="bg-gray-700 hover:bg-gray-600 px-3 py-1 rounded text-sm transition">
                                Limpar
                            </button>
                            <button class="bg-gray-700 hover:bg-gray-600 px-3 py-1 rounded text-sm transition">
                                Exportar
                            </button>
                        </div>
                    </div>
                    <div class="h-64 overflow-y-auto font-mono text-sm text-gray-300 space-y-2">
                        <div class="text-green-400">[10:23:45] AutoFarm iniciado com sucesso</div>
                        <div class="text-blue-400">[10:23:47] Procurando lixeiras próximas...</div>
                        <div class="text-green-400">[10:23:49] Lixeira encontrada - Rua Principal #12</div>
                        <div class="text-blue-400">[10:23:51] Coletando lixo (Progresso: 25%)</div>
                        <div class="text-green-400">[10:23:53] Lixo coletado! +$350</div>
                        <div class="text-blue-400">[10:23:55] Movendo para próxima localização...</div>
                        <div class="text-green-400">[10:23:58] Lixeira encontrada - Avenida Central #5</div>
                        <div class="text-yellow-400">[10:24:00] Detectado jogador próximo - ativando modo discreto</div>
                        <div class="text-blue-400">[10:24:05] Coletando lixo (Progresso: 65%)</div>
                        <div class="text-green-400">[10:24:07] Lixo coletado! +$420</div>
                        <div class="text-blue-400">[10:24:09] Verificando se há policiais na área...</div>
                        <div class="text-green-400">[10:24:10] Área segura - continuando operação</div>
                        <div class="text-blue-400">[10:24:12] Procurando lixeiras próximas...</div>
                        <div class="text-green-400">[10:24:15] Lixeira encontrada - Parque Municipal</div>
                        <div class="text-blue-400">[10:24:17] Coletando lixo (Progresso: 12%)</div>
                    </div>
                </div>
            </div>

            <!-- Right Panel - Controls -->
            <div class="space-y-6">
                <!-- AutoFarm Controls -->
                <div class="bg-gray-800 rounded-lg p-6 shadow-lg">
                    <h2 class="text-xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-robot text-blue-400 mr-2"></i>
                        Controles
                    </h2>

                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium mb-1">Velocidade</label>
                            <select class="w-full bg-gray-700 border border-gray-600 rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option>1x (Seguro)</option>
                                <option selected>3.5x (Recomendado)</option>
                                <option>5x (Risco Moderado)</option>
                                <option>8x (Alto Risco)</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-sm font-medium mb-1">Modo Anti-Detecção</label>
                            <select class="w-full bg-gray-700 border border-gray-600 rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
                                <option>Desativado</option>
                                <option selected>Básico</option>
                                <option>Avançado</option>
                                <option>Extremo (reduz velocidade)</option>
                            </select>
                        </div>

                        <div class="pt-2">
                            <label class="flex items-center space-x-2">
                                <input type="checkbox" class="form-checkbox text-blue-500 rounded" checked>
                                <span>Auto-reiniciar se desconectado</span>
                            </label>
                        </div>

                        <div>
                            <label class="flex items-center space-x-2">
                                <input type="checkbox" class="form-checkbox text-blue-500 rounded" checked>
                                <span>Evitar áreas policiais</span>
                            </label>
                        </div>

                        <div>
                            <label class="flex items-center space-x-2">
                                <input type="checkbox" class="form-checkbox text-blue-500 rounded">
                                <span>Modo noturno (menos visível)</span>
                            </label>
                        </div>

                        <div class="pt-4">
                            <button class="btn-hack w-full py-3 rounded-lg font-bold flex items-center justify-center space-x-2">
                                <i class="fas fa-play"></i>
                                <span>Iniciar AutoFarm</span>
                            </button>
                        </div>

                        <div>
                            <button class="w-full bg-gray-700 hover:bg-gray-600 py-3 rounded-lg font-bold flex items-center justify-center space-x-2 transition">
                                <i class="fas fa-pause"></i>
                                <span>Pausar</span>
                            </button>
                        </div>

                        <div>
                            <button class="w-full bg-red-500 hover:bg-red-600 py-3 rounded-lg font-bold flex items-center justify-center space-x-2 transition">
                                <i class="fas fa-stop"></i>
                                <span>Parar</span>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Stats -->
                <div class="bg-gray-800 rounded-lg p-6 shadow-lg">
                    <h2 class="text-xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-chart-pie text-blue-400 mr-2"></i>
                        Estatísticas
                    </h2>

                    <div class="space-y-3">
                        <div>
                            <div class="flex justify-between text-sm mb-1">
                                <span>Taxa de Sucesso</span>
                                <span>98.7%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="bg-green-500 h-2 rounded-full" style="width: 98.7%"></div>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between text-sm mb-1">
                                <span>Detecção</span>
                                <span>0.2%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="bg-red-500 h-2 rounded-full" style="width: 0.2%"></div>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between text-sm mb-1">
                                <span>Eficiência</span>
                                <span>92%</span>
                            </div>
                            <div class="w-full bg-gray-700 rounded-full h-2">
                                <div class="bg-yellow-500 h-2 rounded-full" style="width: 92%"></div>
                            </div>
                        </div>
                    </div>

                    <div class="mt-6 pt-4 border-t border-gray-700">
                        <div class="text-center text-sm text-gray-400">
                            <div class="mb-2">Última Atualização: v2.4.1</div>
                            <div class="progress-bar rounded-full"></div>
                            <div class="mt-2">Verificando atualizações...</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer class="mt-12 pt-6 border-t border-gray-800 text-center text-gray-500 text-sm">
            <div class="flex justify-center space-x-6 mb-4">
                <a href="#" class="hover:text-blue-400 transition"><i class="fab fa-discord"></i> Discord</a>
                <a href="#" class="hover:text-blue-400 transition"><i class="fab fa-telegram"></i> Telegram</a>
                <a href="#" class="hover:text-blue-400 transition"><i class="fas fa-globe"></i> Site</a>
            </div>
            <div>
                Mini City RP AutoFarm Gari v2.4.1 | Fins educacionais apenas
            </div>
        </footer>
    </div>

    <script>
        // Simulação de log contínuo
        const terminal = document.querySelector('.terminal div[class*="h-64"]');
        const messages = [
            {text: "Movendo para próxima localização...", color: "text-blue-400"},
            {text: "Lixeira encontrada - Rua das Flores #8", color: "text-green-400"},
            {text: "Coletando lixo (Progresso: 45%)", color: "text-blue-400"},
            {text: "Lixo coletado! +$380", color: "text-green-400"},
            {text: "Verificando se há policiais na área...", color: "text-blue-400"},
            {text: "Área segura - continuando operação", color: "text-green-400"},
        ];

        let messageIndex = 0;
        
        function addLogMessage() {
            if (messageIndex >= messages.length) messageIndex = 0;
            
            const now = new Date();
            const timeString = `[${now.getHours().toString().padStart(2, '0')}:${now.getMinutes().toString().padStart(2, '0')}:${now.getSeconds().toString().padStart(2, '0')}]`;
            
            const messageDiv = document.createElement('div');
            messageDiv.className = messages[messageIndex].color;
            messageDiv.textContent = `${timeString} ${messages[messageIndex].text}`;
            
            terminal.appendChild(messageDiv);
            terminal.scrollTop = terminal.scrollHeight;
            
            messageIndex++;
            
            // Adiciona uma mensagem a cada 3-8 segundos
            setTimeout(addLogMessage, Math.random() * 5000 + 3000);
        }

        // Inicia o log após 2 segundos
        setTimeout(addLogMessage, 2000);

        // Botão de iniciar
        const startBtn = document.querySelector('.btn-hack');
        startBtn.addEventListener('click', function() {
            alert('AutoFarm iniciado! Esta é uma demonstração apenas.');
        });
    </script>
</body>
</html>
