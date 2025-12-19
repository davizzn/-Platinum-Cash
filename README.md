<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manual Completo: Como Vender na Kiwify - Guia 2024</title>
    
    <!-- Meta Tags -->
    <meta name="description" content="Guia completo passo a passo para vender produtos digitais na Kiwify. Do zero às primeiras vendas em 7 dias.">
    <meta name="keywords" content="kiwify tutorial, vender produtos digitais, marketing digital, renda online, como usar kiwify">
    
    <!-- Fontes -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- Ícones -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Reset e Variáveis */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary-color: #2563eb;
            --secondary-color: #3b82f6;
            --accent-color: #1d4ed8;
            --text-color: #1f2937;
            --light-color: #f8fafc;
            --gray-color: #64748b;
            --success-color: #10b981;
            --warning-color: #f59e0b;
            --danger-color: #ef4444;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            --radius: 8px;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            color: var(--text-color);
            line-height: 1.6;
            background-color: var(--light-color);
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            margin-bottom: 1rem;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        .header {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
            padding: 80px 20px;
            text-align: center;
            margin-bottom: 60px;
        }
        
        .header h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }
        
        .header-subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
        }
        
        /* Card */
        .card {
            background: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            padding: 30px;
            margin-bottom: 30px;
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        /* Tabelas */
        .table-container {
            overflow-x: auto;
            margin: 30px 0;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        th {
            background-color: var(--primary-color);
            color: white;
            padding: 15px;
            text-align: left;
        }
        
        td {
            padding: 15px;
            border-bottom: 1px solid #e5e7eb;
        }
        
        tr:nth-child(even) {
            background-color: #f9fafb;
        }
        
        /* Listas */
        .checklist {
            list-style: none;
            margin: 20px 0;
        }
        
        .checklist li {
            padding: 10px 0;
            padding-left: 35px;
            position: relative;
        }
        
        .checklist li:before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--success-color);
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        /* Tabs */
        .tabs {
            display: flex;
            flex-wrap: wrap;
            margin: 40px 0;
            border-bottom: 2px solid #e5e7eb;
        }
        
        .tab {
            padding: 15px 30px;
            background: none;
            border: none;
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--gray-color);
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .tab:hover {
            color: var(--primary-color);
        }
        
        .tab.active {
            color: var(--primary-color);
        }
        
        .tab.active:after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100%;
            height: 3px;
            background-color: var(--primary-color);
        }
        
        .tab-content {
            display: none;
            padding: 30px 0;
            animation: fadeIn 0.5s ease;
        }
        
        .tab-content.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Vídeo Container */
        .video-container {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 */
            height: 0;
            overflow: hidden;
            border-radius: var(--radius);
            margin: 30px 0;
            background: #000;
        }
        
        .video-container iframe,
        .video-container video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* Upload Area */
        .upload-area {
            border: 3px dashed #cbd5e1;
            border-radius: var(--radius);
            padding: 60px 20px;
            text-align: center;
            margin: 30px 0;
            cursor: pointer;
            transition: all 0.3s ease;
            background: #f8fafc;
        }
        
        .upload-area:hover {
            border-color: var(--primary-color);
            background: #eff6ff;
        }
        
        .upload-area i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        /* Botões */
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--primary-color);
            color: white;
            border: none;
            border-radius: var(--radius);
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .btn:hover {
            background: var(--accent-color);
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background: #64748b;
        }
        
        .btn-secondary:hover {
            background: #475569;
        }
        
        /* Alertas */
        .alert {
            padding: 20px;
            border-radius: var(--radius);
            margin: 20px 0;
            border-left: 4px solid;
        }
        
        .alert-info {
            background-color: #dbeafe;
            border-color: var(--primary-color);
            color: #1e40af;
        }
        
        .alert-success {
            background-color: #d1fae5;
            border-color: var(--success-color);
            color: #065f46;
        }
        
        .alert-warning {
            background-color: #fef3c7;
            border-color: var(--warning-color);
            color: #92400e;
        }
        
        /* Progress Bar */
        .progress-bar {
            height: 8px;
            background: #e5e7eb;
            border-radius: 4px;
            margin: 20px 0;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            background: var(--primary-color);
            width: 0%;
            transition: width 1s ease;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .tab {
                padding: 12px 20px;
                font-size: 1rem;
                flex: 1 0 auto;
            }
            
            .card {
                padding: 20px;
            }
        }
        
        /* Navegação */
        .nav-toc {
            position: sticky;
            top: 20px;
            background: white;
            border-radius: var(--radius);
            padding: 20px;
            box-shadow: var(--shadow);
            margin-bottom: 30px;
        }
        
        .nav-toc h3 {
            margin-bottom: 15px;
            color: var(--primary-color);
        }
        
        .nav-toc ul {
            list-style: none;
        }
        
        .nav-toc li {
            margin-bottom: 10px;
        }
        
        .nav-toc a {
            color: var(--text-color);
            text-decoration: none;
            padding: 5px 0;
            display: block;
            transition: color 0.3s ease;
        }
        
        .nav-toc a:hover {
            color: var(--primary-color);
        }
        
        /* Contador de Tempo */
        .timer {
            display: inline-flex;
            align-items: center;
            background: #1e293b;
            color: white;
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 600;
            margin: 10px 0;
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background: white;
            padding: 30px;
            border-radius: var(--radius);
            max-width: 800px;
            width: 90%;
            max-height: 90vh;
            overflow-y: auto;
        }
        
        .close-modal {
            float: right;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--gray-color);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <h1><i class="fas fa-graduation-cap"></i> Manual Completo Kiwify 2024</h1>
            <p class="header-subtitle">Guia definitivo passo a passo para vender produtos digitais e criar uma máquina de vendas automática</p>
            <div style="margin-top: 30px;">
                <span class="timer"><i class="fas fa-clock"></i> Tempo de implementação: 7 dias</span>
            </div>
        </div>
    </header>

    <!-- Tabs Navigation -->
    <div class="container">
        <div class="tabs" id="mainTabs">
            <button class="tab active" data-tab="video">🎥 Vídeo Tutorial</button>
            <button class="tab" data-tab="setup">⚙️ Configuração Inicial</button>
            <button class="tab" data-tab="products">📦 Criar Produtos</button>
            <button class="tab" data-tab="payments">💰 Sistema de Pagamentos</button>
            <button class="tab" data-tab="marketing">🚀 Estratégias de Marketing</button>
            <button class="tab" data-tab="automation">🤖 Automação Completa</button>
            <button class="tab" data-tab="scaling">📈 Escalando Vendas</button>
        </div>
    </div>

    <!-- TAB 1: VÍDEO TUTORIAL -->
    <section class="container">
        <div id="video-tab" class="tab-content active">
            <div class="card">
                <h2><i class="fas fa-video card-icon"></i> Área de Vídeos Exclusivos</h2>
                <p>Adicione seus vídeos tutoriais, demonstrações de produto ou depoimentos nesta seção.</p>
                
                <!-- Player de Vídeo Principal -->
                <div class="video-container">
                    <!-- COLE AQUI SEU LINK DO YOUTUBE/VIMEO -->
                    <iframe src="https://www.youtube.com/embed/SEU_VIDEO_ID" 
                            frameborder="0" 
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                            allowfullscreen>
                    </iframe>
                </div>
                
                <div class="alert alert-info">
                    <i class="fas fa-info-circle"></i> <strong>Instruções:</strong> 
                    Substitua o link acima pelo seu vídeo do YouTube ou Vimeo. Para vídeos locais, use a tag &lt;video&gt; abaixo.
                </div>
                
                <!-- Upload de Vídeo Local -->
                <div class="upload-area" id="uploadTrigger">
                    <i class="fas fa-cloud-upload-alt"></i>
                    <h3>Clique para adicionar seu vídeo</h3>
                    <p>Arraste e solte ou clique para fazer upload</p>
                    <p style="color: var(--gray-color); font-size: 0.9rem; margin-top: 10px;">
                        Formatos suportados: MP4, WebM, OGG (Máx: 100MB)
                    </p>
                </div>
                
                <!-- Player para Vídeo Local (Oculto inicialmente) -->
                <div class="video-container" id="localVideoPlayer" style="display: none;">
                    <video id="localVideo" controls>
                        <source src="" type="video/mp4">
                        Seu navegador não suporta vídeos HTML5.
                    </video>
                </div>
                
                <!-- Lista de Vídeos -->
                <h3 style="margin-top: 40px;">Playlist de Tutoriais</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr>
                                <th>#</th>
                                <th>Título do Vídeo</th>
                                <th>Duração</th>
                                <th>Status</th>
                                <th>Ação</th>
                            </tr>
                        </thead>
                        <tbody id="videoPlaylist">
                            <!-- Vídeos serão adicionados dinamicamente -->
                            <tr>
                                <td>1</td>
                                <td><i class="fas fa-play-circle"></i> Como Criar Conta na Kiwify</td>
                                <td>05:23</td>
                                <td><span style="color: var(--success-color);">✔ Disponível</span></td>
                                <td><button class="btn" onclick="playVideo('video1')">Assistir</button></td>
                            </tr>
                            <tr>
                                <td>2</td>
                                <td><i class="fas fa-play-circle"></i> Configuração de Produtos Passo a Passo</td>
                                <td>12:45</td>
                                <td><span style="color: var(--warning-color);">Em breve</span></td>
                                <td><button class="btn btn-secondary" disabled>Em breve</button></td>
                            </tr>
                            <tr>
                                <td>3</td>
                                <td><i class="fas fa-play-circle"></i> Estratégias de Precificação</td>
                                <td>08:17</td>
                                <td><span style="color: var(--warning-color);">Em breve</span></td>
                                <td><button class="btn btn-secondary" disabled>Em breve</button></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <!-- Controles de Vídeo -->
                <div style="margin-top: 30px; display: flex; gap: 10px; flex-wrap: wrap;">
                    <button class="btn" onclick="addVideo()">
                        <i class="fas fa-plus"></i> Adicionar Novo Vídeo
                    </button>
                    <button class="btn btn-secondary" onclick="showUploadModal()">
                        <i class="fas fa-upload"></i> Upload em Massa
                    </button>
                    <button class="btn btn-secondary" onclick="organizePlaylist()">
                        <i class="fas fa-sort"></i> Organizar Playlist
                    </button>
                </div>
            </div>
            
            <!-- Estatísticas de Visualização -->
            <div class="card">
                <h3><i class="fas fa-chart-bar"></i> Estatísticas dos Vídeos</h3>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 20px;">
                    <div style="text-align: center; padding: 20px; background: #f0f9ff; border-radius: var(--radius);">
                        <div style="font-size: 2rem; font-weight: bold; color: var(--primary-color);">1,247</div>
                        <div style="color: var(--gray-color);">Visualizações</div>
                    </div>
                    <div style="text-align: center; padding: 20px; background: #f0f9ff; border-radius: var(--radius);">
                        <div style="font-size: 2rem; font-weight: bold; color: var(--success-color);">68%</div>
                        <div style="color: var(--gray-color);">Taxa de Conclusão</div>
                    </div>
                    <div style="text-align: center; padding: 20px; background: #f0f9ff; border-radius: var(--radius);">
                        <div style="font-size: 2rem; font-weight: bold; color: var(--warning-color);">12:45</div>
                        <div style="color: var(--gray-color);">Tempo Médio</div>
                    </div>
                    <div style="text-align: center; padding: 20px; background: #f0f9ff; border-radius: var(--radius);">
                        <div style="font-size: 2rem; font-weight: bold; color: var(--accent-color);">87%</div>
                        <div style="color: var(--gray-color);">Satisfação</div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- TAB 2: CONFIGURAÇÃO INICIAL -->
        <div id="setup-tab" class="tab-content">
            <div class="card">
                <h2><i class="fas fa-cogs card-icon"></i> Configuração Inicial da Kiwify</h2>
                
                <div class="alert alert-success">
                    <i class="fas fa-check-circle"></i> <strong>Passo 1:</strong> Criação da Conta
                </div>
                
                <ol class="checklist">
                    <li>Acesse <a href="https://kiwify.com.br" target="_blank">kiwify.com.br</a></li>
                    <li>Clique em "Começar Agora"</li>
                    <li>Selecione "Sou Produtor"</li>
                    <li>Preencha dados pessoais com CPF válido</li>
                    <li>Use e-mail profissional (não use @gmail.com)</li>
                    <li>Cadastre número de telefone para verificação</li>
                    <li>Ative autenticação de dois fatores (2FA)</li>
                </ol>
                
                <h3>Configuração do Perfil da Loja</h3>
                <table>
                    <tr>
                        <th>Configuração</th>
                        <th>Recomendação</th>
                        <th>Exemplo</th>
                    </tr>
                    <tr>
                        <td>Nome da Loja</td>
                        <td>Curto, memorável, relacionado ao nicho</td>
                        <td>PlatinumStore, ExpertDigital, MestreIA</td>
                    </tr>
                    <tr>
                        <td>Logo</td>
                        <td>500x500px, PNG com fundo transparente</td>
                        <td>Use Canva para criar gratuitamente</td>
                    </tr>
                    <tr>
                        <td>Descrição</td>
                        <td>Clara, com palavras-chave, máximo 200 caracteres</td>
                        <td>"Sistema de renda automática 100% digital"</td>
                    </tr>
                    <tr>
                        <td>Cores</td>
                        <td>Máximo 2 cores principais + branco</td>
                        <td>Preto/Dourado, Azul/Branco, Verde/Preto</td>
                    </tr>
                </table>
                
                <h3>Configuração Bancária</h3>
                <div class="alert alert-warning">
                    <i class="fas fa-exclamation-triangle"></i> <strong>Atenção:</strong> Use conta específica para negócios
                </div>
                
                <ul class="checklist">
                    <li>Conta corrente ou poupança pessoal</li>
                    <li>CPF deve ser o mesmo do titular da conta</li>
                    <li>Evite contas conjuntas</li>
                    <li>Saques processados em D+2 úteis</li>
                    <li>Primeiro saque pode levar 7-10 dias</li>
                </ul>
            </div>
        </div>
        
        <!-- Modal para Upload de Vídeos -->
        <div id="videoModal" class="modal">
            <div class="modal-content">
                <button class="close-modal" onclick="closeModal()">&times;</button>
                <h2><i class="fas fa-upload"></i> Upload de Múltiplos Vídeos</h2>
                
                <div class="upload-area" style="min-height: 200px;" id="modalUploadArea">
                    <i class="fas fa-file-video"></i>
                    <h3>Arraste e solte seus vídeos aqui</h3>
                    <p>ou clique para selecionar</p>
                    <input type="file" id="multiVideoUpload" multiple accept="video/*" style="display: none;">
                </div>
                
                <div id="uploadProgress" style="display: none;">
                    <h4>Progresso do Upload:</h4>
                    <div class="progress-bar">
                        <div class="progress-fill" id="uploadProgressFill"></div>
                    </div>
                    <p id="uploadStatus"></p>
                </div>
                
                <div style="margin-top: 20px;">
                    <button class="btn" onclick="startUpload()">
                        <i class="fas fa-cloud-upload-alt"></i> Iniciar Upload
                    </button>
                    <button class="btn btn-secondary" onclick="closeModal()">
                        Cancelar
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Navegação TOC -->
    <div class="container">
        <div class="nav-toc">
            <h3><i class="fas fa-list"></i> Navegação Rápida</h3>
            <ul>
                <li><a href="#video-tab" onclick="switchTab('video')">🎥 Vídeo Tutorial</a></li>
                <li><a href="#setup-tab" onclick="switchTab('setup')">⚙️ Configuração Inicial</a></li>
                <li><a href="#products-tab" onclick="switchTab('products')">📦 Criar Produtos</a></li>
                <li><a href="#payments-tab" onclick="switchTab('payments')">💰 Sistema de Pagamentos</a></li>
                <li><a href="#marketing-tab" onclick="switchTab('marketing')">🚀 Estratégias de Marketing</a></li>
                <li><a href="#automation-tab" onclick="switchTab('automation')">🤖 Automação Completa</a></li>
                <li><a href="#scaling-tab" onclick="switchTab('scaling')">📈 Escalando Vendas</a></li>
            </ul>
        </div>
    </div>

    <script>
        // Sistema de Tabs
        function switchTab(tabName) {
            // Remove active class from all tabs and contents
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            document.querySelectorAll('.tab-content').forEach(content => {
                content.classList.remove('active');
            });
            
            // Add active class to selected tab and content
            document.querySelector(`[data-tab="${tabName}"]`).classList.add('active');
            document.getElementById(`${tabName}-tab`).classList.add('active');
            
            // Scroll to top of tab content
            document.getElementById(`${tabName}-tab`).scrollIntoView({ behavior: 'smooth' });
        }
        
        // Add event listeners to tabs
        document.querySelectorAll('.tab').forEach(tab => {
            tab.addEventListener('click', () => {
                const tabName = tab.getAttribute('data-tab');
                switchTab(tabName);
            });
        });
        
        // Upload de Vídeo Local
        document.getElementById('uploadTrigger').addEventListener('click', function() {
            const input = document.createElement('input');
            input.type = 'file';
            input.accept = 'video/*';
            
            input.onchange = function(e) {
                const file = e.target.files[0];
                if (file) {
                    if (file.size > 100 * 1024 * 1024) { // 100MB limit
                        alert('Arquivo muito grande! Máximo 100MB.');
                        return;
                    }
                    
                    const videoPlayer = document.getElementById('localVideoPlayer');
                    const video = document.getElementById('localVideo');
                    
                    const videoURL = URL.createObjectURL(file);
                    video.src = videoURL;
                    videoPlayer.style.display = 'block';
                    
                    // Add to playlist
                    addToPlaylist(file.name, videoURL);
                }
            };
            
            input.click();
        });
        
        // Modal Functions
        function showUploadModal() {
            document.getElementById('videoModal').style.display = 'flex';
        }
        
        function closeModal() {
            document.getElementById('videoModal').style.display = 'none';
        }
        
        // Play Video Function
        function playVideo(videoId) {
            alert('Função playVideo: ' + videoId + '\nImplemente a lógica para trocar o vídeo principal.');
            // Aqui você implementaria a lógica para trocar o vídeo no player principal
        }
        
        // Add Video to Playlist
        function addVideo() {
            const playlist = document.getElementById('videoPlaylist');
            const newRow = document.createElement('tr');
            const rowNumber = playlist.children.length + 1;
            
            newRow.innerHTML = `
                <td>${rowNumber}</td>
                <td><i class="fas fa-play-circle"></i> Novo Vídeo ${rowNumber}</td>
                <td>00:00</td>
                <td><span style="color: var(--warning-color);">Não publicado</span></td>
                <td><button class="btn" onclick="editVideo(${rowNumber})">Editar</button></td>
            `;
            
            playlist.appendChild(newRow);
        }
        
        function addToPlaylist(filename, url) {
            const playlist = document.getElementById('videoPlaylist');
            const newRow = document.createElement('tr');
            const rowNumber = playlist.children.length + 1;
            
            newRow.innerHTML = `
                <td>${rowNumber}</td>
                <td><i class="fas fa-play-circle"></i> ${filename}</td>
                <td>--:--</td>
                <td><span style="color: var(--success-color);">Carregado</span></td>
                <td>
                    <button class="btn" onclick="playLocalVideo('${url}')">Assistir</button>
                    <button class="btn btn-secondary" onclick="removeVideo(this)">Remover</button>
                </td>
            `;
            
            playlist.appendChild(newRow);
        }
        
        function playLocalVideo(url) {
            const videoPlayer = document.getElementById('localVideoPlayer');
            const video = document.getElementById('localVideo');
            
            video.src = url;
            videoPlayer.style.display = 'block';
            video.play();
        }
        
        function removeVideo(button) {
            const row = button.closest('tr');
            row.remove();
            
            // Renumber rows
            const playlist = document.getElementById('videoPlaylist');
            const rows = playlist.getElementsByTagName('tr');
            for (let i = 0; i < rows.length; i++) {
                rows[i].cells[0].textContent = i + 1;
            }
        }
        
        function editVideo(rowNumber) {
            alert(`Editando vídeo ${rowNumber}\nImplemente a lógica de edição aqui.`);
        }
        
        function organizePlaylist() {
            alert('Funcionalidade de organização da playlist.\nImplemente arrastar e soltar se necessário.');
        }
        
        // Upload Simulation
        function startUpload() {
            const progressBar = document.getElementById('uploadProgressFill');
            const progressContainer = document.getElementById('uploadProgress');
            const statusText = document.getElementById('uploadStatus');
            
            progressContainer.style.display = 'block';
            let progress = 0;
            
            const interval = setInterval(() => {
                progress += 10;
                progressBar.style.width = progress + '%';
                statusText.textContent = `Uploading... ${progress}%`;
                
                if (progress >= 100) {
                    clearInterval(interval);
                    statusText.textContent = 'Upload completo!';
                    setTimeout(() => {
                        closeModal();
                        progressContainer.style.display = 'none';
                        progressBar.style.width = '0%';
                    }, 1000);
                }
            }, 300);
        }
        
        // Modal Upload Area Click
        document.getElementById('modalUploadArea').addEventListener('click', function() {
            document.getElementById('multiVideoUpload').click();
        });
        
        // Close modal on outside click
        window.onclick = function(event) {
            const modal = document.getElementById('videoModal');
            if (event.target == modal) {
                closeModal();
            }
        }
        
        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            // Set first tab as active
            switchTab('video');
        });
    </script>
</body>
</html>
