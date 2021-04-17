---
description: Descreve os operadores WQL usados na cláusula WHERE ou na instrução SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operadores WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812328"
---
# <a name="wql-operators"></a><span data-ttu-id="e71bb-103">Operadores WQL</span><span class="sxs-lookup"><span data-stu-id="e71bb-103">WQL Operators</span></span>

<span data-ttu-id="e71bb-104">A linguagem de consulta de Instrumentação de Gerenciamento do Windows (WQL) dá suporte a um conjunto de operadores padrão que são usados na [cláusula WHERE](where-clause.md) de uma instrução SELECT, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e71bb-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="e71bb-105">Operador</span><span class="sxs-lookup"><span data-stu-id="e71bb-105">Operator</span></span>       | <span data-ttu-id="e71bb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e71bb-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="e71bb-107">Igual a</span><span class="sxs-lookup"><span data-stu-id="e71bb-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="e71bb-108">Menor que</span><span class="sxs-lookup"><span data-stu-id="e71bb-108">Less than</span></span>                |
| >           | <span data-ttu-id="e71bb-109">Maior que</span><span class="sxs-lookup"><span data-stu-id="e71bb-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="e71bb-110">Menor ou igual a</span><span class="sxs-lookup"><span data-stu-id="e71bb-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="e71bb-111">Maior ou igual a</span><span class="sxs-lookup"><span data-stu-id="e71bb-111">Greater than or equal to</span></span> |
| <span data-ttu-id="e71bb-112">! = ou <></span><span class="sxs-lookup"><span data-stu-id="e71bb-112">!= or <></span></span> | <span data-ttu-id="e71bb-113">Não igual a</span><span class="sxs-lookup"><span data-stu-id="e71bb-113">Not equal to</span></span>             |



 

<span data-ttu-id="e71bb-114">Há alguns operadores adicionais específicos de WQL: IS, NOT, ISA e LIKE.</span><span class="sxs-lookup"><span data-stu-id="e71bb-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="e71bb-115">Os operadores IS e NOT não são válidos na cláusula WHERE somente se a constante for **nula**.</span><span class="sxs-lookup"><span data-stu-id="e71bb-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="e71bb-116">Por exemplo, as seguintes consultas são válidas:</span><span class="sxs-lookup"><span data-stu-id="e71bb-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="e71bb-117">As consultas a seguir mostram usos inválidos de IS e IS NOT:</span><span class="sxs-lookup"><span data-stu-id="e71bb-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="e71bb-118">O operador ISA é usado na cláusula WHERE de consultas de dados e eventos para testar objetos incorporados para uma hierarquia de classe.</span><span class="sxs-lookup"><span data-stu-id="e71bb-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="e71bb-119">O operador ISA elimina a necessidade de manter o controle de classes derivadas recentemente ao solicitar uma hierarquia de classes.</span><span class="sxs-lookup"><span data-stu-id="e71bb-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="e71bb-120">Quando você usa o ISA, as subclasses recém-criadas e existentes da classe solicitada são incluídas automaticamente no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="e71bb-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="e71bb-121">Para obter mais informações sobre a sintaxe e o uso desse operador, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="e71bb-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="e71bb-122">Operador ISA para consultas de dados</span><span class="sxs-lookup"><span data-stu-id="e71bb-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="e71bb-123">Operador ISA para consultas de evento</span><span class="sxs-lookup"><span data-stu-id="e71bb-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="e71bb-124">Operador ISA para consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="e71bb-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="e71bb-125">O operador LIKE é válido na cláusula WHERE e é usado para determinar se uma determinada cadeia de caracteres corresponde a um padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="e71bb-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="e71bb-126">Por exemplo, a consulta a seguir retorna todas as instâncias de \_ classes Win32.</span><span class="sxs-lookup"><span data-stu-id="e71bb-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="e71bb-127">Para obter mais informações sobre a sintaxe e o uso desse operador, consulte [operador Like](like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="e71bb-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



