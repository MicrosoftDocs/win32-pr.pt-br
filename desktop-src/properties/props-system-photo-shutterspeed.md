---
description: A velocidade do obturador da câmera quando a foto foi tirada. Isso é fornecido em unidades de APEX.
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: System. Photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172ce97bf87e79dd86f83e68c91940748bbc283f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010935"
---
# <a name="systemphotoshutterspeed"></a><span data-ttu-id="6a9ae-104">System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="6a9ae-104">System.Photo.ShutterSpeed</span></span>

<span data-ttu-id="6a9ae-105">A velocidade do obturador da câmera quando a foto foi tirada.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-105">The shutter speed of the camera when the photo was taken.</span></span> <span data-ttu-id="6a9ae-106">Isso é fornecido em unidades de APEX.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-106">This is given in APEX units.</span></span> <span data-ttu-id="6a9ae-107">Essa propriedade é calculada de [System. Photo. ShutterSpeedNumerator](./props-system-photo-shutterspeednumerator.md) e [System. Photo. ShutterSpeedDenominator](./props-system-photo-shutterspeeddenominator.md).</span><span class="sxs-lookup"><span data-stu-id="6a9ae-107">This property is calculated from [System.Photo.ShutterSpeedNumerator](./props-system-photo-shutterspeednumerator.md) and [System.Photo.ShutterSpeedDenominator](./props-system-photo-shutterspeeddenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="6a9ae-108">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a9ae-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="6a9ae-109">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a9ae-109">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6a9ae-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a9ae-110">Remarks</span></span>

<span data-ttu-id="6a9ae-111">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-111">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6a9ae-112">Consulte a especificação de EXIF (exchangable Image File) 2,2, anexo C, para a conversão desse valor em tempo de exposição.</span><span class="sxs-lookup"><span data-stu-id="6a9ae-112">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for the conversion of this value to exposure time.</span></span> <span data-ttu-id="6a9ae-113">Use [System. Photo. exposiçãotime](./props-system-photo-exposuretime.md) em qualquer exibição do Shell em vez de [System. Photo. ShutterSpeed]().</span><span class="sxs-lookup"><span data-stu-id="6a9ae-113">Use [System.Photo.ExposureTime](./props-system-photo-exposuretime.md) in any Shell views instead of [System.Photo.ShutterSpeed]().</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a9ae-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a9ae-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a9ae-115">Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2</span><span class="sxs-lookup"><span data-stu-id="6a9ae-115">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="6a9ae-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6a9ae-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6a9ae-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-118">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6a9ae-118">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-119">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6a9ae-119">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-120">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6a9ae-120">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-121">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6a9ae-121">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-122">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6a9ae-122">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-123">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6a9ae-123">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-124">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6a9ae-124">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-125">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6a9ae-125">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-126">drawControl</span><span class="sxs-lookup"><span data-stu-id="6a9ae-126">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-127">editControl</span><span class="sxs-lookup"><span data-stu-id="6a9ae-127">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-128">filterControl</span><span class="sxs-lookup"><span data-stu-id="6a9ae-128">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6a9ae-129">queryControl</span><span class="sxs-lookup"><span data-stu-id="6a9ae-129">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
