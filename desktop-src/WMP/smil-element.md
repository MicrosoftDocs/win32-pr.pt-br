---
title: Elemento SMIL
description: o elemento smil é sempre o elemento de nível superior em um arquivo de lista de reprodução de mídia Windows (WPL). Ele especifica que o arquivo usa sintaxe e gramática de SMIL (linguagem de integração multimídia sincronizada).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Windows Media Player do elemento SMIL
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15ed9c3d70b0af65019cd384bc68ab9c26f8d01673481b9ced3595730379bf1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763456"
---
# <a name="smil-element"></a>Elemento SMIL

o elemento **smil** é sempre o elemento de nível superior em um arquivo de lista de reprodução de mídia Windows (WPL). Ele especifica que o arquivo usa sintaxe e gramática de SMIL (linguagem de integração multimídia sincronizada).

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

cada lista de reprodução de mídia Windows deve ter o elemento **smil** em sua raiz.

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

[**Windows Referência de elementos de playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





