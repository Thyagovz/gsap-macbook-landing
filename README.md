# Macbook Pro Experience — Creative Web Development

Uma vitrine interativa e de alta performance desenvolvida para apresentar o MacBook Pro, focada em experiências imersivas de renderização 3D e animações complexas baseadas em scroll. O projeto explora a convergência entre o desenvolvimento frontend tradicional e o *creative coding*.

## Visão Geral

Este projeto é uma aplicação Single Page Application (SPA) que utiliza tecnologias de ponta para renderização gráfica no navegador. O objetivo principal é proporcionar uma experiência de usuário fluida e visualmente impactante, simulando a precisão e estética de produtos premium. Através da integração de modelos 3D interativos e uma timeline de animação rigorosamente controlada, a aplicação demonstra capacidades avançadas de performance e fidelidade visual.

## Stack Tecnológica

### Core
- **React & Vite**: Base da aplicação para construção de interfaces reativas e um ambiente de desenvolvimento ultrarrápido com Hot Module Replacement (HMR).
- **Three.js & React Three Fiber (R3F)**: Motor de renderização 3D. O R3F é utilizado para declarar objetos Three.js como componentes React, facilitando a gestão do ciclo de vida da cena 3D.
- **Drei**: Biblioteca de utilitários para R3F, utilizada para carregamento otimizado de modelos (GLTF), controle de câmeras e helpers de ambiente.

### Animação & Performance
- **GSAP (GreenSock Animation Platform)**: Utilizado para orquestrar todas as animações da interface.
    - `ScrollTrigger`: Sincronização de animações com o progresso do scroll.
    - `useGSAP`: Hook especializado para integração segura de animações no ciclo de vida do React.
- **React Responsive**: Gerenciamento de breakpoints para adaptação dinâmica de elementos 2D e 3D de acordo com a viewport.

### Estado & Estilização
- **Zustand**: Gerenciamento de estado global minimalista, utilizado para controlar propriedades do modelo 3D (cor, escala, texturas) de forma performática, evitando re-renders desnecessários.
- **TailwindCSS**: Framework utilitário para construção de uma UI sóbria, moderna e totalmente responsiva.

## Destaques Técnicos

### Renderização 3D & Pipeline
- **Modelo 3D Interativo**: Implementação de um MacBook Pro detalhado com suporte a interações em tempo real (rotação, troca de escala e cor).
- **Texturas de Vídeo Dinâmicas**: Utilização do `useVideoTexture` para renderizar vídeos diretamente na malha (mesh) da tela do MacBook, permitindo transições de conteúdo baseadas em eventos ou progresso de scroll.
- **Setup de Iluminação Customizado**: Implementação de `StudioLights` utilizando `Environment` e `Lightformer` para criar reflexos realistas e iluminação de estúdio de alta fidelidade.

### Orquestração de Scroll (GSAP Timeline)
As animações são controladas por timelines do GSAP scrubbed, garantindo que o progresso da animação esteja perfeitamente vinculado à posição do scroll do usuário. Isso inclui o movimento de componentes de hardware na seção de performance e a transição de estados da câmera na seção de funcionalidades.

### Performance & Otimização
- **Lazy Loading**: Modelos e ativos pesados são carregados de forma assíncrona para garantir um First Contentful Paint (FCP) baixo.
- **Estado Atômico**: Uso do Zustand para atualizações de propriedades específicas do Three.js, minimizando a carga no thread principal do React.

## Funcionalidades
- **Visualizador de Produto**: Troca em tempo real entre modelos de 14" e 16" e variações de cores.
- **Scroll-driven Animations**: Experiência narrativa onde os componentes do hardware e as informações técnicas surgem conforme o scroll.
- **Responsividade Total**: Layout e cena 3D adaptados para dispositivos móveis, garantindo performance e legibilidade.
- **Interatividade 3D**: Controle de apresentação (PresentationControls) que permite ao usuário explorar o modelo em 360 graus.

## Configuração e Instalação

### Pré-requisitos
- Node.js (v18+)
- Gerenciador de pacotes (npm, yarn ou pnpm)

### Execução
1. Instale as dependências:
   ```bash
   npm install
   ```
2. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
3. Para gerar o build de produção:
   ```bash
   npm run build
   ```

---

### Contato & Observações
Este é um projeto com fins de demonstração técnica e portfólio. Focado em demonstrar o potencial de tecnologias modernas de frontend para o mercado de luxo e tecnologia.

Desenvolvido com foco em precisão, performance e design.
