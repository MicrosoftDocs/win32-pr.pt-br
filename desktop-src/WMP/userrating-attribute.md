---
title: Atributo userrating
description: O atributo userrating é a classificação especificada pelo usuário na biblioteca.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Atributo userrating do Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765628"
---
# <a name="userrating-attribute"></a>Atributo userrating

O atributo **userrating** é a classificação especificada pelo usuário na biblioteca.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

As classificações de usuário são representadas por valores inteiros, conforme descrito na tabela a seguir. Ao especificar um valor, use um dos valores da coluna de valor de gravação. Ao recuperar valores, você pode usar os intervalos na coluna valores de leitura para determinar o número de estrelas.



| Classificação  | Valor de gravação | Lendo valores |
|---------|---------------|----------------|
| Sem classificação | 0             | 0              |
| 1 estrela  | 1             | 1 a 12        |
| 2 estrelas | 25            | 13 a 37       |
| 3 estrelas | 50            | 38 a 62       |
| 4 estrelas | 75            | 63 a 86       |
| 5 estrelas | 99            | 87 a 99       |



 

Esse atributo é armazenado somente na biblioteca do.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





