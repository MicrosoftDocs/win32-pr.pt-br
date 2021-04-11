---
title: Elemento ControlSizeDefinition
description: Representa o estilo de layout de um grupo de controles em um modelo personalizado.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Faixa de ControlSizeDefinition do elemento do Windows
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293233"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="602f5-104">Elemento ControlSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="602f5-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="602f5-105">Representa o estilo de layout de um grupo de controles em um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="602f5-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="602f5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="602f5-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="602f5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="602f5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="602f5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="602f5-108">Attribute</span></span></th>
<th><span data-ttu-id="602f5-109">Type</span><span class="sxs-lookup"><span data-stu-id="602f5-109">Type</span></span></th>
<th><span data-ttu-id="602f5-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="602f5-110">Required</span></span></th>
<th><span data-ttu-id="602f5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="602f5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="602f5-112"><strong>Controle de origem</strong></span><span class="sxs-lookup"><span data-stu-id="602f5-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="602f5-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="602f5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="602f5-114">Não</span><span class="sxs-lookup"><span data-stu-id="602f5-114">No</span></span><br/></td>
<td><span data-ttu-id="602f5-115"><dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="602f5-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="602f5-116">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="602f5-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="602f5-117">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="602f5-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="602f5-118">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="602f5-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="602f5-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="602f5-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="602f5-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="602f5-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="602f5-121">Não</span><span class="sxs-lookup"><span data-stu-id="602f5-121">No</span></span><br/></td>
<td><span data-ttu-id="602f5-122">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="602f5-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="602f5-123">
<dt><span></span><span></span><strong></strong> Vários</span><span class="sxs-lookup"><span data-stu-id="602f5-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="602f5-124"><dt><span></span><span></span><strong></strong> Menores</span><span class="sxs-lookup"><span data-stu-id="602f5-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="602f5-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="602f5-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="602f5-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="602f5-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="602f5-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="602f5-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="602f5-128">Não</span><span class="sxs-lookup"><span data-stu-id="602f5-128">No</span></span><br/></td>
<td><span data-ttu-id="602f5-129">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="602f5-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="602f5-130">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="602f5-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="602f5-131">Padrão.</span><span class="sxs-lookup"><span data-stu-id="602f5-131">Default.</span></span> <br/> </dd> <span data-ttu-id="602f5-132"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="602f5-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="602f5-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="602f5-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="602f5-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="602f5-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="602f5-135">Não</span><span class="sxs-lookup"><span data-stu-id="602f5-135">No</span></span><br/></td>
<td><span data-ttu-id="602f5-136">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="602f5-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="602f5-137">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="602f5-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="602f5-138">Padrão.</span><span class="sxs-lookup"><span data-stu-id="602f5-138">Default.</span></span> <br/> </dd> <span data-ttu-id="602f5-139"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="602f5-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="602f5-140"><strong>Ispopup</strong></span><span class="sxs-lookup"><span data-stu-id="602f5-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="602f5-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="602f5-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="602f5-142">Não</span><span class="sxs-lookup"><span data-stu-id="602f5-142">No</span></span><br/></td>
<td><span data-ttu-id="602f5-143">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="602f5-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="602f5-144">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="602f5-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="602f5-145"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="602f5-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="602f5-146">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="602f5-146">Child elements</span></span>

<span data-ttu-id="602f5-147">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="602f5-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="602f5-148">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="602f5-148">Parent elements</span></span>



| <span data-ttu-id="602f5-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="602f5-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="602f5-150">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="602f5-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="602f5-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="602f5-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="602f5-152">**Fila**</span><span class="sxs-lookup"><span data-stu-id="602f5-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="602f5-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="602f5-153">Remarks</span></span>

<span data-ttu-id="602f5-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="602f5-154">Optional.</span></span>

<span data-ttu-id="602f5-155">Pode ocorrer uma ou mais vezes para cada elemento de [**controle**](windowsribbon-element-controlgroup.md), [**linha**](windowsribbon-element-row.md)ou [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="602f5-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="602f5-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="602f5-156">Examples</span></span>

<span data-ttu-id="602f5-157">O exemplo de código a seguir demonstra a marcação básica para um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões com vários elementos **ControlSizeDefinition** .</span><span class="sxs-lookup"><span data-stu-id="602f5-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="602f5-158">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="602f5-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="602f5-159">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="602f5-159">Minimum supported system</span></span><br/> | <span data-ttu-id="602f5-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="602f5-160">Windows 7</span></span> |
| <span data-ttu-id="602f5-161">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="602f5-161">Can be empty</span></span>                        | <span data-ttu-id="602f5-162">Sim</span><span class="sxs-lookup"><span data-stu-id="602f5-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="602f5-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="602f5-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602f5-164">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="602f5-164">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





