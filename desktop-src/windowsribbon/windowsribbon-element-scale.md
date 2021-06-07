---
title: Elemento Scale
description: Representa o tamanho e a preferência de layout de um Grupo de controles por meio de um par Group, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Faixa de opções do Windows do elemento Scale
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445007"
---
# <a name="scale-element"></a><span data-ttu-id="c3911-104">Elemento Scale</span><span class="sxs-lookup"><span data-stu-id="c3911-104">Scale element</span></span>

<span data-ttu-id="c3911-105">Representa o tamanho e a preferência de layout de um [**Grupo**](windowsribbon-element-group.md) de controles por meio de um par {**Grupo**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.</span><span class="sxs-lookup"><span data-stu-id="c3911-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="c3911-106">Uso</span><span class="sxs-lookup"><span data-stu-id="c3911-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="c3911-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3911-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3911-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="c3911-108">Attribute</span></span></th>
<th><span data-ttu-id="c3911-109">Type</span><span class="sxs-lookup"><span data-stu-id="c3911-109">Type</span></span></th>
<th><span data-ttu-id="c3911-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c3911-110">Required</span></span></th>
<th><span data-ttu-id="c3911-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3911-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c3911-112"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="c3911-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="c3911-113">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="c3911-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c3911-114">Sim</span><span class="sxs-lookup"><span data-stu-id="c3911-114">Yes</span></span><br/></td>
<td><span data-ttu-id="c3911-115">Deve corresponder a um <em>CommandName de Grupo existente.</em> <a href="windowsribbon-element-group.md"><strong></strong></a></span><span class="sxs-lookup"><span data-stu-id="c3911-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="c3911-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="c3911-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c3911-117">Uma cadeia de caracteres ou um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="c3911-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="c3911-118">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="c3911-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c3911-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3911-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3911-120"><strong>Tamanho</strong></span><span class="sxs-lookup"><span data-stu-id="c3911-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="c3911-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="c3911-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="c3911-122">Sim</span><span class="sxs-lookup"><span data-stu-id="c3911-122">Yes</span></span><br/></td>
<td><span data-ttu-id="c3911-123">Esse valor deve corresponder a um dos tamanhos válidos para <a href="windowsribbon-element-group.md"><strong></strong></a> o atributo <em>SizeDefinition</em> do Grupo de controles associado especificado no <em>Grupo</em>.</span><span class="sxs-lookup"><span data-stu-id="c3911-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="c3911-124">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3911-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="c3911-125">
<dt><span></span><span></span><strong></strong> (Pop-up)</span><span class="sxs-lookup"><span data-stu-id="c3911-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="c3911-126">Layout de controle idêntico <code>Large</code> para , mas hospedado em um pop-up ou em um painel de lista.</span><span class="sxs-lookup"><span data-stu-id="c3911-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="c3911-127"><dt><span></span><span></span><strong></strong> (Pequeno)</span><span class="sxs-lookup"><span data-stu-id="c3911-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="c3911-128">Modelo <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeno.</span><span class="sxs-lookup"><span data-stu-id="c3911-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="c3911-129"><dt><span></span><span></span><strong></strong> (Médio)</span><span class="sxs-lookup"><span data-stu-id="c3911-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="c3911-130">Modelo <a href="windowsribbon-element-sizedefinition.md"><strong>Medium SizeDefinition.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c3911-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="c3911-131"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="c3911-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="c3911-132">Modelo <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.</span><span class="sxs-lookup"><span data-stu-id="c3911-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c3911-133">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c3911-133">Child elements</span></span>

<span data-ttu-id="c3911-134">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="c3911-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c3911-135">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c3911-135">Parent elements</span></span>



| <span data-ttu-id="c3911-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3911-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3911-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="c3911-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="c3911-138">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="c3911-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c3911-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3911-139">Remarks</span></span>

<span data-ttu-id="c3911-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c3911-140">Optional.</span></span>

<span data-ttu-id="c3911-141">Pode ocorrer uma ou mais vezes para [**cada ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ou [**ScalingPolicy.IdealSizes.**](windowsribbon-element-scalingpolicy-idealsizes.md)</span><span class="sxs-lookup"><span data-stu-id="c3911-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="c3911-142">Cada par de atributos (*Grupo* *,* Tamanho ) deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c3911-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="c3911-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3911-143">Examples</span></span>

<span data-ttu-id="c3911-144">O exemplo a seguir demonstra como [**a**](windowsribbon-element-group.md) aparência dos controles em um grupo pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos Ribbon [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="c3911-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="c3911-145">O [**manifesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) neste exemplo especifica uma preferência [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma **guia** Início. Além disso, **os elementos Scale** são especificados para influenciar o comportamento de ressução, em ordem de tamanho decrescente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="c3911-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="c3911-146">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c3911-146">Element information</span></span>



* <span data-ttu-id="c3911-147">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3911-147">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="c3911-148">**Pode estar vazio:** Sim</span><span class="sxs-lookup"><span data-stu-id="c3911-148">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="c3911-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3911-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3911-150">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="c3911-150">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





