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
# <a name="multichannel-audio-playback-in-directshow"></a><span data-ttu-id="149af-116">Reprodução de áudio multicanal no DirectShow</span><span class="sxs-lookup"><span data-stu-id="149af-116">Multichannel Audio Playback in DirectShow</span></span>

<span data-ttu-id="149af-117">Para reproduzir um arquivo Multichannel de áudio do Windows Media no DirectShow, você deve definir a \_ Propriedade "HIRESOUTPUT" diretamente no decodificador após ele ter sido conectado ao leitor ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="149af-117">To play back a multichannel Windows Media Audio file in DirectShow, you must set the "\_HIRESOUTPUT" property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="149af-118">Nenhuma configuração do objeto leitor é necessária.</span><span class="sxs-lookup"><span data-stu-id="149af-118">No configuration of the Reader Object is necessary.</span></span> <span data-ttu-id="149af-119">No entanto, para trabalhar diretamente com o DMO, você precisa de wmcodecconst. h do [código de exemplo para usar o pacote de download das interfaces de áudio e vídeo do Windows Media](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="149af-119">However, to work with the DMO directly, you need wmcodecconst.h from the [Sample Code for Using the Windows Media Audio and Video Codec Interfaces](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) download package.</span></span>

<span data-ttu-id="149af-120">**Observação** Esse procedimento de configuração tem suporte apenas para arquivos que não são protegidos pelo Rights Management digital.</span><span class="sxs-lookup"><span data-stu-id="149af-120">**Note** This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

<span data-ttu-id="149af-121">As etapas básicas para habilitar a saída de multicanal são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="149af-121">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="149af-122">Chame RenderFile para criar o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="149af-122">Call RenderFile to create the filter graph.</span></span>
2.  <span data-ttu-id="149af-123">Obter um ponteiro para o filtro de invólucro do DMO</span><span class="sxs-lookup"><span data-stu-id="149af-123">Obtain a pointer to the DMO Wrapper filter</span></span>
3.  <span data-ttu-id="149af-124">Desconecte o invólucro de DMO do processador de áudio</span><span class="sxs-lookup"><span data-stu-id="149af-124">Disconnect the DMO Wrapper from the Audio Renderer</span></span>
4.  <span data-ttu-id="149af-125">Defina a \_ Propriedade "HIRESOUTPUT" no decodificador.</span><span class="sxs-lookup"><span data-stu-id="149af-125">Set the "\_HIRESOUTPUT" property on the decoder.</span></span>
5.  <span data-ttu-id="149af-126">Reconecte o invólucro de DMO e o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="149af-126">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="149af-127">Execute o grafo.</span><span class="sxs-lookup"><span data-stu-id="149af-127">Run the graph.</span></span>

<span data-ttu-id="149af-128">Os trechos de código a seguir demonstram essas etapas.</span><span class="sxs-lookup"><span data-stu-id="149af-128">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="149af-129">(Toda a verificação de erros foi omitida por questões de simplicidade.</span><span class="sxs-lookup"><span data-stu-id="149af-129">(All error checking has been omitted for the sake of simplicity.</span></span> <span data-ttu-id="149af-130">Você deve adicionar rotinas de tratamento de erro adequadas se usar esse código em um aplicativo.)</span><span class="sxs-lookup"><span data-stu-id="149af-130">You should add proper error handling routines if you use this code in an application.)</span></span>


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



<span data-ttu-id="149af-131">As funções GetDMOWrapper e GetPin do trecho de código anterior são implementadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="149af-131">The GetDMOWrapper and GetPin functions from the previous code snippet are implemented as follows:</span></span>


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



 

 




