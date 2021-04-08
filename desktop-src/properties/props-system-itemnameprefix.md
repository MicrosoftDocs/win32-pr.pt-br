---
description: 'O prefixo de um item, usado para mensagens de email em que o assunto começa com o prefixo &\# 0034; Re: &\# 0034;.'
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921111"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="6e264-103">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="6e264-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="6e264-104">O prefixo de um item, usado para mensagens de email em que o assunto começa com o prefixo "Re:".</span><span class="sxs-lookup"><span data-stu-id="6e264-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6e264-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e264-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6e264-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e264-106">Remarks</span></span>

<span data-ttu-id="6e264-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6e264-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6e264-108">Se o item for um arquivo, o valor dessa propriedade será VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="6e264-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="6e264-109">Se o item for uma mensagem, o valor dessa propriedade será os prefixos de encaminhamento ou de resposta (incluindo os dois pontos delimitadores, mas sem espaço em branco) ou VT \_ vazio se não houver nenhum prefixo.</span><span class="sxs-lookup"><span data-stu-id="6e264-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="6e264-110">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="6e264-110">Example values:</span></span>



| <span data-ttu-id="6e264-111">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="6e264-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="6e264-112">System. ItemName</span><span class="sxs-lookup"><span data-stu-id="6e264-112">System.ItemName</span></span>  | <span data-ttu-id="6e264-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="6e264-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="6e264-114">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="6e264-114">VT\_EMPTY</span></span>             | <span data-ttu-id="6e264-115">"Ótimo dia"</span><span class="sxs-lookup"><span data-stu-id="6e264-115">"Great day"</span></span>      | <span data-ttu-id="6e264-116">"Ótimo dia"</span><span class="sxs-lookup"><span data-stu-id="6e264-116">"Great day"</span></span>            |
| <span data-ttu-id="6e264-117">"Re:"</span><span class="sxs-lookup"><span data-stu-id="6e264-117">"Re:"</span></span>                 | <span data-ttu-id="6e264-118">"Ótimo dia"</span><span class="sxs-lookup"><span data-stu-id="6e264-118">"Great day"</span></span>      | <span data-ttu-id="6e264-119">"Re: ótimo dia"</span><span class="sxs-lookup"><span data-stu-id="6e264-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="6e264-120">"FWD:"</span><span class="sxs-lookup"><span data-stu-id="6e264-120">"Fwd: "</span></span>               | <span data-ttu-id="6e264-121">"Orçamento mensal"</span><span class="sxs-lookup"><span data-stu-id="6e264-121">"Monthly budget"</span></span> | <span data-ttu-id="6e264-122">"FWD: orçamento mensal"</span><span class="sxs-lookup"><span data-stu-id="6e264-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="6e264-123">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="6e264-123">VT\_EMPTY</span></span>             | <span data-ttu-id="6e264-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="6e264-124">accounts.xls</span></span>     | <span data-ttu-id="6e264-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="6e264-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="6e264-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e264-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e264-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6e264-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6e264-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6e264-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6e264-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6e264-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6e264-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6e264-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6e264-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6e264-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6e264-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6e264-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6e264-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6e264-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6e264-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6e264-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6e264-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6e264-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6e264-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6e264-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6e264-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="6e264-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e264-138">editControl</span><span class="sxs-lookup"><span data-stu-id="6e264-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e264-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="6e264-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6e264-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="6e264-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
