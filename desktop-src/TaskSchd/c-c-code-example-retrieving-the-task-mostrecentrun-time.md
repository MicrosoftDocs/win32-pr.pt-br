---
title: Exemplo de código C/C++ recuperando o tempo de MostRecentRun da tarefa
description: Este exemplo recupera a hora em que a tarefa foi executada pela última vez e a exibe na tela. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.
ms.assetid: 683ff1e1-1cb0-4ef7-bca2-9c3a2b4d1bd0
keywords:
- Recuperando a tarefa de tempo de execução mais recente Agendador de Tarefas
- Recuperando propriedades do item de trabalho Agendador de Tarefas, tempo de execução mais recente da tarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cae40de306d79628fa10230091c571e776c5e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764753"
---
# <a name="cc-code-example-retrieving-the-task-mostrecentrun-time"></a>Exemplo de código C/C++: Recuperando o tempo de MostRecentRun da tarefa

Este exemplo recupera a hora em que a tarefa foi executada pela última vez e a exibe na tela. Este exemplo supõe que a tarefa e a tarefa de teste já existam no computador local.


```C++
#include <windows.h>
#include <wchar.h>
#include <stdio.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>


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
  LPCWSTR lpcwszTaskName = L"Test Task";
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
  // Call ITask::GetMostRecentRunTime and display the most recent 
  // run time of this task.
  ///////////////////////////////////////////////////////////////////

  SYSTEMTIME pstLastRun;
    
  hr = pITask->GetMostRecentRunTime(&pstLastRun);
  
  // Release the ITask interface.
  pITask->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetMostRecentRunTime: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }

  wprintf(L"The most recent run time for this task was: \n");
  wprintf(L"  %u/%u/%u \t %u:%02u\n", pstLastRun.wMonth,
                                      pstLastRun.wDay,
                                      pstLastRun.wYear,
                                      pstLastRun.wHour,
                                      pstLastRun.wMinute);
 

  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




