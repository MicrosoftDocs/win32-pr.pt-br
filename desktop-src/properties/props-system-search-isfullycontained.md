---
description: Emitido como verdadeiro por todos os itens filho de um contêiner (como um email ou um arquivo compactado com uma extensão de nome. zip) que emite System. Search. IsClosedDirectory como TRUE. Isso garante que os itens filho sejam incluídos no índice de pesquisa.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506193"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="ac831-104">System. Search. IsFullyContained</span><span class="sxs-lookup"><span data-stu-id="ac831-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="ac831-105">Emitido como **verdadeiro** por todos os itens filho de um contêiner (como um email ou um arquivo compactado com uma extensão de nome. zip) que emite [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="ac831-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="ac831-106">Isso garante que os itens filho sejam incluídos no índice de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ac831-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="ac831-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac831-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="ac831-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac831-108">Remarks</span></span>

<span data-ttu-id="ac831-109">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="ac831-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="ac831-110">A propriedade [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) ajuda a otimizar o desempenho do indexador, permitindo que o indexador ignore a enumeração dos itens filho de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="ac831-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="ac831-111">No entanto, esses itens filhos são marcados pelo indexador como não visitado e, como tal, serão excluídos do índice.</span><span class="sxs-lookup"><span data-stu-id="ac831-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="ac831-112">Emitindo [System. Search. IsFullyContained]() como **true**, um item não é excluído do índice, apesar de não ter sido visitado.</span><span class="sxs-lookup"><span data-stu-id="ac831-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac831-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac831-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac831-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ac831-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ac831-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ac831-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ac831-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ac831-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ac831-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ac831-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ac831-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ac831-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ac831-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ac831-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ac831-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ac831-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ac831-121">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ac831-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ac831-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ac831-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ac831-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ac831-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ac831-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="ac831-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ac831-125">editControl</span><span class="sxs-lookup"><span data-stu-id="ac831-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ac831-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="ac831-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ac831-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="ac831-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
