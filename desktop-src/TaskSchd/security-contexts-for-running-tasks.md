---
title: Contextos de segurança para tarefas
description: As tarefas são registradas e executadas em um contexto de segurança específico.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6f49ef07818b1fe729fa96a2b5e0712979a17f300e4f411f96cefd2f3917f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738246"
---
# <a name="security-contexts-for-tasks"></a>Contextos de segurança para tarefas

As tarefas são registradas e executadas em um contexto de segurança específico. Os usuários podem criar aplicativos que registram, atualizem, excluam ou executam tarefas com êxito, mas o usuário deve fornecer as credenciais corretas quando uma tarefa é registrada e o aplicativo deve estar em execução em um processo com os privilégios corretos.

## <a name="specifying-credentials"></a>Especificando credenciais

Você pode especificar o contexto de segurança para uma tarefa especificando credenciais nos métodos [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para scripts) ou atribuindo uma entidade de segurança à propriedade principal de [**ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition.Principal**](taskdefinition-principal.md) para script). Se uma entidade de serviço for criada para uma definição de tarefa e, em seguida, a definição de tarefa for registrada usando o método **RegisterTaskDefinition** com credenciais diferentes especificadas nos parâmetros de método, as credenciais especificadas **no método RegisterTaskDefinition** substituirão as credenciais na entidade de entidade. Se uma entidade de serviço for criada para uma definição de tarefa usando XML e, em seguida, o XML da tarefa for registrado usando o método **RegisterTask** com credenciais diferentes especificadas nos parâmetros de método, as credenciais especificadas no **método RegisterTask** substituirão as credenciais na entidade de serviço.

Especifique uma conta de usuário ou grupo ao registrar uma tarefa ou especificar o princípio de uma tarefa. O contexto de segurança da conta de usuário ou grupo é usado para o contexto de segurança da tarefa. Nesses métodos e propriedades, você também define o tipo de logon. O tipo de logon é definido por uma das constantes na [**enumeração TASK \_ LOGON \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)

As tarefas registradas com o sinalizador TASK LOGON PASSWORD ou \_ \_ TASK \_ LOGON S4U serão lançadas somente se o usuário especificado tiver o Logon como privilégio \_ do Lote habilitado. Os usuários do grupo Administradores e Operadores de Backup têm esse privilégio habilitado por padrão.

Quando você chama o método [**ITaskService::Conexão**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService.Conexão**](taskservice-connect.md) para scripts), todas as chamadas de método subsequentes para o serviço Agendador de Tarefas usarão as credenciais que foram passadas para o **método Conexão.** Isso é importante a ser considerado ao registrar tarefas com um tipo de logon interativo. Quando você registra uma tarefa com o tipo de logon igual a TASK LOGON INTERACTIVE TOKEN e a tarefa não tem credenciais especificadas na propriedade Principal da definição da tarefa, especificada nos parâmetros para \_ \_ \_ [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)ou [](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)  especificada no XML passado para [**RegisterTask,**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)a tarefa será registrada com as credenciais do usuário que chamou o método Conexão.

## <a name="user-account-control-uac-security-for-tasks"></a>Segurança de UAC (Controle de Conta de Usuário) para tarefas

