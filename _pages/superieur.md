---
layout: single
title: "Maths supérieures"
permalink: /superieur/
pdfs:
  - title: "Élément de cours et exercices — Arithmétique (sup)"
    file: "Elément de cours et exercices Arithmétique.pdf"
  - title: "Élément de cours et exercices — Analyse : bijectivité et fonctions réciproques (sup)"
    file: "Element de cours et exercices d' analyse bijectivité et fonctions réciproques.pdf"
  - title: "Éléments de cours et exercices — Dénombrement (sup)"
    file: "Éléments de cours et exercices  Dénombrement.pdf"
  - title: "FE15 Structures algébriques (sup)"
    file: "FE15 Structures algèbrique.pdf"
---

Bienvenue dans la section « Maths supérieures ».

<div class="notice--warning" style="margin:1rem 0; padding:0.75rem 1rem">
  <strong>Note :</strong> cette section est en cours de construction ; certains contenus et documents PDF peuvent contenir des erreurs.
  Merci de signaler toute correction à <a href="mailto:nour.coding@gmail.com">nour.coding@gmail.com</a>.
</div>

<h2>Documents (Maths sup)</h2>

<ul>
{% for doc in page.pdfs %}
  <li>
    <a href="{{ '/assets/pdf/sup/' | append: doc.file | relative_url }}" target="_blank" rel="noopener">{{ doc.title }}</a>
  </li>
{% endfor %}
</ul>
