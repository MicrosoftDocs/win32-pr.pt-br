---
description: O modo do programa de exposição da câmera no momento em que a foto foi tirada, como lida com as informações de EXIF (arquivo de imagem intercambiável).
ms.assetid: d27003b4-f30a-4c48-b32f-933b2f29182a
title: System. Photo. ExposureProgram
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e0678f4316cf5aee9c5e13b26518208bf546c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169246"
---
# <a name="systemphotoexposureprogram"></a><span data-ttu-id="f77c5-103">System. Photo. ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="f77c5-103">System.Photo.ExposureProgram</span></span>

<span data-ttu-id="f77c5-104">O modo do programa de exposição da câmera no momento em que a foto foi tirada, como lida com as informações de EXIF (arquivo de imagem intercambiável).</span><span class="sxs-lookup"><span data-stu-id="f77c5-104">The Exposure Program mode of the camera at the time the photo was taken, as read from the Exchangeable Image File (EXIF) information.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="f77c5-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f77c5-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.ExposureProgram
   shellPKey = PKEY_Photo_ExposureProgram
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 34850
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = PHOTO_EXPOSUREPROGRAM_UNKNOWN
         enum
            name = Manual
            value = 1
            text = Manual
            defineToken = PHOTO_EXPOSUREPROGRAM_MANUAL
         enum
            name = Normal
            value = 2
            text = Normal
            defineToken = PHOTO_EXPOSUREPROGRAM_NORMAL
         enum
            name = Aperture
            value = 3
            text = Aperture Priority
            defineToken = PHOTO_EXPOSUREPROGRAM_APERTURE
         enum
            name = Shutter
            value = 4
            text = Shutter Priority
            defineToken = PHOTO_EXPOSUREPROGRAM_SHUTTER
         enum
            name = Creative
            value = 5
            text = Creative Program (biased toward depth of field)
            defineToken = PHOTO_EXPOSUREPROGRAM_CREATIVE
         enum
            name = Action
            value = 6
            text = Action Program (biased toward shutter speed)
            defineToken = PHOTO_EXPOSUREPROGRAM_ACTION
         enum
            name = Portrait
            value = 7
            text = Portrait Mode
            defineToken = PHOTO_EXPOSUREPROGRAM_PORTRAIT
         enum
            name = Landscape
            value = 8
            text = Landscape Mode
            defineToken = PHOTO_EXPOSUREPROGRAM_LANDSCAPE
```

## <a name="windows-vista"></a><span data-ttu-id="f77c5-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f77c5-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ExposureProgram
   shellPKey = PKEY_Photo_ExposureProgram
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 34850
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Unknown
            defineName = PHOTO_EXPOSUREPROGRAM_UNKNOWN
         enum
            value = 1
            text = Manual
            defineName = PHOTO_EXPOSUREPROGRAM_MANUAL
         enum
            value = 2
            text = Normal
            defineName = PHOTO_EXPOSUREPROGRAM_NORMAL
         enum
            value = 3
            text = Aperture Priority
            defineName = PHOTO_EXPOSUREPROGRAM_APERTURE
         enum
            value = 4
            text = Shutter Priority
            defineName = PHOTO_EXPOSUREPROGRAM_SHUTTER
         enum
            value = 5
            text = Creative Program (biased toward depth of field)
            defineName = PHOTO_EXPOSUREPROGRAM_CREATIVE
         enum
            value = 6
            text = Action Program (biased toward shutter speed)
            defineName = PHOTO_EXPOSUREPROGRAM_ACTION
         enum
            value = 7
            text = Portrait Mode
            defineName = PHOTO_EXPOSUREPROGRAM_PORTRAIT
         enum
            value = 8
            text = Landscape Mode
            defineName = PHOTO_EXPOSUREPROGRAM_LANDSCAPE
```

## <a name="remarks"></a><span data-ttu-id="f77c5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f77c5-107">Remarks</span></span>

<span data-ttu-id="f77c5-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="f77c5-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f77c5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f77c5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f77c5-110">Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2</span><span class="sxs-lookup"><span data-stu-id="f77c5-110">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="f77c5-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f77c5-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f77c5-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f77c5-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f77c5-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f77c5-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f77c5-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f77c5-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f77c5-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f77c5-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f77c5-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f77c5-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f77c5-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f77c5-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f77c5-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f77c5-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f77c5-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f77c5-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f77c5-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f77c5-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f77c5-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="f77c5-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f77c5-122">editControl</span><span class="sxs-lookup"><span data-stu-id="f77c5-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f77c5-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="f77c5-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f77c5-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="f77c5-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
