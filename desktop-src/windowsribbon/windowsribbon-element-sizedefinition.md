---
title: Elemento SizeDefinition
description: Representa um modelo de layout personalizado de controles da faixa de opção.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- elemento SizeDefinition da faixa de Windows
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 982825649afb7640f87cb7032b000d837915c4bc9d970444da3c5cd3a5a98375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439531"
---
# <a name="sizedefinition-element"></a>Elemento SizeDefinition

Representa um modelo de layout personalizado de controles da faixa de opção.

## <a name="usage"></a>Uso

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
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
<td><strong>Nome</strong><br/></td>
<td>xs: positiveInteger ou xs: String ou xs: token<br/></td>
<td>Sim<br/></td>
<td>Quando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. SizeDefinitions</strong></a> for o pai, caso contrário, opcional.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String ou xs: token)<br/> </dt> <dd> Uma cadeia de caracteres ou um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                             | Descrição                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**ControlNameMap**](windowsribbon-element-controlnamemap.md)<br/>           | Pode ocorrer no máximo uma vez<br/> <br/>   |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> | Deve ocorrer pelo menos uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Grupo**](windowsribbon-element-group.md)<br/>                                   |
| [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento de [**grupo**](windowsribbon-element-group.md) .

Pode ocorrer uma ou mais vezes para cada elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .

Os modelos de [layout](windowsribbon-templates.md) de estrutura da faixa de opção predefinidos são especificados com o atributo *SizeDefinition* do elemento [**Group**](windowsribbon-element-group.md) .

Se um elemento [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondente não for declarado para cada elemento de [**grupo**](windowsribbon-element-group.md) em um elemento de [**guia**](windowsribbon-element-tab.md) , ocorrerá um erro de validação.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir ilustra um modelo personalizado básico.


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


- **sistema mínimo com suporte**: Windows 7 
- **Pode estar vazio**: não



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





