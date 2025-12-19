<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🖤💎 PlatinumStore - Sistema de Renda Automática 100% Digital</title>
    
    <!-- Meta Tags para SEO e Redes Sociais -->
    <meta name="description" content="Sistema Platinum que gera de R$500 a R$2.000/mês em 72h. Método testado e aprovado. Garantia de 7 dias.">
    <meta name="keywords" content="renda automática, dinheiro online, marketing digital, platinum store, kiwiify">
    <meta property="og:title" content="🖤💎 PlatinumStore - Renda Automática em 72h">
    <meta property="og:description" content="Sistema que já colocou R$17.420 na conta de iniciantes">
    <meta property="og:image" content="https://images.unsplash.com/photo-1611224923853-80b023f02d71?ixlib=rb-1.2.1&auto=format&fit=crop&w=1200&h=630&q=80">
    <meta property="og:url" content="https://platinumstore.com">
    <meta name="theme-color" content="#000000">
    
    <!-- Favicon -->
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🖤💎</text></svg>">
    
    <!-- Fontes do Google -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    
    <!-- Estilos CSS -->
    <style>
        /* Reset e Configurações Globais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --platinum-black: #000000;
            --platinum-gold: #FFD700;
            --platinum-orange: #FFA500;
            --platinum-gray: #1a1a1a;
            --platinum-light: #f8f9fa;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: var(--platinum-black);
            color: white;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 800;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Hero */
        .hero {
            background: linear-gradient(135deg, var(--platinum-black) 0%, #2a2a2a 100%);
            padding: 60px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '🖤💎';
            position: absolute;
            font-size: 300px;
            opacity: 0.05;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 0;
        }
        
        .platinum-badge {
            background: linear-gradient(45deg, var(--platinum-gold), var(--platinum-orange));
            color: var(--platinum-black);
            padding: 12px 30px;
            border-radius: 50px;
            display: inline-block;
            font-weight: 700;
            font-size: 0.9em;
            margin-bottom: 30px;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.2em;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--platinum-gold), white);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            position: relative;
            z-index: 1;
        }
        
        .hero-subtitle {
            font-size: 1.3em;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto 40px;
            position: relative;
            z-index: 1;
        }
        
        /* Botões CTA */
        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, var(--platinum-gold), var(--platinum-orange));
            color: var(--platinum-black);
            padding: 20px 50px;
            text-decoration: none;
            font-weight: 700;
            border-radius: 50px;
            font-size: 1.2em;
            margin: 10px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            position: relative;
            z-index: 1;
        }
        
        .cta-button:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.3);
        }
        
        .cta-secondary {
            background: transparent;
            border: 2px solid var(--platinum-gold);
            color: var(--platinum-gold);
        }
        
        /* Seção de Problemas */
        .problems-section {
            background: var(--platinum-gray);
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 50px;
            color: var(--platinum-gold);
        }
        
        .problems-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .problem-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 15px;
            border-left: 5px solid var(--platinum-orange);
            transition: transform 0.3s ease;
        }
        
        .problem-card:hover {
            transform: translateY(-5px);
        }
        
        .problem-icon {
            font-size: 2.5em;
            margin-bottom: 20px;
        }
        
        /* Seção de Solução */
        .solution-section {
            padding: 100px 0;
            background: linear-gradient(135deg, #1a1a1a 0%, #000000 100%);
            position: relative;
        }
        
        .solution-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        
        /* Produtos */
        .products-section {
            padding: 100px 0;
            background: var(--platinum-black);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        
        .product-card {
            background: linear-gradient(135deg, #2a2a2a 0%, #1a1a1a 100%);
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid rgba(255, 215, 0, 0.2);
            transition: all 0.3s ease;
            position: relative;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            border-color: var(--platinum-gold);
            box-shadow: 0 20px 40px rgba(255, 215, 0, 0.1);
        }
        
        .product-header {
            padding: 40px 30px 20px;
            text-align: center;
            background: rgba(0, 0, 0, 0.3);
        }
        
        .product-price {
            font-size: 2.5em;
            font-weight: 800;
            color: var(--platinum-gold);
            margin: 20px 0;
        }
        
        .product-price span {
            font-size: 0.5em;
            opacity: 0.7;
        }
        
        .product-body {
            padding: 0 30px 40px;
        }
        
        .benefit-list {
            list-style: none;
            margin: 30px 0;
        }
        
        .benefit-list li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .benefit-list li:before {
            content: '✅';
            margin-right: 10px;
            color: var(--platinum-gold);
        }
        
        /* Garantia */
        .guarantee-section {
            background: linear-gradient(135deg, var(--platinum-black) 0%, #1a1a1a 100%);
            padding: 80px 0;
            text-align: center;
            border-top: 3px solid var(--platinum-gold);
            border-bottom: 3px solid var(--platinum-gold);
        }
        
        .guarantee-badge {
            display: inline-block;
            background: var(--platinum-gold);
            color: var(--platinum-black);
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.2em;
            margin-bottom: 30px;
        }
        
        /* Depoimentos */
        .testimonials-section {
            padding: 100px 0;
            background: var(--platinum-gray);
        }
        
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .testimonial-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(255, 215, 0, 0.2);
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            margin-top: 20px;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            background: var(--platinum-gold);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-weight: bold;
            color: var(--platinum-black);
        }
        
        /* FAQ */
        .faq-section {
            padding: 80px 0;
            background: var(--platinum-black);
        }
        
        .faq-item {
            background: rgba(255, 255, 255, 0.05);
            margin-bottom: 15px;
            border-radius: 10px;
            overflow: hidden;
            max-width: 800px;
            margin: 0 auto 15px;
        }
        
        .faq-question {
            padding: 20px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
        }
        
        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }
        
        .faq-answer.active {
            padding: 0 20px 20px;
            max-height: 500px;
        }
        
        /* Footer */
        footer {
            background: #000;
            padding: 60px 0 30px;
            text-align: center;
            border-top: 1px solid #333;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
            flex-wrap: wrap;
        }
        
        .footer-links a {
            color: #888;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--platinum-gold);
        }
        
        .copyright {
            color: #666;
            margin-top: 30px;
            font-size: 0.9em;
        }
        
        /* WhatsApp Button */
        .whatsapp-button {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8em;
            text-decoration: none;
            box-shadow: 0 5px 20px rgba(37, 211, 102, 0.3);
            z-index: 1000;
            transition: all 0.3s ease;
        }
        
        .whatsapp-button:hover {
            transform: scale(1.1);
        }
        
        /* Contador de Vagas */
        .counter-banner {
            background: linear-gradient(45deg, #ff0000, #ff6b6b);
            padding: 20px;
            text-align: center;
            margin: 40px auto;
            border-radius: 10px;
            max-width: 600px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.02); }
            100% { transform: scale(1); }
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.2em;
            }
            
            .hero-subtitle {
                font-size: 1.1em;
            }
            
            .section-title {
                font-size: 1.8em;
            }
            
            .products-grid {
                grid-template-columns: 1fr;
            }
            
            .cta-button {
                padding: 18px 30px;
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <!-- WhatsApp Button -->
    <a href="https://wa.me/5511999999999?text=Olá!%20Gostaria%20de%20saber%20mais%20sobre%20o%20PlatinumStore" 
       class="whatsapp-button" 
       target="_blank" 
       id="whatsappButton">
       💬
    </a>

    <!-- Hero Section -->
    <section class="hero" id="hero">
        <div class="container">
            <div class="platinum-badge">⚠️ OFERTA POR TEMPO LIMITADO</div>
            <h1>Pare de Trocar Seu Tempo Por Dinheiro</h1>
            <p class="hero-subtitle">
                Descubra o Sistema Platinum que já colocou <strong>R$17.420 na conta de iniciantes</strong> nos últimos 30 dias.
                Funciona mesmo se você nunca vendeu nada online.
            </p>
            
            <!-- Contador de Vagas -->
            <div class="counter-banner">
                <h3 style="margin-bottom: 10px;">⚠️ ÚLTIMAS VAGAS DISPONÍVEIS!</h3>
                <div id="countdown" style="font-size: 1.8em; font-weight: bold;">05:00</div>
                <p style="margin-top: 10px; font-size: 0.9em;">O preço sobe para R$97 quando o timer zerar</p>
            </div>
            
            <!-- Vídeo ou Imagem de Destaque -->
            <div style="max-width: 800px; margin: 40px auto; background: #111; padding: 20px; border-radius: 15px;">
                <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 10px;">
                    <div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; display: flex; align-items: center; justify-content: center; background: #000;">
                        <!-- Substitua pelo seu vídeo -->
                        <div style="text-align: center;">
                            <div style="font-size: 4em; margin-bottom: 20px;">🎥</div>
                            <h3>VÍDEO DE APRESENTAÇÃO</h3>
                            <p style="opacity: 0.7;">(Insira seu vídeo de vendas aqui)</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Botões de Ação -->
            <div style="margin-top: 40px;">
                <a href="#produtos" class="cta-button" id="mainButton">
                    🖤💎 QUERO MEU ACESSO PLATINUM - R$37
                </a>
                <br>
                <a href="#garantia" class="cta-button cta-secondary" style="margin-top: 20px;">
                    🛡️ VER GARANTIA DE 7 DIAS
                </a>
            </div>
            
            <div style="margin-top: 30px; opacity: 0.8;">
                <p>⚡ Acesso imediato após o pagamento | 📱 Use no celular ou computador</p>
            </div>
        </div>
    </section>

    <!-- Seção de Problemas -->
    <section class="problems-section">
        <div class="container">
            <h2 class="section-title">Você se identifica com alguma dessas situações?</h2>
            <div class="problems-grid">
                <div class="problem-card">
                    <div class="problem-icon">💸</div>
                    <h3>Falta de Dinheiro Rápido</h3>
                    <p>Precisa de resultados agora, não daqui a 6 meses. Quer ver dinheiro entrando esta semana.</p>
                </div>
                
                <div class="problem-card">
                    <div class="problem-icon">😰</div>
                    <h3>Medo de Aparecer</h3>
                    <p>Não quer gravar vídeos, mostrar o rosto ou expor sua vida nas redes sociais.</p>
                </div>
                
                <div class="problem-card">
                    <div class="problem-icon">🤯</div>
                    <h3>Métodos Complexos</h3>
                    <p>Cansado de cursos com 100 horas de conteúdo e zero resultado prático.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção de Solução -->
    <section class="solution-section">
        <div class="container">
            <div class="solution-content">
                <h2 class="section-title">A Solução Platinum</h2>
                <div style="background: rgba(255,215,0,0.1); padding: 30px; border-radius: 15px; margin: 40px 0;">
                    <p style="font-size: 1.3em; line-height: 1.8;">
                        Eu vou te entregar <strong>OS MESMOS 3 FLUXOS AUTOMÁTICOS</strong> que usei para gerar 
                        <strong style="color: var(--platinum-gold);">R$3.447 em 14 dias</strong>, usando apenas o celular, 
                        sem mostrar meu rosto e gastando menos de R$100 em anúncios.
                    </p>
                </div>
                
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 50px 0;">
                    <div style="text-align: center;">
                        <div style="font-size: 2.5em;">🚀</div>
                        <h4>Rápido</h4>
                        <p>Primeiro resultado em até 72h</p>
                    </div>
                    <div style="text-align: center;">
                        <div style="font-size: 2.5em;">🤫</div>
                        <h4>Anônimo</h4>
                        <p>Zero necessidade de aparecer</p>
                    </div>
                    <div style="text-align: center;">
                        <div style="font-size: 2.5em;">💎</div>
                        <h4>Comprovado</h4>
                        <p>Com prints e casos reais</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção de Produtos -->
    <section class="products-section" id="produtos">
        <div class="container">
            <h2 class="section-title">Escolha Seu Sistema Platinum</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto 50px; opacity: 0.9;">
                Todos os produtos com entrega imediata, área de membros exclusiva e suporte prioritário.
            </p>
            
            <div class="products-grid">
                <!-- Produto 1: PLATINUM FLUXO -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>🖤💎 PLATINUM FLUXO</h3>
                        <div class="product-price">R$<span style="font-size: 1em;">37</span></div>
                        <p style="opacity: 0.8;">Sistema de Renda Automática em 72h</p>
                    </div>
                    <div class="product-body">
                        <p><strong>Para quem:</strong> Iniciante total que quer resultados rápidos</p>
                        
                        <ul class="benefit-list">
                            <li>Fluxo 1: Sistema "Liga-Desliga" com IA</li>
                            <li>Fluxo 2: Máquina de Vendas Silenciosa</li>
                            <li>Fluxo 3: Clonagem de Resultados</li>
                            <li>Templates editáveis prontos</li>
                            <li>Scripts de vendas testados</li>
                            <li>Comunidade VIP Platinum</li>
                        </ul>
                        
                        <!-- LINK KIWIFY - Substitua pela sua URL -->
                        <a href="https://sualoja.kiwify.com.br/checkout/PRODUTO1" 
                           class="cta-button" 
                           style="width: 100%; text-align: center; margin-top: 20px;"
                           onclick="trackConversion('platinum_fluxo')">
                           COMPRAR AGORA
                        </a>
                        
                        <p style="text-align: center; margin-top: 15px; font-size: 0.9em; opacity: 0.7;">
                            ⚡ Entrega Imediata<br>
                            🔄 Pagamento único
                        </p>
                    </div>
                </div>
                
                <!-- Produto 2: PLATINUM IA -->
                <div class="product-card" style="border-color: var(--platinum-gold);">
                    <div class="product-header">
                        <div style="position: absolute; top: -10px; left: 50%; transform: translateX(-50%); background: var(--platinum-gold); color: black; padding: 5px 15px; border-radius: 20px; font-weight: bold;">
                            MAIS VENDIDO
                        </div>
                        <h3>🤖 PLATINUM IA</h3>
                        <div class="product-price">R$<span style="font-size: 1em;">97</span></div>
                        <p style="opacity: 0.8;">Inteligência Artificial Lucrativa</p>
                    </div>
                    <div class="product-body">
                        <p><strong>Para quem:</strong> Quer escalar com tecnologia</p>
                        
                        <ul class="benefit-list">
                            <li>5 ferramentas de IA que pagam agora</li>
                            <li>Prompts exclusivos de alta conversão</li>
                            <li>Automação completa do zero</li>
                            <li>Casos reais brasileiros</li>
                            <li>Atualizações vitalícias</li>
                            <li>Suporte premium</li>
                        </ul>
                        
                        <!-- LINK KIWIFY - Substitua pela sua URL -->
                        <a href="https://sualoja.kiwify.com.br/checkout/PRODUTO2" 
                           class="cta-button" 
                           style="width: 100%; text-align: center; margin-top: 20px;"
                           onclick="trackConversion('platinum_ia')">
                           COMPRAR AGORA
                        </a>
                        
                        <p style="text-align: center; margin-top: 15px; font-size: 0.9em; opacity: 0.7;">
                            ⚡ Entrega Imediata<br>
                            🎁 Bônus exclusivos
                        </p>
                    </div>
                </div>
                
                <!-- Produto 3: PLATINUM FANTASMA -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>👻 PLATINUM FANTASMA</h3>
                        <div class="product-price">R$<span style="font-size: 1em;">67</span></div>
                        <p style="opacity: 0.8;">Perfis Anônimos que Viralizam</p>
                    </div>
                    <div class="product-body">
                        <p><strong>Para quem:</strong> Tem vergonha/medo de aparecer</p>
                        
                        <ul class="benefit-list">
                            <li>3 perfis fantasmas prontos</li>
                            <li>Estratégia de crescimento orgânico</li>
                            <li>Conteúdo pré-formatado</li>
                            <li>Proteção de identidade</li>
                            <li>Viralização garantida</li>
                            <li>Comunidade secreta</li>
                        </ul>
                        
                        <!-- LINK KIWIFY - Substitua pela sua URL -->
                        <a href="https://sualoja.kiwify.com.br/checkout/PRODUTO3" 
                           class="cta-button" 
                           style="width: 100%; text-align: center; margin-top: 20px;"
                           onclick="trackConversion('platinum_fantasma')">
                           COMPRAR AGORA
                        </a>
                        
                        <p style="text-align: center; margin-top: 15px; font-size: 0.9em; opacity: 0.7;">
                            ⚡ Entrega Imediata<br>
                            🔒 100% Anônimo
                        </p>
                    </div>
                </div>
            </div>
            
            <!-- Pacote Completo -->
            <div style="background: linear-gradient(135deg, rgba(255,215,0,0.1) 0%, rgba(255,165,0,0.1) 100%); padding: 40px; border-radius: 20px; margin-top: 60px; text-align: center; border: 2px solid var(--platinum-gold);">
                <h3 style="color: var(--platinum-gold); margin-bottom: 20px;">🎁 PACOTE PLATINUM COMPLETO</h3>
                <p style="font-size: 1.2em; margin-bottom: 20px;">
                    <strong>TODOS OS 3 SISTEMAS + BÔNUS EXCLUSIVOS</strong>
                </p>
                <div style="display: flex; justify-content: center; align-items: center; gap: 20px; flex-wrap: wrap; margin-bottom: 30px;">
                    <div style="text-decoration: line-through; opacity: 0.7;">R$ 201</div>
                    <div style="font-size: 2em; font-weight: bold; color: var(--platinum-gold);">R$ 147</div>
                    <div style="background: #ff0000; color: white; padding: 5px 15px; border-radius: 20px; font-weight: bold;">
                        ECONOMIZE R$ 54
                    </div>
                </div>
                
                <!-- LINK KIWIFY PARA PACOTE - Substitua pela sua URL -->
                <a href="https://sualoja.kiwify.com.br/checkout/PACOTECOMPLETO" 
                   class="cta-button"
                   onclick="trackConversion('pacote_completo')">
                   🖤💎 QUERO O PACOTE COMPLETO
                </a>
                
                <p style="margin-top: 20px; opacity: 0.8;">
                    Inclui todos os produtos + 5 bônus secretos + Mentoria em grupo
                </p>
            </div>
        </div>
    </section>

    <!-- Seção de Garantia -->
    <section class="guarantee-section" id="garantia">
        <div class="container">
            <div class="guarantee-badge">🛡️ GARANTIA PLATINUM</div>
            <h2 style="font-size: 2.5em; margin-bottom: 30px;">7 Dias de Teste Drive Total</h2>
            <div style="max-width: 800px; margin: 0 auto;">
                <p style="font-size: 1.3em; margin-bottom: 30px;">
                    Teste qualquer produto Platinum por <strong>7 dias completos</strong>. Se você não ver pelo menos 
                    <strong>3 oportunidades reais de lucro</strong> ou não estiver 100% satisfeito...
                </p>
                <div style="background: white; color: black; padding: 30px; border-radius: 15px; margin: 40px 0;">
                    <h3 style="color: #000; margin-bottom: 20px;">DEVOLVEMOS 100% DO SEU DINHEIRO</h3>
                    <p style="color: #333;">Sem perguntas. Sem burocracia. Sem letras miúdas.</p>
                </div>
                <p style="opacity: 0.9;">
                    É simples assim: você arrisca <strong>zero</strong>. Ou você fica com um sistema que gera dinheiro, 
                    ou fica com seu dinheiro de volta.
                </p>
            </div>
        </div>
    </section>

    <!-- Seção de Depoimentos -->
    <section class="testimonials-section">
        <div class="container">
            <h2 class="section-title">Quem já está no Platinum</h2>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <p>"Comprei sexta-feira e na segunda já tinha R$247 na conta. Achei que era golpe, mas funciona mesmo!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">MS</div>
                        <div>
                            <strong>Marina S.</strong><br>
                            <small>São Paulo • 28 anos</small>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <p>"Pensei que era mais um curso, mas em 5 dias já fiz R$850. O fluxo com IA é surreal de fácil."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">RT</div>
                        <div>
                            <strong>Rodrigo T.</strong><br>
                            <small>Belo Horizonte • 35 anos</small>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <p>"Finalmente um método que não precisa ser influencer. Trabalho anônimo e ganhando bem."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">CM</div>
                        <div>
                            <strong>Carla M.</strong><br>
                            <small>Curitiba • 31 anos</small>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Comprovantes (simulados) -->
            <div style="text-align: center; margin-top: 50px;">
                <p style="margin-bottom: 20px; opacity: 0.9;">Comprovantes reais disponíveis na área de membros:</p>
                <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
                    <div style="background: #111; padding: 15px; border-radius: 10px; min-width: 200px;">
                        <div style="color: var(--platinum-gold); font-size: 2em;">R$ 3.447</div>
                        <small>Em 14 dias (Pedro L.)</small>
                    </div>
                    <div style="background: #111; padding: 15px; border-radius: 10px; min-width: 200px;">
                        <div style="color: var(--platinum-gold); font-size: 2em;">R$ 1.850</div>
                        <small>Em 7 dias (Ana C.)</small>
                    </div>
                    <div style="background: #111; padding: 15px; border-radius: 10px; min-width: 200px;">
                        <div style="color: var(--platinum-gold); font-size: 2em;">R$ 5.220</div>
                        <small>Em 30 dias (Carlos R.)</small>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ -->
    <section class="faq-section">
        <div class="container">
            <h2 class="section-title">Perguntas Frequentes</h2>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Como recebo o acesso?<span>+</span>
                </div>
                <div class="faq-answer">
                    <p>Imediatamente após a confirmação do pagamento! Você recebe um e-mail com acesso à área de membros e todos os materiais disponíveis para download.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Preciso de experiência?<span>+</span>
                </div>
                <div class="faq-answer">
                    <p>Não! Os sistemas foram criados para iniciantes completos. Tudo é explicado passo a passo, desde o zero.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Funciona no celular?<span>+</span>
                </div>
                <div class="faq-answer">
                    <p>Sim! Todo o sistema pode ser operado apenas com um smartphone. Você não precisa de computador.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Como funciona a garantia?<span>+</span>
                </div>
                <div class="faq-answer">
                    <p>Em até 7 dias após a compra, se você não estiver satisfeito, basta enviar um e-mail para suporte@platinumsystem.com que devolvemos 100% do seu dinheiro.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <div class="faq-question" onclick="toggleFAQ(this)">
                    Tem suporte?<span>+</span>
                </div>
                <div class="faq-answer">
                    <p>Sim! Todos os clientes têm acesso à comunidade exclusiva no Telegram e suporte por e-mail em até 24h úteis.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Call to Action Final -->
    <section style="background: linear-gradient(135deg, #000000 0%, #1a1a1a 100%); padding: 80px 0; text-align: center;">
        <div class="container">
            <h2 style="font-size: 2.5em; margin-bottom: 30px; color: var(--platinum-gold);">
                Sua Decisão Agora Define Seus Próximos 30 Dias
            </h2>
            
            <p style="font-size: 1.3em; max-width: 800px; margin: 0 auto 40px; opacity: 0.9;">
                Você pode continuar procurando "o método perfeito" ou pode começar hoje com um sistema 
                que <strong>já funciona para centenas de pessoas</strong>.
            </p>
            
            <div class="counter-banner" style="max-width: 600px; margin: 40px auto;">
                <h3>⚠️ OFERTA TERMINA EM:</h3>
                <div id="finalCountdown" style="font-size: 2em; font-weight: bold;">05:00</div>
            </div>
            
            <a href="#produtos" class="cta-button" style="font-size: 1.3em; padding: 25px 60px;">
                🖤💎 QUERO COMEÇAR AGORA - R$37
            </a>
            
            <p style="margin-top: 30px; opacity: 0.8;">
                ⚡ Acesso imediato • 🛡️ Garantia de 7 dias • 📱 100% Digital
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <h2 style="color: var(--platinum-gold); margin-bottom: 20px;">🖤💎 PLATINUM STORE</h2>
            <p style="max-width: 600px; margin: 0 auto 30px; opacity: 0.8;">
                Sistema de renda automática 100% digital. Resultados variam de acordo com o esforço e aplicação de cada pessoa.
            </p>
            
            <div class="footer-links">
                <a href="#garantia">Garantia</a>
                <a href="mailto:suporte@platinumsystem.com">Suporte</a>
                <a href="#faq">FAQ</a>
                <a href="#">Termos de Uso</a>
                <a href="#">Política de Privacidade</a>
            </div>
            
            <div class="copyright">
                © 2024 PlatinumStore. Todos os direitos reservados.<br>
                Este site não é afiliado ao Facebook, Instagram, Google ou qualquer plataforma.<br>
                Os resultados mencionados são de casos reais, mas não são típicos e variam individualmente.
            </div>
            
            <div style="margin-top: 30px; opacity: 0.6; font-size: 0.8em;">
                PlatinumStore • CNPJ: 00.000.000/0000-00 • contato@platinumsystem.com
            </div>
        </div>
    </footer>

    <!-- Scripts JavaScript -->
    <script>
        // Timer Countdown
        function startCountdown(elementId, minutes) {
            let time = minutes * 60;
            const countdownElement = document.getElementById(elementId);
            
            const updateCountdown = () => {
                const minutes = Math.floor(time / 60);
                const seconds = time % 60;
                
                countdownElement.innerHTML = 
                    `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                
                if (time <= 0) {
                    countdownElement.innerHTML = "OFERTA ENCERRADA!";
                    countdownElement.style.color = "#ff0000";
                } else {
                    time--;
                    setTimeout(updateCountdown, 1000);
                }
            };
            
            updateCountdown();
        }
        
        // FAQ Toggle
        function toggleFAQ(element) {
            const answer = element.nextElementSibling;
            const isActive = answer.classList.contains('active');
            
            // Fecha todas as outras
            document.querySelectorAll('.faq-answer').forEach(faq => {
                faq.classList.remove('active');
            });
            
            // Abre/fecha a atual
            if (!isActive) {
                answer.classList.add('active');
                element.querySelector('span').textContent = '−';
            } else {
                answer.classList.remove('active');
                element.querySelector('span').textContent = '+';
            }
        }
        
        // Track Conversion
        function trackConversion(product) {
            // Implemente aqui seu pixel do Facebook/Google
            console.log(`Compra do produto: ${product}`);
            
            // Exemplo de Facebook Pixel
            // fbq('track', 'Purchase', {value: 37.00, currency: 'BRL'});
            
            // Exemplo de Google Analytics
            // gtag('event', 'purchase', {
            //     transaction_id: 'ORDER_' + Date.now(),
            //     value: 37.00,
            //     currency: 'BRL',
            //     items: [{item_name: product}]
            // });
        }
        
        // WhatsApp Number Randomizer (para evitar spam)
        function getRandomWhatsAppNumber() {
            const numbers = [
                '5511999999999',
                '5511888888888',
                '5511777777777'
            ];
            return numbers[Math.floor(Math.random() * numbers.length)];
        }
        
        // Inicialização
        document.addEventListener('DOMContentLoaded', function() {
            // Inicia contadores
            startCountdown('countdown', 5); // 5 minutos
            startCountdown('finalCountdown', 5); // 5 minutos
            
            // Atualiza número do WhatsApp
            const whatsappButton = document.getElementById('whatsappButton');
            const randomNumber = getRandomWhatsAppNumber();
            whatsappButton.href = whatsappButton.href.replace('5511999999999', randomNumber);
            
            // Smooth Scroll para âncoras
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    if(targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if(targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // Contador de visualizações (simulação)
            let viewCount = Math.floor(Math.random() * 50) + 150;
            document.getElementById('viewCount').textContent = viewCount;
            
            // Atualiza contador a cada 30 segundos
            setInterval(() => {
                viewCount += Math.floor(Math.random() * 3) + 1;
                document.getElementById('viewCount').textContent = viewCount;
            }, 30000);
        });
        
        // Hotjar Tracking (exemplo)
        // (function(h,o,t,j,a,r){
        //     h.hj=h.hj||function(){(h.hj.q=h.hj.q||[]).push(arguments)};
        //     h._hjSettings={hjid:0000000,hjsv:6};
        //     a=o.getElementsByTagName('head')[0];
        //     r=o.createElement('script');r.async=1;
        //     r.src=t+h._hjSettings.hjid+j+h._hjSettings.hjsv;
        //     a.appendChild(r);
        // })(window,document,'https://static.hotjar.com/c/hotjar-','.js?sv=');
    </script>
    
    <!-- Meta Pixel Code (DESCOMENTE E COLE SEU CÓDIGO) -->
    <!--
    <script>
    !function(f,b,e,v,n,t,s)
    {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
    n.callMethod.apply(n,arguments):n.queue.push(arguments)};
    if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
    n.queue=[];t=b.createElement(e);t.async=!0;
    t.src=v;s=b.getElementsByTagName(e)[0];
    s.parentNode.insertBefore(t,s)}(window, document,'script',
    'https://connect.facebook.net/en_US/fbevents.js');
    fbq('init', 'SEU_PIXEL_ID_AQUI');
    fbq('track', 'PageView');
    </script>
    <noscript><img height="1" width="1" style="display:none"
    src="https://www.facebook.com/tr?id=SEU_PIXEL_ID_AQUI&ev=PageView&noscript=1"
    /></noscript>
    -->
    
    <!-- Google Analytics (DESCOMENTE E COLE SEU CÓDIGO) -->
    <!--
    <script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXX-Y"></script>
    <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'UA-XXXXX-Y');
    </script>
    -->
</body>
</html>
