---
title: Tarefas
description: Uma tarefa é o trabalho agendado que o serviço Agendador de Tarefas executa.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tarefas Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810116"
---
# <a name="tasks"></a>Tarefas

Uma tarefa é o trabalho agendado que o serviço Agendador de Tarefas executa. Uma tarefa é composta por diferentes componentes, mas uma tarefa deve conter um gatilho que o Agendador de Tarefas usa para iniciar a tarefa e uma ação que descreve o trabalho que o Agendador de Tarefas executará.

Quando uma tarefa é criada, ela é armazenada em uma pasta de tarefas. As pastas de tarefas podem ser acessadas por meio da interface [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) para scripts), e as tarefas podem ser acessadas por meio da interface [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) para scripts) quando elas são criadas. Você pode alterar as listas de controle de acesso (ACLs) para tarefas e pastas de tarefas a fim de conceder ou negar a determinados usuários e grupos o acesso a uma tarefa ou pasta de tarefas. Isso pode ser feito usando o método [**IRegisteredTask:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , o método [**ITaskFolder:: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) ou especificando um descritor de segurança quando uma tarefa é registrada usando o método [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ou [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .

> [!Note]  
> Se a conta do sistema local tiver acesso negado a um arquivo de tarefa ou pasta de tarefas, o serviço de Agendador de Tarefas poderá produzir resultados inesperados.

 

## <a name="components-of-a-task"></a>Componentes de uma tarefa

A ilustração a seguir mostra os componentes da tarefa.

![componentes da tarefa](images/taskcomponents.png)

A lista a seguir contém uma breve descrição de cada componente de tarefa:

-   Gatilhos: Agendador de Tarefas usa gatilhos de evento ou baseados em tempo para saber quando iniciar uma tarefa. Cada tarefa pode especificar um ou mais gatilhos para iniciar a tarefa.

    Para obter mais informações sobre gatilhos, consulte [disparadores de tarefas](task-triggers.md).

-   Ações: essas são as ações, o trabalho real, que é executado pela tarefa. Cada tarefa pode especificar uma ou mais ações para concluir seu trabalho.

    Para obter mais informações sobre ações, consulte [ações de tarefas](task-actions.md).

-   Entidades: as entidades definem o contexto de segurança no qual a tarefa é executada. Por exemplo, uma entidade de segurança pode definir um usuário ou grupo de usuários específico que possa executar a tarefa.

    Para obter mais informações sobre entidades, consulte [contextos de segurança para tarefas](security-contexts-for-running-tasks.md).

-   Configurações: essas são as configurações que o Agendador de Tarefas usa para executar a tarefa em relação às condições que são externas à própria tarefa. Por exemplo, essas configurações podem especificar a prioridade da tarefa em relação a outras tarefas, se várias instâncias da tarefa podem ser executadas, como a tarefa é tratada quando o computador está em uma condição ociosa e outras condições.

    Para obter mais informações sobre configurações de tarefas, consulte [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for Scripting).

    > [!Note]  
    > Por padrão, uma tarefa será interrompida em 72 horas depois de começar a ser executada. Você pode alterar isso alterando a configuração [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .

     

-   Informações de registro: são informações administrativas que são coletadas quando a tarefa é registrada. Por exemplo, essas informações descrevem o autor da tarefa, a data em que a tarefa foi registrada, uma descrição XML da tarefa e outras informações.

    Para obter mais informações sobre informações de registro de tarefas, consulte [informações de registro da tarefa](task-registration-information.md).

-   Dados: essa é uma documentação adicional sobre a tarefa fornecida pelo autor da tarefa. Por exemplo, esses dados podem conter ajuda XML que pode ser usada pelos usuários quando eles executam a tarefa.

## <a name="task-apis"></a>APIs de tarefa

O Agendador de Tarefas 2,0 fornece dois conjuntos de APIs: um conjunto de interfaces e objetos de script para Agendador de Tarefas 2,0. Para obter mais informações, consulte [referência de Agendador de tarefas](task-scheduler-reference.md).

A compatibilidade de tarefas, que é definida por meio da propriedade de [**compatibilidade**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , só deve ser definida como compatibilidade de tarefas \_ \_ v1 se uma tarefa precisar ser acessada ou modificada de um computador com Windows XP, Windows Server 2003 ou Windows 2000. Caso contrário, é recomendável que você use a Agendador de Tarefas a compatibilidade 2,0 porque ela tem mais recursos.

A partir do Agendador de Tarefas 2,0, a interface [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) para scripts) é usada como um ponto de partida para criar tarefas em pastas especificadas. A interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) para scripts) é usada para manter todos os componentes de uma tarefa, como as configurações, as ações e os gatilhos. As APIs [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)e [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) fornecem propriedades que são usadas para definir os outros componentes da tarefa. Agendador de Tarefas 1,0 fornece a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , que tem suporte apenas para compatibilidade com versões anteriores.

Para scripts, as interfaces de Agendador de Tarefas são mapeadas para objetos de script que têm nomes, propriedades e métodos semelhantes. Por exemplo, o objeto de script [**TaskService**](taskservice.md) tem as mesmas propriedades e métodos que a interface [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

Para obter mais informações e exemplos sobre como usar as interfaces de Agendador de Tarefas, os objetos de script e o XML, consulte [usando o Agendador de tarefas](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Agendador de Tarefas tarefas 1,0

Uma tarefa Agendador de Tarefas 1,0 é qualquer tipo de aplicativo ou de arquivo que o Agendador de Tarefas possa executar. Eles podem incluir qualquer um dos seguintes (conforme suportado pelo sistema operacional no qual a tarefa será executada): aplicativos Win32, aplicativos Win16, aplicativos do sistema operacional/2, aplicativos do MS-DOS, arquivos em lotes ( \* . bat), arquivos de comando ( \* . cmd) ou qualquer tipo de arquivo registrado corretamente.

Os dados que descrevem uma tarefa são mantidos em um arquivo de tarefa armazenado na pasta tarefas agendadas. Para obter mais informações, consulte [*pasta tarefas agendadas*](s.md). O nome desses arquivos de tarefas inclui o nome da tarefa, seguido por uma extensão de nome de arquivo. Job.

Para obter mais informações sobre como adicionar Agendador de Tarefas tarefas 1,0, consulte [adicionando itens de trabalho](adding-work-items.md).

Para obter mais informações sobre como enumerar por meio de tarefas Agendador de Tarefas 1,0, consulte [enumerando tarefas](enumerating-tasks.md).

Para um computador com Windows Server 2003, Windows XP ou Windows 2000 para criar, monitorar ou controlar tarefas em um computador com Windows Vista, as seguintes operações devem ser concluídas no computador com Windows Vista e o usuário que está chamando o método [**ITaskScheduler:: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) deve ser membro do grupo Administradores no computador remoto do Windows Vista.

**Para habilitar a exceção "compartilhar arquivos e impressoras" no firewall do Windows**

1.  Clique em **Iniciar** e em **Painel de Controle**.
2.  No **painel de controle**, clique em **exibição clássica** e clique duas vezes no ícone **Firewall do Windows** .
3.  Na janela **Firewall do Windows** , clique na guia **exceções** e selecione caixa de seleção de **exceção de compartilhamento de arquivos e impressoras** .

**Para habilitar o serviço "registro remoto"**

-   Abra uma janela de prompt de comando e digite o seguinte comando: **net start "registro remoto"**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Ações de tarefas](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**O ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




