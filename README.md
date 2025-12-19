<!-- ARQUIVO SEPARADO: pagamento.html -->
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagamento via Pix - Platinum Store</title>
    
    <!-- Fontes -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Ícones -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    
    <style>
        :root {
            --pix-green: #32BB6F;
            --pix-green-dark: #2AA65C;
            --dark: #1A1A1A;
            --light: #FFFFFF;
            --gray: #6B7280;
            --radius: 12px;
            --shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
            color: var(--dark);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .payment-container {
            max-width: 500px;
            width: 100%;
            background: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            overflow: hidden;
        }
        
        .payment-header {
            background: linear-gradient(135deg, var(--pix-green) 0%, var(--pix-green-dark) 100%);
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        .payment-header h1 {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 10px;
        }
        
        .payment-content {
            padding: 40px;
        }
        
        .order-summary {
            background: #f8fafc;
            border-radius: var(--radius);
            padding: 25px;
            margin-bottom: 30px;
            border-left: 4px solid var(--pix-green);
        }
        
        .order-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e5e7eb;
        }
        
        .order-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        .order-label {
            font-weight: 600;
            color: var(--gray);
        }
        
        .order-value {
            font-weight: 700;
            color: var(--dark);
        }
        
        .total-value {
            font-size: 1.5rem;
            color: var(--pix-green);
        }
        
        /* QR Code Section */
        .qr-section {
            text-align: center;
            margin: 40px 0;
            padding: 30px;
            background: #f0fdf4;
            border-radius: var(--radius);
            border: 2px dashed var(--pix-green);
        }
        
        .qr-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--pix-green);
            margin-bottom: 20px;
        }
        
        .qr-code-container {
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: var(--radius);
            display: inline-block;
            border: 2px solid #e5e7eb;
        }
        
        .qr-code {
            width: 250px;
            height: 250px;
            display: block;
            margin: 0 auto;
        }
        
        /* CPF Section */
        .cpf-section {
            background: #f8fafc;
            border-radius: var(--radius);
            padding: 25px;
            margin: 30px 0;
            text-align: center;
        }
        
        .cpf-label {
            font-size: 0.9rem;
            color: var(--gray);
            margin-bottom: 10px;
            display: block;
        }
        
        .cpf-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--dark);
            font-family: 'Courier New', monospace;
            letter-spacing: 1px;
            padding: 15px;
            background: white;
            border-radius: var(--radius);
            border: 2px solid #e5e7eb;
            margin: 10px 0;
            word-break: break-all;
        }
        
        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 16px 30px;
            border: none;
            border-radius: var(--radius);
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            width: 100%;
            margin: 10px 0;
        }
        
        .btn-primary {
            background: var(--pix-green);
            color: white;
        }
        
        .btn-primary:hover {
            background: var(--pix-green-dark);
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background: #f3f4f6;
            color: var(--dark);
        }
        
        .btn-secondary:hover {
            background: #e5e7eb;
        }
        
        /* Instructions */
        .instructions {
            background: #fef3c7;
            border-radius: var(--radius);
            padding: 25px;
            margin: 30px 0;
            border-left: 4px solid #f59e0b;
        }
        
        .instructions h4 {
            color: #92400e;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions ol {
            margin-left: 20px;
            color: #92400e;
        }
        
        .instructions li {
            margin-bottom: 10px;
        }
        
        /* Timer */
        .timer {
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background: white;
            border-radius: var(--radius);
            border: 2px solid var(--pix-green);
        }
        
        .timer-title {
            font-size: 1rem;
            color: var(--gray);
            margin-bottom: 10px;
        }
        
        .timer-display {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--pix-green);
            font-family: 'Courier New', monospace;
            margin: 15px 0;
        }
        
        .timer-warning {
            font-size: 0.9rem;
            color: #ef4444;
            margin-top: 10px;
        }
        
        /* Success Message */
        .success-message {
            display: none;
            background: #d1fae5;
            border-radius: var(--radius);
            padding: 30px;
            margin: 30px 0;
            text-align: center;
            border: 2px solid #10b981;
        }
        
        .success-message.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .payment-content {
                padding: 25px;
            }
            
            .qr-code {
                width: 200px;
                height: 200px;
            }
            
            .cpf-value {
                font-size: 1.4rem;
                padding: 12px;
            }
        }
    </style>
