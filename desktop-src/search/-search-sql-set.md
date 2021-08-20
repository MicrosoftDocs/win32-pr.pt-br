---
description: A instrução SET especifica as opções PROPERTYNAME e RANKMETHOD para a consulta.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Instrução SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007128d30091e0ac464f2d9452232a6df018b40f0dd9c04d6e17b0520d94aada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680487"
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

 

 



