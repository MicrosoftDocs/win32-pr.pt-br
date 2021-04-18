---
title: Objeto ErrorItem
description: O objeto ErrorItem fornece uma maneira de acessar informações de erro.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Objeto ErrorItem Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105788167"
---
# <a name="erroritem-object"></a>Objeto ErrorItem

O objeto **ErrorItem** fornece uma maneira de acessar informações de erro.

O objeto **ErrorItem** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [problema](erroritem-condition.md)               | Recupera um valor que indica a condição do erro.                                       |
| [customUrl](erroritem-customurl.md)               | Recupera a URL de um site que exibe informações específicas sobre a falha de download do codec. |
| [errorCode](erroritem-errorcode.md)               | Recupera o código de erro atual.                                                               |
| [errorContext](erroritem-errorcontext.md)         | Recupera um valor que indica o contexto do erro.                                          |
| [errorDescription](erroritem-errordescription.md) | Recupera uma descrição do erro.                                                           |
| **soluciona**                                         | Reservado para uso futuro.                                                                        |



 

O objeto **ErrorItem** é acessado por meio dos métodos a seguir.



| Objeto                    | Método                   |
|---------------------------|--------------------------|
| [Erro](error-object.md) | [item](error-item.md)   |
| [Mídia](media-object.md) | [error](media-error.md) |



 

Para fins de ilustração, *Player*. *erro*. *Item*(*índice*) é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




