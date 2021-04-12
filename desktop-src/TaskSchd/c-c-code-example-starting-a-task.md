---
title: Exemplo de código do C/C++ iniciando uma tarefa
description: Este exemplo tenta executar uma tarefa existente. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: e4f38f8a-3488-4802-913b-f627ecca8bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9fa9ba112b642aa5e14abc3b408c1536c527d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363823"
---
# <a name="cc-code-example-starting-a-task"></a><span data-ttu-id="765e5-104">Exemplo de código C/C++: iniciando uma tarefa</span><span class="sxs-lookup"><span data-stu-id="765e5-104">C/C++ Code Example: Starting a Task</span></span>

<span data-ttu-id="765e5-105">Este exemplo tenta executar uma tarefa existente.</span><span class="sxs-lookup"><span data-stu-id="765e5-105">This example attempts to run an existing task.</span></span> <span data-ttu-id="765e5-106">Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.</span><span class="sxs-lookup"><span data-stu-id="765e5-106">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>
#include<stdio.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
     hr = CoCreateInstance(CLSID_CTaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskScheduler,
                           (void **) &pITS);
     if (FAILED(hr))
     {
        CoUninitialize();
        return 1;
     }
  }
  else
  {
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  
  ITask *pITask;
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Run to start the execution of "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  hr = pITask->Run();
  pITask->Release();

  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::Run, error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }

  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="765e5-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="765e5-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="765e5-108">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="765e5-108">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




