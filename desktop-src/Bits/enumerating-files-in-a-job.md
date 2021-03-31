---
title: Enumerando arquivos em um trabalho
description: Para enumerar arquivos em um trabalho, chame o método método ibackgroundcopyjob EnumFiles. O método retorna um ponteiro de interface IEnumBackgroundCopyFiles que você usa para enumerar os arquivos.
ms.assetid: 0e1fa024-4576-434c-bc5f-518d246b5faa
keywords:
- transferir BITS de trabalho, enumerando arquivos
- enumerando os BITS de arquivos
- Enumerando BITS, arquivos
- BITS de transferência de arquivo, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0db704e47a0e075801de2434ed30ba6fb8d8c91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635114"
---
# <a name="enumerating-files-in-a-job"></a><span data-ttu-id="c114b-108">Enumerando arquivos em um trabalho</span><span class="sxs-lookup"><span data-stu-id="c114b-108">Enumerating Files in a Job</span></span>

<span data-ttu-id="c114b-109">Para enumerar arquivos em um trabalho, chame o método [**método ibackgroundcopyjob:: EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) .</span><span class="sxs-lookup"><span data-stu-id="c114b-109">To enumerate files in a job, call the [**IBackgroundCopyJob::EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) method.</span></span> <span data-ttu-id="c114b-110">O método retorna um ponteiro de interface [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) que você usa para enumerar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="c114b-110">The method returns an [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) interface pointer that you use to enumerate the files.</span></span>

<span data-ttu-id="c114b-111">Observe que a lista enumerada é um instantâneo dos arquivos no trabalho no momento em que você chama o método [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) .</span><span class="sxs-lookup"><span data-stu-id="c114b-111">Note that the enumerated list is a snapshot of the files in the job at the time you call the [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) method.</span></span> <span data-ttu-id="c114b-112">No entanto, os valores de propriedade desses objetos de arquivo refletem os valores atuais do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c114b-112">However, the property values of those file objects reflect the current values of the file.</span></span>

<span data-ttu-id="c114b-113">O exemplo a seguir mostra como enumerar arquivos em um trabalho e recuperar suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c114b-113">The following example shows how to enumerate files in a job and retrieve their properties.</span></span> <span data-ttu-id="c114b-114">O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.</span><span class="sxs-lookup"><span data-stu-id="c114b-114">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
IBackgroundCopyJob* pJob;
IEnumBackgroundCopyFiles* pFiles = NULL;
IBackgroundCopyFile* pFile = NULL;
IBackgroundCopyFile3* pFile3 = NULL;
WCHAR* pLocalFileName = NULL;
ULONG cFileCount = 0;
ULONG idx = 0;

hr = pJob->EnumFiles(&pFiles);
if (SUCCEEDED(hr))
{
  //Get the count of files in the job. 
  pFiles->GetCount(&cFileCount);

  //Enumerate the files in the job.
  for (idx=0; idx<cFileCount; idx++)
  {
    hr = pFiles->Next(1, &pFile, NULL);
    if (S_OK == hr)
    {
      // Query for the latest file interface.
      hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile3), (void**)&pFile3);
      pFile->Release();
      if (FAILED(hr))
      {
        wprintf(L"pFile->QueryInterface failed with 0x%x.\n", hr);
        goto cleanup;
      }

      // You can use the interface to retrieve the local and remote file
      // names, get the ranges to download if only part of the file content
      // is requested, determine the progress of the transfer, change the remote file
      // name, get the name of the temporary file that BITS uses to download
      // the file, determine if the file is downloaded from a peer, and set
      // the validation state of the file so it can be shared with peers.

      //Get the local name of the file.
      hr = pFile3->GetLocalName(&pLocalFileName);
      if (SUCCEEDED(hr))
      {
        //Do something with the file information.
      }

      CoTaskMemFree(pLocalFileName); 
      pFile3->Release();
      pFile3 = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pFiles->Release();
  pFiles = NULL;
}
```



 

 




