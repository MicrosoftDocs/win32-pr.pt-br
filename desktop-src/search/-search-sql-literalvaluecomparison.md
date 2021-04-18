---
description: A comparação de valor literal usa operadores de comparação padrão para corresponder uma coluna de valor único a um valor literal.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparação de valor literal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813231"
---
# <a name="literal-value-comparison"></a>Comparação de valor literal

A comparação de valor literal usa operadores de comparação padrão para corresponder uma coluna de valor único a um valor [literal](-search-sql-literals.md) . Para obter informações sobre como comparar colunas com vários valores, consulte [comparações de valores múltiplos (matriz)](-search-sql-multivaluedcomparisons.md).

O predicado de comparação de valor literal tem a seguinte sintaxe:


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> O lado direito da comparação deve ser um literal. Você não pode comparar uma coluna com um valor calculado e não pode comparar uma coluna com outra coluna.

 

A parte da coluna é qualquer coluna de propriedade válida e pode ser convertida em outro tipo, se necessário. Opcionalmente, você pode colocar o nome da coluna entre aspas duplas para facilitar a leitura sem afetar a funcionalidade. Para obter mais informações, consulte [convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).

O literal pode ser qualquer cadeia de caracteres, numérico, hexadecimal, booliano ou literal de data, entre aspas simples. Somente as correspondências exatas são reconhecidas e os caracteres curinga são ignorados. O literal também pode ser convertido em outro tipo.

## <a name="comparison-operators"></a>Operadores de comparação

A tabela a seguir descreve os operadores de comparação com suporte.



| Operador de comparação | Descrição              |
|---------------------|--------------------------|
| =                   | Igual a                 |
| ! = ou <>      | É diferente de             |
| >                | Maior que             |
| >=               | Maior que ou igual a |
| <                | Menor que                |
| <=               | Menor que ou igual a    |



 

 

Em conjunto com o operador "=", o Windows Search linguagem SQL (SQL) dá suporte ao uso de palavras-chave BEFORE e AFTER, que especificam se a consulta deve comparar valores de coluna antes ou depois de um valor especificado, na ordem de classificação do dicionário.


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>Exemplos

Veja a seguir exemplos do predicado de comparação de valor literal.


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado LIKE](-search-sql-like.md)
</dt> <dt>

[Função DATEADD](-search-sql-dateadd.md)
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

 

 



