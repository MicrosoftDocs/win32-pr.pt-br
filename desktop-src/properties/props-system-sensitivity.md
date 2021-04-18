---
description: .
ms.assetid: ad20504c-4920-4d72-86ef-04c82d71be70
title: System. sensibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507064ab361e33a3f1b04a221da87bd89a423e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815529"
---
# <a name="systemsensitivity"></a><span data-ttu-id="ee154-103">System. sensibilidade</span><span class="sxs-lookup"><span data-stu-id="ee154-103">System.Sensitivity</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="ee154-104">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee154-104">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Sensitivity
   shellPKey = PKEY_Sensitivity
   formatID = F8D3F6AC-4874-42CB-BE59-AB454B30716A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = SENSITIVITY_PROP_NORMAL
         enum
            name = Personal
            value = 1
            text = Personal
            defineToken = SENSITIVITY_PROP_PERSONAL
         enum
            name = Private
            value = 2
            text = Private
            defineToken = SENSITIVITY_PROP_PRIVATE
         enum
            name = Confidential
            value = 3
            text = Confidential
            defineToken = SENSITIVITY_PROP_CONFIDENTIAL
```

## <a name="windows-vista"></a><span data-ttu-id="ee154-105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee154-105">Windows Vista</span></span>

```
propertyDescription
   name = System.Sensitivity
   shellPKey = PKEY_Sensitivity
   formatID = F8D3F6AC-4874-42CB-BE59-AB454B30716A
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = SENSITIVITY_PROP_NORMAL
         enum
            value = 1
            text = Personal
            defineName = SENSITIVITY_PROP_PERSONAL
         enum
            value = 2
            text = Private
            defineName = SENSITIVITY_PROP_PRIVATE
         enum
            value = 3
            text = Confidential
            defineName = SENSITIVITY_PROP_CONFIDENTIAL
```

## <a name="remarks"></a><span data-ttu-id="ee154-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee154-106">Remarks</span></span>

<span data-ttu-id="ee154-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="ee154-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee154-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee154-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee154-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ee154-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ee154-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ee154-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ee154-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ee154-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ee154-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ee154-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ee154-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ee154-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ee154-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ee154-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ee154-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ee154-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ee154-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ee154-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ee154-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ee154-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ee154-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ee154-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ee154-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="ee154-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ee154-120">editControl</span><span class="sxs-lookup"><span data-stu-id="ee154-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ee154-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="ee154-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ee154-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="ee154-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
