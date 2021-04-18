---
description: 'Várias opções estão disponíveis para receber indicações de conclusão, fornecendo assim aplicativos com níveis apropriados de flexibilidade. Isso inclui: aguardando (ou bloqueando) em objetos de evento, objetos de evento de sondagem e rotinas de conclusão de e/s de soquete.'
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Indicações de conclusão de recebimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd05d8297af17c26393b5db113fac283b39fcbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771617"
---
# <a name="receiving-completion-indications"></a>Indicações de conclusão de recebimento

Várias opções estão disponíveis para receber indicações de conclusão, fornecendo assim aplicativos com níveis apropriados de flexibilidade. Isso inclui: aguardando (ou bloqueando) em objetos de evento, objetos de evento de sondagem e rotinas de conclusão de e/s de soquete.

## <a name="blocking-and-waiting-for-completion-indication"></a>Bloqueando e aguardando indicação de conclusão

Os aplicativos podem ser bloqueados enquanto aguardam a definição de um ou mais objetos de evento usando a função [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) . Em implementações do Windows, o processo ou thread realmente bloqueia. Como os objetos de evento do Windows Sockets 2 são implementados como eventos do Windows, a função nativa do Windows, [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) também pode ser usada para essa finalidade. Isso é especialmente útil se o thread precisar aguardar em eventos de soquete e não soquete.

## <a name="polling-for-completion-indication"></a>Sondando a indicação de conclusão

Aplicativos que preferem não bloquear podem usar a função [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para sondar o status de conclusão associado a qualquer objeto de evento específico. Essa função indica se a operação sobreposta foi concluída e, se for concluída, organiza a função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) para recuperar o status de erro da operação sobreposta.

## <a name="using-socket-io-completion-routines"></a>Usando rotinas de conclusão de e/s de soquete

As funções usadas para iniciar e/s sobreposta ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) têm *lpCompletionRoutine* como um parâmetro de entrada opcional. Este é um ponteiro para uma função específica do aplicativo que é chamada após a conclusão bem-sucedida da operação de e/s sobreposta (com êxito ou de outra forma). A rotina de conclusão segue as mesmas regras que estipuladas para rotinas de conclusão de e/s de arquivo do Windows. Ou seja, a rotina de conclusão não é invocada até que o thread esteja em um estado de espera alertável, como quando a função [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) é invocada com o `fAlertable` sinalizador definido. Um aplicativo que usa a opção de rotina de conclusão para uma determinada solicitação de e/s sobreposta pode não usar a opção de espera de [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) para essa mesma solicitação de e/s sobreposta.

Os transportes permitem que um aplicativo invoque operações de envio e recebimento de dentro do contexto da rotina de conclusão de e/s de soquete e garante que, para um determinado soquete, as rotinas de conclusão de e/s não serão aninhadas. Isso permite que as transmissões de dados sensíveis ao tempo ocorram inteiramente dentro de um contexto Preemptive.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Resumo dos mecanismos de indicação de conclusão sobreposta

A determinada indicação de conclusão de e/s sobreposta a ser usada para uma determinada operação sobreposta é determinada pelo fato de o aplicativo fornecer um ponteiro para uma função de conclusão, se uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) é referenciada e pelo valor do membro **hEvent** dentro da estrutura **WSAOVERLAPPED** (se fornecida). A tabela a seguir resume a semântica de conclusão para um Soquete sobreposto e mostra as várias combinações de *lpOverlapped*, **hEvent** e *lpCompletionRoutine*:

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | Indicação de conclusão                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULO           | Não aplicável | Ignored               | A operação é concluída de forma síncrona. Ele se comporta como se fosse um soquete não sobreposto.                                                                                                                                      |
| ! NULO          | NULO           | NULO                  | A operação é concluída sobreposta, mas não há nenhum mecanismo de conclusão com suporte do Windows Sockets 2. O mecanismo de porta de conclusão (se houver suporte) pode ser usado nesse caso. Caso contrário, não haverá nenhuma notificação de conclusão. |
| ! NULO          | ! NULO          | NULO                  | A operação é concluída sobreposta, notificação por objeto de evento de sinalização.                                                                                                                                                  |
| ! NULO          | Ignored        | ! NULO                 | A operação é concluída sobreposta, notificação pela rotina de conclusão do agendamento.                                                                                                                                           |



 

 

 
