---
title: Propriedade Tab. ScalingPolicy
description: Representa um contêiner para as especificações de dimensionamento de tabulação.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Ribbon. ScalingPolicy da propriedade Windows
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455776"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="ac560-104">Propriedade Tab. ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="ac560-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="ac560-105">Representa um contêiner para as especificações de dimensionamento de [Tabulação](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="ac560-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="ac560-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ac560-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="ac560-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac560-107">Attributes</span></span>

<span data-ttu-id="ac560-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ac560-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ac560-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ac560-109">Child elements</span></span>



| <span data-ttu-id="ac560-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ac560-110">Element</span></span>                                                                 | <span data-ttu-id="ac560-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac560-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ac560-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="ac560-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="ac560-113">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="ac560-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ac560-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ac560-114">Parent elements</span></span>



| <span data-ttu-id="ac560-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ac560-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="ac560-116">**Tab**</span><span class="sxs-lookup"><span data-stu-id="ac560-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ac560-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac560-117">Remarks</span></span>

<span data-ttu-id="ac560-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac560-118">Optional.</span></span>

<span data-ttu-id="ac560-119">Pode ocorrer no máximo uma vez para cada [**guia**](windowsribbon-element-tab.md).</span><span class="sxs-lookup"><span data-stu-id="ac560-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="ac560-120">As especificações de dimensionamento descrevem o tamanho e o comportamento de layout dos controles em uma [guia](windowsribbon-controls-tab.md) quando a faixa de opção é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="ac560-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="ac560-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac560-121">Examples</span></span>

<span data-ttu-id="ac560-122">O exemplo de código a seguir demonstra um manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica uma preferência de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="ac560-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ac560-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac560-123">Requirements</span></span>



| <span data-ttu-id="ac560-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac560-124">Requirement</span></span> | <span data-ttu-id="ac560-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ac560-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ac560-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac560-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac560-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ac560-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ac560-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac560-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac560-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ac560-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac560-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac560-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac560-131">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="ac560-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





