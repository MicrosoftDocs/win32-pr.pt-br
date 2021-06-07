---
title: Elemento Group
description: Representa um controle Group que funciona como um contêiner para um grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Faixa de Opções do Windows do elemento group
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442867"
---
# <a name="group-element"></a><span data-ttu-id="97c99-104">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="97c99-104">Group element</span></span>

<span data-ttu-id="97c99-105">Representa um [controle](windowsribbon-controls-group.md) Group que funciona como um contêiner para um grupo de elementos.</span><span class="sxs-lookup"><span data-stu-id="97c99-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="97c99-106">Uso</span><span class="sxs-lookup"><span data-stu-id="97c99-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="97c99-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="97c99-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97c99-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="97c99-108">Attribute</span></span></th>
<th><span data-ttu-id="97c99-109">Type</span><span class="sxs-lookup"><span data-stu-id="97c99-109">Type</span></span></th>
<th><span data-ttu-id="97c99-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="97c99-110">Required</span></span></th>
<th><span data-ttu-id="97c99-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="97c99-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="97c99-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="97c99-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="97c99-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="97c99-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="97c99-114">Não</span><span class="sxs-lookup"><span data-stu-id="97c99-114">No</span></span><br/></td>
<td><span data-ttu-id="97c99-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="97c99-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="97c99-116">Uma cadeia de caracteres que contém uma lista separada por vírgulas de inteiros entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="97c99-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="97c99-117">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="97c99-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="97c99-118">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97c99-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97c99-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="97c99-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="97c99-120">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="97c99-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="97c99-121">Não</span><span class="sxs-lookup"><span data-stu-id="97c99-121">No</span></span><br/></td>
<td><span data-ttu-id="97c99-122">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="97c99-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="97c99-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="97c99-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="97c99-124">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="97c99-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="97c99-125">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="97c99-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="97c99-126">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97c99-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97c99-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="97c99-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="97c99-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="97c99-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="97c99-129">Não</span><span class="sxs-lookup"><span data-stu-id="97c99-129">No</span></span><br/></td>
<td><span data-ttu-id="97c99-130">Quando especificado, o valor de <em>SizeDefinition</em> é restrito a um dos <a href="windowsribbon-templates.md">modelos de layout definidos</a> pela estrutura ribbon.</span><span class="sxs-lookup"><span data-stu-id="97c99-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="97c99-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="97c99-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="97c99-132">Qualquer sequência de zero ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="97c99-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="97c99-133">O comprimento máximo não ébounded.</span><span class="sxs-lookup"><span data-stu-id="97c99-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="97c99-134">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="97c99-134">Child elements</span></span>



| <span data-ttu-id="97c99-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="97c99-135">Element</span></span>                                                                             | <span data-ttu-id="97c99-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="97c99-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="97c99-137">**Botão**</span><span class="sxs-lookup"><span data-stu-id="97c99-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="97c99-138">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-139">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="97c99-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="97c99-140">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="97c99-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="97c99-142">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="97c99-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="97c99-144">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="97c99-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="97c99-146">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="97c99-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="97c99-148">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="97c99-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="97c99-150">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="97c99-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="97c99-152">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="97c99-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="97c99-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="97c99-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="97c99-154">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="97c99-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="97c99-156">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="97c99-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="97c99-157">**Controle giratório**</span><span class="sxs-lookup"><span data-stu-id="97c99-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="97c99-158">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="97c99-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="97c99-160">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="97c99-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="97c99-162">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="97c99-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="97c99-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="97c99-164">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="97c99-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="97c99-165">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="97c99-165">Parent elements</span></span>



| <span data-ttu-id="97c99-166">Elemento</span><span class="sxs-lookup"><span data-stu-id="97c99-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="97c99-167">**Guia**</span><span class="sxs-lookup"><span data-stu-id="97c99-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="97c99-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="97c99-168">Remarks</span></span>

<span data-ttu-id="97c99-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="97c99-169">Optional.</span></span>

<span data-ttu-id="97c99-170">Pode ocorrer uma ou mais vezes para cada [**elemento Tab.**](windowsribbon-element-tab.md)</span><span class="sxs-lookup"><span data-stu-id="97c99-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="97c99-171">[**A guia**](windowsribbon-element-tab.md) dá suporte [aos modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="97c99-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="97c99-172">A marcação Faixa de Opções é válida somente quando os elementos filho de **Group** correspondem ao modelo especificado para *SizeDefinition.*</span><span class="sxs-lookup"><span data-stu-id="97c99-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="97c99-173">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97c99-173">Examples</span></span>

<span data-ttu-id="97c99-174">O exemplo de código a seguir ilustra o uso de um modelo personalizado em um **Grupo**.</span><span class="sxs-lookup"><span data-stu-id="97c99-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="97c99-175">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="97c99-175">Element information</span></span>

* <span data-ttu-id="97c99-176">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="97c99-176">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="97c99-177">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="97c99-177">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="97c99-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="97c99-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c99-179">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="97c99-179">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="97c99-180">Controle de grupo</span><span class="sxs-lookup"><span data-stu-id="97c99-180">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="97c99-181">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="97c99-181">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

