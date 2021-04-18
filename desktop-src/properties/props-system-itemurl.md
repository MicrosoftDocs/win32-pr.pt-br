---
description: Representa uma URL bem formada que aponta para o item.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813653"
---
# <a name="systemitemurl"></a><span data-ttu-id="62635-103">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="62635-103">System.ItemUrl</span></span>

<span data-ttu-id="62635-104">Representa uma URL bem formada que aponta para o item.</span><span class="sxs-lookup"><span data-stu-id="62635-104">Represents a well-formed URL that points to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="62635-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62635-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="62635-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="62635-106">Remarks</span></span>

<span data-ttu-id="62635-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="62635-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="62635-108">Para referenciar itens de namespace do Shell por meio de APIs do Shell, use [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="62635-108">To reference Shell namespace items through Shell APIs, use [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="62635-109">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="62635-109">Example values:</span></span>



| <span data-ttu-id="62635-110">Tipo de item</span><span class="sxs-lookup"><span data-stu-id="62635-110">Item type</span></span> | <span data-ttu-id="62635-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="62635-111">Example</span></span>                        |
|-----------|--------------------------------|
| <span data-ttu-id="62635-112">Arquivo</span><span class="sxs-lookup"><span data-stu-id="62635-112">File</span></span>      | <span data-ttu-id="62635-113">hello.txt file:///c:/mydir/bar/</span><span class="sxs-lookup"><span data-stu-id="62635-113">file:///c:/mydir/bar/hello.txt</span></span> |
| <span data-ttu-id="62635-114">Arquivo</span><span class="sxs-lookup"><span data-stu-id="62635-114">File</span></span>      | <span data-ttu-id="62635-115">CSC://{GUID}/...</span><span class="sxs-lookup"><span data-stu-id="62635-115">csc://{GUID}/...</span></span>               |
| <span data-ttu-id="62635-116">Mensagem</span><span class="sxs-lookup"><span data-stu-id="62635-116">Message</span></span>   | <span data-ttu-id="62635-117">mapi://...</span><span class="sxs-lookup"><span data-stu-id="62635-117">mapi://...</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="62635-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62635-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62635-119">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="62635-119">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="62635-120">searchInfo</span><span class="sxs-lookup"><span data-stu-id="62635-120">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="62635-121">labelInfo</span><span class="sxs-lookup"><span data-stu-id="62635-121">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="62635-122">typeInfo</span><span class="sxs-lookup"><span data-stu-id="62635-122">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="62635-123">displayInfo</span><span class="sxs-lookup"><span data-stu-id="62635-123">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="62635-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="62635-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="62635-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="62635-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="62635-126">numberFormat</span><span class="sxs-lookup"><span data-stu-id="62635-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="62635-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="62635-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="62635-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="62635-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="62635-129">drawControl</span><span class="sxs-lookup"><span data-stu-id="62635-129">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="62635-130">editControl</span><span class="sxs-lookup"><span data-stu-id="62635-130">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="62635-131">filterControl</span><span class="sxs-lookup"><span data-stu-id="62635-131">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="62635-132">queryControl</span><span class="sxs-lookup"><span data-stu-id="62635-132">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
