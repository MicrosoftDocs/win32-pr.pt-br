---
title: Atributo WM/ContentDistributorType
description: O atributo WM/ContentDistributorType é o tipo do distribuidor do item.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Atributo WM/ContentDistributorType do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793336"
---
# <a name="wmcontentdistributortype-attribute"></a>Atributo WM/ContentDistributorType

O atributo **WM/ContentDistributorType** é o tipo do distribuidor do item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

O valor desse atributo será definido como "List" ou "Radio". Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**ContentDistributorType** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMContentDistributorType.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





