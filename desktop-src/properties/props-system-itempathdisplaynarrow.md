---
description: O caminho de exibição amigável para o item.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171008"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="8c2cc-103">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="8c2cc-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="8c2cc-104">O caminho de exibição amigável para o item.</span><span class="sxs-lookup"><span data-stu-id="8c2cc-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="8c2cc-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c2cc-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="8c2cc-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c2cc-106">Remarks</span></span>

<span data-ttu-id="8c2cc-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="8c2cc-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="8c2cc-108">Para otimizar uma coluna de exibição estreita, o formato da cadeia de caracteres deve ser personalizado para que o nome venha primeiro.</span><span class="sxs-lookup"><span data-stu-id="8c2cc-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="8c2cc-109">Se o item for um arquivo, o valor da propriedade excluirá a extensão do arquivo, mas incluirá nomes localizados, se estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="8c2cc-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="8c2cc-110">Se o item for uma mensagem, o valor incluirá [System. ItemNamePrefix](./props-system-itemnameprefix.md).</span><span class="sxs-lookup"><span data-stu-id="8c2cc-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="8c2cc-111">Para analisar um caminho de item, use [System. ItemUrl](./props-system-itemurl.md) ou [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="8c2cc-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="8c2cc-112">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="8c2cc-112">Example values:</span></span>



| <span data-ttu-id="8c2cc-113">Caminho</span><span class="sxs-lookup"><span data-stu-id="8c2cc-113">Path</span></span>                                   | <span data-ttu-id="8c2cc-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="8c2cc-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="8c2cc-115">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="8c2cc-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="8c2cc-116">Olá (c: \\ barra de mydir \\ )</span><span class="sxs-lookup"><span data-stu-id="8c2cc-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="8c2cc-117">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="8c2cc-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="8c2cc-118">GoodNews ( \\ \\ servidor \\ de \\ mydir de compartilhamento)</span><span class="sxs-lookup"><span data-stu-id="8c2cc-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="8c2cc-119">\\\\\\pasta de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="8c2cc-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="8c2cc-120">pasta ( \\ \\ compartilhamento do servidor \\ )</span><span class="sxs-lookup"><span data-stu-id="8c2cc-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="8c2cc-121">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="8c2cc-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="8c2cc-122">MyFolder (c: \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="8c2cc-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="8c2cc-123">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="8c2cc-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="8c2cc-124">Re: Olá!</span><span class="sxs-lookup"><span data-stu-id="8c2cc-124">Re: Hello!</span></span> <span data-ttu-id="8c2cc-125">(Conta do/Mailbox/caixa de entrada)</span><span class="sxs-lookup"><span data-stu-id="8c2cc-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c2cc-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c2cc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c2cc-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="8c2cc-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="8c2cc-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="8c2cc-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="8c2cc-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8c2cc-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="8c2cc-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="8c2cc-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="8c2cc-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8c2cc-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="8c2cc-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="8c2cc-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-138">editControl</span><span class="sxs-lookup"><span data-stu-id="8c2cc-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="8c2cc-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8c2cc-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="8c2cc-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
