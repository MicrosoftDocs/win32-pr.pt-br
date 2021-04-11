---
title: Reprodução de áudio multicanal no DirectShow
description: Reprodução de áudio multicanal no DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- SDK do Windows Media Format, DirectShow
- Windows Media Format SDK, reprodução de áudio multicanal
- SDK do Windows Media Format, reprodução de áudio
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), reprodução de áudio multicanal
- ASF (formato de sistemas avançados), reprodução de áudio multicanal
- ASF (Advanced Systems Format), reprodução de áudio
- ASF (formato de sistemas avançados), reprodução de áudio
- DirectShow, reprodução de áudio multicanal
- DirectShow, reprodução de áudio
- áudio de multicanal, reprodução
- reprodução de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365639"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Reprodução de áudio multicanal no DirectShow

Para reproduzir um arquivo Multichannel de áudio do Windows Media no DirectShow, você deve definir a \_ Propriedade "HIRESOUTPUT" diretamente no decodificador após ele ter sido conectado ao leitor ASF do WM. Nenhuma configuração do objeto leitor é necessária. No entanto, para trabalhar diretamente com o DMO, você precisa de wmcodecconst. h do [código de exemplo para usar o pacote de download das interfaces de áudio e vídeo do Windows Media](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .

**Observação** Esse procedimento de configuração tem suporte apenas para arquivos que não são protegidos pelo Rights Management digital.

As etapas básicas para habilitar a saída de multicanal são as seguintes:

1.  Chame RenderFile para criar o gráfico de filtro.
2.  Obter um ponteiro para o filtro de invólucro do DMO
3.  Desconecte o invólucro de DMO do processador de áudio
4.  Defina a \_ Propriedade "HIRESOUTPUT" no decodificador.
5.  Reconecte o invólucro de DMO e o processador de áudio.
6.  Execute o grafo.

Os trechos de código a seguir demonstram essas etapas. (Toda a verificação de erros foi omitida por questões de simplicidade. Você deve adicionar rotinas de tratamento de erro adequadas se usar esse código em um aplicativo.)


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



As funções GetDMOWrapper e GetPin do trecho de código anterior são implementadas da seguinte maneira:


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




