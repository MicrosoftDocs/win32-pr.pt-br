---
title: Atributo WM/WMCollectionGroupID
description: O atributo WM/WMCollectionGroupID é um GUID que identifica o grupo que contém a coleção à qual o item pertence.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Atributo WM/WMCollectionGroupID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798197"
---
# <a name="wmwmcollectiongroupid-attribute"></a>Atributo WM/WMCollectionGroupID

O atributo **WM/WMCollectionGroupID** é um GUID que identifica o grupo que contém a coleção à qual o item pertence.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**WMCollectionGroupID** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMCollectionGroupID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





