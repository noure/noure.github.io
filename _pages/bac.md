---
layout: single
title: "Science maths (BAC)"
permalink: /bac/
pdfs:
  - title: "Élément de cours et exercices — Arithmétique"
    file: "Elément de cours et exercices Arithmétique.pdf"
  - title: "Élément de cours et exercices — Analyse: bijectivité et fonctions réciproques"
    file: "Element de cours et exercices d' analyse bijectivité et fonctions réciproques.pdf"
  - title: "FE01 Sommes et récurrences"
    file: "FE01 sommes et récurrences.pdf"
  - title: "FE02 Limites et continuités"
    file: "FE02 Limites et continuités.pdf"
  - title: "FE03 Généralités sur les suites"
    file: "FE03 Généralité sur les suites.pdf"
  - title: "FE04 Suites — convergence"
    file: "FE04 Suites convergence.pdf"
  - title: "FE04 Bis — Fonctions réciproques"
    file: "FE04 Bis les fonctions réciproques.pdf"
  - title: "FE05 Dérivation (1/2)"
    file: "FE05 Dérivation 1 sur 2.pdf"
  - title: "FE05 Dérivation (2/2) — Primitives"
    file: "FE05 Dérivation 2 sur 2( Primitves).pdf"
  - title: "FE06 Suites récurrentes"
    file: "FE06 Suites récurrentes.pdf"
  - title: "FE07 Dérivation et bijection"
    file: "FE07 Dérivation et bijection.pdf"
  - title: "FE08 Suites implicites"
    file: "FE08 Suites implicites.pdf"
  - title: "FE09 Études de fonctions"
    file: "FE09 Etudes de fonctions.pdf"
  - title: "FE10 Calcul intégral (1/3)"
    file: "FE10 Calcul intégrale 1 sur 3.pdf"
  - title: "FE11 Calcul intégral (2/3)"
    file: "FE11 calcul intégrale 2 sur 3.pdf"
  - title: "FE12 Calcul intégral (3/3)"
    file: "FE12 Calcul intégrale 3 sur 3.pdf"
  - title: "FE13 Nombres complexes"
    file: "FE13 Les nombres complexes.pdf"
---

Bienvenue dans la section « Science maths (BAC) ».

<h2>Documents</h2>

<!-- Menu de filtrage/accès rapide -->
<div class="notice--primary" style="padding:1rem; margin-bottom:1rem">
  <form id="filtre-bac" onsubmit="return false;" style="display:flex; gap:.5rem; flex-wrap:wrap; align-items:center">
    <label for="q" style="margin-right:.25rem">Rechercher:</label>
    <input type="search" id="q" placeholder="Titre, FE01, dérivation…" style="flex:1; min-width:220px" />

    <label for="groupe" style="margin-left:.5rem">Groupe:</label>
    <select id="groupe">
      <option value="">Tous</option>
      <option value="cours">Éléments de cours</option>
      <option value="fe">Fiches FE</option>
      <option value="analyse">Analyse</option>
      <option value="suites">Suites</option>
      <option value="derivation">Dérivation / Primitives</option>
      <option value="integrale">Calcul intégral</option>
      <option value="complexes">Nombres complexes</option>
    </select>

    <a href="#" id="reset" class="btn btn--small">Réinitialiser</a>
  </form>
</div>

<ul id="liste-pdfs">
{% for doc in page.pdfs %}
  {% assign t = doc.title | downcase %}
  {% assign tags = '' %}
  {% if t contains 'élément' or t contains 'element' %}{% assign tags = tags | append: ' cours' %}{% endif %}
  {% if t contains 'fe0' %}{% assign tags = tags | append: ' fe' %}{% endif %}
  {% if t contains 'suite' %}{% assign tags = tags | append: ' suites analyse' %}{% endif %}
  {% if t contains 'dérivation' or t contains 'derivation' or t contains 'primitive' %}{% assign tags = tags | append: ' derivation analyse' %}{% endif %}
  {% if t contains 'intégral' or t contains 'integral' %}{% assign tags = tags | append: ' integrale analyse' %}{% endif %}
  {% if t contains 'fonction' %}{% assign tags = tags | append: ' analyse' %}{% endif %}
  {% if t contains 'complexe' %}{% assign tags = tags | append: ' complexes' %}{% endif %}
  <li data-tags="{{ tags | strip }}">
    <a href="{{ '/assets/pdf/bac/' | append: doc.file | relative_url }}" target="_blank" rel="noopener">
      {{ doc.title }}
    </a>
  </li>
{% endfor %}
</ul>

<script>
(function(){
  var q = document.getElementById('q');
  var groupe = document.getElementById('groupe');
  var reset = document.getElementById('reset');
  var items = Array.prototype.slice.call(document.querySelectorAll('#liste-pdfs > li'));

  function normalise(s){ return (s||'').toLowerCase().normalize('NFD').replace(/[\u0300-\u036f]/g,''); }

  function filtre(){
    var qv = normalise(q.value);
    var gv = normalise(groupe.value);
    items.forEach(function(li){
      var text = normalise(li.textContent);
      var tags = normalise(li.getAttribute('data-tags'));
      var okText = !qv || text.indexOf(qv) !== -1;
      var okTag = !gv || (tags && tags.split(/\s+/).indexOf(gv) !== -1);
      li.style.display = (okText && okTag) ? '' : 'none';
    });
  }

  q.addEventListener('input', filtre);
  groupe.addEventListener('change', filtre);
  reset.addEventListener('click', function(e){ e.preventDefault(); q.value=''; groupe.value=''; filtre(); });
})();
</script>
