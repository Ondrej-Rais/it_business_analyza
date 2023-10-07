---
date: 7.10.2023
author: Ondřej Rais
title: Specifikace požadavků
---

## 1. Úvod

<span style="background: yellow">Pozn.: žlutou barvou označené texty jsou připravené dotazy.</span>

### 1.1 Účel dokumentu 

Objednatel objednává systém a potřebuje se s dodavatelem domluvit na rozsahu systému. Cílem tohoto dokumentu je poskytnout popis systému vč. všech požadavků objednatele. Slouží dodavateli jako podklad pro realizaci. Objednateli slouží pro ujasnění požadavků a jako kontrolní seznam při přebírání díla od dodavatele.

[&laquo; Zpět na obsah](#obsah)

### 1.2 Vize a rozsah systému 

Online taxislužba je systém určený řidičům a zákazníkům taxislužby. Umožňuje provést zákazníkům rezervaci (vč. předběžných rezervací) s možností platby. Systém poskytuje vedení společnosti přehled o kvalifikaci a zákaznickém hodnocení řidičů. Systém dále umožňuje zákazníkům kontaktovat technickou podporu systému.  

![Myšlenková mapa](https://cdn-0.plantuml.com/plantuml/png/VPAnJiCm48RtFeNdF4MH65YW4kK5hlP9k8djoBv4DE_0JiMKiKF46tHnyrvSObU2e39uyDt_V-VxvNKWy6IqLGRgLI4sjj8M1S6R3bKpddUmAWgnFGIA9oDgx_Y0TAsDGtdWLY7k6a9BkWE9yttyY4E7t1SXkHekJupQnxw57_xnQs4eMwWq7PB-4KXB5CgrgAnZqf3g3uwlSjQFHwtqvJrn2l4KUuOpkXUk1XgFaoWF9wO5qYNC8rzGlbejIrRMJjNEm-yt4lUGCdTflegws9VGvKN-4thiqBSW_pnccMr6tixsEPCmWJObcF6isPx1Wj2RE5WqMR3Re-8yfh3ssiQJSC7jBf-taanJxXr19om8oZ6v9iVKfBsSrB6l9b-80rrnMnM7QgQHXy0B9DPaO_9KvyrwC_-8DLgLFzqt)

<span style="background: yellow"><b>Dotaz č. 1: </b> jakým způsobem zákazníci provádí rezervace nyní? Co je bude motivovat k registraci systému?</span>

<span style="background: yellow"><b>Dotaz č. 2: </b> jaké máte obchodní cíle? Je cílem přivést nové zákazníky? Pokud ano, jakou by měl mít systém výhodu oproti konkurenci?</span>

<span style="background: yellow"><b>Dotaz č. 3: </b> přemýšleli jste nad tím, co budou kritéria úspěchu tohoto projektu? Jak poznáte, že byl projekt úspěšný? Navrhuji stanovit konkrétní, měřitelný a časově ohraničený cíl.</span>

<span style="background: yellow"><b>Dotaz č. 4: </b> existují nějaká rizika, která by omezila naplnění cílů?</span>

[&laquo; Zpět na obsah](#obsah)

### 1.3 Reference

<span style="background: yellow"><b>Dotaz č. 5: </b> existují nějaké materiály či dokumenty, např. manuál firemní identity, které bude nutné zohlednit při vývoji systému?</span>

[&laquo; Zpět na obsah](#obsah)

## 2. Všeobecný popis

### 2.1 Kontext systému

<span style="background: yellow"><b>Dotaz č. 6: </b> existuje ve vaší společnosti nějaký jiný systém, na který by měl být nový systém napojen? Pokud ano, o jaké systémy se jedná? Máte k dispozici diagram architektury systémů?</span>

[&laquo; Zpět na obsah](#obsah)

### 2.2 Přehled hlavních funkcí systému

{% for category in site.categories %}
* {{ category[0] }}
{% endfor %}

[&laquo; Zpět na obsah](#obsah)

### 2.3 Charakteristika uživatelů systému

| Typ uživatele | Stručný popis |
|---------------|---------------|
| Vedení              | Najímá pracovníky, spravuje je v systému, sleduje reporty a zákaznické hodnocení. |
| Řidič              | Přijímá rezervace z dispečinku, realizuje přepravu.              |
| Podpora              |  Odpovídá na dotazy od zákazníků, příp. předává na vývojový tým.      |
| Dispečink              | Přijímá telefonické rezervace a předává je dostupným řidičům.              |
| Zákazník              | Rezervuje, hodnotí, provádí platbu, pokládá dotazy na technickou podporu.              |

![Diagram uživatelů](https://cdn-0.plantuml.com/plantuml/png/SoWkIImgAStDuKfCAYufIamkKGW0albbUOVNPdCXc0esDRgw2c6fAQb07eQuIsPnGUgHtimyJ2r7PsIcP1xfnH0Fo4yfo2zAv4hEIImkLeWwl30xiGfifqDgNWhGFG00)

[&laquo; Zpět na obsah](#obsah)

### 2.4 Omezení při návrhu a implementaci

<div style="background: yellow"><b>Dotaz č. 7: </b> existují nějaká omezení či normy, které musí dodavatel, resp. systém splňovat? Zřejmě budeme řešit následující:
<ul>  
<li>110/2019 Sb. Zákon o zpracování osobních údajů (registrace zákazníků, osobní údaje zaměstnanců)</li>
<li>235/2004 Sb. Zákon o dani z přidané hodnoty (zjednodušený daňový doklad)</li>
<li>563/1991 Sb. Zákon o účetnictví (příjmové pokladní doklady)</li>
</ul>
</div>

<span style="background: yellow"><b>Dotaz č. 8: </b> budou vývojáři limitováni nějakou technologií? Musí se jednat o nativní mobilní aplikaci nebo může být využito technologie tenkého klienta a systém vytvořen jako webová responzivní aplikace?</span>

[&laquo; Zpět na obsah](#obsah)

## 3. Přehled požadavků na systém

### 3.1 Funkční požadavky

<span style="background: yellow">Kromě požadavků, které byly přímo zmíněny ve vašemu úvodním dopise, přikládám i mnou navrhované požadavky, které vychází ze zkušeností s podobnými systémy.</span>

<span style="background: yellow">Pozn.: používám jméno Jan Novák jako jména objednatele.</span>

**Legenda - priority:**

🔴 Must have

🟡 Should have

⚪ Could have

{% for category in site.categories %}
#### {{ category[0] }}

<table class="full">
  <thead>
    <tr>
      <th width="40">&nbsp;</th> 
      <th width="100">Označení</th> 
      <th>Název</th>       
      <th width="160">Typ uživatele</th> 
      <th width="200">Zdroj</th> 
      <th width="80">Detail</th> 
    </tr>
  </thead>
  <tbody>
    {% assign sortedPosts = category[1] | sort: 'number' %}
    {% for post in sortedPosts %}
      <tr>
        <td style="text-align: center;">
          {% if post.priority contains 'Must have' %}
          🔴
          {% elsif post.priority contains 'Should have' %}
          🟡
          {% elsif post.priority contains 'Could have' %}
          ⚪
          {% else %}
          {{ post.priority }}
          {% endif %}
        </td>
        <td>
          {% if post.detail %}
          <a href=".{{ post.url }}" title="{{ post.number }}">{{ post.number }}</a>
          {% else %}
          {{ post.number }}
          {% endif %}
        </td>
        <td>
          {% if post.detail %}
          <a href=".{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
          {% else %}
          {{ post.title }}
          {% endif %}
        </td>        
        <td>{{ post.user }}</td>
        <td>{{ post.source }}</td>
        <td>
          {% if post.detail %}
          <a href=".{{ post.url }}" title="Více informace">Více &raquo;</a>
          {% endif %}
        </td>
      </tr>
      {% if post.questions %}
      <tr>
        <td colspan="6">{{ post.questions }}</td>
      </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>
{% endfor %}

[&laquo; Zpět na obsah](#obsah)

### 3.2 Nefunkční požadavky 

{% for tag in site.tags %}
{% if tag[0] contains 'Nefunkční' %}
<table class="full">
  <thead>
    <tr>
      <th width="100">Označení</th> 
      <th>Název</th>       
      <th width="200">Zdroj</th> 
    </tr>
  </thead>
  <tbody>
  {% assign sortedPosts = tag[1] | sort: 'number' %}
  {% for post in sortedPosts %}
  <tr>    
    <td>
      {{ post.number }}
    </td>
    <td>
      {{ post.title }}      
    </td>        
    <td>{{ post.source }}</td>
  </tr>
  {% if post.description %}
  <tr>
    <td colspan="3">{{ post.description }}</td>
  </tr>
  {% endif %}
  {% endfor %}
  </tbody>
</table>
{% endif %}
{% endfor %}

<span style="background:yellow"><strong>Dotaz č. 36:</strong> jaké máte požadavky na dokumentaci systému? Myslím si, že by měla obsahovat alespoň datový model - průběžně aktualizovaný popis struktury databáze, programátorskou dokumentaci, uživatelskou příručku pro pracovníky i zákazníky.</span>

<span style="background:yellow"><strong>Dotaz č. 37:</strong> existují požadavky na architekturu systému? Viz dotaz č. 8</span>

<span style="background:yellow"><strong>Dotaz č. 38:</strong> existují požadavky na HW rozhraní? Jaké zařízení musí systém podporovat?</span>

<span style="background:yellow"><strong>Dotaz č. 39:</strong> existují požadavky na SW rozhraní? Jaké OS musí systém podporovat?</span>

<span style="background:yellow"><strong>Dotaz č. 40:</strong> existují požadavky na komunikační rozhraní (např. komunikace REST API)?</span>

<span style="background:yellow"><strong>Dotaz č. 41:</strong> jak velké objemy dat předpokládáte (počet zákazníků v systému celkem/denně, počet rezervací celkem/denně)?</span>

<span style="background:yellow"><strong>Dotaz č. 42:</strong> jaké máte požadavky na čas odezvy systému (např. 95% žádostí na zobrazení okna systému musí být zpracováno do 3s, statistiky, filtrování a řazení dat nesmí trvat déle než 7s)?</span>

[&laquo; Zpět na obsah](#obsah)

## 4. Ostatní

### 4.1 Slovník výrazů

[&laquo; Zpět na obsah](#obsah)

### 4.2 Úkoly k dořešení

[&laquo; Zpět na obsah](#obsah)
