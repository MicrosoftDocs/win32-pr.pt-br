---
title: Criando uma tarefa usando o exemplo NewWorkItem
description: Ao criar uma tarefa, você usará duas interfaces Agendador de Tarefas ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- criando itens de trabalho Agendador de Tarefas
- itens de trabalho Agendador de Tarefas , criando tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d0e0d216c5aaccee6a51cbac939b2b3bfa421338e12d66ffdd3b8cf055862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139579"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Criando uma tarefa usando o exemplo NewWorkItem

Ao criar uma tarefa, você usará duas interfaces Agendador de Tarefas: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Você deve fornecer um nome exclusivo para a tarefa, o identificador de classe do objeto de tarefa e o identificador de interface de **ITask.** O identificador de classe e o identificador de interface são mostrados no exemplo de código após este tópico.

> [!Note]  
> Você também pode criar uma tarefa chamando [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Quando você faz essa rota, é sua responsabilidade criar uma instância do objeto **Task** (que dá suporte à interface [**ITask)**](/windows/desktop/api/Mstask/nn-mstask-itask) e, em seguida, adicionar a tarefa com o nome que você fornecer.

 

> [!Note]  
> Por padrão, somente um membro do grupo Administradores, Operadores de Backup ou Operadores de Servidor pode criar tarefas no Windows Server 2003. Um membro do grupo Administradores pode alterar o descritor de segurança da pasta Windows Tarefa para permitir que \\ outras pessoas criem tarefas.

 

O nome que você fornece para a tarefa deve ser exclusivo na pasta Tarefas Agendadas. Se uma tarefa com o mesmo nome já existir, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) retornará ERROR \_ FILE \_ EXISTS. Se você receber esse valor de retorno, deverá especificar um nome diferente e tentar criar a tarefa novamente.

O procedimento a seguir descreve como criar uma nova tarefa de item de trabalho.

**Para criar uma nova tarefa de item de trabalho**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Este exemplo presume que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) para criar uma nova tarefa. (Esse método retorna um ponteiro para uma interface [**ITask.)**](/windows/desktop/api/Mstask/nn-mstask-itask)
3.  Salve a nova tarefa no disco chamando [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface COM padrão com suporte pela interface **ITask.)**
4.  Chame **ITask::Release para** liberar todos os recursos. (Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um [**método IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para um exemplo de código de  | Consulte                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Criando uma única tarefa | [Exemplo de código C/C++: criando uma tarefa usando NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 