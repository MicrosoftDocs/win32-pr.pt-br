---
title: Atributo WM/ContentDistributor
description: O atributo WM/ContentDistributor é o nome do distribuidor do item.
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- Windows Media Player do atributo WM/ContentDistributor
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba79ab07b8579961db70038ef80f79da974ba5dff6d3ac88781be5d4f046f088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122702"
---
# <a name="wmcontentdistributor-attribute"></a>Atributo WM/ContentDistributor

O atributo **WM/ContentDistributor** é o nome do distribuidor do item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**ContentDistributor** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMContentDistributor.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





