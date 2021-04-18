---
title: Tipos de gatilho
description: Os gatilhos baseados em tempo e eventos que são descritos abaixo permitem iniciar tarefas de várias maneiras.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- disparadores Agendador de Tarefas, tipos
- Agendador de Tarefas do gatilho de inicialização
- gatilho de inicialização Agendador de Tarefas, descrito
- Agendador de Tarefas do gatilho de registro
- gatilho de registro Agendador de Tarefas, descrito
- Agendador de Tarefas do gatilho de calendário
- Agendador de Tarefas do gatilho de calendário, descrito
- Agendador de Tarefas de gatilho diário
- Agendador de Tarefas de gatilho diário, descrito
- gatilho semanal Agendador de Tarefas
- gatilho semanal Agendador de Tarefas, descrito
- Agendador de Tarefas de gatilho mensal
- Agendador de Tarefas do gatilho mensal, descrito
- Agendador de Tarefas do gatilho monthlyDOW
- Agendador de Tarefas do gatilho monthlyDOW, descrito
- Agendador de Tarefas de gatilho de evento
- gatilho de evento Agendador de Tarefas, descrito
- Agendador de Tarefas do gatilho de logon
- gatilho de logon Agendador de Tarefas, descrito
- gatilho de ociosidade Agendador de Tarefas
- gatilho de ociosidade Agendador de Tarefas, descrito
- gatilho de dia da semana Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee1e846e4b2fa8138f675cdd39e926884d2bfae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792601"
---
# <a name="trigger-types"></a>Tipos de gatilho

Os gatilhos baseados em tempo e eventos que são descritos abaixo permitem iniciar tarefas de várias maneiras.

## <a name="task-scheduler-20-triggers"></a>Agendador de Tarefas gatilhos 2,0

Os tipos de gatilho a seguir são definidos pela enumeração [**\_ \_ TYPE2 do gatilho de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .

| Gatilho                                                                                                                                                                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gatilho de evento (gatilho baseado em evento) para desenvolvimento de scripts, consulte [**EventTrigger**](eventtrigger.md).<br/> Para desenvolvimento em C++, consulte [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Inicia a tarefa quando ocorre um evento específico do sistema.                                                                                                                                         |
| Gatilho de tempo (gatilho baseado em tempo) para desenvolvimento de scripts, consulte [**timetrigger**](timetrigger.md).<br/> Para desenvolvimento em C++, consulte [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Para desenvolvimento de XML, consulte [**elemento timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Inicia a tarefa em uma data e hora específicas.                                                                                                                                                 |
| Gatilho diário (gatilho de calendário baseado em tempo) para desenvolvimento de scripts, consulte [**DailyTrigger**](dailytrigger.md).<br/> Para desenvolvimento em C++, consulte [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Inicia a tarefa em um horário específico em um agendamento diário. Por exemplo, a tarefa começa às 8:00, todos os dias ou a cada dia.                                                                |
| Gatilho semanal (gatilho de calendário baseado em tempo) para desenvolvimento de scripts, consulte [**WeeklyTrigger**](weeklytrigger.md).<br/> Para desenvolvimento em C++, consulte [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Inicia a tarefa em um horário específico em um cronograma semanal. Por exemplo, a tarefa começa às 8:00 em um dia específico da semana a cada semana ou em um dia específico da semana a cada semana. |
| Gatilho mensal (gatilho de calendário baseado em tempo) para desenvolvimento de scripts, consulte [**MonthlyTrigger**](monthlytrigger.md).<br/> Para desenvolvimento em C++, consulte [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Inicia a tarefa em um horário específico em um agendamento mensal. Por exemplo, a tarefa começa às 8:00 em dias específicos do mês em meses específicos.                                          |
| Gatilho mensal (DOW) do dia da semana (gatilho de calendário baseado em tempo) para desenvolvimento de scripts, consulte [**MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Para desenvolvimento em C++, consulte [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Inicia a tarefa em um horário específico em uma agenda mensal de dia da semana. Por exemplo, a tarefa começa às 8:00 em dias específicos da semana, semanas do mês e meses do ano.      |
| Gatilho de ociosidade (gatilho baseado em evento) para desenvolvimento de scripts, consulte [**IdleTrigger**](idletrigger.md).<br/> Para desenvolvimento em C++, consulte [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia a tarefa quando o computador entra em um estado ocioso.                                                                                                                                      |
| Gatilho de registro (gatilho baseado em evento) para desenvolvimento de scripts, consulte [**RegistrationTrigger**](registrationtrigger.md).<br/> Para desenvolvimento em C++, consulte [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Inicia a tarefa quando a tarefa é registrada ou atualizada.                                                                                                                                      |
| Gatilho de inicialização (gatilho baseado em evento) para desenvolvimento de scripts, consulte [**BootTrigger**](boottrigger.md).<br/> Para desenvolvimento em C++, consulte [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia a tarefa quando o sistema é inicializado.                                                                                                                                                   |
| Gatilho de logon (gatilho baseado em evento) para desenvolvimento de scripts, consulte [**LogonTrigger**](logontrigger.md).<br/> Para desenvolvimento em C++, consulte [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Inicia a tarefa quando um usuário faz logon.                                                                                                                                                         |
| Gatilho de alteração de estado de sessão (gatilho baseado em evento) para desenvolvimento de scripts, consulte [**SessionStateChangeTrigger**](sessionstatechangetrigger.md).<br/> Para desenvolvimento em C++, consulte [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger).<br/> Para o desenvolvimento XML, consulte o [**elemento SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Inicia a tarefa quando uma sessão de Terminal Server muda de estado.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Agendador de Tarefas gatilhos 1,0

Os tipos de gatilho a seguir são definidos pela enumeração de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) . Para implementar qualquer um dos seguintes gatilhos, consulte a estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .

-   Depois do gatilho: inicia a tarefa uma única vez.
-   Gatilho diário: inicia a tarefa em um intervalo diário.
-   Gatilho semanal: inicia a tarefa em um agendamento semanal.
-   Gatilho mensal: inicia a tarefa em um agendamento mensal.
-   Gatilho de DOW mensal: inicia a tarefa em uma agenda mensal de dia da semana.
-   No gatilho ocioso: inicia a tarefa quando o computador está em um estado ocioso.
-   Gatilho de início do sistema: inicia a tarefa quando o computador é inicializado.
-   Gatilho de logon: inicia a tarefa quando um usuário específico faz logon.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Interfaces de gatilho](trigger-interfaces.md)
</dt> <dt>

[Estruturas de gatilho](trigger-structures.md)
</dt> </dl>

 

