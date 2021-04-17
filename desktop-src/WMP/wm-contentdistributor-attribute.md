---
title: Atributo WM/ContentDistributor
description: O atributo WM/ContentDistributor é o nome do distribuidor do item.
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- Atributo WM/ContentDistributor do Windows Media Player
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420e3e05a68f89d8e37b8ef95dd1247802442700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813698"
---
# <a name="wmcontentdistributor-attribute"></a>Atributo WM/ContentDistributor

O atributo **WM/ContentDistributor** é o nome do distribuidor do item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**ContentDistributor** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMContentDistributor.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





