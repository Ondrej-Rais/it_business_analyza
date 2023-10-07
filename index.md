---
date: 7.10.2023
author: Ondřej Rais
title: Specifikace požadavků
---

## 1. Úvod

<span style="background: yellow">Pozn.: žlutou barvou označené texty jsou připravené dotazy.</span>

### 1.1 Účel dokumentu 

Objednatel objednává systém a potřebuje se s dodavatelem domluvit na rozsahu systému. Cílem tohoto dokumentu je poskytnout popis systému vč. všech požadavků objednatele. Slouží dodavateli jako podklad pro realizaci. Objednateli slouží pro ujasnění požadavků a jako kontrolní seznam při přebírání díla od dodavatele.

### 1.2 Vize a rozsah systému 

Online taxi služba určená řidičům a zákazníkům taxislužby. Umožňuje provést zákazníkům rezervaci (vč. předběžných rezervací) s možností platby. Systém poskytuje vedení společnosti přehled o kvalifikaci a zákaznickém hodnocení řidičů. Systém dále umožňuje zákazníkům kontaktovat technickou podporu systému.  

![Myšlenková mapa](https://cdn-0.plantuml.com/plantuml/png/LP0zSeCm48LxJg6QKxXCat4cJfLkGJlE6hHYf8L9V0SV89EAqWMJFeMRXNi512vSlXzzUj8k2WHnnDP1a-LcppKn6e5FYdKxtGh8yjmScg1z1sRw9alZPVgTpTmyWr29nleEBVieEYJxoS-gHDRXeMzUyOoXWn9JQr-1csuaUatoO0I3qu7HhN5ncg7QBvGJiLwDZxuOVr9udnCseWuh_qXH0gH99dx5cUtQ9NcfGR1OK9kRAEyGTQZNA_Hll0WoLalz3SiFfhBItZJUDZx0EibYtEhM2vpRXot9kZzqFYF4nso7RBU__GS0)

<span style="background: yellow"><b>Dotaz č. 1: </b> jakým způsobem zákazníci provádí rezervace nyní? Co je bude motivovat k registraci systému?</span>

<span style="background: yellow"><b>Dotaz č. 2: </b> jaké máte obchodní cíle? Je cílem přivést nové zákazníky? Pokud ano, jakou by měl mít systém výhodu oproti konkurenci?</span>

<span style="background: yellow"><b>Dotaz č. 3: </b> přemýšleli jste nad tím, co budou kritéria úspěchu tohoto projektu? Jak poznáte, že byl projekt úspěšný? Navrhuji stanovit konkrétní, měřitelný a časově ohraničený cíl.</span>

### 1.3 Reference

<span style="background: yellow"><b>Dotaz č. 4: </b> existují nějaké materiály či dokumenty, např. manuál firemní identity, které bude nutné zohlednit při vývoji systému?</span>

## 2. Všeobecný popis

### 2.1 Kontext systému

<span style="background: yellow"><b>Dotaz č. 5: </b> existuje ve vaší společnosti nějaký jiný systém, na který by měl být nový systém napojen? Pokud ano, o jaké systémy se jedná? Máte k dispozici diagram architektury systémů?</span>

### 2.2 Přehled hlavních funkcí systému

* Rezervační systém
* Systém hodnocení řidičů
* Monitoring dovedností řidičů
* Technická podpora
* Report pro vedení

### 2.3 Charakteristika uživatelů systému



*Identify the various user classes that you anticipate will use this product. User classes may be
differentiated based on frequency of use, subset of product functions used, technical expertise,
security or privilege levels, educational level, or experience. Describe the pertinent characteristics
of each user class. Certain requirements may pertain only to certain user classes. Distinguish the
most important user classes for this product from those who are less important to satisfy*

### 2.4 Omezení při návrhu a implementaci

*<Popište všechny položky nebo problémy, které budou omezovat možnosti dostupné vývojářům. Tyto by mohly
zahrnují: podnikové nebo regulační zásady; hardwarová omezení (požadavky na časování, paměť
požadavky); rozhraní k jiným aplikacím; konkrétní technologie, nástroje a databáze
použitý; paralelní operace; jazykové požadavky; komunikační protokoly; bezpečnostní
úvahy; designové konvence nebo programovací standardy (například, pokud zákazníka
organizace bude odpovědná za údržbu dodaného softwaru).>*

### 2.5 Předpoklady a závislosti

*uvádí vąechny faktory od nichž jsou odvozeny nebo na nichž závisí požadavky specifikované dále v dokumentu, kromě již uvedených omezení. Např. se zde uvede, co musí být organizačně a technicky připraveno na místě zákazníka, než bude možné systém nainstalovat a provozovat.*

## 3. Přehled požadavků na systém

### 3.1 Funkční požadavky

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>  {{ post.number }} {{ post.source }}
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href=".{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

### 3.2 Nefunkční požadavky 

3.1 User Interfaces
<Describe the logical characteristics of each interface between the software product and the
users. This may include sample screen images, any GUI standards or product family style guides
that are to be followed, screen layout constraints, standard buttons and functions (e.g., help) that
will appear on every screen, keyboard shortcuts, error message display standards, and so on.
Define the software components for which a user interface is needed. Details of the user interface
design should be documented in a separate user interface specification.>

Uživatelské rozhraní
V rámci úspory nákladu musí být využit některý z volně dostupných frameworků uživatelského rozhraní (bude použit https://vuetifyjs.com/). Systém musí být responsivní pro přístup z mobilních zařízení. Objednatel nepožaduje vícejazyčné rozhraní (pouze české). Objednatel nepožaduje realizovat systém dle požadavků zákona o přístupnosti webových stránek (Zákon č. 99/2019 Sb.).

Před započetím programátorských prací, předloží dodavatel ke konzultaci prototyp navrženého uživatelského rozhraní systému.

Dokumentace 
Dokumentace musí obsahovat minimálně: datový model - průběžně aktualizovaný popis struktury databáze, programátorskou dokumentaci (phpDoc), podklady pro uživatelskou příručku (výslednou uživatelskou příručku bude sestavovat pro své zaměstnance objednatel).

Dostupnost, záložní řešení

Požadavky na architekturu systému
Využít výlučně architekturu tenkého klienta, tj. navrhnout systém tak, aby na straně pracovní stanice uživatele nebylo nutno instalovat žádný speciálně vytvořený software. Uživatelské rozhraní systému pro všechny role bude realizováno prostřednictvím tenkého klienta (webové řešení) podporované současnými hlavními prohlížeči (při nejmenším Google Chrome, Mozilla FireFox, Microsoft Edge, na iOS pak Safari).

3.2 Hardware Interfaces
<Describe the logical and physical characteristics of each interface between the software product
and the hardware components of the system. This may include the supported device types, the
nature of the data and control interactions between the software and the hardware, and
communication protocols to be used.>

3.3 Software Interfaces
<Describe the connections between this product and other specific software components (name
and version), including databases, operating systems, tools, libraries, and integrated commercial
components. Identify the data items or messages coming into the system and going out and
describe the purpose of each. Describe the services needed and the nature of communications.
Refer to documents that describe detailed application programming interface protocols. Identify
data that will be shared across software components. If the data sharing mechanism must be
implemented in a specific way (for example, use of a global data area in a multitasking operating
system), specify this as an implementation constraint.>

3.4 Communications Interfaces
<Describe the requirements associated with any communications functions required by this
product, including e-mail, web browser, network server communications protocols, electronic
forms, and so on. Define any pertinent message formatting. Identify any communication standards
that will be used, such as FTP or HTTP. Specify any communication security or encryption issues,
data transfer rates, and synchronization mechanisms.>

Objem dat?

Přenositelonost

5.2 Safety Requirements (Kybernetická bezpečnost) 2
5.3 Security Requirements
<Specify any requirements regarding security or privacy issues surrounding use of the product or
protection of the data used or created by the product. Define any user identity authentication
requirements. Refer to any external policies or regulations containing security issues that affect the
product. Define any security or privacy certifications that must be satisfied.>

5.3.3 Performance requirements (Čas odezvy systému) 8
Čas odezvy systému
Systém musí 95% žádostí na zobrazení stránky zpracovat do 3s. Žádost na filtrování a řazení dat nesmí trvat déle než 7s.


5.4 Software Quality Attributes
<Specify any additional quality characteristics for the product that will be important to either the
customers or the developers. Some to consider are: adaptability, availability, correctness,
flexibility, interoperability, maintainability, portability, reliability, reusability, robustness, testability,
and usability. Write these to be specific, quantitative, and verifiable when possible. At the least,
clarify the relative preferences for various attributes, such as ease of use over ease of learning.>

lokalizace

## 4. Ostatní

## 4.1 Slovník výrazů

## 4.2 Úkoly k dořešení
