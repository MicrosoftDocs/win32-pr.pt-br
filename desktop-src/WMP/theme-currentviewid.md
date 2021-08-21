---
title: THEME.currentViewID
description: O atributo currentViewID especifica ou recupera o VIEW exibido no momento.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME.currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21bf3027b0249286689862e53fc2d616d1d33b19eca562c886e981bffb7f0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117807"
---
# <a name="themecurrentviewid"></a>THEME.currentViewID

O **atributo currentViewID** especifica ou recupera o VIEW exibido **no momento.**

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que especifica **a ID** do **VIEW atual.** Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Especificar **currentViewID** fecha automaticamente o **currentView** existente (apontado pelo atributo global **de** exibição) e abre a **VIEW especificada.**

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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





