---
title: Propriedade ApplicationMenu. RecentItems
description: Representa um contêiner para o controle itens recentes no menu do aplicativo.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Faixa de ApplicationMenu de propriedades do Windows. RecentItems
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369651"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="d8785-104">Propriedade ApplicationMenu. RecentItems</span><span class="sxs-lookup"><span data-stu-id="d8785-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="d8785-105">Representa um contêiner para o controle [itens recentes](windowsribbon-controls-recentitems.md) no [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="d8785-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d8785-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d8785-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="d8785-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8785-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8785-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="d8785-108">Attribute</span></span></th>
<th><span data-ttu-id="d8785-109">Type</span><span class="sxs-lookup"><span data-stu-id="d8785-109">Type</span></span></th>
<th><span data-ttu-id="d8785-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8785-110">Required</span></span></th>
<th><span data-ttu-id="d8785-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8785-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8785-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d8785-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d8785-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="d8785-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d8785-114">Não</span><span class="sxs-lookup"><span data-stu-id="d8785-114">No</span></span><br/></td>
<td><span data-ttu-id="d8785-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d8785-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d8785-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="d8785-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d8785-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="d8785-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d8785-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d8785-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d8785-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8785-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d8785-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d8785-120">Child elements</span></span>



| <span data-ttu-id="d8785-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8785-121">Element</span></span>                                                             | <span data-ttu-id="d8785-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8785-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="d8785-123">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="d8785-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="d8785-124">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="d8785-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d8785-125">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d8785-125">Parent elements</span></span>



| <span data-ttu-id="d8785-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8785-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="d8785-127">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="d8785-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d8785-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8785-128">Remarks</span></span>

<span data-ttu-id="d8785-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d8785-129">Optional.</span></span>

<span data-ttu-id="d8785-130">Pode ocorrer no máximo uma vez para cada elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="d8785-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="d8785-131">O controle [itens recentes](windowsribbon-controls-recentitems.md) exibe a lista de itens usados mais recentemente (MRU) do aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d8785-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="d8785-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8785-132">Examples</span></span>

<span data-ttu-id="d8785-133">O exemplo a seguir demonstra a marcação básica para o controle [itens recentes](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="d8785-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="d8785-134">O exemplo a seguir mostra uma declaração de comando [**RecentItems**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="d8785-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="d8785-135">O exemplo a seguir mostra a declaração de controles **ApplicationMenu. RecentItems** e [**RecentItems**](windowsribbon-element-recentitems.md) associados.</span><span class="sxs-lookup"><span data-stu-id="d8785-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="d8785-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8785-136">Requirements</span></span>



| <span data-ttu-id="d8785-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8785-137">Requirement</span></span> | <span data-ttu-id="d8785-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d8785-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d8785-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8785-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d8785-140">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d8785-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d8785-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8785-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d8785-142">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d8785-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8785-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8785-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8785-144">Controle de menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="d8785-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="d8785-145">Controle de itens recentes</span><span class="sxs-lookup"><span data-stu-id="d8785-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





