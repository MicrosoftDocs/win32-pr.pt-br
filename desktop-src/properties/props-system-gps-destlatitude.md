---
description: Saiba como a propriedade System. GPS. DestLatitude indica a latitude do ponto de destino.
ms.assetid: 63d8a3a3-76ec-4121-b48b-eb5034117d04
title: System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbed51e89926b8bb505457bd9fd7bf7bd3b69ff2
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988961"
---
# <a name="systemgpsdestlatitude"></a><span data-ttu-id="c7ecb-103">System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="c7ecb-103">System.GPS.DestLatitude</span></span>

<span data-ttu-id="c7ecb-104">Indica a latitude do ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="c7ecb-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="c7ecb-105">Essa é uma matriz de três valores, da seguinte maneira: o índice 0 é o grau, o índice 1 é o minutos, o índice 2 é de segundos.</span><span class="sxs-lookup"><span data-stu-id="c7ecb-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="c7ecb-106">Cada um é calculado com base nos valores em PKEY \_ GPS \_ DESTLATITUDENUMERATOR e PKEY \_ GPS \_ DestLatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="c7ecb-106">Each is calculated from the values in PKEY\_GPS\_DestLatitudeNumerator and PKEY\_GPS\_DestLatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c7ecb-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7ecb-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLatitude
   shellPKey = PKEY_GPS_DestLatitude
   formatID = 9D1D7CC5-5C39-451C-86B3-928E2D18CC47
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c7ecb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ecb-108">Remarks</span></span>

<span data-ttu-id="c7ecb-109">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c7ecb-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7ecb-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7ecb-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7ecb-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c7ecb-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c7ecb-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c7ecb-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c7ecb-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c7ecb-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c7ecb-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c7ecb-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c7ecb-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c7ecb-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c7ecb-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="c7ecb-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-122">editControl</span><span class="sxs-lookup"><span data-stu-id="c7ecb-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="c7ecb-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c7ecb-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="c7ecb-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
