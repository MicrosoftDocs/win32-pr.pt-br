---
title: Criando um trabalho
description: Para criar um trabalho de transferência, chame o método IBackgroundCopyManager CreateJob.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- transferir BITS de trabalho
- transferir BITS de trabalho, criando
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453535"
---
# <a name="creating-a-job"></a>Criando um trabalho

Para criar um trabalho de transferência, chame o método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) . Depois que o BITS cria o trabalho, [adicione arquivos ao trabalho](adding-files-to-a-job.md) e [modifique as propriedades do trabalho](setting-and-retrieving-the-properties-of-a-job.md) conforme apropriado para seu aplicativo. Para ativar o trabalho na fila, chame o método [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .

O método [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) cria um GUID que identifica exclusivamente o trabalho. Você usa o GUID para [recuperar o trabalho da fila de transferência](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). O nome de exibição que você fornece ao criar o trabalho não é exclusivo; mais de um trabalho pode usar o mesmo nome.

O BITS limita o número de trabalhos na fila para trabalhos de 300 e o número de trabalhos que um usuário pode criar para o trabalho de 60. Esses limites não se aplicam a administradores ou serviços. Para alterar esses limites padrão, consulte [políticas de grupo](group-policies.md).

O exemplo a seguir mostra como criar um trabalho de download. O exemplo supõe que a \_ variável g pbcm é um ponteiro de interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) válido. Para obter detalhes sobre como criar o ponteiro de interface **IBackgroundCopyManager** , consulte [conectando-se ao serviço bits](connecting-to-the-bits-service.md).


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



Para obter a interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) mais recente, chame o método **método ibackgroundcopyjob:: QueryInterface** . O exemplo a seguir mostra como obter a interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




