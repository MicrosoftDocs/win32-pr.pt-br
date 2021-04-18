---
description: Essa propriedade é igual a System. Search. UrlToIndex, exceto pelo fato de que ela inclui a hora em que a URL foi modificada pela última vez.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785262"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="4f691-103">System. Search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="4f691-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="4f691-104">Essa propriedade é igual a [**System. Search. UrlToIndex**](props-system-search-urltoindex.md) , exceto pelo fato de que ela inclui a hora em que a URL foi modificada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="4f691-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="4f691-105">Essa é uma otimização para o indexador para que ele não precise chamar de volta para o manipulador de protocolo para solicitar essas informações para determinar se o conteúdo precisa ser indexado novamente.</span><span class="sxs-lookup"><span data-stu-id="4f691-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="4f691-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f691-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="4f691-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f691-107">Remarks</span></span>

<span data-ttu-id="4f691-108">Esta propriedade [System. Search. UrlToIndexWithModificationTime]() é a mesma que a propriedade [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , exceto que você também passa a hora da última modificação do documento.</span><span class="sxs-lookup"><span data-stu-id="4f691-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="4f691-109">Se a hora da última modificação for correspondente, o indexador assumirá que o documento já está indexado e lançará a notificação.</span><span class="sxs-lookup"><span data-stu-id="4f691-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="4f691-110">Essa propriedade é um vetor com dois elementos, um valor de **\_ LPWStr do VT** que contém a URL e um valor de **\_ FILETIME do VT** que contém a hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="4f691-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="4f691-111">[System. Search. UrlToIndexWithModificationTime]() foi chamado \_ de PID GTHR \_ DIRLINK \_ com \_ tempo em versões anteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4f691-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="4f691-112">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="4f691-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f691-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f691-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4f691-114">[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f691-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4f691-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4f691-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4f691-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4f691-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4f691-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4f691-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4f691-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4f691-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4f691-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4f691-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4f691-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4f691-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4f691-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4f691-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4f691-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="4f691-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4f691-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4f691-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4f691-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4f691-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4f691-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="4f691-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4f691-126">editControl</span><span class="sxs-lookup"><span data-stu-id="4f691-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4f691-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="4f691-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4f691-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="4f691-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
