---
title: Exibindo nomes e Estados de tarefas (C++)
description: Esses dois exemplos de C++ mostram como enumerar tarefas. Um exemplo mostra como exibir informações de tarefas em uma pasta de tarefas e os outros exemplos mostram como exibir informações para todas as tarefas em execução.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6189960ef5b6e4ad78e75f156a482481f347b4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637163"
---
# <a name="displaying-task-names-and-states-c"></a><span data-ttu-id="fd349-104">Exibindo nomes e Estados de tarefas (C++)</span><span class="sxs-lookup"><span data-stu-id="fd349-104">Displaying Task Names and States (C++)</span></span>

<span data-ttu-id="fd349-105">Esses dois exemplos de C++ mostram como enumerar tarefas.</span><span class="sxs-lookup"><span data-stu-id="fd349-105">These two C++ examples show how to enumerate tasks.</span></span> <span data-ttu-id="fd349-106">Um exemplo mostra como exibir informações de tarefas em uma pasta de tarefas e os outros exemplos mostram como exibir informações para todas as tarefas em execução.</span><span class="sxs-lookup"><span data-stu-id="fd349-106">One example shows how to display information for tasks in a task folder, and the other examples shows how to display information for all running tasks.</span></span>

<span data-ttu-id="fd349-107">O procedimento a seguir descreve como exibir nomes de tarefas e o estado de todas as tarefas em uma pasta de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fd349-107">The following procedure describes how to display task names and state for all the tasks in a task folder.</span></span>

<span data-ttu-id="fd349-108">**Para exibir nomes de tarefas e o estado de todas as tarefas em uma pasta de tarefas**</span><span class="sxs-lookup"><span data-stu-id="fd349-108">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="fd349-109">Inicialize COM e defina a segurança COM geral.</span><span class="sxs-lookup"><span data-stu-id="fd349-109">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="fd349-110">Crie o objeto [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="fd349-110">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="fd349-111">Esse objeto permite que você se conecte ao serviço de Agendador de Tarefas e acesse uma pasta de tarefas específica.</span><span class="sxs-lookup"><span data-stu-id="fd349-111">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

3.  <span data-ttu-id="fd349-112">Obtenha uma pasta de tarefas que contém as tarefas sobre as quais você deseja obter informações.</span><span class="sxs-lookup"><span data-stu-id="fd349-112">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="fd349-113">Use o método [**o ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) para obter a pasta.</span><span class="sxs-lookup"><span data-stu-id="fd349-113">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder.</span></span>

4.  <span data-ttu-id="fd349-114">Obtenha a coleção de tarefas da pasta.</span><span class="sxs-lookup"><span data-stu-id="fd349-114">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="fd349-115">Use o método [**ITaskFolder::**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) gettasks para obter a coleção de tarefas ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).</span><span class="sxs-lookup"><span data-stu-id="fd349-115">Use the [**ITaskFolder::GetTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) method to get the collection of tasks ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).</span></span>

5.  <span data-ttu-id="fd349-116">Obtenha o número de tarefas na coleção e enumere-a em cada tarefa na coleção.</span><span class="sxs-lookup"><span data-stu-id="fd349-116">Get the number of tasks in the collection, and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="fd349-117">Use a [**Propriedade Item de IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) para obter uma instância de [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) .</span><span class="sxs-lookup"><span data-stu-id="fd349-117">Use the [**Item Property of IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) to get an [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) instance.</span></span> <span data-ttu-id="fd349-118">Cada instância conterá uma tarefa na coleção.</span><span class="sxs-lookup"><span data-stu-id="fd349-118">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="fd349-119">Em seguida, você pode exibir as informações (valores de propriedade) de cada tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="fd349-119">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="fd349-120">O exemplo de C++ a seguir mostra como exibir o nome e o estado de todas as tarefas na pasta de tarefas raiz.</span><span class="sxs-lookup"><span data-stu-id="fd349-120">The following C++ example shows how to display the name and state of all the tasks in the root task folder.</span></span>


