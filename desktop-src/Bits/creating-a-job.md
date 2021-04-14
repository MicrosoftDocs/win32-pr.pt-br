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
# <a name="creating-a-job"></a><span data-ttu-id="9798d-105">Criando um trabalho</span><span class="sxs-lookup"><span data-stu-id="9798d-105">Creating a Job</span></span>

<span data-ttu-id="9798d-106">Para criar um trabalho de transferência, chame o método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="9798d-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="9798d-107">Depois que o BITS cria o trabalho, [adicione arquivos ao trabalho](adding-files-to-a-job.md) e [modifique as propriedades do trabalho](setting-and-retrieving-the-properties-of-a-job.md) conforme apropriado para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9798d-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="9798d-108">Para ativar o trabalho na fila, chame o método [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .</span><span class="sxs-lookup"><span data-stu-id="9798d-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="9798d-109">O método [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) cria um GUID que identifica exclusivamente o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9798d-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="9798d-110">Você usa o GUID para [recuperar o trabalho da fila de transferência](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="9798d-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="9798d-111">O nome de exibição que você fornece ao criar o trabalho não é exclusivo; mais de um trabalho pode usar o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="9798d-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="9798d-112">O BITS limita o número de trabalhos na fila para trabalhos de 300 e o número de trabalhos que um usuário pode criar para o trabalho de 60.</span><span class="sxs-lookup"><span data-stu-id="9798d-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="9798d-113">Esses limites não se aplicam a administradores ou serviços.</span><span class="sxs-lookup"><span data-stu-id="9798d-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="9798d-114">Para alterar esses limites padrão, consulte [políticas de grupo](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9798d-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="9798d-115">O exemplo a seguir mostra como criar um trabalho de download.</span><span class="sxs-lookup"><span data-stu-id="9798d-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="9798d-116">O exemplo supõe que a \_ variável g pbcm é um ponteiro de interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) válido.</span><span class="sxs-lookup"><span data-stu-id="9798d-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="9798d-117">Para obter detalhes sobre como criar o ponteiro de interface **IBackgroundCopyManager** , consulte [conectando-se ao serviço bits](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="9798d-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


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



<span data-ttu-id="9798d-118">Para obter a interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) mais recente, chame o método **método ibackgroundcopyjob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="9798d-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="9798d-119">O exemplo a seguir mostra como obter a interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .</span><span class="sxs-lookup"><span data-stu-id="9798d-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


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



 

 




