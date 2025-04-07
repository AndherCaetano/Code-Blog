<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog Dra. Gabrielle Moreira</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        /* Banner Responsivo */
        .banner-container {
            width: 100%;
            overflow: hidden;
            position: relative;
            margin: 0 auto;
        }

        .banner-img {
            width: 100%;
            height: auto;
            display: block;
            object-fit: cover;
            object-position: center 10%;
            transition: transform 0.5s ease;
        }

        .banner-container:hover .banner-img {
            transform: scale(1.03);
        }

        /* Media Queries para o Banner */
        @media (min-width: 1024px) {
            .banner-img {
                object-position: center 8% !important;
            }
        }

        @media (min-width: 992px) and (max-width: 1199px) {
            .banner-img {
                height: 350px;
                object-position: center 50%;
            }
        }

        @media (min-width: 768px) and (max-width: 1280px) {
            .banner-img {
                height: 400px;
                object-position: center 45%;
            }
        }

        @media (min-width: 576px) and (max-width: 767px) {
            .banner-img {
                height: 250px;
                object-position: center 25%;
            }
        }

        @media (max-width: 575px) {
            .banner-img {
                height: 200px;
                object-position: center 20%;
            }
        }

        @media (min-width: 1600px) {
            .banner-img {
                height: 70vh;
                object-position: center 5% !important;
                object-fit: cover;
            }
        }

        @media (min-width: 2500px) {
            .banner-img {
                height: 80vh;
                object-position: center 3% !important;
            }
        }
        
        .blog-container {
            display: flex;
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 15px;
            gap: 30px;
        }
        
        .main-content {
            flex: 1;
        }
        
        .posts-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .post {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            flex: 1 1 calc(33.333% - 14px);
            min-width: 300px;
            transition: transform 0.3s;
        }
        
        .post:hover {
            transform: translateY(-5px);
        }
        
        .post img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }
        
        .post-content {
            padding: 20px;
            text-align: left;
        }
        
        .post h2 {
            color: #000;
            font-weight: bold;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }
        
        .post p {
            color: #000;
            margin-bottom: 15px;
            font-size: 0.95rem;
            text-align: justify;
            text-justify: inter-word;
        }
        
        .post-date {
            color: #888;
            font-size: 0.75rem;
            margin-bottom: 10px;
            font-style: italic;
        }
        
        .read-more {
            background-color: #C39B82;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s;
            font-size: 0.9rem;
            text-decoration: none;
            display: inline-block;
            margin-right: auto;
            margin-left: 0;
        }
        
        .read-more:hover {
            background-color: #b08a70;
        }
        
        .load-more-container {
            text-align: center;
            margin: 30px 0;
        }
        
        .load-more {
            background-color: #C39B82;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s;
            font-size: 1rem;
        }
        
        .load-more:hover {
            background-color: #b08a70;
        }
        
        .sidebar {
            width: 350px;
            position: sticky;
            top: 20px;
            height: fit-content;
        }
        
        .profile-card {
            background: white;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            text-align: left;
        }
        
        .profile-card img {
            width: 150px;
            height: auto;
            border-radius: 50%;
            margin: 0 auto 15px;
            display: block;
        }
        
        .profile-card h3 {
            color: #C39B82;
            margin-bottom: 15px;
            font-size: 1.2rem;
            text-align: center;
        }
        
        .profile-card p {
            color: #333;
            margin-bottom: 10px;
            font-size: 0.9rem;
            text-align: justify;
            text-justify: inter-word;
        }
        
        .profile-card strong {
            color: #C39B82;
        }
        
        .sidebar-posts {
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            text-align: left;
        }
        
        .sidebar-posts h3 {
            color: #C39B82;
            margin-bottom: 15px;
            font-size: 1.3rem;
            padding-bottom: 10px;
            border-bottom: 1px solid #C39B82;
        }
        
        .sidebar-posts ul {
            list-style: none;
            padding-left: 0;
            margin-left: 0;
        }
        
        .sidebar-posts li {
            margin-bottom: 12px;
            padding-bottom: 12px;
            border-bottom: 1px solid #eee;
            text-align: left;
        }
        
        .sidebar-posts li:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        .sidebar-posts a {
            color: #C39B82;
            text-decoration: none;
            transition: color 0.3s;
            font-size: 0.95rem;
            display: block;
            text-align: left;
        }
        
        .sidebar-posts a:hover {
            color: #b08a70;
            text-decoration: underline;
        }
        
        @media (max-width: 992px) {
            .blog-container {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                position: static;
                display: flex;
                flex-direction: column;
            }
            
            .sidebar-posts {
                order: 1;
            }
            
            .profile-card {
                order: 2;
                margin-top: 0;
            }
            
            .post {
                flex: 1 1 calc(50% - 10px);
            }
        }
        
        @media (max-width: 768px) {
            .profile-card img {
                width: 120px;
            }
            
            .post {
                flex: 1 1 100%;
            }

            body {
                background-color: #ffffff !important;
            }
        }
    </style>
