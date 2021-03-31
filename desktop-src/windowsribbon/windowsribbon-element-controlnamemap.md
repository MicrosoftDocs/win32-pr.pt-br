---
title: Elemento ControlNameMap
description: Representa um contêiner para nomes de controle em um modelo de layout de SizeDefinition personalizado.
ms.assetid: b4bceb90-a9a3-42d7-a85b-bf6e4e02784b
keywords:
- Faixa de ControlNameMap do elemento do Windows
topic_type:
- apiref
api_name:
- ControlNameMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ca5338978be7f9ddf3432cbe1a0fb8d243d8c00
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823269"
---
# <a name="controlnamemap-element"></a><span data-ttu-id="19234-104">Elemento ControlNameMap</span><span class="sxs-lookup"><span data-stu-id="19234-104">ControlNameMap element</span></span>

<span data-ttu-id="19234-105">Representa um contêiner para nomes de controle em um modelo de layout de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizado.</span><span class="sxs-lookup"><span data-stu-id="19234-105">Represents a container for control names in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="19234-106">Uso</span><span class="sxs-lookup"><span data-stu-id="19234-106">Usage</span></span>

``` syntax
<ControlNameMap>
  child elements
</ControlNameMap>
```

## <a name="attributes"></a><span data-ttu-id="19234-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="19234-107">Attributes</span></span>

<span data-ttu-id="19234-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="19234-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="19234-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="19234-109">Child elements</span></span>



| <span data-ttu-id="19234-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="19234-110">Element</span></span>                                                                                 | <span data-ttu-id="19234-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="19234-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="19234-112">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="19234-112">**ControlNameDefinition**</span></span>](windowsribbon-element-controlnamedefinition.md)<br/> | <span data-ttu-id="19234-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="19234-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="19234-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="19234-114">Parent elements</span></span>



| <span data-ttu-id="19234-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="19234-115">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="19234-116">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="19234-116">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="19234-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="19234-117">Remarks</span></span>

<span data-ttu-id="19234-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19234-118">Optional.</span></span>

<span data-ttu-id="19234-119">Pode ocorrer no máximo uma vez para cada elemento [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="19234-119">May occur at most once for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="19234-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19234-120">Examples</span></span>

<span data-ttu-id="19234-121">O exemplo de código a seguir demonstra a marcação básica para um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões com um elemento **ControlNameMap** .</span><span class="sxs-lookup"><span data-stu-id="19234-121">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with a **ControlNameMap** element.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="19234-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="19234-122">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="19234-123">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19234-123">Minimum supported system</span></span><br/> | <span data-ttu-id="19234-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19234-124">Windows 7</span></span> |
| <span data-ttu-id="19234-125">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="19234-125">Can be empty</span></span>                        | <span data-ttu-id="19234-126">Não</span><span class="sxs-lookup"><span data-stu-id="19234-126">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="19234-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="19234-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19234-128">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="19234-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





