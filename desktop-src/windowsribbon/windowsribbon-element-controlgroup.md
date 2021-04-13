---
title: Elemento Control
description: Representa um grupo de controles em um modelo de layout SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Faixa de das janelas do elemento controlus
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365477"
---
# <a name="controlgroup-element"></a><span data-ttu-id="482cb-104">Elemento Control</span><span class="sxs-lookup"><span data-stu-id="482cb-104">ControlGroup element</span></span>

<span data-ttu-id="482cb-105">Representa um grupo de controles em um modelo de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="482cb-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="482cb-106">Uso</span><span class="sxs-lookup"><span data-stu-id="482cb-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="482cb-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="482cb-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="482cb-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="482cb-108">Attribute</span></span></th>
<th><span data-ttu-id="482cb-109">Type</span><span class="sxs-lookup"><span data-stu-id="482cb-109">Type</span></span></th>
<th><span data-ttu-id="482cb-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="482cb-110">Required</span></span></th>
<th><span data-ttu-id="482cb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="482cb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="482cb-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="482cb-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="482cb-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="482cb-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="482cb-114">Não</span><span class="sxs-lookup"><span data-stu-id="482cb-114">No</span></span><br/></td>
<td><span data-ttu-id="482cb-115">Válido somente quando o <a href="windowsribbon-element-group.md"><strong>grupo</strong></a> é o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="482cb-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="482cb-116">Cada <em>SequenceNumber</em> deve ser exclusivo dentro de um elemento de <a href="windowsribbon-element-group.md"><strong>grupo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="482cb-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="482cb-117">Os valores de <em>SequenceNumber</em> devem aumentar para cada elemento de <strong>grupo</strong> , mas não precisam ser sequenciais.</span><span class="sxs-lookup"><span data-stu-id="482cb-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="482cb-118">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="482cb-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="482cb-119">Qualquer valor inteiro positivo entre 1000 e 59999, inclusive.</span><span class="sxs-lookup"><span data-stu-id="482cb-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="482cb-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="482cb-120">Child elements</span></span>



| <span data-ttu-id="482cb-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="482cb-121">Element</span></span>                                                                                 | <span data-ttu-id="482cb-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="482cb-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="482cb-123">**Botão**</span><span class="sxs-lookup"><span data-stu-id="482cb-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="482cb-124">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-125">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="482cb-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="482cb-126">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="482cb-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="482cb-128">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="482cb-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="482cb-130">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="482cb-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="482cb-132">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="482cb-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="482cb-134">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="482cb-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="482cb-136">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="482cb-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="482cb-138">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="482cb-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="482cb-139">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="482cb-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="482cb-140">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-141">**Controle giratório**</span><span class="sxs-lookup"><span data-stu-id="482cb-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="482cb-142">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="482cb-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="482cb-144">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="482cb-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="482cb-146">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="482cb-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="482cb-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="482cb-148">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="482cb-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="482cb-149">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="482cb-149">Parent elements</span></span>



| <span data-ttu-id="482cb-150">Elemento</span><span class="sxs-lookup"><span data-stu-id="482cb-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="482cb-151">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="482cb-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="482cb-152">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="482cb-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="482cb-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="482cb-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="482cb-154">**Fila**</span><span class="sxs-lookup"><span data-stu-id="482cb-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="482cb-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="482cb-155">Remarks</span></span>

<span data-ttu-id="482cb-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="482cb-156">Optional.</span></span>

<span data-ttu-id="482cb-157">Pode ocorrer uma ou mais vezes para cada elemento [**Group**](windowsribbon-element-group.md) ou **Control** .</span><span class="sxs-lookup"><span data-stu-id="482cb-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="482cb-158">Se nenhum número de sequência for fornecido, os elementos serão renderizados na ordem especificada na marcação da faixa de lista.</span><span class="sxs-lookup"><span data-stu-id="482cb-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="482cb-159">Se [**Group ou grupo**](windowsribbon-element-group.md) de **controle** for o elemento pai, então **Control** agrupar será restrito aos seguintes elementos filho possíveis: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="482cb-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="482cb-160">Caso contrário, quando [**Row**](windowsribbon-element-row.md) ou [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) for o pai, [**Group**](windowsribbon-element-group.md) será restrito ao seguinte elemento filho possível: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="482cb-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="482cb-161">Exemplos</span><span class="sxs-lookup"><span data-stu-id="482cb-161">Examples</span></span>

<span data-ttu-id="482cb-162">O exemplo de código a seguir demonstra a marcação básica para um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões com vários elementos de [**grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="482cb-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="482cb-163">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="482cb-163">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="482cb-164">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="482cb-164">Minimum supported system</span></span><br/> | <span data-ttu-id="482cb-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="482cb-165">Windows 7</span></span> |
| <span data-ttu-id="482cb-166">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="482cb-166">Can be empty</span></span>                        | <span data-ttu-id="482cb-167">Não</span><span class="sxs-lookup"><span data-stu-id="482cb-167">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="482cb-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="482cb-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482cb-169">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="482cb-169">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





