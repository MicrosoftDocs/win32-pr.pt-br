---
title: Elemento ColumnBreak
description: Representa um separador vertical (visível ou oculto) em modelos de layout SizeDefinition personalizados.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Faixa de ColumnBreak do elemento do Windows
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5bff1682cdf55b44092a176abd6dc7e935220a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444837"
---
# <a name="columnbreak-element"></a><span data-ttu-id="2994e-104">Elemento ColumnBreak</span><span class="sxs-lookup"><span data-stu-id="2994e-104">ColumnBreak element</span></span>

<span data-ttu-id="2994e-105">Representa um separador vertical (visível ou oculto) em modelos de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizados.</span><span class="sxs-lookup"><span data-stu-id="2994e-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="2994e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2994e-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="2994e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2994e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2994e-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="2994e-108">Attribute</span></span></th>
<th><span data-ttu-id="2994e-109">Type</span><span class="sxs-lookup"><span data-stu-id="2994e-109">Type</span></span></th>
<th><span data-ttu-id="2994e-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2994e-110">Required</span></span></th>
<th><span data-ttu-id="2994e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2994e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2994e-112"><strong>Separador</strong></span><span class="sxs-lookup"><span data-stu-id="2994e-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="2994e-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="2994e-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="2994e-114">Não</span><span class="sxs-lookup"><span data-stu-id="2994e-114">No</span></span><br/></td>
<td><span data-ttu-id="2994e-115">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2994e-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2994e-116">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="2994e-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2994e-117">Padrão.</span><span class="sxs-lookup"><span data-stu-id="2994e-117">Default.</span></span> <br/> </dd> <span data-ttu-id="2994e-118"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="2994e-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2994e-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2994e-119">Child elements</span></span>

<span data-ttu-id="2994e-120">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="2994e-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2994e-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2994e-121">Parent elements</span></span>



| <span data-ttu-id="2994e-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="2994e-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="2994e-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2994e-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2994e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2994e-124">Remarks</span></span>

<span data-ttu-id="2994e-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2994e-125">Optional.</span></span>

<span data-ttu-id="2994e-126">Pode ocorrer uma ou mais vezes para cada elemento [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2994e-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2994e-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2994e-127">Examples</span></span>

<span data-ttu-id="2994e-128">O exemplo a seguir demonstra a marcação básica para um elemento **ColumnBreak** em um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões.</span><span class="sxs-lookup"><span data-stu-id="2994e-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="2994e-129">O **ColumnBreak** só é especificado para o `Large` modelo.</span><span class="sxs-lookup"><span data-stu-id="2994e-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2994e-130">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2994e-130">Element information</span></span>

* <span data-ttu-id="2994e-131">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="2994e-131">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="2994e-132">**Pode estar vazio**: Sim</span><span class="sxs-lookup"><span data-stu-id="2994e-132">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="2994e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2994e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2994e-134">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="2994e-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





