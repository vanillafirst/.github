# Contribuindo com o VanillaFirst

Obrigado por fortalecer o movimento. O VanillaFirst existe para provar que a base da tecnologia é robusta o suficiente para resolver problemas reais. Nossa regra principal é simples: **tente o código puro antes do framework.**

## Regras de Ouro

1. **Zero Dependências:** O projeto não deve exigir a instalação de pacotes de terceiros (nada de `npm install`, `pip install` para libs externas ou `composer require`). Utilize apenas a biblioteca padrão (Standard Library) de cada linguagem e APIs nativas dos navegadores.
2. **Código Legível:** Escreva de forma que outro desenvolvedor entenda facilmente. Evite abstrações complexas e priorize a clareza.
3. **Sem Clichês:** Documentação e comentários devem ir direto ao ponto, explicando o *porquê* daquela lógica existir.

## Padrões Técnicos Exigidos

Para garantir a qualidade e a segurança do que construímos, todo código enviado deve respeitar os seguintes critérios:

### Front-end
* **Estrutura e Estilo:** Use HTML5 semântico (`<header>`, `<article>`, `<section>`, etc.) e CSS3 (aproveitando custom properties/variáveis).
* **JavaScript:** 100% puro (Vanilla JS). Gerencie eventos de forma limpa (ex: `DOMContentLoaded`, `defer`).
* **Experiência:** O layout deve ter compatibilidade cross-browser (desktop e mobile).
* **Acessibilidade e SEO:** É obrigatório o uso de atributos `alt` em imagens, navegação acessível por teclado, `aria-label` quando necessário e hierarquia correta de títulos (H1, H2, etc.).
* **Performance:** Aplique técnicas nativas de otimização, como carregamento preguiçoso (`loading="lazy"`) em imagens.

### Back-end
* **Tratamento de Erros:** Não ignore falhas. Estruture blocos de `try/catch` de forma adequada e devolva mensagens de erro claras.
* **Comentários:** Siga o padrão da linguagem escolhida (Docstrings para Python, PHPDoc para PHP, etc.).

### Segurança (Inadiável)
* **Proteção de Dados:** Nunca confie no input do usuário. Faça a validação e a sanitização rigorosa diretamente no back-end.
* **Vulnerabilidades:** Aplique proteção contra XSS (escapando saídas) e CSRF (usando tokens em formulários).
* **Comunicação:** Configure políticas de CORS de forma estrita e segura. Nunca armazene senhas em texto puro.

## Como enviar seu Pull Request (PR)

1. Faça o Fork do repositório.
2. Crie uma branch para sua funcionalidade (`git checkout -b minha-solucao-nativa`).
3. Faça commits claros explicando o que foi feito.
4. Abra o PR detalhando o problema resolvido e garantindo na descrição que nenhuma biblioteca externa foi utilizada.

Todo código será revisado pela comunidade para garantir que a filosofia VanillaFirst seja mantida.
