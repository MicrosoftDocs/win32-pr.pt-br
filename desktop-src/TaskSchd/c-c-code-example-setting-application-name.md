---
title: Exemplo de código do C/C++ definindo nome do aplicativo
description: Este exemplo define o nome do aplicativo associado a uma tarefa conhecida. Este exemplo pressupõe que a tarefa \ 0034; teste a tarefa \ 0034; Já existe no computador local e o serviço de Agendador de Tarefas está em execução.
ms.assetid: 1d86f945-0f13-4a7f-8123-df7e63a02238
keywords:
- definindo propriedades da tarefa Agendador de Tarefas, nome do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5ce664079217778e08dcd44ef8c646a4c4eaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005613"
---
# <a name="cc-code-example-setting-application-name"></a><span data-ttu-id="e2728-105">Exemplo de código C/C++: definindo o nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e2728-105">C/C++ Code Example: Setting Application Name</span></span>

<span data-ttu-id="e2728-106">Este exemplo define o nome do aplicativo associado a uma tarefa conhecida.</span><span class="sxs-lookup"><span data-stu-id="e2728-106">This example sets the name of the application associated with a known task.</span></span> <span data-ttu-id="e2728-107">Este exemplo pressupõe que a tarefa "Test Task" já exista no computador local e que o serviço Agendador de Tarefas esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="e2728-107">This example assumes that the task "test task" already exists on the local computer and that the Task Scheduler service is running.</span></span>


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
  
  // Release the ITaskScheduler interface.
  pITS->Release();  
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::SetApplicationName to specify the Application name
  // for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszApplicationName = L"C:\\Windows\\System32\\notepad.exe";
 
  hr = pITask->SetApplicationName(pwszApplicationName);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetApplicationName: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }

  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"Set the application name for Test Task.\n");  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="e2728-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2728-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2728-109">Exemplos de Agendador de Tarefas 1,0</span><span class="sxs-lookup"><span data-stu-id="e2728-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




