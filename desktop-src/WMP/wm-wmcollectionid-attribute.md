---
title: Atributo WM/WMCollectionID
description: O atributo WM/WMCollectionID é um GUID que identifica a coleção à qual o item pertence.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- Atributo WM/WMCollectionID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808249"
---
# <a name="wmwmcollectionid-attribute"></a>Atributo WM/WMCollectionID

O atributo **WM/WMCollectionID** é um GUID que identifica a coleção à qual o item pertence.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia.

**WMCollectionID** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMCollectionID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





