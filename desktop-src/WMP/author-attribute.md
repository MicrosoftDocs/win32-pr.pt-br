---
title: Atributo de autor
description: O atributo autor é o nome de um artista de mídia ou ator associado ao conteúdo.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Atributo de autor Windows Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760473"
---
# <a name="author-attribute"></a>Atributo de autor

O atributo **autor** é o nome de um artista de mídia ou ator associado ao conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Arquivos de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Media. getItemInfoByType](media-getiteminfobytype.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia.

Esse atributo pode ter vários valores. Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar a *mídia*. método **getItemInfoByType** , não a *mídia*. método **getItemInfo** .

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMAuthor.

**Ator** e **artista** são aliases para este atributo.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





