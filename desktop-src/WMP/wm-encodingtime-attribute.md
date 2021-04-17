---
title: Atributo WM/Encodingtime
description: O atributo WM/Encodingtime é a data e a hora em que o conteúdo foi codificado.
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- Atributo WM/Encodingtime Windows Media Player
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659a1ec5b192782370804745da3f232db6e439dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797989"
---
# <a name="wmencodingtime-attribute"></a>Atributo WM/Encodingtime

O atributo **WM/encodingtime** é a data e a hora em que o conteúdo foi codificado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**CreationDate** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMEncodingTime.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





