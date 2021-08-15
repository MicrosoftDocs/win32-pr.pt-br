---
title: Elemento head
description: O elemento head contém metadados que se aplica à playlist inteira.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- elemento head Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a865419a005927cd85ea6b03d4fabad2e2ac3ef15a840b3bd01209a4df00c075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339160"
---
# <a name="head-element"></a>Elemento head

O **elemento head** contém metadados que se aplica à playlist inteira.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                                  |
|-----------|-----------------------------------------------------------|
| Pai    | [Smil](smil-element.md)                                  |
| Filho     | [title](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Comentários

Normalmente, o **elemento principal** contém um elemento **de título** e um ou mais **metadados** que definem características globais da playlist.

## <a name="examples"></a>Exemplos


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**elemento meta**](meta-element.md)
</dt> <dt>

[**Elemento title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Windows Referência de elementos da playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





