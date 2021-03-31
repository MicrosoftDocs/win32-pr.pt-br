---
title: Determinando o progresso de um trabalho
description: O BITS mantém as informações de progresso de cada trabalho. Use as informações de progresso para determinar quantos bytes e arquivos foram transferidos.
ms.assetid: 8bac62b3-cb7e-45ba-85f0-95f3a7e8bffd
keywords:
- transferir BITS de trabalho, progresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085ddcdeea106be2998f828879bc92273f22b328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822299"
---
# <a name="determining-the-progress-of-a-job"></a><span data-ttu-id="9a2da-105">Determinando o progresso de um trabalho</span><span class="sxs-lookup"><span data-stu-id="9a2da-105">Determining the Progress of a Job</span></span>

<span data-ttu-id="9a2da-106">O BITS mantém as informações de progresso de cada trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a2da-106">BITS maintains progress information for each job.</span></span> <span data-ttu-id="9a2da-107">Use as informações de progresso para determinar quantos bytes e arquivos foram transferidos.</span><span class="sxs-lookup"><span data-stu-id="9a2da-107">Use the progress information to determine how many bytes and files have been transferred.</span></span>

<span data-ttu-id="9a2da-108">Para recuperar as informações de progresso do trabalho, chame o método [**método ibackgroundcopyjob:: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a2da-108">To retrieve progress information for the job, call the [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) method as shown in the following example.</span></span> <span data-ttu-id="9a2da-109">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.</span><span class="sxs-lookup"><span data-stu-id="9a2da-109">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
#define PROGRESS_COMPLETE_LEN 50

HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR szProgressComplete[PROGRESS_COMPLETE_LEN+1];
BG_JOB_PROGRESS Progress;

hr = pJob->GetProgress(&Progress); 
if (FAILED(hr))
{
  //Handle error
}

//Because the BytesTotal member can be 0 or BG_SIZE_UNKNOWN, you may not be able 
//to determine a percentage value to display, such as 57%. It is best to display a 
//string that shows the number of bytes transferred. For example, "123456 of 
//999999" or "123456 of Unknown".
if (BG_SIZE_UNKNOWN == Progress.BytesTotal)
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of Unknown", 
     Progress.BytesTransferred);
}
else
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of %I64d", 
     Progress.BytesTransferred, Progress.BytesTotal); 
}
```



<span data-ttu-id="9a2da-110">Para recuperar as informações de progresso na parte de resposta de um trabalho de resposta de upload, chame o método [**IBackgroundCopyJob2:: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a2da-110">To retrieve progress information on the reply portion of an upload reply job, call the [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) method as shown in the following example.</span></span> <span data-ttu-id="9a2da-111">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.</span><span class="sxs-lookup"><span data-stu-id="9a2da-111">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
#define REPLY_COMPLETE_LEN 4

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szReplyComplete[REPLY_COMPLETE_LEN+1];
BG_JOB_REPLY_PROGRESS Progress;

pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
hr = pJob2->GetReplyProgress(&Progress); 
if (SUCCEEDED(hr))
{
  if (0 == Progress.BytesTotal) //The job type is not BG_JOB_TYPE_UPLOAD_REPLY
  {
    //Logic to deal with this case  
  }
  else if (BG_SIZE_UNKNOWN == Progress.BytesTotal) //The reply has not begun
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1, L"0%%");
  }
  else
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1 L"%I64d%%",
       100*Progress.BytesTransferred/Progress.BytesTotal); 
  }
}
```



<span data-ttu-id="9a2da-112">Os arquivos também contêm informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="9a2da-112">Files also contain progress information.</span></span> <span data-ttu-id="9a2da-113">Para recuperar as informações de progresso, use o método [**IBackgroundCopyFile:: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyfile-getprogress) .</span><span class="sxs-lookup"><span data-stu-id="9a2da-113">To retrieve the progress information, use the [**IBackgroundCopyFile::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyfile-getprogress) method.</span></span> <span data-ttu-id="9a2da-114">Para obter informações sobre como recuperar os arquivos de um trabalho, consulte [enumerando arquivos em um trabalho](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="9a2da-114">For information on how to retrieve the files of a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

 

 




