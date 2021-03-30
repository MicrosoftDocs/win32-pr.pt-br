---
title: Propriedade Ribbon. HelpButton
description: Representa um contêiner para o botão de ajuda.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Faixa de HelpButton da propriedade Windows da faixa de propriedades
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644848"
---
# <a name="ribbonhelpbutton-property"></a>Propriedade Ribbon. HelpButton

Representa um contêiner para o [botão de ajuda](windowsribbon-controls-helpbutton.md).

## <a name="usage"></a>Uso

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                           | Descrição                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [**HelpButton**](windowsribbon-element-helpbutton.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Faixa de opções**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica necessária para implementar um botão de ajuda da faixa de opções.

Esta seção de código mostra a declaração de comando **Ribbon. HelpButton** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



Esta seção de código mostra a declaração de controle **Ribbon. HelpButton** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





