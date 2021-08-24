---
title: Tarefas
description: Uma tarefa é o trabalho agendado que o serviço Agendador de Tarefas executa.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tarefas Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f6122bcf32e0c3e242b6dce119432a9014718d4b65d19c613ce27794355491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517097"
---
# <a name="tasks"></a>Tarefas

Uma tarefa é o trabalho agendado que o serviço Agendador de Tarefas executa. Uma tarefa é composta por componentes diferentes, mas uma tarefa deve conter um gatilho que o Agendador de Tarefas usa para iniciar a tarefa e uma ação que descreve o trabalho que o Agendador de Tarefas executará.

Quando uma tarefa é criada, ela é armazenada em uma pasta de tarefas. As pastas de tarefas podem ser acessadas por meio da interface [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) para scripts) e as tarefas podem ser acessadas por meio da interface [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) para scripts) quando elas são criadas. Você pode alterar as ACLs (listas de controle de acesso) para tarefas e pastas de tarefas para conceder ou negar acesso a determinados usuários e grupos a uma tarefa ou pasta de tarefas. Isso pode ser feito usando o método [**IRegisteredTask::SetSecurityDescriptor,**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) o [**método ITaskFolder::SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) ou especificando um descritor de segurança quando uma tarefa é registrada usando o método [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ou [**RegisterTask.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)

> [!Note]  
> Se a conta sistema local tiver o acesso negado a um arquivo de tarefa ou pasta de tarefas, o serviço Agendador de Tarefas poderá produzir resultados inesperados.

 

## <a name="components-of-a-task"></a>Componentes de uma tarefa

A ilustração a seguir mostra os componentes da tarefa.

![componentes da tarefa](images/taskcomponents.png)

A lista a seguir contém uma breve descrição de cada componente de tarefa:

-   Gatilhos: Agendador de Tarefas usa gatilhos baseados em tempo ou evento para saber quando iniciar uma tarefa. Cada tarefa pode especificar um ou mais gatilhos para iniciar a tarefa.

    Para obter mais informações sobre gatilhos, consulte [Gatilhos de tarefa](task-triggers.md).

-   Ações: essas são as ações, o trabalho real, que é executado pela tarefa. Cada tarefa pode especificar uma ou mais ações para concluir seu trabalho.

    Para obter mais informações sobre ações, consulte [Ações de tarefa](task-actions.md).

-   Entidades de segurança: as entidades definem o contexto de segurança no qual a tarefa é executado. Por exemplo, uma entidade de entidade pode definir um usuário ou grupo de usuários específico que pode executar a tarefa.

    Para obter mais informações sobre entidades de segurança, consulte [Contextos de segurança para tarefas](security-contexts-for-running-tasks.md).

-   Configurações: essas são as configurações que o Agendador de Tarefas usa para executar a tarefa em relação a condições externas à própria tarefa. Por exemplo, essas configurações podem especificar a prioridade da tarefa em relação a outras tarefas, se várias instâncias da tarefa podem ser executadas, como a tarefa é tratada quando o computador está em uma condição ociosa e outras condições.

    Para obter mais informações sobre configurações de tarefa, consulte [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).

    > [!Note]  
    > Por padrão, uma tarefa será interrompida 72 horas depois de começar a ser executado. Você pode alterar isso alterando a [**configuração ExecutionTimeLimit.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit)

     

-   Informações de registro: essas são informações administrativas coletadas quando a tarefa é registrada. Por exemplo, essas informações descrevem o autor da tarefa, a data em que a tarefa foi registrada, uma descrição XML da tarefa e outras informações.

    Para obter mais informações sobre informações de registro de tarefa, consulte [Informações de registro de tarefa](task-registration-information.md).

-   Dados: esta é uma documentação adicional sobre a tarefa fornecida pelo autor da tarefa. Por exemplo, esses dados podem conter a Ajuda XML que pode ser usada pelos usuários quando eles executarem a tarefa.

## <a name="task-apis"></a>APIs de tarefa

Agendador de Tarefas 2.0 fornece dois conjuntos de APIs: um conjunto de interfaces e objetos de script para Agendador de Tarefas 2.0. Para obter mais informações, [consulte Agendador de Tarefas Referência de](task-scheduler-reference.md).

A compatibilidade da tarefa, [](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) definida por meio da propriedade Compatibilidade, só deverá ser definida como TASK COMPATIBILITY V1 se uma tarefa deve ser acessada ou modificada de um computador \_ do Windows \_ XP, Windows Server 2003 ou Windows 2000. Caso contrário, é recomendável que você use Agendador de Tarefas compatibilidade 2.0 porque ele tem mais recursos.

A partir do Agendador de Tarefas 2.0, a interface [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) para scripts) é usada como um ponto de partida para criar tarefas em pastas especificadas. A interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) para scripts) é usada para manter todos os componentes de uma tarefa, como configurações, ações e gatilhos. As APIs [**ITaskTrigger,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) fornecem propriedades que são usadas para definir os outros componentes da tarefa. Agendador de Tarefas 1.0 fornece a interface [**ITask,**](/windows/desktop/api/Mstask/nn-mstask-itask) que tem suporte apenas para compatibilidade com backward.

