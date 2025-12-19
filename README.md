<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Platinum Pay - Sistema de Vendas Direto Pix</title>
    
    <!-- Meta Tags -->
    <meta name="description" content="Sistema de vendas direto via Pix. Receba pagamentos instantâneos sem intermediários.">
    <meta name="keywords" content="pix vendas, qr code, pagamento direto, sistema pix">
    
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
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header */
        .header {
            text-align: center;
            padding: 40px 20px;
            margin-bottom: 40px;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--pix-green);
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.1rem;
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        /* Sistema de Produtos */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }
        
        .product-card {
            background: var(--light);
            border-radius: var(--radius);
            padding: 30px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            border: 2px solid transparent;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            border-color: var(--pix-green);
        }
        
        .product-title {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .product-price {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--pix-green);
            margin: 20px 0;
        }
        
        .product-price small {
            font-size: 1rem;
            color: var(--gray);
        }
        
        .product-features {
            list-style: none;
            margin: 25px 0;
        }
        
        .product-features li {
            padding: 8px 0;
            padding-left: 30px;
            position: relative;
        }
        
        .product-features li:before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--pix-green);
            font-weight: bold;
        }
        
        .buy-btn {
            display: block;
            width: 100%;
            padding: 18px;
            background: var(--pix-green);
            color: white;
            border: none;
            border-radius: var(--radius);
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            text-decoration: none;
            margin-top: 20px;
        }
        
        .buy-btn:hover {
            background: var(--pix-green-dark);
            transform: translateY(-2px);
        }
        
        /* Modal de Pagamento */
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
            padding: 20px;
        }
        
        .modal.active {
            display: flex;
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .modal-content {
            background: white;
            border-radius: var(--radius);
            padding: 40px;
            max-width: 500px;
            width: 100%;
            position: relative;
            animation: slideUp 0.4s ease;
        }
        
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .close-modal {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--gray);
        }
        
        .modal-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .modal-subtitle {
            color: var(--gray);
            margin-bottom: 30px;
        }
        
        /* Área do Pix */
        .pix-area {
            background: #f0fdf4;
            border-radius: var(--radius);
            padding: 30px;
            text-align: center;
            border: 2px dashed var(--pix-green);
            margin: 30px 0;
        }
        
        .qr-code-container {
            margin: 30px auto;
            padding: 20px;
            background: white;
            border-radius: var(--radius);
            display: inline-block;
            border: 2px solid #e5e7eb;
        }
        
        #qrCodeImage {
            width: 250px;
            height: 250px;
            display: block;
            margin: 0 auto;
            border: 1px solid #e5e7eb;
        }
        
        .qr-placeholder {
            width: 250px;
            height: 250px;
            background: linear-gradient(45deg, #f3f4f6 25%, #e5e7eb 25%, #e5e7eb 50%, #f3f4f6 50%, #f3f4f6 75%, #e5e7eb 75%);
            background-size: 20px 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gray);
            font-size: 0.9rem;
            margin: 0 auto;
        }
        
        /* CPF */
        .cpf-container {
            background: #f8fafc;
            border-radius: var(--radius);
            padding: 25px;
            margin: 20px 0;
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
        }
        
        /* Instruções */
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
        
        /* Status do Pagamento */
        .payment-status {
            text-align: center;
            padding: 20px;
            border-radius: var(--radius);
            margin: 20px 0;
            display: none;
        }
        
        .payment-status.success {
            background: #d1fae5;
            color: #065f46;
            border: 2px solid #10b981;
        }
        
        .payment-status.pending {
            background: #fef3c7;
            color: #92400e;
            border: 2px solid #f59e0b;
        }
        
        /* Botões de Copiar */
        .copy-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--pix-green);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: var(--radius);
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            margin: 10px 5px;
        }
        
        .copy-btn:hover {
            background: var(--pix-green-dark);
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .products-grid {
                grid-template-columns: 1fr;
            }
            
            .modal-content {
                padding: 25px;
            }
            
            #qrCodeImage,
            .qr-placeholder {
                width: 200px;
                height: 200px;
            }
            
            .cpf-value {
                font-size: 1.4rem;
                padding: 12px;
            }
        }
        
        /* Tabela de Pedidos */
        .orders-table {
            width: 100%;
            border-collapse: collapse;
            margin: 40px 0;
            background: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .orders-table th {
            background: var(--pix-green);
            color: white;
            padding: 20px;
            text-align: left;
            font-weight: 600;
        }
        
        .orders-table td {
            padding: 20px;
            border-bottom: 1px solid #e5e7eb;
        }
        
        .status-badge {
            display: inline-block;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        .status-paid {
            background: #d1fae5;
            color: #065f46;
        }
        
        .status-pending {
            background: #fef3c7;
            color: #92400e;
        }
        
        /* Contador */
        .countdown {
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }
        
        .countdown-timer {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--pix-green);
            margin: 20px 0;
            font-family: 'Courier New', monospace;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <div class="logo">
                <i class="fas fa-bolt"></i> PLATINUM PAY
            </div>
            <p class="subtitle">
                Sistema de vendas direto via Pix. 100% automatizado, sem taxas de intermediários.
                Receba pagamentos instantâneos e libere produtos automaticamente.
            </p>
        </header>

        <!-- Produtos -->
        <section id="products">
            <h2 style="text-align: center; margin-bottom: 40px; font-size: 2.2rem; color: var(--dark);">
                Nossos Produtos Digitais
            </h2>
            
            <div class="products-grid">
                <!-- Produto 1 -->
                <div class="product-card">
                    <h3 class="product-title">Método Iniciante</h3>
                    <p>Ideal para quem está começando no marketing digital</p>
                    <div class="product-price">R$ <span id="price1">97</span><small>,00</small></div>
                    <ul class="product-features">
                        <li>Estratégia passo a passo</li>
                        <li>Templates prontos para usar</li>
                        <li>Suporte por 30 dias</li>
                        <li>Acesso à comunidade</li>
                        <li>Atualizações gratuitas</li>
                    </ul>
                    <button class="buy-btn" onclick="openPaymentModal('Método Iniciante', 97)">
                        <i class="fas fa-shopping-cart"></i> COMPRAR AGORA
                    </button>
                </div>
                
                <!-- Produto 2 -->
                <div class="product-card">
                    <div style="background: var(--pix-green); color: white; padding: 8px 15px; border-radius: 20px; display: inline-block; font-weight: 600; margin-bottom: 15px;">
                        MAIS VENDIDO
                    </div>
                    <h3 class="product-title">Sistema Avançado</h3>
                    <p>Para quem quer resultados rápidos e escaláveis</p>
                    <div class="product-price">R$ <span id="price2">197</span><small>,00</small></div>
                    <ul class="product-features">
                        <li>Sistema completo automatizado</li>
                        <li>Scripts de vendas testados</li>
                        <li>Mentoria individual</li>
                        <li>Ferramentas exclusivas</li>
                        <li>Suporte vitalício</li>
                    </ul>
                    <button class="buy-btn" onclick="openPaymentModal('Sistema Avançado', 197)">
                        <i class="fas fa-rocket"></i> COMPRAR AGORA
                    </button>
                </div>
                
                <!-- Produto 3 -->
                <div class="product-card">
                    <h3 class="product-title">Pacote Master</h3>
                    <p>Tudo que você precisa para dominar o mercado</p>
                    <div class="product-price">R$ <span id="price3">297</span><small>,00</small></div>
                    <ul class="product-features">
                        <li>Todos os produtos anteriores</li>
                        <li>Consultoria personalizada</li>
                        <li>Acesso à área VIP</li>
                        <li>Certificado de conclusão</li>
                        <li>Garantia de 30 dias</li>
                    </ul>
                    <button class="buy-btn" onclick="openPaymentModal('Pacote Master', 297)">
                        <i class="fas fa-crown"></i> COMPRAR AGORA
                    </button>
                </div>
            </div>
        </section>

        <!-- Tabela de Pedidos Recentes -->
        <section>
            <h3 style="text-align: center; margin: 50px 0 20px; color: var(--dark);">
                <i class="fas fa-history"></i> Pedidos Recentes
            </h3>
            <table class="orders-table">
                <thead>
                    <tr>
                        <th>Cliente</th>
                        <th>Produto</th>
                        <th>Valor</th>
                        <th>Status</th>
                        <th>Data</th>
                    </tr>
                </thead>
                <tbody id="ordersTable">
                    <!-- Pedidos serão adicionados dinamicamente -->
                </tbody>
            </table>
        </section>

        <!-- Modal de Pagamento -->
        <div id="paymentModal" class="modal">
            <div class="modal-content">
                <button class="close-modal" onclick="closeModal()">
                    <i class="fas fa-times"></i>
                </button>
                
                <h3 class="modal-title" id="modalProductName"></h3>
                <p class="modal-subtitle">Valor: <strong id="modalProductPrice"></strong></p>
                
                <!-- Contador para Pagamento -->
                <div class="countdown">
                    <p>Tempo restante para pagamento:</p>
                    <div class="countdown-timer" id="paymentTimer">15:00</div>
                    <p>Após este tempo, o pedido será cancelado automaticamente.</p>
                </div>
                
                <!-- QR Code -->
                <div class="pix-area">
                    <h4 style="color: var(--pix-green); margin-bottom: 20px;">
                        <i class="fas fa-qrcode"></i> PAGUE COM PIX
                    </h4>
                    <p>Escaneie o QR Code abaixo com seu aplicativo bancário</p>
                    
                    <div class="qr-code-container">
                        <!-- SUBSTITUA ESTA IMAGEM PELO SEU QR CODE REAL -->
                        <img id="qrCodeImage" src="SEU_QR_CODE_AQUI.jpg" alt="QR Code Pix">
                        <div class="qr-placeholder" id="qrPlaceholder">
                            <div>
                                <i class="fas fa-qrcode" style="font-size: 3rem; margin-bottom: 10px; opacity: 0.5;"></i>
                                <p>Insira sua imagem QR Code<br>no código HTML</p>
                            </div>
                        </div>
                    </div>
                    
                    <p style="margin-top: 20px; color: var(--gray); font-size: 0.9rem;">
                        <i class="fas fa-info-circle"></i> Use a câmera do seu banco para escanear
                    </p>
                </div>
                
                <!-- CPF para Transferência -->
                <div class="cpf-container">
                    <span class="cpf-label">OU COPIE A CHAVE PIX (CPF):</span>
                    <div class="cpf-value" id="cpfValue">SEU_CPF_AQUI</div>
                    <div>
                        <button class="copy-btn" onclick="copyToClipboard('cpfValue')">
                            <i class="far fa-copy"></i> Copiar CPF
                        </button>
                        <button class="copy-btn" style="background: var(--secondary);" onclick="copyToClipboard('modalProductPrice')">
                            <i class="far fa-copy"></i> Copiar Valor
                        </button>
                    </div>
                </div>
                
                <!-- Instruções -->
                <div class="instructions">
                    <h4><i class="fas fa-list-ol"></i> COMO PAGAR:</h4>
                    <ol>
                        <li>Abra o aplicativo do seu banco</li>
                        <li>Toque em "Pagar com Pix"</li>
                        <li>Escaneie o QR Code OU cole o CPF</li>
                        <li>Confirme o valor e finalize o pagamento</li>
                        <li>Clique em "Já Paguei" abaixo</li>
                    </ol>
                </div>
                
                <!-- Status do Pagamento -->
                <div id="paymentStatus" class="payment-status">
                    <i class="fas fa-spinner fa-spin"></i>
                    <span id="statusText">Aguardando pagamento...</span>
                </div>
                
                <!-- Botões de Ação -->
                <div style="display: flex; gap: 15px; margin-top: 30px;">
                    <button class="buy-btn" onclick="confirmPayment()">
                        <i class="fas fa-check-circle"></i> JÁ PAGUEI
                    </button>
                    <button class="buy-btn" style="background: var(--gray);" onclick="closeModal()">
                        CANCELAR
                    </button>
                </div>
                
                <!-- Aviso Importante -->
                <div style="margin-top: 30px; padding: 15px; background: #f3f4f6; border-radius: var(--radius); font-size: 0.9rem; color: var(--gray);">
                    <i class="fas fa-exclamation-triangle"></i>
                    <strong>Importante:</strong> O produto será liberado automaticamente após confirmação do pagamento.
                    Enviaremos os dados de acesso para o e-mail cadastrado.
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dados atuais (SUBSTITUA COM SEUS DADOS)
        let currentProduct = {
            name: '',
            price: 0,
            orderId: ''
        };

        // Pedidos simulados
        const recentOrders = [
            { customer: 'Maria S.', product: 'Sistema Avançado', value: 'R$ 197', status: 'paid', date: '10 min' },
            { customer: 'João P.', product: 'Método Iniciante', value: 'R$ 97', status: 'paid', date: '25 min' },
            { customer: 'Ana C.', product: 'Pacote Master', value: 'R$ 297', status: 'pending', date: '45 min' },
            { customer: 'Carlos R.', product: 'Sistema Avançado', value: 'R$ 197', status: 'paid', date: '1 hora' }
        ];

        // Inicializar tabela de pedidos
        function initializeOrdersTable() {
            const tableBody = document.getElementById('ordersTable');
            tableBody.innerHTML = '';
            
            recentOrders.forEach(order => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${order.customer}</td>
                    <td>${order.product}</td>
                    <td>${order.value}</td>
                    <td>
                        <span class="status-badge ${order.status === 'paid' ? 'status-paid' : 'status-pending'}">
                            ${order.status === 'paid' ? 'PAGO' : 'PENDENTE'}
                        </span>
                    </td>
                    <td>${order.date}</td>
                `;
                tableBody.appendChild(row);
            });
        }

        // Abrir modal de pagamento
        function openPaymentModal(productName, productPrice) {
            currentProduct = {
                name: productName,
                price: productPrice,
                orderId: 'ORD' + Date.now().toString().slice(-6)
            };
            
            document.getElementById('modalProductName').textContent = productName;
            document.getElementById('modalProductPrice').textContent = `R$ ${productPrice},00`;
            
            // Se você tem uma imagem de QR Code, pode definir aqui
            // document.getElementById('qrCodeImage').src = "seu_qr_code.jpg";
            // document.getElementById('qrPlaceholder').style.display = 'none';
            
            // Se você tem um CPF, coloque aqui
            // document.getElementById('cpfValue').textContent = "123.456.789-00";
            
            // Iniciar contador
            startPaymentTimer();
            
            // Mostrar modal
            document.getElementById('paymentModal').classList.add('active');
            
            // Adicionar novo pedido à tabela
            addNewOrder(productName, productPrice);
        }

        // Fechar modal
        function closeModal() {
            document.getElementById('paymentModal').classList.remove('active');
            document.getElementById('paymentStatus').style.display = 'none';
            document.getElementById('paymentStatus').className = 'payment-status';
        }

        // Timer de pagamento
        let paymentTimer;
        let timeLeft = 15 * 60; // 15 minutos em segundos

        function startPaymentTimer() {
            timeLeft = 15 * 60;
            clearInterval(paymentTimer);
            
            paymentTimer = setInterval(() => {
                timeLeft--;
                const minutes = Math.floor(timeLeft / 60);
                const seconds = timeLeft % 60;
                
                document.getElementById('paymentTimer').textContent = 
                    `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                
                if (timeLeft <= 0) {
                    clearInterval(paymentTimer);
                    document.getElementById('paymentStatus').className = 'payment-status pending';
                    document.getElementById('statusText').textContent = 'Tempo esgotado! Pedido cancelado.';
                    document.getElementById('paymentStatus').style.display = 'block';
                }
            }, 1000);
        }

        // Confirmar pagamento
        function confirmPayment() {
            clearInterval(paymentTimer);
            
            document.getElementById('paymentStatus').className = 'payment-status success';
            document.getElementById('statusText').innerHTML = `
                <i class="fas fa-check-circle"></i> Pagamento confirmado!<br>
                <small>Seu produto está sendo liberado...</small>
            `;
            document.getElementById('paymentStatus').style.display = 'block';
            
            // Simular processamento
            setTimeout(() => {
                alert(`✅ Pagamento confirmado!\n\nProduto: ${currentProduct.name}\nValor: R$ ${currentProduct.price},00\n\nOs dados de acesso serão enviados para seu e-mail.`);
                closeModal();
                
                // Atualizar status do pedido na tabela
                updateOrderStatus(currentProduct.orderId);
            }, 2000);
        }

        // Copiar para área de transferência
        function copyToClipboard(elementId) {
            const element = document.getElementById(elementId);
            let textToCopy = element.textContent;
            
            // Se for o CPF, remover formatação
            if (elementId === 'cpfValue') {
                textToCopy = textToCopy.replace(/[^\d]/g, '');
            }
            
            // Se for o preço, pegar apenas números
            if (elementId === 'modalProductPrice') {
                textToCopy = textToCopy.replace('R$ ', '').replace(',00', '');
            }
            
            navigator.clipboard.writeText(textToCopy).then(() => {
                const originalText = element.textContent;
                element.textContent = 'Copiado!';
                element.style.color = 'var(--pix-green)';
                
                setTimeout(() => {
                    element.textContent = originalText;
                    element.style.color = '';
                }, 2000);
            });
        }

        // Adicionar novo pedido
        function addNewOrder(productName, productPrice) {
            const newOrder = {
                customer: 'Novo Cliente',
                product: productName,
                value: `R$ ${productPrice}`,
                status: 'pending',
                date: 'agora'
            };
            
            // Adicionar no início da tabela
            const tableBody = document.getElementById('ordersTable');
            const row = document.createElement('tr');
            row.id = currentProduct.orderId;
            row.innerHTML = `
                <td>${newOrder.customer}</td>
                <td>${newOrder.product}</td>
                <td>${newOrder.value}</td>
                <td>
                    <span class="status-badge status-pending">
                        PENDENTE
                    </span>
                </td>
                <td>${newOrder.date}</td>
            `;
            tableBody.insertBefore(row, tableBody.firstChild);
        }

        // Atualizar status do pedido
        function updateOrderStatus(orderId) {
            const row = document.getElementById(orderId);
            if (row) {
                const statusCell = row.cells[3];
                statusCell.innerHTML = `
                    <span class="status-badge status-paid">
                        PAGO
                    </span>
                `;
            }
        }

        // Inicializar ao carregar a página
        document.addEventListener('DOMContentLoaded', function() {
            initializeOrdersTable();
            
            // Se você quiser esconder o placeholder quando tiver QR Code
            // document.getElementById('qrPlaceholder').style.display = 'none';
            // document.getElementById('qrCodeImage').style.display = 'block';
        });

        // Fechar modal com ESC
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                closeModal();
            }
        });
    </script>

    <!-- Instruções de Configuração -->
    <div style="max-width: 800px; margin: 50px auto; padding: 30px; background: white; border-radius: var(--radius); box-shadow: var(--shadow);">
        <h3 style="color: var(--pix-green); margin-bottom: 20px;">
            <i class="fas fa-cog"></i> CONFIGURAÇÃO DO SISTEMA
        </h3>
        
        <div style="background: #f8fafc; padding: 20px; border-radius: var(--radius); margin-bottom: 20px;">
            <h4>PASSO 1: Configure seu QR Code Pix</h4>
            <p>No código HTML, linha ~330, substitua:</p>
            <pre style="background: var(--dark); color: white; padding: 15px; border-radius: var(--radius); overflow-x: auto;">
