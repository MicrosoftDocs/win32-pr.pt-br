---
title: Elemento ScalingPolicy
description: Representa um contêiner para especificações de dimensionamento.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Faixa de ScalingPolicy do elemento do Windows
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f0d0f484ebded1233e3c64f6c7830882395b90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638669"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="0af85-104">Elemento ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="0af85-104">ScalingPolicy element</span></span>

<span data-ttu-id="0af85-105">Representa um contêiner para especificações de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="0af85-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="0af85-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0af85-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="0af85-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0af85-107">Attributes</span></span>

<span data-ttu-id="0af85-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="0af85-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0af85-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0af85-109">Child elements</span></span>



| <span data-ttu-id="0af85-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="0af85-110">Element</span></span>                                                                                       | <span data-ttu-id="0af85-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0af85-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0af85-112">**Escala**</span><span class="sxs-lookup"><span data-stu-id="0af85-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="0af85-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="0af85-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0af85-114">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="0af85-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="0af85-115">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="0af85-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="0af85-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0af85-116">Parent elements</span></span>



| <span data-ttu-id="0af85-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0af85-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="0af85-118">**Guia. ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="0af85-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0af85-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0af85-119">Remarks</span></span>

<span data-ttu-id="0af85-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0af85-120">Required.</span></span>

<span data-ttu-id="0af85-121">Deve ocorrer uma vez para cada [**guia. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="0af85-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="0af85-122">O elemento **ScalingPolicy** contém um manifesto de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e declarações de [**escala**](windowsribbon-element-scale.md) que especificam preferências de layout adaptável para um ou mais elementos de [**grupo**](windowsribbon-element-group.md) quando a faixa de opções é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="0af85-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="0af85-123">A lista de declarações de [**escala**](windowsribbon-element-scale.md) deve estar em ordem decrescente de tamanhos válidos (Large, Medium, Small, popup) para o [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associado ao elemento [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="0af85-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="0af85-124">É altamente recomendável que a escala de detalhes da política de dimensionamento adequada seja especificada de modo que uma faixa de bits possa ser renderizada sem barras de rolagem quando redimensionada para uma largura de 300 pixels a 96 pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="0af85-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="0af85-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0af85-125">Examples</span></span>

<span data-ttu-id="0af85-126">O exemplo a seguir demonstra como a aparência de controles em um [**grupo**](windowsribbon-element-group.md) pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos de faixa de opções [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="0af85-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="0af85-127">O manifesto **ScalingPolicy** neste exemplo especifica uma preferência de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="0af85-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0af85-128">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0af85-128">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="0af85-129">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0af85-129">Minimum supported system</span></span><br/> | <span data-ttu-id="0af85-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0af85-130">Windows 7</span></span> |
| <span data-ttu-id="0af85-131">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="0af85-131">Can be empty</span></span>                        | <span data-ttu-id="0af85-132">Não</span><span class="sxs-lookup"><span data-stu-id="0af85-132">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="0af85-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0af85-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af85-134">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="0af85-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





