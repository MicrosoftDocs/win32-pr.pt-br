---
title: Tipos de gatilho
description: Os gatilhos baseados em tempo e baseados em eventos descritos abaixo permitem que você inicie tarefas de várias maneiras.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- gatilhos Agendador de Tarefas , tipos
- gatilho de inicialização Agendador de Tarefas
- gatilho de inicialização Agendador de Tarefas , descrito
- gatilho de registro Agendador de Tarefas
- gatilho de registro Agendador de Tarefas , descrito
- gatilho de calendário Agendador de Tarefas
- gatilho de calendário Agendador de Tarefas , descrito
- gatilho diário Agendador de Tarefas
- gatilho diário Agendador de Tarefas , descrito
- gatilho semanal Agendador de Tarefas
- gatilho semanal Agendador de Tarefas , descrito
- gatilhos mensais Agendador de Tarefas
- monthly trigger Agendador de Tarefas , descrito
- gatilho monthlyDOW Agendador de Tarefas
- monthlyDOW trigger Agendador de Tarefas , descrito
- gatilho de evento Agendador de Tarefas
- event trigger Agendador de Tarefas , descrito
- logon trigger Agendador de Tarefas
- logon trigger Agendador de Tarefas , descrito
- gatilho ocioso Agendador de Tarefas
- gatilho ocioso Agendador de Tarefas , descrito
- gatilho do dia da semana Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0e09b6ecc1ac3c817f374e70c6756fa09afc78ccaac7e549f3f04ad074c8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099686"
---
# <a name="trigger-types"></a>Tipos de gatilho

Os gatilhos baseados em tempo e baseados em eventos descritos abaixo permitem que você inicie tarefas de várias maneiras.

## <a name="task-scheduler-20-triggers"></a>Agendador de Tarefas gatilhos 2.0

Os seguintes tipos de gatilho são definidos pela [**enumeração TASK \_ TRIGGER \_ TYPE2.**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)

| Gatilho                                                                                                                                                                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gatilho de evento (gatilho baseado em evento) Para desenvolvimento de scripts, [**consulte EventTrigger**](eventtrigger.md).<br/> Para desenvolvimento em C++, consulte [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Para desenvolvimento XML, consulte [**Elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Inicia a tarefa quando ocorre um evento específico do sistema.                                                                                                                                         |
| Gatilho de tempo (gatilho baseado em tempo)Para desenvolvimento de scripts, consulte [**TimeTrigger**](timetrigger.md).<br/> Para desenvolvimento em C++, consulte [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Para desenvolvimento XML, consulte [**Elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Inicia a tarefa em uma data e hora específicas.                                                                                                                                                 |
| Gatilho diário (gatilho de calendário baseado em tempo)Para desenvolvimento de scripts, consulte [**DailyTrigger**](dailytrigger.md).<br/> Para desenvolvimento em C++, consulte [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Para desenvolvimento XML, consulte [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Inicia a tarefa em um horário específico em uma agenda diária. Por exemplo, a tarefa começa às 8h todos os dias ou todos os outros dias.                                                                |
| Gatilho semanal (gatilho de calendário baseado em tempo)Para desenvolvimento de scripts, consulte [**WeeklyTrigger**](weeklytrigger.md).<br/> Para desenvolvimento em C++, consulte [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Para desenvolvimento XML, consulte [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Inicia a tarefa em um momento específico em uma agenda semanal. Por exemplo, a tarefa começa às 8h em um dia específico da semana toda semana ou em um dia específico da semana a cada outra semana. |
| Gatilho mensal (gatilho de calendário baseado em tempo)Para desenvolvimento de scripts, [**consulte MonthlyTrigger**](monthlytrigger.md).<br/> Para desenvolvimento em C++, consulte [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Para desenvolvimento XML, consulte [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Inicia a tarefa em um momento específico em um agendamento mensal. Por exemplo, a tarefa começa às 8h em dias específicos do mês em meses específicos.                                          |
| Gatilho do DOW (dia da semana mensal) (gatilho de calendário baseado em tempo)Para desenvolvimento de scripts, consulte [**MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Para desenvolvimento em C++, consulte [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Para desenvolvimento XML, consulte [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Inicia a tarefa em um horário específico em uma agenda mensal do dia da semana. Por exemplo, a tarefa começa às 8h em dias específicos da semana, semanas do mês e meses do ano.      |
| Gatilho ocioso (gatilho baseado em evento)Para o desenvolvimento de scripts, consulte [**IdleTrigger**](idletrigger.md).<br/> Para desenvolvimento em C++, consulte [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger).<br/> Para desenvolvimento XML, consulte [**Elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia a tarefa quando o computador entra em um estado ocioso.                                                                                                                                      |
| Gatilho de registro (gatilho baseado em evento)Para desenvolvimento de scripts, consulte [**RegistrationTrigger**](registrationtrigger.md).<br/> Para desenvolvimento em C++, consulte [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger).<br/> Para desenvolvimento XML, consulte [**Elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Inicia a tarefa quando a tarefa é registrada ou atualizada.                                                                                                                                      |
| Gatilho de inicialização (gatilho baseado em evento)Para desenvolvimento de scripts, consulte [**BootTrigger**](boottrigger.md).<br/> Para desenvolvimento em C++, consulte [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Para desenvolvimento XML, consulte [**Elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia a tarefa quando o sistema é inicializado.                                                                                                                                                   |
| Gatilho de logon (gatilho baseado em evento)Para desenvolvimento de scripts, consulte [**LogonTrigger**](logontrigger.md).<br/> Para desenvolvimento em C++, consulte [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Para desenvolvimento XML, consulte [**Elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Inicia a tarefa quando um usuário faz login.                                                                                                                                                         |
| Gatilho de alteração de estado de sessão (gatilho baseado em evento)Para o desenvolvimento de scripts, [**consulte SessionStateChangeTrigger**](sessionstatechangetrigger.md).<br/> Para desenvolvimento em C++, consulte [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger).<br/> Para desenvolvimento XML, consulte [**Elemento SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Inicia a tarefa quando uma sessão do Servidor de Terminal altera o estado.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Agendador de Tarefas gatilhos 1.0

Os seguintes tipos de gatilho são definidos pela [**enumeração TASK \_ TRIGGER \_ TYPE.**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) Para implementar qualquer um dos gatilhos a seguir, consulte a estrutura [**TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)

-   Gatilho uma vez: inicia a tarefa uma única vez.
-   Gatilho diário: inicia a tarefa em um intervalo diário.
-   Gatilho semanal: inicia a tarefa em uma agenda semanal.
-   Gatilho mensal: inicia a tarefa em uma agenda mensal.
-   Gatilho do DOW mensal: inicia a tarefa em um agendamento mensal do dia da semana.
-   Em Gatilho ocioso: inicia a tarefa quando o computador está em um estado ocioso.
-   Gatilho de inicialização do sistema: inicia a tarefa quando o computador é inicializado.
-   Gatilho de logon: inicia a tarefa quando um usuário específico faz logon.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Interfaces de gatilho](trigger-interfaces.md)
</dt> <dt>

[Estruturas de gatilho](trigger-structures.md)
</dt> </dl>

 

