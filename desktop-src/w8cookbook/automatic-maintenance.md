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
# <a name="automatic-maintenance"></a><span data-ttu-id="fd04a-103">Manutenção automática</span><span class="sxs-lookup"><span data-stu-id="fd04a-103">Automatic Maintenance</span></span>

## <a name="platforms"></a><span data-ttu-id="fd04a-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="fd04a-104">Platforms</span></span>

<span data-ttu-id="fd04a-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="fd04a-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="fd04a-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd04a-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="fd04a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd04a-107">Description</span></span>

<span data-ttu-id="fd04a-108">O Windows depende da execução da caixa de entrada e da atividade de manutenção de terceiros para grande parte de seu valor agregado, incluindo Windows Update e desfragmentação automática de disco, bem como atualizações e verificações de antivírus.</span><span class="sxs-lookup"><span data-stu-id="fd04a-108">Windows depends on execution of inbox and third party maintenance activity for much of its value-add, including Windows Update, and automatic disk defragmentation, as well as antivirus updates and scans.</span></span> <span data-ttu-id="fd04a-109">Além disso, as empresas frequentemente usam atividades de manutenção, como a verificação de NAP (proteção de acesso à rede), para ajudar a reforçar os padrões de segurança em todas as estações de trabalho empresariais.</span><span class="sxs-lookup"><span data-stu-id="fd04a-109">Additionally, enterprises frequently use maintenance activity such as Network Access Protection (NAP) scanning to help enforce security standards on all enterprise workstations.</span></span>

<span data-ttu-id="fd04a-110">A atividade de manutenção no Windows foi projetada para ser executada em segundo plano com interação limitada do usuário e impacto mínimo sobre desempenho e eficiência energética.</span><span class="sxs-lookup"><span data-stu-id="fd04a-110">Maintenance activity in Windows is designed to run in the background with limited user interaction and minimal impact to performance and energy efficiency.</span></span> <span data-ttu-id="fd04a-111">No entanto, no Windows 7 e em versões anteriores, a eficiência de desempenho e energia ainda é afetada devido à programação não determinística e amplamente variada das várias atividades de manutenção no Windows.</span><span class="sxs-lookup"><span data-stu-id="fd04a-111">However, in Windows 7 and earlier versions, performance and energy efficiency are still impacted due to the non-deterministic and widely varied schedule of the multiple maintenance activities in Windows.</span></span> <span data-ttu-id="fd04a-112">A capacidade de resposta aos usuários é reduzida quando a atividade de manutenção é executada enquanto os usuários estão usando o computador ativamente.</span><span class="sxs-lookup"><span data-stu-id="fd04a-112">Responsiveness to users is reduced when maintenance activity runs while users are actively using the computer.</span></span> <span data-ttu-id="fd04a-113">Os aplicativos também solicitam que o usuário atualize seu software e execute a manutenção em segundo plano e direcione os usuários para várias experiências, incluindo a central de ações, o painel de controle, o Windows Update, o snap-in do MMC Agendador de Tarefas e controles de terceiros.</span><span class="sxs-lookup"><span data-stu-id="fd04a-113">Apps also frequently ask the user to update their software and run background maintenance, and direct users to multiple experiences, including Action Center, Control Panel, Windows Update, Task Scheduler MMC snap-in, and third-party controls.</span></span>

<span data-ttu-id="fd04a-114">O objetivo da manutenção automática é combinar todas as atividades de manutenção em segundo plano no Windows e ajudar os desenvolvedores de terceiros a adicionar suas atividades de manutenção ao Windows sem afetar negativamente o desempenho e a eficiência energética.</span><span class="sxs-lookup"><span data-stu-id="fd04a-114">The goal of Automatic Maintenance is to combine all background maintenance activity in Windows and help third-party developers add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="fd04a-115">Além disso, a manutenção automática permite que os usuários e as empresas controlem o agendamento e a configuração da atividade de manutenção.</span><span class="sxs-lookup"><span data-stu-id="fd04a-115">Additionally, Automatic Maintenance enables users as well as enterprises to be in control of maintenance activity scheduling and configuration.</span></span>

<span data-ttu-id="fd04a-116">**Principais problemas**</span><span class="sxs-lookup"><span data-stu-id="fd04a-116">**Key problems**</span></span>

