---
title: T (Agendador de Tarefas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499209"
---
# <a name="t-task-scheduler"></a>T (Agendador de Tarefas)

A B C D [E](e.md) F G H [i](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objetos de tarefa**
</dt> <dd>

Instâncias de um objeto que fornece métodos para gerenciar tarefas. Isso inclui métodos para configuração e recuperação de propriedades; executando, encerrando e excluindo tarefas; e criando novos gatilhos e recuperando gatilhos antigos.

O objeto Task é criado por chamadas para [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objetos do Agendador de tarefas**
</dt> <dd>

Instâncias de um objeto o representa o serviço Agendador de Tarefas. Este objeto dá suporte a duas interfaces: **IUnknown** e [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (atualmente, as tarefas são o único tipo de itens de trabalho com suporte no serviço Agendador de tarefas).

Os objetos do Agendador de tarefas são criados por chamadas para **CoCreateInstance**.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objetos de gatilho de tarefa**
</dt> <dd>

Instâncias de um objeto o fornece métodos para configurar e recuperar gatilhos de tarefa. Este objeto dá suporte a duas interfaces: **IUnknown** e [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).

Os objetos de gatilho de tarefa são criados por chamadas para [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: gettrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

Consulte também: *gatilhos*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tarefa**
</dt> <dd>

Qualquer item que o Agendador de Tarefas possa executar. Esses itens podem incluir qualquer um dos seguintes (conforme suportado pelo sistema operacional no qual a tarefa será executada): aplicativos de® Win32, aplicativos Win16, aplicativos do sistema operacional/2, aplicativos do MS-DOS®, arquivos em lotes ( \* . bat), arquivos de comando ( \* . cmd) ou qualquer tipo de arquivo registrado corretamente.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Pasta tarefas**
</dt> <dd>

A pasta que lista todos os arquivos de tarefas (atualmente, tarefas são os únicos itens de trabalho disponíveis). Esses arquivos contêm as informações sobre a tarefa. O nome desses arquivos reflete o nome da tarefa.

Você pode recuperar o local da pasta tarefas do registro obtendo dados para o seguinte valor:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**gatilhos**
</dt> <dd>

Um conjunto de critérios que, quando atendidos, fará com que uma tarefa seja executada. O Agendador de Tarefas fornece gatilhos baseados em tempo e eventos que podem especificar horários de início da tarefa, critérios de repetição e outros parâmetros.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**cadeias de caracteres de gatilho**
</dt> <dd>

Uma cadeia de caracteres que descreve o gatilho. Essa cadeia de caracteres é criada pelo serviço de Agendador de Tarefas e aparece na interface do usuário do Agendador de Tarefas em um formato semelhante a "at 14h todos os dias, começando em 5/11/97".

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**estruturas de gatilho**
</dt> <dd>

A estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) usada ao configurar ou recuperar os critérios que definem o gatilho. Os critérios incluem quando o gatilho será acionado e o tipo do gatilho.

</dd> </dl>

 

 




