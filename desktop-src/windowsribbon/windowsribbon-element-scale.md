---
title: Elemento Scale
description: Representa o tamanho e a preferência de layout de um grupo de controles por meio de um par de grupo, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Faixa de das janelas do elemento Scale
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365498"
---
# <a name="scale-element"></a>Elemento Scale

Representa o tamanho e a preferência de layout de um [**grupo**](windowsribbon-element-group.md) de controles por meio de um par {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.

## <a name="usage"></a>Uso

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
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
<td><strong>Grupo</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Sim<br/></td>
<td>Deve corresponder a um <a href="windowsribbon-element-group.md"><strong>grupo</strong></a> de <em>CommandName</em>existente.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres ou um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Tamanho</strong><br/></td>
<td>xs:string<br/></td>
<td>Sim<br/></td>
<td>Esse valor deve corresponder a um dos tamanhos válidos para o atributo <em>SizeDefinition</em> do <a href="windowsribbon-element-group.md"><strong>grupo</strong></a> associado de controles especificado no <em>grupo</em>. <br/> Restrito a um dos seguintes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> Pop-up<br/> </dt> <dd> Layout de controle idêntico a <code>Large</code> , mas hospedado em um pop-up ou em um painel suspenso.<br/> </dd> <dt><span></span><span></span><strong></strong> Menores<br/> </dt> <dd> Modelo de <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeno.<br/> </dd> <dt><span></span><span></span><strong></strong> Médio<br/> </dt> <dd> Modelo de <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> médio.<br/> </dd> <dt><span></span><span></span><strong></strong> Vários<br/> </dt> <dd> Modelo de <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ou [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).

Cada par de atributos (*grupo*, *tamanho*) deve ser exclusivo.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra como a aparência de controles em um [**grupo**](windowsribbon-element-group.md) pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos de faixa de opções [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

O manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) neste exemplo especifica uma preferência de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos **Scale** são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Sim       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





