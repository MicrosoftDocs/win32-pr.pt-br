---
description: As portas de conclusão de E/S fornecem um modelo de threading eficiente para processar várias solicitações de E/S assíncronas em um sistema multiprocessador.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Portas de conclusão de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2133bb14c661580eaf8004bd92c6f947b3b8777a4b1a5f6b330fe631b2be6c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050826"
---
# <a name="io-completion-ports"></a>Portas de conclusão de E/S

As portas de conclusão de E/S fornecem um modelo de threading eficiente para processar várias solicitações de E/S assíncronas em um sistema multiprocessador. Quando um processo cria uma porta de conclusão de E/S, o sistema cria um objeto de fila associado para solicitações cuja única finalidade é a manutenção dessas solicitações. Processos que lidam com muitas solicitações de E/S assíncronas simultâneas podem fazer isso de forma mais rápida e eficiente usando portas de conclusão de E/S em conjunto com um pool de threads pré-alocado do que criando threads no momento em que recebem uma solicitação de E/S.

## <a name="how-io-completion-ports-work"></a>Como funcionam as portas de conclusão de E/S

A [**função CreateIoCompletionPort**](createiocompletionport.md) cria uma porta de conclusão de E/S e associa um ou mais alças de arquivo a essa porta. Quando uma operação de E/S assíncrona em um desses alçamentos de arquivo é concluída, um pacote de conclusão de E/S é enfocado na ordem FIFO (primeiro a entrar no primeiro a sair) para a porta de conclusão de E/S associada. Um uso poderoso para esse mecanismo é combinar o ponto de sincronização para vários identificador de arquivo em um único objeto, embora também haja outros aplicativos úteis. Observe que, embora os pacotes sejam ensuados na ordem FIFO, eles podem ser ensuados em uma ordem diferente.

> [!Note]
>
> O termo *alça de arquivo,* conforme usado aqui, refere-se a uma abstração do sistema que representa um ponto de extremidade de E/S sobresalo, não apenas um arquivo em disco. Por exemplo, pode ser um ponto de extremidade de rede, soquete TCP, pipe nomeado ou slot de email. Qualquer objeto do sistema que dá suporte a E/S sobressalo pode ser usado. Para ver uma lista de funções de E/S relacionadas, consulte o final deste tópico.

 

Quando um alça de arquivo estiver associado a uma porta de conclusão, o bloco de status passado não será atualizado até que o pacote seja removido da porta de conclusão. A única exceção será se a operação original retornar de forma síncrona com um erro. Um thread (criado pelo thread principal ou pelo próprio thread principal) usa a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para aguardar a conclusão de um pacote de conclusão para a porta de conclusão de E/S, em vez de aguardar diretamente a conclusão da E/S assíncrona. Os threads que bloqueiam sua execução em uma porta de conclusão de E/S são liberados na ordem LIFO (último a entrar primeiro a sair) e o próximo pacote de conclusão é retirado da fila FIFO da porta de conclusão de E/S para esse thread. Isso significa que, quando um pacote de conclusão é liberado para um thread, o sistema libera o último thread (mais recente) associado a essa porta, passando as informações de conclusão para a conclusão de E/S mais antiga.

