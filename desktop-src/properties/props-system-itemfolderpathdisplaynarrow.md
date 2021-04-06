---
description: O caminho de exibição amigável para o usuário da pasta pai de um item.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898927c23aae95b5037919c908a3ae86e020e1fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011093"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="eeeca-103">System. ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="eeeca-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="eeeca-104">O caminho de exibição amigável para o usuário da pasta pai de um item.</span><span class="sxs-lookup"><span data-stu-id="eeeca-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="eeeca-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eeeca-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="eeeca-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="eeeca-106">Remarks</span></span>

<span data-ttu-id="eeeca-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="eeeca-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="eeeca-108">O formato da cadeia de caracteres deve ser adaptado para que o nome da pasta venha primeiro, para otimizar uma coluna de exibição estreita.</span><span class="sxs-lookup"><span data-stu-id="eeeca-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="eeeca-109">Se a pasta for uma pasta de arquivos, o valor incluirá todos os nomes localizados.</span><span class="sxs-lookup"><span data-stu-id="eeeca-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="eeeca-110">Se [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) for VT \_ Empty, essa propriedade também deverá estar vazia.</span><span class="sxs-lookup"><span data-stu-id="eeeca-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="eeeca-111">Caso contrário, ele deve ser derivado adequadamente pela fonte de dados de System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="eeeca-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeeca-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eeeca-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeeca-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="eeeca-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="eeeca-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="eeeca-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="eeeca-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="eeeca-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="eeeca-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="eeeca-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="eeeca-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="eeeca-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="eeeca-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="eeeca-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="eeeca-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="eeeca-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="eeeca-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="eeeca-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="eeeca-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="eeeca-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="eeeca-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="eeeca-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="eeeca-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="eeeca-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="eeeca-124">editControl</span><span class="sxs-lookup"><span data-stu-id="eeeca-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="eeeca-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="eeeca-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="eeeca-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="eeeca-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
