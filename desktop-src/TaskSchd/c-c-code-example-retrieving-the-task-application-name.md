---
title: Exemplo de código C/C++ recuperando o nome do aplicativo da tarefa
description: Este exemplo recupera o nome do aplicativo associado a uma determinada tarefa e exibe esse nome na tela. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: 7cf20a14-fee3-4507-83a9-4a081a9783fc
keywords:
- Recuperando nomes de aplicativos Agendador de Tarefas
- Recuperando propriedades da tarefa Agendador de Tarefas, nome do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb590900cf7b4c6d8821560e91e2f05c21c0f73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759958"
---
# <a name="cc-code-example-retrieving-the-task-application-name"></a><span data-ttu-id="16d15-106">Exemplo de código do C/C++: Recuperando o nome do aplicativo da tarefa</span><span class="sxs-lookup"><span data-stu-id="16d15-106">C/C++ Code Example: Retrieving the Task Application Name</span></span>

<span data-ttu-id="16d15-107">Este exemplo recupera o nome do aplicativo associado a uma determinada tarefa e exibe esse nome na tela.</span><span class="sxs-lookup"><span data-stu-id="16d15-107">This example retrieves the name of the application associated with a given task and displays that name on the screen.</span></span> <span data-ttu-id="16d15-108">Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.</span><span class="sxs-lookup"><span data-stu-id="16d15-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetApplicationName to display the name of the 
  // application associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszApplicationName;
  hr = pITask->GetApplicationName(&lpwszApplicationName);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetApplicationName\n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process the returned string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with: %s\n", lpwszApplicationName);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszApplicationName);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="16d15-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16d15-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16d15-110">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="16d15-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