<span data-ttu-id="fd04a-117">A manutenção automática foi projetada para resolver esses problemas com a atividade de manutenção no Windows:</span><span class="sxs-lookup"><span data-stu-id="fd04a-117">Automatic Maintenance is designed to address these problems with maintenance activity in Windows:</span></span>

-   <span data-ttu-id="fd04a-118">Agendamento do prazo</span><span class="sxs-lookup"><span data-stu-id="fd04a-118">Deadline scheduling</span></span>
-   <span data-ttu-id="fd04a-119">Conflitos de utilização de recursos</span><span class="sxs-lookup"><span data-stu-id="fd04a-119">Resource utilization conflicts</span></span>
-   <span data-ttu-id="fd04a-120">Eficiência energética</span><span class="sxs-lookup"><span data-stu-id="fd04a-120">Energy efficiency</span></span>
-   <span data-ttu-id="fd04a-121">Transparência para o usuário</span><span class="sxs-lookup"><span data-stu-id="fd04a-121">Transparency to the user</span></span>

## <a name="functionality"></a><span data-ttu-id="fd04a-122">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="fd04a-122">Functionality</span></span>

<span data-ttu-id="fd04a-123">A manutenção automática facilita a eficiência de ociosidade e permite que todas as atividades sejam executadas de maneira oportuna e priorizada.</span><span class="sxs-lookup"><span data-stu-id="fd04a-123">Automatic Maintenance facilitates idle efficiency and permits all activity to run in a timely and prioritized fashion.</span></span> <span data-ttu-id="fd04a-124">Ele também ajuda a habilitar a visibilidade unificada e controlar a atividade de manutenção e permite que desenvolvedores de terceiros adicionem sua atividade de manutenção ao Windows sem afetar negativamente o desempenho e a eficiência de energia.</span><span class="sxs-lookup"><span data-stu-id="fd04a-124">It also helps enable unified visibility and control over maintenance activity, and allows third-party developers to add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="fd04a-125">Para fazer isso, ele fornece um modo totalmente automático, modo iniciado pelo usuário, parada automática, prazos e notificações e controle corporativo.</span><span class="sxs-lookup"><span data-stu-id="fd04a-125">To do this, it provides a fully automatic mode, user-initiated mode, automatic stop, deadlines and notification, and enterprise control.</span></span> <span data-ttu-id="fd04a-126">Cada um é descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="fd04a-126">These are each described below.</span></span>

<span data-ttu-id="fd04a-127">**Modo totalmente automático**</span><span class="sxs-lookup"><span data-stu-id="fd04a-127">**Fully automatic mode**</span></span>

<span data-ttu-id="fd04a-128">Esse modo padrão permite o agendamento inteligente durante o tempo ocioso do PC e em horários agendados — a execução e a pausa automática da atividade de manutenção sem nenhuma intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="fd04a-128">This default mode enables intelligent scheduling during PC idle-time and at scheduled times—the execution and automatic pausing of maintenance activity without any user intervention.</span></span> <span data-ttu-id="fd04a-129">O usuário pode definir uma agenda semanal ou diária.</span><span class="sxs-lookup"><span data-stu-id="fd04a-129">The user can set a weekly or daily schedule.</span></span> <span data-ttu-id="fd04a-130">Toda a atividade de manutenção é não interativa e é executada silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="fd04a-130">All maintenance activity is non-interactive and executes silently.</span></span>

<span data-ttu-id="fd04a-131">O computador é retomado automaticamente do modo de suspensão quando o sistema provavelmente não está em uso, respeitando a política de gerenciamento de energia, que, no caso de laptops, usa como padrão permitir a ativação somente se ela estiver em corrente ALTERNAda.</span><span class="sxs-lookup"><span data-stu-id="fd04a-131">The computer automatically is resumed from sleep when the system is not likely to be in use, respecting the Power Management policy, which in the case of laptops, defaults to allow wake-up only if it is on AC power.</span></span> <span data-ttu-id="fd04a-132">Recursos completos do sistema com alta potência são usados para concluir a atividade de manutenção o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="fd04a-132">Full system resources at high power are used to complete the maintenance activity as quickly as possible.</span></span> <span data-ttu-id="fd04a-133">Se o sistema tiver sido retomado da suspensão para manutenção automática, ele será solicitado a retornar ao estado de suspensão.</span><span class="sxs-lookup"><span data-stu-id="fd04a-133">If the system was resumed from sleep for Automatic Maintenance, it is requested to return to sleep.</span></span>

