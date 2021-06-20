---
description: Leia sobre a propriedade System. ItemPathDisplayNarrow, que representa o caminho de exibição amigável para o item.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84455a8b69ebf42cb91c191d1c275b70eeeb5ac
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403889"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="39ae0-103">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="39ae0-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="39ae0-104">O caminho de exibição amigável para o item.</span><span class="sxs-lookup"><span data-stu-id="39ae0-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="39ae0-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39ae0-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="39ae0-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="39ae0-106">Remarks</span></span>

<span data-ttu-id="39ae0-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="39ae0-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="39ae0-108">Para otimizar uma coluna de exibição estreita, o formato da cadeia de caracteres deve ser personalizado para que o nome venha primeiro.</span><span class="sxs-lookup"><span data-stu-id="39ae0-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="39ae0-109">Se o item for um arquivo, o valor da propriedade excluirá a extensão do arquivo, mas incluirá nomes localizados, se estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="39ae0-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="39ae0-110">Se o item for uma mensagem, o valor incluirá [System. ItemNamePrefix](./props-system-itemnameprefix.md).</span><span class="sxs-lookup"><span data-stu-id="39ae0-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="39ae0-111">Para analisar um caminho de item, use [System. ItemUrl](./props-system-itemurl.md) ou [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="39ae0-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="39ae0-112">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="39ae0-112">Example values:</span></span>



| <span data-ttu-id="39ae0-113">Caminho</span><span class="sxs-lookup"><span data-stu-id="39ae0-113">Path</span></span>                                   | <span data-ttu-id="39ae0-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="39ae0-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="39ae0-115">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="39ae0-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="39ae0-116">Olá (c: \\ barra de mydir \\ )</span><span class="sxs-lookup"><span data-stu-id="39ae0-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="39ae0-117">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="39ae0-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="39ae0-118">GoodNews ( \\ \\ servidor \\ de \\ mydir de compartilhamento)</span><span class="sxs-lookup"><span data-stu-id="39ae0-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="39ae0-119">\\\\\\pasta de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="39ae0-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="39ae0-120">pasta ( \\ \\ compartilhamento do servidor \\ )</span><span class="sxs-lookup"><span data-stu-id="39ae0-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="39ae0-121">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="39ae0-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="39ae0-122">MyFolder (c: \\ mydir)</span><span class="sxs-lookup"><span data-stu-id="39ae0-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="39ae0-123">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="39ae0-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="39ae0-124">Re: Olá!</span><span class="sxs-lookup"><span data-stu-id="39ae0-124">Re: Hello!</span></span> <span data-ttu-id="39ae0-125">(Conta do/Mailbox/caixa de entrada)</span><span class="sxs-lookup"><span data-stu-id="39ae0-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="39ae0-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39ae0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39ae0-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="39ae0-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="39ae0-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="39ae0-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="39ae0-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="39ae0-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="39ae0-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="39ae0-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="39ae0-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="39ae0-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="39ae0-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="39ae0-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="39ae0-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="39ae0-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="39ae0-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="39ae0-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="39ae0-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="39ae0-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="39ae0-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="39ae0-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="39ae0-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="39ae0-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="39ae0-138">editControl</span><span class="sxs-lookup"><span data-stu-id="39ae0-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="39ae0-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="39ae0-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="39ae0-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="39ae0-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