</head>
<body>

<!-- Banner Responsivo -->
<div class="banner-container">
    <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2025-04-05-as-13.27.38-e1743870754287.png" 
         alt="Banner do Blog Dra. Gabrielle Moreira" 
         class="banner-img">
</div>

<div class="newsletter-container" style="font-family: Arial, sans-serif; background-color: #E5DED7; display: flex; justify-content: center; padding: 20px 0;">
    <div style="display: flex; flex-wrap: wrap; align-items: center; background: #E5DED7; padding: 20px; border-radius: 8px; max-width: 800px; width: 100%; gap: 10px;">
        <div style="margin-right: 20px; flex: 1 1 200px;">
            <h2 style="margin: 0; font-size: 18px;">Inscreva-se e obtenha mais informações</h2>
            <p style="font-size: 14px; color: #666; margin: 5px 0 0;">Preencha seu telefone para saber mais sobre os tratamentos.</p>
        </div>
        <input type="tel" id="phone" placeholder="Insira seu número de telefone" 
               style="padding: 10px; border: 1px solid #ccc; border-radius: 5px; min-width: 250px; text-align: center; flex: 1;"
               maxlength="11" pattern="[0-9]{11}" title="Digite os 11 números do telefone">
        <button onclick="subscribe()" 
                style="padding: 10px 15px; background-color: #5C4441; color: white; border: none; cursor: pointer; border-radius: 5px; flex: 0 0 auto;">
            Se inscrever
        </button>
    </div>
</div>

<div class="blog-container">
    <div class="main-content">
        <div class="posts-grid" id="posts-container">
            <!-- Posts serão inseridos via JavaScript -->
        </div>
        
        <div class="load-more-container">
            <button class="load-more" id="load-more-btn">Carregar Mais Posts</button>
        </div>
    </div>
    
    <aside class="sidebar">
        <div class="sidebar-posts">
            <h3>Posts Recentes</h3>
            <ul id="recent-posts-list">
                <!-- Posts recentes serão inseridos via JavaScript -->
            </ul>
        </div>
        
        <div class="profile-card">
            <img src="https://gabriellemoreira.com.br/wp-content/uploads/2024/12/Gabee-fundo-transparente.png" alt="Dra. Gabrielle Moreira">
            <h3>Dra. Gabrielle Moreira</h3>
            <p><strong>🎓 Formação:</strong></p>
            <p>Doutora em Fisioterapia (UNIFRAN)</p>
            <p>Cursos no Hospital Albert Einstein</p>
            <p>Especialista em Laserterapia</p>
            <p><strong>🏆 Reconhecimento:</strong></p>
            <p>Habilitada pelo Remove INK (maior congresso de remoção de tatuagens do Brasil)</p>
            <p>Única profissional em Franca com certificação em 2 tipos de lasers</p>
            <p>5+ especializações em laserterapia</p>
            <p><strong>💡 Diferenciais:</strong></p>
            <p>Prescrição de medicamentos e aplicação de injetáveis</p>
            <p>Técnicas avançadas com segurança e conforto</p>
            <p>Atualização constante em congressos científicos</p>
            <p><strong>✨Excelência em tratamentos que unem ciência e tecnologia de ponta!</strong></p>
        </div>
    </aside>
</div>

