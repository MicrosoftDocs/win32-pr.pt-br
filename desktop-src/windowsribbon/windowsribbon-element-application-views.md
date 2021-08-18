---
title: Propriedade Application. views
description: Representa um contêiner para cada exibição de estrutura da faixa de forma, especificamente a faixa de e ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- propriedade Application. views Windows Ribbon
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe063397698a74da0421cf0c9c3b2ef46861f1477e0f4ac99fe5d6e6063c7251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964305"
---
# <a name="applicationviews-property"></a>Propriedade Application. views

Representa um contêiner para cada exibição de estrutura da faixa de forma, especificamente a [**faixa**](windowsribbon-element-ribbon.md) de e [**ContextPopup**](windowsribbon-element-contextpopup.md).

## <a name="usage"></a>Uso

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Descrição                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Faixa de opções**](windowsribbon-element-ribbon.md)<br/>             | Deve ocorrer exatamente uma vez<br/> <br/>     |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Aplicativo**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada elemento de [**aplicativo**](windowsribbon-element-application.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um elemento **Application. views** que contém um manifesto de controles de faixa de opções, cada um com uma referência a um comando declarado no elemento [**Application. paracommands**](windowsribbon-element-application-commands.md) .


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Application. Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





