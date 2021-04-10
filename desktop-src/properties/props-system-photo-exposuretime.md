---
description: O tempo de exposição para a foto, em segundos, como lido das informações de EXIF (arquivo de imagem intercambiável).
ms.assetid: 44f7e6d5-c4d9-4b41-b6c6-15145abb7983
title: Sistema. Photo. Exposiçãotime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5811a3d375f41883d1db8f392e714b7bbe0dfa8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169244"
---
# <a name="systemphotoexposuretime"></a><span data-ttu-id="00455-103">Sistema. Photo. Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="00455-103">System.Photo.ExposureTime</span></span>

<span data-ttu-id="00455-104">O tempo de exposição para a foto, em segundos, como lido das informações de EXIF (arquivo de imagem intercambiável).</span><span class="sxs-lookup"><span data-stu-id="00455-104">The exposure time for the photo, in seconds, as read from the Exchangeable Image File (EXIF) information.</span></span> <span data-ttu-id="00455-105">Essa propriedade é calculada de [System. Photo. ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) e [System. Photo. ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md).</span><span class="sxs-lookup"><span data-stu-id="00455-105">This property is calculated from [System.Photo.ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) and [System.Photo.ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md).</span></span>

<span data-ttu-id="00455-106">A seguir está uma lista de possíveis valores obtidos da especificação EXIF 2,2.</span><span class="sxs-lookup"><span data-stu-id="00455-106">The following is a list of possible values taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="00455-107">30</span><span class="sxs-lookup"><span data-stu-id="00455-107">30</span></span>
-   <span data-ttu-id="00455-108">15</span><span class="sxs-lookup"><span data-stu-id="00455-108">15</span></span>
-   <span data-ttu-id="00455-109">8</span><span class="sxs-lookup"><span data-stu-id="00455-109">8</span></span>
-   <span data-ttu-id="00455-110">4</span><span class="sxs-lookup"><span data-stu-id="00455-110">4</span></span>
-   <span data-ttu-id="00455-111">2</span><span class="sxs-lookup"><span data-stu-id="00455-111">2</span></span>
-   <span data-ttu-id="00455-112">1</span><span class="sxs-lookup"><span data-stu-id="00455-112">1</span></span>
-   <span data-ttu-id="00455-113">1/2</span><span class="sxs-lookup"><span data-stu-id="00455-113">1/2</span></span>
-   <span data-ttu-id="00455-114">1/4</span><span class="sxs-lookup"><span data-stu-id="00455-114">1/4</span></span>
-   <span data-ttu-id="00455-115">1/8</span><span class="sxs-lookup"><span data-stu-id="00455-115">1/8</span></span>
-   <span data-ttu-id="00455-116">1/15</span><span class="sxs-lookup"><span data-stu-id="00455-116">1/15</span></span>
-   <span data-ttu-id="00455-117">1/30</span><span class="sxs-lookup"><span data-stu-id="00455-117">1/30</span></span>
-   <span data-ttu-id="00455-118">1/60</span><span class="sxs-lookup"><span data-stu-id="00455-118">1/60</span></span>
-   <span data-ttu-id="00455-119">1/125</span><span class="sxs-lookup"><span data-stu-id="00455-119">1/125</span></span>
-   <span data-ttu-id="00455-120">1/250</span><span class="sxs-lookup"><span data-stu-id="00455-120">1/250</span></span>
-   <span data-ttu-id="00455-121">1/500</span><span class="sxs-lookup"><span data-stu-id="00455-121">1/500</span></span>
-   <span data-ttu-id="00455-122">1/1000</span><span class="sxs-lookup"><span data-stu-id="00455-122">1/1000</span></span>
-   <span data-ttu-id="00455-123">1/2000</span><span class="sxs-lookup"><span data-stu-id="00455-123">1/2000</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="00455-124">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00455-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ExposureTime
   shellPKey = PKEY_Photo_ExposureTime
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33434
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="00455-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="00455-125">Remarks</span></span>

<span data-ttu-id="00455-126">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="00455-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00455-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00455-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00455-128">Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2</span><span class="sxs-lookup"><span data-stu-id="00455-128">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="00455-129">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="00455-129">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="00455-130">searchInfo</span><span class="sxs-lookup"><span data-stu-id="00455-130">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="00455-131">labelInfo</span><span class="sxs-lookup"><span data-stu-id="00455-131">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="00455-132">typeInfo</span><span class="sxs-lookup"><span data-stu-id="00455-132">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="00455-133">displayInfo</span><span class="sxs-lookup"><span data-stu-id="00455-133">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="00455-134">stringFormat</span><span class="sxs-lookup"><span data-stu-id="00455-134">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="00455-135">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="00455-135">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="00455-136">numberFormat</span><span class="sxs-lookup"><span data-stu-id="00455-136">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="00455-137">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="00455-137">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="00455-138">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="00455-138">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="00455-139">drawControl</span><span class="sxs-lookup"><span data-stu-id="00455-139">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="00455-140">editControl</span><span class="sxs-lookup"><span data-stu-id="00455-140">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="00455-141">filterControl</span><span class="sxs-lookup"><span data-stu-id="00455-141">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="00455-142">queryControl</span><span class="sxs-lookup"><span data-stu-id="00455-142">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
