---
title: Atributo WM/MediaClassSecondaryID
description: O atributo WM/MediaClassSecondaryID é um GUID que especifica a classe de mídia secundária, que é uma subclasse da classe de mídia primária.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Atributo WM/MediaClassSecondaryID Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9582fc3db713b8db945ec17534f1dc9c951402eea88489285526d6a3cfbdf147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000986"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Atributo WM/MediaClassSecondaryID

O **atributo WM/MediaClassSecondaryID** é um GUID que especifica a classe de mídia secundária, que é uma subclasse da classe de mídia primária.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado na biblioteca e no arquivo de mídia digital.

A tabela a seguir lista os GUIDs com suporte e suas descrições.



| GUID                                 | Descrição                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | O objeto de mídia representa uma playlist estática. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | O objeto de mídia representa uma playlist automática.  |



 

**MediaClassSecondaryID** é um alias para esse atributo.

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszWMMediaClassSecondaryID.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | O item de foto só tem suporte no Windows Media Player 10 ou posterior. O item de rádio tem suporte apenas no Windows Media Player Série 9 Todos os outros itens têm suporte no Windows Media Player Série 9 e posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





