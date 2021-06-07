---
title: Elemento ControlSizeDefinition
description: Representa o estilo de layout de um grupo de controles em um modelo personalizado.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Faixa de Opções do Windows do elemento ControlSizeDefinition
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff5217c08b4ea6da1931b0c65501f912f2cc5dc
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443407"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="6b239-104">Elemento ControlSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="6b239-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="6b239-105">Representa o estilo de layout de um grupo de controles em um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b239-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="6b239-106">Uso</span><span class="sxs-lookup"><span data-stu-id="6b239-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="6b239-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b239-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b239-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="6b239-108">Attribute</span></span></th>
<th><span data-ttu-id="6b239-109">Type</span><span class="sxs-lookup"><span data-stu-id="6b239-109">Type</span></span></th>
<th><span data-ttu-id="6b239-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6b239-110">Required</span></span></th>
<th><span data-ttu-id="6b239-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b239-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b239-112"><strong>Controlname</strong></span><span class="sxs-lookup"><span data-stu-id="6b239-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="6b239-113">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="6b239-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6b239-114">Não</span><span class="sxs-lookup"><span data-stu-id="6b239-114">No</span></span><br/></td>
<td><span data-ttu-id="6b239-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="6b239-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6b239-116">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="6b239-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6b239-117">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="6b239-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6b239-118">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b239-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b239-119"><strong>Imagesize</strong></span><span class="sxs-lookup"><span data-stu-id="6b239-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="6b239-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b239-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="6b239-121">Não</span><span class="sxs-lookup"><span data-stu-id="6b239-121">No</span></span><br/></td>
<td><span data-ttu-id="6b239-122">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6b239-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="6b239-123">
<dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="6b239-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6b239-124"><dt><span></span><span></span><strong></strong> (Pequeno)</span><span class="sxs-lookup"><span data-stu-id="6b239-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="6b239-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="6b239-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b239-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="6b239-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="6b239-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="6b239-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="6b239-128">Não</span><span class="sxs-lookup"><span data-stu-id="6b239-128">No</span></span><br/></td>
<td><span data-ttu-id="6b239-129">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="6b239-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="6b239-130">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="6b239-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="6b239-131">Padrão.</span><span class="sxs-lookup"><span data-stu-id="6b239-131">Default.</span></span> <br/> </dd> <span data-ttu-id="6b239-132"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="6b239-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b239-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="6b239-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="6b239-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="6b239-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="6b239-135">Não</span><span class="sxs-lookup"><span data-stu-id="6b239-135">No</span></span><br/></td>
<td><span data-ttu-id="6b239-136">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="6b239-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="6b239-137">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="6b239-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="6b239-138">Padrão.</span><span class="sxs-lookup"><span data-stu-id="6b239-138">Default.</span></span> <br/> </dd> <span data-ttu-id="6b239-139"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="6b239-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b239-140"><strong>IsPopup</strong></span><span class="sxs-lookup"><span data-stu-id="6b239-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="6b239-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="6b239-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="6b239-142">Não</span><span class="sxs-lookup"><span data-stu-id="6b239-142">No</span></span><br/></td>
<td><span data-ttu-id="6b239-143">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="6b239-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="6b239-144">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="6b239-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="6b239-145"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="6b239-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6b239-146">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6b239-146">Child elements</span></span>

<span data-ttu-id="6b239-147">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="6b239-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6b239-148">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6b239-148">Parent elements</span></span>



| <span data-ttu-id="6b239-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="6b239-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b239-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="6b239-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="6b239-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="6b239-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="6b239-152">**Linha**</span><span class="sxs-lookup"><span data-stu-id="6b239-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="6b239-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b239-153">Remarks</span></span>

<span data-ttu-id="6b239-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6b239-154">Optional.</span></span>

<span data-ttu-id="6b239-155">Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup,**](windowsribbon-element-controlgroup.md) [**Row**](windowsribbon-element-row.md)ou [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="6b239-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="6b239-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b239-156">Examples</span></span>

<span data-ttu-id="6b239-157">O exemplo de código a seguir demonstra a marcação básica para um modelo de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizado de quatro botões com vários **elementos ControlSizeDefinition.**</span><span class="sxs-lookup"><span data-stu-id="6b239-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="6b239-158">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6b239-158">Element information</span></span>

* <span data-ttu-id="6b239-159">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b239-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="6b239-160">**Pode estar vazio:** Sim</span><span class="sxs-lookup"><span data-stu-id="6b239-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="6b239-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b239-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b239-162">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="6b239-162">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





