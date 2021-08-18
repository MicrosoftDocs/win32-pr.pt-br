---
description: Capturando em vários arquivos
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Capturando em vários arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ce7a1b4b91a0f78031a661e2c2e10895b4a21b1cfb068ca505429468a3af1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017574"
---
# <a name="capturing-to-multiple-files"></a>Capturando em vários arquivos

Depois de capturar algum vídeo em um arquivo, você pode alternar para um novo arquivo interrompendo o grafo e definindo o nome do arquivo no filtro [Do autor do](file-writer-filter.md) arquivo. Chame o [**método IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) no File Writer. Você pode obter um ponteiro para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) ao criar o grafo, por meio do parâmetro *pSink* do método SetOutputFileName. O código a seguir mostra como fazer isso:


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando vídeo em um arquivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