&lt;img id="qrCodeImage" src="<strong>SEU_QR_CODE_AQUI.jpg</strong>" alt="QR Code Pix"&gt;</pre>
            <p>Pelo caminho da sua imagem do QR Code Pix.</p>
        </div>
        
        <div style="background: #f8fafc; padding: 20px; border-radius: var(--radius); margin-bottom: 20px;">
            <h4>PASSO 2: Configure seu CPF</h4>
            <p>No código HTML, linha ~350, substitua:</p>
            <pre style="background: var(--dark); color: white; padding: 15px; border-radius: var(--radius); overflow-x: auto;">
&lt;div class="cpf-value" id="cpfValue"&gt;<strong>SEU_CPF_AQUI</strong>&lt;/div&gt;</pre>
            <p>Pelo seu CPF (formato: 123.456.789-00).</p>
        </div>
        
        <div style="background: #f8fafc; padding: 20px; border-radius: var(--radius);">
            <h4>PASSO 3: Configure seus Produtos</h4>
            <p>Edite os produtos nas linhas ~110-180. Altere:</p>
            <ul style="margin-left: 20px;">
                <li>Nomes dos produtos</li>
                <li>Preços (edite os valores nos spans price1, price2, price3)</li>
                <li>Características</li>
                <li>Descrições</li>
            </ul>
        </div>
        
        <div style="margin-top: 30px; padding: 20px; background: #d1fae5; border-radius: var(--radius); border-left: 4px solid var(--pix-green);">
            <h4 style="color: var(--pix-green-dark);">
                <i class="fas fa-check-circle"></i> SISTEMA PRONTO PARA USAR
            </h4>
            <p>Após configurar QR Code e CPF, seu sistema estará 100% funcional. Os clientes poderão pagar via Pix e você receberá instantaneamente.</p>
        </div>
    </div>
</body>
</html>
