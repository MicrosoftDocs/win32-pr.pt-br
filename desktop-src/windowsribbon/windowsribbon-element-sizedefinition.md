---
title: Elemento SizeDefinition
description: Representa um modelo de layout personalizado dos controles de Faixa de Opções.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Elemento SizeDefinition Da Faixa de Opções do Windows
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444797"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="30153-104">Elemento SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="30153-104">SizeDefinition element</span></span>

<span data-ttu-id="30153-105">Representa um modelo de layout personalizado dos controles de Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="30153-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="30153-106">Uso</span><span class="sxs-lookup"><span data-stu-id="30153-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="30153-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="30153-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30153-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="30153-108">Attribute</span></span></th>
<th><span data-ttu-id="30153-109">Type</span><span class="sxs-lookup"><span data-stu-id="30153-109">Type</span></span></th>
<th><span data-ttu-id="30153-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30153-110">Required</span></span></th>
<th><span data-ttu-id="30153-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="30153-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30153-112"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="30153-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="30153-113">xs:positiveInteger ou xs:string ou xs:token</span><span class="sxs-lookup"><span data-stu-id="30153-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="30153-114">Sim</span><span class="sxs-lookup"><span data-stu-id="30153-114">Yes</span></span><br/></td>
<td><span data-ttu-id="30153-115">Quando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> é o pai, caso contrário, opcional.</span><span class="sxs-lookup"><span data-stu-id="30153-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="30153-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string ou xs:token)</span><span class="sxs-lookup"><span data-stu-id="30153-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="30153-117">Uma cadeia de caracteres ou um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="30153-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="30153-118">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="30153-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="30153-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="30153-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="30153-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="30153-120">Child elements</span></span>



| <span data-ttu-id="30153-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="30153-121">Element</span></span>                                                                             | <span data-ttu-id="30153-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="30153-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="30153-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="30153-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="30153-124">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="30153-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="30153-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="30153-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="30153-126">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="30153-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="30153-127">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="30153-127">Parent elements</span></span>



| <span data-ttu-id="30153-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="30153-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30153-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="30153-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="30153-130">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="30153-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="30153-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="30153-131">Remarks</span></span>

<span data-ttu-id="30153-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="30153-132">Optional.</span></span>

<span data-ttu-id="30153-133">Pode ocorrer no máximo uma vez para cada [**elemento Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="30153-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="30153-134">Pode ocorrer uma ou mais vezes para cada [**elemento Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="30153-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="30153-135">Os modelos de layout da estrutura da Faixa de Opções Predefinidos são [especificados](windowsribbon-templates.md) com o *atributo SizeDefinition* do [**elemento Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="30153-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="30153-136">Se um elemento [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondente não for declarado para cada elemento [**Group**](windowsribbon-element-group.md) em um elemento [**Tab,**](windowsribbon-element-tab.md) ocorrerá um erro de validação.</span><span class="sxs-lookup"><span data-stu-id="30153-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="30153-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30153-137">Examples</span></span>

<span data-ttu-id="30153-138">O exemplo de código a seguir ilustra um modelo personalizado básico.</span><span class="sxs-lookup"><span data-stu-id="30153-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="30153-139">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="30153-139">Element information</span></span>


- <span data-ttu-id="30153-140">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="30153-140">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="30153-141">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="30153-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="30153-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="30153-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30153-143">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="30153-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





