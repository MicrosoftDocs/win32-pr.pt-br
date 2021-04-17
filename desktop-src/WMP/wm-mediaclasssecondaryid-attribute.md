---
title: Atributo WM/MediaClassSecondaryID
description: O atributo WM/MediaClassSecondaryID é um GUID que especifica a classe de mídia secundária, que é uma subclasse da classe de mídia primária.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Atributo WM/MediaClassSecondaryID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797985"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Atributo WM/MediaClassSecondaryID

O atributo **WM/MediaClassSecondaryID** é um GUID que especifica a classe de mídia secundária, que é uma subclasse da classe de mídia primária.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

A tabela a seguir lista os GUIDs com suporte e suas descrições.



| GUID                                 | Descrição                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | O objeto de mídia representa uma lista de reprodução estática. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | O objeto de mídia representa uma lista de reprodução automática.  |



 

**MediaClassSecondaryID** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMMediaClassSecondaryID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | O item de foto tem suporte apenas no Windows Media Player 10 ou posterior. o item de rádio só tem suporte no Windows Media Player 9 Series todos os outros itens têm suporte no Windows Media Player 9 Series e posteriores<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





