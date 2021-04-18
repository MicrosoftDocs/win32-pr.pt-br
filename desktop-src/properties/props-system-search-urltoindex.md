---
description: Emitido por um IFilter de contêiner para cada URL filho dentro do contêiner. Os filhos são eventualmente rastreados pelo indexador se estiverem dentro do escopo.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. Search. UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814484"
---
# <a name="systemsearchurltoindex"></a><span data-ttu-id="8aac3-104">System. Search. UrlToIndex</span><span class="sxs-lookup"><span data-stu-id="8aac3-104">System.Search.UrlToIndex</span></span>

<span data-ttu-id="8aac3-105">Emitido por um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de contêiner para cada URL filho dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8aac3-105">Emitted by a container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) for each child URL within the container.</span></span> <span data-ttu-id="8aac3-106">Os filhos são eventualmente rastreados pelo indexador se estiverem dentro do escopo.</span><span class="sxs-lookup"><span data-stu-id="8aac3-106">The children are eventually crawled by the indexer if they are within scope.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="8aac3-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8aac3-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="8aac3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8aac3-108">Remarks</span></span>

<span data-ttu-id="8aac3-109">Essa propriedade contém uma URL e é emitida por um manipulador de protocolo para cada URL filho ou Directory sob a URL atual.</span><span class="sxs-lookup"><span data-stu-id="8aac3-109">This property contains a URL and is emitted by a protocol handler for each child URL or directoy under the current URL.</span></span> <span data-ttu-id="8aac3-110">O indexador chama novamente o manipulador de protocolo e solicita que esse documento seja indexado.</span><span class="sxs-lookup"><span data-stu-id="8aac3-110">The indexer calls back into the protocol handler, and asks for that document to be indexed.</span></span> <span data-ttu-id="8aac3-111">[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) foi chamado PID \_ GTHR \_ DIRLINK em versões anteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="8aac3-111">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) was called PID\_GTHR\_DIRLINK in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="8aac3-112">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="8aac3-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aac3-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8aac3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aac3-114">System. Search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="8aac3-114">System.Search.UrlToIndexWithModificationTime</span></span>](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[<span data-ttu-id="8aac3-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="8aac3-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8aac3-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="8aac3-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8aac3-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="8aac3-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8aac3-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="8aac3-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8aac3-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8aac3-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8aac3-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="8aac3-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8aac3-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="8aac3-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8aac3-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="8aac3-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8aac3-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8aac3-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8aac3-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="8aac3-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8aac3-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="8aac3-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8aac3-126">editControl</span><span class="sxs-lookup"><span data-stu-id="8aac3-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8aac3-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="8aac3-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8aac3-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="8aac3-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
