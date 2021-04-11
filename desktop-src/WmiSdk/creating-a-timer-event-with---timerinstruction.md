---
description: Você cria um evento de temporizador criando uma instância de classes derivadas da \_ \_ classe TimerInstruction em qualquer namespace WMI.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Criando um evento de temporizador com __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e502678525569dae272edb7b03c0916db25edfd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171452"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Criando um evento de temporizador com \_ \_ TimerInstruction

Você cria um evento de temporizador criando uma instância de classes derivadas da classe [**\_ \_ TimerInstruction**](--timerinstruction.md) em qualquer namespace WMI. Em seguida, o WMI gera o evento de temporizador no momento apropriado. Se você perder um evento de temporizador devido ao tempo de inatividade do computador, o WMI o notificará sobre o evento perdido. O WMI dá suporte a eventos de timer para compatibilidade com versões anteriores e para cenários em que você deve saber quantos eventos foram perdidos desde o último evento entregue. No entanto, para a maioria dos eventos de timer, você deve criar um filtro de eventos para [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime). Para obter mais informações, consulte [criando um evento de timer com Win32 \_ localtime ou Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

O procedimento a seguir descreve como criar e receber um evento de temporizador com \_ \_ TimerInstruction.

**Para criar e receber um evento de temporizador com \_ \_ TimerInstruction**

1.  Crie uma instância das classes [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) ou [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

    As classes [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) são derivadas da classe [**\_ \_ TimerInstruction**](--timerinstruction.md) , que contém uma cadeia de caracteres exclusiva atribuída pelo desenvolvedor que identifica o tipo de evento de timer. A classe **\_ \_ TimerInstruction** também contém um valor que especifica se o WMI deve enviar uma notificação Belated se o evento timer ocorrer quando o WMI não estiver disponível.

    Use [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) para enviar eventos de timer absolutos, que ocorrem em uma data específica em um momento específico. Use [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) para enviar eventos de timer de intervalo, que ocorrem regularmente.

2.  Defina seu aplicativo para receber uma instância de [**\_ \_ TimerEvent**](--timerevent.md) .

    Para gerar um evento, o WMI cria uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) e encaminha a instância para o consumidor. A instância **\_ \_ TimerEvent** contém o identificador de instrução do temporizador do consumidor. A instância também contém um valor que especifica quantas vezes o WMI deve enviar a notificação de eventos de timer durante qualquer intervalo quando o WMI não puder acessar o consumidor.

 

 
