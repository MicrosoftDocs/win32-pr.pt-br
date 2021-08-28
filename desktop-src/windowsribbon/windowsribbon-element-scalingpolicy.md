---
title: Elemento ScalingPolicy
description: Representa um contêiner para especificações de dimensionamento.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Elemento ScalingPolicy Windows Faixa de Opções
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 202112a24a74c9b20d429910fd0ee9447002ce7f2cb95133165fb968eaaf4f69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007466"
---
# <a name="scalingpolicy-element"></a>Elemento ScalingPolicy

Representa um contêiner para especificações de dimensionamento.

## <a name="usage"></a>Uso

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                       | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Escala**](windowsribbon-element-scale.md)<br/>                                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer uma vez para [**cada Tab.ScalingPolicy.**](windowsribbon-element-tab-scalingpolicy.md)

O **elemento ScalingPolicy** contém um manifesto de [**declarações ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e [**Scale**](windowsribbon-element-scale.md) que especificam preferências de layout adaptável para um ou mais elementos [**Group**](windowsribbon-element-group.md) quando a Faixa de Opções é recalizada.

A lista [**de**](windowsribbon-element-scale.md) declarações scale deve estar em ordem decrescente de tamanhos válidos (Grande, Médio, Pequeno, Pop-up) para o [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associado ao [**elemento Group.**](windowsribbon-element-group.md)

> [!Note]  
> É altamente recomendável que os detalhes adequados da política de dimensionamento sejam especificados de forma que uma Faixa de Opções seja capaz de renderizar sem barras de rolagem quando re dimensionada para uma largura de 300 pixels a 96 pontos por polegada (dpi).

 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra como [**a**](windowsribbon-element-group.md) aparência dos controles em um grupo pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos Ribbon [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)

O **manifesto ScalingPolicy** neste exemplo especifica uma preferência [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma **guia** Início. Além disso, [**os elementos Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de ressução, em ordem de tamanho decrescente, de cada grupo.


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

- **Sistema mínimo com suporte:** Windows 7 
- **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





