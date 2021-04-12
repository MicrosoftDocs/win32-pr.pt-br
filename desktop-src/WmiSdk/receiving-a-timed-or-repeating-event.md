---
description: Um evento cronometrado ou repetitivo é um evento que ocorre em uma data e hora específicas, ou repetidamente em intervalos regulares. Por exemplo, um evento pode ocorrer à meia-noite em apenas 2 de dezembro de 2015, ou uma vez por semana às terças-feiras às 2:31 PM.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Recebendo um evento cronometrado ou repetido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165220"
---
# <a name="receiving-a-timed-or-repeating-event"></a>Recebendo um evento cronometrado ou repetido

Um evento cronometrado ou repetitivo é um evento que ocorre em uma data e hora específicas, ou repetidamente em intervalos regulares. Por exemplo, um evento pode ocorrer à meia-noite em apenas 2 de dezembro de 2015, ou uma vez por semana às terças-feiras às 2:31 PM.

A tabela a seguir lista as diferentes classes que são usadas para criar um evento cronometrado ou repetido.



| Classe                                                                                            | Descrição                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ Localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [ **\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | Modelo de evento padrão da Microsoft.<br/> Para obter mais informações, consulte [criando um evento de timer com Win32 \_ localtime ou Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).<br/> |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                               | Técnica herdada.<br/> Para obter mais informações, consulte [criando um evento de timer com \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).<br/>                                             |



 

Se você quiser agendar uma tarefa ou trabalho para ocorrer em um momento específico ou repetidamente, use a classe [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) e seus métodos. Essa classe representa um trabalho criado com o comando AT em uma janela de comando de **Iniciar** e **executar**, ou das **tarefas agendadas** no **painel de controle**.

 

