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
ms.openlocfilehash: 00257783c0c8a7919251004a4b1996ab4d994c3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105765602"
---
# <a name="columnbreak-element"></a><span data-ttu-id="02035-104">Elemento ColumnBreak</span><span class="sxs-lookup"><span data-stu-id="02035-104">ColumnBreak element</span></span>

<span data-ttu-id="02035-105">Representa um separador vertical (visível ou oculto) em modelos de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizados.</span><span class="sxs-lookup"><span data-stu-id="02035-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="02035-106">Uso</span><span class="sxs-lookup"><span data-stu-id="02035-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="02035-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="02035-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02035-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="02035-108">Attribute</span></span></th>
<th><span data-ttu-id="02035-109">Type</span><span class="sxs-lookup"><span data-stu-id="02035-109">Type</span></span></th>
<th><span data-ttu-id="02035-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02035-110">Required</span></span></th>
<th><span data-ttu-id="02035-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="02035-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02035-112"><strong>Separador</strong></span><span class="sxs-lookup"><span data-stu-id="02035-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="02035-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="02035-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="02035-114">Não</span><span class="sxs-lookup"><span data-stu-id="02035-114">No</span></span><br/></td>
<td><span data-ttu-id="02035-115">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="02035-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="02035-116">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="02035-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="02035-117">Padrão.</span><span class="sxs-lookup"><span data-stu-id="02035-117">Default.</span></span> <br/> </dd> <span data-ttu-id="02035-118"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="02035-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="02035-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="02035-119">Child elements</span></span>

<span data-ttu-id="02035-120">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="02035-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="02035-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="02035-121">Parent elements</span></span>



| <span data-ttu-id="02035-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="02035-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="02035-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="02035-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="02035-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="02035-124">Remarks</span></span>

<span data-ttu-id="02035-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="02035-125">Optional.</span></span>

<span data-ttu-id="02035-126">Pode ocorrer uma ou mais vezes para cada elemento [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="02035-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="02035-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02035-127">Examples</span></span>

<span data-ttu-id="02035-128">O exemplo a seguir demonstra a marcação básica para um elemento **ColumnBreak** em um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões.</span><span class="sxs-lookup"><span data-stu-id="02035-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="02035-129">O **ColumnBreak** só é especificado para o `Large` modelo.</span><span class="sxs-lookup"><span data-stu-id="02035-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="02035-130">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="02035-130">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="02035-131">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02035-131">Minimum supported system</span></span><br/> | <span data-ttu-id="02035-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02035-132">Windows 7</span></span> |
| <span data-ttu-id="02035-133">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="02035-133">Can be empty</span></span>                        | <span data-ttu-id="02035-134">Sim</span><span class="sxs-lookup"><span data-stu-id="02035-134">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="02035-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="02035-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02035-136">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="02035-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





