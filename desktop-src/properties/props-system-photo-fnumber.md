---
description: O valor de FNumber quando a foto foi tirada, como lida com as informações de EXIF (arquivo de imagem intercambiável).
ms.assetid: 914dc34d-34e9-4283-be26-203da945d3e9
title: System. Photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22498d498bdf606cb0562f93df9a7b4d40405ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169241"
---
# <a name="systemphotofnumber"></a><span data-ttu-id="f9cf1-103">System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="f9cf1-103">System.Photo.FNumber</span></span>

<span data-ttu-id="f9cf1-104">O valor de FNumber quando a foto foi tirada, como lida com as informações de EXIF (arquivo de imagem intercambiável). Essa propriedade é calculada de [System. Photo. FNumberNumerator](./props-system-photo-fnumbernumerator.md) e [System. Photo. FNumberDenominator](./props-system-photo-fnumberdenominator.md).</span><span class="sxs-lookup"><span data-stu-id="f9cf1-104">The FNumber value when the photo was taken, as read from the Exchangeable Image File (EXIF) information.This property is calculated from [System.Photo.FNumberNumerator](./props-system-photo-fnumbernumerator.md) and [System.Photo.FNumberDenominator](./props-system-photo-fnumberdenominator.md).</span></span>

<span data-ttu-id="f9cf1-105">Veja a seguir os possíveis valores obtidos da especificação EXIF 2,2.</span><span class="sxs-lookup"><span data-stu-id="f9cf1-105">The following are possible values as taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="f9cf1-106">1</span><span class="sxs-lookup"><span data-stu-id="f9cf1-106">1</span></span>
-   <span data-ttu-id="f9cf1-107">1.4</span><span class="sxs-lookup"><span data-stu-id="f9cf1-107">1.4</span></span>
-   <span data-ttu-id="f9cf1-108">2</span><span class="sxs-lookup"><span data-stu-id="f9cf1-108">2</span></span>
-   <span data-ttu-id="f9cf1-109">2.8</span><span class="sxs-lookup"><span data-stu-id="f9cf1-109">2.8</span></span>
-   <span data-ttu-id="f9cf1-110">4</span><span class="sxs-lookup"><span data-stu-id="f9cf1-110">4</span></span>
-   <span data-ttu-id="f9cf1-111">5.6</span><span class="sxs-lookup"><span data-stu-id="f9cf1-111">5.6</span></span>
-   <span data-ttu-id="f9cf1-112">8</span><span class="sxs-lookup"><span data-stu-id="f9cf1-112">8</span></span>
-   <span data-ttu-id="f9cf1-113">11</span><span class="sxs-lookup"><span data-stu-id="f9cf1-113">11</span></span>
-   <span data-ttu-id="f9cf1-114">16</span><span class="sxs-lookup"><span data-stu-id="f9cf1-114">16</span></span>
-   <span data-ttu-id="f9cf1-115">22</span><span class="sxs-lookup"><span data-stu-id="f9cf1-115">22</span></span>
-   <span data-ttu-id="f9cf1-116">32</span><span class="sxs-lookup"><span data-stu-id="f9cf1-116">32</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="f9cf1-117">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9cf1-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.FNumber
   shellPKey = PKEY_Photo_FNumber
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33437
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="f9cf1-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9cf1-118">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.FNumber
   shellPKey = PKEY_Photo_FNumber
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33437
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="f9cf1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9cf1-119">Remarks</span></span>

<span data-ttu-id="f9cf1-120">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="f9cf1-120">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9cf1-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9cf1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9cf1-122">Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2</span><span class="sxs-lookup"><span data-stu-id="f9cf1-122">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="f9cf1-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f9cf1-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f9cf1-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f9cf1-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f9cf1-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f9cf1-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f9cf1-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f9cf1-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-130">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f9cf1-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f9cf1-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f9cf1-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="f9cf1-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-134">editControl</span><span class="sxs-lookup"><span data-stu-id="f9cf1-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="f9cf1-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f9cf1-136">queryControl</span><span class="sxs-lookup"><span data-stu-id="f9cf1-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
