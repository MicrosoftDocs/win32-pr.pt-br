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
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="5912e-109">Enumerando trabalhos na fila de transferência</span><span class="sxs-lookup"><span data-stu-id="5912e-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="5912e-110">Para enumerar trabalhos da fila de transferência, chame o método [**IBackgroundCopyManager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="5912e-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="5912e-111">O método retorna um ponteiro de interface [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) que você usa para enumerar os trabalhos na fila.</span><span class="sxs-lookup"><span data-stu-id="5912e-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="5912e-112">Para recuperar os trabalhos do usuário, defina o primeiro parâmetro do método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) como 0.</span><span class="sxs-lookup"><span data-stu-id="5912e-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="5912e-113">Para recuperar todos os trabalhos na fila, defina o primeiro parâmetro do método **EnumJobs** como BG \_ Job \_ enum \_ todos \_ os usuários.</span><span class="sxs-lookup"><span data-stu-id="5912e-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="5912e-114">Somente os usuários com privilégios de administrador podem recuperar todos os trabalhos na fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="5912e-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="5912e-115">Observe que a lista enumerada é um instantâneo dos trabalhos na fila de transferência no momento em que você chama o método [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="5912e-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="5912e-116">No entanto, os valores de propriedade desses trabalhos refletem os valores atuais do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5912e-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="5912e-117">Se você quiser recuperar trabalhos de transferência individuais, chame o método [**IBackgroundCopyManager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .</span><span class="sxs-lookup"><span data-stu-id="5912e-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="5912e-118">Para enumerar arquivos em um trabalho, consulte [enumerando arquivos em um trabalho](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="5912e-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="5912e-119">O exemplo a seguir mostra como enumerar trabalhos na fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="5912e-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="5912e-120">A \_ variável g XferManager no exemplo é um ponteiro de interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="5912e-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="5912e-121">Para obter detalhes sobre como criar o ponteiro de interface **IBackgroundCopyManager** , consulte [conectando-se ao serviço bits](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="5912e-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


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



 

 




