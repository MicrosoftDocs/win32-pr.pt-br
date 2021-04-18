---
title: Elemento FlowMenuLayout
description: Representa um layout horizontal com quebras de linha para itens em uma galeria.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Faixa de FlowMenuLayout do elemento do Windows
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105793205"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="a324e-104">Elemento FlowMenuLayout</span><span class="sxs-lookup"><span data-stu-id="a324e-104">FlowMenuLayout element</span></span>

<span data-ttu-id="a324e-105">Representa um layout horizontal com quebras de linha para itens em uma galeria.</span><span class="sxs-lookup"><span data-stu-id="a324e-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="a324e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a324e-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="a324e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a324e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a324e-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a324e-108">Attribute</span></span></th>
<th><span data-ttu-id="a324e-109">Type</span><span class="sxs-lookup"><span data-stu-id="a324e-109">Type</span></span></th>
<th><span data-ttu-id="a324e-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a324e-110">Required</span></span></th>
<th><span data-ttu-id="a324e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a324e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a324e-112"><strong>Colunas</strong></span><span class="sxs-lookup"><span data-stu-id="a324e-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="a324e-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a324e-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="a324e-114">Não</span><span class="sxs-lookup"><span data-stu-id="a324e-114">No</span></span><br/></td>
<td><span data-ttu-id="a324e-115">Especifica o número de itens a serem exibidos em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="a324e-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="a324e-116">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="a324e-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="a324e-117">Qualquer inteiro positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="a324e-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="a324e-118">O padrão é <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="a324e-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a324e-119"><strong>Garra</strong></span><span class="sxs-lookup"><span data-stu-id="a324e-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="a324e-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="a324e-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="a324e-121">Não</span><span class="sxs-lookup"><span data-stu-id="a324e-121">No</span></span><br/></td>
<td><span data-ttu-id="a324e-122">Um identificador de redimensionamento anexado ao menu suspenso da galeria.</span><span class="sxs-lookup"><span data-stu-id="a324e-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="a324e-123">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a324e-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="a324e-124">
<dt><span></span><span></span><strong></strong> None</span><span class="sxs-lookup"><span data-stu-id="a324e-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a324e-125"><dt><span></span><span></span><strong></strong> Vertical</span><span class="sxs-lookup"><span data-stu-id="a324e-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="a324e-126"><dt><span></span><span></span><strong></strong> Canto</span><span class="sxs-lookup"><span data-stu-id="a324e-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="a324e-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a324e-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a324e-128"><strong>Linhas</strong></span><span class="sxs-lookup"><span data-stu-id="a324e-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="a324e-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a324e-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="a324e-130">Não</span><span class="sxs-lookup"><span data-stu-id="a324e-130">No</span></span><br/></td>
<td><span data-ttu-id="a324e-131">Especifica o número de linhas de item a serem visíveis sem rolagem.</span><span class="sxs-lookup"><span data-stu-id="a324e-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="a324e-132">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="a324e-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="a324e-133">Qualquer inteiro positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="a324e-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="a324e-134">O padrão é <strong>-1</strong> , que especifica a exibição de quantas linhas de item possível.</span><span class="sxs-lookup"><span data-stu-id="a324e-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a324e-135">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a324e-135">Child elements</span></span>

<span data-ttu-id="a324e-136">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="a324e-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a324e-137">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a324e-137">Parent elements</span></span>



| <span data-ttu-id="a324e-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="a324e-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a324e-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="a324e-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="a324e-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="a324e-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="a324e-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="a324e-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a324e-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="a324e-142">Remarks</span></span>

<span data-ttu-id="a324e-143">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a324e-143">Required.</span></span>

<span data-ttu-id="a324e-144">O elemento [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou **FlowMenuLayout** deve ocorrer uma vez para cada elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="a324e-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="a324e-145">Os elementos são organizados de acordo com as propriedades de quebra de linha inerentes aos atributos de *linha* e *coluna* .</span><span class="sxs-lookup"><span data-stu-id="a324e-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="a324e-146">Quando o conteúdo excede o comprimento de uma única linha, o menu quebra linhas, delimita linhas e alinha o conteúdo adequadamente.</span><span class="sxs-lookup"><span data-stu-id="a324e-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="a324e-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a324e-147">Examples</span></span>

<span data-ttu-id="a324e-148">O exemplo a seguir demonstra a marcação básica para o [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="a324e-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="a324e-149">Esta seção de código mostra a declaração de controle [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) com uma especificação **FlowMenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="a324e-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="a324e-150">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a324e-150">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a324e-151">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a324e-151">Minimum supported system</span></span><br/> | <span data-ttu-id="a324e-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a324e-152">Windows 7</span></span> |
| <span data-ttu-id="a324e-153">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a324e-153">Can be empty</span></span>                        | <span data-ttu-id="a324e-154">Sim</span><span class="sxs-lookup"><span data-stu-id="a324e-154">Yes</span></span>       |



 

 





