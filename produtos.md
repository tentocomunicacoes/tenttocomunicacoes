---
layout: default
title: Todos os Produtos
permalink: /produtos/
---

# Todos os Produtos

<div class="produtos-grid">
  {% for produto in site.produtos %}
    <div class="produto-card">
      <a href="{{ produto.url | relative_url }}">
        <img src="{{ produto.image | relative_url }}" alt="{{ produto.title }}">
        <h3>{{ produto.title }}</h3>
        <p class="preco">R$ {{ produto.price | number_format: 2, ',', '.' }}</p>
      </a>
      <button class="adicionar-carrinho" data-id="{{ produto.id }}" data-titulo="{{ produto.title }}" data-preco="{{ produto.price }}">Adicionar ao Carrinho</button>
    </div>
  {% endfor %}
</div>
