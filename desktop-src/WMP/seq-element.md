---
title: Elemento seq
description: O elemento seq contém elementos que definem uma lista de reprodução estática ou elementos que definem uma lista de reprodução inteligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento seq Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751779"
---
# <a name="seq-element"></a>Elemento seq

O elemento **Seq** contém elementos que definem uma lista de reprodução estática ou elementos que definem uma lista de reprodução inteligente.

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                                               |
|-----------|------------------------------------------------------------------------|
| Pai    | [body](body-element.md)                                               |
| Filho     | [mídia](media-element.md), [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>Comentários

Quando um elemento **Seq** contém apenas elementos de **mídia** que fazem referência a itens de mídia específicos, a playlist é considerada estática. Quando um elemento **Seq** contém um elemento **smartPlaylist** , é considerado uma lista de reprodução dinâmica "inteligente".

## <a name="examples"></a>Exemplos


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento body**](body-element.md)
</dt> <dt>

[**Elemento de mídia**](media-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