Embora qualquer número de threads possa chamar [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para uma porta de conclusão de E/S especificada, quando um thread especificado chamar **GetQueuedCompletionStatus** pela primeira vez, ele se tornará associado à porta de conclusão de E/S especificada até que uma das três coisas ocorra: o thread sai, especifica uma porta de conclusão de E/S diferente ou fecha a porta de conclusão de E/S especificada. Em outras palavras, um único thread pode ser associado, no máximo, a uma porta de conclusão de E/S.

Quando um pacote de conclusão é en fila para uma porta de conclusão de E/S, o sistema primeiro verifica quantos threads associados a essa porta estão em execução. Se o número de threads em execução for menor que o valor de simultnância (discutido na próxima seção), um dos threads em espera (o mais recente) poderá processar o pacote de conclusão. Quando um thread em execução conclui seu processamento, ele normalmente chama [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) novamente, quando ele retorna com o próximo pacote de conclusão ou aguarda se a fila está vazia.

Os threads podem usar a [**função PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) para colocar pacotes de conclusão na fila de uma porta de conclusão de E/S. Ao fazer isso, a porta de conclusão pode ser usada para receber comunicações de outros threads do processo, além de receber pacotes de conclusão de E/S do sistema de E/S. A **função PostQueuedCompletionStatus** permite que um aplicativo enfileira seus próprios pacotes de conclusão de finalidade especial para a porta de conclusão de E/S sem iniciar uma operação de E/S assíncrona. Isso é útil para notificar threads de trabalho de eventos externos, por exemplo.

O alça de porta de conclusão de E/S e cada alça de arquivo associado a essa porta de conclusão de E/S específica são conhecidas como referências à porta de conclusão de *E/S*. A porta de conclusão de E/S é liberada quando não há mais referências a ela. Portanto, todos esses alças devem ser fechados corretamente para liberar a porta de conclusão de E/S e seus recursos do sistema associados. Depois que essas condições são atendidas, um aplicativo deve fechar o alçamento da porta de conclusão de E/S chamando a [**função CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

> [!Note]
>
> Uma porta de conclusão de E/S está associada ao processo que a criou e não é compartilhável entre processos. No entanto, um único handle é compartilhável entre threads no mesmo processo.

 

## <a name="threads-and-concurrency"></a>Threads e concurrency

A propriedade mais importante de uma porta de conclusão de E/S a ser considerada com cuidado é o valor de simulta. O valor de simultnia de uma porta de conclusão é especificado quando ela é criada com [**CreateIoCompletionPort**](createiocompletionport.md) por meio do *parâmetro NumberOfConcurrentThreads.* Esse valor limita o número de threads que podem ser executados associados à porta de conclusão. Quando o número total de threads que podem ser executados associados à porta de conclusão atingir o valor de simultosa, o sistema bloqueará a execução de quaisquer threads subsequentes associados a essa porta de conclusão até que o número de threads que podem ser executados seja inferior ao valor de simultnidade.

O cenário mais eficiente ocorre quando há pacotes de conclusão aguardando na fila, mas nenhuma espera pode ser atendida porque a porta atingiu seu limite de simultrreidade. Considere o que acontece com um valor de concurrency de um e vários threads aguardando na chamada de função [**GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Nesse caso, se a fila sempre tiver pacotes de conclusão aguardando, quando o thread em execução chamar **GetQueuedCompletionStatus**, ela não bloqueará a execução porque, conforme mencionado anteriormente, a fila de threads será LIFO. Em vez disso, esse thread escolherá imediatamente o próximo pacote de conclusão na fila. Nenhuma alternação de contexto de thread ocorrerá, porque o thread em execução está continuamente escolhendo pacotes de conclusão e os outros threads não podem ser executados.

> [!Note]
>
> No exemplo anterior, os threads extras parecem ser inúteis e nunca são executados, mas isso pressuém que o thread em execução nunca é colocado em um estado de espera por algum outro mecanismo, encerra ou fecha sua porta de conclusão de E/S associada. Considere todas essas ramificações de execução de thread ao projetar o aplicativo.

 

O melhor valor máximo geral a ser escolher para o valor de competência é o número de CPUs no computador. Se a transação exigir um cálculo demorado, um valor de simultrreidade maior permitirá que mais threads executem. Cada pacote de conclusão pode levar mais tempo para ser concluído, mas mais pacotes de conclusão serão processados ao mesmo tempo. Você pode experimentar o valor de concurrency em conjunto com ferramentas de criação de perfil para obter o melhor efeito para seu aplicativo.

O sistema também permite que um thread aguardando em [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) processe um pacote de conclusão se outro thread em execução associado à mesma porta de conclusão de E/S entrar em um estado de espera por outros motivos, por exemplo, a [**função SuspendThread.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) Quando o thread no estado de espera começa a ser executado novamente, pode haver um breve período quando o número de threads ativos excede o valor de simultaneidade. No entanto, o sistema reduz rapidamente esse número, não permitindo novos threads ativos até que o número de threads ativos seja inferior ao valor de simultencial. Esse é um motivo para seu aplicativo criar mais threads em seu pool de threads do que o valor de concurrency. O gerenciamento de pool de threads está além do escopo deste tópico, mas uma boa regra geral é ter um mínimo de duas vezes mais threads no pool de threads que há processadores no sistema. Para obter informações adicionais sobre o pool de threads, consulte [Pools de threads](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Funções de E/S com suporte

As funções a seguir podem ser usadas para iniciar operações de E/S concluídas usando portas de conclusão de E/S. Você deve passar a função uma instância da estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e um alçamento de arquivo associado anteriormente a uma porta de conclusão de E/S (por uma chamada para [**CreateIoCompletionPort**](createiocompletionport.md)) para habilitar o mecanismo de porta de conclusão de E/S:

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**Waitcommevent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**Wsasendto**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**Wsasend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**Wsarecvfrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**Wsarecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>


</dt> <dt>

[Sobre Processos e Threads](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**Createiocompletionport**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
