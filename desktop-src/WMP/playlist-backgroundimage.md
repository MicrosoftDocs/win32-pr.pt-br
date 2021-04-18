---
title: PLAYLIST. backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Windows Media Player de PLAYLIST. backgroundImage
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814016"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST. backgroundImage

O atributo **backgroundImage** especifica ou recupera a imagem de plano de fundo.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

Se a altura e a largura da imagem forem menores do que a altura e a largura do elemento **playlist** , a imagem será colocada em lado. Os formatos com suporte são BMP, JPG, GIF e PNG.

A especificação de um valor de "gradação" para a imagem de fundo faz com que o plano de fundo da lista de reprodução seja exibido como um gradiente de cor. Isso significa que a cor do plano de fundo faz a transição gradualmente entre o [playlist. BackgroundColor](playlist-backgroundcolor.md) (na parte superior do plano de fundo) e os valores de [playlist. statusColor](playlist-statuscolor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior, Windows Media Player 10 para o recurso de gradiente<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





