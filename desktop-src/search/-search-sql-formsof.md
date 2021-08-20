---
description: O termo FORMSOF executa as combinações usando outras formas linguísticas da palavra.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Termo FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863439"
---
# <a name="formsof-term"></a>Termo FORMSOF

O termo FORMSOF executa as combinações usando outras formas linguísticas da palavra. Veja a seguir a sintaxe do termo FORMSOF:


```
FORMSOF (<generation_type>,<match_words>)
```



O tipo de geração especifica como o Microsoft Windows Search escolhe os formulários de palavras alternativos. O **valor INFLECTIONAL** escolhe formulários de inflexão alternativos para as palavras de combinação. Se a palavra for um verbo, tempos alternativos serão usados. Se a palavra for um substantivo, as formas singular, plural e possessiva serão usadas para detectar as correspondeções.

O valor \_ de palavras de combinação é uma ou mais palavras, separadas por vírgulas.

## <a name="examples"></a>Exemplos

O exemplo a seguir procura por corresponde à palavra "run". Este exemplo corresponde a documentos que contêm "run", "running" ou "ran".


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

 

 



