---
title: Objeto de mídia
description: O objeto de mídia fornece uma maneira de especificar ou recuperar propriedades de um item de mídia, usando as propriedades e os métodos a seguir.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Windows Media Player de objeto de mídia
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c1dbcb3dc662a431f279e03697620b80c242c99eb32e3bbcdc26d71796f7e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123306"
---
# <a name="media-object"></a>Objeto de mídia

O objeto de **mídia** fornece uma maneira de especificar ou recuperar propriedades de um item de mídia, usando as propriedades e os métodos a seguir.

O objeto de **mídia** dá suporte às propriedades a seguir.



| Propriedade                                         | Descrição                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | Recupera o número de atributos que podem ser consultados e/ou definidos para o item de mídia.              |
| [duration](media-duration.md)                   | Recupera a duração em segundos do item de mídia atual.                                       |
| [duraçãostring](media-durationstring.md)       | Recupera um valor de **cadeia de caracteres** que indica a duração do item de mídia atual no formato hh: mm: SS. |
| [error](media-error.md)                         | Recupera um objeto [ErrorItem](erroritem-object.md) se o item de mídia tiver uma condição de erro.    |
| [imageSourceHeight](media-imagesourceheight.md) | Recupera a altura do item de mídia atual em pixels.                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | Recupera a largura do item de mídia atual em pixels.                                           |
| [markerCount](media-markercount.md)             | Recupera o número de marcadores no item de mídia.                                                 |
| [name](media-name.md)                           | Especifica ou recupera o nome do item de mídia.                                                 |
| [sourceURL](media-sourceurl.md)                 | Recupera a URL do item de mídia.                                                               |



 

O objeto de **mídia** dá suporte aos métodos a seguir.



| Método                                                       | Descrição                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | Recupera o número de atributos associados ao nome do atributo e idioma especificados.            |
| [GetAttributeName](media-getattributename.md)               | Recupera o nome do atributo correspondente ao índice especificado.                                |
| [getItemInfo](media-getiteminfo.md)                         | Recupera o valor do atributo especificado para o item de mídia.                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | Recupera o valor do atributo com o número de índice especificado.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados. |
| [Getmarkname](media-getmarkername.md)                     | Recupera o nome do marcador no índice especificado.                                                 |
| [getmarcadortime](media-getmarkertime.md)                     | Recupera a hora do marcador no índice especificado.                                                 |
| [isidêntico](media-isidentical.md)                         | Recupera um valor que indica se o objeto fornecido é o mesmo que o atual.                 |
| [isMemberOf](media-ismemberof.md)                           | Recupera um valor que indica se o item de mídia especificado é um membro da playlist especificada.     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | Recupera um valor que indica se os atributos do item de mídia especificado podem ser editados.           |
| [setItemInfo](media-setiteminfo.md)                         | Define o valor do atributo especificado para o item de mídia.                                            |



 

O objeto de **mídia** é acessado por meio das propriedades e métodos a seguir.



| Objeto                          | Propriedade ou método                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Controles](controls-object.md) | [currentItem](controls-currentitem.md)                                  |
| [Jogador](player-object.md)     | [currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md) |
| [Playlist](playlist-object.md) | [item](playlist-item.md)                                                |



 

Porque é o meio mais comum de acesso, *Player*. **currentMedia** é usado para fins de ilustração nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




