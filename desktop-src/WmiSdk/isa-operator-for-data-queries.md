---
description: Use o operador ISA na cláusula WHERE de uma consulta de dados para solicitar objetos incorporados em uma hierarquia de classe.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operador ISA para consultas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761313"
---
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="05d98-103">Operador ISA para consultas de dados</span><span class="sxs-lookup"><span data-stu-id="05d98-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="05d98-104">Use o operador ISA na cláusula WHERE de uma consulta de dados para solicitar objetos incorporados em uma hierarquia de classe.</span><span class="sxs-lookup"><span data-stu-id="05d98-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="05d98-105">O exemplo a seguir mostra a sintaxe para solicitar objetos incorporados em uma hierarquia de classe.</span><span class="sxs-lookup"><span data-stu-id="05d98-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="05d98-106">O resultado inclui instâncias de **classe** com objetos inseridos que são derivados de **ParentClass** na propriedade **EmbeddedProp** .</span><span class="sxs-lookup"><span data-stu-id="05d98-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="05d98-107">Nem toda instância do objeto de **classe** é derivada de **ParentClass**, mas o resultado retorna os objetos inseridos que são derivados de **ParentClass**.</span><span class="sxs-lookup"><span data-stu-id="05d98-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="05d98-108">Por exemplo, na consulta a seguir, a **ClasseA** inclui a propriedade **EmbeddedObj** de tipo fraco.</span><span class="sxs-lookup"><span data-stu-id="05d98-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="05d98-109">A classe **ClassID** tem dez instâncias.</span><span class="sxs-lookup"><span data-stu-id="05d98-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="05d98-110">Cinco dessas instâncias têm objetos inseridos com um tipo derivado de **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="05d98-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="05d98-111">Os outros cinco têm objetos incorporados de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="05d98-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="05d98-112">O exemplo a seguir mostra a consulta que retorna as cinco instâncias, que incluem os objetos que são derivados de **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="05d98-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