Para scripts, as interfaces Agendador de Tarefas são mapeadas para objetos de script que têm nomes, propriedades e métodos semelhantes. Por exemplo, o objeto de script [**TaskService**](taskservice.md) tem as mesmas propriedades e métodos que a interface [**ITaskService.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

Para obter mais informações e exemplos sobre como usar as interfaces Agendador de Tarefas, objetos de script e XML, consulte Usando o [Agendador de Tarefas](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Agendador de Tarefas tarefas 1.0

Uma Agendador de Tarefas tarefa 1.0 é qualquer tipo de aplicativo ou arquivo que o Agendador de Tarefas pode executar. Eles podem incluir qualquer um dos seguintes (conforme o suporte do sistema operacional no qual a tarefa será executada): aplicativos Win32, aplicativos Win16, aplicativos OS/2, aplicativos MS-DOS, arquivos em lotes (.bat), arquivos de \* comando ( .cmd) ou qualquer tipo de arquivo registrado \* corretamente.

Os dados que descrevem uma tarefa são mantidos em um arquivo de tarefa armazenado na pasta Tarefas Agendadas. Para obter mais informações, consulte [*Pasta tarefas agendadas*](s.md). O nome desses arquivos de tarefa inclui o nome da tarefa, seguido por uma extensão de nome de arquivo .job.

Para obter mais informações sobre como Agendador de Tarefas tarefas 1.0, consulte [Adicionando itens de trabalho](adding-work-items.md).

Para obter mais informações sobre como enumerar Agendador de Tarefas tarefas 1.0, consulte [Enumerando tarefas](enumerating-tasks.md).

Para um computador Windows Server 2003, Windows XP ou Windows 2000 para criar, monitorar ou controlar tarefas em um computador do Windows Vista, as seguintes operações devem ser concluídas no computador Windows Vista e o usuário que está chamando o método [**ITaskScheduler::SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) deve ser um membro do grupo Administradores no computador remoto Windows Vista.

**Para habilitar a exceção "Compartilhar Arquivo e Impressoras" Windows Firewall**

1.  Clique em **Iniciar** e em **Painel de Controle**.
2.  No **Painel de Controle**, clique em **Exibição Clássica** e clique duas vezes no ícone Windows **Firewall.**
3.  Na janela **Windows Firewall,** clique  na guia Exceções e marque a caixa de **seleção** Exceção de Compartilhamento de Arquivos e Impressoras.

**Para habilitar o serviço "Registro Remoto"**

-   Abra uma janela do Prompt de Comando e insira o seguinte comando: **net start "Remote Registry".**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Ações de tarefa](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




