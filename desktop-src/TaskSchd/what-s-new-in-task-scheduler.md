---
title: Novidades no Agendador de Tarefas
description: Lista de novas funcionalidades introduzidas por diferentes versões do Agendador de Tarefas.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Agendador de Tarefas Agendador de Tarefas , novidades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3592cc5efd08afe4737e9af429d52fa41216b6c756a64faeaa45f6cc5c0774b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354778"
---
# <a name="whats-new-in-task-scheduler"></a>Novidades no Agendador de Tarefas

As alterações a seguir resumem as novidades em diferentes versões do Agendador de Tarefas.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (e Windows Server 2016)

As seguintes Agendador de Tarefas são introduzidas no Windows 10.

-   Quando economia de bateria estiver ativado, Windows Agendador de Tarefas tarefas serão disparadas somente se a tarefa for:

    -   Não definido como **Iniciar a tarefa somente se o computador estiver ocioso...** (a tarefa não usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Não definido para ser executado durante a manutenção automática (a tarefa não usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   É definido como **Executar somente quando o usuário está** conectado (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) é **TASK \_ LOGON INTERACTIVE \_ \_ TOKEN** ou **TASK \_ LOGON \_ GROUP**)

    Todos os outros gatilhos são atrasados até economia de bateria está desligado. Para obter mais informações sobre como economia de bateria status em seu aplicativo, consulte [**SYSTEM \_ POWER \_ STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Para obter informações gerais sobre economia de bateria, [consulte economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   Por motivos de segurança, um usuário não administrador não pode exibir nem gerenciar uma Windows Agendador de Tarefas que foi criada por outro usuário.

## <a name="windows-8"></a>Windows 8

As seguintes Agendador de Tarefas 2.0 são introduzidas no Windows 8:

-   Suporte do PowerShell: os usuários podem gerenciar (criar, excluir, modificar, iniciar explicitamente, parar etc.) Windows Agendador de Tarefas tarefas usando o módulo do PowerShell ScheduledTasks.
-   Senhas gerenciadas: os administradores podem usar as contas de senha gerenciadas do Active Directory como entidades de tarefas. Essas tarefas não exigem mais uma política de redefinição de senha imposta.
-   Alterações de API: introduziu duas novas configurações de tarefa com a interface [**ITaskSettings3.**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3)
    -   [**MaintenanceSettings:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)tarefas que usam essas configurações são tratadas como um novo tipo de tarefas agendadas que são invocadas durante o tempo de manutenção automática do sistema operacional, de acordo com a periodicidade e a data limite especificadas.
    -   [**Volátil:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)as tarefas que são definidas como voláteis são sempre desabilitadas em uma inicialização do sistema operacional e devem ser habilitadas explicitamente novamente quando necessário. Tarefas voláteis são utilizadas pelos clusters de failover para garantir que apenas uma instância de tarefa seja agendada em um cluster por vez.
-   O mecanismo de agendamento unificado agora dá suporte aos seguintes recursos:
    -   Tipo de logon S4U, por meio do [**elemento LogonType.**](taskschedulerschema-logontype-principaltype-element.md)
    -   Valores de consulta XPath para gatilhos de evento, por meio [**do elemento ValueQueries.**](taskschedulerschema-valuequeries-eventtriggertype-element.md)
    -   Não permita o final rígido da tarefa por meio [**do elemento AllowHardTerminate.**](taskschedulerschema-allowhardterminate-settingstype-element.md)
-   Recursos preterido nesta versão
    -   Ação: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (você pode usar [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) com o cmdlet [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) como uma solução alternativa).
    -   Ação: [**showMessage.**](taskschedulerschema-showmessage-actiongroup-element.md)
    -   AT.exe utilitário de linha de cmdline

## <a name="windows-7"></a>Windows 7

As seguintes Agendador de Tarefas 2.0 são introduzidas no Windows 7:

-   Usando o mecanismo de agendamento unificado fornecido pelo sistema operacional subjacente.
-   Capacidade de rejeitar tarefas in início em sessões RAIL (Remote Applications Integrated Locally).
-   Proteção de segurança de tarefa (somente para tarefas executadas como "SERVIÇO DE REDE" ou "SERVIÇO LOCAL"):

    -   Capacidade de atribuir um tipo sid (identificador de segurança) de token de processo (por exemplo, irrestrito ou nenhum) a uma tarefa.
    -   Permitir que os desenvolvedores de tarefas solicitem o conjunto exato de privilégios que sua tarefa requer.

-   Alterações na API:

    -   Suporte à segurança da tarefa: o novo recurso de segurança de tarefa é introduzido com a nova interface IPrincipal2.
    -   Introduziu duas novas configurações de tarefa com a nova interface ITaskSettings2.

        -   DisallowStartOnRemoteAppSession: a nova configuração DisallowStartOnRemoteAppSession pode rejeitar um início de tarefa se disparado em sessões RAIL (Remote Applications Integrated [Locally).](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546)
        -   UseUnifiedSchedulingEngine: usar a configuração UseUnifiedSchedulingEngine fornece um comportamento coeso para tarefas e serviços do Windows porque está sendo gerenciado de maneira uniforme por um mecanismo de agendamento comum em todo o sistema. Embora o uso de um mecanismo unificado seja recomendado, ele não dá suporte a alguns dos Agendador de Tarefas recursos. Se a combinação de propriedades não permitir a execução da tarefa em um mecanismo unificado, o registro desse tipo será rejeitado.
        -   Os recursos de tarefa que não são suportados pelo mecanismo de agendamento unificado incluem:

            -   Tipos de logon:

                -   [TOKEN \_ INTERATIVO OU SENHA DO \_ \_ LOGON DA \_ \_ TAREFA](./taskschedulerschema-logontype-principaltype-element.md)

            -   Política de várias instâncias:

                -   [**AS \_ INSTÂNCIAS DE \_ TAREFA \_ PARAM DE EXISTIR**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Ações:

                -   [Enviar email](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Exibir mensagem](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Configurações:

                -   [Configurações de rede de tarefas](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Não permitir que a tarefa seja encerrada](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Gatilhos:

                -   [Limite de tempo de execução do gatilho](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Padrões de repetição para gatilhos de calendário]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valores de consulta XPath para gatilhos de evento]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Tipos de](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) gatilho mensal [e mensal do dia da](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) semana

## <a name="windows-vista"></a>Windows Vista

A API Agendador de Tarefas 2.0 deve ser usada no desenvolvimento de aplicativos que usam o serviço Agendador de Tarefas no Windows Vista. Para obter mais informações, [consulte Agendador de Tarefas e](task-scheduler-reference.md) Usando o [Agendador de Tarefas](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP e Windows Server 2003

A api Agendador de Tarefas 2.0 não está disponível. Use Agendador de Tarefas 1.0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> </dl>

 

 
