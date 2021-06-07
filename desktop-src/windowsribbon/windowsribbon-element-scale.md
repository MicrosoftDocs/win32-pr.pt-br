---
title: Elemento Scale
description: Representa o tamanho e a preferência de layout de um Grupo de controles por meio de um par Group, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Faixa de opções do Windows do elemento Scale
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445007"
---
# <a name="scale-element"></a>Elemento Scale

Representa o tamanho e a preferência de layout de um [**Grupo**](windowsribbon-element-group.md) de controles por meio de um par {**Grupo**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.

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
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Sim<br/></td>
<td>Deve corresponder a um <em>CommandName de Grupo existente.</em> <a href="windowsribbon-element-group.md"><strong></strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres ou um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Tamanho</strong><br/></td>
<td>xs:string<br/></td>
<td>Sim<br/></td>
<td>Esse valor deve corresponder a um dos tamanhos válidos para <a href="windowsribbon-element-group.md"><strong></strong></a> o atributo <em>SizeDefinition</em> do Grupo de controles associado especificado no <em>Grupo</em>. <br/> Restrito a um dos seguintes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> (Pop-up)<br/> </dt> <dd> Layout de controle idêntico <code>Large</code> para , mas hospedado em um pop-up ou em um painel de lista.<br/> </dd> <dt><span></span><span></span><strong></strong> (Pequeno)<br/> </dt> <dd> Modelo <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeno.<br/> </dd> <dt><span></span><span></span><strong></strong> (Médio)<br/> </dt> <dd> Modelo <a href="windowsribbon-element-sizedefinition.md"><strong>Medium SizeDefinition.</strong></a><br/> </dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Modelo <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.<br/> </dd> </dl></td>
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

Pode ocorrer uma ou mais vezes para [**cada ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ou [**ScalingPolicy.IdealSizes.**](windowsribbon-element-scalingpolicy-idealsizes.md)

Cada par de atributos (*Grupo* *,* Tamanho ) deve ser exclusivo.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra como [**a**](windowsribbon-element-group.md) aparência dos controles em um grupo pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos Ribbon [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)

O [**manifesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) neste exemplo especifica uma preferência [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma **guia** Início. Além disso, **os elementos Scale** são especificados para influenciar o comportamento de ressução, em ordem de tamanho decrescente, de cada grupo.


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



* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Sim



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





