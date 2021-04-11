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
# <a name="set-statement"></a><span data-ttu-id="de05d-103">Instrução SET</span><span class="sxs-lookup"><span data-stu-id="de05d-103">SET Statement</span></span>

<span data-ttu-id="de05d-104">A instrução SET especifica as opções PROPERTYNAME e RANKMETHOD para a consulta.</span><span class="sxs-lookup"><span data-stu-id="de05d-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="de05d-105">PROPERTYNAME</span><span class="sxs-lookup"><span data-stu-id="de05d-105">PROPERTYNAME</span></span>

<span data-ttu-id="de05d-106">Você pode associar uma propriedade a um alias amigável para a consulta usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="de05d-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="de05d-107">RANKMETHOD</span><span class="sxs-lookup"><span data-stu-id="de05d-107">RANKMETHOD</span></span>

<span data-ttu-id="de05d-108">Você pode especificar o método de classificação para consultas com o termo ISABOUT usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="de05d-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="de05d-109">Os métodos RANKMETHOD que podem ser especificados usando a instrução SET são JACCARD coeficiente, coeficiente de comportas e produto interno.</span><span class="sxs-lookup"><span data-stu-id="de05d-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



