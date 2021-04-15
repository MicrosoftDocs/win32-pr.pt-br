---
title: Propriedade Ribbon. Tabs
description: Representa um contêiner para todas as guias de núcleo em uma faixa de faixas.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Faixa de das propriedades do Windows da faixa de guia. Tabs
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454713"
---
# <a name="ribbontabs-property"></a>Propriedade Ribbon. Tabs

Representa um contêiner para todas as guias de núcleo em uma faixa de faixas.

## <a name="usage"></a>Uso

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                             | Descrição                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Tab**](windowsribbon-element-tab.md)<br/> | Deve ocorrer pelo menos uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Faixa de opções**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Pode ocorrer uma ou mais vezes para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para um elemento **Ribbon. Tabs** com uma declaração de [**guia**](windowsribbon-element-tab.md) **página inicial** .


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





