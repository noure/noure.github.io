---
layout: single
title: "Science maths (BAC)"
permalink: /maths/bac/
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

<ul>
{% for doc in page.pdfs %}
  <li>
    <a href="{{ '/assets/pdf/bac/' | append: doc.file | relative_url }}" target="_blank" rel="noopener">
      {{ doc.title }}
    </a>
  </li>
{% endfor %}
</ul>