<span data-ttu-id="fd04a-134">Todas as interações de usuário necessárias relacionadas a atividades como a configuração são executadas fora da execução de manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="fd04a-134">Any required user interactions related to activities such as configuration are performed outside of Automatic Maintenance execution.</span></span>

<span data-ttu-id="fd04a-135">**Modo iniciado pelo usuário**</span><span class="sxs-lookup"><span data-stu-id="fd04a-135">**User-initiated mode**</span></span>

<span data-ttu-id="fd04a-136">Se os usuários precisarem se preparar para a viagem, esperar ter energia na bateria por um tempo prolongado ou se desejar otimizar o desempenho e a capacidade de resposta, eles terão a opção de iniciar a manutenção automática sob demanda.</span><span class="sxs-lookup"><span data-stu-id="fd04a-136">If users need to prepare for travel, expect to be on battery power for a prolonged time, or wish to optimize for performance and responsiveness, they have the option of initiating Automatic Maintenance on demand.</span></span> <span data-ttu-id="fd04a-137">Os usuários podem configurar atributos de manutenção automática, incluindo a agenda de execução automática.</span><span class="sxs-lookup"><span data-stu-id="fd04a-137">Users can configure Automatic Maintenance attributes, including the automatic run schedule.</span></span> <span data-ttu-id="fd04a-138">Eles podem exibir o status atual da execução de manutenção automática e podem interromper a manutenção automática, se necessário.</span><span class="sxs-lookup"><span data-stu-id="fd04a-138">They can view the current status of Automatic Maintenance execution, and they can stop Automatic Maintenance if needed.</span></span>

<span data-ttu-id="fd04a-139">**Parada automática**</span><span class="sxs-lookup"><span data-stu-id="fd04a-139">**Automatic stop**</span></span>

<span data-ttu-id="fd04a-140">A manutenção automática automaticamente interrompe as atividades de manutenção em execução no momento se o usuário começar a interagir com o computador.</span><span class="sxs-lookup"><span data-stu-id="fd04a-140">Automatic Maintenance automatically stops currently running maintenance activities if the user starts interacting with the computer.</span></span> <span data-ttu-id="fd04a-141">A atividade de manutenção será retomada quando o sistema retornar ao status ocioso.</span><span class="sxs-lookup"><span data-stu-id="fd04a-141">Maintenance activity will resume when the system returns to idle status.</span></span>

> [!Note]  
> <span data-ttu-id="fd04a-142">Todas as atividades na manutenção automática devem dar suporte à interrupção em 2 segundos ou menos.</span><span class="sxs-lookup"><span data-stu-id="fd04a-142">All activities in Automatic Maintenance must support stopping in 2 seconds or less.</span></span> <span data-ttu-id="fd04a-143">O usuário deve ser notificado de que a atividade foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="fd04a-143">The user should be notified that the activity has been stopped.</span></span>

 

<span data-ttu-id="fd04a-144">**Prazos e notificações**</span><span class="sxs-lookup"><span data-stu-id="fd04a-144">**Deadlines and notification**</span></span>

