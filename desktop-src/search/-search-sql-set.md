---
description: A instrução SET especifica as opções PROPERTYNAME e RANKMETHOD para a consulta.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Instrução SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090061"
---
# <a name="set-statement"></a>Instrução SET

A instrução SET especifica as opções PROPERTYNAME e RANKMETHOD para a consulta.

## <a name="propertyname"></a>PROPERTYNAME

Você pode associar uma propriedade a um alias amigável para a consulta usando a seguinte sintaxe:


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>RANKMETHOD

Você pode especificar o método de classificação para consultas com o termo ISABOUT usando a seguinte sintaxe:


```
SET RANKMETHOD <rankmethod>      
```



Os métodos RANKMETHOD que podem ser especificados usando a instrução SET são JACCARD coeficiente, coeficiente de comportas e produto interno.

 

 



