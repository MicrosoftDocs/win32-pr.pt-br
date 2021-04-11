---
title: Enumerando trabalhos na fila de transferência
description: Para enumerar trabalhos da fila de transferência, chame o método IBackgroundCopyManager EnumJobs. O método retorna um ponteiro de interface IEnumBackgroundCopyJobs que você usa para enumerar os trabalhos na fila.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- transferir BITS de trabalho, enumerando
- Enumerando trabalhos nos BITS da fila de transferência
- BITS da fila de transferência, enumerando
- Enumerando BITS
- Enumerando BITS, trabalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291828"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a>Enumerando trabalhos na fila de transferência

Para enumerar trabalhos da fila de transferência, chame o método [**IBackgroundCopyManager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . O método retorna um ponteiro de interface [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) que você usa para enumerar os trabalhos na fila.

Para recuperar os trabalhos do usuário, defina o primeiro parâmetro do método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) como 0. Para recuperar todos os trabalhos na fila, defina o primeiro parâmetro do método **EnumJobs** como BG \_ Job \_ enum \_ todos \_ os usuários. Somente os usuários com privilégios de administrador podem recuperar todos os trabalhos na fila de transferência.

Observe que a lista enumerada é um instantâneo dos trabalhos na fila de transferência no momento em que você chama o método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . No entanto, os valores de propriedade desses trabalhos refletem os valores atuais do trabalho.

Se você quiser recuperar trabalhos de transferência individuais, chame o método [**IBackgroundCopyManager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .

Para enumerar arquivos em um trabalho, consulte [enumerando arquivos em um trabalho](enumerating-files-in-a-job.md).

O exemplo a seguir mostra como enumerar trabalhos na fila de transferência. A \_ variável g XferManager no exemplo é um ponteiro de interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) . Para obter detalhes sobre como criar o ponteiro de interface **IBackgroundCopyManager** , consulte [conectando-se ao serviço bits](connecting-to-the-bits-service.md).


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




