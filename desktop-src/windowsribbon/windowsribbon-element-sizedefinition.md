---
title: Elemento SizeDefinition
description: Representa um modelo de layout personalizado de controles da faixa de opção.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Faixa de SizeDefinition do elemento do Windows
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bfab87f01700f8f4d36f76cbcbfe3696acfbec2
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105790559"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="1f619-104">Elemento SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="1f619-104">SizeDefinition element</span></span>

<span data-ttu-id="1f619-105">Representa um modelo de layout personalizado de controles da faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="1f619-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="1f619-106">Uso</span><span class="sxs-lookup"><span data-stu-id="1f619-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="1f619-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f619-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f619-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="1f619-108">Attribute</span></span></th>
<th><span data-ttu-id="1f619-109">Type</span><span class="sxs-lookup"><span data-stu-id="1f619-109">Type</span></span></th>
<th><span data-ttu-id="1f619-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f619-110">Required</span></span></th>
<th><span data-ttu-id="1f619-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f619-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f619-112"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="1f619-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="1f619-113">xs: positiveInteger ou xs: String ou xs: token</span><span class="sxs-lookup"><span data-stu-id="1f619-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="1f619-114">Sim</span><span class="sxs-lookup"><span data-stu-id="1f619-114">Yes</span></span><br/></td>
<td><span data-ttu-id="1f619-115">Quando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. SizeDefinitions</strong></a> for o pai, caso contrário, opcional.</span><span class="sxs-lookup"><span data-stu-id="1f619-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="1f619-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String ou xs: token)</span><span class="sxs-lookup"><span data-stu-id="1f619-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="1f619-117">Uma cadeia de caracteres ou um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="1f619-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="1f619-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="1f619-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1f619-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1f619-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1f619-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1f619-120">Child elements</span></span>



| <span data-ttu-id="1f619-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f619-121">Element</span></span>                                                                             | <span data-ttu-id="1f619-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f619-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="1f619-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="1f619-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="1f619-124">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="1f619-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="1f619-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="1f619-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="1f619-126">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="1f619-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1f619-127">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1f619-127">Parent elements</span></span>



| <span data-ttu-id="1f619-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f619-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f619-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="1f619-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="1f619-130">**Ribbon. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="1f619-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1f619-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f619-131">Remarks</span></span>

<span data-ttu-id="1f619-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1f619-132">Optional.</span></span>

<span data-ttu-id="1f619-133">Pode ocorrer no máximo uma vez para cada elemento de [**grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="1f619-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="1f619-134">Pode ocorrer uma ou mais vezes para cada elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="1f619-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="1f619-135">Os modelos de [layout](windowsribbon-templates.md) de estrutura da faixa de opção predefinidos são especificados com o atributo *SizeDefinition* do elemento [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="1f619-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="1f619-136">Se um elemento [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondente não for declarado para cada elemento de [**grupo**](windowsribbon-element-group.md) em um elemento de [**guia**](windowsribbon-element-tab.md) , ocorrerá um erro de validação.</span><span class="sxs-lookup"><span data-stu-id="1f619-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="1f619-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f619-137">Examples</span></span>

<span data-ttu-id="1f619-138">O exemplo de código a seguir ilustra um modelo personalizado básico.</span><span class="sxs-lookup"><span data-stu-id="1f619-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1f619-139">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1f619-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="1f619-140">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f619-140">Minimum supported system</span></span><br/> | <span data-ttu-id="1f619-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f619-141">Windows 7</span></span> |
| <span data-ttu-id="1f619-142">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="1f619-142">Can be empty</span></span>                        | <span data-ttu-id="1f619-143">Não</span><span class="sxs-lookup"><span data-stu-id="1f619-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="1f619-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f619-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f619-145">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="1f619-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





