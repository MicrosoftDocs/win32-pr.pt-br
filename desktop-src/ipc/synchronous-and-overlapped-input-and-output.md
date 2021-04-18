---
description: E/s de pipe síncrono e I/O de pipe assíncrono. As funções ReadFile, WriteFile, TransactNamedPipe e ConnectNamedPipe podem executar operações de entrada e saída em um pipe de forma síncrona ou assíncrona.
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: E/s de pipe síncrono e sobreposto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788843"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>E/s de pipe síncrono e sobreposto

As funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) podem executar operações de entrada e saída em um pipe de forma síncrona ou assíncrona. Quando uma função é executada de forma síncrona, ela não retorna até que a operação que ele está executando seja concluída. Isso significa que a execução do thread de chamada pode ser bloqueada por um período indefinido enquanto aguarda uma operação demorada ser concluída. Quando uma função é executada de forma assíncrona, ela retorna imediatamente, mesmo que a operação não tenha sido concluída. Isso permite que uma operação demorada seja executada em segundo plano enquanto o thread de chamada está livre para executar outras tarefas.

O uso de e/s assíncrona permite que um servidor de pipe use um loop que executa as seguintes etapas:

1.  Especifique vários objetos de evento em uma chamada para a função Wait e aguarde até que um dos objetos seja definido para o estado sinalizado.
2.  Use o valor de retorno da função de espera para determinar qual operação sobreposta foi concluída.
3.  Execute as tarefas necessárias para limpar a operação concluída e iniciar a próxima operação para esse identificador de pipe. Isso pode envolver o início de outra operação sobreposta para o mesmo identificador de pipe.

As operações sobrepostas possibilitam que um pipe Leia e grave dados simultaneamente e que um único thread execute operações de e/s simultâneas em vários identificadores de pipe. Isso permite que um servidor de pipe de thread único manipule comunicações com vários clientes de pipe com eficiência. Para obter um exemplo, consulte [servidor de pipe nomeado usando e/s sobreposta](named-pipe-server-using-overlapped-i-o.md).

Para que um servidor de pipe Use operações síncronas para se comunicar com mais de um cliente, ele deve criar um thread separado para cada cliente de pipe para que um ou mais threads possam ser executados enquanto outros threads estiverem aguardando. Para obter um exemplo de um servidor de pipe multi-threaded que usa operações síncronas, consulte [servidor de pipe multi-threaded](multithreaded-pipe-server.md).

## <a name="enabling-asynchronous-operation"></a>Habilitando operação assíncrona

As funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) podem ser executadas de forma assíncrona somente se você habilitar o modo Sobreposto para o identificador de pipe especificado e especificar um ponteiro válido para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Se o ponteiro **sobreposto** for **nulo**, o valor de retorno da função poderá indicar incorretamente que a operação foi concluída. Portanto, é altamente recomendável que, se você criar um identificador com o sinalizador de arquivo \_ \_ sobreposto e desejar um comportamento assíncrono, sempre deverá especificar uma estrutura **sobreposta** válida.

O membro **hEvent** da estrutura [**Overlapped**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) especificada deve conter um identificador para um objeto de evento de redefinição manual. Esse é um objeto de sincronização criado pela função [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) . O thread que inicia a operação sobreposta usa o objeto de evento para determinar quando a operação foi concluída. Você não deve usar o identificador de pipe para sincronização ao executar operações simultâneas no mesmo identificador porque não há nenhuma maneira de saber qual a conclusão da operação fez com que o identificador de pipe fosse sinalizado. A única técnica confiável para executar operações simultâneas no mesmo identificador de pipe é usar uma estrutura **sobreposta** separada com seu próprio objeto de evento para cada operação. Para obter mais informações sobre objetos de evento, consulte [sincronização](/windows/desktop/Sync/synchronization).

Além disso, você pode ser notificado quando uma operação sobreposta for concluída usando as funções [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ou [**GetQueuedCompletionStatusEx**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) . Nesse caso, você não precisa atribuir o evento de redefinição manual na estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e a conclusão ocorre em relação ao identificador de pipe da mesma maneira que uma operação de leitura ou gravação assíncrona. Para obter mais informações, consulte [portas de conclusão de e/s](/windows/desktop/FileIO/i-o-completion-ports).

Quando as operações [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) são executadas de forma assíncrona, uma das seguintes situações ocorrerá:

-   Se a operação for concluída quando a função retornar, o valor de retorno indicará o êxito ou a falha da operação. Se ocorrer um erro, o valor de retorno será zero e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará algo diferente de \_ e/s de erro \_ pendente.
-   Se a operação não tiver sido concluída quando a função retornar, o valor de retorno será zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará a \_ e/s de erro \_ pendente. Nesse caso, o thread de chamada deve aguardar até que a operação seja concluída. O thread de chamada deve chamar a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar os resultados.

## <a name="using-completion-routines"></a>Usando rotinas de conclusão

As funções [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) fornecem outra forma de e/s sobreposta. Ao contrário das funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) sobrepostas, que usam um objeto de evento para sinalizar a conclusão, as funções estendidas especificam uma *rotina de conclusão*. Uma rotina de conclusão é uma função que é enfileirada para execução quando a operação de leitura ou gravação é concluída. A rotina de conclusão não é executada até que o thread que chamou **ReadFileEx** e **WriteFileEx** inicie uma *operação de espera alertável* chamando uma das [funções de espera alertáveis](/windows/desktop/Sync/wait-functions) com o parâmetro *fAlertable* definido como **true**. Em uma operação de espera alertável, as funções também retornam quando uma rotina de conclusão de **ReadFileEx** ou **WriteFileEx** é enfileirada para execução. Um servidor de pipe pode usar as funções estendidas para executar uma sequência de operações de leitura e gravação para cada cliente que se conecta a ele. Cada operação de leitura ou gravação na sequência especifica uma rotina de conclusão e cada rotina de conclusão inicia a próxima etapa na sequência. Para obter um exemplo, consulte [servidor de pipe nomeado usando rotinas de conclusão](named-pipe-server-using-completion-routines.md).

 

 
