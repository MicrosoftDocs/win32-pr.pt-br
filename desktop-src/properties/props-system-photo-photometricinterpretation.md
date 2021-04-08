---
description: A composição de pixel.
ms.assetid: e2bb7f82-10dc-4fa0-875d-fc58c133024d
title: System. Photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f6b431470780def946dbb8958e9e3eb6698322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010938"
---
# <a name="systemphotophotometricinterpretation"></a><span data-ttu-id="4d6a2-103">System. Photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="4d6a2-103">System.Photo.PhotometricInterpretation</span></span>

<span data-ttu-id="4d6a2-104">A composição de pixel.</span><span class="sxs-lookup"><span data-stu-id="4d6a2-104">The pixel composition.</span></span> <span data-ttu-id="4d6a2-105">Em dados compactados em JPEG, um marcador JPEG é usado em vez dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="4d6a2-105">In JPEG compressed data, a JPEG marker is used instead of this property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="4d6a2-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d6a2-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.PhotometricInterpretation
   shellPKey = PKEY_Photo_PhotometricInterpretation
   formatID = 341796F1-1DF9-4B1C-A564-91BDEFA43877
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = RGB
            value = 2
            text = RGB
            defineToken = PHOTO_PHOTOMETRIC_RGB
         enum
            name = YCbCr
            value = 6
            text = YCbCr
            defineToken = PHOTO_PHOTOMETRIC_YCBCR
```

## <a name="windows-vista"></a><span data-ttu-id="4d6a2-107">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d6a2-107">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.PhotometricInterpretation
   shellPKey = PKEY_Photo_PhotometricInterpretation
   formatID = 341796F1-1DF9-4B1C-A564-91BDEFA43877
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 2
            text = RGB
            defineName = PHOTO_PHOTOMETRIC_RGB
         enum
            value = 6
            text = YCbCr
            defineName = PHOTO_PHOTOMETRIC_YCBCR
```

## <a name="remarks"></a><span data-ttu-id="4d6a2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d6a2-108">Remarks</span></span>

<span data-ttu-id="4d6a2-109">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="4d6a2-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="4d6a2-110">O valor padrão do `isInnate` atributo do elemento **TypeInfo** foi alterado de **false** para **true** a partir do Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4d6a2-110">The default value of the `isInnate` attribute of the **typeInfo** element was changed from **false** to **true** as of Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d6a2-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d6a2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d6a2-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4d6a2-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4d6a2-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4d6a2-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4d6a2-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4d6a2-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4d6a2-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4d6a2-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="4d6a2-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4d6a2-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4d6a2-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="4d6a2-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-123">editControl</span><span class="sxs-lookup"><span data-stu-id="4d6a2-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="4d6a2-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4d6a2-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="4d6a2-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
