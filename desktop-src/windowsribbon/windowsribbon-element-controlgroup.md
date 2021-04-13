---
title: Elemento Control
description: Representa um grupo de controles em um modelo de layout SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Faixa de das janelas do elemento controlus
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365477"
---
# <a name="controlgroup-element"></a>Elemento Control

Representa um grupo de controles em um modelo de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

## <a name="usage"></a>Uso

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
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
<td><strong>SequenceNumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>Válido somente quando o <a href="windowsribbon-element-group.md"><strong>grupo</strong></a> é o elemento pai.<br/> Cada <em>SequenceNumber</em> deve ser exclusivo dentro de um elemento de <a href="windowsribbon-element-group.md"><strong>grupo</strong></a> . Os valores de <em>SequenceNumber</em> devem aumentar para cada elemento de <strong>grupo</strong> , mas não precisam ser sequenciais. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1000 e 59999, inclusive.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                 | Descrição                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>             | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                     | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>             | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Controle giratório**](windowsribbon-element-spinner.md)<br/>                             | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                             |
|-------------------------------------------------------------------------------------|
| **Controlador de controle**<br/>                                                         |
| [**Grupo**](windowsribbon-element-group.md)<br/>                             |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Fila**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada elemento [**Group**](windowsribbon-element-group.md) ou **Control** .

Se nenhum número de sequência for fornecido, os elementos serão renderizados na ordem especificada na marcação da faixa de lista.

Se [**Group ou grupo**](windowsribbon-element-group.md) de **controle** for o elemento pai, então **Control** agrupar será restrito aos seguintes elementos filho possíveis: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md)

Caso contrário, quando [**Row**](windowsribbon-element-row.md) ou [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) for o pai, [**Group**](windowsribbon-element-group.md) será restrito ao seguinte elemento filho possível: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir demonstra a marcação básica para um modelo personalizado de layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de quatro botões com vários elementos de [**grupo**](windowsribbon-element-group.md) .


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Não        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





