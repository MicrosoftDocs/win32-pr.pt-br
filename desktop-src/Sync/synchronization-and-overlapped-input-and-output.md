---
description: Você pode executar operações de E/S síncronas ou assíncronas (também chamadas de operações de E/S sobrepacotados) em arquivos, pipes nomeados e dispositivos de comunicação serial.
ms.assetid: db44990e-5a0f-4153-8ff6-79dd7cda48af
title: Sincronização e entrada e saída sobrecarradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e462e4c2cffa3f1c9dee9bc33a7c75b910ce8139dbdfab9c190b4691c4b6bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975906"
---
# <a name="synchronization-and-overlapped-input-and-output"></a>Sincronização e entrada e saída sobrecarradas

Você pode executar operações de E/S síncronas ou assíncronas (também chamadas de operações de E/S sobrepacotados) em arquivos, pipes nomeados e dispositivos de comunicação serial. As funções [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol), [**WaitCommEvent**](/windows/win32/api/winbase/nf-winbase-waitcommevent), [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)e [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) podem ser executadas de forma síncrona ou assíncrona. As [**funções ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex) [**e WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) só podem ser executadas de forma assíncrona.

Quando uma função é executada de forma síncrona, ela não retorna até que a operação seja concluída. Isso significa que a execução do thread de chamada pode ser bloqueada por um período indefinido enquanto aguarda a execução de uma operação demorada. As funções chamadas para a operação sobreexplorada podem retornar imediatamente, mesmo que a operação não tenha sido concluída. Isso permite que uma operação de E/S demorada seja executada em segundo plano enquanto o thread de chamada está livre para executar outras tarefas. Por exemplo, um único thread pode executar operações simultâneas de E/S em diferentes alças ou até mesmo operações simultâneas de leitura e gravação no mesmo handle.

Para sincronizar sua execução com a conclusão da operação sobreexplorada, o thread de chamada usa a função [**GetOverlappedResult,**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) a [**função GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) ou uma das funções de espera para determinar quando a operação sobreexplorada foi concluída. [](wait-functions.md) Você também pode usar a [**macro HasOverlappedIoCompleted**](/windows/desktop/api/WinBase/nf-winbase-hasoverlappediocompleted) para sondar a conclusão.

Para cancelar todas as operações de E/S assíncronas pendentes, use a função [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) e forneça uma estrutura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) que especifica a solicitação a ser cancelada. Use a [**função CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio) para cancelar operações de E/S assíncronas pendentes emitidas pelo thread de chamada para o alçamento de arquivo especificado.

As operações sobrecarradas exigem um arquivo, pipe nomeado ou dispositivo de comunicação que foi criado com o sinalizador **FILE \_ FLAG \_ OVERLAPPED.** Quando um thread chama uma função (como a [**função ReadFile)**](/windows/win32/api/fileapi/nf-fileapi-readfile) para executar uma operação sobrecarada, o thread de chamada deve especificar um ponteiro para uma estrutura [**OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) (Se esse ponteiro for **NULL,** o valor de retorno da função poderá indicar incorretamente que a operação foi concluída.) Todos os membros da estrutura **OVERLAPPED** devem ser inicializados como zero, a menos que um evento seja usado para sinalizar a conclusão de uma operação de E/S. Se um evento for usado, o **membro hEvent** da estrutura **OVERLAPPED** especificará um identificador para o objeto de evento alocado. O sistema define o estado do objeto de evento como não sinalizado quando uma chamada para a função de E/S retorna antes que a operação seja concluída. O sistema define o estado do objeto de evento para sinalizado quando a operação foi concluída. Um evento será necessário somente se houver mais de uma operação de E/S pendente ao mesmo tempo. Se um evento não for usado, cada operação de E/S concluída sinaliza o arquivo, o pipe nomeado ou o dispositivo de comunicação.

Quando uma função é chamada para executar uma operação sobrecarada, a operação pode ser concluída antes que a função retorne. Quando isso acontece, os resultados são tratados como se a operação tivesse sido executada de forma síncrona. Se a operação não tiver sido concluída, no entanto, o valor de retorno da função será **FALSE** e a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará **ERROR \_ IO \_ PENDING.**

