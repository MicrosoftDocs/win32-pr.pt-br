---
description: O valor de brilho da imagem, em unidades de APEX, geralmente no intervalo de-99,99 a 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772582"
---
# <a name="systemphotobrightness"></a><span data-ttu-id="6279e-103">System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="6279e-103">System.Photo.Brightness</span></span>

<span data-ttu-id="6279e-104">O valor de brilho da imagem, em unidades de APEX, geralmente no intervalo de-99,99 a 99,99.</span><span class="sxs-lookup"><span data-stu-id="6279e-104">The brightness value of the image, in APEX units, usually in the range of -99.99 to 99.99.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6279e-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6279e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6279e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="6279e-106">Remarks</span></span>

<span data-ttu-id="6279e-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6279e-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6279e-108">Consulte a especificação EXIF 2,2, anexo C, para obter uma comparação de números de [System. Photo. Brightness]() e Foot-Lambert medidas.</span><span class="sxs-lookup"><span data-stu-id="6279e-108">See the EXIF 2.2 specification, Annex C, for a comparison of [System.Photo.Brightness]() numbers and Foot-Lambert measurements.</span></span> <span data-ttu-id="6279e-109">Essa propriedade é calculada de [System. Photo. BrightnessNumerator](./props-system-photo-brightnessnumerator.md) e [System. Photo. BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span><span class="sxs-lookup"><span data-stu-id="6279e-109">This property is calculated from [System.Photo.BrightnessNumerator](./props-system-photo-brightnessnumerator.md) and [System.Photo.BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span></span> <span data-ttu-id="6279e-110">Se o numerador do valor registrado for FFFFFFFF. H, "desconhecido" deve ser indicado.</span><span class="sxs-lookup"><span data-stu-id="6279e-110">If the numerator of the recorded value is FFFFFFFF.H, "Unknown" should be indicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6279e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6279e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6279e-112">Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2</span><span class="sxs-lookup"><span data-stu-id="6279e-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="6279e-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6279e-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6279e-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6279e-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6279e-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6279e-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6279e-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6279e-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6279e-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6279e-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6279e-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6279e-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6279e-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6279e-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6279e-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6279e-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6279e-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6279e-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6279e-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6279e-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6279e-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="6279e-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6279e-124">editControl</span><span class="sxs-lookup"><span data-stu-id="6279e-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6279e-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="6279e-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6279e-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="6279e-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
