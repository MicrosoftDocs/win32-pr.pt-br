---
description: Se a variante for \_ verdadeira, o instalador do dispositivo estará instalando o software no momento.
ms.assetid: 7C62C1E3-D3F3-49ce-A19D-B3A1C14E24D6
title: System. Devices. IsSoftwareInstalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ba8b61b2c2a11c6e35efb9bafaae69aeb3d01d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010950"
---
# <a name="systemdevicesissoftwareinstalling"></a><span data-ttu-id="80d58-103">System. Devices. IsSoftwareInstalling</span><span class="sxs-lookup"><span data-stu-id="80d58-103">System.Devices.IsSoftwareInstalling</span></span>

<span data-ttu-id="80d58-104">Se a variante for \_ verdadeira, o instalador do dispositivo estará instalando o software no momento.</span><span class="sxs-lookup"><span data-stu-id="80d58-104">If VARIANT\_TRUE, the device installer is currently installing software.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="80d58-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="80d58-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Device setup in progress
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="windows-7"></a><span data-ttu-id="80d58-106">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80d58-106">Windows 7</span></span>

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Software is installing for this device
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="remarks"></a><span data-ttu-id="80d58-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="80d58-107">Remarks</span></span>

<span data-ttu-id="80d58-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="80d58-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80d58-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80d58-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d58-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="80d58-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="80d58-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="80d58-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="80d58-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="80d58-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="80d58-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="80d58-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="80d58-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="80d58-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="80d58-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="80d58-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="80d58-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="80d58-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="80d58-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="80d58-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="80d58-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="80d58-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="80d58-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="80d58-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="80d58-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="80d58-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="80d58-121">editControl</span><span class="sxs-lookup"><span data-stu-id="80d58-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="80d58-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="80d58-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="80d58-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="80d58-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