Um thread pode gerenciar operações sobrecaradas por um dos dois métodos:

-   Use a [**função GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) para aguardar a conclusão da operação sobrecarada. Se **GetOverlappedResultEx** for usado, o thread de chamada poderá especificar um tempo máximo para a operação sobrecarada ou executar uma espera alertável.
-   Especifique um identificador para o objeto de evento de [](wait-functions.md) redefinição manual da estrutura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) em uma das funções de espera e, depois que a função de espera for retornada, chame [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex). A função retorna os resultados da operação sobrecarrada concluída e, para funções nas quais essas informações são apropriadas, ela relata o número real de bytes que foram transferidos.

Ao executar várias operações sobrecaradas simultâneas em um único thread, o thread de chamada deve especificar uma [**estrutura OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) para cada operação. Cada **estrutura OVERLAPPED** deve especificar um identificador para um objeto de evento de redefinição manual diferente. Para aguardar que qualquer uma das operações sobreposição seja concluída, o thread especifica todos os identificadores de evento de redefinição manual como critérios de espera em uma das funções de espera de [vários objetos](wait-functions.md). O valor de retorno da função de espera de vários objetos indica qual objeto de evento de redefinição manual foi sinalizado, para que o thread possa determinar qual operação sobreposição fez com que a operação de espera fosse concluída.

É mais seguro usar um objeto de evento separado para cada operação sobreexplorada, em vez de especificar nenhum objeto de evento ou reutilizar o mesmo objeto de evento para várias operações. Se nenhum objeto de evento for especificado na estrutura [**OVERLAPPED,**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) o sistema sinaliza o estado do arquivo, o pipe nomeado ou o dispositivo de comunicações quando a operação sobrecodizada foi concluída. Portanto, você pode especificar esses identificador como objetos de sincronização em uma função de espera, embora seu uso para essa finalidade possa ser difícil de gerenciar porque, ao executar operações sobrecarradas simultâneas no mesmo arquivo, pipe nomeado ou dispositivo de comunicação, não há como saber qual operação fez com que o estado do objeto fosse sinalizado.

Um thread não deve reutilizar um evento com a suposição de que o evento será sinalizado somente pela operação sobrecarada desse thread. Um evento é sinalizado no mesmo thread que a operação sobreexplorada que está sendo realizada. Usar o mesmo evento em vários threads pode levar a uma condição de corrida na qual o evento é sinalizado corretamente para o thread cuja operação é concluída primeiro e prematuramente para outros threads usando esse evento. Em seguida, quando a próxima operação sobreexplorada for concluída, o evento será sinalizado novamente para todos os threads que usam esse evento e assim por diante até que todas as operações sobrecaruladas sejam concluídas.

Para obter exemplos que ilustram o uso de operações sobrecarradas, rotinas de conclusão e a função [**GetOverlappedResult,**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) consulte [Usando pipes](../ipc/using-pipes.md).

**Windows Vista, Windows Server 2003 e Windows XP: **

Tenha cuidado ao reutilar [**estruturas OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Se estruturas **OVERLAPPED** são reutilizada em vários threads e [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) é chamado com o parâmetro *bWait* definido como **TRUE**, o thread de chamada deve garantir que o evento associado seja sinalizado antes de reutilizar a estrutura. Isso pode ser feito usando a função [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) depois de chamar **GetOverlappedResult** para forçar o thread a aguardar até que a operação seja concluída. Observe que o objeto de evento deve ser um objeto de evento de redefinição manual. Se um objeto de evento autoreset for usado, chamar **GetOverlappedResult** com o parâmetro *bWait* definido como **TRUE** faz com que a função seja bloqueada indefinidamente. Esse comportamento mudou a partir do Windows 7 e Windows Server 2008 R2 para aplicativos que especificam Windows 7 como o sistema operacional com suporte no manifesto do aplicativo. Para obter mais informações, consulte [Manifestos do aplicativo](/previous-versions/windows/desktop/adrms_sdk/application-manifests).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de E/S](../fileio/i-o-concepts.md)
</dt> </dl>

 

 
