---
title: Exemplo de código C/C++ recuperando o Criador da Tarefa
description: Este exemplo recupera o nome do criador da tarefa e o exibe na tela. Este exemplo presume que a tarefa e a tarefa de teste já existem no computador local.
ms.assetid: 02554ce1-2d52-48e9-95f1-d5d480519035
keywords:
- recuperando o criador da tarefa Agendador de Tarefas
- recuperando propriedades de item de trabalho Agendador de Tarefas , criador de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa756fbb10e2d0cd68cce8953dd38cf2d31ab0242d74faea07423292908665b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872486"
---
# <a name="cc-code-example-retrieving-the-task-creator"></a>Exemplo de código C/C++: Recuperando o Criador da Tarefa

Este exemplo recupera o nome do criador da tarefa e o exibe na tela. Este exemplo presume que a tarefa e a tarefa de teste já existem no computador local.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