<span data-ttu-id="fd04a-145">A atividade de manutenção crítica deve ser executada em uma janela de tempo predefinida.</span><span class="sxs-lookup"><span data-stu-id="fd04a-145">Critical maintenance activity must execute within a pre-defined time window.</span></span> <span data-ttu-id="fd04a-146">Se as tarefas críticas não puderem ser executadas dentro do horário designado, a manutenção automática iniciará automaticamente a execução na próxima oportunidade de ociosidade do sistema disponível.</span><span class="sxs-lookup"><span data-stu-id="fd04a-146">If critical tasks have not been able to run within their designated time, Automatic Maintenance will automatically start executing at the next available system idle opportunity.</span></span> <span data-ttu-id="fd04a-147">No entanto, se o estado da tarefa permanecer atrás do prazo, a manutenção automática notificará o usuário sobre a atividade e fornecerá uma opção para uma execução manual da manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="fd04a-147">However, if the task state remains behind deadline, Automatic Maintenance will notify the user about the activity and provide an option for a manual run of Automatic Maintenance.</span></span> <span data-ttu-id="fd04a-148">Todas as tarefas agendadas para manutenção serão executadas, embora as tarefas mais privantes tenham precedência.</span><span class="sxs-lookup"><span data-stu-id="fd04a-148">All tasks scheduled for maintenance will run, although the most starved tasks take precedence.</span></span> <span data-ttu-id="fd04a-149">Essa atividade pode afetar o desempenho e a capacidade de resposta do sistema; Portanto, a manutenção automática notificará o usuário de que a atividade de manutenção crítica está em execução.</span><span class="sxs-lookup"><span data-stu-id="fd04a-149">This activity may impact system responsiveness and performance; therefore, Automatic Maintenance will notify the user that critical maintenance activity is executing.</span></span>

<span data-ttu-id="fd04a-150">**Controle corporativo**</span><span class="sxs-lookup"><span data-stu-id="fd04a-150">**Enterprise control**</span></span>

<span data-ttu-id="fd04a-151">Os profissionais de ti empresariais devem ser capazes de determinar quando a manutenção automática é executada em seus sistemas Windows, impor essa agenda via interfaces de gerenciamento padronizadas e recuperar dados de eventos sobre o status das tentativas de execução de manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="fd04a-151">Enterprise IT professionals should be able to determine when Automatic Maintenance executes on their Windows systems, enforce that schedule via standardized management interfaces, and retrieve event data about the status of Automatic Maintenance execution attempts.</span></span> <span data-ttu-id="fd04a-152">Além disso, os profissionais de ti devem ser capazes de invocar remotamente uma atividade de manutenção automática específica por meio de interfaces de gerenciamento padrão.</span><span class="sxs-lookup"><span data-stu-id="fd04a-152">Additionally, IT professionals should be able to invoke specific Automatic Maintenance activity remotely via standard management interfaces.</span></span> <span data-ttu-id="fd04a-153">Cada vez que a manutenção automática é executada, o relatório de status, incluindo notificações quando a manutenção automática não pôde ser executada porque o usuário pausou a atividade manualmente, é executado.</span><span class="sxs-lookup"><span data-stu-id="fd04a-153">Each time Automatic Maintenance executes, status reporting, including notifications when Automatic Maintenance could not be executed because the user has manually paused the activity, runs.</span></span> <span data-ttu-id="fd04a-154">Os profissionais de ti devem considerar a movimentação de scripts de logon para a manutenção automática para ajudar a tornar a experiência de logon do usuário mais rápida.</span><span class="sxs-lookup"><span data-stu-id="fd04a-154">IT professionals should consider moving logon scripts to Automatic Maintenance to help make the user’s logon experience quicker.</span></span>

## <a name="creating-an-automatic-maintenance-task"></a><span data-ttu-id="fd04a-155">Criando uma tarefa de manutenção automática</span><span class="sxs-lookup"><span data-stu-id="fd04a-155">Creating an Automatic Maintenance task</span></span>

<span data-ttu-id="fd04a-156">Esta seção detalha como os desenvolvedores podem criar uma tarefa usando uma definição de tarefa em linguagem XML ou C.</span><span class="sxs-lookup"><span data-stu-id="fd04a-156">This section details how developers can create a task using a task definition in XML or C language.</span></span> <span data-ttu-id="fd04a-157">Tenha em mente que a atividade de manutenção não deve iniciar nenhuma interface do usuário que exija interação do usuário, pois a manutenção automática é completamente silenciosa e é executada quando o usuário não está presente.</span><span class="sxs-lookup"><span data-stu-id="fd04a-157">Keep in mind that maintenance activity should not launch any user interface that requires user interaction, as Automatic Maintenance is completely silent and runs when the user is not present.</span></span> <span data-ttu-id="fd04a-158">Na verdade, se o usuário interage com o computador durante a manutenção automática, todas as tarefas em andamento serão encerradas até o próximo período ocioso.</span><span class="sxs-lookup"><span data-stu-id="fd04a-158">Indeed, if the user interacts with the computer during Automatic Maintenance, any tasks in process will be ended until the next idle period.</span></span>

