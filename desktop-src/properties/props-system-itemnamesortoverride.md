---
description: Essa cadeia de caracteres deve ser definida como a versão fonética do nome de exibição conforme definido em System. ItemNameDisplay em local CJK (CHS Pinyin, JPN hiragana, KOR Hangul, etc.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170700"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="ed8d3-103">System. ItemNameSortOverride</span><span class="sxs-lookup"><span data-stu-id="ed8d3-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="ed8d3-104">Essa cadeia de caracteres deve ser definida como a versão fonética do nome de exibição conforme definido em System. ItemNameDisplay em local CJK (CHS Pinyin, JPN hiragana, KOR Hangul, etc.).</span><span class="sxs-lookup"><span data-stu-id="ed8d3-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="ed8d3-105">O primeiro caractere desse campo também é usado para agrupar nomes por FirstLetter.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="ed8d3-106">Para a maioria dos idiomas não-CJK, esse campo não precisa ser definido (nesse caso, System. ItemNameDisplay será usado). No entanto, se for desejável substituir a letra de agrupamento (por exemplo, para remover os principais artigos, como "a" e "o"), uma cadeia de caracteres alternativa poderá ser fornecida aqui.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="ed8d3-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="ed8d3-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="ed8d3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed8d3-108">Remarks</span></span>

<span data-ttu-id="ed8d3-109">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed8d3-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed8d3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed8d3-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ed8d3-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ed8d3-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ed8d3-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ed8d3-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ed8d3-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ed8d3-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ed8d3-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ed8d3-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ed8d3-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ed8d3-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="ed8d3-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-122">editControl</span><span class="sxs-lookup"><span data-stu-id="ed8d3-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="ed8d3-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ed8d3-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="ed8d3-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
