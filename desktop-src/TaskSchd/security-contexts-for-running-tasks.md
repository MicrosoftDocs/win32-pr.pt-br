---
title: Contextos de segurança para tarefas
description: As tarefas são registradas e executadas em um contexto de segurança específico.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329f354518daeb11a5f330ae3fdc2c332b66d5c3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365641"
---
# <a name="security-contexts-for-tasks"></a>Contextos de segurança para tarefas

As tarefas são registradas e executadas em um contexto de segurança específico. Os usuários podem criar aplicativos que registram, atualizam, excluem ou executam tarefas com êxito, mas o usuário deve fornecer as credenciais corretas quando uma tarefa é registrada e o aplicativo deve estar em execução em um processo com os privilégios corretos.

## <a name="specifying-credentials"></a>Especificando credenciais

Você pode especificar o contexto de segurança para uma tarefa especificando as credenciais nos métodos [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para scripts) ou atribuindo uma entidade de segurança à [**Propriedade principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition. principal**](taskdefinition-principal.md) para scripts). Se uma entidade de segurança for criada para uma definição de tarefa e a definição de tarefa for registrada usando o método **RegisterTaskDefinition** com credenciais diferentes especificadas nos parâmetros do método, as credenciais especificadas no método **RegisterTaskDefinition** substituirão as credenciais na entidade de segurança. Se uma entidade de segurança for criada para uma definição de tarefa usando XML e, em seguida, o XML para a tarefa for registrado usando o método **RegisterTask** com credenciais diferentes especificadas nos parâmetros do método, as credenciais especificadas no método **RegisterTask** substituirão as credenciais na entidade de segurança.

Você especifica uma conta de usuário ou grupo ao registrar uma tarefa ou especificar o princípio de uma tarefa. O contexto de segurança da conta de usuário ou grupo é usado para o contexto de segurança da tarefa. Nesses métodos e propriedades, você também define o tipo de logon. O tipo de logon é definido por uma das constantes na enumeração [**do \_ \_ tipo de logon da tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) .

As tarefas registradas com a senha de logon da tarefa \_ \_ ou o \_ \_ sinalizador S4U de logon da tarefa serão iniciados somente se o usuário especificado tiver o privilégio fazer logon como lote habilitado. Os administradores e os usuários do grupo operadores de backup têm esse privilégio habilitado por padrão.

Quando você chama o método [**o ITaskService:: Connect**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService. Connect**](taskservice-connect.md) for Scripting), todas as chamadas de método subsequentes para o serviço de Agendador de tarefas usarão as credenciais que foram passadas para o método **Connect** . Isso é importante considerar ao registrar tarefas com um tipo de logon interativo. Quando você registra uma tarefa com o tipo de logon igual ao \_ token interativo de logon de tarefa \_ \_ e a tarefa não tem credenciais especificadas na propriedade [**principal**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) da definição de tarefa, especificada nos parâmetros para [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)ou especificada no XML que é passado para [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask), a tarefa será registrada com as credenciais do usuário que chamou o método **Connect** .

## <a name="user-account-control-uac-security-for-tasks"></a>Segurança do controle de conta de usuário (UAC) para tarefas

