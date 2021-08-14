---
title: Propriedade Ribbon.Tabs
description: Representa um contêiner para todas as guias principais em uma Faixa de Opções.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Propriedade Ribbon.Tabs Windows Faixa de Opções
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b055a2fd8d69b45e2f7059022908b5cb91f8e790196504172c0ad1c608b78c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202207"
---
# <a name="ribbontabs-property"></a>Propriedade Ribbon.Tabs

Representa um contêiner para todas as guias principais em uma Faixa de Opções.

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

Pode ocorrer uma ou mais vezes para cada Faixa de [**Opções.**](windowsribbon-element-ribbon.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para um **elemento Ribbon.Tabs** com uma **declaração de** [**Guia**](windowsribbon-element-tab.md) Base.


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
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





