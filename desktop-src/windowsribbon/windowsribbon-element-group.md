---
title: Elemento Group
description: Representa um controle de grupo que funciona como um contêiner para um grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Faixa de das janelas do elemento de grupo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366339"
---
# <a name="group-element"></a><span data-ttu-id="bf311-104">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="bf311-104">Group element</span></span>

<span data-ttu-id="bf311-105">Representa um controle de [grupo](windowsribbon-controls-group.md) que funciona como um contêiner para um grupo de elementos.</span><span class="sxs-lookup"><span data-stu-id="bf311-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="bf311-106">Uso</span><span class="sxs-lookup"><span data-stu-id="bf311-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="bf311-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf311-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf311-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="bf311-108">Attribute</span></span></th>
<th><span data-ttu-id="bf311-109">Type</span><span class="sxs-lookup"><span data-stu-id="bf311-109">Type</span></span></th>
<th><span data-ttu-id="bf311-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bf311-110">Required</span></span></th>
<th><span data-ttu-id="bf311-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf311-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf311-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="bf311-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="bf311-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="bf311-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="bf311-114">Não</span><span class="sxs-lookup"><span data-stu-id="bf311-114">No</span></span><br/></td>
<td><span data-ttu-id="bf311-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="bf311-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bf311-116">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="bf311-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="bf311-117">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="bf311-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="bf311-118">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bf311-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf311-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="bf311-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="bf311-120">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="bf311-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="bf311-121">Não</span><span class="sxs-lookup"><span data-stu-id="bf311-121">No</span></span><br/></td>
<td><span data-ttu-id="bf311-122">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bf311-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="bf311-123">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="bf311-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bf311-124">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="bf311-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="bf311-125">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="bf311-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="bf311-126">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bf311-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf311-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="bf311-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="bf311-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="bf311-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="bf311-129">Não</span><span class="sxs-lookup"><span data-stu-id="bf311-129">No</span></span><br/></td>
<td><span data-ttu-id="bf311-130">Quando especificado, o valor de <em>SizeDefinition</em> é restrito a um dos <a href="windowsribbon-templates.md">modelos de layout</a> definidos pela estrutura da faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="bf311-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="bf311-131">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="bf311-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bf311-132">Qualquer sequência de zero ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="bf311-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="bf311-133">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="bf311-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="bf311-134">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bf311-134">Child elements</span></span>



| <span data-ttu-id="bf311-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf311-135">Element</span></span>                                                                             | <span data-ttu-id="bf311-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf311-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bf311-137">**Botão**</span><span class="sxs-lookup"><span data-stu-id="bf311-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="bf311-138">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-139">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="bf311-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="bf311-140">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="bf311-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="bf311-142">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-143">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="bf311-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="bf311-144">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="bf311-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="bf311-146">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="bf311-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="bf311-148">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="bf311-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="bf311-150">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="bf311-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="bf311-152">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="bf311-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="bf311-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="bf311-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="bf311-154">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="bf311-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="bf311-156">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="bf311-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="bf311-157">**Controle giratório**</span><span class="sxs-lookup"><span data-stu-id="bf311-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="bf311-158">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="bf311-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="bf311-160">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="bf311-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="bf311-162">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf311-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="bf311-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="bf311-164">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bf311-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bf311-165">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bf311-165">Parent elements</span></span>



| <span data-ttu-id="bf311-166">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf311-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="bf311-167">**Tab**</span><span class="sxs-lookup"><span data-stu-id="bf311-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bf311-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf311-168">Remarks</span></span>

<span data-ttu-id="bf311-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bf311-169">Optional.</span></span>

<span data-ttu-id="bf311-170">Pode ocorrer uma ou mais vezes para cada elemento de [**guia**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="bf311-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="bf311-171">[**Guia**](windowsribbon-element-tab.md) dá suporte a [modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="bf311-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="bf311-172">A marcação da faixa de faixas é válida somente quando os elementos filho do **grupo** correspondem ao modelo especificado para *SizeDefinition*.</span><span class="sxs-lookup"><span data-stu-id="bf311-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="bf311-173">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bf311-173">Examples</span></span>

<span data-ttu-id="bf311-174">O exemplo de código a seguir ilustra o uso de um modelo personalizado em um **grupo**.</span><span class="sxs-lookup"><span data-stu-id="bf311-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="bf311-175">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bf311-175">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="bf311-176">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf311-176">Minimum supported system</span></span><br/> | <span data-ttu-id="bf311-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf311-177">Windows 7</span></span> |
| <span data-ttu-id="bf311-178">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="bf311-178">Can be empty</span></span>                        | <span data-ttu-id="bf311-179">Não</span><span class="sxs-lookup"><span data-stu-id="bf311-179">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="bf311-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf311-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf311-181">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="bf311-181">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="bf311-182">Controle de grupo</span><span class="sxs-lookup"><span data-stu-id="bf311-182">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="bf311-183">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="bf311-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

