---
title: Elemento de menu
description: Representa um contêiner de controles a serem exibidos em uma galeria, um menu ou uma barra de ferramentas.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Faixa de das janelas de elemento de menu do Windows
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103639719"
---
# <a name="menugroup-element"></a><span data-ttu-id="d022a-104">Elemento de menu</span><span class="sxs-lookup"><span data-stu-id="d022a-104">MenuGroup element</span></span>

<span data-ttu-id="d022a-105">Representa um contêiner de controles a serem exibidos em uma galeria, um menu ou uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d022a-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="d022a-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d022a-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="d022a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d022a-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d022a-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="d022a-108">Attribute</span></span></th>
<th><span data-ttu-id="d022a-109">Type</span><span class="sxs-lookup"><span data-stu-id="d022a-109">Type</span></span></th>
<th><span data-ttu-id="d022a-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d022a-110">Required</span></span></th>
<th><span data-ttu-id="d022a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d022a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d022a-112"><strong>Classe</strong></span><span class="sxs-lookup"><span data-stu-id="d022a-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="d022a-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d022a-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d022a-114">Não</span><span class="sxs-lookup"><span data-stu-id="d022a-114">No</span></span><br/></td>
<td><span data-ttu-id="d022a-115">Especifica o tamanho e o estilo de layout dos elementos na interface do usuário do menu.</span><span class="sxs-lookup"><span data-stu-id="d022a-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="d022a-116">Um recurso de imagem pode ser fornecido em dois tamanhos (grandes e pequenos) e associado ao elemento na marcação usando os elementos de propriedade <a href="windowsribbon-element-command-largeimages.md"><strong>Command. LargeImages</strong></a> e <a href="windowsribbon-element-command-smallimages.md"><strong>Command. SmallImages</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d022a-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="d022a-117">Se apenas uma imagem for fornecida, a estrutura a redimensionará conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d022a-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="d022a-118">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d022a-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d022a-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span><span class="sxs-lookup"><span data-stu-id="d022a-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="d022a-120">Padrão.</span><span class="sxs-lookup"><span data-stu-id="d022a-120">Default.</span></span> <br/> <span data-ttu-id="d022a-121">Estilo: imagem pequena e texto de realçado.</span><span class="sxs-lookup"><span data-stu-id="d022a-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="d022a-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span><span class="sxs-lookup"><span data-stu-id="d022a-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="d022a-123">Estilo: imagem grande e texto em negrito.</span><span class="sxs-lookup"><span data-stu-id="d022a-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d022a-124">Se o <strong>menu de menus</strong> for filho de <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, o atributo de <em>classe</em> será ignorado e um estilo de <code>MajorItems</code> será imposto pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="d022a-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d022a-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d022a-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d022a-126">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="d022a-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d022a-127">Não</span><span class="sxs-lookup"><span data-stu-id="d022a-127">No</span></span><br/></td>
<td><span data-ttu-id="d022a-128">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d022a-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d022a-129">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="d022a-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d022a-130">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="d022a-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d022a-131">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d022a-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d022a-132">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d022a-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d022a-133">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d022a-133">Child elements</span></span>



| <span data-ttu-id="d022a-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="d022a-134">Element</span></span>                                                                             | <span data-ttu-id="d022a-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="d022a-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d022a-136">**Botão**</span><span class="sxs-lookup"><span data-stu-id="d022a-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="d022a-137">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-138">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="d022a-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="d022a-139">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="d022a-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="d022a-141">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d022a-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="d022a-143">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-144">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="d022a-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="d022a-145">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-146">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d022a-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="d022a-147">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-148">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="d022a-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="d022a-149">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="d022a-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="d022a-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d022a-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="d022a-151">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-152">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d022a-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="d022a-153">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d022a-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="d022a-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="d022a-155">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="d022a-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d022a-156">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d022a-156">Parent elements</span></span>



| <span data-ttu-id="d022a-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="d022a-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d022a-158">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="d022a-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="d022a-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="d022a-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="d022a-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d022a-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="d022a-161">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="d022a-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="d022a-162">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="d022a-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="d022a-163">**Minibarra**</span><span class="sxs-lookup"><span data-stu-id="d022a-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="d022a-164">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="d022a-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="d022a-165">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="d022a-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d022a-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="d022a-166">Remarks</span></span>

<span data-ttu-id="d022a-167">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d022a-167">Required.</span></span>

<span data-ttu-id="d022a-168">Deve ocorrer pelo menos uma vez para cada [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**Minibarra**](windowsribbon-element-minitoolbar.md)ou [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="d022a-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="d022a-169">Se [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) for o elemento pai, o **menu de menus** será restrito aos seguintes elementos filho: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="d022a-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="d022a-170">Se [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)ou [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) for o elemento pai, o **menu de menus** será restrito aos seguintes elementos filho: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="d022a-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="d022a-171">Se [**Minibarra**](windowsribbon-element-minitoolbar.md) for o elemento pai, o **menu de menus** será restrito aos seguintes elementos filho: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="d022a-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="d022a-172">O atributo de classe não é necessário quando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) é o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="d022a-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="d022a-173">A estrutura impõe um valor de MajorItems para o atributo de classe.</span><span class="sxs-lookup"><span data-stu-id="d022a-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="d022a-174">Quando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) é o elemento pai, o atributo de classe não é necessário.</span><span class="sxs-lookup"><span data-stu-id="d022a-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="d022a-175">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d022a-175">Examples</span></span>

<span data-ttu-id="d022a-176">O exemplo a seguir demonstra a marcação básica para o [**SplitButton**](windowsribbon-element-splitbutton.md) com um elemento de **menu** .</span><span class="sxs-lookup"><span data-stu-id="d022a-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="d022a-177">Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e de **menu de menus** com um recurso de imagem grande e um pequeno.</span><span class="sxs-lookup"><span data-stu-id="d022a-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="d022a-178">Um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai do elemento **SplitButton** também é declarado.</span><span class="sxs-lookup"><span data-stu-id="d022a-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="d022a-179">Esta seção de código mostra as declarações de controle [**SplitButton**](windowsribbon-element-splitbutton.md) e de **menu de menus** com `StandardItems` and `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="d022a-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="d022a-180">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d022a-180">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d022a-181">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d022a-181">Minimum supported system</span></span><br/> | <span data-ttu-id="d022a-182">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d022a-182">Windows 7</span></span> |
| <span data-ttu-id="d022a-183">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="d022a-183">Can be empty</span></span>                        | <span data-ttu-id="d022a-184">Não</span><span class="sxs-lookup"><span data-stu-id="d022a-184">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="d022a-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="d022a-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d022a-186">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="d022a-186">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="d022a-187">Grupo de menus</span><span class="sxs-lookup"><span data-stu-id="d022a-187">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





