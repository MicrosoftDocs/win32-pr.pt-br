---
title: Elemento VerticalMenuLayout
description: Representa um layout vertical de itens em uma galeria.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Faixa de VerticalMenuLayout do elemento do Windows
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2020
ms.locfileid: "103640360"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="8ce4b-104">Elemento VerticalMenuLayout</span><span class="sxs-lookup"><span data-stu-id="8ce4b-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="8ce4b-105">Representa um layout vertical de itens em uma galeria.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="8ce4b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8ce4b-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="8ce4b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ce4b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ce4b-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="8ce4b-108">Attribute</span></span></th>
<th><span data-ttu-id="8ce4b-109">Type</span><span class="sxs-lookup"><span data-stu-id="8ce4b-109">Type</span></span></th>
<th><span data-ttu-id="8ce4b-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8ce4b-110">Required</span></span></th>
<th><span data-ttu-id="8ce4b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ce4b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ce4b-112"><strong>Garra</strong></span><span class="sxs-lookup"><span data-stu-id="8ce4b-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="8ce4b-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="8ce4b-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="8ce4b-114">Não</span><span class="sxs-lookup"><span data-stu-id="8ce4b-114">No</span></span><br/></td>
<td><span data-ttu-id="8ce4b-115">Um identificador de redimensionamento anexado ao menu suspenso da galeria.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="8ce4b-116">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="8ce4b-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="8ce4b-117">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="8ce4b-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8ce4b-118"><dt><span></span><span></span><strong></strong> Vertical</span><span class="sxs-lookup"><span data-stu-id="8ce4b-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="8ce4b-119">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ce4b-120"><strong>IsMultipleHighlightingEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="8ce4b-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="8ce4b-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="8ce4b-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="8ce4b-122">Não</span><span class="sxs-lookup"><span data-stu-id="8ce4b-122">No</span></span><br/></td>
<td><span data-ttu-id="8ce4b-123"><strong>Windows 8 e mais recente</strong></span><span class="sxs-lookup"><span data-stu-id="8ce4b-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="8ce4b-124">Realça todos os itens na lista até, e incluindo, o item atual de mouseover (em vez do item de mouseover somente).</span><span class="sxs-lookup"><span data-stu-id="8ce4b-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="8ce4b-125">Normalmente usado para várias funcionalidades de <strong>desfazer</strong> e <strong>refazer</strong> .</span><span class="sxs-lookup"><span data-stu-id="8ce4b-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="8ce4b-126">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="8ce4b-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8ce4b-127"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="8ce4b-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ce4b-128">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ce4b-129"><strong>Linhas</strong></span><span class="sxs-lookup"><span data-stu-id="8ce4b-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="8ce4b-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8ce4b-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="8ce4b-131">Não</span><span class="sxs-lookup"><span data-stu-id="8ce4b-131">No</span></span><br/></td>
<td><span data-ttu-id="8ce4b-132">Especifica o número de linhas de item a serem visíveis sem rolagem.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="8ce4b-133">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="8ce4b-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="8ce4b-134">Qualquer inteiro positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="8ce4b-135">O padrão é <strong>-1</strong> , que especifica a exibição de quantas linhas de item possível.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8ce4b-136">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8ce4b-136">Child elements</span></span>

<span data-ttu-id="8ce4b-137">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8ce4b-138">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8ce4b-138">Parent elements</span></span>



| <span data-ttu-id="8ce4b-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="8ce4b-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ce4b-140">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="8ce4b-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="8ce4b-141">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="8ce4b-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="8ce4b-142">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="8ce4b-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8ce4b-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ce4b-143">Remarks</span></span>

<span data-ttu-id="8ce4b-144">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8ce4b-144">Required.</span></span>

<span data-ttu-id="8ce4b-145">O elemento **VerticalMenuLayout** ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deve ocorrer uma vez para cada elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="8ce4b-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="8ce4b-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ce4b-146">Examples</span></span>

<span data-ttu-id="8ce4b-147">O exemplo a seguir demonstra a marcação básica para um elemento **VerticalMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="8ce4b-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="8ce4b-148">Esta seção de código mostra as declarações de controle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="8ce4b-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="8ce4b-149">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8ce4b-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="8ce4b-150">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ce4b-150">Minimum supported system</span></span><br/> | <span data-ttu-id="8ce4b-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ce4b-151">Windows 7</span></span> |
| <span data-ttu-id="8ce4b-152">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="8ce4b-152">Can be empty</span></span>                        | <span data-ttu-id="8ce4b-153">Sim</span><span class="sxs-lookup"><span data-stu-id="8ce4b-153">Yes</span></span>       |



 

 





