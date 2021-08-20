---
title: THEME.openViewRelative
description: O método openViewRelative abre uma VIEW em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME.openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a26040bb8f47d85be99f0d8df602bdd69835cfa648ac6d5898f786e4518acdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117770"
---
# <a name="themeopenviewrelative"></a>THEME.openViewRelative

O **método openViewRelative** abre uma **VIEW** em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Ver*
</dt> <dd>

Uma **Cadeia de** caracteres que especifica a **ID** do **VIEW** a ser aberto.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*Deixou*
</dt> <dd>

Um **Número** (**longo**) que especifica a distância inicial em pixels da borda esquerda da **VIEW** da borda esquerda da capa. Um valor negativo indica uma posição inicial à esquerda da borda da capa.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Início*
</dt> <dd>

Um **Número** (**longo**) que especifica a posição inicial da borda superior da **VIEW** em relação à borda superior da capa. Um valor negativo indica uma posição inicial acima da borda da capa.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A posição especificada para VIEW **é** usada na primeira vez que esse método é chamado, após o qual o usuário pode arrastar **VIEW** para outro local. A nova posição é salva e, em chamadas subsequentes, a posição mais recente é usada.

## <a name="examples"></a>Exemplos


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





