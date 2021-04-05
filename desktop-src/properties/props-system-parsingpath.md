---
description: O caminho do namespace do Shell para o item.
ms.assetid: e0fb2092-0427-40c9-9e09-aefc5ef017e6
title: System. ParsingPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae62243ff37464617f87654f8ca1f04c3ea606da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828138"
---
# <a name="systemparsingpath"></a><span data-ttu-id="c30d2-103">System. ParsingPath</span><span class="sxs-lookup"><span data-stu-id="c30d2-103">System.ParsingPath</span></span>

<span data-ttu-id="c30d2-104">O caminho do namespace do Shell para o item.</span><span class="sxs-lookup"><span data-stu-id="c30d2-104">The Shell namespace path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c30d2-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c30d2-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ParsingPath
   shellPKey = PKEY_ParsingPath
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 30
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c30d2-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="c30d2-106">Remarks</span></span>

<span data-ttu-id="c30d2-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c30d2-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="c30d2-108">Esse valor pode ser passado para [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) para analisar o caminho para a pasta do Shell correta.</span><span class="sxs-lookup"><span data-stu-id="c30d2-108">This value can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="c30d2-109">Se o item for um arquivo, o valor será idêntico a [System. ItemPathDisplay](./props-system-itempathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="c30d2-109">If the item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).</span></span> <span data-ttu-id="c30d2-110">Se o item não puder ser acessado por meio do namespace do Shell, esse valor será VT \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="c30d2-110">If the item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c30d2-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c30d2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c30d2-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c30d2-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c30d2-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c30d2-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c30d2-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c30d2-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c30d2-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c30d2-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c30d2-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c30d2-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c30d2-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c30d2-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c30d2-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c30d2-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c30d2-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c30d2-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c30d2-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c30d2-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c30d2-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c30d2-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c30d2-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="c30d2-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c30d2-123">editControl</span><span class="sxs-lookup"><span data-stu-id="c30d2-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c30d2-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="c30d2-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c30d2-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="c30d2-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
