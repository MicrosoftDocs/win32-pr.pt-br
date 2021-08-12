---
title: Propriedade ScalingPolicy. IdealSizes
description: Representa um contêiner de especificações de escala para o modelo de SizeDefinition preferencial, com base no tamanho da faixa de medida.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- propriedade ScalingPolicy. IdealSizes Windows Ribbon
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500f6193411ed72b8858506816d9af4f82b1219680fa0537bf54b3daa7735211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439521"
---
# <a name="scalingpolicyidealsizes-property"></a>Propriedade ScalingPolicy. IdealSizes

Representa um contêiner de especificações de escala para o modelo de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferencial, com base no tamanho da faixa de medida.

## <a name="usage"></a>Uso

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                 | Descrição                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Escala**](windowsribbon-element-scale.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).

Se **ScalingPolicy. IdealSizes** for definido, uma entrada de [**escala**](windowsribbon-element-scale.md) para cada elemento de [**grupo**](windowsribbon-element-group.md) em um elemento de [**guia**](windowsribbon-element-tab.md) deverá estar presente.

**ScalingPolicy. IdealSizes** são os layouts de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferenciais para um [**grupo**](windowsribbon-element-group.md) de controles.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra como a aparência de controles em um [**grupo**](windowsribbon-element-group.md) pode ser personalizada por meio da funcionalidade de layout adaptável dos modelos de faixa de opções [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

O manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) neste exemplo especifica uma preferência de **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.


```C++
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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





