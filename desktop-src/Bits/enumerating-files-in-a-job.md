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
ms.openlocfilehash: 01a986b8a8869008db34e97c1cc7e0cd733c301f5cdc57ce4ef6e313ff382479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801456"
---
# <a name="enumerating-files-in-a-job"></a>Enumerando arquivos em um trabalho

Para enumerar arquivos em um trabalho, chame o método [**método ibackgroundcopyjob:: EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) . O método retorna um ponteiro de interface [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) que você usa para enumerar os arquivos.

Observe que a lista enumerada é um instantâneo dos arquivos no trabalho no momento em que você chama o método [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) . No entanto, os valores de propriedade desses objetos de arquivo refletem os valores atuais do arquivo.

O exemplo a seguir mostra como enumerar arquivos em um trabalho e recuperar suas propriedades. O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido.


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



 

 




