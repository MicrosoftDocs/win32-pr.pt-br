---
title: THEME. openView
description: O método openView abre uma exibição em uma nova janela.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- TEMA. openView do Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760732"
---
# <a name="themeopenview"></a>THEME. openView

O método **openView** abre uma **exibição** em uma nova janela.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*exibição*
</dt> <dd>

Uma **cadeia de caracteres** que especifica a **ID** da **exibição** a ser aberta.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="examples"></a>Exemplos


```JScript
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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