[O UAC](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (Controle de Conta de Usuário) permite que os usuários exerçam funcionalidades gerais, como executar programas e salvar e modificar dados sem expor privilégios administrativos. Por padrão, uma tarefa é executado com privilégios de baixo nível quando o UAC está ligado. As tarefas podem especificar que serão executadas com privilégios elevados ou privilégios baixos definindo um nível de privilégio da enumeração [**TASK \_ RUNLEVEL \_ TYPE**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) para a propriedade [**RunLevel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ([**Principal.RunLevel**](principal-runlevel.md) para script). O valor da **propriedade RunLevel** determina o nível de privilégio no qual as ações de uma tarefa serão executados. Se as ações de uma tarefa devem ter privilégios elevados para ser executado, você deve definir a propriedade **RunLevel** como **TASK \_ RUNLEVEL \_ HIGHEST.** Se uma tarefa for registrada usando o grupo Administradores para o contexto de segurança da tarefa, você também deverá definir a propriedade **RunLevel** como **TASK \_ RUNLEVEL \_ HIGHEST** se quiser executar a tarefa. Se uma tarefa for registrada usando a conta administrador integrado ou as contas sistema local ou serviço local, a propriedade \\ **RunLevel** será ignorada. O valor da propriedade também será ignorado se o UAC (Controle de Conta de Usuário) estiver desligado. O valor da **propriedade RunLevel** não afeta as permissões necessárias para executar ou excluir uma tarefa.

> [!Note]  
> Depois de atualizar um sistema operacional do Windows XP para o Windows Vista, as tarefas que foram registradas usando a conta administrador integrado no Windows XP terão a propriedade \\ [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) definida como **TASK \_ RUNLEVEL \_ LUA.** Isso pode fazer com que algumas tarefas falhem. Você pode atualizar essa propriedade manualmente para garantir que todas as tarefas serão executadas.

 

Em um processo de baixo privilégio, você não pode registrar uma tarefa com a propriedade [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a **TASK \_ RUNLEVEL \_ HIGHEST**, mas você pode registrar uma tarefa com a propriedade **RunLevel** igual a **TASK \_ RUNLEVEL \_ LUA**. As ações de tarefa serão executados com privilégios baixos. Você não tem permissão para registrar a tarefa como Builtin/Administrator, Sistema Local ou para um grupo.

Em um processo de privilégio elevado, você pode registrar uma tarefa com a propriedade [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a **TASK \_ RUNLEVEL \_ HIGHEST** ou **TASK \_ RUNLEVEL \_ LUA**. A tarefa será executado com um nível de privilégio decidido pela propriedade **RunLevel,** a menos que você esteja usando a conta de Administrador, caso em que a tarefa é executado com privilégios elevados.

Em um processo elevado, você pode registrar uma tarefa Agendador de Tarefas 1.0. O Agendador de Tarefas serviço definirá o nível de executar da tarefa como TASK RUNLEVEL HIGHEST e a tarefa será executado \_ \_ com privilégios elevados.

Em um processo de baixo privilégio, você também pode registrar uma Agendador de Tarefas 1.0. O Agendador de Tarefas serviço definirá o nível de executar da tarefa como TASK RUNLEVEL LUA e a tarefa será executado \_ \_ com privilégios baixos. Se essa tarefa for atualizada de um processo elevado, o nível de executar da tarefa permanecerá TASK \_ RUNLEVEL \_ LUA.

## <a name="security-for-registering-tasks"></a>Segurança para registrar tarefas

Ao registrar uma tarefa de uma conta que seja membro do grupo Administradores, você só precisará especificar uma senha ao registrar a tarefa nas seguintes situações:

-   Se você registrar a tarefa a ser executado no contexto de segurança da sua conta ou da conta de um usuário diferente e usar o sinalizador TASK LOGON PASSWORD no método \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
-   Se você registrar a tarefa a ser executado no contexto de segurança da conta de um usuário diferente e usar o sinalizador S4U DE LOGON DE TAREFA no \_ \_ método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Não é possível usar um grupo de usuários como o contexto de segurança de uma tarefa ao registrar a tarefa usando o sinalizador S4U DE LOGON DE TAREFA ou o sinalizador TASK LOGON PASSWORD no \_ \_ método \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Quando você registra uma tarefa de uma conta de usuário que não é membro do grupo Administradores, não é necessário especificar uma senha ao registrar a tarefa se você registrar a tarefa para ser executado no contexto de segurança da sua conta e usar o tipo de logon interativo ou S4U. Caso contrário, você precisará especificar uma senha ao registrar a tarefa. Além disso, você não pode registrar a tarefa usando a conta de Serviço Local ou usando um grupo para o contexto de segurança da tarefa.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Segurança para leitura, atualização, exclusão e execução de tarefas

Por padrão, um usuário que cria uma tarefa pode ler, atualizar, excluir e executar a tarefa. Um usuário deve ter permissão de gravação de arquivo em um arquivo de tarefa para atualizar uma tarefa, permissão de leitura de arquivo em um arquivo de tarefa para ler uma tarefa, excluir permissão em um arquivo de tarefa para excluir uma tarefa e permissão de execução de arquivo em uma tarefa para executar uma tarefa usando os métodos [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) ou [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask.Run**](registeredtask-run.md) e [**RunEx**](registeredtask-runex.md) para script). Os membros do grupo Administradores ou da conta SYSTEM podem ler, atualizar, excluir e executar tarefas. Os membros do grupo Usuários, da conta LocalService e da conta NetworkService só podem ler, atualizar, excluir e executar as tarefas que criaram. Esse comportamento padrão é alterado quando a DACL do arquivo de tarefa é alterada, nesse caso, a DACL define quais usuários têm permissão de gravação, leitura, execução e exclusão de arquivos. Para definir permissões para um arquivo de tarefa, use o método IRegisteredTask.SetSecurityDescriptor (RegisteredTask.SetSecurityDescriptor para scripts) ou defina o descritor de segurança ao registrar a tarefa usando os métodos [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Um usuário deve ter a permissão WriteDAC além das permissões de leitura/gravação para atualizar uma tarefa se a atualização da tarefa exigir uma alteração na DACL para a tarefa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Informações de registro de tarefa](task-registration-information.md)
</dt> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> <dt>

[Proteger a segurança da tarefa](task-security-hardening.md)
</dt> <dt>

[**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Propriedade Principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**TIPO \_ DE LOGON \_ DE TAREFA**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




