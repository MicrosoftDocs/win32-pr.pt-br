---
description: Os comandos adiados são enfileirados por chamadas para métodos na interface IQueueCommand e são expostos pelo Gerenciador de gráfico de filtro e por alguns filtros.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: Classe CDeferredCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d3db3f35b5589a6cd17791d72aa9931124ccfbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087866"
---
# <a name="cdeferredcommand-class"></a>Classe CDeferredCommand

![hierarquia de classe cdeferredcommand](images/cutil13.png)

Os comandos adiados são enfileirados por chamadas para métodos na interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) e são expostos pelo Gerenciador de gráfico de filtro e por alguns filtros. Uma chamada bem-sucedida para um desses métodos retorna uma interface [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) que representa o comando enfileirado.

Um `CDeferredCommand` objeto representa um único comando adiado e expõe a interface [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) , bem como outros métodos que permitem verificações de tempo e execução real. Um `CDeferredCommand` objeto contém uma referência ao objeto [**CCmdQueue**](ccmdqueue.md) no qual ele está na fila.

As contagens de referência controlam o tempo de vida da `CDeferredCommand` classe. Ao chamar a função de membro [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) , o aplicativo de chamada Obtém um ponteiro de interface que é contado por referência e o objeto [**CCmdQueue**](ccmdqueue.md) também mantém uma contagem de referência no comando adiado. Chamar a função de membro [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) usa o comando adiado da fila de comandos e, portanto, reduz a contagem de referência em um. Após a retirada da fila, o comando não pode ser colocado de volta na fila.



| Membros de Dados Protegidos                                        | Descrição                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| \_bStream m                                                    | Sinalizador para tempo de [**fluxo**](stream-time.md) ou de apresentação. a ser passado para o método invocado.                   |
| expedição de m \_                                                   | Acessa a interface **ITypeInfo** .                                                                                   |
| \_dispidMethod m                                               | O método na interface a ser executado.                                                                                         |
| \_DispParams m                                                 | Objeto [**CDispParams**](cdispparams.md) que contém a lista de parâmetros **DISPPARAMS**                                  |
| \_hrResult m                                                   | Armazena o valor **HRESULT** retornado.                                                                                  |
| \_IID m                                                        | **GUID**(identificador global exclusivo) da interface.                                                                 |
| \_pQueue m                                                     | Ponteiro para o objeto [**CCmdQueue**](ccmdqueue.md) que expõe a interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . |
| \_punk m                                                       | Ponteiro de **IUnknown** para a interface na qual o comando será executado.                                                 |
| \_pVarResult m                                                 | Informações resultantes, se houver, do método invocado.                                                                 |
| \_tempo m                                                       | Hora em que o comando será executado.                                                                                  |
| \_wFlags m                                                     | Sinalizadores que especificam o contexto da invocação.                                                                         |
| Funções de membro                                              | Descrição                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Constrói um objeto **CDeferredCommand** .                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Recupera os sinalizadores de contexto associados ao comando adiado.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Recupera o identificador de interface (IID) da interface na qual o método será executado.                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | Recupera o identificador de expedição do método a ser executado.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Recupera a lista de argumentos **DISPPARAMS** para o método.                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Recupera a lista de argumentos resultantes, se houver.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Recupera a hora em que o método será executado.                                                                         |
| [**Chame**](cdeferredcommand-invoke.md)                     | Fornece acesso a métodos e propriedades expostas por um objeto.                                                         |
| [**Isstreamtime**](cdeferredcommand-isstreamtime.md)         | Especifica se o comando deve ser executado no momento do fluxo ou na hora da apresentação.                                         |
| Métodos IDeferredCommand                                      | Descrição                                                                                                             |
| [**Cancelar**](cdeferredcommand-cancel.md)                     | Cancela uma solicitação [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) enfileirada anteriormente.                        |
| [**Confiança**](cdeferredcommand-confidence.md)             | Não implementado atualmente.                                                                                              |
| [**Adiar**](cdeferredcommand-postpone.md)                 | Especifica um novo tempo de apresentação para um comando anteriormente enfileirado.                                                      |
| [**Gethresult**](cdeferredcommand-gethresult.md)             | Recupera o valor **HRESULT** do método invocado.                                                                  |



 

 

 



