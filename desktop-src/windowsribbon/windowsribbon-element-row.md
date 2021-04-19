---
title: Elemento Row
description: Representa uma linha de controles em um modelo de layout SizeDefinition personalizado.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Faixa de das janelas do elemento Row
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83a0a5a9e7908cc1c8cff688b3fefc1e8910b6a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105785224"
---
# <a name="row-element"></a><span data-ttu-id="527fb-104">Elemento Row</span><span class="sxs-lookup"><span data-stu-id="527fb-104">Row element</span></span>

<span data-ttu-id="527fb-105">Representa uma linha de controles em um modelo de layout SizeDefinition personalizado.</span><span class="sxs-lookup"><span data-stu-id="527fb-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="527fb-106">Uso</span><span class="sxs-lookup"><span data-stu-id="527fb-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="527fb-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="527fb-107">Attributes</span></span>

<span data-ttu-id="527fb-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="527fb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="527fb-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="527fb-109">Child elements</span></span>



| <span data-ttu-id="527fb-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="527fb-110">Element</span></span>                                                                                 | <span data-ttu-id="527fb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="527fb-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="527fb-112">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="527fb-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="527fb-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="527fb-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="527fb-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="527fb-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="527fb-115">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="527fb-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="527fb-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="527fb-116">Parent elements</span></span>



| <span data-ttu-id="527fb-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="527fb-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="527fb-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="527fb-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="527fb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="527fb-119">Remarks</span></span>

<span data-ttu-id="527fb-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="527fb-120">Optional.</span></span>

<span data-ttu-id="527fb-121">Pode ocorrer uma ou mais vezes para cada elemento [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="527fb-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="527fb-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="527fb-122">Examples</span></span>

<span data-ttu-id="527fb-123">O exemplo de código a seguir demonstra a marcação básica para um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões com vários elementos de **linha** .</span><span class="sxs-lookup"><span data-stu-id="527fb-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="527fb-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="527fb-124">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="527fb-125">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="527fb-125">Minimum supported system</span></span><br/> | <span data-ttu-id="527fb-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="527fb-126">Windows 7</span></span> |
| <span data-ttu-id="527fb-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="527fb-127">Can be empty</span></span>                        | <span data-ttu-id="527fb-128">Não</span><span class="sxs-lookup"><span data-stu-id="527fb-128">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="527fb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="527fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527fb-130">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="527fb-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





