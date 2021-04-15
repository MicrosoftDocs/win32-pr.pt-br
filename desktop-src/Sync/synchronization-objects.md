---
description: Um objeto de sincronização é um objeto cujo identificador pode ser especificado em uma das funções de espera para coordenar a execução de vários threads.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Objetos de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299cbd6225b3cc7629378f5fe500fc36ccbe8e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505919"
---
# <a name="synchronization-objects"></a>Objetos de sincronização

Um *objeto de sincronização* é um objeto cujo identificador pode ser especificado em uma das [funções de espera](wait-functions.md) para coordenar a execução de vários threads. Mais de um processo pode ter um identificador para o mesmo objeto de sincronização, tornando possível a sincronização entre processos.

Os tipos de objeto a seguir são fornecidos exclusivamente para sincronização.



| Tipo           | Descrição                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento          | Notifica um ou mais threads de espera em que um evento ocorreu. Para obter mais informações, consulte [objetos de evento](event-objects.md).                                                                                   |
| Mutex          | Pode pertencer apenas a um thread por vez, permitindo que os threads coordenem o acesso mutuamente exclusivo a um recurso compartilhado. Para obter mais informações, consulte [objetos mutex](mutex-objects.md).                          |
| Sinal      | Mantém uma contagem entre zero e um valor máximo, limitando o número de threads que estão acessando simultaneamente um recurso compartilhado. Para obter mais informações, consulte [Semaphore Objects](semaphore-objects.md). |
| Temporizador de espera | Notifica um ou mais threads em espera que chegaram um tempo especificado. Para obter mais informações, consulte [objetos de timer de espera](waitable-timer-objects.md).                                                          |



 

Embora esteja disponível para outros usos, os objetos a seguir também podem ser usados para sincronização.



| Objeto                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Notificação de alteração          | Criado pela função [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) , seu estado é definido como sinalizado quando um tipo especificado de alteração ocorre dentro de um diretório ou árvore de diretórios especificados. Para obter mais informações, consulte [obtendo notificações de alteração de diretório](../fileio/obtaining-directory-change-notifications.md).                                                                                                                                   |
| Entrada do console                | Criado quando um console é criado. O identificador para a entrada do console é retornado pela função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) quando CONIN $ é especificado ou pela função [**GetStdHandle**](/windows/console/getstdhandle) . Seu estado é definido para sinalizado quando há entrada não lida no buffer de entrada do console e definido como não sinalizado quando o buffer de entrada está vazio. Para obter mais informações sobre consoles, consulte [aplicativos em modo de caractere](/windows/console/character-mode-applications) |
| Trabalho                          | Criado chamando a função [**CreateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) . O estado de um objeto de trabalho é definido como sinalizado quando todos os seus processos são encerrados porque o limite de tempo final do trabalho especificado foi excedido. Para obter mais informações sobre objetos de trabalho, consulte [objetos de trabalho](../procthread/job-objects.md).                                                                                                                                                             |
| Notificação de recursos de memória | Criado pela função [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) . Seu estado é definido para sinalizado quando um tipo especificado de alteração ocorre na memória física. Para obter mais informações sobre memória, consulte [Gerenciamento de memória](../memory/memory-management.md).                                                                                                                                                                                  |
| Processar                      | Criado chamando a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Seu estado é definido como não sinalizado enquanto o processo está em execução e definido como sinalizado quando o processo é encerrado. Para obter mais informações sobre processos, consulte [processos e threads](../procthread/processes-and-threads.md).                                                                                                                                                                                  |
| Thread                       | Criado quando um novo thread é criado chamando a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Seu estado é definido como não sinalizado enquanto o thread está em execução e definido como sinalizado quando o thread é encerrado. Para obter mais informações sobre threads, consulte [processos e threads](../procthread/processes-and-threads.md).                                                            |



 

Em algumas circunstâncias, você também pode usar um arquivo, um pipe nomeado ou um dispositivo de comunicação como um objeto de sincronização; no entanto, seu uso para essa finalidade não é recomendado. Em vez disso, use e/s assíncrona e aguarde o conjunto de objetos de evento na estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . É mais seguro usar o objeto Event devido à confusão que pode ocorrer quando várias operações sobrepostas simultâneas são executadas no mesmo arquivo, pipe nomeado ou dispositivo de comunicação. Nessa situação, não há como saber qual operação causou a sinalização do estado do objeto.

Para obter informações adicionais sobre operações de e/s em arquivos, pipes nomeados ou comunicações, consulte [sincronização e entrada e saída sobrepostas](synchronization-and-overlapped-input-and-output.md).

 

 
