<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kit Aceleração e Consistência | Instituto Oliver Costa</title>
    <style>
        /* Reset e configurações gerais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f9f9f9;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Cores principais */
        :root {
            --primary: #0056b3;
            --secondary: #ffcc00;
            --dark: #333;
            --light: #f9f9f9;
            --gray: #777;
            --success: #28a745;
        }
        
        /* Header */
        .header {
            background: linear-gradient(135deg, var(--primary) 0%, #003d82 100%);
            color: white;
            padding: 40px 30px;
            text-align: center;
            border-radius: 10px;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,186.7C384,213,480,235,576,213.3C672,192,768,128,864,128C960,128,1056,192,1152,192C1248,192,1344,128,1392,96L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            background-position: center;
        }
        
        .header-content {
            position: relative;
            z-index: 1;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 10px;
            display: inline-block;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .subtitle {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            background: var(--secondary);
            color: #000;
            padding: 16px 40px;
            font-size: 1.2rem;
            font-weight: bold;
            border-radius: 50px;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            margin: 10px;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
            background: #ffd633;
        }
        
        .guarantee-badge {
            display: inline-flex;
            align-items: center;
            margin-top: 20px;
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
        }
        
        /* Sections */
        .section {
            padding: 50px 30px;
            margin-bottom: 30px;
            border-radius: 10px;
        }
        
        .bg-white {
            background: white;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .bg-light {
            background: var(--light);
        }
        
        h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            text-align: center;
            color: var(--primary);
        }
        
        h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .section-intro {
            text-align: center;
            max-width: 800px;
            margin: 0 auto 50px;
            font-size: 1.1rem;
            color: var(--gray);
        }
        
        /* Problem Section */
        .problem-container {
            display: flex;
            align-items: center;
            gap: 40px;
            flex-wrap: wrap;
        }
        
        .problem-content {
            flex: 1;
            min-width: 300px;
        }
        
        .problem-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .problem-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .problem-list {
            list-style: none;
            margin: 20px 0;
        }
        
        .problem-list li {
            padding: 10px 0;
            padding-left: 35px;
            position: relative;
        }
        
        .problem-list li::before {
            content: "✗";
            position: absolute;
            left: 0;
            color: #e74c3c;
            font-weight: bold;
        }
        
        /* Testimonials */
        .testimonials {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .testimonial {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            padding: 30px;
            transition: transform 0.3s ease;
        }
        
        .testimonial:hover {
            transform: translateY(-5px);
        }
        
        .testimonial-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .testimonial-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
            border: 3px solid var(--primary);
        }
        
        .testimonial-info h4 {
            margin-bottom: 5px;
        }
        
        .testimonial-info p {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .testimonial-rating {
            color: var(--secondary);
            margin: 10px 0;
        }
        
        /* Modules */
        .modules {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .module {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease;
        }
        
        .module:hover {
            transform: translateY(-5px);
        }
        
        .module-header {
            background: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        .module-content {
            padding: 25px;
        }
        
        .module-content ul {
            list-style: none;
        }
        
        .module-content li {
            padding: 10px 0;
            padding-left: 30px;
            position: relative;
        }
        
        .module-content li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--success);
            font-weight: bold;
        }
        
        /* Bonus */
        .bonus-container {
            background: linear-gradient(135deg, #fff8e1 0%, #ffecb3 100%);
            border-radius: 15px;
            padding: 40px;
            text-align: center;
            margin-top: 40px;
            border: 2px dashed var(--secondary);
        }
        
        .bonus-item {
            display: flex;
            align-items: center;
            margin: 20px 0;
            text-align: left;
        }
        
        .bonus-icon {
            font-size: 2rem;
            margin-right: 20px;
            color: var(--primary);
        }
        
        /* Pricing */
        .pricing-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 50px;
        }
        
        .pricing-card {
            background: white;
            border-radius: 15px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            flex: 1;
            min-width: 300px;
            max-width: 400px;
            border: 2px solid #eaeaea;
            transition: all 0.3s ease;
        }
        
        .pricing-card.featured {
            border-color: var(--primary);
            transform: scale(1.05);
            position: relative;
        }
        
        .pricing-badge {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary);
            color: white;
            padding: 8px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: bold;
        }
        
        .price {
            font-size: 3rem;
            font-weight: bold;
            color: var(--primary);
            margin: 20px 0;
        }
        
        .price-old {
            text-decoration: line-through;
            color: var(--gray);
            font-size: 1.5rem;
        }
        
        .price-saving {
            background: var(--success);
            color: white;
            padding: 5px 15px;
            border-radius: 30px;
            display: inline-block;
            margin-bottom: 20px;
            font-weight: bold;
        }
        
        .pricing-features {
            list-style: none;
            margin: 30px 0;
            text-align: left;
        }
        
        .pricing-features li {
            padding: 10px 0;
            padding-left: 35px;
            position: relative;
        }
        
        .pricing-features li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--success);
            font-weight: bold;
        }
        
        /* FAQ */
        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .faq-item {
            margin-bottom: 15px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
        }
        
        .faq-question {
            background: white;
            padding: 20px;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .faq-answer {
            background: #f8f9fa;
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
        }
        
        .faq-answer.active {
            padding: 20px;
            max-height: 500px;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 50px 30px 20px;
            border-radius: 10px;
            margin-top: 30px;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 200px;
        }
        
        .footer-column h4 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .section {
                padding: 30px 20px;
            }
            
            .pricing-card.featured {
                transform: none;
            }
        }
        
        /* Estilos específicos para PDF */
        @media print {
            .cta-button {
                background: #ffcc00 !important;
                color: #000 !important;
                -webkit-print-color-adjust: exact;
            }
            
            .header {
                background: #0056b3 !important;
                -webkit-print-color-adjust: exact;
            }
            
            .module-header {
                background: #0056b3 !important;
                -webkit-print-color-adjust: exact;
            }
            
            .bonus-container {
                background: #fff8e1 !important;
                -webkit-print-color-adjust: exact;
            }
            
            .testimonial {
                break-inside: avoid;
            }
            
            .module {
                break-inside: avoid;
            }
            
            .pricing-card {
                break-inside: avoid;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-content">
            <div class="logo">Instituto Oliver Costa</div>
            <h1>Kit "Aceleração e Consistência"</h1>
            <p class="subtitle">Transforme seu atendimento inconsistente em um sistema previsível que melhora sua nota e a confiança do cliente</p>
            <a href="#oferta" class="cta-button">QUERO MELHORAR MINHA REPUTAÇÃO AGORA</a>
            <div class="guarantee-badge">
                🛡️ 7 dias de garantia incondicional
            </div>
        </div>
    </header>

    <!-- Problem Section -->
    <section class="section bg-light">
        <div class="container">
            <h2>Sua empresa está na <span style="color: var(--primary);">Zona de Atenção</span>?</h2>
            <p class="section-intro">Empresas com atendimento inconsistente enfrentam desafios que impactam diretamente nos resultados</p>
            
            <div class="problem-container">
                <div class="problem-content">
                    <h3>Você se identifica com algum desses problemas?</h3>
                    <ul class="problem-list">
                        <li>Reclamações recorrentes nas redes sociais e Reclame Aqui</li>
                        <li>Nota baixa de reputação afastando clientes em potencial</li>
                        <li>Falta de padrão no atendimento entre diferentes colaboradores</li>
                        <li>Dificuldade em transformar clientes insatisfeitos em promotores da marca</li>
                        <li>Processos internos ineficientes que geram retrabalho</li>
                        <li>Falta de dados claros para tomar decisões sobre reputação</li>
                    </ul>
                    <p>Se você respondeu "sim" para pelo menos um item, o Kit "Aceleração e Consistência" foi desenvolvido para resolver exatamente esses problemas.</p>
                </div>
                <div class="problem-image">
                    <!-- Imagem representativa de problemas de reputação -->
                    <div style="width: 100%; height: 300px; background: #e0e0e0; border-radius: 10px; display: flex; align-items: center; justify-content: center; color: #777; font-size: 1.2rem;">
                        [Imagem: Gráfico mostrando baixa reputação]
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="section bg-white">
        <div class="container">
            <h2>O que dizem empresas que já transformaram sua reputação</h2>
            <p class="section-intro">Empresas reais, resultados reais - conheça histórias de sucesso de quem aplicou a metodologia</p>
            
            <div class="testimonials">
                <div class="testimonial">
                    <div class="testimonial-header">
                        <div class="testimonial-avatar" style="background: #e0e0e0; display: flex; align-items: center; justify-content: center; color: #777;">
                            MP
                        </div>
                        <div class="testimonial-info">
                            <h4>Móveis Planejados Aconchego</h4>
                            <p>Marcenaria em São Paulo</p>
                        </div>
                    </div>
                    <div class="testimonial-rating">★★★★★</div>
                    <p>"Em 45 dias, nossa nota no Reclame Aqui saltou de 6,2 para 8,7. O checklist de respostas foi um divisor de águas - agora temos padrão e qualidade em todas as interações!"</p>
                </div>
                
                <div class="testimonial">
                    <div class="testimonial-header">
                        <div class="testimonial-avatar" style="background: #e0e0e0; display: flex; align-items: center; justify-content: center; color: #777;">
                            TS
                        </div>
                        <div class="testimonial-info">
                            <h4>TechSolutions Brasil</h4>
                            <p>TI e Suporte em Curitiba</p>
                        </div>
                    </div>
                    <div class="testimonial-rating">★★★★★</div>
                    <p>"A planilha de KPIs nos mostrou onde estávamos errando. Em 2 meses, reduzimos o tempo médio de resposta de 48h para 6h e aumentamos a taxa de solução em 40%."</p>
                </div>
                
                <div class="testimonial">
                    <div class="testimonial-header">
                        <div class="testimonial-avatar" style="background: #e0e0e0; display: flex; align-items: center; justify-content: center; color: #777;">
                            DN
                        </div>
                        <div class="testimonial-info">
                            <h4>Delícia Natural</h4>
                            <p>Alimentação Saudável no RJ</p>
                        </div>
                    </div>
                    <div class="testimonial-rating">★★★★☆</div>
                    <p>"O framework de causa raiz nos ajudou a identificar que 70% das reclamações vinham de um único processo. Corrigimos e as reclamações caíram pela metade no primeiro mês!"</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Solution -->
    <section class="section bg-light">
        <div class="container">
            <h2>Conheça o Kit "Aceleração e Consistência"</h2>
            <p class="section-intro">Um sistema completo em 3 módulos para transformar seu atendimento e reputação online</p>
            
            <div class="modules">
                <div class="module">
                    <div class="module-header">
                        <h3>Módulo 1</h3>
                        <p>Padronização e Excelência no Atendimento</p>
                    </div>
                    <div class="module-content">
                        <ul>
                            <li><strong>Guia Completo:</strong> "Definindo o Tom de Voz e a Política de Atendimento"</li>
                            <li><strong>Treinamento Rápido:</strong> "Atendimento que Encanta Online" com slides e exercícios</li>
                            <li><strong>Checklist de Qualidade:</strong> Para respostas no Reclame Aqui e Redes Sociais</li>
                        </ul>
                        <p style="margin-top: 20px; font-style: italic;">Resultado: Equipe alinhada, comunicação consistente e atendimento de excelência</p>
                    </div>
                </div>
                
                <div class="module">
                    <div class="module-header">
                        <h3>Módulo 2</h3>
                        <p>Otimização e Análise de Processos</p>
                    </div>
                    <div class="module-content">
                        <ul>
                            <li><strong>Framework Completo:</strong> Análise de Causa Raiz para Reclamações</li>
                            <li><strong>Planilha de KPIs:</strong> Dashboard de Reputação e Atendimento</li>
                            <li><strong>Guia Prático:</strong> "Transformando Feedback Negativo em Melhoria Contínua"</li>
                        </ul>
                        <p style="margin-top: 20px; font-style: italic;">Resultado: Processos otimizados, menos reclamações e decisões baseadas em dados</p>
                    </div>
                </div>
                
                <div class="module">
                    <div class="module-header">
                        <h3>Módulo 3</h3>
                        <p>Proatividade e Construção de Imagem Positiva</p>
                    </div>
                    <div class="module-content">
                        <ul>
                            <li><strong>Guia Estratégico:</strong> Como Gerar Avaliações Positivas no Reclame Aqui e Google</li>
                            <li><strong>Template Prático:</strong> Pesquisa de Satisfação Pós-Atendimento</li>
                            <li><strong>Manual Avançado:</strong> "Transformando Clientes Satisfeitos em Defensores da Marca"</li>
                        </ul>
                        <p style="margin-top: 20px; font-style: italic;">Resultado: Mais avaliações positivas, clientes fiéis e defensores da sua marca</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Bonus -->
    <section class="section bg-white">
        <div class="container">
            <h2>Bônus Exclusivos</h2>
            <p class="section-intro">Itens extras para potencializar ainda mais seus resultados (por tempo limitado)</p>
            
            <div class="bonus-container">
                <div class="bonus-item">
                    <div class="bonus-icon">🎓</div>
                    <div>
                        <h3>Masterclass Gravada</h3>
                        <p>"O Segredo das Empresas com Reputação 100%" - Aula em vídeo de 75 minutos com Edna Oliver compartilhando cases reais e estratégias comprovadas.</p>
                    </div>
                </div>
                
                <div class="bonus-item">
                    <div class="bonus-icon">📊</div>
                    <div>
                        <h3>Template de Relatório para Diretoria</h3>
                        <p>Modelo profissional para apresentar resultados de reputação para a alta gestão, mostrando ROI e impacto no negócio.</p>
                    </div>
                </div>
                
                <div class="bonus-item">
                    <div class="bonus-icon">👥</div>
                    <div>
                        <h3>Acesso ao Grupo Exclusivo</h3>
                        <p>Comunidade fechada para troca de experiências e networking com outros gestores focados em excelência no atendimento.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing -->
    <section id="oferta" class="section bg-light">
        <div class="container">
            <h2>Invista na Sua Reputação Hoje</h2>
            <p class="section-intro">Escolha a melhor forma de adquirir o kit e comece a transformar seu atendimento</p>
            
            <div class="pricing-container">
                <div class="pricing-card">
                    <h3>Kit Básico</h3>
                    <div class="price">R$ 197</div>
                    <ul class="pricing-features">
                        <li>3 Módulos Completos</li>
                        <li>Materiais em PDF</li>
                        <li>Planilhas editáveis</li>
                        <li>Acesso vitalício</li>
                        <li>Certificado de conclusão</li>
                    </ul>
                    <a href="#" class="cta-button" style="background: #e0e0e0; color: #333;">ESCOLHER ESTE</a>
                </div>
                
                <div class="pricing-card featured">
                    <div class="pricing-badge">MAIS POPULAR</div>
                    <h3>Kit Completo</h3>
                    <div class="price-old">R$ 497</div>
                    <div class="price">R$ 297</div>
                    <div class="price-saving">Economize R$ 200</div>
                    <ul class="pricing-features">
                        <li>3 Módulos Completos</li>
                        <li>Materiais em PDF</li>
                        <li>Planilhas editáveis</li>
                        <li>Acesso vitalício</li>
                        <li>Certificado de conclusão</li>
                        <li><strong>2 Bônus Exclusivos</strong></li>
                        <li><strong>Acesso ao Grupo VIP</strong></li>
                        <li><strong>Suporte Prioritário</strong></li>
                    </ul>
                    <a href="#" class="cta-button">ESCOLHER ESTE</a>
                </div>
                
                <div class="pricing-card">
                    <h3>Kit Premium</h3>
                    <div class="price">R$ 497</div>
                    <ul class="pricing-features">
                        <li>3 Módulos Completos</li>
                        <li>Materiais em PDF</li>
                        <li>Planilhas editáveis</li>
                        <li>Acesso vitalício</li>
                        <li>Certificado de conclusão</li>
                        <li>3 Bônus Exclusivos</li>
                        <li>Acesso ao Grupo VIP</li>
                        <li>Suporte Prioritário</li>
                        <li><strong>1 Sessão de Mentoria Individual (60min)</strong></li>
                    </ul>
                    <a href="#" class="cta-button" style="background: #e0e0e0; color: #333;">ESCOLHER ESTE</a>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 30px;">
                <div class="guarantee-badge" style="background: var(--primary); color: white; display: inline-flex;">
                    🛡️ 7 dias de garantia incondicional - Se não gostar, devolvemos seu dinheiro
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ -->
    <section class="section bg-white">
        <div class="container">
            <h2>Perguntas Frequentes</h2>
            
            <div class="faq-container">
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Para quem é este kit?</span>
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        <p>O kit é ideal para empresas que se encontram na Zona de Atenção do Diagnóstico de Reputação - ou seja, que têm notas entre 6.0 e 7.9 no Reclame Aqui ou avaliações mistas no Google. É perfeito para donos de negócio, gerentes de atendimento e profissionais de CX que querem transformar um atendimento inconsistente em um sistema previsível e de excelência.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Como receberei o material?</span>
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Imediatamente após a confirmação do pagamento, você receberá um e-mail com acesso à área de membros, onde todos os materiais estarão disponíveis para download. Você pode acessar de qualquer dispositivo, a qualquer momento.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Quanto tempo leva para ver resultados?</span>
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Os primeiros resultados podem ser percebidos em poucas semanas, especialmente na padronização do atendimento. Empresas que implementam consistentemente relatam melhoras significativas na nota de reputação em 60-90 dias.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Preciso de uma equipe grande para implementar?</span>
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Não! O kit foi desenvolvido para ser implementado mesmo por empresas com equipes enxutas. Muitos dos materiais são de aplicação imediata, e as planilhas são automatizadas para facilitar a análise mesmo com poucos recursos.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">
                        <span>E se eu não gostar do kit?</span>
                        <span>+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Oferecemos uma garantia incondicional de 7 dias. Se por qualquer motivo você não ficar satisfeito, basta nos enviar um e-mail que devolvemos 100% do seu investimento, sem burocracia.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="section" style="background: linear-gradient(135deg, var(--primary) 0%, #003d82 100%); color: white; text-align: center;">
        <div class="container">
            <h2>Está pronto para transformar sua reputação?</h2>
            <p style="max-width: 700px; margin: 0 auto 30px; font-size: 1.2rem;">Não espere que uma crise de reputação afete seu negócio. Tome uma atitude proativa hoje e construa uma base sólida de confiança com seus clientes.</p>
            <a href="#oferta" class="cta-button">SIM, QUERO MELHORAR MINHA REPUTAÇÃO</a>
            <p style="margin-top: 20px; opacity: 0.8;">Últimas vagas com preço promocional</p>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h4>Instituto Oliver Costa</h4>
                    <p>Especialistas em reputação online e experiência do cliente. Ajudamos empresas a transformarem seu atendimento e construírem marcas admiradas.</p>
                </div>
                
                <div class="footer-column">
                    <h4>Links Rápidos</h4>
                    <ul class="footer-links">
                        <li><a href="#">Página Inicial</a></li>
                        <li><a href="#">Sobre Nós</a></li>
                        <li><a href="#">Depoimentos</a></li>
                        <li><a href="#">Contato</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h4>Suporte</h4>
                    <ul class="footer-links">
                        <li><a href="#">Central de Ajuda</a></li>
                        <li><a href="#">Política de Privacidade</a></li>
                        <li><a href="#">Termos de Uso</a></li>
                        <li><a href="#">Garantia</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2024 Instituto Oliver Costa. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // FAQ toggle
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const answer = question.nextElementSibling;
                answer.classList.toggle('active');
                
                // Change the icon
                const icon = question.querySelector('span:last-child');
                icon.textContent = answer.classList.contains('active') ? '−' : '+';
            });
        });
    </script>
</body>
</html>
