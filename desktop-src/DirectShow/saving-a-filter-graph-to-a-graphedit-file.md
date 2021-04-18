---
description: Salvando um grafo de filtro em um arquivo GraphEdit
ms.assetid: f7eeae3c-506b-484c-8fe5-ddd391af5a59
title: Salvando um grafo de filtro em um arquivo GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5fb24c40f11dbeb5dad8b542f0f152449f8951
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768782"
---
# <a name="saving-a-filter-graph-to-a-graphedit-file"></a>Salvando um grafo de filtro em um arquivo GraphEdit

O exemplo de código a seguir mostra como salvar um gráfico de filtro em um arquivo GraphEdit (. GRF). Isso pode ser útil para depurar seus aplicativos.


```C++
HRESULT SaveGraphFile(IGraphBuilder *pGraph, WCHAR *wszPath) 
{
    const WCHAR wszStreamName[] = L"ActiveMovieGraph"; 
    HRESULT hr;
    
    IStorage *pStorage = NULL;
    hr = StgCreateDocfile(
        wszPath,
        STGM_CREATE | STGM_TRANSACTED | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0, &pStorage);
    if(FAILED(hr)) 
    {
        return hr;
    }

    IStream *pStream;
    hr = pStorage->CreateStream(
        wszStreamName,
        STGM_WRITE | STGM_CREATE | STGM_SHARE_EXCLUSIVE,
        0, 0, &pStream);
    if (FAILED(hr)) 
    {
        pStorage->Release();    
        return hr;
    }

    IPersistStream *pPersist = NULL;
    pGraph->QueryInterface(IID_IPersistStream, (void**)&pPersist);
    hr = pPersist->Save(pStream, TRUE);
    pStream->Release();
    pPersist->Release();
    if (SUCCEEDED(hr)) 
    {
        hr = pStorage->Commit(STGC_DEFAULT);
    }
    pStorage->Release();
    return hr;
}
```



Por exemplo, o código a seguir cria um grafo de reprodução de arquivo e o salva em um arquivo chamado MYGRAPH. GRF:


```C++
void __cdecl main(void)
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    CoInitialize(NULL);
    
    // Create the Filter Graph Manager and render a file.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
        IID_IGraphBuilder, reinterpret_cast<void**>(&pGraph));
    hr = pGraph->RenderFile(L"C:\\Video.avi", NULL);

    if (SUCCEEDED(hr))
    {
        hr = SaveGraphFile(pGraph, L"C:\\MyGraph.grf");
    }
    
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Simulando a criação de gráficos com o GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgCreateDocfile**](/windows/win32/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> </dl>

 

 
