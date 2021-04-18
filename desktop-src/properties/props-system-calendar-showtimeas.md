---
description: Indica o status do participante durante o evento. O usuário pode optar por definir o status como livre, ocupado, provisório ou fora do escritório.
ms.assetid: ce2a1ab8-2937-446e-ac84-313649a4134d
title: System. Calendar. extimeas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a5766f459e0280a7c9397b513115c0f0ae9e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759800"
---
# <a name="systemcalendarshowtimeas"></a><span data-ttu-id="50953-104">System. Calendar. extimeas</span><span class="sxs-lookup"><span data-stu-id="50953-104">System.Calendar.ShowTimeAs</span></span>

<span data-ttu-id="50953-105">Indica o status do participante durante o evento.</span><span class="sxs-lookup"><span data-stu-id="50953-105">Indicates the status of the attendee during the event.</span></span> <span data-ttu-id="50953-106">O usuário pode optar por definir o status como livre, ocupado, provisório ou fora do escritório.</span><span class="sxs-lookup"><span data-stu-id="50953-106">User can choose to set the status as free, busy, tentative or out of office.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="50953-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="50953-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Calendar.ShowTimeAs
   shellPKey = PKEY_Calendar_ShowTimeAs
   formatID = 5BF396D4-5EB2-466F-BDE9-2FB3F2361D6E
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Free
            value = 0
            text = Free
            defineToken = CALENDAR_SHOWTIMEAS_FREE
         enum
            name = Tentative
            value = 1
            text = Tentative
            defineToken = CALENDAR_SHOWTIMEAS_TENTATIVE
         enum
            name = Busy
            value = 2
            text = Busy
            defineToken = CALENDAR_SHOWTIMEAS_BUSY
         enum
            name = OOF
            value = 3
            text = OOF
            defineToken = CALENDAR_SHOWTIMEAS_OOF
            mnemonics = Out of Office
```

## <a name="windows-vista"></a><span data-ttu-id="50953-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50953-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Calendar.ShowTimeAs
   shellPKey = PKEY_Calendar_ShowTimeAs
   formatID = 5BF396D4-5EB2-466F-BDE9-2FB3F2361D6E
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Free
            defineName = CALENDAR_SHOWTIMEAS_FREE
         enum
            value = 1
            text = Tentative
            defineName = CALENDAR_SHOWTIMEAS_TENTATIVE
         enum
            value = 2
            text = Busy
            defineName = CALENDAR_SHOWTIMEAS_BUSY
         enum
            value = 3
            text = OOF
            defineName = CALENDAR_SHOWTIMEAS_OOF
            mnemonics = Out of Office
```

## <a name="remarks"></a><span data-ttu-id="50953-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="50953-109">Remarks</span></span>

<span data-ttu-id="50953-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="50953-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50953-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50953-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50953-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="50953-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="50953-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="50953-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="50953-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="50953-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="50953-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="50953-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="50953-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="50953-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="50953-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="50953-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="50953-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="50953-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="50953-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="50953-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="50953-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="50953-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="50953-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="50953-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="50953-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="50953-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="50953-123">editControl</span><span class="sxs-lookup"><span data-stu-id="50953-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="50953-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="50953-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="50953-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="50953-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
