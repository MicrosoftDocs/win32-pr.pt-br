---
description: Capturando uma imagem de um PIN de imagem ainda
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Capturando uma imagem de um PIN de imagem ainda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645796"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="8ea08-103">Capturando uma imagem de um PIN de imagem ainda</span><span class="sxs-lookup"><span data-stu-id="8ea08-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="8ea08-104">Algumas câmeras podem produzir uma imagem ainda separada do fluxo de captura e, muitas vezes, a imagem ainda é de maior qualidade do que as imagens produzidas pelo fluxo de captura.</span><span class="sxs-lookup"><span data-stu-id="8ea08-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="8ea08-105">A câmera pode ter um botão que atue como um gatilho de hardware ou pode dar suporte ao acionamento de software.</span><span class="sxs-lookup"><span data-stu-id="8ea08-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="8ea08-106">Uma câmera que dá suporte a imagens ainda exporá um PIN de imagem ainda, que é fixar categoria de PIN de categoria \_ \_ ainda.</span><span class="sxs-lookup"><span data-stu-id="8ea08-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="8ea08-107">A maneira recomendada de obter imagens do dispositivo é usar as APIs de aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="8ea08-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="8ea08-108">Para obter mais informações, consulte "aquisição de imagem do Windows" na documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="8ea08-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="8ea08-109">No entanto, você também pode usar o DirectShow para capturar uma imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea08-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="8ea08-110">Para disparar o PIN ainda, use o método [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) quando o grafo estiver em execução, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8ea08-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


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



<span data-ttu-id="8ea08-111">Consulte o filtro de captura para [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span><span class="sxs-lookup"><span data-stu-id="8ea08-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="8ea08-112">Se a interface tiver suporte, obtenha um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino ainda chamando o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="8ea08-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="8ea08-113">Em seguida, chame [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) com o ponteiro **IPin** e o \_ sinalizador de gatilho VideoControlFlag.</span><span class="sxs-lookup"><span data-stu-id="8ea08-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="8ea08-114">Dependendo da câmera, talvez seja necessário renderizar o pino de captura (fixar \_ categoria \_ Capture) antes que o PIN ainda seja conectado.</span><span class="sxs-lookup"><span data-stu-id="8ea08-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="8ea08-115">Exemplo: usando o filtro de apoio de exemplo</span><span class="sxs-lookup"><span data-stu-id="8ea08-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="8ea08-116">Uma maneira de capturar a imagem é com o filtro de [**apoio de exemplo**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea08-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="8ea08-117">O exemplo de apoio usa uma função de retorno de chamada definida pelo aplicativo para processar a imagem.</span><span class="sxs-lookup"><span data-stu-id="8ea08-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="8ea08-118">Para obter mais informações sobre o filtro de apoio de exemplo, consulte [usando o exemplo de apoio](using-the-sample-grabber.md).</span><span class="sxs-lookup"><span data-stu-id="8ea08-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="8ea08-119">O exemplo a seguir pressupõe que o PIN ainda fornece uma imagem RGB não compactada.</span><span class="sxs-lookup"><span data-stu-id="8ea08-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="8ea08-120">Primeiro, defina uma classe que irá implementar a interface de retorno de chamada de exemplo, [**ISampleGrabberCB**](isamplegrabbercb.md):</span><span class="sxs-lookup"><span data-stu-id="8ea08-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="8ea08-121">A implementação da classe é descrita em breve.</span><span class="sxs-lookup"><span data-stu-id="8ea08-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="8ea08-122">Em seguida, conecte o pino ainda ao exemplo de amostra e conecte o exemplo de amostra ao filtro de [**renderizador nulo**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea08-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="8ea08-123">O processador nulo simplesmente descarta amostras de mídia recebidas; o trabalho real será feito dentro do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8ea08-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="8ea08-124">(O único motivo para o renderizador NULL é conectar o pino de saída do exemplo de amostra a algo). Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar os filtros de amostra e de processador nulo de exemplo e chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar ambos os filtros ao grafo:</span><span class="sxs-lookup"><span data-stu-id="8ea08-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


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



<span data-ttu-id="8ea08-125">Você pode usar o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar todos os três filtros em uma chamada de método, indo do pino ainda para o exemplo de amostra e do exemplo de apoio para o renderizador nulo:</span><span class="sxs-lookup"><span data-stu-id="8ea08-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="8ea08-126">Agora, use a interface [**ISampleGrabber**](isamplegrabber.md) para configurar o exemplo de apoio de forma que ele armazena em buffer exemplos:</span><span class="sxs-lookup"><span data-stu-id="8ea08-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


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



<span data-ttu-id="8ea08-127">Defina a interface de retorno de chamada com um ponteiro para o objeto de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="8ea08-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="8ea08-128">Obtenha o tipo de mídia que ainda é o PIN usado para se conectar com o exemplo de apoio:</span><span class="sxs-lookup"><span data-stu-id="8ea08-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="8ea08-129">Esse tipo de mídia conterá a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define o formato da imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="8ea08-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="8ea08-130">Libere o tipo de mídia antes de o aplicativo sair:</span><span class="sxs-lookup"><span data-stu-id="8ea08-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="8ea08-131">O que vem a seguir é um exemplo da classe de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8ea08-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="8ea08-132">Observe que a classe implementa **IUnknown**, que herda pela interface [**ISampleGrabber**](isamplegrabber.md) , mas não mantém uma contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="8ea08-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="8ea08-133">Isso é seguro porque o aplicativo cria o objeto na pilha e o objeto permanece no escopo durante todo o tempo de vida do gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="8ea08-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="8ea08-134">Todo o trabalho ocorre no método [**BufferCB**](isamplegrabbercb-buffercb.md) , que é chamado pelo apoio de exemplo sempre que obtém um novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="8ea08-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="8ea08-135">No exemplo a seguir, o método grava o bitmap em um arquivo:</span><span class="sxs-lookup"><span data-stu-id="8ea08-135">In the following example, the method writes the bitmap to a file:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8ea08-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ea08-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea08-137">Tarefas de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8ea08-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
