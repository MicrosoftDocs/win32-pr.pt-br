---
title: Objeto ErrorItem
description: O objeto ErrorItem fornece uma maneira de acessar informações de erro.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Windows Media Player de objeto ErrorItem
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 533a9144ca5be7de4881d59486aaa928c4b693b851280a2d6b5fd27c344ea018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837965"
---
# <a name="erroritem-object"></a>Objeto ErrorItem

O objeto **ErrorItem** fornece uma maneira de acessar informações de erro.

O objeto **ErrorItem** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [condition](erroritem-condition.md)               | Recupera um valor que indica a condição do erro.                                       |
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

 

 




