---
description: Embora as palavras e as regras linguísticas sejam significativamente diferentes, há algumas considerações, como números, datas e horas, que são tratadas de forma consistente em todos os disjuntores de palavras.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalização do Surface Form
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f96ce5c90075c49608ad386b64514e4d003e5b5b4c6fc582441fd7e110d1921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862430"
---
# <a name="surface-form-normalization"></a>Normalização do Surface Form

Embora as palavras e as regras linguísticas sejam significativamente diferentes, há algumas considerações, como números, datas e horas, que são tratadas de forma consistente em todos os disjuntores de palavras. Este tópico documenta considerações de normalização que podem afetar sua implementação de disjuntor de palavras.

Este tópico é organizado da seguinte forma:

-   [Hifenização](#hyphenation)
-   [Possessivos](#possessives)
-   [Diacríticos](#diacritics)
-   [Clitics](#clitics)

## <a name="hyphenation"></a>Hifenização

Hifens (-) são usados entre as partes de uma palavra composta ou nome. Eles também são usados entre as syllables de uma palavra quando a palavra é dividida no final de uma linha de texto. Em inglês, as palavras são unidas com hifens para indicar uma relação especial no contexto, mas essas palavras normalmente não podem ser hifenadas em outros contextos; por exemplo, "passo a passo". Durante a criação do índice, o separador de palavras deve tratar o hífen como um separador de palavras. Por exemplo, "base de dados" seria armazenado como "dados" mais "base". No momento da consulta, uma frase hifenização deve ser substituída por duas alternativas: a variante de duas palavras e o composto verdadeiro. Por exemplo, "data-base" seria substituído por "dados" mais "base" e "banco de dados". Essa diferença entre o índice e o tempo de consulta aumenta as combinações de representações para palavras hífens e torna as palavras mais fáceis de corresponder em uma consulta.

A tabela a seguir mostra como tratar hifens como separadores de palavras no idioma inglês aumenta o número de termos de consulta de acordo para cada termo incluído no índice.



| Termos incluídos no índice | Corresponde ao tempo de consulta   |
|-----------------------------|----------------------|
| Base de dados                   | base de dados, base de dados |
| Base de dados                   | base de dados, base de dados |
| Banco de dados                    | base de dados, banco de dados  |



 

## <a name="possessives"></a>Possessivos

Os possessivos são variações em um substantivo que indicam posse. Os possessivos em inglês são representados pela aposição de um apóstrofo (') ou um apóstrofo e um (s) a uma palavra. Por exemplo, para indicar a posse, a palavra "Maria" é representada como "Maria". O disjuntor de palavras gera os formulários apóstrofo e apóstrofo no momento da consulta. As consultas de "Maria" devem corresponder a "Maria" e "Maria".

## <a name="diacritics"></a>Sinais diacríticos

Diacríticas são marcas adicionadas a uma letra ou phoneme para indicar um valor phoneético especial para pronúncia. Os diacréticos podem distinguir palavras que, de outra forma, são graficamente idênticas; por exemplo, "resume" e "resumé" em inglês. No entanto, salvar diacríticas no índice aumenta o número de chaves de palavras exclusivas no índice, o que reduz o desempenho da consulta. Se os diacréticos são usados apenas minimamente em um idioma, o disjuntor de palavras para esse idioma deve removê-los durante a criação e a consulta do índice. Por exemplo, o disjuntor de palavras em inglês gera "retomar" ao processar "resumé", causando apenas impacto mínimo sobre a relevância dos resultados da consulta.

## <a name="clitics"></a>Clitics

Um clitic é uma palavra sem esforço que não é capaz de ficar por conta própria e anexa a uma palavra de estresse para formar uma única unidade. Os clitics não podem ser facilmente classificados como histográficos, sintáticos ou morfográficos. Clitics vêm em dois tipos: *proclitics* *e enclitics*. Os proclitics se anexam ao início de uma palavra. Os enclitics se anexam ao final de uma palavra.

Os clitics são mais difíceis de analisar em idiomas como espanhol. Um verbo espanhol pode gerar muitas formas de superfície, dependendo do tempo. É necessário fazer considerações entre remover o clitic durante a criação do índice e gerar os formulários de superfície por meio da derivação no momento da consulta. Remover clitics em casos em que a morfologia da composição clítica é ambígua pode levar a resultados imprevisíveis. Gerar um grande número de formulários de superfície para uma palavra aumenta o tamanho do índice de texto completo e pode reduzir o desempenho da consulta. É recomendável que o stemmer gere apenas um pequeno número de formulários de superfície.

 

 



