---
description: Este tópico descreve como criar, identificar, definir e excluir temporizadores.
ms.assetid: 509a6fc4-ddee-4ff4-88a2-25dad4c48c2f
title: Sobre temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3163dbfd5357de516e0202665cd76d017335593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922832"
---
# <a name="about-timers"></a>Sobre temporizadores

Este tópico descreve como criar, identificar, definir e excluir temporizadores. Um aplicativo usa um temporizador para agendar um evento para uma janela depois que um tempo especificado tiver decorrido. Cada vez que o intervalo especificado (ou valor de tempo limite) para um temporizador expira, o sistema notifica a janela associada ao temporizador. Como a precisão de um temporizador depende da taxa de relógio do sistema e da frequência com que o aplicativo recupera mensagens da fila de mensagens, o valor de tempo limite é aproximado.

Este tópico inclui as seções a seguir.

-   [Operações de temporizador](#timer-operations)
-   [Temporizador de alta resolução](#high-resolution-timer)
-   [Objetos de timer que esperam](#waitable-timer-objects)
-   [Tópicos relacionados](#related-topics)

## <a name="timer-operations"></a>Operações de temporizador

Os aplicativos criam temporizadores usando a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Um novo temporizador começa a cronometrar o intervalo assim que ele é criado. Um aplicativo pode alterar o valor de tempo limite de um temporizador usando **SetTimer** e pode destruir um temporizador usando a função [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) . Para usar os recursos do sistema com eficiência, os aplicativos devem destruir temporizadores que não são mais necessários.

Cada temporizador tem um identificador exclusivo. Ao criar um temporizador, um aplicativo pode especificar um identificador ou fazer com que o sistema crie um valor exclusivo. O primeiro parâmetro de uma mensagem de [**\_ temporizador do WM**](wm-timer.md) contém o identificador do temporizador que postou a mensagem.

Se você especificar um identificador de janela na chamada para [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer), o aplicativo associará o temporizador a essa janela. Sempre que o valor de tempo limite para o temporizador expira, o sistema posta uma mensagem de [**\_ temporizador do WM**](wm-timer.md) na janela associada ao temporizador. Se nenhum identificador de janela for especificado na chamada para **SetTimer**, o aplicativo que criou o temporizador deverá monitorar sua fila de mensagens para mensagens de **\_ temporizador do WM** e expedir para a janela apropriada. Se você especificar uma função de retorno de chamada [**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc) , o procedimento de janela padrão chamará a função de retorno de chamada ao processar o **\_ temporizador do WM**. Portanto, você precisa enviar mensagens no thread de chamada, mesmo quando você usa **TimerProc** em vez de processar **o \_ temporizador do WM**.

Se você precisar ser notificado quando um temporizador decorrer, use um temporizador que poderá ser aguardado. Para obter mais informações, consulte [objetos de timer de espera](/windows/desktop/Sync/waitable-timer-objects).

## <a name="high-resolution-timer"></a>Temporizador de High-Resolution

Um contador é um termo geral usado na programação para se referir a uma variável de incremento. Alguns sistemas incluem um contador de desempenho de alta resolução que fornece tempos decorridos de alta resolução.

Se houver um contador de desempenho de alta resolução no sistema, você poderá usar a função [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) para expressar a frequência, em contagens por segundo. O valor da contagem é dependente do processador. Em alguns processadores, por exemplo, a contagem pode ser a taxa de ciclo do relógio do processador.

A função [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) recupera o valor atual do contador de desempenho de alta resolução. Ao chamar essa função no início e no final de uma seção do código, um aplicativo usa basicamente o contador como um temporizador de alta resolução. Por exemplo, suponha que [**QueryPerformanceFrequency**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancefrequency) indica que a frequência do contador de desempenho de alta resolução é de 50.000 contagens por segundo. Se o aplicativo chamar **QueryPerformanceCounter** imediatamente antes e imediatamente após a seção do código ser cronometrado, os valores do contador poderão ser 1500 contagens e 3500 contagens, respectivamente. Esses valores indicam que .04 segundos (contagens de 2000) decorridos enquanto o código foi executado.

## <a name="waitable-timer-objects"></a>Objetos de timer que esperam

Um objeto de timer de espera é um objeto de sincronização cujo estado é definido como sinalizado quando o tempo de espera especificado chega. Há dois tipos de temporizadores esperados que podem ser criados: redefinição manual e sincronização. Um temporizador de qualquer tipo também pode ser um temporizador periódico.

Um thread usa a função [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ou [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) para criar um objeto de temporizador. O thread de criação especifica se o temporizador é um temporizador de redefinição manual ou um temporizador de sincronização. O thread de criação pode especificar um nome para o objeto de timer. Os threads em outros processos podem abrir um identificador para um temporizador existente especificando seu nome em uma chamada para a função [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Qualquer thread com um identificador para um objeto de timer pode usar uma das funções Wait para aguardar que o estado do timer seja definido como signaled.

Para obter mais informações sobre como usar objetos de temporizador de espera para a sincronização de threads, consulte [objetos de timer de espera](/windows/desktop/Sync/waitable-timer-objects).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando temporizadores](using-timers.md)
</dt> </dl>

 

 
