---
description: O termo FORMSOF executa correspondências usando outras formas linguísticas da palavra.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF termo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863439"
---
# <a name="formsof-term"></a>FORMSOF termo

O termo FORMSOF executa correspondências usando outras formas linguísticas da palavra. A seguir está a sintaxe do termo FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



o tipo de geração especifica como o Microsoft Windows Search escolhe os formatos de palavra alternativos. O valor de **Inflexde** escolhe formulários de inflexão alternativos para as palavras de correspondência. Se a palavra for um verbo, as dezenases alternativas serão usadas. Se a palavra for um substantivo, os formulários singular, plural e Possessive serão usados para detectar correspondências.

O valor de corresponder \_ palavras é uma ou mais palavras, separadas por vírgulas.

## <a name="examples"></a>Exemplos

O exemplo a seguir pesquisa correspondências de inflexões para a palavra "Run". Este exemplo corresponde a documentos que contêm "Run", "Running" ou "Execute".


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



