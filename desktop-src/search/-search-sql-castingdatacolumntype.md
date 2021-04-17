---
description: 'Saiba mais sobre: convertendo o tipo de dados de uma coluna'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Convertendo o tipo de dados de uma coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798210"
---
# <a name="casting-the-data-type-of-a-column"></a>Convertendo o tipo de dados de uma coluna

Às vezes, talvez seja necessário converter dados de cadeia de caracteres extraídos de documentos como outro tipo de dados, para que uma comparação apropriada possa ser feita. Converta um identificador ou um literal como outro tipo de dados usando a seguinte sintaxe:


```
CAST (<identifier> | <literal> AS <datatype>)
```



Por exemplo:


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamentos de tipo de dados](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