```C++
/********************************************************************
 This sample enumerates through the tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


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
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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
    //  Get the pointer to the root task folder.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    
    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
    
    //  -------------------------------------------------------
    //  Get the registered tasks in the folder.
    IRegisteredTaskCollection* pTaskCollection = NULL;
    hr = pRootFolder->GetTasks( NULL, &pTaskCollection );

    pRootFolder->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get the registered tasks.: %x", hr);
        CoUninitialize();
        return 1;
    }

    LONG numTasks = 0;
    hr = pTaskCollection->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pTaskCollection->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of Tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRegisteredTask* pRegisteredTask = NULL;
        hr = pTaskCollection->get_Item( _variant_t(i+1), &pRegisteredTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRegisteredTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRegisteredTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRegisteredTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pTaskCollection->Release();
    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="fd349-121">O procedimento a seguir descreve como exibir nomes de tarefas e o estado de todas as tarefas em execução.</span><span class="sxs-lookup"><span data-stu-id="fd349-121">The following procedure describes how to display task names and state for all running tasks.</span></span>

<span data-ttu-id="fd349-122">**Para exibir os nomes e o estado da tarefa para todas as tarefas em execução**</span><span class="sxs-lookup"><span data-stu-id="fd349-122">**To display task names and state for all running tasks**</span></span>

1.  <span data-ttu-id="fd349-123">Inicialize COM e defina a segurança COM geral.</span><span class="sxs-lookup"><span data-stu-id="fd349-123">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="fd349-124">Crie o objeto [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="fd349-124">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="fd349-125">Esse objeto permite que você se conecte ao serviço de Agendador de Tarefas e acesse uma pasta de tarefas específica.</span><span class="sxs-lookup"><span data-stu-id="fd349-125">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

3.  <span data-ttu-id="fd349-126">Use o método [**o ITaskService:: GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) para obter uma coleção de todas as tarefas em execução ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)).</span><span class="sxs-lookup"><span data-stu-id="fd349-126">Use the [**ITaskService::GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) method to get a collection of all the running tasks ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)).</span></span> <span data-ttu-id="fd349-127">Você pode especificar para obter instâncias da tarefa em execução, incluindo ou excluindo tarefas ocultas.</span><span class="sxs-lookup"><span data-stu-id="fd349-127">You can specify to get instances of running task either including or excluding hidden tasks.</span></span>
4.  <span data-ttu-id="fd349-128">Obtenha o número de tarefas na coleção e enumere-a em cada tarefa na coleção.</span><span class="sxs-lookup"><span data-stu-id="fd349-128">Get the number of tasks in the collection, and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="fd349-129">Use a [**Propriedade Item de IRunningTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) para obter uma instância de [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) .</span><span class="sxs-lookup"><span data-stu-id="fd349-129">Use the [**Item property of IRunningTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) to get an [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) instance.</span></span> <span data-ttu-id="fd349-130">Cada instância conterá uma tarefa na coleção.</span><span class="sxs-lookup"><span data-stu-id="fd349-130">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="fd349-131">Em seguida, você pode exibir as informações (valores de propriedade) de cada tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="fd349-131">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="fd349-132">O exemplo de C++ a seguir mostra como exibir o nome e o estado de todas as tarefas em execução, incluindo tarefas ocultas.</span><span class="sxs-lookup"><span data-stu-id="fd349-132">The following C++ example shows how to display the name and state of all the running tasks, including hidden tasks.</span></span>


```C++
/********************************************************************
 This sample enumerates through all running tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


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
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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

       // Get the running tasks.
       IRunningTaskCollection* pRunningTasks = NULL;
       hr = pService->GetRunningTasks(TASK_ENUM_HIDDEN, &pRunningTasks);

    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
        
    LONG numTasks = 0;
    hr = pRunningTasks->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pRunningTasks->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of running tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRunningTask* pRunningTask = NULL;
        hr = pRunningTasks->get_Item( _variant_t(i+1), &pRunningTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRunningTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRunningTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRunningTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pRunningTasks->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="fd349-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd349-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd349-134">Usando o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="fd349-134">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




