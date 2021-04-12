---
description: O nome de exibição amigável da pasta pai de um item.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170484"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="1c8fe-103">System. ItemFolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="1c8fe-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="1c8fe-104">O nome de exibição amigável da pasta pai de um item.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="1c8fe-105">Isso é derivado de [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="1c8fe-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="1c8fe-106">Se essa propriedade for VT \_ vazia, essa propriedade deverá ser também.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="1c8fe-107">Se a pasta for uma pasta de arquivos, o valor será localizado se um nome localizado estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1c8fe-108">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c8fe-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1c8fe-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c8fe-109">Remarks</span></span>

<span data-ttu-id="1c8fe-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="1c8fe-111">Se [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) for VT \_ Empty, essa propriedade também deverá estar vazia.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="1c8fe-112">Caso contrário, ele deve ser derivado adequadamente pela fonte de dados de System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="1c8fe-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="1c8fe-113">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="1c8fe-113">Examples:</span></span>



| <span data-ttu-id="1c8fe-114">Caminho fornecido</span><span class="sxs-lookup"><span data-stu-id="1c8fe-114">Given path</span></span>                             | <span data-ttu-id="1c8fe-115">Nome de exibição da pasta</span><span class="sxs-lookup"><span data-stu-id="1c8fe-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="1c8fe-116">c: \\ Myfiles \\hello.txt de texto \\</span><span class="sxs-lookup"><span data-stu-id="1c8fe-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="1c8fe-117">Texto</span><span class="sxs-lookup"><span data-stu-id="1c8fe-117">Text</span></span>                |
| <span data-ttu-id="1c8fe-118">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="1c8fe-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="1c8fe-119">mydir</span><span class="sxs-lookup"><span data-stu-id="1c8fe-119">mydir</span></span>               |
| <span data-ttu-id="1c8fe-120">\\\\\\numbers.xls de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="1c8fe-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="1c8fe-121">compartilhar</span><span class="sxs-lookup"><span data-stu-id="1c8fe-121">share</span></span>               |
| <span data-ttu-id="1c8fe-122">c: \\ pastas \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="1c8fe-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="1c8fe-123">Pastas</span><span class="sxs-lookup"><span data-stu-id="1c8fe-123">Folders</span></span>             |
| <span data-ttu-id="1c8fe-124">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="1c8fe-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="1c8fe-125">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="1c8fe-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="1c8fe-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c8fe-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c8fe-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1c8fe-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1c8fe-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1c8fe-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1c8fe-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1c8fe-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1c8fe-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1c8fe-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1c8fe-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1c8fe-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1c8fe-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="1c8fe-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-138">editControl</span><span class="sxs-lookup"><span data-stu-id="1c8fe-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="1c8fe-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1c8fe-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="1c8fe-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
