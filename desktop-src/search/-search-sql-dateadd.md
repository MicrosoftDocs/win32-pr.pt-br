---
description: A função DATEADD executa cálculos de data e hora para propriedades correspondentes com tipos de data. Use a função DATEADD para obter datas e horas em um período de tempo especificado antes da apresentação.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Função DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090071"
---
# <a name="dateadd-function"></a>Função DATEADD

A função DATEADD executa cálculos de data e hora para propriedades correspondentes com tipos de data. Use a função DATEADD para obter datas e horas em um período de tempo especificado antes da apresentação.

## <a name="syntax"></a>Sintaxe


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>Argumentos

*DateTimeUnits*

Especifica as unidades do parâmetro de *data e hora* : ano, trimestre, mês, semana, dia, hora, minuto ou segundo. Esse valor diferencia maiúsculas de minúsculas e aspas não são necessárias em todo o parâmetro.

*Deslocamento*

Especifica o deslocamento de tempo, nas unidades especificadas pelo parâmetro *DateTimeUnits* . **OffsetValue** deve ser um número inteiro negativo. Não há suporte para valores positivos.

*DateTime*

Especifica um carimbo de data/hora do qual calcular o deslocamento. Isso não pode ser um literal de data. Ele deve ser GETGMTDATE ou o resultado de outra função DATEADD.

## <a name="remarks"></a>Comentários

A função DATEADD pode ser usada somente em comparações de valor literal e somente no lado direito do operador de comparação.

A função GETGMTDATE retorna a data e a hora atuais no Greenwich Mean Time (GMT). Lembre-se de que esse valor pode não ser o mesmo que o horário local do computador.

Não use o operador de comparação Equals (=) porque a representação de tempo interna pode produzir erros de arredondamento que resultam em resultados de correspondência inesperados.

Você pode usar várias funções de DATEADD para combinar unidades de deslocamento.

### <a name="examples"></a>Exemplos

A cláusula WHERE de exemplo a seguir corresponde aos documentos que foram modificados nos últimos cinco dias:


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



A cláusula WHERE de exemplo a seguir corresponde aos documentos que foram modificados nos últimos dois dias e quatro horas:


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Comparação de valor literal](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparações de vários valores (matriz)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



