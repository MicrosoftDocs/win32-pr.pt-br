---
title: Criando uma tarefa usando o exemplo NewWorkItem
description: Ao criar uma tarefa, você usará duas interfaces de Agendador de Tarefas ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- criando itens de trabalho Agendador de Tarefas
- Agendador de Tarefas de itens de trabalho, criando tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294288"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Criando uma tarefa usando o exemplo NewWorkItem

Ao criar uma tarefa, você usará duas interfaces Agendador de Tarefas: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Você deve fornecer um nome exclusivo para a tarefa, o identificador de classe do objeto de tarefa e o identificador de interface de **ITask**. O identificador de classe e o identificador de interface são mostrados no exemplo de código após este tópico.

> [!Note]  
> Você também pode criar uma tarefa chamando [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Quando você faz essa rota, é sua responsabilidade criar uma instância do objeto de **tarefa** (que dá suporte à interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ) e, em seguida, adicionar a tarefa com o nome que você fornecer.

 

> [!Note]  
> Por padrão, somente um membro do grupo Administradores, operadores de backup ou operadores de servidor pode criar tarefas no Windows Server 2003. Um membro do grupo Administradores pode alterar o descritor de segurança da pasta de tarefas do Windows \\ para permitir que outras pessoas criem tarefas.

 

O nome que você fornece para a tarefa deve ser exclusivo na pasta tarefas agendadas. Se já existir uma tarefa com o mesmo nome, [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) retornará o \_ arquivo de erro \_ . Se você receber esse valor de retorno, deverá especificar um nome diferente e tentar criar a tarefa novamente.

O procedimento a seguir descreve como criar uma nova tarefa de item de trabalho.

**Para criar uma nova tarefa de item de trabalho**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) para criar uma nova tarefa. (Esse método retorna um ponteiro para uma interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
3.  Salve a nova tarefa em disco chamando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão com suporte da interface **ITask** .)
4.  Chame **ITask:: Release** para liberar todos os recursos. (Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para obter um exemplo de código de  | Consulte                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Criando uma única tarefa | [Exemplo de código C/C++: criando uma tarefa usando NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 