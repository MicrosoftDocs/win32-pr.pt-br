---
title: Exemplo de gatilho de registro (C++)
description: Este exemplo de C++ mostra como criar uma tarefa que está agendada para executar o bloco de notas quando uma tarefa é registrada.
ms.assetid: 5e2e8fa6-66c7-4356-8fd6-22f7974791b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090a690601e24e1245040d0e7b394123afa94b07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761810"
---
# <a name="registration-trigger-example-c"></a><span data-ttu-id="617cc-103">Exemplo de gatilho de registro (C++)</span><span class="sxs-lookup"><span data-stu-id="617cc-103">Registration Trigger Example (C++)</span></span>

<span data-ttu-id="617cc-104">Este exemplo de C++ mostra como criar uma tarefa que está agendada para executar o bloco de notas quando uma tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="617cc-104">This C++ example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="617cc-105">A tarefa contém um gatilho de registro que especifica um limite inicial e um limite final para a tarefa e também um atraso para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="617cc-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task and also a delay for the task.</span></span> <span data-ttu-id="617cc-106">O limite inicial especifica quando o gatilho é ativado e o atraso define a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="617cc-106">The start boundary specifies when the trigger is activated, and the delay sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="617cc-107">A tarefa também contém uma ação que especifica a tarefa para executar o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="617cc-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="617cc-108">Quando uma tarefa com um gatilho de registro é atualizada, a tarefa será executada Depois que a atualização ocorrer.</span><span class="sxs-lookup"><span data-stu-id="617cc-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="617cc-109">O procedimento a seguir descreve como agendar uma tarefa para iniciar um executável quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="617cc-109">The following procedure describes how to schedule a task to start an executable when the task is registered.</span></span>

<span data-ttu-id="617cc-110">**Para agendar o bloco de notas para iniciar quando uma tarefa for registrada**</span><span class="sxs-lookup"><span data-stu-id="617cc-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="617cc-111">Inicialize COM e defina a segurança COM geral.</span><span class="sxs-lookup"><span data-stu-id="617cc-111">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="617cc-112">Crie o objeto [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="617cc-112">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span> <span data-ttu-id="617cc-113">Esse objeto permite que você crie tarefas em uma pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="617cc-113">This object allows you to create tasks in a specified folder.</span></span>
3.  <span data-ttu-id="617cc-114">Obtenha uma pasta de tarefas na qual criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="617cc-114">Get a task folder to create a task in.</span></span> <span data-ttu-id="617cc-115">Use o método [**o ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) para obter a pasta e o método [**O ITaskService:: NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) para criar o objeto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="617cc-115">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>
4.  <span data-ttu-id="617cc-116">Defina informações sobre a tarefa usando o objeto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , como as informações de registro para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="617cc-116">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span> <span data-ttu-id="617cc-117">Use a [**Propriedade RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) e outras propriedades da interface **ITaskDefinition** para definir as informações da tarefa.</span><span class="sxs-lookup"><span data-stu-id="617cc-117">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the **ITaskDefinition** interface to define the task information.</span></span>
5.  <span data-ttu-id="617cc-118">Crie um gatilho de registro usando a [**Propriedade Triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) para acessar o [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="617cc-118">Create a registration trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span> <span data-ttu-id="617cc-119">Use o método [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) (especificando o tipo de gatilho que você deseja criar) para criar um gatilho de registro.</span><span class="sxs-lookup"><span data-stu-id="617cc-119">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method (specifying the type of trigger you want to create) to create a registration trigger.</span></span>
6.  <span data-ttu-id="617cc-120">Crie uma ação para a tarefa Executar usando a [**Propriedade Actions de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) para acessar a interface [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="617cc-120">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span> <span data-ttu-id="617cc-121">Use o método [**IActionCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) para especificar o tipo de ação que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="617cc-121">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="617cc-122">Este exemplo usa um objeto [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , que representa uma ação que executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="617cc-122">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>
7.  <span data-ttu-id="617cc-123">Registre a tarefa usando o método [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="617cc-123">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="617cc-124">O exemplo de C++ a seguir mostra como agendar uma tarefa para executar o bloco de notas 30 segundos depois que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="617cc-124">The following C++ example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start notepad.exe 30 seconds after
 the task is registered. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")
#pragma comment(lib, "credui.lib")

using namespace std;


int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
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
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Registration Trigger Test Task";

    //  Get the windows directory and set the path to notepad.exe.
    wstring wstrExecutablePath = _wgetenv( L"WINDIR");
    wstrExecutablePath += L"\\SYSTEM32\\NOTEPAD.EXE";


    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        printf("Failed to create an instance of ITaskService: %x", hr);
        CoUninitialize();
        return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    hr = pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
        printf("Failed to create a task definition: %x", hr);
        pRootFolder->Release();
        CoUninitialize();
        return 1;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    IRegistrationInfo *pRegInfo= NULL;
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        printf("\nCannot get identification pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegInfo->put_Author( L"Author Name" );
    pRegInfo->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task
    IPrincipal *pPrincipal = NULL;
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        printf("\nCannot get principal pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set up principal information: 
    hr = pPrincipal->put_Id( _bstr_t(L"Principal1") ); 
    if( FAILED(hr) )
        printf("\nCannot put the principal ID: %x", hr);

    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
        printf("\nCannot put principal logon type: %x", hr);

    //  Run the task with the least privileges (LUA) 
    hr = pPrincipal->put_RunLevel( TASK_RUNLEVEL_LUA ); 
    pPrincipal->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put principal run level: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
   

    //  ------------------------------------------------------
    //  Create the settings for the task
    ITaskSettings *pSettings = NULL;
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get settings pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set setting values for the task.
    hr = pSettings->put_StartWhenAvailable(VARIANT_TRUE);    
    pSettings->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot put setting info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the registration trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Add the registration trigger to the task.
    ITrigger *pTrigger = NULL;    
    hr = pTriggerCollection->Create( TASK_TRIGGER_REGISTRATION, &pTrigger );
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create a registration trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }     
    
    IRegistrationTrigger *pRegistrationTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_IRegistrationTrigger, (void**) &pRegistrationTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed on IRegistrationTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegistrationTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);
    
    //  Define the delay for the registration trigger.
    hr = pRegistrationTrigger->put_Delay( L"PT30S" );
    pRegistrationTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put registration trigger delay: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }   
    

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute notepad.exe.     
    IActionCollection *pActionCollection = NULL;

    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get Task collection pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Create the action, specifying that it is an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    IExecAction *pExecAction = NULL;

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) ); 
    pExecAction->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot put the action executable path: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    printf("\n Success! Task successfully registered. " );

    //  Clean up.
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="617cc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="617cc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="617cc-126">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="617cc-126">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




