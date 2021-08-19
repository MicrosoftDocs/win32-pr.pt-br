---
title: Atributos assíncronos
description: Quando um programa invoca um procedimento em uma interface, o procedimento pode ser executado de forma síncrona ou assíncrona.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- IDL MIDL, atributos MIDL, assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14ad045be5c3f5980c99fac0e924181c31ae7859f801608c7bb53fe3d81a2b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807849"
---
# <a name="asynchronous-attributes"></a>Atributos assíncronos

Quando um programa invoca um procedimento em uma interface, o procedimento pode ser executado de forma síncrona ou assíncrona. Um procedimento síncrono faz com que o programa de chamada aguarde até que o procedimento retorne antes que o programa possa continuar. Um procedimento assíncrono retorna imediatamente sem aguardar os resultados. O programa de chamada deve ser ressincronizado posteriormente com o procedimento de interface para receber dados. Para obter mais informações, consulte [RPC assíncrono.](/windows/desktop/Rpc/asynchronous-rpc)

Você pode usar os atributos a seguir para dar suporte a chamadas de procedimento remoto assíncrono.



| Atributo                         | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)            | Quando aplicado a um parâmetro de função, define um alça que permite que o chamador faça uma chamada assíncrona e retorne imediatamente sem aguardar os resultados e, posteriormente, ressincronize com a função chamada para receber dados após a conclusão da chamada. O [**atributo assíncrono**](async.md) também é usado em arquivos ACF para definir um alçamento assíncrono para um procedimento ou uma interface inteira. Para interfaces COM, essa interface é obsoleta e não pode ser usada para novas interfaces. |
| [**async \_ uuid**](async-uuid.md) | Direciona o compilador MIDL para definir versões síncronas e assíncronas de uma interface COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Talvez**](maybe.md)            | O cliente que está fazendo essa chamada de procedimento remoto não espera nenhuma resposta indicando entrega ou conclusão da chamada, e a entrega não é garantida. Isso é diferente das operações **de mensagem** em que nenhuma resposta é esperada, mas a entrega é garantida.                                                                                                                                                                                                                    |
| [**Mensagem**](message.md)        | A chamada de procedimento remoto deve ser tratada como uma mensagem assíncrona do cliente para o servidor. O cliente faz a chamada e retorna imediatamente, enquanto a chamada real é manipulada pelo transporte na fila de mensagens ([**ncadg \_ mq**](ncadg-mq.md)).                                                                                                                                                                                                                              |



 

 

 