---
description: As funções wait permitem que um thread bloqueie sua própria execução.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funções de espera
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: 15bfc37dcd8fe541c14b9a0693c7b743cae6ed3e548c418baf0585f078e6d59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764960"
---
# <a name="wait-functions"></a>Funções de espera

*As funções wait* permitem que um thread bloqueie sua própria execução. As funções de espera não retornam até que os critérios especificados tenham sido atendidos. O tipo de função de espera determina o conjunto de critérios usados. Quando uma função de espera é chamada, ela verifica se os critérios de espera foram atendidos. Se os critérios não foram atendidos, o thread de chamada entra no estado de espera até que as condições dos critérios de espera tenham sido atendidas ou o intervalo de tempo-tempo especificado desempate.

-   [Funções de espera de objeto único](#single-object-wait-functions)
-   [Funções de espera de vários objetos](#multiple-object-wait-functions)
-   [Funções de espera alertáveis](#alertable-wait-functions)
-   [Funções de espera registradas](#registered-wait-functions)
-   [Aguardando um endereço](#waiting-on-an-address)
-   [Funções de espera e intervalos de tempo-out](#wait-functions-and-time-out-intervals)
-   [Funções de espera e objetos de sincronização](#wait-functions-and-synchronization-objects)
-   [Funções de espera e criação de Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funções de espera de objeto único

As [**funções SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) exigem um identificador para um objeto de sincronização. Essas funções retornam quando ocorre uma das seguintes:

-   O objeto especificado está no estado sinalizado.
-   O intervalo de tempo-out é desempesado. O intervalo de tempo-out pode ser definido como **INFINITE** para especificar que a espera não passará do tempo."

A [**função SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) permite que o thread de chamada de definição atômica do estado de um objeto seja sinalizado e aguarde até que o estado de outro objeto seja definido como sinalizado.

## <a name="multiple-object-wait-functions"></a>Funções de espera de vários objetos

As funções [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permitem que o thread de chamada especifique uma matriz que contém um ou mais identificadors de objeto de sincronização. Essas funções retornam quando ocorre uma das seguintes:

-   O estado de qualquer um dos objetos especificados é definido como sinalizado ou os estados de todos os objetos foram definidos como sinalizados. Você controla se um ou todos os estados serão usados na chamada de função.
-   O intervalo de tempo-out é desempesado. O intervalo de tempo-out pode ser definido como **INFINITE** para especificar que a espera não passará do tempo."

A [**função MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) e [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permitem especificar objetos de evento de entrada na matriz de identificador de objeto. Isso é feito quando você especifica o tipo de entrada a ser aguardado na fila de entrada do thread. Por exemplo, um thread pode usar **MsgWaitForMultipleObjects** para bloquear sua execução até que o estado de um objeto especificado tenha sido definido como sinalizado e haja entrada do mouse disponível na fila de entrada do thread. O thread pode usar a [**função GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) para recuperar a entrada.

Ao aguardar que os estados de todos os objetos sejam definidos como sinalizados, essas funções de vários objetos não modificam os estados dos objetos especificados até que os estados de todos os objetos tenham sido sinalados. Por exemplo, o estado de um objeto mutex pode ser sinalizado, mas o thread de chamada não obterá a propriedade até que os estados dos outros objetos especificados na matriz também tenham sido definidos como sinalizados. Enquanto isso, algum outro thread pode obter a propriedade do objeto mutex, definindo assim seu estado como não sinal.

Ao aguardar o estado de um único objeto ser definido como sinalizado, essas funções de vários objetos verificam os identificador na matriz em ordem começando com o índice 0, até que um dos objetos seja sinalizado. Se vários objetos se tornarem sinal, a função retornará o índice do primeiro identificador na matriz cujo objeto foi sinalizado.

## <a name="alertable-wait-functions"></a>Funções de espera alertáveis

As funções [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)e [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) diferem das outras funções de espera, já que podem, opcionalmente, executar uma operação de espera alertável *.* Em uma operação de espera alertável, a função pode retornar quando as condições especificadas são atendidas, mas também poderá retornar se o sistema enfileirar uma rotina de conclusão de E/S ou um APC para execução pelo thread em espera. Para obter mais informações sobre operações de espera alertáveis e rotinas de conclusão de E/S, consulte [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md). Para obter mais informações sobre APCs, consulte Chamadas de procedimento [assíncrono](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Funções de espera registradas

A [**função RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) difere das outras funções de espera, já que a operação de espera é executada por um thread do [pool de threads](../procthread/thread-pooling.md). Quando as condições especificadas são atendidas, a função de retorno de chamada é executada por um thread de trabalho do pool de threads.

Por padrão, uma operação de espera registrada é uma operação de espera múltipla. O sistema redefine o temporizador toda vez que o evento é sinalizado (ou o intervalo de tempo-tempo é cancelado) até que você chame a [**função UnregisterWaitEx**](unregisterwaitex.md) para cancelar a operação. Para especificar que uma operação de espera deve ser executada apenas uma vez, defina o parâmetro *dwFlags* [**de RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) como **WT \_ EXECUTEONLYONCE**.

Se o thread chamar funções que usam APCs, defina o parâmetro *dwFlags* [**de RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) como **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>Aguardando um endereço

Um thread pode usar a [**função WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) para aguardar o valor de um endereço de destino mudar de algum valor indesejável para qualquer outro valor. Isso permite que os threads aguardem a alteração de um valor sem a necessidade de girar ou lidar com os problemas de sincronização que podem surgir quando o thread captura um valor indesejável, mas o valor muda antes que o thread possa esperar.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) retorna quando o código que modifica o valor de destino sinaliza a alteração chamando [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) para a wake de um único thread de espera ou [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) para a wake todos os threads em espera. Se um intervalo de tempo-out for especificado com **WaitOnAddress** e nenhum thread chamar uma função de a wake, a função retornará quando o intervalo de tempo-tempo for desempesado. Se nenhum intervalo de tempo-tempo for especificado, o thread aguardará indefinidamente.

## <a name="wait-functions-and-time-out-intervals"></a>Funções de espera e intervalos de tempo-out

A precisão do intervalo de tempo-out especificado depende da resolução do relógio do sistema. O relógio do sistema "tiques" em uma taxa constante. Se o intervalo de tempo-out for menor que a resolução do relógio do sistema, a espera poderá chegar ao tempo máximo em menor que o período de tempo especificado. Se o intervalo de tempo-tempo for maior que um tique, mas menor que dois, a espera poderá estar em qualquer lugar entre um e dois tiques e assim por diante.

Para aumentar a precisão do intervalo de tempo limite para as funções de espera, chame a função **timeGetDevCaps** para determinar a resolução mínima do temporizador com suporte e a **função timeBeginPeriod** para definir a resolução do temporizador como o mínimo. Cuidado ao chamar **timeBeginPeriod,** pois chamadas frequentes podem afetar significativamente o relógio do sistema, o uso de energia do sistema e o agendador. Se você chamar **timeBeginPeriod**, chame-o uma vez no início do aplicativo e chame a função **timeEndPeriod** no final do aplicativo.

## <a name="wait-functions-and-synchronization-objects"></a>Funções de espera e objetos de sincronização

As funções de espera podem modificar os estados de alguns tipos de [objetos de sincronização](synchronization-objects.md). A modificação ocorre somente para o objeto ou objetos cujo estado sinalizado fez a função retornar. As funções wait podem modificar os estados dos objetos de sincronização da seguinte forma:

-   A contagem de um objeto semáforo diminui em um e o estado do semáforo é definido como não sinal se sua contagem for zero.
-   Os estados de mutex, evento de redefinição automática e objetos de notificação de alteração são definidos como não sinal.
-   O estado de um temporizador de sincronização é definido como não sinal.
-   Os estados dos objetos de entrada do evento de redefinição manual, temporizador de redefinição manual, processo, thread e console não são afetados por uma função de espera.

## <a name="wait-functions-and-creating-windows"></a>Funções de espera e criação de Windows

Você precisa ter cuidado ao usar as funções de espera e o código que cria janelas direta ou indiretamente. Se um thread criar janelas, ele deverá processar mensagens. As transmissões de mensagem são enviadas para todas as janelas do sistema. Se você tiver um thread que usa uma função de espera sem intervalo de tempo-out, o sistema será deadlock. Dois exemplos de código que cria janelas indiretamente são DDE e a **função CoInitialize.** Portanto, se você tiver um thread que cria [**janelas, use MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)em vez das outras funções de espera.

 

 