</head>
<body>
    <div class="payment-container">
        <div class="payment-header">
            <h1><i class="fas fa-lock"></i> PAGAMENTO SEGURO</h1>
            <p>Finalize sua compra via Pix</p>
        </div>
        
        <div class="payment-content">
            <!-- Resumo do Pedido -->
            <div class="order-summary">
                <div class="order-item">
                    <span class="order-label">Produto:</span>
                    <span class="order-value" id="productName">Método Platinum</span>
                </div>
                <div class="order-item">
                    <span class="order-label">Valor:</span>
                    <span class="order-value total-value" id="productPrice">R$ 97,00</span>
                </div>
                <div class="order-item">
                    <span class="order-label">Pedido:</span>
                    <span class="order-value" id="orderId">#PIX001</span>
                </div>
            </div>
            
            <!-- Timer -->
            <div class="timer">
                <div class="timer-title">Tempo restante para pagamento:</div>
                <div class="timer-display" id="paymentTimer">15:00</div>
                <div class="timer-warning">
                    <i class="fas fa-exclamation-circle"></i>
                    Após este tempo, o pedido será cancelado
                </div>
            </div>
            
            <!-- QR Code -->
            <div class="qr-section">
                <div class="qr-title">
                    <i class="fas fa-qrcode"></i> ESCANEIE O QR CODE
                </div>
                <p>Use a câmera do seu banco para escanear</p>
                
                <div class="qr-code-container">
                    <!-- SUA IMAGEM DO QR CODE AQUI -->
                    <img src="SEU_QR_CODE_AQUI.jpg" alt="QR Code Pix" class="qr-code" id="qrCodeImage">
                    <div style="text-align: center; padding: 20px; display: none;" id="qrPlaceholder">
                        <i class="fas fa-qrcode" style="font-size: 4rem; color: #e5e7eb; margin-bottom: 15px;"></i>
                        <p style="color: var(--gray);">QR Code será gerado automaticamente</p>
                    </div>
                </div>
            </div>
            
            <!-- CPF -->
            <div class="cpf-section">
                <span class="cpf-label">OU COPIE A CHAVE PIX (CPF):</span>
                <div class="cpf-value" id="cpfValue">SEU.CPF.AQUI</div>
                <div style="display: flex; gap: 10px; margin-top: 20px;">
                    <button class="btn btn-secondary" onclick="copyToClipboard('cpfValue')">
                        <i class="far fa-copy"></i> Copiar CPF
                    </button>
                    <button class="btn btn-secondary" onclick="copyToClipboard('productPrice')">
                        <i class="far fa-copy"></i> Copiar Valor
                    </button>
                </div>
            </div>
            
            <!-- Instruções -->
            <div class="instructions">
                <h4><i class="fas fa-list-ol"></i> COMO PAGAR:</h4>
                <ol>
                    <li>Abra o app do seu banco</li>
                    <li>Toque em "Pagar com Pix"</li>
                    <li>Escaneie o QR Code ou cole o CPF</li>
                    <li>Confirme o valor e pague</li>
                    <li>Clique em "JÁ PAGUEI" abaixo</li>
                </ol>
            </div>
            
            <!-- Mensagem de Sucesso -->
            <div class="success-message" id="successMessage">
                <i class="fas fa-check-circle" style="font-size: 3rem; color: #10b981; margin-bottom: 20px;"></i>
                <h3 style="color: #065f46; margin-bottom: 15px;">PAGAMENTO CONFIRMADO!</h3>
                <p>Seu produto está sendo processado. Você receberá os dados de acesso em até 5 minutos.</p>
                <button class="btn btn-primary" onclick="goBack()" style="margin-top: 20px;">
                    <i class="fas fa-home"></i> VOLTAR À LOJA
                </button>
            </div>
            
            <!-- Botões de Ação -->
            <div id="actionButtons">
                <button class="btn btn-primary" onclick="confirmPayment()">
                    <i class="fas fa-check-circle"></i> JÁ PAGUEI
                </button>
                <button class="btn btn-secondary" onclick="goBack()">
                    <i class="fas fa-arrow-left"></i> VOLTAR
                </button>
            </div>
        </div>
    </div>

    <script>
        // Obter parâmetros da URL
        const urlParams = new URLSearchParams(window.location.search);
        const produto = urlParams.get('produto') || 'platinum';
        const valor = urlParams.get('valor') || '97';
        
        // Configurar dados do produto
        const produtos = {
            'platinum': { nome: 'Método Platinum', valor: 97 },
            'avancado': { nome: 'Sistema Avançado', valor: 197 },
            'master': { nome: 'Pacote Master', valor: 297 }
        };
        
        const produtoSelecionado = produtos[produto] || produtos['platinum'];
        
        // Atualizar informações na página
        document.getElementById('productName').textContent = produtoSelecionado.nome;
        document.getElementById('productPrice').textContent = `R$ ${produtoSelecionado.valor},00`;
        
        // Gerar ID do pedido
        const orderId = 'PIX' + Math.floor(Math.random() * 10000).toString().padStart(4, '0');
        document.getElementById('orderId').textContent = `#${orderId}`;
        
        // Configurar CPF (SUBSTITUA PELO SEU CPF)
        const cpf = "123.456.789-00"; // SEU CPF AQUI
        document.getElementById('cpfValue').textContent = cpf;
        
        // Timer de pagamento
        let timeLeft = 15 * 60; // 15 minutos em segundos
        let timerInterval;
        
        function startTimer() {
            clearInterval(timerInterval);
            timerInterval = setInterval(() => {
                timeLeft--;
                const minutes = Math.floor(timeLeft / 60);
                const seconds = timeLeft % 60;
                
                document.getElementById('paymentTimer').textContent = 
                    `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    alert('Tempo esgotado! Pedido cancelado.');
                    goBack();
                }
            }, 1000);
        }
        
        // Função para copiar texto
        function copyToClipboard(elementId) {
            const element = document.getElementById(elementId);
            let textToCopy = element.textContent;
            
            // Limpar formatação
            if (elementId === 'cpfValue') {
                textToCopy = textToCopy.replace(/[^\d]/g, '');
            }
            if (elementId === 'productPrice') {
                textToCopy = textToCopy.replace('R$ ', '').replace(',00', '');
            }
            
            navigator.clipboard.writeText(textToCopy).then(() => {
                const originalText = element.textContent;
                element.textContent = 'Copiado! ✓';
                element.style.color = '#32BB6F';
                
                setTimeout(() => {
                    element.textContent = originalText;
                    element.style.color = '';
                }, 2000);
            });
        }
        
        // Confirmar pagamento
        function confirmPayment() {
            clearInterval(timerInterval);
            
            // Mostrar mensagem de sucesso
            document.getElementById('successMessage').classList.add('active');
            document.getElementById('actionButtons').style.display = 'none';
            document.querySelector('.timer').style.display = 'none';
            
            // Salvar no localStorage (opcional)
            localStorage.setItem('lastPayment', JSON.stringify({
                product: produtoSelecionado.nome,
                value: produtoSelecionado.valor,
                date: new Date().toISOString(),
                orderId: orderId
            }));
        }
        
        // Voltar para a loja
        function goBack() {
            window.location.href = 'index.html';
        }
        
        // Inicializar
        document.addEventListener('DOMContentLoaded', function() {
            startTimer();
            
            // Verificar se há imagem de QR Code
            const qrImage = document.getElementById('qrCodeImage');
            if (qrImage.src.includes('SEU_QR_CODE_AQUI')) {
                qrImage.style.display = 'none';
                document.getElementById('qrPlaceholder').style.display = 'block';
            }
        });
    </script>
</body>
</html>
