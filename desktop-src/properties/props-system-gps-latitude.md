---
description: Indica latitude.
ms.assetid: f36f81b3-4e3d-4e06-a039-c243fd69c937
title: System. GPS. latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996c0edf41e03bc7f4a824ae9ed812450eb36e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502095"
---
# <a name="systemgpslatitude"></a><span data-ttu-id="3a0d1-103">System. GPS. latitude</span><span class="sxs-lookup"><span data-stu-id="3a0d1-103">System.GPS.Latitude</span></span>

<span data-ttu-id="3a0d1-104">Indica latitude.</span><span class="sxs-lookup"><span data-stu-id="3a0d1-104">Indicates latitude.</span></span> <span data-ttu-id="3a0d1-105">Essa é uma matriz de três valores, da seguinte maneira: o índice 0 é o grau, o índice 1 é o minutos, o índice 2 é de segundos.</span><span class="sxs-lookup"><span data-stu-id="3a0d1-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="3a0d1-106">Cada um é calculado com base nos valores em PKEY \_ GPS \_ LATITUDENUMERATOR e PKEY \_ GPS \_ LatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="3a0d1-106">Each is calculated from the values in PKEY\_GPS\_LatitudeNumerator and PKEY\_GPS\_LatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="3a0d1-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a0d1-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.GPS.Latitude
   shellPKey = PKEY_GPS_Latitude
   formatID = 8727CFFF-4868-4EC6-AD5B-81B98521D1AB
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a><span data-ttu-id="3a0d1-108">Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a0d1-108">Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.Latitude
   shellPKey = PKEY_GPS_Latitude
   formatID = 8727CFFF-4868-4EC6-AD5B-81B98521D1AB
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="3a0d1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a0d1-109">Remarks</span></span>

<span data-ttu-id="3a0d1-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="3a0d1-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="3a0d1-111">O requisito de uma referência de cadeia de caracteres indireta específica para o `label` atributo de **labelInfo** foi adicionado ao Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3a0d1-111">The requirement of a specific indirect string reference for the `label` attribute of **labelInfo** was added for Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a0d1-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a0d1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a0d1-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3a0d1-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3a0d1-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3a0d1-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="3a0d1-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3a0d1-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3a0d1-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3a0d1-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="3a0d1-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3a0d1-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3a0d1-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="3a0d1-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-124">editControl</span><span class="sxs-lookup"><span data-stu-id="3a0d1-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="3a0d1-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3a0d1-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="3a0d1-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
