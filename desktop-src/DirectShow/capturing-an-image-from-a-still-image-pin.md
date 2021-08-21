---
description: Capturando uma imagem de um PIN de imagem ainda
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Capturando uma imagem de um PIN de imagem ainda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab750fb6b847bc39d28c8906df8dcb982278f7a4447bfc3d79631ee58eb574e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158658"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Capturando uma imagem de um PIN de imagem ainda

Algumas câmeras podem produzir uma imagem ainda separada do fluxo de captura e, muitas vezes, a imagem ainda é de maior qualidade do que as imagens produzidas pelo fluxo de captura. A câmera pode ter um botão que atue como um gatilho de hardware ou pode dar suporte ao acionamento de software. Uma câmera que dá suporte a imagens ainda exporá um PIN de imagem ainda, que é fixar categoria de PIN de categoria \_ \_ ainda.

a maneira recomendada de obter imagens do dispositivo é usar as APIs da WIA (Windows Image Acquisition). para obter mais informações, consulte "Windows Image Acquisition" na documentação do Platform SDK. no entanto, você também pode usar DirectShow para capturar uma imagem.

Para disparar o PIN ainda, use o método [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) quando o grafo estiver em execução, da seguinte maneira:


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



Consulte o filtro de captura para [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol). Se a interface tiver suporte, obtenha um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino ainda chamando o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , conforme mostrado no exemplo anterior. Em seguida, chame [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) com o ponteiro **IPin** e o \_ sinalizador de gatilho VideoControlFlag.

> [!Note]  
> Dependendo da câmera, talvez seja necessário renderizar o pino de captura (fixar \_ categoria \_ Capture) antes que o PIN ainda seja conectado.

 

### <a name="example-using-the-sample-grabber-filter"></a>Exemplo: usando o filtro de apoio de exemplo

Uma maneira de capturar a imagem é com o filtro de [**apoio de exemplo**](sample-grabber-filter.md) . O exemplo de apoio usa uma função de retorno de chamada definida pelo aplicativo para processar a imagem. Para obter mais informações sobre o filtro de apoio de exemplo, consulte [usando o exemplo de apoio](using-the-sample-grabber.md).

O exemplo a seguir pressupõe que o PIN ainda fornece uma imagem RGB não compactada. Primeiro, defina uma classe que irá implementar a interface de retorno de chamada de exemplo, [**ISampleGrabberCB**](isamplegrabbercb.md):


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



A implementação da classe é descrita em breve.

Em seguida, conecte o pino ainda ao exemplo de amostra e conecte o exemplo de amostra ao filtro de [**renderizador nulo**](null-renderer-filter.md) . O processador nulo simplesmente descarta amostras de mídia recebidas; o trabalho real será feito dentro do retorno de chamada. (O único motivo para o renderizador NULL é conectar o pino de saída do exemplo de amostra a algo). Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar os filtros de amostra e de processador nulo de exemplo e chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar ambos os filtros ao grafo:


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



Você pode usar o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar todos os três filtros em uma chamada de método, indo do pino ainda para o exemplo de amostra e do exemplo de apoio para o renderizador nulo:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



Agora, use a interface [**ISampleGrabber**](isamplegrabber.md) para configurar o exemplo de apoio de forma que ele armazena em buffer exemplos:


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



Defina a interface de retorno de chamada com um ponteiro para o objeto de retorno de chamada:


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Obtenha o tipo de mídia que ainda é o PIN usado para se conectar com o exemplo de apoio:


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Esse tipo de mídia conterá a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define o formato da imagem ainda. Libere o tipo de mídia antes de o aplicativo sair:


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



O que vem a seguir é um exemplo da classe de retorno de chamada. Observe que a classe implementa **IUnknown**, que herda pela interface [**ISampleGrabber**](isamplegrabber.md) , mas não mantém uma contagem de referência. Isso é seguro porque o aplicativo cria o objeto na pilha e o objeto permanece no escopo durante todo o tempo de vida do gráfico de filtro.

Todo o trabalho ocorre no método [**BufferCB**](isamplegrabbercb-buffercb.md) , que é chamado pelo apoio de exemplo sempre que obtém um novo exemplo. No exemplo a seguir, o método grava o bitmap em um arquivo:


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de captura de vídeo](video-capture-tasks.md)
</dt> </dl>

 

 
