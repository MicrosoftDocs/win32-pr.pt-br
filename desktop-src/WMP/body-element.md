---
title: Elemento body
description: O elemento body contém os elementos que definem o conteúdo de uma playlist.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Elemento de corpo Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c785b7db7b44177469596450ee75a460e2bc6224b191a2811baf95380bea25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135949"
---
# <a name="body-element"></a>Elemento body

O elemento **Body** contém os elementos que definem o conteúdo de uma playlist.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                 |
|-----------|--------------------------|
| Pai    | [SMIL](smil-element.md) |
| Filho     | [Seq](seq-element.md)   |



 

## <a name="remarks"></a>Comentários

O conteúdo de uma lista de reprodução é organizado em um elemento **Seq** que está contido no elemento **Body** . Normalmente, há um elemento **Seq** que define um conjunto estático de itens de mídia e contém elementos de **mídia** , ou há um que define um conjunto dinâmico de itens de mídia e contém um elemento **smartPlaylist** .

## <a name="examples"></a>Exemplos


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de mídia**](media-element.md)
</dt> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento SMIL**](smil-element.md)
</dt> <dt>

[**Windows Referência de elementos de playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





