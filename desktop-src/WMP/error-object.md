---
title: Objeto de erro (SDK do WMP)
description: O objeto Error fornece acesso a uma coleção de objetos ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Objeto de erro do Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2019
ms.locfileid: "105763352"
---
# <a name="error-object"></a>Objeto Error

O objeto **Error** fornece acesso a uma coleção de objetos [ErrorItem](erroritem-object.md) .

O objeto de **erro** dá suporte à propriedade a seguir.



| Propriedade                           | Descrição                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Recupera o número de erros na fila de erros. |



 

O objeto de **erro** dá suporte aos métodos a seguir.



| Método                                       | Descrição                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Limpa os erros da fila de erros.                                                         |
| [item](error-item.md)                       | Recupera um objeto [ErrorItem](erroritem-object.md) da fila de erros.                     |
| [Webhelp](error-webhelp.md)                 | Inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o erro. |



 

O objeto de **erro** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                  |
|-----------------------------|---------------------------|
| [Jogador](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




