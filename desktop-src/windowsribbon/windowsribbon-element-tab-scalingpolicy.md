---
title: Propriedade Tab. ScalingPolicy
description: Representa um contêiner para as especificações de dimensionamento de tabulação.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Ribbon. ScalingPolicy da propriedade Windows
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455776"
---
# <a name="tabscalingpolicy-property"></a>Propriedade Tab. ScalingPolicy

Representa um contêiner para as especificações de dimensionamento de [Tabulação](windowsribbon-controls-tab.md) .

## <a name="usage"></a>Uso

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                 | Descrição                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                             |
|-----------------------------------------------------|
| [**Tab**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**guia**](windowsribbon-element-tab.md).

As especificações de dimensionamento descrevem o tamanho e o comportamento de layout dos controles em uma [guia](windowsribbon-controls-tab.md) quando a faixa de opção é redimensionada.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir demonstra um manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica uma preferência de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





