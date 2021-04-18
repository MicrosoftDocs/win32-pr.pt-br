---
description: Carregando um arquivo GraphEdit programaticamente
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Carregando um arquivo GraphEdit programaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456631"
---
# <a name="loading-a-graphedit-file-programmatically"></a><span data-ttu-id="53a40-103">Carregando um arquivo GraphEdit programaticamente</span><span class="sxs-lookup"><span data-stu-id="53a40-103">Loading a GraphEdit File Programmatically</span></span>

<span data-ttu-id="53a40-104">Um aplicativo pode usar a interface **IPersistStream** para carregar um arquivo GraphEdit (. GRF).</span><span class="sxs-lookup"><span data-stu-id="53a40-104">An application can use the **IPersistStream** interface to load a GraphEdit (.grf) file.</span></span> <span data-ttu-id="53a40-105">Use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="53a40-105">Use the following code:</span></span>


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> <span data-ttu-id="53a40-106">A chamada para **IPersistStream:: Load** no exemplo de código anterior pode retornar um erro do DirectShow ou um código de êxito.</span><span class="sxs-lookup"><span data-stu-id="53a40-106">The call to **IPersistStream::Load** in the previous code example can return a DirectShow error or success code.</span></span> <span data-ttu-id="53a40-107">Para obter uma lista de possíveis valores de retorno, consulte [códigos de erro e êxito](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="53a40-107">For a list of possible return values, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 

<span data-ttu-id="53a40-108">Os arquivos GraphEdit são destinados apenas para teste e depuração.</span><span class="sxs-lookup"><span data-stu-id="53a40-108">GraphEdit files are intended only for testing and debugging.</span></span> <span data-ttu-id="53a40-109">Eles não são destinados ao uso por aplicativos do usuário final.</span><span class="sxs-lookup"><span data-stu-id="53a40-109">They are not meant for use by end-user applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53a40-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53a40-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53a40-111">Simulando a criação de gráficos com o GraphEdit</span><span class="sxs-lookup"><span data-stu-id="53a40-111">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="53a40-112">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="53a40-112">**StgIsStorageFile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[<span data-ttu-id="53a40-113">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="53a40-113">**StgOpenStorage**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
