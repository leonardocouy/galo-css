# 🐓 GaloDoido.css

**Framework CSS Extremista do Atlético Mineiro**

> "Ditadura Total: Preto & Branco, sem meio termo!"

Um framework CSS agressivo que força qualquer página web a adotar a identidade visual icônica do **Clube Atlético Mineiro**: **Preto e Branco absolutos**.

Inspirado pelo mascote caótico **Galo Doido** e pela paixão da **Massa Atleticana**, este framework usa `!important` em TODAS as regras para garantir domínio total sobre qualquer estilo existente.

---

## 🌐 Demo Online

**Veja o framework em ação:** [https://leonardocouy.github.io/galo-css/](https://leonardocouy.github.io/galo-css/)

---

## ✨ Características

- 🎨 **Ditadura P&B:** Força TODOS os elementos a serem preto (#000000) ou branco (#FFFFFF)
- 🐓 **Cursor Galo Doido:** Substitui o cursor padrão pelo mascote
- 🚫 **Bloqueio Rival:** Esconde automaticamente elementos com "blue", "cruzeiro", "maria"
- 🏟️ **Locais Sagrados:** Destaque especial para IDs de estádios do Galo
- ⚡ **Efeito Bicada:** Links invertem cores rapidamente no hover (0.15s)
- 🖼️ **Filtro Grayscale:** Todas as imagens em P&B (exceto `.galo-oficial`)
- 💪 **100% CSS:** Zero JavaScript, zero dependências, zero build tools

---

## 🚀 Instalação e Uso

### Método 1: Link Direto (Recomendado)

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="galodoido.css">
</head>
<body>
    <h1>Aqui é Galo!</h1>
</body>
</html>
```

### Método 2: Import CSS

```css
@import url('galodoido.css');
```

### Método 3: Injeção Dinâmica (Modo Troll)

Para "galoizar" qualquer site, use este bookmarklet JavaScript:

```javascript
javascript:(function(){
    var link = document.createElement('link');
    link.rel = 'stylesheet';
    link.href = 'https://seu-dominio.com/galodoido.css';
    document.head.appendChild(link);
    alert('Site GALOIZADO! Aqui é Galo! 🐓');
})();
```

**Como usar o bookmarklet:**
1. Crie um novo favorito no navegador
2. Cole o código acima no campo URL
3. Visite qualquer site e clique no favorito
4. Veja a mágica acontecer!

---

## 📚 Documentação

### Component Library

Abra `docs/index.html` no navegador para ver a documentação interativa completa com exemplos de todos os componentes e regras CSS.

### Demo Completo

Abra `docs/demo/news-site.html` para ver uma transformação antes/depois de um site de notícias completo.

---

## 🎨 Regras CSS

### 1. Ditadura das Cores

```css
* {
    color: white !important;
    background-color: black !important;
    border-color: white !important;
}
```

**Efeito:** TODO elemento fica preto e branco, sem exceções.

### 2. Cursor Personalizado

```css
* {
    cursor: url('assets/galo-cursor-32.png'), auto !important;
}
```

**Efeito:** Cursor do mouse vira o mascote Galo Doido.

### 3. Links (Efeito Bicada)

```css
a:hover {
    color: black !important;
    background-color: white !important;
    transition: all 0.15s ease-in-out !important;
}
```

**Efeito:** Links invertem cores rapidamente no hover, simulando uma bicada.

### 4. Filtro de Imagens

```css
img:not(.galo-oficial) {
    filter: grayscale(100%) contrast(120%) !important;
}
```

**Efeito:** Todas as imagens ficam em escala de cinza, exceto as com classe `.galo-oficial`.

**Exceção:**
```html
<img src="escudo-galo.png" class="galo-oficial" alt="Escudo do Galo">
```

### 5. Bloqueio de Rivais

```css
[class*="blue"],
[class*="cruzeiro"],
[id*="maria"] {
    display: none !important;
    visibility: hidden !important;
}
```

**Efeito:** Elementos com "blue", "cruzeiro", ou "maria" no nome da classe/ID desaparecem! 🚫

### 6. Locais Sagrados

```css
#mineirao, #independencia, #arena-mrv, #horto {
    border: 5px solid white !important;
    font-weight: 900 !important;
    text-transform: uppercase !important;
}
```

**Efeito:** Elementos com IDs de estádios históricos recebem destaque especial.

**IDs reconhecidos:**
- `#mineirao` - Gigante da Pampulha
- `#independencia` - Estádio Independência
- `#arena-mrv` - Arena MRV (nova casa)
- `#horto` - Local do Milagre da Libertadores 2013

---

## 🏗️ Estrutura do Projeto

```
galo-css/
├── galodoido.css           # Framework principal
├── assets/
│   ├── galo-cursor-32.png  # Cursor otimizado (32x32)
│   ├── galo-cursor.png     # Cursor original
│   └── galo-logo-128.png   # Logo para branding
├── docs/
│   ├── index.html          # Component library (Storybook-style)
│   ├── components/
│   │   └── images.html     # Demo de filtros de imagem
│   └── demo/
│       └── news-site.html  # Demo completo (site de notícias)
└── README.md               # Este arquivo
```

---

## 🎭 Casos de Uso

### 1. Homenagem ao Galo
Use em sites pessoais de torcedores para demonstrar paixão atleticana.

### 2. Ferramenta Educacional
Demonstração poderosa de CSS specificity e `!important` para estudantes de frontend.

### 3. Modo Troll (Responsável)
Injeção temporária em sites para brincadeiras entre amigos torcedores.

### 4. Tema Alternativo
Use como tema alternativo "dark mode P&B" em projetos pessoais.

---

## ⚠️ Avisos Importantes

### Desempenho
- O uso extensivo de `!important` e seletores universais pode impactar performance
- Recomendado apenas para fins demonstrativos ou projetos pequenos

### Acessibilidade
- Este framework **NÃO** é otimizado para acessibilidade
- Contraste P&B pode dificultar leitura para alguns usuários
- Não recomendado para sites de produção que precisam cumprir WCAG

### Compatibilidade
- **Suportado:** Chrome, Firefox, Safari, Edge (versões modernas)
- **CSS Features:** Todos os recursos são bem suportados (sem necessidade de prefixos vendor)
- **Cursor customizado:** Funciona em todos os navegadores modernos

### Falsos Positivos
- Elementos com "blue", "blueberry", "bluetooth" serão bloqueados
- Elementos com "maria" (nomes próprios) serão bloqueados
- Considere isso uma "feature, not a bug" 😄

---

## 🎨 Personalização

### Desabilitando Bloqueio de Rivais

Se você quiser usar o framework sem o bloqueio de elementos rivais, comente as seguintes linhas em `galodoido.css`:

```css
/* Comentar estas linhas:
[class*="blue"],
[class*="cruzeiro"],
[id*="maria"] {
    display: none !important;
    visibility: hidden !important;
}
*/
```

### Ajustando Cores de Links Visitados

Altere a cor dos links visitados editando:

```css
a:visited {
    color: #666666 !important; /* Ajuste aqui */
}
```

---

## 🐓 Cultura Galoista

Este framework incorpora elementos da rica cultura atleticana:

### Gritos de Guerra
- "Aqui é Galo!"
- "Eu Acredito!"
- "Caiu no Horto, tá morto!" (Milagre 2013)
- "Galo Forte Vingador!"
- "Massa Atleticana presente!"

### Locais Históricos
- **Mineirão** - Gigante da Pampulha
- **Independência** - Palco de glórias no Horto
- **Arena MRV** - Nova casa do Galo
- **Horto** - Local do Milagre da Libertadores 2013

### Momentos Memoráveis
- **Libertadores 2013** - Título continental épico
- **Brasileiro 1971** - Primeiro título nacional
- **Brasileiro 2021** - Título do centenário
- **Milagre do Horto** - Defesas históricas de Victor

---

## 📄 Licença

Este é um projeto de demonstração e homenagem ao Clube Atlético Mineiro.

**Uso educacional e demonstrativo:** Livre
**Uso comercial:** Consulte os direitos de imagem do clube

---

## 🤝 Contribuindo

Este é um projeto de demonstração. Sugestões e melhorias são bem-vindas!

### Ideias para Contribuição:
- Adicionar mais locais sagrados
- Criar variações temáticas (ex: modo "Libertadores", modo "Brasileiro")
- Melhorar performance do seletor universal
- Adicionar mais Easter eggs da cultura galoista
- Criar versão "lite" sem bloqueio de rivais

---

## 🏆 Títulos do Galo (Para Contexto)

- 🏆 **Copa Libertadores:** 2013
- 🏆 **Campeonato Brasileiro:** 1971, 2021
- 🏆 **Copa do Brasil:** 2014, 2021
- 🏆 **Recopa Sul-Americana:** 2014
- 🏆 **Campeonato Mineiro:** 48 títulos
- 🏆 **Supercopa do Brasil:** 2022

---

## 📞 Contato

Para dúvidas, sugestões ou apenas para gritar "Aqui é Galo!":

- **Projeto Galo Doido:** [github.com/seu-usuario/galo-doido](https://github.com)
- **Site Oficial do Galo:** [atletico.com.br](https://atletico.com.br)

---

<div align="center">

**🐓 Aqui é Galo! 🐓**

*"Caiu no Horto, tá morto!"*

**Preto & Branco Forever** ⚫⚪

*Massa Atleticana - Desde 1908*

</div>
