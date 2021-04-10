---
description: Indica a taxa de quadros para o fluxo de vídeo, em quadros por 1000 segundos.
ms.assetid: cd5a2ae0-43ef-44e4-aa70-bca33baf2a56
title: System. vídeo. taxa de quadros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbdee7991186621a9d636e2072cecafc70176d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170322"
---
# <a name="systemvideoframerate"></a><span data-ttu-id="13622-103">System. vídeo. taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="13622-103">System.Video.FrameRate</span></span>

<span data-ttu-id="13622-104">Indica a taxa de quadros para o fluxo de vídeo, em quadros por 1000 segundos.</span><span class="sxs-lookup"><span data-stu-id="13622-104">Indicates the frame rate for the video stream, in frames per 1000 seconds.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="13622-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="13622-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="13622-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13622-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="13622-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="13622-107">Remarks</span></span>

<span data-ttu-id="13622-108">Para ajudar a reduzir o erro de truncamento, essa propriedade não usa a medida de taxa de quadros padrão de quadros por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="13622-108">To help reduce truncation error, this property does not use the standard frame rate measure of frames per second (FPS).</span></span> <span data-ttu-id="13622-109">Em vez disso, essa propriedade mede a taxa de quadros como quadros por 1000 segundos (FPS multiplicado por 1000).</span><span class="sxs-lookup"><span data-stu-id="13622-109">Instead, this property measures frame rate as frames per 1000 seconds (FPS multiplied by 1000).</span></span> <span data-ttu-id="13622-110">Por exemplo, [System. video.]() coderate expressaria uma taxa de quadros de 29,97 fps como um valor inteiro de 29970.</span><span class="sxs-lookup"><span data-stu-id="13622-110">For example, [System.Video.FrameRate]() would express a frame rate of 29.97 FPS as an integer value of 29970.</span></span>

<span data-ttu-id="13622-111">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="13622-111">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13622-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13622-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13622-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="13622-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="13622-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="13622-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="13622-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="13622-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="13622-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="13622-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="13622-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="13622-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="13622-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="13622-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="13622-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="13622-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="13622-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="13622-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="13622-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="13622-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="13622-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="13622-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="13622-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="13622-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="13622-124">editControl</span><span class="sxs-lookup"><span data-stu-id="13622-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="13622-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="13622-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="13622-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="13622-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
