# 🎨 Resumo de CSS (Cascading Style Sheets)

## 📌 1. O que é CSS?
CSS é a linguagem usada para definir a aparência dos elementos HTML em uma página web, separando **estrutura** (HTML) de **estilo** (CSS).

---

## 🧱 2. Formas de Aplicar CSS

| Tipo      | Exemplo                                         | Observações                            |
|-----------|--------------------------------------------------|----------------------------------------|
| Inline    | `<p style="color:red;">Texto</p>`               | Não recomendado para projetos grandes  |
| Interno   | `<style> p { color: red; } </style>`            | Dentro da tag `<head>`                 |
| Externo   | `<link rel="stylesheet" href="style.css">`      | Recomendado, facilita manutenção       |

---

## 🎯 3. Seletores Comuns

| Seletor           | Exemplo               | Descrição                                  |
|-------------------|-----------------------|--------------------------------------------|
| Universal         | `*`                   | Seleciona todos os elementos               |
| Tipo (tag)        | `p`, `h1`             | Seleciona todas as tags `p`, `h1`, etc.    |
| Classe            | `.menu`               | Seleciona todos com `class="menu"`         |
| ID                | `#topo`               | Seleciona o elemento com `id="topo"`       |
| Descendente       | `div p`               | Seleciona `<p>` dentro de `<div>`          |
| Filho direto      | `ul > li`             | Seleciona `<li>` filho direto de `<ul>`    |
| Irmão adjacente   | `h1 + p`              | Seleciona `<p>` imediatamente após `<h1>`  |
| Atributo          | `input[type="text"]`  | Seleciona `input` com tipo `text`          |

---

## 🎨 4. Principais Propriedades

### 🔤 Propriedades de Texto

| Propriedade        | Descrição                                      |
|--------------------|------------------------------------------------|
| `color`            | Define a cor do texto                          |
| `font-size`        | Define o tamanho da fonte                      |
| `font-family`      | Define o tipo de fonte usada                   |
| `font-weight`      | Define a espessura da fonte (normal, bold...)  |
| `text-align`       | Alinhamento do texto (left, center, right)    |
| `text-decoration`  | Sublinhado, linha acima, etc                   |
| `text-transform`   | Transforma texto em maiúsculas, minúsculas... |
| `line-height`      | Espaçamento entre linhas                       |
| `letter-spacing`   | Espaçamento entre letras                       |

---

### 📦 Propriedades de Caixa & Layout

| Propriedade       | Descrição                                       |
|-------------------|-------------------------------------------------|
| `width`, `height` | Define largura e altura do elemento             |
| `padding`         | Espaço interno entre conteúdo e borda           |
| `margin`          | Espaço externo entre elementos                  |
| `border`          | Define borda do elemento                        |
| `border-radius`   | Arredonda os cantos da borda                    |
| `box-sizing`      | Controla como o tamanho do box é calculado     |
| `display`         | Tipo de renderização (block, inline, flex...)  |
| `position`        | Tipo de posicionamento (relative, absolute...) |
| `top`, `left`     | Posição em relação ao pai ou tela              |
| `z-index`         | Ordem de sobreposição                          |
| `overflow`        | Como tratar conteúdo que ultrapassa o elemento |
| `float`, `clear`  | Posicionamento lateral (antigo layout)         |

---

### 🧭 Propriedades de Flexbox

| Propriedade         | Descrição                                       |
|---------------------|-------------------------------------------------|
| `display: flex`     | Ativa o Flexbox                                 |
| `flex-direction`    | Direção dos itens (row, column...)              |
| `justify-content`   | Alinhamento horizontal dos itens                |
| `align-items`       | Alinhamento vertical dos itens                  |
| `flex-wrap`         | Permite quebra de linha dos itens               |
| `gap`               | Espaçamento entre os itens do flex container    |

---

### 🎥 Animação e Transição

| Propriedade      | Descrição                                          |
|------------------|----------------------------------------------------|
| `transition`     | Transição suave entre valores de propriedades      |
| `transform`      | Transforma elemento (rotate, scale, translate...)  |
| `animation`      | Controla animações personalizadas (keyframes)      |
| `opacity`        | Define opacidade do elemento (0 a 1)               |

---

### 🎲 Propriedades de Fundo (Background)

| Propriedade           | Descrição                                     |
|------------------------|----------------------------------------------|
| `background-color`     | Cor de fundo                                 |
| `background-image`     | Imagem de fundo                              |
| `background-size`      | Tamanho da imagem (cover, contain, px...)    |
| `background-repeat`    | Repetição da imagem (repeat, no-repeat...)   |
| `background-position`  | Posição da imagem (top, center, left...)     |

---

### 🖱️ Outras Propriedades Úteis

| Propriedade        | Descrição                                 |
|--------------------|--------------------------------------------|
| `cursor`           | Define o tipo de cursor do mouse          |
| `visibility`       | Visibilidade do elemento (`visible`, `hidden`) |
| `box-shadow`       | Sombra ao redor do elemento               |
| `outline`          | Contorno (sem ocupar espaço como a borda) |

---

## 📏 5. Unidades de Medida

| Unidade | Exemplo  | Base                                      |
|---------|----------|-------------------------------------------|
| `px`    | `16px`   | Tamanho fixo                              |
| `%`     | `50%`    | Relativo ao elemento pai                  |
| `em`    | `1.5em`  | Relativo ao tamanho da fonte do elemento pai |
| `rem`   | `1.5rem` | Relativo à fonte do elemento raiz `<html>` |
| `vw`    | `100vw`  | Largura da viewport                       |
| `vh`    | `100vh`  | Altura da viewport                        |

---

## 🧠 6. Especificidade e Cascata

### Prioridade de Estilos:
1. Inline (`style=""`) — mais forte  
2. ID (`#exemplo`)  
3. Classe (`.exemplo`) / Atributo / Pseudo-classe  
4. Elemento (`p`, `div`, etc.)

> O último estilo lido substitui os anteriores se tiver mesma prioridade.

---

## ✅ 7. Boas Práticas

- Use **CSS externo**
- Prefira **classes** a IDs para reutilização
- Use **nomes claros** e semânticos
- Evite o uso de `!important`
- Use `box-sizing: border-box`
- Aplique `reset.css` ou `normalize.css` para compatibilidade entre navegadores

---

## 💡 8. Exemplo Prático

```css
/* Estilo de um botão */
.botao {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.botao:hover {
  background-color: #2980b9;
}
