---
title: O que há de novo no Agendador de Tarefas
description: Lista de novas funcionalidades introduzidas por diferentes versões do Agendador de Tarefas.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Agendador de Tarefas Agendador de Tarefas, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769390"
---
# <a name="whats-new-in-task-scheduler"></a>O que há de novo no Agendador de Tarefas

As alterações a seguir resumem o que há de novo em versões diferentes do Agendador de Tarefas.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (e Windows Server 2016)

As seguintes Agendador de Tarefas alterações são introduzidas no Windows 10.

-   Quando a economia de bateria estiver ativada, as tarefas do Windows Agendador de Tarefas serão disparadas somente se a tarefa for:

    -   Não definido para **iniciar a tarefa somente se o computador estiver ocioso...** (a tarefa não usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Não definido para execução durante a manutenção automática (a tarefa não usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Está definido para ser **executado somente quando o usuário está conectado** (o Task [**LoginType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) é um **\_ \_ \_ token interativo de logon de tarefa** ou **\_ \_ grupo de logon de tarefa**)

    Todos os outros gatilhos serão atrasados até que a economia de bateria esteja desativada. Para obter mais informações sobre como acessar o status de economia de bateria em seu aplicativo, consulte [**\_ \_ status de energia do sistema**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   Por motivos de segurança, um usuário não administrador não pode exibir nem gerenciar uma tarefa do Windows Agendador de Tarefas que foi criada por outro usuário.

## <a name="windows-8"></a>Windows 8

As alterações Agendador de Tarefas 2,0 a seguir são introduzidas no Windows 8:

-   Suporte do PowerShell: os usuários podem gerenciar (criar, excluir, modificar, iniciar explicitamente, parar etc.) Tarefas do Windows Agendador de Tarefas usando o módulo do PowerShell do ScheduledTasks.
-   Senhas gerenciadas: os administradores podem usar o Active Directory contas de senha gerenciada como entidades de tarefa. Essas tarefas não exigem mais uma política de redefinição de senha imposta.
-   Alterações de API: introduziu duas novas configurações de tarefa com a interface [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .
    -   [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): as tarefas que usam essas configurações são tratadas como um novo tipo de tarefas agendadas que são invocadas durante o tempo de manutenção automática do so, de acordo com a periodicidade e a data limite especificadas.
    -   [**Volátil**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tarefas que são definidas como voláteis são sempre desabilitadas em uma inicialização de sistema operacional e devem ser reabilitadas explicitamente quando necessário. As tarefas voláteis são utilizadas pelos clusters de failover para garantir que apenas uma instância de tarefa seja agendada em um cluster por vez.
-   O mecanismo de agendamento unificado agora dá suporte aos seguintes recursos:
    -   Tipo de logon S4U, por meio do elemento [**Logontype**](taskschedulerschema-logontype-principaltype-element.md) .
    -   Valores de consulta XPath para gatilhos de evento, por meio do elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .
    -   Não permita o encerramento de uma tarefa, por meio do elemento [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .
-   Recursos preteridos nesta versão
    -   Ação: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (você pode usar [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) com o cmdlet [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) do [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)como uma solução alternativa).
    -   Ação: [**exmessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe o utilitário cmdline

## <a name="windows-7"></a>Windows 7

As seguintes Agendador de Tarefas 2,0 alterações são introduzidas no Windows 7:

-   Usando o mecanismo de agendamento unificado fornecido pelo sistema operacional subjacente.
-   Capacidade de rejeitar tarefas iniciais em sessões do trilho (integradas ao local) de aplicativos remotos.
-   Proteção de segurança de tarefa (somente para tarefas em execução como "serviço de rede" ou "serviço LOCAL"):

    -   Capacidade de atribuir um tipo de SID (identificador de segurança) de token de processo (por exemplo, irrestrito ou nenhum) a uma tarefa.
    -   Permitir que os desenvolvedores de tarefas solicitem o conjunto exato de privilégios exigidos por sua tarefa.

-   Alterações de API:

    -   Suporte à proteção de segurança de tarefas: o novo recurso de proteção de segurança de tarefas é introduzido com a nova interface IPrincipal2.
    -   Introduziu duas novas configurações de tarefa com a nova interface ITaskSettings2.

        -   DisallowStartOnRemoteAppSession: a nova configuração DisallowStartOnRemoteAppSession pode rejeitar uma tarefa de início se disparada em sessões do [trilho (integradas localmente) de aplicativos remotos](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .
        -   UseUnifiedSchedulingEngine: usar a configuração UseUnifiedSchedulingEngine fornece um comportamento coeso para tarefas e serviços do Windows, pois ele está sendo gerenciado de maneira uniforme por um mecanismo de agendamento comum em todo o sistema. Embora o uso de um mecanismo unificado seja recomendado, ele não oferece suporte a alguns dos recursos de Agendador de Tarefas. Se a combinação de propriedades não permitir a execução da tarefa em um mecanismo unificado, o registro de tal será rejeitado.
        -   Os recursos de tarefa que não são suportados pelo mecanismo de agendamento unificado incluem:

            -   Tipos de logon:

                -   [\_ \_ \_ token \_ ou senha de logon \_ interativo da tarefa](./taskschedulerschema-logontype-principaltype-element.md)

            -   Política de várias instâncias:

                -   [**as \_ instâncias de tarefa \_ param \_ existentes**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Ações:

                -   [Enviar email](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Exibir mensagem](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Configurações:

                -   [Configurações de rede de tarefas](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Não permitir o encerramento forçado da tarefa](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Gatilhos:

                -   [Limite de tempo de execução do gatilho](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Padrões de repetição para gatilhos de calendário]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valores de consulta XPath para gatilhos de eventos]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   Tipos de gatilhos [mensais](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) e [mensais do dia da semana](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)

## <a name="windows-vista"></a>Windows Vista

A API Agendador de Tarefas 2,0 deve ser usada no desenvolvimento de aplicativos que usam o serviço Agendador de Tarefas no Windows Vista. Para obter mais informações, consulte [Agendador de tarefas referência](task-scheduler-reference.md) e [usando o Agendador de tarefas](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP e Windows Server 2003

A API Agendador de Tarefas 2,0 não está disponível. Use Agendador de Tarefas 1,0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> </dl>

 

 
