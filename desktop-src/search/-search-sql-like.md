---
description: O predicado LIKE executa a comparação de correspondência de padrões na coluna especificada.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Predicado LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814581"
---
# <a name="like-predicate"></a>Predicado LIKE

O predicado LIKE executa a comparação de correspondência de padrões na coluna especificada. Ela usa a seguinte sintaxe:


```
...WHERE <column> LIKE '<wildcard_literal>'
```



O <column> pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado. A coluna é limitada às propriedades no repositório de propriedades.

O literal de curinga <\_> é um literal de cadeia de caracteres. Ele é colocado entre aspas e, opcionalmente, pode conter caracteres curinga. A cadeia de caracteres de correspondência pode conter vários caracteres curinga, se necessário. A tabela a seguir descreve os caracteres curinga que o predicado LIKE reconhece.



| Curinga                | Descrição                                                                                                                                                                                     | Exemplo                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (porcentagem)             | Corresponde a zero ou mais caracteres.                                                                                                                                                         | ' comp% r ' corresponde a ' comp ' seguido de zero ou mais caracteres, terminando em um r.                                                                                                                                  |
| \_ sublinhado         | Corresponde a qualquer caractere único.                                                                                                                                                                   | ' compse \_ ' corresponde a ' comp ' seguido de exatamente um de qualquer caractere, seguido de ' los '.                                                                                                                              |
| \[\](colchetes) | Corresponde a qualquer caractere único dentro do intervalo ou conjunto especificado. Por exemplo, \[ a-z \] especifica um intervalo; \[ aeiou \] especifica o conjunto de vogais.                                                  | ' comp \[ a-z \] re ' corresponde a ' comp ' seguido de um único caractere no intervalo de a até z, seguido de is '. ' comp \[ ' \] corresponde a ' comp ' seguido de um único caractere que deve ser um ou um.<br/> |
| \[^ \] acento          | Corresponde a qualquer caractere único que não esteja dentro do intervalo ou conjunto especificado. Por exemplo, \[ ^ a-z \] especifica um intervalo que exclui de a a z; \[ ^ aeiou \] especifica um conjunto que exclui as vogais. | ' comp \[ ^ u \] ' corresponde a ' comp ' seguido de qualquer caractere único que não seja um u.                                                                                                                                        |



 

Se você criar predicados com vários intervalos, os intervalos deverão estar em ordem.

> [!Note]  
> Para corresponder os caracteres curinga como caracteres literais para correspondência e não como caracteres curinga, coloque o caractere dentro de colchetes. Por exemplo, para corresponder ao sinal de porcentagem, use ' \[ % \] '

 

## <a name="examples"></a>Exemplos


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Comparação de valor literal](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparações de vários valores (matriz)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Predicado nulo](-search-sql-null.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




