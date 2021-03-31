---
title: Exemplo de código do C/C++ recuperando o diretório de trabalho da tarefa
description: Este exemplo recupera o diretório de trabalho associado a uma tarefa e exibe o caminho para o diretório de trabalho na tela. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: 46dfd996-6d5f-4a77-87a9-daf1909e1509
keywords:
- Recuperando Agendador de Tarefas do diretório de trabalho
- Recuperando propriedades da tarefa Agendador de Tarefas, diretório de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44d29de7df9307ee40f3d10d9dd28f87f89d8a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005614"
---
# <a name="cc-code-example-retrieving-the-task-working-directory"></a><span data-ttu-id="d8999-106">Exemplo de código do C/C++: Recuperando o diretório de trabalho da tarefa</span><span class="sxs-lookup"><span data-stu-id="d8999-106">C/C++ Code Example: Retrieving the Task Working Directory</span></span>

<span data-ttu-id="d8999-107">Este exemplo recupera o diretório de trabalho associado a uma tarefa e exibe o caminho para o diretório de trabalho na tela.</span><span class="sxs-lookup"><span data-stu-id="d8999-107">This example retrieves the working directory associated with a task and displays the path to the working directory on the screen.</span></span> <span data-ttu-id="d8999-108">Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.</span><span class="sxs-lookup"><span data-stu-id="d8999-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
     wprintf(L"Failed calling ITaskScheduler::Activate: error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetWorkingDirectory to display the working 
  // directory associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszWorkDir;
  hr = pITask->GetWorkingDirectory(&lpwszWorkDir);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetWorkingDirectory: \n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process returned string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with : %s\n", lpwszWorkDir);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszWorkDir);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d8999-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8999-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8999-110">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="d8999-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




