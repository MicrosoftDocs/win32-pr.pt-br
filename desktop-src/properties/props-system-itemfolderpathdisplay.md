---
description: O caminho de exibição amigável para o usuário da pasta pai de um item.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765114"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="1b1af-103">System. ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="1b1af-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="1b1af-104">O caminho de exibição amigável para o usuário da pasta pai de um item.</span><span class="sxs-lookup"><span data-stu-id="1b1af-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1b1af-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b1af-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1b1af-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b1af-106">Remarks</span></span>

<span data-ttu-id="1b1af-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="1b1af-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="1b1af-108">Se [System. ItemPathDisplay](./props-system-itempathdisplay.md) for VT \_ Empty, essa propriedade também deverá estar vazia.</span><span class="sxs-lookup"><span data-stu-id="1b1af-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="1b1af-109">Caso contrário, ele deve ser derivado adequadamente pela fonte de dados de System. ItemPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="1b1af-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="1b1af-110">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="1b1af-110">Example values:</span></span>



| <span data-ttu-id="1b1af-111">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b1af-111">Path</span></span>                                   | <span data-ttu-id="1b1af-112">ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="1b1af-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="1b1af-113">c: \\ arquivos \\ \\hello.txt pessoais</span><span class="sxs-lookup"><span data-stu-id="1b1af-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="1b1af-114">c: \\ arquivos \\ pessoais</span><span class="sxs-lookup"><span data-stu-id="1b1af-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="1b1af-115">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="1b1af-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="1b1af-116">\\\\\\mydir de compartilhamento de servidor \\</span><span class="sxs-lookup"><span data-stu-id="1b1af-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="1b1af-117">\\\\\\numbers.xls de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="1b1af-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="1b1af-118">\\\\compartilhamento de servidor \\</span><span class="sxs-lookup"><span data-stu-id="1b1af-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="1b1af-119">c: \\ comida na minha \\ pasta</span><span class="sxs-lookup"><span data-stu-id="1b1af-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="1b1af-120">c: \\ comida</span><span class="sxs-lookup"><span data-stu-id="1b1af-120">c:\\food</span></span>                 |
| <span data-ttu-id="1b1af-121">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="1b1af-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="1b1af-122">Conta de/Mailbox/caixa de entrada</span><span class="sxs-lookup"><span data-stu-id="1b1af-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="1b1af-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b1af-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b1af-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1b1af-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1b1af-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1b1af-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1b1af-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1b1af-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1b1af-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1b1af-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1b1af-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1b1af-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1b1af-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1b1af-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1b1af-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1b1af-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1b1af-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1b1af-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1b1af-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1b1af-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1b1af-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1b1af-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1b1af-134">drawControl</span><span class="sxs-lookup"><span data-stu-id="1b1af-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1b1af-135">editControl</span><span class="sxs-lookup"><span data-stu-id="1b1af-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1b1af-136">filterControl</span><span class="sxs-lookup"><span data-stu-id="1b1af-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1b1af-137">queryControl</span><span class="sxs-lookup"><span data-stu-id="1b1af-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
