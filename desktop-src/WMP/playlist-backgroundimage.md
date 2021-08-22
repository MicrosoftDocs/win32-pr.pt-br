---
title: PLAYLIST.backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST.backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ddcb42f118a5a672b6678079825b6cb3d6aba5fbdc54953fb566e4222f583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054244"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST.backgroundImage

O **atributo backgroundImage** especifica ou recupera a imagem de plano de fundo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres **de** leitura/gravação que contém o nome de um arquivo de imagem. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Se a altura e a largura da imagem são menores que a altura e a largura do elemento **PLAYLIST,** a imagem é lado a lado. Os formatos com suporte são BMP, JPG, GIF e PNG.

Especificar um valor de "gradiente" para a imagem da tela de fundo faz com que a tela de fundo da playlist seja exibida como um gradiente de cores. Isso significa que a cor da tela de fundo faz a transição gradual entre os valores [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (na parte superior da tela de fundo) e [PLAYLIST.statusColor.](playlist-statuscolor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior, Windows Media Player 10 para o recurso de gradiente<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





