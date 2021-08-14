---
description: Embora as palavras e as regras linguísticas sejam significativamente diferentes, há algumas considerações, como números, datas e horas, que são manipuladas consistentemente em todos os separadores de palavras.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalização do formulário de superfície
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f96ce5c90075c49608ad386b64514e4d003e5b5b4c6fc582441fd7e110d1921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862430"
---
# <a name="surface-form-normalization"></a>Normalização do formulário de superfície

Embora as palavras e as regras linguísticas sejam significativamente diferentes, há algumas considerações, como números, datas e horas, que são manipuladas consistentemente em todos os separadores de palavras. Este tópico documenta as considerações de normalização que podem afetar a implementação do seu separador de palavras.

Este tópico é organizado da seguinte maneira:

-   [Hifenização](#hyphenation)
-   [Possessivos](#possessives)
-   [Diacríticos](#diacritics)
-   [Clitics](#clitics)

## <a name="hyphenation"></a>Hifenização

Hifens (-) são usados entre as partes de uma palavra ou nome composto. Eles também são usados entre as sílabas de uma palavra quando a palavra é dividida no final de uma linha de texto. Em inglês, as palavras são unidas com hifens para indicar uma relação especial no contexto, mas essas palavras normalmente não podem ser hifenizadas em outros contextos; por exemplo, "passo a passo". Durante a criação do índice, o separador de palavras deve tratar o hífen como um separador de palavras. Por exemplo, "base de dados" seria armazenado como "dados" mais "base". No momento da consulta, uma frase hifenizada deve ser substituída por duas alternativas: a variante de duas palavras e o composto real. Por exemplo, "base de dados" seria substituído por "data", além de "base" e "Database". Essa diferença entre o tempo de consulta e de índice aumenta as combinações de representações de palavras hifenizadas e torna as palavras mais fáceis de corresponder em uma consulta.

A tabela a seguir mostra como tratar hifens como separadores de palavras no idioma inglês aumenta o número de termos de consulta correspondentes para cada termo incluído no índice.



| Termos incluídos no índice | Correspondências de tempo de consulta   |
|-----------------------------|----------------------|
| Banco de dados                   | banco de dados, base de dados |
| Base de dados                   | banco de dados, base de dados |
| Banco de dados                    | data-base, banco de dados  |



 

## <a name="possessives"></a>Possessivos

Possessivos são variações em um substantivo que indicam posse. Os possessivos em inglês são representados acrescentando um apóstrofo (') ou um apóstrofo e um s () a uma palavra. Por exemplo, para indicar a posse, a palavra "Mary" é representada como "Mary ' s". O separador de palavras gera os formulários de apóstrofo e apóstrofo no momento da consulta. As consultas para "Mary" devem corresponder a "Mary" e "Mary".

## <a name="diacritics"></a>Sinais diacríticos

Diacríticos são marcas adicionadas a uma letra ou fonema para indicar um valor fonético especial para pronúncia. Os diacríticos podem distinguir palavras que, de outra forma, são graficamente idênticas; por exemplo, "retomar" e "resumé" em inglês. No entanto, salvar sinais diacríticos no índice aumenta o número de chaves de palavras exclusivas no índice, o que reduz o desempenho da consulta. Se os diacríticos forem usados apenas minimamente em uma linguagem, o separador de palavras para esse idioma deverá removê-los durante a criação e consulta de índice. Por exemplo, o separador de palavras em inglês gera "resume" ao processar "resumé", causando apenas impacto mínimo sobre a relevância dos resultados da consulta.

## <a name="clitics"></a>Clitics

Um clitic é uma palavra sem estresse que é incapaz de ficar por conta própria e é anexada a uma palavra sob estresse para formar uma única unidade. Clitics não pode ser facilmente classificado como phonological, sintático ou morfológicas. Clitics são fornecidos em dois tipos: *proclitics* e *enclitics*. Proclitics se anexam ao início de uma palavra. Enclitics se anexam ao final de uma palavra.

Clitics são mais difíceis de analisar em linguagens como o espanhol. Um verbo espanhol pode gerar muitos formulários de superfície, dependendo do conjugação. As considerações devem ser feitas entre a remoção do clitic durante a criação do índice e a geração de formulários de superfície por meio da lematização no momento da consulta. Remover clitics em casos em que a morphology da composição clitic é ambígua pode levar a resultados imprevisíveis. Gerar um grande número de formulários de superfície para uma palavra aumenta o tamanho do índice de texto completo e pode retardar o desempenho da consulta. É recomendável que o lematizador gere apenas um pequeno número de formulários de superfície.

 

 



