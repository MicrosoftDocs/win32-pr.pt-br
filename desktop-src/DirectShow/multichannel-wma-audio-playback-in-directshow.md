---
description: Reprodução de áudio de WMA multicanal no DirectShow
ms.assetid: 99c69290-545a-4368-8f51-74e547c9466d
title: Reprodução de áudio de WMA multicanal no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400ee9f0cede6c7268bcd3632365db1b423d114e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296024"
---
# <a name="multichannel-wma-audio-playback-in-directshow"></a>Reprodução de áudio de WMA multicanal no DirectShow

Para reproduzir um arquivo Multichannel de áudio do Windows Media no DirectShow, você deve definir a propriedade **MFPKEY \_ WMADEC \_ HIRESOUTPUT** diretamente no decodificador depois que ele estiver conectado ao leitor ASF do WM. Essa propriedade é definida no arquivo de cabeçalho wmcodecdsp. h, que está disponível no SDK do Windows.

> [!Note]  
> Esse procedimento de configuração tem suporte apenas para arquivos que não são protegidos pelo Rights Management digital.

 

As etapas básicas para habilitar a saída de multicanal são as seguintes:

1.  Chame **RenderFile** para criar o gráfico de filtro.
2.  Obtenha um ponteiro para o filtro de invólucro do DMO.
3.  Desconecte o invólucro de DMO do processador de áudio.
4.  Use a interface **IPropertyBag** para definir a propriedade **MFPKEY \_ WMADEC \_ HIRESOUTPUT** no decodificador. O nome da propriedade é definido pela constante global **g \_ wszWMACHiResOutput**.
5.  Reconecte o invólucro de DMO e o processador de áudio.
6.  Execute o grafo.

Os trechos de código a seguir demonstram essas etapas. Esse código pressupõe que o arquivo de origem contém um fluxo de áudio e nenhum fluxo de vídeo. O Video Codec DMO não dá suporte à propriedade **MFPKEY \_ WMADEC \_ HIRESOUTPUT** .


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



As funções auxiliares do trecho de código anterior são implementadas da seguinte maneira:


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

 

 



