# Old, Chefe

**Descrição**

Este pequeno projeto é uma página interativa em HTML/CSS/JS que simula um diálogo cômico entre um funcionário e o chefe, com botões para aceitar ou recusar um aumento. Ao aceitar, aparece uma tela de confirmação; ao recusar, o botão "Não" foge do mouse.

---

## Funcionalidades principais

* Tela inicial com pergunta e dois botões: **"Claro, Meu Melhor Funcionário"** e **"Não"**.
* Botão **"Não"** foge do cursor quando o usuário passa o mouse sobre ele.
* Ao clicar no botão **"Claro, Meu Melhor Funcionário"**, a página mostra uma tela de confirmação (page2).
* Versão atual: o botão de confirmação pode substituir o conteúdo por um ícone de check (arquivo `img/check.png`) — isto foi implementado via JavaScript.

---

## Requisitos

* Navegador moderno (Chrome, Firefox, Edge, Safari)
* Estrutura de arquivos local com a pasta `img/` contendo as imagens usadas no projeto

---

## Como executar

1. Clone ou copie os arquivos para uma pasta local.
2. Abra `index.html` em um navegador (duplo clique ou arraste para o navegador).

> Não é necessário servidor — é uma página estática. Se preferir usar um servidor local (por exemplo `live-server`), também funciona.

---

## Estrutura de arquivos (exemplo)

```
project-root/
├─ index.html
├─ img/
│  ├─ chuva.gif
│  ├─ goku.gif
│  ├─ urso-pidao.png
│  └─ check.png    <-- ícone de check que aparece na confirmação
```

---

## Código relevante / personalizações rápidas

### 1. Substituir o texto por um ícone de check

* Coloque o ícone desejado dentro da pasta `img/` com o nome `check.png` (ou ajuste o `src` no script).
* O comportamento já proposto no `index.html` altera o conteúdo da `.confirmation-card` para exibir apenas o ícone quando o botão de confirmação for clicado.

### 2. Remover a ação de voltar

* A implementação atual remove a lógica de "voltar" ao clicar no botão de confirmação e apenas troca o conteúdo por um check. Se quiser que o modal/overlay feche definitivamente, remova qualquer código que faça `classList.remove('show')`/`classList.remove('hidden')` e, se necessário, desative o botão.

### 3. Trocar imagens ou textos

* Para trocar qualquer imagem, substitua o arquivo dentro de `img/` mantendo o mesmo nome, ou atualize as referências no HTML/CSS.
* Para alterar textos (títulos, subtítulos, atributos), edite o HTML dentro de `.confirmation-card`.

---

## Estilos e responsividade

* O layout usa regras CSS simples e inclui media queries para telas menores (até 768px).
* A confirmação é posicionada como um card central com `backdrop` (fundo do `body` continua visível). Para alterar esse comportamento (por exemplo, fundo sólido), edite a regra `.page2` no CSS.

---

## Acessibilidade e melhorias sugeridas

* Adicionar `aria-labels` nos botões (`yesBtn`, `noBtn`, `confirmBtn`) para leitores de tela.
* Garantir contraste suficiente entre texto e fundo para melhor legibilidade.
* Fornecer fallback caso imagens não carreguem (atributo `alt`).
* Desativar movimento infinito (animação `bounce`) em preferências do usuário que reduzem movimento.

---

## Licença

Sinta-se à vontade para usar e modificar este projeto para fins pessoais e educacionais. Não há restrições específicas de distribuição — se quiser, adicione uma licença (por exemplo MIT) aqui.