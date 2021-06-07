---
title: Elemento GroupSizeDefinition
description: Representa um tamanho de layout para um grupo de controles em um modelo personalizado.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Faixa de Opções do Windows do elemento GroupSizeDefinition
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 650301a29ace2c6df9316a315d4cdbad448e5573
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443377"
---
# <a name="groupsizedefinition-element"></a>Elemento GroupSizeDefinition

Representa um tamanho de layout para um grupo de controles em um modelo personalizado.

## <a name="usage"></a>Uso

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tamanho</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (Médio)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Pequeno)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                 | Descrição                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ColumnBreak**](windowsribbon-element-columnbreak.md)<br/>                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                   | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Controlsizedefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Linha**](windowsribbon-element-row.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                   |
|---------------------------------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer até três vezes para cada [**elemento SizeDefinition**](windowsribbon-element-sizedefinition.md) (uma vez para cada *Tamanho*).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir ilustra um modelo personalizado básico que inclui os três tamanhos de layout de grupo que devem ser definidos com o elemento **GroupSizeDefinition** ao criar um modelo personalizado.


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



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





