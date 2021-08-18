---
title: Exemplo de código C/C++ Recuperando a tarefa MaisRecentRun Time
description: Este exemplo recupera a hora em que a tarefa foi executado pela última vez e a exibe na tela. Este exemplo presume que a tarefa e a tarefa de teste já existem no computador local.
ms.assetid: 683ff1e1-1cb0-4ef7-bca2-9c3a2b4d1bd0
keywords:
- recuperação da tarefa mais recente de tempo de Agendador de Tarefas
- recuperando propriedades de item de trabalho Agendador de Tarefas , tempo de executar mais recente da tarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e8a49372a082567f5f454cfd01a84239ff622f7ab6121fa07a1f557976c4de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738566"
---
# <a name="cc-code-example-retrieving-the-task-mostrecentrun-time"></a>Exemplo de código C/C++: Recuperando a tarefa MaisRecentRun Time

Este exemplo recupera a hora em que a tarefa foi executado pela última vez e a exibe na tela. Este exemplo presume que a tarefa e a tarefa de teste já existem no computador local.


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

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