<span data-ttu-id="fd04a-159">**Usando XML**</span><span class="sxs-lookup"><span data-stu-id="fd04a-159">**Using XML**</span></span>

<span data-ttu-id="fd04a-160">Agendador de Tarefas inclui uma ferramenta de linha de comando interna, schtasks.exe, que pode importar uma definição de tarefa em formato XML.</span><span class="sxs-lookup"><span data-stu-id="fd04a-160">Task Scheduler includes a built-in command-line tool, schtasks.exe, that can import a task definition in XML format.</span></span> <span data-ttu-id="fd04a-161">O esquema para definição de tarefa está documentado em https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx .</span><span class="sxs-lookup"><span data-stu-id="fd04a-161">The schema for task definition is documented at https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx.</span></span> <span data-ttu-id="fd04a-162">Veja abaixo um exemplo de uma tarefa de manutenção automática definida em XML.</span><span class="sxs-lookup"><span data-stu-id="fd04a-162">Below is an example of an Automatic Maintenance task defined in XML.</span></span>


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



<span data-ttu-id="fd04a-163">Para salvar a tarefa em um computador Windows, salve o XML acima como um arquivo de texto e use esta linha de comando:</span><span class="sxs-lookup"><span data-stu-id="fd04a-163">To save the task on a Windows computer, save the above XML as a text file and use this command line:</span></span>

`Schtasks.exe /create /tn <task name> /xml <text file name>`

<span data-ttu-id="fd04a-164">**Usando C**</span><span class="sxs-lookup"><span data-stu-id="fd04a-164">**Using C**</span></span>

<span data-ttu-id="fd04a-165">Uma tarefa de manutenção automática também pode ser criada usando código C.</span><span class="sxs-lookup"><span data-stu-id="fd04a-165">An Automatic Maintenance task also can be created using C code.</span></span> <span data-ttu-id="fd04a-166">Abaixo está um exemplo de código que pode ser usado para definir as configurações de manutenção automática de uma tarefa:</span><span class="sxs-lookup"><span data-stu-id="fd04a-166">Below is a code sample that can be used to configure a task’s Automatic Maintenance settings:</span></span>


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



## <a name="validating-tasks"></a><span data-ttu-id="fd04a-167">Validando tarefas</span><span class="sxs-lookup"><span data-stu-id="fd04a-167">Validating tasks</span></span>

<span data-ttu-id="fd04a-168">Valide se a tarefa foi criada com êxito e é executada como parte da manutenção.</span><span class="sxs-lookup"><span data-stu-id="fd04a-168">Validate that the task has been created successfully and runs as part of maintenance.</span></span>

<span data-ttu-id="fd04a-169">**Validando a criação da tarefa**</span><span class="sxs-lookup"><span data-stu-id="fd04a-169">**Validating task creation**</span></span>

<span data-ttu-id="fd04a-170">Use esta linha de comando para exportar a definição de tarefa para um arquivo e garantir que a definição da tarefa seja conforme o esperado:</span><span class="sxs-lookup"><span data-stu-id="fd04a-170">Use this command line to export the task definition to a file and ensure that the task definition is as expected:</span></span>

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

<span data-ttu-id="fd04a-171">**Validando a execução da tarefa**</span><span class="sxs-lookup"><span data-stu-id="fd04a-171">**Validating task execution**</span></span>

<span data-ttu-id="fd04a-172">Execute esta linha de comando para iniciar a tarefa e validar que a interface do usuário do Agendador de Tarefas (Taskschd. msc) mostra que a tarefa foi executada:</span><span class="sxs-lookup"><span data-stu-id="fd04a-172">Run this command line to launch the task and validate that the Task Scheduler UI (taskschd.msc) shows the task has run:</span></span>

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a><span data-ttu-id="fd04a-173">Recursos</span><span class="sxs-lookup"><span data-stu-id="fd04a-173">Resources</span></span>

-   <span data-ttu-id="fd04a-174">[Agenda de tarefas 2,0](/previous-versions/bb756979(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fd04a-174">[Task Schedule 2.0](/previous-versions/bb756979(v=msdn.10))</span></span>

 

 