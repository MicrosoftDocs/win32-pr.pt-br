---
title: Elemento GroupSizeDefinition
description: Representa um tamanho de layout para um grupo de controles em um modelo personalizado.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Faixa de GroupSizeDefinition do elemento do Windows
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105763053"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="046c9-104">Elemento GroupSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="046c9-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="046c9-105">Representa um tamanho de layout para um grupo de controles em um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="046c9-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="046c9-106">Uso</span><span class="sxs-lookup"><span data-stu-id="046c9-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="046c9-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="046c9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="046c9-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="046c9-108">Attribute</span></span></th>
<th><span data-ttu-id="046c9-109">Type</span><span class="sxs-lookup"><span data-stu-id="046c9-109">Type</span></span></th>
<th><span data-ttu-id="046c9-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="046c9-110">Required</span></span></th>
<th><span data-ttu-id="046c9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="046c9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="046c9-112"><strong>Tamanho</strong></span><span class="sxs-lookup"><span data-stu-id="046c9-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="046c9-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="046c9-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="046c9-114">Não</span><span class="sxs-lookup"><span data-stu-id="046c9-114">No</span></span><br/></td>
<td><span data-ttu-id="046c9-115">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="046c9-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="046c9-116">
<dt><span></span><span></span><strong></strong> Vários</span><span class="sxs-lookup"><span data-stu-id="046c9-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="046c9-117">Padrão.</span><span class="sxs-lookup"><span data-stu-id="046c9-117">Default.</span></span> <br/> </dd> <span data-ttu-id="046c9-118"><dt><span></span><span></span><strong></strong> Médio</span><span class="sxs-lookup"><span data-stu-id="046c9-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="046c9-119"><dt><span></span><span></span><strong></strong> Menores</span><span class="sxs-lookup"><span data-stu-id="046c9-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="046c9-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="046c9-120">Child elements</span></span>



| <span data-ttu-id="046c9-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="046c9-121">Element</span></span>                                                                                 | <span data-ttu-id="046c9-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="046c9-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="046c9-123">**ColumnBreak**</span><span class="sxs-lookup"><span data-stu-id="046c9-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="046c9-124">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="046c9-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="046c9-125">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="046c9-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="046c9-126">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="046c9-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="046c9-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="046c9-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="046c9-128">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="046c9-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="046c9-129">**Fila**</span><span class="sxs-lookup"><span data-stu-id="046c9-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="046c9-130">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="046c9-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="046c9-131">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="046c9-131">Parent elements</span></span>



| <span data-ttu-id="046c9-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="046c9-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="046c9-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="046c9-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="046c9-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="046c9-134">Remarks</span></span>

<span data-ttu-id="046c9-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="046c9-135">Optional.</span></span>

<span data-ttu-id="046c9-136">Pode ocorrer até três vezes para cada elemento [**SizeDefinition**](windowsribbon-element-sizedefinition.md) (uma vez para cada *tamanho*).</span><span class="sxs-lookup"><span data-stu-id="046c9-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="046c9-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="046c9-137">Examples</span></span>

<span data-ttu-id="046c9-138">O exemplo de código a seguir ilustra um modelo personalizado básico que inclui os três tamanhos de layout de grupo que devem ser definidos com o elemento **GroupSizeDefinition** ao criar um modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="046c9-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="046c9-139">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="046c9-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="046c9-140">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="046c9-140">Minimum supported system</span></span><br/> | <span data-ttu-id="046c9-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="046c9-141">Windows 7</span></span> |
| <span data-ttu-id="046c9-142">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="046c9-142">Can be empty</span></span>                        | <span data-ttu-id="046c9-143">Não</span><span class="sxs-lookup"><span data-stu-id="046c9-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="046c9-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="046c9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046c9-145">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="046c9-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





