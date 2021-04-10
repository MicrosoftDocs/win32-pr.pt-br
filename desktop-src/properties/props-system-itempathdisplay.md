---
description: O caminho de exibição amigável para o item.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091583"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="fe61d-103">System. ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="fe61d-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="fe61d-104">O caminho de exibição amigável para o item.</span><span class="sxs-lookup"><span data-stu-id="fe61d-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="fe61d-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe61d-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="fe61d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe61d-106">Remarks</span></span>

<span data-ttu-id="fe61d-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="fe61d-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="fe61d-108">Se o item for um arquivo ou uma pasta, essa propriedade incluirá a extensão em todos os casos e será localizada se um nome localizado estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="fe61d-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="fe61d-109">Para outros itens, esse é o equivalente amigável, supondo que o item exista no armazenamento hierárquico.</span><span class="sxs-lookup"><span data-stu-id="fe61d-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="fe61d-110">Ao contrário de [System. ItemUrl](./props-system-itemurl.md), esse valor de propriedade não inclui o esquema de URL.</span><span class="sxs-lookup"><span data-stu-id="fe61d-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="fe61d-111">Para analisar um caminho de item, use System. ItemUrl ou [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="fe61d-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="fe61d-112">Para referenciar itens de namespace do shell usando APIs do Shell, use System. ParsingPath.</span><span class="sxs-lookup"><span data-stu-id="fe61d-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="fe61d-113">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="fe61d-113">Example values:</span></span>



| <span data-ttu-id="fe61d-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="fe61d-114">Path</span></span>                                   | <span data-ttu-id="fe61d-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="fe61d-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="fe61d-116">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="fe61d-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="fe61d-117">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="fe61d-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="fe61d-118">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="fe61d-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="fe61d-119">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="fe61d-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="fe61d-120">\\\\\\numbers.xls de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="fe61d-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="fe61d-121">\\\\\\numbers.xls de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="fe61d-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="fe61d-122">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="fe61d-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="fe61d-123">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="fe61d-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="fe61d-124">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="fe61d-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="fe61d-125">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="fe61d-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="fe61d-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe61d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe61d-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="fe61d-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fe61d-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="fe61d-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fe61d-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="fe61d-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fe61d-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="fe61d-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fe61d-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fe61d-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fe61d-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fe61d-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fe61d-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="fe61d-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fe61d-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="fe61d-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fe61d-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fe61d-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fe61d-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fe61d-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fe61d-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="fe61d-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fe61d-138">editControl</span><span class="sxs-lookup"><span data-stu-id="fe61d-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fe61d-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="fe61d-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fe61d-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="fe61d-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