<script>
    // Funções auxiliares para datas
    function formatRelativeDate(date) {
        const now = new Date();
        const diffTime = now - date;
        const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
        
        if (diffDays === 0) return "hoje";
        if (diffDays === 1) return "ontem";
        if (diffDays < 7) return `há ${diffDays} dias`;
        if (diffDays < 14) return "há 1 semana";
        if (diffDays < 30) return `há ${Math.floor(diffDays / 7)} semanas`;
        if (diffDays < 60) return "há 1 mês";
        return `há ${Math.floor(diffDays / 30)} meses`;
    }

    function formatDate(date) {
        const day = String(date.getDate()).padStart(2, '0');
        const month = String(date.getMonth() + 1).padStart(2, '0');
        const year = String(date.getFullYear()).slice(-2);
        return `${day}/${month}/${year}`;
    }

    // Lista completa de posts (originais + adicionais)
    const allPosts = [
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2024/12/estagio-5-remove.png",
            title: "Resultados Progressivos: Remoção de Tatuagem",
            excerpt: "Acompanhe a evolução do tratamento em cinco (5) sessões...",
            category: "Remoção de Tatuagem",
            link: "https://gabriellemoreira.com.br/removetatoo/",
            date: new Date(2025, 3, 5) // 5 de abril de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2025-04-01-as-00.59.20.png",
            title: "Sessões de Laserterapia para Alívio de Dores",
            excerpt: "Conheça esse surpreendente tratamento...",
            category: "Laserterapia",
            link: "https://gabriellemoreira.com.br/dor-e-recuperacao-muscular/",
            date: new Date(2025, 3, 1) // 1 de abril de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2024-11-17-as-22.53.53.png",
            title: "Fortalecimento e Reabilitação",
            excerpt: "Saiba como exercícios específicos na fisioterapia ajudam a fortalecer músculos...",
            category: "Fisioterapia",
            link: "https://gabriellemoreira.com.br/reabilitacao-fisica/",
            date: new Date(2024, 10, 17) // 17 de novembro de 2024
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2025-04-01-as-12.41.22.png",
            title: "Controle e insuficiência cardíaca",
            excerpt: "Melhore a oxigenação e capacidade respiratória através...",
            category: "Cardiologia",
            link: "https://gabriellemoreira.com.br/fisioterapia-cardiovascular/",
            date: new Date(2025, 3, 1) // 1 de abril de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2024-12-07-as-22.45.05.png",
            title: "Laserterapia no alívio de dores",
            excerpt: "Tecnologia para tratamentos de dores...",
            category: "Laserterapia",
            link: "https://gabriellemoreira.com.br/dor-e-recuperacao-muscular/",
            date: new Date(2024, 11, 7) // 7 de dezembro de 2024
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2024-12-05-as-00.11.50-e1743109960680.png",
            title: "Remoção eficaz de todos os tipos de tinta",
            excerpt: "O processo de remoção é gradual e requer várias sessões espaçadas...",
            category: "Remoção de Tatuagem",
            link: "https://gabriellemoreira.com.br/removetatoo/",
            date: new Date(2024, 11, 5) // 5 de dezembro de 2024
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2024/12/Captura-de-Tela-2024-11-17-as-22.33.26-e1739219614738.png",
            title: "Recuperação da capacidade pulmonar após sequelas",
            excerpt: "Exercícios de expansão pulmonar, treinamento...",
            category: "Fisioterapia",
            link: "https://gabriellemoreira.com.br/fisioterapia-respiratoria/",
            date: new Date(2024, 10, 17) // 17 de novembro de 2024
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-31-as-13.58.52.png",
            title: "Melhore a aparência dos poros!",
            excerpt: "A laserterapia é uma solução eficaz para tratar diversos...",
            category: "Estética",
            link: "https://gabriellemoreira.com.br/remocao-de-manchas/",
            date: new Date(2025, 2, 31) // 31 de março de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-28-as-13.31.30-1.png",
            title: "Remoção de pigmentos",
            excerpt: "A laserterapia é uma solução...",
            category: "Estética",
            link: "https://gabriellemoreira.com.br/despigmentacao-a-laser/",
            date: new Date(2025, 2, 28) // 28 de março de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2024-11-17-as-22.43.28-1.png",
            title: "Invista na melhoria da mobilidade",
            excerpt: "Ganho de amplitude muscular...",
            category: "Fisioterapia",
            link: "https://gabriellemoreira.com.br/reabilitacao-fisica/",
            date: new Date(2024, 10, 17) // 17 de novembro de 2024
        },
        // Posts adicionais sobre Fisioterapia Esportiva
        {
            image: "https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
            title: "Fisioterapia Esportiva: Prevenção de Lesões",
            excerpt: "Técnicas avançadas para atletas evitarem lesões durante treinos intensivos...",
            category: "Fisioterapia Esportiva",
            link: "https://gabriellemoreira.com.br/fisioterapia-esportiva-3/",
            date: new Date(2025, 3, 10) // 10 de abril de 2025
        },
        {
            image: "https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
            title: "Recuperação Pós-Competição",
            excerpt: "Protocolos específicos para atletas após competições de alto rendimento...",
            category: "Fisioterapia Esportiva",
            link: "https://gabriellemoreira.com.br/fisioterapia-esportiva-3/",
            date: new Date(2025, 3, 8) // 8 de abril de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2025-04-06-as-21.51.44.png",
            title: "Treinamento Funcional para Atletas",
            excerpt: "Exercícios específicos para melhorar performance esportiva...",
            category: "Fisioterapia Esportiva",
            link: "https://gabriellemoreira.com.br/fisioterapia-esportiva-3/",
            date: new Date(2025, 3, 5) // 5 de abril de 2025
        },
        // Outros posts adicionais
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2025-04-06-as-21.53.36.png",
            title: "Laserterapia: tecnologia no combate à dor",
            excerpt: "Conheça os benefícios surpreendentes desta terapia que combina tecnologia e saúde...",
            category: "Laserterapia",
            link: "https://gabriellemoreira.com.br/dor-e-recuperacao-muscular/",
            date: new Date(2025, 2, 25) // 25 de março de 2025
        },
        {
            image: "https://gabriellemoreira.com.br/wp-content/uploads/2025/04/Captura-de-Tela-2025-04-06-as-21.56.11.png",
            title: "Protocolos avançados em laserterapia",
            excerpt: "Entenda passo a passo como o tratamento é realizado e quais os resultados esperados...",
            category: "Laserterapia",
            link: "https://gabriellemoreira.com.br/dor-e-recuperacao-muscular/",
            date: new Date(2025, 2, 20) // 20 de março de 2025
        }
    ];

    // Categorias e links correspondentes
    const categoryLinks = {
        "Laserterapia": "https://gabriellemoreira.com.br/laserterapia/",
        "Fisioterapia": "https://gabriellemoreira.com.br/fisioterapia/",
        "Remoção de Manchas": "https://gabriellemoreira.com.br/remocao-de-manchas/",
        "Despigmentação": "https://gabriellemoreira.com.br/despigmentacao/",
        "Fisioterapia Cardiovascular": "https://gabriellemoreira.com.br/fisioterapia-cardiovascular/",
        "Fisioterapia Respiratória": "https://gabriellemoreira.com.br/fisioterapia-respiratoria/",
        "Reabilitação Física": "https://gabriellemoreira.com.br/reabilitacao/",
        "Tratamento de Dor": "https://gabriellemoreira.com.br/tratamento-dor/",
        "Estética": "https://gabriellemoreira.com.br/estetica/",
        "Procedimentos Avançados": "https://gabriellemoreira.com.br/procedimentos/",
        "Fisioterapia Esportiva": "https://gabriellemoreira.com.br/fisioterapia-esportiva-3/",
        "Remoção de Tatuagem": "https://gabriellemoreira.com.br/removetatoo/",
        "Cardiologia": "https://gabriellemoreira.com.br/fisioterapia-cardiovascular/",
        "Orçamento": "https://gabriellemoreira.com.br/orcamento/"
    };

    // Elementos do DOM
    const postsContainer = document.getElementById('posts-container');
    const loadMoreBtn = document.getElementById('load-more-btn');
    const recentPostsList = document.getElementById('recent-posts-list');
    
    // Variáveis de controle
    let visiblePosts = 6;
    const postsPerLoad = 6;
    let recentPostsInterval;

    // Função para renderizar os posts principais
    function renderPosts() {
        postsContainer.innerHTML = '';
        
        const postsToShow = allPosts.slice(0, visiblePosts);
        
        postsToShow.forEach(post => {
            const postElement = document.createElement('div');
            postElement.className = 'post';
            postElement.innerHTML = `
                <img src="${post.image}" alt="${post.title}">
                <div class="post-content">
                    <h2>${post.title}</h2>
                    <p class="post-date">${formatDate(post.date)} • ${formatRelativeDate(post.date)}</p>
                    <p>${post.excerpt}</p>
                    <a href="${post.link}" class="read-more">Leia mais...</a>
                </div>
            `;
            postsContainer.appendChild(postElement);
        });
        
        // Mostrar/ocultar botão "Carregar Mais"
        loadMoreBtn.style.display = visiblePosts >= allPosts.length ? 'none' : 'block';
    }

    // Função para gerar posts recentes aleatórios
    function generateRandomRecentPosts() {
        // Embaralha todos os posts
        const shuffledPosts = [...allPosts].sort(() => 0.5 - Math.random());
        
        // Seleciona apenas 6 posts para mostrar
        const selectedPosts = shuffledPosts.slice(0, 6);
        
        // Limpa a lista atual
        recentPostsList.innerHTML = '';
        
        // Adiciona cada post selecionado
        selectedPosts.forEach(post => {
            const li = document.createElement('li');
            li.innerHTML = `
                <a href="${post.link}" target="_blank">
                    <strong>${post.title}</strong><br>
                    <small>${post.excerpt}</small>
                    <span class="post-date">(${formatRelativeDate(post.date)})</span>
                </a>
            `;
            recentPostsList.appendChild(li);
        });
    }

    // Função para iniciar a rotação de posts recentes
    function startRecentPostsRotation() {
        // Gera os primeiros posts imediatamente
        generateRandomRecentPosts();
        
        // Configura o intervalo para trocar os posts a cada 30 segundos
        recentPostsInterval = setInterval(generateRandomRecentPosts, 30000);
    }

    // Evento para carregar mais posts
    loadMoreBtn.addEventListener('click', function() {
        visiblePosts += postsPerLoad;
        renderPosts();
        
        // Rolagem suave para o final dos posts
        setTimeout(() => {
            postsContainer.scrollIntoView({ behavior: 'smooth', block: 'end' });
        }, 100);
    });

    // Função para ajustar layout responsivo
    function adjustLayout() {
        const posts = document.querySelectorAll('.post');
        
        if (window.innerWidth >= 992) {
            posts.forEach(post => {
                post.style.flex = '1 1 calc(33.333% - 14px)';
            });
        } else if (window.innerWidth >= 768) {
            posts.forEach(post => {
                post.style.flex = '1 1 calc(50% - 10px)';
            });
        } else {
            posts.forEach(post => {
                post.style.flex = '1 1 100%';
            });
        }
    }

    // Função para inscrição na newsletter
    function subscribe() {
        let phoneInput = document.getElementById("phone").value;
        let regex = /^\d{11}$/; // Aceita exatamente 11 dígitos sem formatação

        if (!regex.test(phoneInput)) {
            alert("Por favor, insira um telefone válido com 11 dígitos.");
            return;
        }

        // Formata o número para exibição (opcional)
        let formattedPhone = phoneInput.replace(/(\d{2})(\d{5})(\d{4})/, '$1-$2-$3');
        
        let url = `https://api.whatsapp.com/send/?phone=5516993427665&text=Olá, Dra. Gabrielle, tudo bem?%0AGostaria de mais informações sobre os tratamentos%0AMeu telefone: ${formattedPhone}&type=phone_number&app_absent=0`;
        window.open(url, "_blank");
    }

    // Validação em tempo real para aceitar apenas números
    document.getElementById('phone').addEventListener('input', function(e) {
        this.value = this.value.replace(/\D/g, ''); // Remove tudo que não for dígito
    });

    // Inicialização
    document.addEventListener('DOMContentLoaded', function() {
        renderPosts();
        startRecentPostsRotation();
        adjustLayout();
        
        window.addEventListener('resize', adjustLayout);
    });

    // Limpar intervalo quando a página for fechada
    window.addEventListener('beforeunload', function() {
        clearInterval(recentPostsInterval);
    });
</script>
</body>
</html>
