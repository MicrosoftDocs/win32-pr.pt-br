---
title: Propriedade ScalingPolicy. IdealSizes
description: Representa um contêiner de especificações de escala para o modelo de SizeDefinition preferencial, com base no tamanho da faixa de medida.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Faixa de ScalingPolicy de propriedades do Windows. IdealSizes
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105793204"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="b807c-104">Propriedade ScalingPolicy. IdealSizes</span><span class="sxs-lookup"><span data-stu-id="b807c-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="b807c-105">Representa um contêiner de especificações de escala para o modelo de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferencial, com base no tamanho da faixa de medida.</span><span class="sxs-lookup"><span data-stu-id="b807c-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="b807c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="b807c-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="b807c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b807c-107">Attributes</span></span>

<span data-ttu-id="b807c-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="b807c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b807c-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b807c-109">Child elements</span></span>



| <span data-ttu-id="b807c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b807c-110">Element</span></span>                                                 | <span data-ttu-id="b807c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b807c-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b807c-112">**Escalonáve**</span><span class="sxs-lookup"><span data-stu-id="b807c-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="b807c-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="b807c-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b807c-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b807c-114">Parent elements</span></span>



| <span data-ttu-id="b807c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="b807c-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="b807c-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="b807c-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b807c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b807c-117">Remarks</span></span>

<span data-ttu-id="b807c-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b807c-118">Optional.</span></span>

<span data-ttu-id="b807c-119">Pode ocorrer no máximo uma vez para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b807c-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="b807c-120">Se **ScalingPolicy. IdealSizes** for definido, uma entrada de [**escala**](windowsribbon-element-scale.md) para cada elemento de [**grupo**](windowsribbon-element-group.md) em um elemento de [**guia**](windowsribbon-element-tab.md) deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="b807c-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="b807c-121">**ScalingPolicy. IdealSizes** são os layouts de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferenciais para um [**grupo**](windowsribbon-element-group.md) de controles.</span><span class="sxs-lookup"><span data-stu-id="b807c-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="b807c-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b807c-122">Examples</span></span>

<span data-ttu-id="b807c-123">O exemplo a seguir demonstra como a aparência de controles em um [**grupo**](windowsribbon-element-group.md) pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos de faixa de opções [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="b807c-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="b807c-124">O manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) neste exemplo especifica uma preferência de **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="b807c-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="b807c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b807c-125">Requirements</span></span>



| <span data-ttu-id="b807c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b807c-126">Requirement</span></span> | <span data-ttu-id="b807c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b807c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b807c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b807c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b807c-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b807c-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b807c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b807c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b807c-131">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b807c-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b807c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b807c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b807c-133">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="b807c-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





