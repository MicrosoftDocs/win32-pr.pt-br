---
title: Elemento SMIL
description: O elemento SMIL é sempre o elemento de nível superior em um arquivo de lista de reprodução de mídia do Windows (WPL). Ele especifica que o arquivo usa sintaxe e gramática de SMIL (linguagem de integração multimídia sincronizada).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Elemento SMIL Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754071"
---
# <a name="smil-element"></a>Elemento SMIL

O elemento **SMIL** é sempre o elemento de nível superior em um arquivo de lista de reprodução de mídia do Windows (WPL). Ele especifica que o arquivo usa sintaxe e gramática de SMIL (linguagem de integração multimídia sincronizada).

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                           |
|-----------|----------------------------------------------------|
| Pai    | Nenhum                                               |
| Filho     | [cabeçalho](head-element.md), [corpo](body-element.md) |



 

## <a name="remarks"></a>Comentários

Cada playlist do Windows Media deve ter o elemento **SMIL** em sua raiz.

## <a name="examples"></a>Exemplos


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento body**](body-element.md)
</dt> <dt>

[**Elemento head**](head-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





