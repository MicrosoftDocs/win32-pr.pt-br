---
title: Atributo de direitos autorais (msfeeds. h)
description: O atributo de direitos autorais é a mensagem de direitos autorais do item.
ms.assetid: 617272cb-883f-46d6-b0a9-29ac32c63148
keywords:
- Windows Media Player de atributo de direitos autorais
topic_type:
- apiref
api_name:
- Copyright
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b42e68e0d3485824f502dea991048121e788dfbe574b8fa4921e93a3b7afb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651956"
---
# <a name="copyright-attribute"></a>Atributo de direitos autorais

O atributo de **direitos autorais** é a mensagem de direitos autorais do item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [arquivos de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMCopyright.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                    |
| Cabeçalho<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





