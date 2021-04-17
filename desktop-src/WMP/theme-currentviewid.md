---
title: THEME. currentViewID
description: O atributo currentViewID especifica ou recupera a exibição exibida no momento.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751140"
---
# <a name="themecurrentviewid"></a>THEME. currentViewID

O atributo **currentViewID** especifica ou recupera a **exibição** exibida no momento.

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que especifica a **ID** da **exibição** atual. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

A especificação de **currentViewID** fecha automaticamente o **modoatual** existente (apontado pelo atributo global **View** ) e abre a **exibição** especificada.

## <a name="examples"></a>Exemplos


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





