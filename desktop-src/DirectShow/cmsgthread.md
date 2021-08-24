---
description: A classe CMsgThread é uma classe de thread de trabalho que enfileira solicitações para o thread de enfileiramento para conclusão de forma assíncrona.
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
ms.openlocfilehash: 021683808900a7265f4708dae0bb29ff6d07f6619430ed5687eb77d5e2332a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813696"
---
# <a name="cmsgthread-class"></a>Classe CMsgThread

A classe é uma classe worker-thread que enfileira solicitações para o `CMsgThread` thread de enfileiramento para conclusão de forma assíncrona. Para usar essa classe, derive sua classe dela e substitua a função membro [**CMsgThread::ThreadMessageProc.**](cmsgthread-threadmessageproc.md) A **função membro ThreadMessageProc** executa cada solicitação. Suas funções de cliente e a função membro **ThreadMessageProc** devem compartilhar uma definição comum dos parâmetros no [**objeto CMsg.**](cmsg.md)

Um mecanismo negociado informa ao thread de trabalho para sair. Normalmente, esse será um valor do código de mensagem [**uMsg**](cmsg.md) da classe **CMsg.**

É uma boa ideia enviar essa mensagem do destruidor da classe derivada e chamar a função de membro [**CMsgThread::WaitForThreadExit**](cmsgthread-waitforthreadexit.md) antes de concluir a destruição da classe derivada.



| Membros de Dados Protegidos                                    | Descrição                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | Indica um alça usado para sinalização.                                                                                                |
| bloqueio \_ m                                                   | Protege o acesso a listas.                                                                                                             |
| m \_ lWaiting                                               | Indica a espera de um thread livre.                                                                                                  |
| m \_ ThreadQueue                                            | Substitui a [**função membro CMsgThread::GetThreadMsg**](cmsgthread-getthreadmsg.md) e bloqueia coisas diferentes dessa fila. |
| Funções de membro                                          | Descrição                                                                                                                           |
| [**Cmsgthread**](cmsgthread-cmsgthread.md)               | Constrói **um objeto CMsgThread.**                                                                                                   |
| [**Createthread**](cmsgthread-createthread.md)           | Cria um thread.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Recupera o alça de thread.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Recupera o identificador do thread.                                                                                               |
| [**Getthreadpriority**](cmsgthread-getthreadpriority.md) | Recupera a prioridade de thread atual.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Enfileiro uma solicitação de execução pelo thread de trabalho.                                                                                  |
| [**Resumethread**](cmsgthread-resumethread.md)           | Continua a operação do thread de trabalho.                                                                                         |
| [**Setthreadpriority**](cmsgthread-setthreadpriority.md) | Define a prioridade do thread para um novo valor.                                                                                       |
| [**Suspendthread**](cmsgthread-suspendthread.md)         | Suspende a operação de um thread em execução.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Bloqueia até que o thread saia após uma chamada para a função de membro [**CMsgThread::SuspendThread.**](cmsgthread-suspendthread.md) |
| Funções de membro que podem ser substituídos                              | Descrição                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Recupera um objeto [**CMsg na**](cmsg.md) fila que contém uma solicitação.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Fornece inicialização em um thread.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Processa solicitações. Essa é uma função de membro virtual pura.                                                                           |



 

 

 



