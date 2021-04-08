---
description: NULL indica o caso normal (o arquivo está disponível offline). O caso parcial é apenas para pastas em que algum conteúdo pode estar disponível offline e alguns podem não.
ms.assetid: 46b03632-702e-46df-8204-33ada85adbee
title: System. FileOfflineAvailabilityStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ca5c3f004c89cfb7b8625f9eb939a42f7fe842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828609"
---
# <a name="systemfileofflineavailabilitystatus"></a><span data-ttu-id="404ec-104">System. FileOfflineAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="404ec-104">System.FileOfflineAvailabilityStatus</span></span>

<span data-ttu-id="404ec-105">NULL indica o caso normal (o arquivo está disponível offline).</span><span class="sxs-lookup"><span data-stu-id="404ec-105">Null indicates the normal case (file is available offline).</span></span> <span data-ttu-id="404ec-106">O caso parcial é apenas para pastas em que algum conteúdo pode estar disponível offline e alguns podem não.</span><span class="sxs-lookup"><span data-stu-id="404ec-106">The partial case is only for folders where some content may be available offline and some may not.</span></span>

## <a name="windows-10-version-1703"></a><span data-ttu-id="404ec-107">Windows 10, versão 1703</span><span class="sxs-lookup"><span data-stu-id="404ec-107">Windows 10, version 1703</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PARTIAL
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE
         enum
            name = CompletePinned
            value = 3
            text = CompletePinned
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE_PINNED
         enum
            name = Excluded
            value = 4
            text = Excluded
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_EXCLUDED
         enum
            name = Empty
            value = 5
            text = Empty
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_FOLDER_EMPTY
```

## <a name="windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="404ec-108">Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="404ec-108">Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_PARTIALLYAVAILABLEOFFLINE
```

## <a name="remarks"></a><span data-ttu-id="404ec-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="404ec-109">Remarks</span></span>

<span data-ttu-id="404ec-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="404ec-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="404ec-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="404ec-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="404ec-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="404ec-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="404ec-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="404ec-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="404ec-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="404ec-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="404ec-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="404ec-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="404ec-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="404ec-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="404ec-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="404ec-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="404ec-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="404ec-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="404ec-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="404ec-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="404ec-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="404ec-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="404ec-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="404ec-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="404ec-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="404ec-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="404ec-123">editControl</span><span class="sxs-lookup"><span data-stu-id="404ec-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="404ec-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="404ec-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="404ec-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="404ec-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
