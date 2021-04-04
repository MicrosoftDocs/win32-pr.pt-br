---
title: Elemento RecentItems
description: Representa o controle itens recentes no menu do aplicativo.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Faixa de RecentItems do elemento do Windows
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104007055"
---
# <a name="recentitems-element"></a><span data-ttu-id="2bc16-104">Elemento RecentItems</span><span class="sxs-lookup"><span data-stu-id="2bc16-104">RecentItems element</span></span>

<span data-ttu-id="2bc16-105">Representa o controle [itens recentes](windowsribbon-controls-recentitems.md) no [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="2bc16-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="2bc16-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2bc16-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="2bc16-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2bc16-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bc16-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="2bc16-108">Attribute</span></span></th>
<th><span data-ttu-id="2bc16-109">Type</span><span class="sxs-lookup"><span data-stu-id="2bc16-109">Type</span></span></th>
<th><span data-ttu-id="2bc16-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2bc16-110">Required</span></span></th>
<th><span data-ttu-id="2bc16-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bc16-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bc16-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2bc16-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2bc16-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="2bc16-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2bc16-114">Não</span><span class="sxs-lookup"><span data-stu-id="2bc16-114">No</span></span><br/></td>
<td><span data-ttu-id="2bc16-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2bc16-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2bc16-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="2bc16-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2bc16-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="2bc16-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2bc16-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="2bc16-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2bc16-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2bc16-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bc16-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="2bc16-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="2bc16-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="2bc16-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="2bc16-122">Não</span><span class="sxs-lookup"><span data-stu-id="2bc16-122">No</span></span><br/></td>
<td><span data-ttu-id="2bc16-123">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="2bc16-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="2bc16-124">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="2bc16-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2bc16-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="2bc16-125">Default.</span></span> <br/> </dd> <span data-ttu-id="2bc16-126"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="2bc16-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bc16-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="2bc16-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="2bc16-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="2bc16-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="2bc16-129">Não</span><span class="sxs-lookup"><span data-stu-id="2bc16-129">No</span></span><br/></td>
<td><span data-ttu-id="2bc16-130">O número de itens recentes a serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="2bc16-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="2bc16-131">
<dt><span></span><span></span><strong></strong> (xs: nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="2bc16-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="2bc16-132">Um valor inteiro de 0 ou maior.</span><span class="sxs-lookup"><span data-stu-id="2bc16-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="2bc16-133">O padrão é <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="2bc16-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2bc16-134">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2bc16-134">Child elements</span></span>

<span data-ttu-id="2bc16-135">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="2bc16-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2bc16-136">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2bc16-136">Parent elements</span></span>



| <span data-ttu-id="2bc16-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="2bc16-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bc16-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="2bc16-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2bc16-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bc16-139">Remarks</span></span>

<span data-ttu-id="2bc16-140">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="2bc16-140">Required.</span></span>

<span data-ttu-id="2bc16-141">Deve ocorrer exatamente uma vez para cada elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="2bc16-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="2bc16-142">O controle [itens recentes](windowsribbon-controls-recentitems.md) exibe a lista de itens usados mais recentemente (MRU) do aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="2bc16-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="2bc16-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2bc16-143">Examples</span></span>

<span data-ttu-id="2bc16-144">O exemplo a seguir demonstra a marcação básica para o controle [itens recentes](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="2bc16-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="2bc16-145">O exemplo a seguir mostra uma declaração de comando **RecentItems** .</span><span class="sxs-lookup"><span data-stu-id="2bc16-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="2bc16-146">O exemplo a seguir mostra a declaração de controles **RecentItems** associada.</span><span class="sxs-lookup"><span data-stu-id="2bc16-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="2bc16-147">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2bc16-147">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2bc16-148">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bc16-148">Minimum supported system</span></span><br/> | <span data-ttu-id="2bc16-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bc16-149">Windows 7</span></span> |
| <span data-ttu-id="2bc16-150">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="2bc16-150">Can be empty</span></span>                        | <span data-ttu-id="2bc16-151">Sim</span><span class="sxs-lookup"><span data-stu-id="2bc16-151">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="2bc16-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bc16-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc16-153">Controle de menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2bc16-153">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="2bc16-154">Controle de itens recentes</span><span class="sxs-lookup"><span data-stu-id="2bc16-154">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





