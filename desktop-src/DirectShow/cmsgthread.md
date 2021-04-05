---
description: A classe CMsgThread é uma classe de thread de trabalho que enfileira solicitações para o thread de enfileiramento para conclusão assíncrona.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: Classe CMsgThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 307b24e1563fe0545ee6f9405f9fb53e1b6d61b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646162"
---
# <a name="cmsgthread-class"></a>Classe CMsgThread

A `CMsgThread` classe é uma classe de thread de trabalho que enfileira solicitações para o thread de enfileiramento para conclusão assíncrona. Para usar essa classe, derive sua classe a partir dela e substitua a função membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) . A função membro **ThreadMessageProc** executa cada solicitação. As funções de cliente e a função de membro **ThreadMessageProc** devem compartilhar uma definição comum dos parâmetros no objeto [**CMsg**](cmsg.md) .

Um mecanismo negociado informa o thread de trabalho para sair. Normalmente, esse será um valor do código de mensagem **uMsg** da classe [**CMsg**](cmsg.md) .

É uma boa ideia enviar essa mensagem do destruidor de sua classe derivada e chamar a função de membro [**CMsgThread:: WaitForThreadExit**](cmsgthread-waitforthreadexit.md) antes de concluir a destruição da classe derivada.



| Membros de Dados Protegidos                                    | Descrição                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| \_hSem m                                                   | Indica um identificador usado para sinalização.                                                                                                |
| bloqueio de m \_                                                   | Protege o acesso a listas.                                                                                                             |
| \_lWaiting m                                               | Indica aguardar um thread gratuito.                                                                                                  |
| \_ThreadQueue m                                            | Substitui a função de membro [**CMsgThread:: GetThreadMsg**](cmsgthread-getthreadmsg.md) e os blocos em coisas diferentes dessa fila. |
| Funções de membro                                          | Descrição                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Constrói um objeto **CMsgThread** .                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Cria um thread.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Recupera o identificador de thread.                                                                                                          |
| [**GetThreadId**](cmsgthread-getthreadid.md)             | Recupera o identificador do thread.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Recupera a prioridade de thread atual.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Enfileira uma solicitação de execução pelo thread de trabalho.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Continua a operação do thread de trabalho.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Define a prioridade do thread para um novo valor.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Suspende a operação de um thread em execução.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Bloqueia até que o thread seja encerrado após uma chamada para a função de membro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) . |
| Funções de membro substituíveis                              | Descrição                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Recupera um objeto [**CMsg**](cmsg.md) enfileirado que contém uma solicitação.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Fornece inicialização em um thread.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Processa solicitações. Essa é uma função de membro virtual pura.                                                                           |



 

 

 



