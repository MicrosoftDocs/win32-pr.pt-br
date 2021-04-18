---
title: Elemento Title (WPL)
description: O elemento Title especifica um título para a lista de reprodução.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento Title (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786255"
---
# <a name="title-element-wpl"></a>Elemento Title (WPL)

O elemento **title** especifica um título para a lista de reprodução.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                 |
|-----------|--------------------------|
| Pai    | [principal](head-element.md) |
| Filho     | Nenhum                     |



 

## <a name="remarks"></a>Comentários

Ao escolher um título para uma lista de reprodução de mídia do Windows (WPL), considere que o conteúdo da lista de reprodução pode ser dinâmico. Uma boa abordagem é basear o título na lógica nos elementos de **argumento** porque isso é o que define o conteúdo da lista de reprodução. Exemplos disso são "minhas músicas de rock favoritas de 1966" ou "dança canções que não reproduzi recentemente".

## <a name="examples"></a>Exemplos


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento Argument**](argument-element.md)
</dt> <dt>

[**Elemento head**](head-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





