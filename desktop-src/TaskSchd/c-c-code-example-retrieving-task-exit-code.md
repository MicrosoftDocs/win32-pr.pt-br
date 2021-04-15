---
title: Exemplo de código do C/C++ recuperando código de saída da tarefa
description: Este exemplo recupera o último código de saída retornado por uma tarefa conhecida. (Um valor retornado de \ 0034; 0 \ 0034; indica que a tarefa nunca foi executada.) Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: e7bfe645-7f4c-4700-9adf-c581e6895aec
keywords:
- Recuperando o comentário da tarefa Agendador de Tarefas
- Recuperando propriedades do item de trabalho Agendador de Tarefas, comentário da tarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5911cad3831dc8da04e44f161a644bda9742bd33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498692"
---
# <a name="cc-code-example-retrieving-task-exit-code"></a><span data-ttu-id="053ae-106">Exemplo de código do C/C++: Recuperando o código de saída da tarefa</span><span class="sxs-lookup"><span data-stu-id="053ae-106">C/C++ Code Example: Retrieving Task Exit Code</span></span>

<span data-ttu-id="053ae-107">Este exemplo recupera o último código de saída retornado por uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="053ae-107">This example retrieves the last exit code returned by a known task.</span></span> <span data-ttu-id="053ae-108">(Um valor retornado de "0" indica que a tarefa nunca foi executada.) Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.</span><span class="sxs-lookup"><span data-stu-id="053ae-108">(A returned value of "0" indicates the task was never run.) This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  lpcwszTaskName = L"TestTask";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  // Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetExitCode. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  DWORD pdwExitCode;
  
  hr = pITask->GetExitCode(&pdwExitCode);
  
  // Release ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetExitCode: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The last exit code of Test Task is: %d\n", pdwExitCode);
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="053ae-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="053ae-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="053ae-110">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="053ae-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




