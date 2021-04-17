---
description: As portas de conclusão de e/s fornecem um modelo de Threading eficiente para processar várias solicitações de e/s assíncronas em um sistema multiprocessador.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Portas de conclusão de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882363ef99821a0b0b40810f45d609c5b5f7760c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769354"
---
# <a name="io-completion-ports"></a>Portas de conclusão de e/s

As portas de conclusão de e/s fornecem um modelo de Threading eficiente para processar várias solicitações de e/s assíncronas em um sistema multiprocessador. Quando um processo cria uma porta de conclusão de e/s, o sistema cria um objeto de fila associado para solicitações cujo único propósito é atender a essas solicitações. Processos que lidam com muitas solicitações simultâneas de e/s assíncronas podem fazer isso com mais rapidez e eficiência usando portas de conclusão de e/s em conjunto com um pool de threads pré-alocado do que criar threads no momento em que recebem uma solicitação de e/s.

## <a name="how-io-completion-ports-work"></a>Como funcionam as portas de conclusão de e/s

A função [**CreateIoCompletionPort**](createiocompletionport.md) cria uma porta de conclusão de e/s e associa um ou mais identificadores de arquivo a essa porta. Quando uma operação de e/s assíncrona em um desses identificadores de arquivo é concluída, um pacote de conclusão de e/s é enfileirado na ordem FIFO (primeiro a entrar, primeiro a sair) para a porta de conclusão de e/s associada. Um uso poderoso para esse mecanismo é combinar o ponto de sincronização para vários identificadores de arquivo em um único objeto, embora também haja outros aplicativos úteis. Observe que, enquanto os pacotes são enfileirados na ordem FIFO, eles podem ser recolocados na fila em uma ordem diferente.

> [!Note]
>
> O termo *identificador de arquivo* conforme usado aqui refere-se a uma abstração de sistema que representa um ponto de extremidade de e/s sobreposto, não apenas um arquivo no disco. Por exemplo, ele pode ser um ponto de extremidade de rede, soquete TCP, pipe nomeado ou slot de correio. Qualquer objeto do sistema que dê suporte a e/s sobreposta pode ser usado. Para obter uma lista de funções de e/s relacionadas, consulte o final deste tópico.

 

Quando um identificador de arquivo é associado a uma porta de conclusão, o bloco de status transmitido não será atualizado até que o pacote seja removido da porta de conclusão. A única exceção é se a operação original retornar de forma síncrona com um erro. Um thread (criado pelo thread principal ou o próprio thread principal) usa a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para aguardar que um pacote de conclusão seja colocado na fila para a porta de conclusão de e/s, em vez de aguardar diretamente a conclusão da e/s assíncrona. Os threads que bloqueiam a execução em uma porta de conclusão de e/s são liberados na ordem UEPS (último a entrar, primeiro a sair) e o próximo pacote de conclusão é extraído da fila FIFO da porta de conclusão de e/s para esse thread. Isso significa que, quando um pacote de conclusão é liberado para um thread, o sistema libera o último thread (mais recente) associado a essa porta, passando as informações de conclusão para a conclusão de e/s mais antiga.

