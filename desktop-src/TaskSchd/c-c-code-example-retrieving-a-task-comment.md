---
title: Exemplo de código C/C++ recuperando um comentário de tarefa
description: Este exemplo recupera a cadeia de caracteres de comentário de uma tarefa conhecida e exibe a cadeia de caracteres de comentário na tela. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: f6f558d8-2e34-4314-9583-f815921aac7e
keywords:
- Recuperando o comentário da tarefa Agendador de Tarefas
- Recuperando propriedades do item de trabalho Agendador de Tarefas, comentário da tarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89ada9b135e42e25a81baf9bee60910b4e1a483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292235"
---
# <a name="cc-code-example-retrieving-a-task-comment"></a><span data-ttu-id="69798-106">Exemplo de código C/C++: Recuperando um comentário de tarefa</span><span class="sxs-lookup"><span data-stu-id="69798-106">C/C++ Code Example: Retrieving a Task Comment</span></span>

<span data-ttu-id="69798-107">Este exemplo recupera a cadeia de caracteres de comentário de uma tarefa conhecida e exibe a cadeia de caracteres de comentário na tela.</span><span class="sxs-lookup"><span data-stu-id="69798-107">This example retrieves the comment string of a known task and displays the comment string on the screen.</span></span> <span data-ttu-id="69798-108">Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.</span><span class="sxs-lookup"><span data-stu-id="69798-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::GetComment. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR ppwszComment;
  
  hr = pITask->GetComment(&ppwszComment);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetComment: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The comment for Test Task is: ");
  wprintf(L"  %s\n",ppwszComment);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free the string.
  ///////////////////////////////////////////////////////////////////
  CoTaskMemFree(ppwszComment);
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="69798-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69798-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69798-110">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="69798-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




