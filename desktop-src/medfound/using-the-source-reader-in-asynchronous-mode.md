---
description: Este tópico descreve como usar o leitor de origem no modo assíncrono.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Usando o leitor de origem no modo assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010659"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="5d051-103">Usando o leitor de origem no modo assíncrono</span><span class="sxs-lookup"><span data-stu-id="5d051-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="5d051-104">Este tópico descreve como usar o [leitor de origem](source-reader.md) no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="5d051-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="5d051-105">No modo assíncrono, o aplicativo fornece uma interface de retorno de chamada, que é usada para notificar o aplicativo de que os dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5d051-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="5d051-106">Este tópico pressupõe que você já tenha lido o tópico [usando o leitor de origem para processar dados de mídia](processing-media-data-with-the-source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="5d051-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="5d051-107">Usando o modo assíncrono</span><span class="sxs-lookup"><span data-stu-id="5d051-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="5d051-108">O leitor de origem opera no modo síncrono ou no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="5d051-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="5d051-109">O exemplo de código mostrado na seção anterior pressupõe que o leitor de origem está usando o modo síncrono, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="5d051-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="5d051-110">No modo síncrono, o método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) é bloqueado enquanto a origem da mídia produz o próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="5d051-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="5d051-111">Uma fonte de mídia normalmente adquire dados de alguma fonte externa (como um arquivo local ou uma conexão de rede), para que o método possa bloquear o thread de chamada para um período de tempo perceptível.</span><span class="sxs-lookup"><span data-stu-id="5d051-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="5d051-112">No modo assíncrono, o [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retorna imediatamente e o trabalho é executado em outro thread.</span><span class="sxs-lookup"><span data-stu-id="5d051-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="5d051-113">Depois que a operação for concluída, o leitor de origem chamará o aplicativo por meio da interface de retorno de chamada [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) .</span><span class="sxs-lookup"><span data-stu-id="5d051-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="5d051-114">Para usar o modo assíncrono, você deve fornecer um ponteiro de retorno de chamada ao criar pela primeira vez o leitor de origem, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5d051-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="5d051-115">Crie um repositório de atributos chamando a função [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="5d051-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="5d051-116">Defina o atributo de [ \_ retorno de \_ \_ \_ chamada assíncrono do leitor de origem MF](mf-source-reader-async-callback.md) no repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="5d051-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="5d051-117">O valor do atributo é um ponteiro para seu objeto de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5d051-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="5d051-118">Ao criar o leitor de origem, passe o repositório de atributos para a função de criação no parâmetro *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="5d051-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="5d051-119">Todas as funções para criar o leitor de origem têm esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5d051-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="5d051-120">O exemplo a seguir mostra estas etapas.</span><span class="sxs-lookup"><span data-stu-id="5d051-120">The following example shows these steps.</span></span>


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="5d051-121">Depois de criar o leitor de origem, você não pode alternar os modos entre síncrono e assíncrono.</span><span class="sxs-lookup"><span data-stu-id="5d051-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="5d051-122">Para obter dados no modo assíncrono, chame o método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , mas defina os últimos quatro parâmetros como **NULL**, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d051-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="5d051-123">Quando o método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) é concluído de forma assíncrona, o leitor de origem chama o método [**IMFSourceReaderCallback:: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) .</span><span class="sxs-lookup"><span data-stu-id="5d051-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="5d051-124">Esse método tem cinco parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5d051-124">This method has five parameters:</span></span>

-   <span data-ttu-id="5d051-125">*hrStatus*: contém um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d051-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="5d051-126">Esse é o mesmo valor que [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) retornaria no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="5d051-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="5d051-127">Se *hrStatus* contiver um código de erro, você poderá ignorar os parâmetros restantes.</span><span class="sxs-lookup"><span data-stu-id="5d051-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="5d051-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp e *pSample*: esses três parâmetros são equivalentes aos últimos três parâmetros em [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="5d051-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="5d051-129">Eles contêm o número de fluxo, os sinalizadores de status e o ponteiro [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5d051-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="5d051-130">Além disso, a interface de retorno de chamada define dois outros métodos:</span><span class="sxs-lookup"><span data-stu-id="5d051-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="5d051-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span><span class="sxs-lookup"><span data-stu-id="5d051-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="5d051-132">Notifica o aplicativo quando determinados eventos ocorrem na origem de mídia, como buffer ou eventos de conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="5d051-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="5d051-133">Por [**descarregamento**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span><span class="sxs-lookup"><span data-stu-id="5d051-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="5d051-134">Chamado quando o método [**flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) é concluído.</span><span class="sxs-lookup"><span data-stu-id="5d051-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="5d051-135">Implementando a interface de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="5d051-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="5d051-136">A interface de retorno de chamada deve ser thread-safe, pois [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) e os outros métodos de retorno de chamada são chamados de threads de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5d051-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="5d051-137">Há várias abordagens diferentes que você pode tomar ao implementar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5d051-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="5d051-138">Por exemplo, você pode fazer todo o trabalho dentro do retorno de chamada, ou pode usar o retorno de chamada para notificar o aplicativo (por exemplo, sinalizando um identificador de evento) e, em seguida, trabalhar no thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d051-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="5d051-139">O método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) será chamado uma vez para cada chamada que você fizer para o método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) .</span><span class="sxs-lookup"><span data-stu-id="5d051-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="5d051-140">Para obter o próximo exemplo, chame **ReadSample** novamente.</span><span class="sxs-lookup"><span data-stu-id="5d051-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="5d051-141">Se ocorrer um erro, **OnReadSample** será chamado com um código de erro para o parâmetro *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="5d051-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="5d051-142">O exemplo a seguir mostra uma implementação mínima da interface de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5d051-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="5d051-143">Primeiro, aqui está a declaração de uma classe que implementa a interface.</span><span class="sxs-lookup"><span data-stu-id="5d051-143">First, here is the declaration of a class that implements the interface.</span></span>


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



<span data-ttu-id="5d051-144">Neste exemplo, não estamos [**interessados nos métodos**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) [**ondescarrega e onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , então eles simplesmente retornam **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d051-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="5d051-145">A classe usa um identificador de evento para sinalizar o aplicativo; Esse identificador é fornecido por meio do construtor.</span><span class="sxs-lookup"><span data-stu-id="5d051-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="5d051-146">Neste exemplo mínimo, o método [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) apenas imprime o carimbo de data/hora na janela do console.</span><span class="sxs-lookup"><span data-stu-id="5d051-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="5d051-147">Em seguida, ele armazena o código de status e o sinalizador de fim de fluxo e sinaliza o identificador de evento:</span><span class="sxs-lookup"><span data-stu-id="5d051-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



<span data-ttu-id="5d051-148">O código a seguir mostra que o aplicativo usaria essa classe de retorno de chamada para ler todos os quadros de vídeo de um arquivo de mídia:</span><span class="sxs-lookup"><span data-stu-id="5d051-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5d051-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d051-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d051-150">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="5d051-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



