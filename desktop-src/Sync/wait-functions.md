---
description: As funções Wait permitem que um thread bloqueie sua própria execução.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funções de espera
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: f5a21b0d95a316b926fcaad037004edc8c418246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748373"
---
# <a name="wait-functions"></a>Funções de espera

As *funções Wait* permitem que um thread bloqueie sua própria execução. As funções Wait não retornam até que os critérios especificados tenham sido atendidos. O tipo de função Wait determina o conjunto de critérios usados. Quando uma função Wait é chamada, ela verifica se os critérios de espera foram atendidos. Se os critérios não tiverem sido atendidos, o thread de chamada entrará no estado de espera até que as condições dos critérios de espera tenham sido atendidas ou o intervalo de tempo limite especificado decorra.

-   [Funções de espera de objeto único](#single-object-wait-functions)
-   [Funções de espera de vários objetos](#multiple-object-wait-functions)
-   [Funções de espera alertáveis](#alertable-wait-functions)
-   [Funções de espera registradas](#registered-wait-functions)
-   [Aguardando um endereço](#waiting-on-an-address)
-   [Funções de espera e intervalos de tempo limite](#wait-functions-and-time-out-intervals)
-   [Funções de espera e objetos de sincronização](#wait-functions-and-synchronization-objects)
-   [Funções de espera e criação de janelas](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funções de espera de objeto único

As funções [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) exigem um identificador para um objeto de sincronização. Essas funções retornam quando ocorre uma das seguintes opções:

-   O objeto especificado está no estado sinalizado.
-   O intervalo de tempo limite expirou. O intervalo de tempo limite pode ser definido como **infinito** para especificar que a espera não atingirá o tempo limite.

A função [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) permite que o thread de chamada defina atomicamente o estado de um objeto para sinalizado e aguarde até que o estado de outro objeto seja definido para sinalizado.

## <a name="multiple-object-wait-functions"></a>Funções de espera de vários objetos

As funções [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permitem que o thread de chamada especifique uma matriz que contenha um ou mais identificadores de objeto de sincronização. Essas funções retornam quando ocorre uma das seguintes opções:

-   O estado de qualquer um dos objetos especificados é definido como signaled ou os Estados de todos os objetos foram definidos como signaled. Você controla se um ou todos os Estados serão usados na chamada de função.
-   O intervalo de tempo limite expirou. O intervalo de tempo limite pode ser definido como **infinito** para especificar que a espera não atingirá o tempo limite.

A função [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permite especificar objetos de evento de entrada na matriz de identificadores de objeto. Isso é feito quando você especifica o tipo de entrada a ser aguardado na fila de entrada do thread. Por exemplo, um thread poderia usar **MsgWaitForMultipleObjects** para bloquear sua execução até que o estado de um objeto especificado tenha sido definido como signaled e haja entrada do mouse disponível na fila de entrada do thread. O thread pode usar a função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) para recuperar a entrada.

Ao aguardar que os Estados de todos os objetos sejam definidos para serem sinalizados, essas funções de vários objetos não modificam os Estados dos objetos especificados até que os Estados de todos os objetos tenham sido definidos sinalizados. Por exemplo, o estado de um objeto mutex pode ser sinalizado, mas o thread de chamada não obtém a propriedade até que os Estados dos outros objetos especificados na matriz também tenham sido configurados para serem sinalizados. Enquanto isso, algum outro thread pode obter a propriedade do objeto mutex, definindo, assim, seu estado como não sinalizado.

Ao aguardar que o estado de um único objeto seja definido para sinalizado, essas funções de vários objetos verificam os identificadores na matriz na ordem iniciando com o índice 0, até que um dos objetos seja sinalizado. Se vários objetos ficarem sinalizados, a função retornará o índice do primeiro identificador na matriz cujo objeto foi sinalizado.

## <a name="alertable-wait-functions"></a>Funções de espera alertáveis

As funções [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) diferem das outras funções Wait no que podem, opcionalmente, executar uma *operação de espera alertável*. Em uma operação de espera alertável, a função pode retornar quando as condições especificadas são atendidas, mas também pode retornar se o sistema enfileira uma rotina de conclusão de e/s ou uma APC para execução pelo thread em espera. Para obter mais informações sobre as operações de espera do alerta e as rotinas de conclusão de e/s, consulte [sincronização e entrada e saída sobrepostas](synchronization-and-overlapped-input-and-output.md). Para obter mais informações sobre APCs, consulte [chamadas de procedimento assíncrono](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Funções de espera registradas

A função [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) difere das outras funções Wait em que a operação Wait é executada por um thread do pool de [threads](../procthread/thread-pooling.md). Quando as condições especificadas são atendidas, a função de retorno de chamada é executada por um thread de trabalho do pool de threads.

Por padrão, uma operação de espera registrada é uma operação de espera múltipla. O sistema redefine o timer sempre que o evento é sinalizado (ou o intervalo de tempo limite expira) até que você chame a função [**UnregisterWaitEx**](unregisterwaitex.md) para cancelar a operação. Para especificar que uma operação de espera deve ser executada apenas uma vez, defina o parâmetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) como **WT \_ EXECUTEONLYONCE**.

Se o thread chamar funções que usam APCs, defina o parâmetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) como **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>Aguardando um endereço

Um thread pode usar a função [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) para aguardar o valor de um endereço de destino ser alterado de um valor indesejado para qualquer outro valor. Isso permite que os threads aguardem que um valor seja alterado sem precisar girar ou lidar com os problemas de sincronização que podem surgir quando o thread captura um valor indesejado, mas o valor é alterado antes que o thread possa aguardar.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) retorna quando o código que modifica o valor de destino sinaliza a alteração chamando [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) para ativar um único thread em espera ou [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) para ativar todos os threads em espera. Se um intervalo de tempo limite for especificado com **WaitOnAddress** e nenhum thread chamar uma função Wake, a função retornará quando o intervalo de tempo limite expirar. Se nenhum intervalo de tempo limite for especificado, o thread aguardará indefinidamente.

## <a name="wait-functions-and-time-out-intervals"></a>Funções de espera e intervalos de tempo limite

A precisão do intervalo de tempo limite especificado depende da resolução do relógio do sistema. O relógio do sistema "tiques" a uma taxa constante. Se o intervalo de tempo limite for menor que a resolução do relógio do sistema, a espera poderá atingir o tempo limite em menos do que o período especificado. Se o intervalo de tempo limite for maior que um tique, mas menor que dois, a espera poderá estar em qualquer lugar entre um e dois tiques, e assim por diante.

Para aumentar a precisão do intervalo de tempo limite para as funções de espera, chame a função **timeGetDevCaps** para determinar a resolução mínima de timer com suporte e a função **timeBeginPeriod** para definir a resolução do temporizador como seu mínimo. Tenha cuidado ao chamar **timeBeginPeriod**, uma vez que as chamadas frequentes podem afetar significativamente o relógio do sistema, o uso de energia do sistema e o Agendador. Se você chamar **timeBeginPeriod**, chame-o uma vez no início do aplicativo e certifique-se de chamar a função **timeEndPeriod** no final do aplicativo.

## <a name="wait-functions-and-synchronization-objects"></a>Funções de espera e objetos de sincronização

As funções Wait podem modificar os Estados de alguns tipos de [objetos de sincronização](synchronization-objects.md). A modificação ocorre apenas para o objeto ou objetos cujo estado sinalizado fez com que a função fosse retornada. As funções Wait podem modificar os Estados dos objetos de sincronização da seguinte maneira:

-   A contagem de um objeto de semáforo diminui em um, e o estado do semáforo é definido como não sinalizado se sua contagem for zero.
-   Os Estados do mutex, do evento de redefinição automática e dos objetos de notificação de alteração são definidos como sem sinal.
-   O estado de um temporizador de sincronização é definido como não sinalizado.
-   Os Estados dos objetos de evento de redefinição manual, timer de redefinição manual, processo, thread e entrada do console não são afetados por uma função Wait.

## <a name="wait-functions-and-creating-windows"></a>Funções de espera e criação de janelas

Você precisa ter cuidado ao usar as funções de espera e o código que cria o Windows direta ou indiretamente. Se um thread criar qualquer Windows, ele deverá processar mensagens. Difusões de mensagens são enviadas a todas as janelas no sistema. Se você tiver um thread que usa uma função Wait sem intervalo de tempo limite, o sistema irá deadlock. Dois exemplos de código que cria indiretamente o Windows são DDE e a função **CoInitialize** . Portanto, se você tiver um thread que cria o Windows, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), em vez de outras funções de espera.

 

 
