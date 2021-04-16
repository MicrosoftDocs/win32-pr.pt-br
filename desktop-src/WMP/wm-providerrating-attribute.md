---
title: Atributo WM/ProviderRating
description: O atributo WM/ProviderRating é a classificação do item atribuído pelo provedor dos valores de atributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Atributo WM/ProviderRating do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0f71985d948e59b8c0f98d50445a48263d67cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765346"
---
# <a name="wmproviderrating-attribute"></a>Atributo WM/ProviderRating

O atributo **WM/ProviderRating** é a classificação do item atribuído pelo provedor dos valores de atributo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

A **classificação** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProviderRating.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





