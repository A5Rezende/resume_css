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

| Seletor           | Exemplo               | Descrição                                 |
|-------------------|------------------------|--------------------------------------------|
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

### 🔤 Texto
- `color`
- `font-size`
- `font-family`
- `font-weight`
- `text-align`
- `text-decoration`
- `text-transform`
- `line-height`
- `letter-spacing`

### 📦 Caixa & Layout
- `width`, `height`
- `padding`, `margin`
- `border`, `border-radius`
- `box-sizing: border-box`
- `display`, `position`, `z-index`
- `overflow`, `float`, `clear`

### 🧭 Flexbox
- `display: flex`
- `justify-content`
- `align-items`
- `flex-direction`
- `gap`, `flex-wrap`

### 🎥 Animação
- `transition`
- `transform`
- `animation`
- `opacity`

### 🎲 Fundo
- `background-color`
- `background-image`
- `background-size`
- `background-repeat`
- `background-position`

### 🖱️ Outros
- `cursor`
- `visibility`
- `box-shadow`
- `outline`

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
