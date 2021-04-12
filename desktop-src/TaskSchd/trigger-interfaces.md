---
title: Interfaces de gatilho
description: As APIs que são usadas para gerenciar gatilhos variam de acordo com a versão do Agendador de Tarefas. No entanto, em ambos os casos, essas APIs permitem criar novos gatilhos, recuperar e atualizar gatilhos existentes e excluir gatilhos que não são mais necessários.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- gatilhos Agendador de Tarefas, interfaces
- disparadores Agendador de Tarefas, interfaces, descritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294620"
---
# <a name="trigger-interfaces"></a>Interfaces de gatilho

As APIs que são usadas para gerenciar gatilhos variam de acordo com a versão do Agendador de Tarefas. No entanto, em ambos os casos, essas APIs permitem criar novos gatilhos, recuperar e atualizar gatilhos existentes e excluir gatilhos que não são mais necessários.


Os aplicativos desenvolvidos usando Agendador de Tarefas 2,0 podem usar objetos e interfaces para criar, recuperar, modificar e excluir os gatilhos de uma tarefa.

Na ilustração a seguir, uma tarefa especifica uma coleção de gatilhos usando sua propriedade Triggers. Esta coleção contém uma ou mais APIs de gatilho individuais com cada API especificando um tipo de gatilho específico. Por exemplo, na ilustração abaixo, a coleção de gatilho contém um gatilho de inicialização, um gatilho de logon e um gatilho diário.

![interfaces de gatilho do Agendador de tarefas 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>APIs de objeto para desenvolvimento de scripts

Para obter mais informações sobre os métodos e as propriedades dos objetos usados para especificar gatilhos, consulte:

-   [**TaskDefinition**](taskdefinition.md)
-   [**Disparador**](triggercollection.md)
-   [**Of**](trigger.md)
-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>APIs de interfaces para desenvolvimento em C++

Para obter mais informações sobre os métodos e as propriedades das interfaces usadas para especificar gatilhos, consulte:

-   [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Agendador de Tarefas interfaces de gatilho 1,0

Os aplicativos existentes que são desenvolvidos usando Agendador de Tarefas 1,0 podem usar os métodos que estão disponíveis nas interfaces Agendador de Tarefas 1,0 para criar, recuperar, modificar e excluir os gatilhos de um [*item de trabalho*](w.md). No entanto, observe que todas as interfaces, enumerações e estruturas do Agendador de Tarefas 1,0 são obsoletas e não devem ser usadas para o desenvolvimento de novos aplicativos.

As duas interfaces que são usadas para fazer isso são mostradas na ilustração a seguir. A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) é usada para gerenciar todos os gatilhos associados a um item de trabalho (esse gerenciamento inclui a criação de um novo disparador para o item de trabalho). A interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) é usada para gerenciar um gatilho específico.

![interfaces de gatilho do Agendador de tarefas 1,0](images/tsktri2.png)

A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece métodos para criar um novo gatilho para um item de trabalho, recuperando o número de gatilhos associados a um item de trabalho, recuperando as [*estruturas de gatilho*](t.md) associadas ao item de trabalho, recuperando [*cadeias de caracteres de gatilho*](t.md) associadas ao item de trabalho e para excluir gatilhos.

Depois que o objeto de gatilho estiver disponível, você poderá usar a interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar a estrutura do gatilho e a cadeia de caracteres do gatilho e definir os critérios usados para acionar o gatilho. Essa interface é usada somente quando você está trabalhando com um [*objeto de gatilho de tarefa*](t.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Tipos de gatilho](trigger-types.md)
</dt> <dt>

[Estruturas de gatilho](trigger-structures.md)
</dt> </dl>

 

 