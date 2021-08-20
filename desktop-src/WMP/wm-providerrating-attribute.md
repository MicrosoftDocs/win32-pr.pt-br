---
title: Atributo WM/ProviderRating
description: O atributo WM/ProviderRating é a classificação do item atribuído pelo provedor dos valores de atributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Atributo WM/ProviderRating Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcff262f21b4f31daff6f704dba1cb096f54bb295a21a3ae9a7c90f574af34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116595"
---
# <a name="wmproviderrating-attribute"></a>Atributo WM/ProviderRating

O **atributo WM/ProviderRating** é a classificação do item atribuído pelo provedor dos valores de atributo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [CD Playlists](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado na biblioteca (ou cache) e no arquivo de mídia digital.

**Classificação** é um alias para esse atributo.

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszWMProviderRating.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





