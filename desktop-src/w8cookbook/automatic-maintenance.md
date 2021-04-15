---
title: Manutenção automática (manual de compatibilidade para Windows)
description: Manutenção automática
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104454411"
---
# <a name="automatic-maintenance"></a>Manutenção automática

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

O Windows depende da execução da caixa de entrada e da atividade de manutenção de terceiros para grande parte de seu valor agregado, incluindo Windows Update e desfragmentação automática de disco, bem como atualizações e verificações de antivírus. Além disso, as empresas frequentemente usam atividades de manutenção, como a verificação de NAP (proteção de acesso à rede), para ajudar a reforçar os padrões de segurança em todas as estações de trabalho empresariais.

A atividade de manutenção no Windows foi projetada para ser executada em segundo plano com interação limitada do usuário e impacto mínimo sobre desempenho e eficiência energética. No entanto, no Windows 7 e em versões anteriores, a eficiência de desempenho e energia ainda é afetada devido à programação não determinística e amplamente variada das várias atividades de manutenção no Windows. A capacidade de resposta aos usuários é reduzida quando a atividade de manutenção é executada enquanto os usuários estão usando o computador ativamente. Os aplicativos também solicitam que o usuário atualize seu software e execute a manutenção em segundo plano e direcione os usuários para várias experiências, incluindo a central de ações, o painel de controle, o Windows Update, o snap-in do MMC Agendador de Tarefas e controles de terceiros.

O objetivo da manutenção automática é combinar todas as atividades de manutenção em segundo plano no Windows e ajudar os desenvolvedores de terceiros a adicionar suas atividades de manutenção ao Windows sem afetar negativamente o desempenho e a eficiência energética. Além disso, a manutenção automática permite que os usuários e as empresas controlem o agendamento e a configuração da atividade de manutenção.

**Principais problemas**

A manutenção automática foi projetada para resolver esses problemas com a atividade de manutenção no Windows:

-   Agendamento do prazo
-   Conflitos de utilização de recursos
-   Eficiência energética
-   Transparência para o usuário

## <a name="functionality"></a>Funcionalidade

A manutenção automática facilita a eficiência de ociosidade e permite que todas as atividades sejam executadas de maneira oportuna e priorizada. Ele também ajuda a habilitar a visibilidade unificada e controlar a atividade de manutenção e permite que desenvolvedores de terceiros adicionem sua atividade de manutenção ao Windows sem afetar negativamente o desempenho e a eficiência de energia. Para fazer isso, ele fornece um modo totalmente automático, modo iniciado pelo usuário, parada automática, prazos e notificações e controle corporativo. Cada um é descrito abaixo.

**Modo totalmente automático**

Esse modo padrão permite o agendamento inteligente durante o tempo ocioso do PC e em horários agendados — a execução e a pausa automática da atividade de manutenção sem nenhuma intervenção do usuário. O usuário pode definir uma agenda semanal ou diária. Toda a atividade de manutenção é não interativa e é executada silenciosamente.

O computador é retomado automaticamente do modo de suspensão quando o sistema provavelmente não está em uso, respeitando a política de gerenciamento de energia, que, no caso de laptops, usa como padrão permitir a ativação somente se ela estiver em corrente ALTERNAda. Recursos completos do sistema com alta potência são usados para concluir a atividade de manutenção o mais rápido possível. Se o sistema tiver sido retomado da suspensão para manutenção automática, ele será solicitado a retornar ao estado de suspensão.

Todas as interações de usuário necessárias relacionadas a atividades como a configuração são executadas fora da execução de manutenção automática.

**Modo iniciado pelo usuário**

Se os usuários precisarem se preparar para a viagem, esperar ter energia na bateria por um tempo prolongado ou se desejar otimizar o desempenho e a capacidade de resposta, eles terão a opção de iniciar a manutenção automática sob demanda. Os usuários podem configurar atributos de manutenção automática, incluindo a agenda de execução automática. Eles podem exibir o status atual da execução de manutenção automática e podem interromper a manutenção automática, se necessário.

**Parada automática**

A manutenção automática automaticamente interrompe as atividades de manutenção em execução no momento se o usuário começar a interagir com o computador. A atividade de manutenção será retomada quando o sistema retornar ao status ocioso.

> [!Note]  
> Todas as atividades na manutenção automática devem dar suporte à interrupção em 2 segundos ou menos. O usuário deve ser notificado de que a atividade foi interrompida.

 

**Prazos e notificações**

A atividade de manutenção crítica deve ser executada em uma janela de tempo predefinida. Se as tarefas críticas não puderem ser executadas dentro do horário designado, a manutenção automática iniciará automaticamente a execução na próxima oportunidade de ociosidade do sistema disponível. No entanto, se o estado da tarefa permanecer atrás do prazo, a manutenção automática notificará o usuário sobre a atividade e fornecerá uma opção para uma execução manual da manutenção automática. Todas as tarefas agendadas para manutenção serão executadas, embora as tarefas mais privantes tenham precedência. Essa atividade pode afetar o desempenho e a capacidade de resposta do sistema; Portanto, a manutenção automática notificará o usuário de que a atividade de manutenção crítica está em execução.

**Controle corporativo**

Os profissionais de ti empresariais devem ser capazes de determinar quando a manutenção automática é executada em seus sistemas Windows, impor essa agenda via interfaces de gerenciamento padronizadas e recuperar dados de eventos sobre o status das tentativas de execução de manutenção automática. Além disso, os profissionais de ti devem ser capazes de invocar remotamente uma atividade de manutenção automática específica por meio de interfaces de gerenciamento padrão. Cada vez que a manutenção automática é executada, o relatório de status, incluindo notificações quando a manutenção automática não pôde ser executada porque o usuário pausou a atividade manualmente, é executado. Os profissionais de ti devem considerar a movimentação de scripts de logon para a manutenção automática para ajudar a tornar a experiência de logon do usuário mais rápida.

## <a name="creating-an-automatic-maintenance-task"></a>Criando uma tarefa de manutenção automática

Esta seção detalha como os desenvolvedores podem criar uma tarefa usando uma definição de tarefa em linguagem XML ou C. Tenha em mente que a atividade de manutenção não deve iniciar nenhuma interface do usuário que exija interação do usuário, pois a manutenção automática é completamente silenciosa e é executada quando o usuário não está presente. Na verdade, se o usuário interage com o computador durante a manutenção automática, todas as tarefas em andamento serão encerradas até o próximo período ocioso.

**Usando XML**

Agendador de Tarefas inclui uma ferramenta de linha de comando interna, schtasks.exe, que pode importar uma definição de tarefa em formato XML. O esquema para definição de tarefa está documentado em https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . Veja abaixo um exemplo de uma tarefa de manutenção automática definida em XML.


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



Para salvar a tarefa em um computador Windows, salve o XML acima como um arquivo de texto e use esta linha de comando:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Usando C**

Uma tarefa de manutenção automática também pode ser criada usando código C. Abaixo está um exemplo de código que pode ser usado para definir as configurações de manutenção automática de uma tarefa:


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a>Validando tarefas

Valide se a tarefa foi criada com êxito e é executada como parte da manutenção.

**Validando a criação da tarefa**

Use esta linha de comando para exportar a definição de tarefa para um arquivo e garantir que a definição da tarefa seja conforme o esperado:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Validando a execução da tarefa**

Execute esta linha de comando para iniciar a tarefa e validar que a interface do usuário do Agendador de Tarefas (Taskschd. msc) mostra que a tarefa foi executada:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Recursos

-   [Agenda de tarefas 2,0](/previous-versions/bb756979(v=msdn.10))

 

 