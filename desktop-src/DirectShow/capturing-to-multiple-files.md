---
description: Capturando para vários arquivos
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Capturando para vários arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087462"
---
# <a name="capturing-to-multiple-files"></a><span data-ttu-id="796af-103">Capturando para vários arquivos</span><span class="sxs-lookup"><span data-stu-id="796af-103">Capturing to Multiple Files</span></span>

<span data-ttu-id="796af-104">Depois de capturar algum vídeo em um arquivo, você pode alternar para um novo arquivo interrompendo o grafo e Configurando o nome do arquivo no filtro do [gravador de arquivo](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="796af-104">After you have captured some video to a file, you can switch to a new file by stopping the graph and setting the file name on the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="796af-105">Chame o método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) no gravador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="796af-105">Call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method on the File Writer.</span></span> <span data-ttu-id="796af-106">Você pode obter um ponteiro para a interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) ao criar o grafo, por meio do parâmetro *PSink* do método SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="796af-106">You can get a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface when you build the graph, through the *pSink* parameter of the SetOutputFileName method.</span></span> <span data-ttu-id="796af-107">O código a seguir mostra como fazer isso:</span><span class="sxs-lookup"><span data-stu-id="796af-107">The following code shows how to do this:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="796af-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="796af-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="796af-109">Capturando vídeo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="796af-109">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