O UAC ( [controle de conta de usuário](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ) permite que os usuários exerçam funcionalidades gerais, como executar programas e salvar e modificar dados sem expor privilégios administrativos. Por padrão, uma tarefa é executada com privilégios de nível baixo quando o UAC é ativado. As tarefas podem especificar que serão executadas com privilégios elevados ou privilégios baixos definindo um nível de privilégio da enumeração [**de \_ \_ tipo de tarefa runlevel**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) para a [**Propriedade runlevel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ([**principal. runlevel**](principal-runlevel.md) para scripts). O valor da propriedade **runlevel** determina o nível de privilégio no qual as ações de uma tarefa serão executadas. Se as ações de uma tarefa precisarem ter privilégios elevados para serem executadas, você deverá definir a propriedade **runlevel** para **Task \_ runlevel \_ mais alta**. Se uma tarefa for registrada usando o grupo Administradores para o contexto de segurança da tarefa, você também deverá definir a propriedade **runlevel** para **Task \_ runlevel \_ mais alta** se desejar executar a tarefa. Se uma tarefa for registrada usando a \\ conta de administrador interno ou o sistema local ou as contas de serviço local, a propriedade **runlevel** será ignorada. O valor da propriedade também será ignorado se o UAC (controle de conta de usuário) estiver desativado. O valor da propriedade **runlevel** não afeta as permissões necessárias para executar ou excluir uma tarefa.

> [!Note]  
> Depois de atualizar um sistema operacional do Windows XP para o Windows Vista, as tarefas que foram registradas usando a \\ conta de administrador interno no Windows XP terão a propriedade [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) definida como **Task \_ runlevel \_ lua**. Isso pode fazer com que algumas tarefas falhem. Você pode atualizar essa propriedade manualmente para garantir que todas as tarefas sejam executadas.

 

De um processo de baixo privilégio, não é possível registrar uma tarefa com a propriedade [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual à **tarefa \_ runlevel \_ mais alta**, mas você pode registrar uma tarefa com a propriedade **runlevel** igual a **Task \_ runlevel \_ lua**. As ações da tarefa serão executadas com privilégios baixos. Você não tem permissão para registrar a tarefa como interno/administrador, sistema local ou para um grupo.

A partir de um processo de privilégio elevado, você pode registrar uma tarefa com a propriedade [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) igual a **Task \_ runlevel \_ mais alta** ou a **tarefa \_ runlevel \_ lua**. A tarefa será executada com um nível de privilégio decidido pela propriedade **runlevel** , a menos que você esteja usando a conta de administrador; nesse caso, a tarefa é executada com privilégios elevados.

Em um processo elevado, você pode registrar uma tarefa Agendador de Tarefas 1,0. O serviço de Agendador de Tarefas definirá o nível de execução da tarefa para a tarefa \_ runlevel \_ mais alta e a tarefa será executada com privilégios elevados.

De um processo de baixo privilégio, você também pode registrar uma tarefa Agendador de Tarefas 1,0. O serviço de Agendador de Tarefas definirá o nível de execução da tarefa para a tarefa \_ runlevel \_ lua e a tarefa será executada com privilégios baixos. Se essa tarefa for atualizada a partir de um processo elevado, o nível de execução da tarefa permanecerá a tarefa \_ runlevel \_ lua.

## <a name="security-for-registering-tasks"></a>Segurança para registrar tarefas

Ao registrar uma tarefa de uma conta que seja membro do grupo Administradores, você só precisa especificar uma senha durante o registro da tarefa nas seguintes situações:

-   Se você registrar a tarefa para ser executada no contexto de segurança de sua conta ou em uma conta de usuário diferente e usar o \_ sinalizador de senha de logon da tarefa \_ no método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .
-   Se você registrar a tarefa para ser executada no contexto de segurança de uma conta de usuário diferente e usar o \_ sinalizador de logon S4U da tarefa \_ no método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Você não pode usar um grupo de usuários como o contexto de segurança de uma tarefa ao registrar a tarefa usando o sinalizador de registro de tarefa de \_ logon \_ ou o sinalizador de senha de logon da tarefa \_ \_ no método [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Ao registrar uma tarefa de uma conta de usuário que não seja membro do grupo Administradores, você não precisará especificar uma senha ao registrar a tarefa se registrar a tarefa para ser executada no contexto de segurança de sua conta e usar o tipo de logon interativo ou S4U. Caso contrário, você precisará especificar uma senha ao registrar a tarefa. Além disso, você não pode registrar a tarefa usando a conta de serviço local ou usando um grupo para o contexto de segurança da tarefa.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Segurança para leitura, atualização, exclusão e execução de tarefas

Por padrão, um usuário que cria uma tarefa pode ler, atualizar, excluir e executar a tarefa. Um usuário deve ter permissão de gravação de arquivo em um arquivo de tarefa para atualizar uma tarefa, permissão de leitura de arquivo em um arquivo de tarefa para ler uma tarefa, excluir permissão em um arquivo de tarefa para excluir uma tarefa e executar a permissão File em uma tarefa para executar uma tarefa usando os métodos [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) ou [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask. Run**](registeredtask-run.md) e [**RunEx**](registeredtask-runex.md) para scripts). Os membros do grupo Administradores ou da conta sistema podem ler, atualizar, excluir e executar tarefas. Os membros do grupo usuários, a conta LocalService e a conta NetworkService só podem ler, atualizar, excluir e executar as tarefas que eles criaram. Esse comportamento padrão é alterado quando a DACL do arquivo de tarefa é alterada; nesse caso, a DACL define quais usuários têm a permissão gravar, ler, executar e excluir. Para definir permissões para um arquivo de tarefa, use o método IRegisteredTask. SetSecurityDescriptor (RegisteredTask. SetSecurityDescriptor para script) ou defina o descritor de segurança ao registrar a tarefa usando os métodos [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ou [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Um usuário deve ter a permissão WriteDAC além das permissões de leitura/gravação para atualizar uma tarefa se a atualização da tarefa exigir uma alteração na DACL para a tarefa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Informações de registro da tarefa](task-registration-information.md)
</dt> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> <dt>

[Proteção de segurança de tarefa](task-security-hardening.md)
</dt> <dt>

[**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Propriedade principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**\_tipo de logon da tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




