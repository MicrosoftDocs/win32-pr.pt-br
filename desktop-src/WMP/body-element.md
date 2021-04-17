---
title: Elemento body
description: O elemento body contém os elementos que definem o conteúdo de uma playlist.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Elemento body Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761482"
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

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





