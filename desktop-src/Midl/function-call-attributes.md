---
title: Atributos de chamada de função
description: Os programas podem usar esses atributos em funções individuais dentro da interface e afetar apenas essa função.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- MIDL, atributos, chamada de função IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637096"
---
# <a name="function-call-attributes"></a>Atributos de chamada de função

Os programas podem usar esses atributos em funções individuais dentro da interface e afetar apenas essa função.



| Atributo                        | Uso                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mensagem**](message.md)       | A chamada de procedimento remoto deve ser tratada como uma mensagem assíncrona do cliente para o servidor. O cliente faz a chamada e retorna imediatamente, enquanto a chamada real é tratada pelo [**ncadg \_ MQ**](ncadg-mq.md)(transporte de enfileiramento de mensagens). |
| [**Eu**](maybe.md)           | O cliente que faz essa chamada de procedimento remoto não espera nenhuma resposta indicando a entrega ou a conclusão da chamada. Isso está em contraste com as operações de [**mensagem**](message.md) em que nenhuma resposta é esperada, mas a entrega é garantida.        |
| [**difusor**](broadcast.md)   | A chamada de procedimento remoto deve ser enviada a todos os servidores na rede. O cliente aceita o primeiro retorno, as respostas subsequentes de outros servidores são descartadas.                                                                                    |
| [**idempotente**](idempotent.md) | A chamada não altera o estado e retorna as mesmas informações cada vez que é chamada com os mesmos parâmetros de entrada.                                                                                                                                     |
| [**retorno de chamada**](callback.md)     | Designa uma função que reside no aplicativo cliente, que o servidor pode chamar para obter informações do cliente.                                                                                                                             |
| [**chamar \_ como**](call-as.md)      | Mapeia uma função não Remotable para uma chamada de procedimento remoto.                                                                                                                                                                                                   |
| [**local**](local.md)           | Designa um procedimento local para o qual MIDL não gere código stub.                                                                                                                                                                                   |



 

Em interfaces que não são de [**objeto**](object.md) , você também pode aplicar o atributo de [**\_ identificador de contexto**](context-handle.md) a uma função para especificar características do valor de retorno.

 

 




