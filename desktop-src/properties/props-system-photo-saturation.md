---
description: Indica a direção do processamento de saturação aplicado pela câmera quando a foto foi tirada.
ms.assetid: 209edf55-fd6c-416b-b175-346f5158fc2a
title: System. Photo. saturação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50655b1d9344bb3c25576de9ece3ac6ef2bba95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794562"
---
# <a name="systemphotosaturation"></a><span data-ttu-id="c8364-103">System. Photo. saturação</span><span class="sxs-lookup"><span data-stu-id="c8364-103">System.Photo.Saturation</span></span>

<span data-ttu-id="c8364-104">Indica a direção do processamento de saturação aplicado pela câmera quando a foto foi tirada.</span><span class="sxs-lookup"><span data-stu-id="c8364-104">Indicates the direction of saturation processing applied by the camera when the photo was taken.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="c8364-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8364-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_SATURATION_NORMAL
         enum
            name = Low
            value = 1
            text = Low saturation
            defineToken = PHOTO_SATURATION_LOW
         enum
            name = High
            value = 2
            text = High saturation
            defineToken = PHOTO_SATURATION_HIGH
```

## <a name="windows-vista"></a><span data-ttu-id="c8364-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8364-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Saturation
   shellPKey = PKEY_Photo_Saturation
   formatID = 49237325-A95A-4F67-B211-816B2D45D2E0
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_SATURATION_NORMAL
         enum
            value = 1
            text = Low saturation
            defineName = PHOTO_SATURATION_LOW
         enum
            value = 2
            text = High saturation
            defineName = PHOTO_SATURATION_HIGH
```

## <a name="remarks"></a><span data-ttu-id="c8364-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8364-107">Remarks</span></span>

<span data-ttu-id="c8364-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c8364-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8364-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8364-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8364-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c8364-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c8364-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c8364-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c8364-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c8364-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c8364-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c8364-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c8364-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c8364-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c8364-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c8364-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c8364-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c8364-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c8364-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c8364-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c8364-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c8364-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c8364-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c8364-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c8364-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="c8364-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c8364-121">editControl</span><span class="sxs-lookup"><span data-stu-id="c8364-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c8364-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="c8364-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c8364-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="c8364-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
