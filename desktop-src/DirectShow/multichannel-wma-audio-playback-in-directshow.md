---
description: Reprodução de áudio WMA multicanal DirectShow
ms.assetid: 99c69290-545a-4368-8f51-74e547c9466d
title: Reprodução de áudio WMA multicanal DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e7f7841677a7b7bc4087b2644632bbf6ec9cd48bccc15274506c6c57f96f89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830976"
---
# <a name="multichannel-wma-audio-playback-in-directshow"></a>Reprodução de áudio WMA multicanal DirectShow

Para reproduzir um arquivo de áudio de mídia multicanal Windows no DirectShow, você deve definir a propriedade **MFPKEY \_ WCODE \_ HIRESOUTPUT** diretamente no decodificador depois que ele tiver sido conectado ao Leitor do WM ASF. Essa propriedade é definida no arquivo de header wmcodecdsp.h, que está disponível no SDK do Windows.

> [!Note]  
> Esse procedimento de configuração tem suporte apenas para arquivos que não são protegidos pelo Digital Rights Management.

 

As etapas básicas para habilitar a saída multicanal são as seguintes:

1.  Chame **RenderFile** para criar o grafo de filtro.
2.  Obtenha um ponteiro para o filtro DMO Wrapper.
3.  Desconecte DMO Wrapper do Renderdor de Áudio.
4.  Use a interface **IPropertyBag** para definir a **propriedade \_ MFPKEY WCODE \_ HIRESOUTPUT** no decodificador. O nome da propriedade é definido pela constante global **g \_ wszWMACHiResOutput**.
5.  Reconecte o DMO Wrapper e o Renderdor de Áudio.
6.  Execute o grafo.

Os snippets de código a seguir demonstram essas etapas. Esse código presume que o arquivo de origem contém um fluxo de áudio e nenhum fluxo de vídeo. O codec de DMO de vídeo não dá suporte à **propriedade MFPKEY \_ W VIRALC \_ HIRESOUTPUT.**


```C++
HRESULT BuildGraph(IGraphBuilder *pGraph, const WCHAR *wFileName)
{
    HRESULT hr = S_OK;
    IBaseFilter       *pDmoWrapper = NULL;
    IPin              *pDmoOut = NULL;
    IPin              *pRendererIn = NULL;
    IPropertyBag      *pPropBag = NULL;

    hr = pGraph->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    if (SUCCEEDED(hr))
    {
        hr = GetDMOWrapper(pGraph, &pDmoWrapper); 
    }

    //Disconnect the DMO Wrapper from the Audio Renderer.
    if (SUCCEEDED(hr))
    {
        hr = GetPin(pDmoWrapper, PINDIR_OUTPUT, &pDmoOut);
    }
    if (SUCCEEDED(hr))
    {
        hr = DisconnectPin(pGraph, pDmoOut, &pRendererIn);
    }

    //Set the property on the DMO.
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;

    if (SUCCEEDED(hr))
    {
        hr = pDmoWrapper->QueryInterface(IID_IPropertyBag, (void**)&pPropBag);
    }
    if (SUCCEEDED(hr))
    {
        hr = pPropBag->Write(g_wszWMACHiResOutput, &varg);
    }

    // Reconnect the DMO Wrapper and the Audio Renderer
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Connect(pDmoOut, pRendererIn);
    }

    SAFE_RELEASE(pDmoWrapper);
    SAFE_RELEASE(pDmoOut);
    SAFE_RELEASE(pRendererIn);
    SAFE_RELEASE(pPropBag);
    return hr;
}
```



As funções auxiliares do snippet de código anterior são implementadas da seguinte forma:


```C++
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** ppFilter) 
{
    BOOL bFound = FALSE;

    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter = NULL;
    IDMOWrapperFilter *pWrapper = NULL;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pFilter, NULL) == S_OK)
        {
            // If we find the IDMOWrapperFilter interface, that means we 
            // have the DMO Wrapper filter. 
            hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
            if (SUCCEEDED(hr))
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pFilter);
        }
    }

    if (bFound)
    {
        *ppFilter = pFilter;
        (*ppFilter)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pEnum);
    SAFE_RELEASE(pFilter);
    SAFE_RELEASE(pWrapper);
    return hr;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    BOOL bFound = FALSE;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (SUCCEEDED(hr))
    {
        while(pEnum->Next(1, &pPin, 0) == S_OK)
        {
            PIN_DIRECTION PinDirThis;
            hr = pPin->QueryDirection(&PinDirThis);
            if (FAILED(hr))
            {
                break;
            }
            if (PinDir == PinDirThis)
            {
                bFound = TRUE;
                break;
            }
            SAFE_RELEASE(pPin);
        }
    }

    if (bFound)
    {
        *ppPin = pPin;
        (*ppPin)->AddRef();
    }
    else
    {
        hr = E_FAIL;
    }

    SAFE_RELEASE(pPin);
    SAFE_RELEASE(pEnum);
    return hr;
}

HRESULT DisconnectPin(IGraphBuilder *pGraph, IPin *pPin, IPin **ppConnected)
{
    IPin *pConnected = NULL;

    HRESULT hr = pPin->ConnectedTo(&pConnected);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pPin);
    }
    if (SUCCEEDED(hr))
    {
        hr = pGraph->Disconnect(pConnected);
    }
    if (SUCCEEDED(hr))
    {
        *ppConnected = pConnected;
        (*ppConnected)->AddRef();
    }

    SAFE_RELEASE(pConnected);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



