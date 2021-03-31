---
title: Exemplo de código do C/C++ recuperando o criador da tarefa
description: Este exemplo recupera o nome do criador da tarefa e o exibe na tela. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: 02554ce1-2d52-48e9-95f1-d5d480519035
keywords:
- Recuperando Agendador de Tarefas do criador da tarefa
- Recuperando propriedades de item de trabalho Agendador de Tarefas, criador de tarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3546d676a5f1ac4b99595e47f2514b84e38f4c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005418"
---
# <a name="cc-code-example-retrieving-the-task-creator"></a><span data-ttu-id="901f5-106">Exemplo de código do C/C++: Recuperando o criador da tarefa</span><span class="sxs-lookup"><span data-stu-id="901f5-106">C/C++ Code Example: Retrieving the Task Creator</span></span>

<span data-ttu-id="901f5-107">Este exemplo recupera o nome do criador da tarefa e o exibe na tela.</span><span class="sxs-lookup"><span data-stu-id="901f5-107">This example retrieves the name of the creator of the task and displays it on the screen.</span></span> <span data-ttu-id="901f5-108">Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.</span><span class="sxs-lookup"><span data-stu-id="901f5-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
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
  
  //Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetCreator. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR ppwszCreator;
  
  hr = pITask->GetCreator(&ppwszCreator);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetCreator: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The creator of Test Task is: ");
  wprintf(L"  %s\n",ppwszCreator);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free the string.
  ///////////////////////////////////////////////////////////////////
  CoTaskMemFree(ppwszCreator);
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="901f5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="901f5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="901f5-110">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="901f5-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




