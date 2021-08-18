---
title: Exibindo nomes e Estados de tarefas (C++)
description: Esses dois exemplos de C++ mostram como enumerar tarefas. Um exemplo mostra como exibir informações de tarefas em uma pasta de tarefas e os outros exemplos mostram como exibir informações para todas as tarefas em execução.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80ec17b71ae45c951a27ca582855936d73457401d878b0f21f69bcbaa71ca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760181"
---
# <a name="displaying-task-names-and-states-c"></a>Exibindo nomes e Estados de tarefas (C++)

Esses dois exemplos de C++ mostram como enumerar tarefas. Um exemplo mostra como exibir informações de tarefas em uma pasta de tarefas e os outros exemplos mostram como exibir informações para todas as tarefas em execução.

O procedimento a seguir descreve como exibir nomes de tarefas e o estado de todas as tarefas em uma pasta de tarefas.

**Para exibir nomes de tarefas e o estado de todas as tarefas em uma pasta de tarefas**

1.  Inicialize COM e defina a segurança COM geral.
2.  Crie o objeto [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

    Esse objeto permite que você se conecte ao serviço de Agendador de Tarefas e acesse uma pasta de tarefas específica.

3.  Obtenha uma pasta de tarefas que contém as tarefas sobre as quais você deseja obter informações.

    Use o método [**o ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) para obter a pasta.

4.  Obtenha a coleção de tarefas da pasta.

    Use o método [**ITaskFolder::**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) gettasks para obter a coleção de tarefas ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).

5.  Obtenha o número de tarefas na coleção e enumere-a em cada tarefa na coleção.

    Use a [**Propriedade Item de IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) para obter uma instância de [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) . Cada instância conterá uma tarefa na coleção. Em seguida, você pode exibir as informações (valores de propriedade) de cada tarefa registrada.

O exemplo de C++ a seguir mostra como exibir o nome e o estado de todas as tarefas na pasta de tarefas raiz.


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



O procedimento a seguir descreve como exibir nomes de tarefas e o estado de todas as tarefas em execução.

**Para exibir os nomes e o estado da tarefa para todas as tarefas em execução**

1.  Inicialize COM e defina a segurança COM geral.
2.  Crie o objeto [**o ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

    Esse objeto permite que você se conecte ao serviço de Agendador de Tarefas e acesse uma pasta de tarefas específica.

3.  Use o método [**o ITaskService:: GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) para obter uma coleção de todas as tarefas em execução ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)). Você pode especificar para obter instâncias da tarefa em execução, incluindo ou excluindo tarefas ocultas.
4.  Obtenha o número de tarefas na coleção e enumere-a em cada tarefa na coleção.

    Use a [**Propriedade Item de IRunningTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) para obter uma instância de [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) . Cada instância conterá uma tarefa na coleção. Em seguida, você pode exibir as informações (valores de propriedade) de cada tarefa registrada.

O exemplo de C++ a seguir mostra como exibir o nome e o estado de todas as tarefas em execução, incluindo tarefas ocultas.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




