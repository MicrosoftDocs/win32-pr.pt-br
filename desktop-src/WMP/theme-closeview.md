---
title: THEME.closeView
description: O método closeView fecha uma VIEW aberta.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEME.closeView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e66a0c56ab2f5fc3d5d6a27d996d8b3f3cf7834c61e62113a40af3c42aeb4d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932541"
---
# <a name="themecloseview"></a>THEME.closeView

O **método closeView** fecha um **VIEW aberto.**

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*
</dt> <dd>

Uma **Cadeia de** caracteres que especifica a **ID** do **VIEW a** ser fechado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="examples"></a>Exemplos


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





