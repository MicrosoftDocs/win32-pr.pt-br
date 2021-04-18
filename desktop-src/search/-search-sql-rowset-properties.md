---
description: Depois que um resultado é retornado de uma consulta, você pode acessar várias propriedades para o conjunto de linhas.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Propriedades do conjunto de linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782464"
---
# <a name="rowset-properties"></a>Propriedades do conjunto de linhas

Depois que um resultado é retornado de uma consulta, você pode acessar várias propriedades para o conjunto de linhas.

Além das propriedades padrão do conjunto de linhas OLE-DB, o Windows Search SQL oferece as quatro propriedades personalizadas a seguir. O GUID para este conjunto de propriedades é {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.

O Windows Search dá suporte à propriedade padrão OLE-DB DBPROP \_ COMMANDTIMEOUT da propriedade conjunto de [ \_ linhas DBPROPSET](/previous-versions//ms691738(v=vs.85)) .



| Nome da propriedade                  | PROPID/Type | Descrição                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DONOTCOMPUTEEXPENSIVEPROPS     | 15/VT \_ bool | Definir isso como verdadeiro impede a computação de propriedades caras como resultados encontrados e a classificação máxima que exigem a avaliação de toda a consulta quando qualquer propriedade de conjunto de linhas é acessada.                                                                                                                                                                         |
| Classificação máxima ( \_ classificação máxima)       | 6/VT \_ i4    | A classificação mais alta calculada para qualquer resultado.                                                                                                                                                                                                                                                                                                          |
| Resultados encontrados (resultados \_ encontrados) | 7/VT \_ i4    | O número total de itens exclusivos para esta consulta. Para uma consulta SELECT, este é o número de itens no conjunto de linhas. Para um grupo na consulta, este é o número de itens folha exclusivos. Essa propriedade não identifica o número de linhas no conjunto de linhas de nível superior (o número de grupos de nível superior).                                                        |
| Onde ID (WHEREid)             | 8/VT \_ i4    | O identificador para as restrições usadas para uma consulta. Se um conjunto de linhas for aberto quando uma nova consulta for executada, a nova consulta poderá reutilizar as restrições da consulta mais antiga, aproveitando assim o trabalho já concluído. Para obter mais informações sobre como reutilizar restrições WHERE, consulte a [função ReuseWhere](-search-sql-reusewhere.md). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Priorização de indexação e eventos de conjunto de linhas no Windows 7](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
