---
title: THEME.openView
description: O método openView abre uma VIEW em uma nova janela.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEME.openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e5dd33760cb86ef1f85f7efd8a3ff38cb36f0408076555e2fe8732ffb53779a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466606"
---
# <a name="themeopenview"></a>THEME.openView

O **método openView** abre **uma VIEW** em uma nova janela.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Ver*
</dt> <dd>

Uma **Cadeia de** caracteres que especifica a **ID** do **VIEW** a ser aberto.

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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





