---
title: Elemento title (WPL)
description: O elemento title especifica um título para a playlist.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento title (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1de2679d5f78b48ceef569491ef21998fc13faf7126e61f76ad31959bdc2ac6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122776"
---
# <a name="title-element-wpl"></a>Elemento title (WPL)

O **elemento title** especifica um título para a playlist.

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
| Pai    | [Cabeça](head-element.md) |
| Filho     | Nenhum                     |



 

## <a name="remarks"></a>Comentários

Ao escolher um título para uma playlist Windows mídia (WPL), considere que o conteúdo da playlist pode ser dinâmico. Uma boa abordagem é basear o  título na lógica nos elementos de argumento porque é isso que define o conteúdo da playlist. Exemplos disso são "Minhas músicas de rock favoritas de 1966" ou "Músicas de música de música que não toquei recentemente".

## <a name="examples"></a>Exemplos


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento head**](head-element.md)
</dt> <dt>

[**Windows Referência de elementos da playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





