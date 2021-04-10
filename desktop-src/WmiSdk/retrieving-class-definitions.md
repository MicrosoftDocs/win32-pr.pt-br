---
description: As consultas de esquema são instruções WQL que solicitam definições de classe e informações sobre associações de esquema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recuperando definições de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091302"
---
# <a name="retrieving-class-definitions"></a><span data-ttu-id="cdfb7-103">Recuperando definições de classe</span><span class="sxs-lookup"><span data-stu-id="cdfb7-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="cdfb7-104">As consultas de esquema são instruções WQL que solicitam definições de classe e informações sobre [associações de esquema](schema-associations.md).</span><span class="sxs-lookup"><span data-stu-id="cdfb7-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="cdfb7-105">Os provedores de classe usam consultas de esquema em suas instâncias da classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) para especificar as classes que dão suporte ao se registrarem com o WMI.</span><span class="sxs-lookup"><span data-stu-id="cdfb7-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="cdfb7-106">As consultas de esquema são colocadas nas propriedades **ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries** da instância **\_ \_ ClassProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="cdfb7-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="cdfb7-107">As consultas de esquema são semelhantes às consultas de dados, pois dão suporte às seguintes instruções WQL:</span><span class="sxs-lookup"><span data-stu-id="cdfb7-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="cdfb7-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="cdfb7-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="cdfb7-109">ASSOCIADORES DE</span><span class="sxs-lookup"><span data-stu-id="cdfb7-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="cdfb7-110">REFERÊNCIAS DE</span><span class="sxs-lookup"><span data-stu-id="cdfb7-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="cdfb7-111">ISA</span><span class="sxs-lookup"><span data-stu-id="cdfb7-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="cdfb7-112">Uma consulta de esquema é semelhante a uma [referência de consulta de](references-of-statement.md) dados que especifica a palavra-chave **ClassDefsOnly** ; em outras palavras, isso retorna um conjunto de resultados de objetos de definição de classe em vez de instâncias reais de classes de associação.</span><span class="sxs-lookup"><span data-stu-id="cdfb7-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="cdfb7-113">No entanto, as referências de retornam definições de classe somente se houver instâncias presentes.</span><span class="sxs-lookup"><span data-stu-id="cdfb7-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="cdfb7-114">Uma consulta de esquema retorna definições de classe se as instâncias estão presentes ou não.</span><span class="sxs-lookup"><span data-stu-id="cdfb7-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



