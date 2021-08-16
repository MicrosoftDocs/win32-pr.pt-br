---
title: Atributo WM/Encodingtime
description: O atributo WM/Encodingtime é a data e a hora em que o conteúdo foi codificado.
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- Windows Media Player do atributo WM/Encodingtime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b143218b854177852049c1ae1ed530360c196eecd217db3ed53d9f46bd2915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122656"
---
# <a name="wmencodingtime-attribute"></a>Atributo WM/Encodingtime

O atributo **WM/encodingtime** é a data e a hora em que o conteúdo foi codificado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**CreationDate** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMEncodingTime.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





