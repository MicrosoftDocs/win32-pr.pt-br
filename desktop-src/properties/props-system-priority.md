---
description: System. Priority
ms.assetid: 43f81cb5-7f2e-4f8f-ad31-8aad71765f60
title: System. Priority
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66e6930c9746d61f181c88076d10677d5cfdd787
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091744"
---
# <a name="systempriority"></a><span data-ttu-id="12a47-103">System. Priority</span><span class="sxs-lookup"><span data-stu-id="12a47-103">System.Priority</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="12a47-104">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="12a47-104">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Priority
   shellPKey = PKEY_Priority
   formatID = 9C1FCF74-2D97-41BA-B4AE-CB2E3661A6E4
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Low
            value = 0
            text = Low
            defineToken = PRIORITY_PROP_LOW
         enum
            name = Normal
            value = 1
            text = Normal
            defineToken = PRIORITY_PROP_NORMAL
         enum
            name = High
            value = 2
            text = High
            defineToken = PRIORITY_PROP_HIGH
```

## <a name="windows-vista"></a><span data-ttu-id="12a47-105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12a47-105">Windows Vista</span></span>

```
propertyDescription
   name = System.Priority
   shellPKey = PKEY_Priority
   formatID = 9C1FCF74-2D97-41BA-B4AE-CB2E3661A6E4
   propID = 5
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Low
            defineName = PRIORITY_PROP_LOW
         enum
            value = 1
            text = Normal
            defineName = PRIORITY_PROP_NORMAL
         enum
            value = 2
            text = High
            defineName = PRIORITY_PROP_HIGH
```

## <a name="remarks"></a><span data-ttu-id="12a47-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="12a47-106">Remarks</span></span>

<span data-ttu-id="12a47-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="12a47-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12a47-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12a47-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a47-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="12a47-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="12a47-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="12a47-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="12a47-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="12a47-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="12a47-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="12a47-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="12a47-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="12a47-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="12a47-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="12a47-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="12a47-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="12a47-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="12a47-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="12a47-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="12a47-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="12a47-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="12a47-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="12a47-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="12a47-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="12a47-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="12a47-120">editControl</span><span class="sxs-lookup"><span data-stu-id="12a47-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="12a47-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="12a47-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="12a47-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="12a47-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
