---
title: Objeto MetadataPicture
description: O objeto MetadataPicture fornece uma maneira de recuperar os valores do atributo de metadados do WM/Picture. Esse atributo corresponde à arte do álbum contida em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.
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
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454269"
---
# <a name="metadatapicture-object"></a>Objeto MetadataPicture

O objeto **MetadataPicture** fornece uma maneira de recuperar os valores do atributo de metadados do [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) . Esse atributo corresponde à arte do álbum contida em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.

O objeto **MetadataPicture** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**ndescrição**](metadatapicture-description.md) | Recupera uma descrição da imagem de metadados.    |
| [**MIME**](metadatapicture-mimetype.md)       | Recupera o tipo MIME da imagem de metadados.    |
| [**TipoDeFigura**](metadatapicture-picturetype.md) | Recupera o tipo de imagem da imagem de metadados. |
| [**URL**](metadatapicture-url.md)                 | Somente para uso interno.                                |



 

O objeto **MetadataPicture** é acessado por meio do método a seguir.



| Objeto                        | Método                                               |
|-------------------------------|------------------------------------------------------|
| [**Mídia**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

Para fins de ilustração, `player.currentMedia.getItemInfoByType(name, language, index)` é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 