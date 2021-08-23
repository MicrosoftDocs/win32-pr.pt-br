---
description: 'Várias opções estão disponíveis para receber indicações de conclusão, fornecendo, assim, aos aplicativos níveis apropriados de flexibilidade. Isso inclui: espera (ou bloqueio) em objetos de evento, sondagem de objetos de evento e rotinas de conclusão de E/S de soquete.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Recebendo indicações de conclusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0ea3d46707eb31d803362f327c309d3c9d948812c0eb3a810e31b896e895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569246"
---
# <a name="receiving-completion-indications"></a>Recebendo indicações de conclusão

Várias opções estão disponíveis para receber indicações de conclusão, fornecendo, assim, aos aplicativos níveis apropriados de flexibilidade. Isso inclui: espera (ou bloqueio) em objetos de evento, sondagem de objetos de evento e rotinas de conclusão de E/S de soquete.

## <a name="blocking-and-waiting-for-completion-indication"></a>Bloqueando e aguardando indicação de conclusão

Os aplicativos podem ser bloqueados enquanto aguardam que um ou mais objetos de evento se tornem definidos usando a [**função WSAWaitForMultipleEvents.**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) Em Windows implementações, o processo ou thread realmente bloqueia. Como Windows objetos de evento sockets 2 são implementados como eventos Windows, a função Windows nativa, [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) também pode ser usada para essa finalidade. Isso é especialmente útil se o thread precisar aguardar eventos soquetes e nãoocket.

## <a name="polling-for-completion-indication"></a>Sondagem para indicação de conclusão

Aplicativos que preferem não bloquear podem usar a [**função WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para sondar o status de conclusão associado a qualquer objeto de evento específico. Essa função indica se a operação sobreexplorada foi concluída ou não e, se concluída, organiza a [**função WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) para recuperar o status de erro da operação sobrecodada.

## <a name="using-socket-io-completion-routines"></a>Usando rotinas de conclusão de E/S de soquete

As funções usadas para iniciar E/S sobrecarrecada ( [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSASendTo,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) todas levam *lpCompletionRoutine* como um parâmetro de entrada opcional. Esse é um ponteiro para uma função específica do aplicativo que é chamada após a conclusão de uma operação de E/S sobressalada iniciada com êxito (com êxito ou de outra forma). A rotina de conclusão segue as mesmas regras que o estipulado para Windows de conclusão de E/S de arquivo. Ou seja, a rotina de conclusão não é invocada até que o thread está em um estado de espera alertável, como quando a função [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) é invocada com o sinalizador `fAlertable` definido. Um aplicativo que usa a opção de rotina de conclusão para uma solicitação de E/S sobressaltada específica pode não usar a opção de espera [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para essa mesma solicitação de E/S sobressaltada.

Os transportes permitem que um aplicativo invoque operações de envio e recebimento de dentro do contexto da rotina de conclusão de E/S de soquete e garanta que, para um determinado soquete, as rotinas de conclusão de E/S não serão aninhadas. Isso permite que transmissões de dados sensíveis ao tempo ocorram inteiramente dentro de um contexto preemptivo.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Resumo dos mecanismos de indicação de conclusão sobressalo

A indicação de conclusão de E/S sobressaltada específica a ser usada para uma determinada operação sobrecarnada é determinada por se o aplicativo fornece um ponteiro para uma função de conclusão, se uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) é referenciada e pelo valor do membro **hEvent** dentro da estrutura **WSAOVERLAPPED** (se fornecida). A tabela a seguir resume a semântica de conclusão para um soquete sobressalo e mostra as várias combinações de *lpOverlapped,* **hEvent** e *lpCompletionRoutine:*

| *Lpoverlapped* | Hevent         | *Lpcompletionroutine* | Indicação de conclusão                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULO           | Não se aplica | Ignored               | A operação é concluída de forma síncrona. Ele se comporta como se fosse um soquete não mapeado.                                                                                                                                      |
| ! Null          | NULO           | NULO                  | A operação é concluída sobrecarro, mas não há Windows mecanismo de conclusão com suporte para Soquetes 2. O mecanismo de porta de conclusão (se tiver suporte) pode ser usado nesse caso. Caso contrário, não haverá nenhuma notificação de conclusão. |
| ! Null          | ! Null          | NULO                  | A operação é concluída sobrecarrada, notificação sinalizando o objeto de evento.                                                                                                                                                  |
| ! Null          | Ignored        | ! Null                 | A operação é concluída sobrecarrada, notificação agendando a rotina de conclusão.                                                                                                                                           |



 

 

 
