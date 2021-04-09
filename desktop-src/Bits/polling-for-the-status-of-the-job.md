---
title: Sondando o status do trabalho
description: Por padrão, um aplicativo deve sondar as alterações no status de um trabalho.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- transferir BITS de trabalho, sondagem
- sondando BITS de status do trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822325"
---
# <a name="polling-for-the-status-of-the-job"></a>Sondando o status do trabalho

Por padrão, um aplicativo deve sondar as alterações no status de um trabalho. Para capturar as alterações no estado do trabalho, chame o método [**método ibackgroundcopyjob:: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) . Para capturar as alterações no número de bytes e arquivos transferidos, chame o método [**método ibackgroundcopyjob:: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) . Para recuperar as informações de progresso na parte de resposta de um trabalho de resposta de upload, chame o método [**IBackgroundCopyJob2:: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) . Para obter um exemplo que usa as informações de progresso, consulte [determinando o progresso de um trabalho](determining-the-progress-of-a-job.md).

A enumeração de [**\_ \_ estado do trabalho BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) define os Estados de um trabalho e a estrutura de [**\_ \_ progresso do trabalho BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contém informações sobre o número de bytes e arquivos transferidos.

Para usar a sondagem, você precisa criar um mecanismo para iniciar a sondagem. Por exemplo, crie um temporizador ou use um botão de "atualização" na interface do usuário. No entanto, pode ser mais fácil registrar-se para notificação de eventos e receber eventos quando o estado ou o progresso for alterado. Para obter informações sobre notificação de eventos, consulte [registrando um retorno de chamada com](registering-a-com-callback.md).

O exemplo a seguir usa um temporizador para sondar o estado de um trabalho. O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




