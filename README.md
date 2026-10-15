# Biblioteca Digital UniFECAF

Projeto acadêmico da disciplina **Design Web**: uma primeira interface para a
Biblioteca Digital UniFECAF, construída com HTML semântico e CSS, sem frameworks
ou construtores de sites.

**Autor: Álvaro Sena**

## Identidade visual

A paleta prioriza o azul institucional da UniFECAF, com tons suaves de azul nos
fundos e pequenos detalhes verdes para complementar a composição.

## Objetivo

Transformar a proposta de uma biblioteca digital em uma página clara, responsiva
e acessível para apresentar sugestões de livros acadêmicos e facilitar a
navegação por áreas de conhecimento. Esta é uma demonstração independente para
apresentação em sala, não um catálogo institucional em funcionamento.

## Tecnologias

- HTML5 para estrutura e conteúdo;
- CSS3 para identidade visual, layout responsivo, estados de foco e movimento reduzido;
- SVGs locais para as ilustrações e capas de destaque;
- cinco arquivos de texto com prévias fictícias para testar os downloads.

Não há dependências externas, processo de compilação ou JavaScript.

## Estrutura

```text
biblioteca-unifecaf/
├── index.html
├── README.md
├── .github/
│   └── workflows/
│       └── pages.yml
├── css/
│   └── style.css
└── assets/
    ├── imagens/
    │   ├── capa-design.svg
    │   ├── capa-educacao.svg
    │   ├── capa-negocios.svg
    │   ├── capa-psicologia.svg
    │   ├── capa-tecnologia.svg
    │   └── hero-livros.svg
    └── previews/
        ├── previa-entre-linhas-e-codigos.txt
        ├── previa-formas-de-amanha.txt
        ├── previa-ideias-em-movimento.txt
        ├── previa-mapa-dos-habitos.txt
        └── previa-sala-das-descobertas.txt
```

## Como abrir

1. Baixe ou clone o repositório.
2. Abra `index.html` em um navegador.
3. Para editar, abra a pasta do projeto no VS Code e altere `index.html` ou `css/style.css`.

Os caminhos de CSS e imagens são relativos, então a página também funciona em hospedagem estática, como o GitHub Pages.

## Funcionalidades

- navegação interna para as seções e os livros;
- apresentação de cinco livros e autores fictícios;
- botão “Saiba mais” para abrir a descrição de cada título, usando o elemento HTML `details`;
- botão “Baixar prévia fictícia” em cada livro: baixa um arquivo `.txt` de demonstração, não um livro completo;
- categorias que levam ao livro correspondente na própria página;
- layout adaptado para computadores e smartphones;
- link para pular ao conteúdo, textos alternativos nas imagens e destaque de foco por teclado;
- suporte à preferência do sistema por movimento reduzido.

Os cinco livros, autores, capas, descrições e arquivos de prévia são fictícios e
foram criados para esta demonstração. A página não tem busca, empréstimo, login,
disponibilidade real ou conexão com serviços da UniFECAF.

## Testes realizados

- Página aberta no navegador a partir do arquivo local;
- imagens SVG carregadas e caminhos locais conferidos;
- navegação interna e destinos dos links conferidos;
- visualização testada em larguras de 320, 375, 768 e 1440 pixels, sem rolagem horizontal;
- controles “Saiba mais” e links das áreas conferidos no navegador;
- os cinco arquivos para download conferidos no navegador local (resposta HTTP 200).

## Publicar no GitHub Pages

### 1. Criar o repositório

No GitHub, crie um repositório público chamado `biblioteca-unifecaf`. Para
seguir os comandos abaixo, deixe a opção de adicionar README desmarcada, pois
este projeto já inclui um.

### 2. Enviar os arquivos pelo PowerShell

Abra o PowerShell e execute os comandos abaixo. Substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub:

```powershell
Set-Location 'C:\Users\user\Desktop\FECAF\TRABALHOS\AULAHTML'
git init -b main
git rev-parse --show-toplevel
git add index.html README.md css/style.css assets
git commit -m "Cria site da Biblioteca Digital UniFECAF"
git remote add origin https://github.com/SEU-USUARIO/biblioteca-unifecaf.git
git push -u origin main
```

Confirme que `git rev-parse --show-toplevel` mostra a pasta `AULAHTML` antes de
adicionar ou enviar arquivos. Se o Git informar que o repositório já foi
inicializado, não repita `git init`; confira se o terminal está dentro da pasta
deste projeto. Caso o comando de commit peça sua identificação, configure seu
nome e e-mail do Git:

```powershell
git config --global user.name "Seu nome"
git config --global user.email "seu-email@example.com"
```

Use um e-mail que você esteja confortável em associar aos commits. Nunca coloque
senha ou token nos comandos, arquivos do projeto ou repositório.

### 3. Ativar o GitHub Pages

1. Abra `https://github.com/SEU-USUARIO/biblioteca-unifecaf` e acesse **Settings**.
2. No menu lateral, abra **Pages**.
3. Em **Build and deployment**, escolha **GitHub Actions** como fonte de publicação.
4. Acesse **Actions**, abra o workflow **Publicar site no GitHub Pages** e clique em **Re-run jobs** para repetir a primeira publicação.
5. Quando a execução terminar com sucesso, o endereço será `https://SEU-USUARIO.github.io/biblioteca-unifecaf/`.

O workflow em `.github/workflows/pages.yml` publica automaticamente o site a cada
envio para a branch `main`. A primeira execução requer que uma pessoa com acesso
de administrador ative **GitHub Actions** como fonte na configuração **Pages**.

Após novas alterações, envie-as com:

```powershell
git add index.html README.md css/style.css assets
git commit -m "Atualiza site da biblioteca"
git push
```

## Referências da atividade

- [Biblioteca UniFECAF](https://www.unifecaf.com.br/biblioteca)
- [W3Schools](https://www.w3schools.com/)
- [Material Design](https://m2.material.io/)
- [Elementos HTML — MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element)
- [Bootstrap](https://getbootstrap.com/)

O Bootstrap foi consultado como material de referência, mas não foi incluído
como dependência: o layout foi desenvolvido diretamente em CSS, conforme os
requisitos da atividade.
