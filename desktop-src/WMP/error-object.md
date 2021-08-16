---
title: Objeto de erro (SDK do WMP)
description: O objeto Error fornece acesso a uma coleção de objetos ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Windows Media Player de objeto de erro
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748465"
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
| [Webhelp](error-webhelp.md)                 | inicia a página de ajuda da Web Windows Media Player para exibir mais informações sobre o erro. |



 

O objeto de **erro** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                  |
|-----------------------------|---------------------------|
| [Jogador](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




