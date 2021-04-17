---
title: Exemplo de gatilho de registro (XML)
description: O XML neste exemplo define uma tarefa que inicia o bloco de notas quando a tarefa é registrada.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "105813042"
---
# <a name="registration-trigger-example-xml"></a>Exemplo de gatilho de registro (XML)

O XML neste exemplo define uma tarefa que inicia o bloco de notas quando a tarefa é registrada.

Para registrar uma tarefa que é definida em XML, você pode usar a função [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripts) ou a ferramenta de linha de comando Schtasks.exe. Se você usar a ferramenta de Schtasks.exe (localizada no diretório C: \\ Windows \\ System32), poderá usar o comando a seguir para registrar a tarefa: **SCHTASKS/CREATE/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

> [!Note]  
> Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>Para definir uma tarefa para iniciar o bloco de notas no registro

O exemplo de XML a seguir mostra como definir uma tarefa com uma única ação de execução (iniciando bloco de notas), um único gatilho de registro que inicia a tarefa quando ela é registrada e várias outras configurações de tarefa que afetam o modo como a tarefa é manipulada pelo Agendador de Tarefas.

> [!Note]  
> Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Elementos do esquema TaskScheduler

Aqui estão alguns elementos importantes para ter em mente ao usar este exemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contém informações de registro sobre a tarefa.
-   [**Triggers**](taskschedulerschema-triggers-tasktype-element.md): define o gatilho que inicia a tarefa.
-   [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): define o gatilho de registro. Nesse caso, somente dois elementos filho são usados: os limites inicial e final que especificam quando o gatilho é ativado e desativado.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define o contexto de segurança em que uma tarefa é executada.
-   [**Configurações**](taskschedulerschema-settings-tasktype-element.md): define as configurações de tarefa que o Agendador de tarefas usa para executar a tarefa.
-   [**Ações**](taskschedulerschema-actions-tasktype-element.md): define as ações que a tarefa executa. Nesse caso, executar o bloco de notas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




