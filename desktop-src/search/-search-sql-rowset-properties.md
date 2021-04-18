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
# <a name="rowset-properties"></a><span data-ttu-id="ab3ad-103">Propriedades do conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="ab3ad-103">Rowset Properties</span></span>

<span data-ttu-id="ab3ad-104">Depois que um resultado é retornado de uma consulta, você pode acessar várias propriedades para o conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="ab3ad-105">Além das propriedades padrão do conjunto de linhas OLE-DB, o Windows Search SQL oferece as quatro propriedades personalizadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="ab3ad-106">O GUID para este conjunto de propriedades é {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="ab3ad-107">O Windows Search dá suporte à propriedade padrão OLE-DB DBPROP \_ COMMANDTIMEOUT da propriedade conjunto de [ \_ linhas DBPROPSET](/previous-versions//ms691738(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ab3ad-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="ab3ad-108">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="ab3ad-108">Property name</span></span>                  | <span data-ttu-id="ab3ad-109">PROPID/Type</span><span class="sxs-lookup"><span data-stu-id="ab3ad-109">PROPID/type</span></span> | <span data-ttu-id="ab3ad-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab3ad-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3ad-111">DONOTCOMPUTEEXPENSIVEPROPS</span><span class="sxs-lookup"><span data-stu-id="ab3ad-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="ab3ad-112">15/VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="ab3ad-112">15/VT\_BOOL</span></span> | <span data-ttu-id="ab3ad-113">Definir isso como verdadeiro impede a computação de propriedades caras como resultados encontrados e a classificação máxima que exigem a avaliação de toda a consulta quando qualquer propriedade de conjunto de linhas é acessada.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="ab3ad-114">Classificação máxima ( \_ classificação máxima)</span><span class="sxs-lookup"><span data-stu-id="ab3ad-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="ab3ad-115">6/VT \_ i4</span><span class="sxs-lookup"><span data-stu-id="ab3ad-115">6/VT\_I4</span></span>    | <span data-ttu-id="ab3ad-116">A classificação mais alta calculada para qualquer resultado.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ab3ad-117">Resultados encontrados (resultados \_ encontrados)</span><span class="sxs-lookup"><span data-stu-id="ab3ad-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="ab3ad-118">7/VT \_ i4</span><span class="sxs-lookup"><span data-stu-id="ab3ad-118">7/VT\_I4</span></span>    | <span data-ttu-id="ab3ad-119">O número total de itens exclusivos para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-119">The total number of unique items for this query.</span></span> <span data-ttu-id="ab3ad-120">Para uma consulta SELECT, este é o número de itens no conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="ab3ad-121">Para um grupo na consulta, este é o número de itens folha exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="ab3ad-122">Essa propriedade não identifica o número de linhas no conjunto de linhas de nível superior (o número de grupos de nível superior).</span><span class="sxs-lookup"><span data-stu-id="ab3ad-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="ab3ad-123">Onde ID (WHEREid)</span><span class="sxs-lookup"><span data-stu-id="ab3ad-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="ab3ad-124">8/VT \_ i4</span><span class="sxs-lookup"><span data-stu-id="ab3ad-124">8/VT\_I4</span></span>    | <span data-ttu-id="ab3ad-125">O identificador para as restrições usadas para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="ab3ad-126">Se um conjunto de linhas for aberto quando uma nova consulta for executada, a nova consulta poderá reutilizar as restrições da consulta mais antiga, aproveitando assim o trabalho já concluído.</span><span class="sxs-lookup"><span data-stu-id="ab3ad-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="ab3ad-127">Para obter mais informações sobre como reutilizar restrições WHERE, consulte a [função ReuseWhere](-search-sql-reusewhere.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ad-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ab3ad-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab3ad-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab3ad-129">Priorização de indexação e eventos de conjunto de linhas no Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab3ad-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
