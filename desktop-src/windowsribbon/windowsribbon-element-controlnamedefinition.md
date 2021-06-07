---
title: Elemento ControlNameDefinition
description: Representa um nome de um controle em um modelo de layout SizeDefinition personalizado.
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- Faixa de Opções do Windows do elemento ControlNameDefinition
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b2dc1db251d4d657c3793d2a66a9add1d324c37
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443437"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="04a34-104">Elemento ControlNameDefinition</span><span class="sxs-lookup"><span data-stu-id="04a34-104">ControlNameDefinition element</span></span>

<span data-ttu-id="04a34-105">Representa um nome de um controle em um modelo de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizado.</span><span class="sxs-lookup"><span data-stu-id="04a34-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="04a34-106">Uso</span><span class="sxs-lookup"><span data-stu-id="04a34-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="04a34-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="04a34-107">Attributes</span></span>



| <span data-ttu-id="04a34-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="04a34-108">Attribute</span></span>           | <span data-ttu-id="04a34-109">Type</span><span class="sxs-lookup"><span data-stu-id="04a34-109">Type</span></span>                                       | <span data-ttu-id="04a34-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="04a34-110">Required</span></span>      | <span data-ttu-id="04a34-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="04a34-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a34-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="04a34-112">**Name**</span></span><br/> | <span data-ttu-id="04a34-113">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="04a34-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="04a34-114">Não</span><span class="sxs-lookup"><span data-stu-id="04a34-114">No</span></span><br/> | <span data-ttu-id="04a34-115"><dt> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="04a34-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="04a34-116">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="04a34-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="04a34-117">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="04a34-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="04a34-118">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="04a34-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="04a34-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="04a34-119">Child elements</span></span>



| <span data-ttu-id="04a34-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="04a34-120">Element</span></span>                              | <span data-ttu-id="04a34-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="04a34-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="04a34-122">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="04a34-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="04a34-123">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="04a34-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="04a34-124">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="04a34-124">Parent elements</span></span>



| <span data-ttu-id="04a34-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="04a34-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="04a34-126">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="04a34-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="04a34-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="04a34-127">Remarks</span></span>

<span data-ttu-id="04a34-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="04a34-128">Optional.</span></span>

<span data-ttu-id="04a34-129">Pode ocorrer uma ou mais vezes para cada [**elemento ControlNameMap.**](windowsribbon-element-controlnamemap.md)</span><span class="sxs-lookup"><span data-stu-id="04a34-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="04a34-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04a34-130">Examples</span></span>

<span data-ttu-id="04a34-131">O exemplo de código a seguir demonstra a marcação básica para um modelo de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizado de quatro botões com quatro **elementos ControlNameDefinition.**</span><span class="sxs-lookup"><span data-stu-id="04a34-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="04a34-132">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="04a34-132">Element information</span></span>

* <span data-ttu-id="04a34-133">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="04a34-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="04a34-134">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="04a34-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="04a34-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="04a34-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a34-136">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="04a34-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





