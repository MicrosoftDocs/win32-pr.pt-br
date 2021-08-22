---
title: Exemplo de código C/C++ Recuperando o tempo de espera ocioso da tarefa
description: Este exemplo recupera o tempo de espera ocioso da tarefa e o exibe na tela. Este exemplo presume que a tarefa e a tarefa de teste já existem no computador local.
ms.assetid: 2784b925-678c-422c-ae78-84d2982c2b02
keywords:
- recuperando o tempo de espera de ociosidade da tarefa Agendador de Tarefas
- recuperando propriedades de item de trabalho Agendador de Tarefas tempo de espera ocioso da tarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7946d4a8b80dd49db2b8c5291f8d382a9e3b40b4de8a759f10f4057905593f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738766"
---
# <a name="cc-code-example-retrieving-task-idle-wait-time"></a>Exemplo de código C/C++: Recuperando o tempo de espera ocioso da tarefa

Este exemplo recupera o tempo de espera ocioso da tarefa e o exibe na tela. Este exemplo presume que a tarefa e a tarefa de teste já existem no computador local.


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
  // Call ITask::GetIdleWait. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  WORD pwIdleMinutes;
  WORD pwDeadlineMinutes;
  
  hr = pITask->GetIdleWait(&pwIdleMinutes,
                           &pwDeadlineMinutes);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetIdleWait: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The idle wait of Test Task is: \n");
  wprintf(L" %d minutes\n", pwIdleMinutes);
  wprintf(L" %d minutes\n", pwDeadlineMinutes);
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




