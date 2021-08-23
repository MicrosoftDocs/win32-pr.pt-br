---
title: Objeto MetadataPicture
description: O objeto MetadataPicture fornece uma maneira de recuperar os valores do atributo de metadados WM/Picture. Esse atributo corresponde à arte do álbum contida em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Objeto MetadataPicture Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996206"
---
# <a name="metadatapicture-object"></a>Objeto MetadataPicture

O **objeto MetadataPicture** fornece uma maneira de recuperar os valores do atributo de metadados [**WM/Picture.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) Esse atributo corresponde à arte do álbum contida em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.

O **objeto MetadataPicture** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**Descrição**](metadatapicture-description.md) | Recupera uma descrição da imagem de metadados.    |
| [**Tipo MIME**](metadatapicture-mimetype.md)       | Recupera o tipo MIME da imagem de metadados.    |
| [**pictureType**](metadatapicture-picturetype.md) | Recupera o tipo de imagem da imagem de metadados. |
| [**URL**](metadatapicture-url.md)                 | Somente para uso interno.                                |



 

O **objeto MetadataPicture** é acessado por meio do método a seguir.



| Objeto                        | Método                                               |
|-------------------------------|------------------------------------------------------|
| [**Mídia**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

Para fins de ilustração, `player.currentMedia.getItemInfoByType(name, language, index)` é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 