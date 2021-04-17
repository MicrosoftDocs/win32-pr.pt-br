---
title: Elemento head
description: O elemento head contém metadados que se aplicam a toda a lista de reprodução.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Elemento de cabeçalho Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759701"
---
# <a name="head-element"></a>Elemento head

O elemento **Head** contém metadados que se aplicam a toda a lista de reprodução.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                                  |
|-----------|-----------------------------------------------------------|
| Pai    | [SMIL](smil-element.md)                                  |
| Filho     | [título](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Comentários

Normalmente, o elemento **Head** contém um elemento **title** e um ou mais **meta** Elements que definem características globais da playlist.

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
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento meta**](meta-element.md)
</dt> <dt>

[**Elemento Title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





