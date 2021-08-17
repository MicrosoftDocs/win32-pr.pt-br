---
title: Objeto MetadataText
description: O objeto MetadataText fornece uma maneira de recuperar metadados para atributos de metadados textuais complexos.
ms.assetid: cf8e4524-6fc5-4534-9542-6bdc7d34bca4
keywords:
- Objeto MetadataText Windows Media Player
topic_type:
- apiref
api_name:
- MetadataText Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f79c4f4bb80855cf84d576c126e30dc5301c45ca6f1a7c34c5d54e57844abfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135019"
---
# <a name="metadatatext-object"></a>Objeto MetadataText

O **objeto MetadataText** fornece uma maneira de recuperar metadados para atributos de metadados textuais complexos.

O **objeto MetadataText** dá suporte às propriedades a seguir.



| Propriedade                                    | Descrição                                   |
|---------------------------------------------|-----------------------------------------------|
| [descrição](metadatatext-description.md) | Recupera uma descrição do texto de metadados. |
| [text](metadatatext-text.md)               | Recupera o texto de metadados.                  |



 

O **objeto MetadataText** é acessado por meio do método a seguir.



| Objeto                    | Método                                           |
|---------------------------|--------------------------------------------------|
| [Mídia](media-object.md) | [getItemInfoByType](media-getiteminfobytype.md) |



 

Para fins de ilustração, *player*. *currentMedia*. **getItemInfoByType**(*name*, *language*, *index*) é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




