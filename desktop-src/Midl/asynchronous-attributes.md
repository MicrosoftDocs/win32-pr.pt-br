---
title: Atributos assíncronos
description: Quando um programa invoca um procedimento em uma interface, o procedimento pode ser executado de forma síncrona ou assíncrona.
ms.assetid: 3e6c6c13-1524-41b2-96dc-3885eadb847c
keywords:
- MIDL IDL, atributos MIDL, assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aca2276bf1fa5178f1dca3ae4803544066d983
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105751459"
---
# <a name="asynchronous-attributes"></a>Atributos assíncronos

Quando um programa invoca um procedimento em uma interface, o procedimento pode ser executado de forma síncrona ou assíncrona. Um procedimento síncrono faz com que o programa de chamada aguarde até que o procedimento seja retornado antes que o programa possa continuar. Um procedimento assíncrono retorna imediatamente sem esperar por resultados. O programa de chamada deve posteriormente ressincronizar com o procedimento de interface para receber dados. Para obter mais informações, consulte [RPC assíncrono](/windows/desktop/Rpc/asynchronous-rpc).

Você pode usar os atributos a seguir para fornecer suporte para chamadas de procedimento remoto assíncronas.



| Atributo                         | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)            | Quando aplicado a um parâmetro de função, define um identificador que permite que o chamador faça uma chamada assíncrona e retorne imediatamente sem esperar pelos resultados e, posteriormente, Ressincronize com a função chamada para receber dados após a conclusão da chamada. O atributo [**Async**](async.md) também é usado em arquivos ACF para definir um identificador assíncrono para um procedimento ou uma interface inteira. Para interfaces COM, essa interface é obsoleta e não pode ser usada para novas interfaces. |
| [**\_UUID assíncrono**](async-uuid.md) | Direciona o compilador MIDL para definir as versões síncrona e assíncrona de uma interface COM.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Eu**](maybe.md)            | O cliente que faz essa chamada de procedimento remoto não espera nenhuma resposta indicando a entrega ou a conclusão da chamada, e a entrega não é garantida. Isso está em contraste com as operações de **mensagem** em que nenhuma resposta é esperada, mas a entrega é garantida.                                                                                                                                                                                                                    |
| [**Mensagem**](message.md)        | A chamada de procedimento remoto deve ser tratada como uma mensagem assíncrona do cliente para o servidor. O cliente faz a chamada e retorna imediatamente, enquanto a chamada real é tratada pelo [**ncadg \_ MQ**](ncadg-mq.md)(transporte de enfileiramento de mensagens).                                                                                                                                                                                                                              |



 

 

 