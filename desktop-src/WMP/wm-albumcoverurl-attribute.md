---
title: Atributo WM/AlbumCoverURL
description: O atributo WM/AlbumCoverURL é o Uniform Resource Locator (URL) para arte de álbum ou uma imagem em miniatura.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Atributo WM/AlbumCoverURL do Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813745"
---
# <a name="wmalbumcoverurl-attribute"></a>Atributo WM/AlbumCoverURL

O atributo **WM/AlbumCoverURL** é o Uniform Resource Locator (URL) para arte de álbum ou uma imagem em miniatura.

## <a name="applies-to"></a>Aplica-se A

-   [**Itens de áudio**](audio-item-attributes.md)
-   [**Itens de foto**](photo-item-attributes.md)
-   [**Itens de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Para um item de áudio, esse atributo é a URL da arte do álbum. Para um item de foto ou de vídeo, esse atributo é a URL de uma imagem em miniatura.

Este atributo não está disponível para itens de mídia na biblioteca local do usuário atual. Ele está disponível somente para itens de mídia que pertencem a uma biblioteca remota; ou seja, uma biblioteca que foi disponibilizada por outro usuário na rede doméstica. Para determinar se uma biblioteca de mídia é remota, chame o [**\_ tipo IWMPLibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 12 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





