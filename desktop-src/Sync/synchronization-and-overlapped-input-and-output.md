---
description: Você pode executar operações síncronas ou assíncronas (também chamadas sobrepostas) de e/s em arquivos, pipes nomeados e dispositivos de comunicação serial.
ms.assetid: db44990e-5a0f-4153-8ff6-79dd7cda48af
title: Sincronização e entrada e saída sobrepostas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e263bb39badc7cbfadd67d80eb169dc1fe6d6c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754483"
---
# <a name="synchronization-and-overlapped-input-and-output"></a>Sincronização e entrada e saída sobrepostas

Você pode executar operações síncronas ou assíncronas (também chamadas sobrepostas) de e/s em arquivos, pipes nomeados e dispositivos de comunicação serial. As funções [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol), [**WaitCommEvent**](/windows/win32/api/winbase/nf-winbase-waitcommevent), [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)e [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) podem ser executadas de forma síncrona ou assíncrona. As funções [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) podem ser executadas apenas de forma assíncrona.

Quando uma função é executada de forma síncrona, ela não retorna até que a operação seja concluída. Isso significa que a execução do thread de chamada pode ser bloqueada por um período indefinido enquanto aguarda a conclusão de uma operação demorada. As funções chamadas para a operação sobreposta podem retornar imediatamente, embora a operação não tenha sido concluída. Isso permite que uma operação de e/s demorada seja executada em segundo plano enquanto o thread de chamada está livre para executar outras tarefas. Por exemplo, um único thread pode executar operações de e/s simultâneas em diferentes identificadores ou até mesmo operações de leitura e gravação simultâneas no mesmo identificador.

Para sincronizar sua execução com a conclusão da operação sobreposta, o thread de chamada usa a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) , a função [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) ou uma das [funções Wait](wait-functions.md) para determinar quando a operação sobreposta foi concluída. Você também pode usar a macro [**HasOverlappedIoCompleted**](/windows/desktop/api/WinBase/nf-winbase-hasoverlappediocompleted) para sondar a conclusão.

Para cancelar todas as operações de e/s assíncronas pendentes, use a função [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) e forneça uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) que especifique a solicitação a ser cancelada. Use a função [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio) para cancelar as operações de e/s assíncronas pendentes emitidas pelo thread de chamada para o identificador de arquivo especificado.

As operações sobrepostas exigem um arquivo, um pipe nomeado ou um dispositivo de comunicação criado com o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** . Quando um thread chama uma função (como a função [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) ) para executar uma operação sobreposta, o thread de chamada deve especificar um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . (Se esse ponteiro for **nulo**, o valor de retorno da função poderá indicar incorretamente que a operação foi concluída.) Todos os membros da estrutura **sobreposta** devem ser inicializados para zero, a menos que um evento seja usado para sinalizar a conclusão de uma operação de e/s. Se um evento for usado, o membro **hEvent** da estrutura **sobreposta** especificará um identificador para o objeto de evento alocado. O sistema define o estado do objeto de evento como não sinalizado quando uma chamada para a função de e/s retorna antes de a operação ser concluída. O sistema define o estado do objeto de evento para sinalizado quando a operação foi concluída. Um evento será necessário apenas se houver mais de uma operação de e/s pendente ao mesmo tempo. Se um evento não for usado, cada operação de e/s concluída sinalizará o arquivo, o pipe nomeado ou o dispositivo de comunicação.

Quando uma função é chamada para executar uma operação sobreposta, a operação pode ser concluída antes que a função retorne. Quando isso acontece, os resultados são tratados como se a operação tivesse sido executada de forma síncrona. Se a operação não tiver sido concluída, no entanto, o valor de retorno da função será **false** e a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ e/s \_ pendente**.

Um thread pode gerenciar operações sobrepostas de um dos dois métodos:

-   Use a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) para aguardar a conclusão da operação sobreposta. Se **GetOverlappedResultEx** for usado, o thread de chamada poderá especificar um tempo limite para a operação sobreposta ou executar uma espera alertável.
-   Especifique um identificador para o objeto de evento de redefinição manual da estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) em uma das [funções de espera](wait-functions.md) e, depois, a função Wait retorna, chame [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex). A função retorna os resultados da operação sobreposta concluída e, para funções nas quais essas informações são apropriadas, ele relata o número real de bytes que foram transferidos.

Ao executar várias operações sobrepostas simultâneas em um único thread, o thread de chamada deve especificar uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) para cada operação. Cada estrutura **sobreposta** deve especificar um identificador para um objeto de evento de redefinição manual diferente. Para aguardar a conclusão de qualquer uma das operações sobrepostas, o thread especifica todos os identificadores de eventos de redefinição manual como critérios de espera em uma das [funções de espera](wait-functions.md)de vários objetos. O valor de retorno da função Wait de vários objetos indica qual objeto de evento de redefinição manual foi sinalizado, para que o thread possa determinar qual operação sobreposta causou a conclusão da operação de espera.

É mais seguro usar um objeto de evento separado para cada operação sobreposta, em vez de especificar nenhum objeto de evento ou reutilizar o mesmo objeto de evento para várias operações. Se nenhum objeto de evento for especificado na estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , o sistema sinalizará o estado do arquivo, o pipe nomeado ou o dispositivo de comunicação quando a operação sobreposta tiver sido concluída. Assim, você pode especificar esses identificadores como objetos de sincronização em uma função de espera, embora seu uso para essa finalidade possa ser difícil de gerenciar porque, ao executar operações sobrepostas simultâneas no mesmo arquivo, pipe nomeado ou dispositivo de comunicação, não há como saber qual operação causou a sinalização do estado do objeto.

Um thread não deve reutilizar um evento com a suposição de que o evento será sinalizado somente pela operação sobreposta do thread. Um evento é sinalizado no mesmo thread que a operação sobreposta que está sendo concluída. Usar o mesmo evento em vários threads pode levar a uma condição de corrida na qual o evento é sinalizado corretamente para o thread cuja operação é concluída primeiro e prematuramente para outros threads que usam esse evento. Em seguida, quando a próxima operação sobreposta for concluída, o evento será sinalizado novamente para todos os threads que usam esse evento e assim por diante até que todas as operações sobrepostas sejam concluídas.

Para obter exemplos que ilustram o uso de operações sobrepostas, rotinas de conclusão e a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) , consulte [usando pipes](../ipc/using-pipes.md).

* * Windows Vista, Windows Server 2003 e Windows XP: * *

Tenha cuidado ao reutilizar estruturas [**sobrepostas**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . Se as estruturas **sobrepostas** forem reutilizadas em vários threads e [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) for chamado com o parâmetro *bWait* definido como **true**, o thread de chamada deverá garantir que o evento associado seja sinalizado antes de reutilizar a estrutura. Isso pode ser feito usando a função [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) depois de chamar **GetOverlappedResult** para forçar o thread a aguardar até que a operação seja concluída. Observe que o objeto de evento deve ser um objeto de evento de redefinição manual. Se um objeto de evento AutoReset for usado, chamar **GetOverlappedResult** com o parâmetro *BWait* definido como **true** fará com que a função seja bloqueada indefinidamente. Esse comportamento mudou a partir do Windows 7 e do Windows Server 2008 R2 para aplicativos que especificam o Windows 7 como o sistema operacional com suporte no manifesto do aplicativo. Para obter mais informações, consulte [manifestos do aplicativo](/previous-versions/windows/desktop/adrms_sdk/application-manifests).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de e/s](../fileio/i-o-concepts.md)
</dt> </dl>

 

 