Embora qualquer número de threads possa chamar [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para uma porta de conclusão de e/s especificada, quando um thread especificado chama **GetQueuedCompletionStatus** na primeira vez, ele se torna associado à porta de conclusão de e/s especificada até que uma das três coisas ocorra: o thread sai, especifica uma porta de conclusão de e/s diferente ou fecha a porta de conclusão de e/s. Em outras palavras, um único thread pode ser associado a, no máximo, uma porta de conclusão de e/s.

Quando um pacote de conclusão é enfileirado para uma porta de conclusão de e/s, o sistema verifica primeiro quantos threads associados a essa porta estão em execução. Se o número de threads em execução for menor que o valor de simultaneidade (discutido na próxima seção), um dos threads em espera (o mais recente) tem permissão para processar o pacote de conclusão. Quando um thread em execução conclui seu processamento, ele normalmente chama [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) novamente, no ponto em que ele retorna com o próximo pacote de conclusão ou aguarda se a fila está vazia.

Os threads podem usar a função [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) para colocar os pacotes de conclusão em uma fila da porta de conclusão de e/s. Ao fazer isso, a porta de conclusão pode ser usada para receber comunicações de outros threads do processo, além de receber pacotes de conclusão de e/s do sistema de e/s. A função **PostQueuedCompletionStatus** permite que um aplicativo enfileirar seus próprios pacotes de conclusão de finalidade especial para a porta de conclusão de e/s sem iniciar uma operação de e/s assíncrona. Isso é útil para notificar threads de trabalho de eventos externos, por exemplo.

O identificador de porta de conclusão de e/s e todos os identificadores de arquivo associados a essa porta de conclusão de e/s específica são conhecidos como *referências à porta de conclusão de e/s*. A porta de conclusão de e/s é liberada quando não há mais referências a ela. Portanto, todos esses identificadores devem ser fechados corretamente para liberar a porta de conclusão de e/s e seus recursos de sistema associados. Depois que essas condições forem satisfeitas, um aplicativo deverá fechar o identificador da porta de conclusão de e/s chamando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

> [!Note]
>
> Uma porta de conclusão de e/s é associada ao processo que a criou e não é compartilhável entre processos. No entanto, um único identificador é compartilhável entre threads no mesmo processo.

 

## <a name="threads-and-concurrency"></a>Threads e simultaneidade

A propriedade mais importante de uma porta de conclusão de e/s a ser considerada cuidadosamente é o valor de simultaneidade. O valor de simultaneidade de uma porta de conclusão é especificado quando é criado com [**CreateIoCompletionPort**](createiocompletionport.md) por meio do parâmetro *NumberOfConcurrentThreads* . Esse valor limita o número de threads executáveis associados à porta de conclusão. Quando o número total de threads executáveis associados à porta de conclusão atingir o valor de simultaneidade, o sistema bloqueará a execução de quaisquer threads subsequentes associados a essa porta de conclusão até que o número de threads executáveis fique abaixo do valor de simultaneidade.

O cenário mais eficiente ocorre quando há pacotes de conclusão aguardando na fila, mas nenhuma espera pode ser satisfeita porque a porta atingiu seu limite de simultaneidade. Considere o que acontece com um valor de simultaneidade de um e vários threads aguardando na chamada de função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Nesse caso, se a fila sempre tiver pacotes de conclusão aguardando, quando o thread em execução chamar **GetQueuedCompletionStatus**, ele não bloqueará a execução porque, como mencionado anteriormente, a fila de threads será UEPS. Em vez disso, esse thread irá selecionar imediatamente o próximo pacote de conclusão na fila. Nenhuma alternância de contexto de thread ocorrerá, pois o thread em execução está continuamente selecionando pacotes de conclusão e os outros threads não podem ser executados.

> [!Note]
>
> No exemplo anterior, os threads extras parecem ser inúteis e nunca são executados, mas isso pressupõe que o thread em execução nunca é colocado em um estado de espera por algum outro mecanismo, termina ou fecha sua porta de conclusão de e/s associada. Considere todas essas ramificações de execução de thread ao projetar o aplicativo.

 

O melhor valor geral máximo a ser escolhido para o valor de simultaneidade é o número de CPUs no computador. Se sua transação exigir uma computação demorada, um valor de simultaneidade maior permitirá a execução de mais threads. Cada pacote de conclusão pode levar mais tempo para ser concluído, mas os pacotes de conclusão serão processados ao mesmo tempo. Você pode experimentar o valor de simultaneidade em conjunto com as ferramentas de criação de perfil para obter o melhor efeito para seu aplicativo.

O sistema também permite que um thread esperando em [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) processe um pacote de conclusão se outro thread em execução associado à mesma porta de conclusão de e/s entrar em um estado de espera por outros motivos, por exemplo, a função [**SuspendThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) . Quando o thread no estado de espera começar a ser executado novamente, poderá haver um breve período quando o número de threads ativos exceder o valor de simultaneidade. No entanto, o sistema reduz rapidamente esse número, não permitindo novos threads ativos até que o número de threads ativos esteja abaixo do valor de simultaneidade. Essa é uma razão para que seu aplicativo crie mais threads em seu pool de threads do que o valor de simultaneidade. O gerenciamento de pool de threads está além do escopo deste tópico, mas uma boa regra prática é ter, no mínimo, o dobro de threads no pool de threads, pois há processadores no sistema. Para obter informações adicionais sobre o pool de threads, consulte [pools de threads](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Funções de e/s com suporte

As funções a seguir podem ser usadas para iniciar operações de e/s que são concluídas usando portas de conclusão de e/s. Você deve passar a função de uma instância da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e um identificador de arquivo associado anteriormente a uma porta de conclusão de e/s (por uma chamada para [**CreateIoCompletionPort**](createiocompletionport.md)) para habilitar o mecanismo de porta de conclusão de e/s:

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**WSASend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[Sobre Processos e Threads](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
