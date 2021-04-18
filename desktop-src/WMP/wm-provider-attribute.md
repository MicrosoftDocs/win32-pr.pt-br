---
title: Atributo do WM/provedor
description: O atributo WM/Provider é o nome do provedor dos valores de atributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Atributo do WM/provedor do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793359"
---
# <a name="wmprovider-attribute"></a>Atributo do WM/provedor

O atributo **WM/Provider** é o nome do provedor dos valores de atributo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

O **MetadataName** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProvider.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





