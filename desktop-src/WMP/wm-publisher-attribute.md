---
title: Atributo WM/Publisher
description: O atributo WM/Publisher é o nome da empresa que publicou o conteúdo.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Atributo WM/Publisher Windows Media Player
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22aa04eecb3999b3029948739eef51dab094d0ebf9b65ba01ccdcf6de59efc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053784"
---
# <a name="wmpublisher-attribute"></a>Atributo WM/Publisher

O **atributo WM/Publisher** é o nome da empresa que publicou o conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [CD Playlists](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado na biblioteca (ou cache) e no arquivo de mídia digital.

**Rótulo**, **ReleasedBy** e **Studio são** aliases para esse atributo.

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszWMPublisher.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





