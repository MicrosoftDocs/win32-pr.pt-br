---
description: Este tópico faz uma análise detalhada do exemplo de SDK de origem de mídia MPEG-1.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Estudo de caso: fonte de mídia MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011918"
---
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="9a4a8-103">Estudo de caso: fonte de mídia MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9a4a8-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="9a4a8-104">No Microsoft Media Foundation, o objeto que apresenta os dados de mídia no pipeline de dados é chamado de *fonte de mídia*.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="9a4a8-105">Este tópico faz uma análise detalhada do exemplo de SDK de [origem de mídia MPEG-1](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="9a4a8-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9a4a8-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="9a4a8-107">Classes C++ usadas na origem MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9a4a8-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="9a4a8-108">Manipulador de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="9a4a8-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="9a4a8-109">Descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="9a4a8-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="9a4a8-110">Estados de streaming</span><span class="sxs-lookup"><span data-stu-id="9a4a8-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="9a4a8-111">Iniciar</span><span class="sxs-lookup"><span data-stu-id="9a4a8-111">Start</span></span>](#start)
    -   [<span data-ttu-id="9a4a8-112">Pausar</span><span class="sxs-lookup"><span data-stu-id="9a4a8-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="9a4a8-113">Parar</span><span class="sxs-lookup"><span data-stu-id="9a4a8-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="9a4a8-114">Solicitações de amostra</span><span class="sxs-lookup"><span data-stu-id="9a4a8-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="9a4a8-115">Fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="9a4a8-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="9a4a8-116">Operações assíncronas</span><span class="sxs-lookup"><span data-stu-id="9a4a8-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="9a4a8-117">Fila de operações</span><span class="sxs-lookup"><span data-stu-id="9a4a8-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="9a4a8-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a4a8-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="9a4a8-119">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9a4a8-119">Prerequisites</span></span>

<span data-ttu-id="9a4a8-120">Antes de ler este tópico, você deve entender os seguintes conceitos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="9a4a8-121">Modelo de objeto de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="9a4a8-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="9a4a8-122">[Métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="9a4a8-123">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="9a4a8-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="9a4a8-124">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="9a4a8-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="9a4a8-125">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="9a4a8-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="9a4a8-126">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="9a4a8-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="9a4a8-127">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="9a4a8-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="9a4a8-128">Você também deve ter um entendimento básico da arquitetura de Media Foundation, particularmente a função das fontes de mídia no pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="9a4a8-129">(Para obter mais informações, consulte [fontes de mídia](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="9a4a8-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="9a4a8-130">Além disso, talvez você queira ler o tópico [escrevendo uma fonte de mídia personalizada](writing-a-custom-media-source.md), que fornece uma visão geral mais geral das etapas descritas aqui.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="9a4a8-131">Este tópico não reproduz todo o código do exemplo do SDK, porque o exemplo é bastante grande.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="9a4a8-132">Classes C++ usadas na origem MPEG-1</span><span class="sxs-lookup"><span data-stu-id="9a4a8-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="9a4a8-133">A fonte MPEG-1 de exemplo é implementada com as seguintes classes C++:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="9a4a8-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="9a4a8-135">Implementa o manipulador de fluxo de bytes para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="9a4a8-136">Dado um fluxo de bytes, o manipulador de fluxo de bytes cria uma instância da origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="9a4a8-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-137">`MPEG1Source`.</span></span> <span data-ttu-id="9a4a8-138">Implementa a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-138">Implements the media source.</span></span>
-   <span data-ttu-id="9a4a8-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-139">`MPEG1Stream`.</span></span> <span data-ttu-id="9a4a8-140">Implementa os objetos de fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-140">Implements the media stream objects.</span></span> <span data-ttu-id="9a4a8-141">A origem de mídia cria um `MPEG1Stream` objeto para cada fluxo de áudio ou vídeo no fragmentado MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="9a4a8-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-142">`Parser`.</span></span> <span data-ttu-id="9a4a8-143">Analisa o fragmentado MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="9a4a8-144">Para a maior parte, os detalhes dessa classe não são relevantes para as APIs de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="9a4a8-145">SourceOp, OpQueue: essas duas classes gerenciam operações assíncronas na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="9a4a8-146">(Consulte [operações assíncronas](#asynchronous-operations)).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="9a4a8-147">Outras classes auxiliares diversas são descritas posteriormente no tópico.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="9a4a8-148">Manipulador de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="9a4a8-148">Byte-Stream Handler</span></span>

<span data-ttu-id="9a4a8-149">O manipulador de *fluxo de bytes* é o objeto que cria a origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="9a4a8-150">O manipulador de fluxo de bytes é criado pelo resolvedor de origem; os aplicativos não interagem diretamente com o manipulador de fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="9a4a8-151">O resolvedor de origem descobre o manipulador de fluxo de bytes examinando o registro.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="9a4a8-152">O manipulador é registrado por extensão de nome de arquivo ou tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="9a4a8-153">Para a origem MPEG-1, o manipulador de fluxo de bytes é registrado para a extensão de nome de arquivo ". mpg".</span><span class="sxs-lookup"><span data-stu-id="9a4a8-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="9a4a8-154">Se você quiser dar suporte a esquemas de URL personalizados, também poderá escrever um *manipulador de esquema*.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="9a4a8-155">A fonte MPEG-1 foi projetada para arquivos locais e Media Foundation já fornece um manipulador de esquema para URLs "file://".</span><span class="sxs-lookup"><span data-stu-id="9a4a8-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="9a4a8-156">O manipulador byte-Stream implementa a interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="9a4a8-157">Essa interface tem dois métodos mais importantes que devem ser implementados:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="9a4a8-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="9a4a8-159">Inicia uma operação assíncrona para criar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="9a4a8-160">[](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="9a4a8-161">Conclui a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="9a4a8-162">Dois outros métodos são opcionais e não são implementados no exemplo do SDK:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="9a4a8-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="9a4a8-164">Cancela o método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="9a4a8-165">Esse método é útil para uma fonte de rede que pode ter uma alta latência na inicialização.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="9a4a8-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="9a4a8-167">Obtém o número máximo de bytes que o manipulador lerá do fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="9a4a8-168">Implemente esse método se você souber a quantidade de dados que o manipulador de fluxo de bytes antes de poder criar a origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="9a4a8-169">Caso contrário, basta retornar **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="9a4a8-170">Aqui está a implementação do método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :</span><span class="sxs-lookup"><span data-stu-id="9a4a8-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



<span data-ttu-id="9a4a8-171">O método executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="9a4a8-172">Cria uma nova instância do objeto `MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="9a4a8-173">Crie um objeto de resultado assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-173">Create an asynchronous result object.</span></span> <span data-ttu-id="9a4a8-174">Esse objeto é usado posteriormente para invocar o método de retorno de chamada do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="9a4a8-175">Chama `MPEG1Source::BeginOpen` , um método assíncrono definido na `MPEG1Source` classe.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="9a4a8-176">Define *ppIUnknownCancelCookie* como **NULL**, que informa ao chamador que não há suporte para [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="9a4a8-177">O `MPEG1Source::BeginOpen` método faz o trabalho real de ler o fluxo de bytes e inicializar o `MPEG1Source` objeto.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="9a4a8-178">Esse método não faz parte da API pública.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-178">This method is not part of the public API.</span></span> <span data-ttu-id="9a4a8-179">Você pode definir qualquer mecanismo entre o manipulador e a fonte de mídia que atenda às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="9a4a8-180">Colocar a maior parte da lógica na origem da mídia mantém o manipulador de fluxo de bytes relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="9a4a8-181">Resumindo, `BeginOpen` o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="9a4a8-182">Chama [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) para verificar se o fluxo de bytes de origem é legível e pesquisável.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="9a4a8-183">Chama [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) para iniciar uma solicitação de e/s assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="9a4a8-184">O restante da inicialização ocorre de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="9a4a8-185">A origem da mídia lê dados suficientes do fluxo para analisar os cabeçalhos de sequência MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="9a4a8-186">Em seguida, ele cria um *descritor de apresentação*, que é o objeto usado para descrever os fluxos de áudio e vídeo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="9a4a8-187">(Para obter mais informações, consulte [descritor de apresentação](#presentation-descriptor).) Quando a `BeginOpen` operação é concluída, o manipulador de fluxo de bytes invoca o método de retorno de chamada do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="9a4a8-188">Nesse ponto, o resolvedor de origem chama [**IMFByteStreamHandler:: Endcreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="9a4a8-189">O método **Endcreateobject** retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-189">The **EndCreateObject** method returns the status of the operation.</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



<span data-ttu-id="9a4a8-190">Se ocorrer um erro a qualquer momento durante esse processo, o retorno de chamada será invocado com um código de status de erro.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="9a4a8-191">Descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="9a4a8-191">Presentation Descriptor</span></span>

<span data-ttu-id="9a4a8-192">O descritor de apresentação descreve o conteúdo do arquivo MPEG-1, incluindo as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="9a4a8-193">O número de fluxos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-193">The number of the streams.</span></span>
-   <span data-ttu-id="9a4a8-194">O formato de cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-194">The format of each stream.</span></span>
-   <span data-ttu-id="9a4a8-195">Identificadores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-195">Stream identifiers.</span></span>
-   <span data-ttu-id="9a4a8-196">O status de seleção de cada fluxo (selecionado ou desmarcado).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="9a4a8-197">Em termos da arquitetura de Media Foundation, o descritor de apresentação contém um ou mais descritores de *fluxo*.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="9a4a8-198">Cada descritor de fluxo contém um *manipulador de tipo de mídia*, que é usado para obter ou definir tipos de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="9a4a8-199">Media Foundation fornece implementações de estoque para o descritor de apresentação e o descritor de fluxo; Eles são adequados para a maioria das fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="9a4a8-200">Para criar um descritor de apresentação, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="9a4a8-201">Para cada fluxo:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-201">For each stream:</span></span>
    1.  <span data-ttu-id="9a4a8-202">Forneça uma ID de fluxo e uma matriz de tipos de mídia possíveis.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="9a4a8-203">Se o fluxo der suporte a mais de um tipo de mídia, ordene a lista de tipos de mídia por preferência, se houver.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="9a4a8-204">(Coloque o tipo ideal primeiro e o tipo menos ideal por último.)</span><span class="sxs-lookup"><span data-stu-id="9a4a8-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="9a4a8-205">Chame [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) para criar o descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="9a4a8-206">Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="9a4a8-207">Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para definir o formato padrão para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="9a4a8-208">Se houver mais de um tipo de mídia, você geralmente deve definir o primeiro tipo na lista.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="9a4a8-209">Chame [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) e transmita a matriz de ponteiros de descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="9a4a8-210">Para cada fluxo, chame [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) ou [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) para definir o estado de seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="9a4a8-211">Se houver mais de um fluxo do mesmo tipo (áudio ou vídeo), somente um deverá ser selecionado por padrão.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="9a4a8-212">O `MPEG1Source` objeto cria o descritor de apresentação em seu `InitPresentationDescriptor` método:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



<span data-ttu-id="9a4a8-213">O aplicativo obtém o descritor de apresentação chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="9a4a8-214">Esse método cria uma cópia superficial do descritor de apresentação chamando [**IMFPresentationDescriptor:: clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="9a4a8-215">(A cópia contém ponteiros para os descritores de fluxo originais.) O aplicativo pode usar o descritor de apresentação para definir o tipo de mídia, selecionar um fluxo ou anular a seleção de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="9a4a8-216">Opcionalmente, os descritores de apresentação e os descritores de fluxo podem conter atributos que fornecem informações adicionais sobre a origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="9a4a8-217">Para obter uma lista desses atributos, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="9a4a8-218">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="9a4a8-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="9a4a8-219">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="9a4a8-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="9a4a8-220">Um atributo merece menção especial: o atributo de [**\_ \_ duração de PD de MF**](mf-pd-duration-attribute.md) contém a duração total da origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="9a4a8-221">Defina este atributo se souber a duração antecipada; por exemplo, a duração pode ser especificada nos cabeçalhos de arquivo, dependendo do formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="9a4a8-222">O aplicativo pode exibir esse valor ou usá-lo para definir uma barra de progresso ou uma barra de busca.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="9a4a8-223">Estados de streaming</span><span class="sxs-lookup"><span data-stu-id="9a4a8-223">Streaming States</span></span>

<span data-ttu-id="9a4a8-224">Uma fonte de mídia define os seguintes Estados:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-224">A media source defines the following states:</span></span>



| <span data-ttu-id="9a4a8-225">Estado</span><span class="sxs-lookup"><span data-stu-id="9a4a8-225">State</span></span>    | <span data-ttu-id="9a4a8-226">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a4a8-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4a8-227">Iniciado</span><span class="sxs-lookup"><span data-stu-id="9a4a8-227">Started</span></span>  | <span data-ttu-id="9a4a8-228">A origem aceita e processa solicitações de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="9a4a8-229">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="9a4a8-229">Paused</span></span>   | <span data-ttu-id="9a4a8-230">A origem aceita solicitações de exemplo, mas não as processa.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="9a4a8-231">As solicitações são enfileiradas até que a origem seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="9a4a8-232">Stopped.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-232">Stopped.</span></span> | <span data-ttu-id="9a4a8-233">A origem rejeita solicitações de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="9a4a8-234">Iniciar</span><span class="sxs-lookup"><span data-stu-id="9a4a8-234">Start</span></span>

<span data-ttu-id="9a4a8-235">O método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="9a4a8-236">Ele usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="9a4a8-237">Um descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="9a4a8-238">Um GUID de formato temporal.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-238">A time-format GUID.</span></span>
-   <span data-ttu-id="9a4a8-239">Uma posição inicial.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-239">A start position.</span></span>

<span data-ttu-id="9a4a8-240">O aplicativo deve obter o descritor de apresentação chamando [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) na origem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="9a4a8-241">Não há um mecanismo definido para validar um descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="9a4a8-242">Se o aplicativo especificar o descritor de apresentação errado, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="9a4a8-243">O GUID de formato de tempo especifica como interpretar a posição inicial.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="9a4a8-244">O formato padrão é de 100-nanossegundos (ns), indicado por GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="9a4a8-245">Cada fonte de mídia deve dar suporte a unidades 100-NS.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="9a4a8-246">Opcionalmente, uma fonte pode dar suporte a outras unidades de tempo, como um número de quadro ou código de tempo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="9a4a8-247">No entanto, não há uma maneira padrão de consultar uma fonte de mídia para a lista de formatos de hora com suporte.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="9a4a8-248">A posição inicial é fornecida como um **PROPVARIANT**, permitindo tipos de dados diferentes, dependendo do formato de hora.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="9a4a8-249">Para 100-NS, o tipo **PROPVARIANT** é **VT \_ i8** ou **VT \_ vazio**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="9a4a8-250">Se **VT \_ i8**, o **PROPVARIANT** conterá a posição inicial nas unidades 100-NS.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="9a4a8-251">O valor **VT \_ vazio** tem o significado especial "Iniciar na posição atual".</span><span class="sxs-lookup"><span data-stu-id="9a4a8-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="9a4a8-252">Implemente o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="9a4a8-253">Validar parâmetros e estado:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="9a4a8-254">Verifique se há parâmetros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="9a4a8-255">Verifique o GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-255">Check the time-format GUID.</span></span> <span data-ttu-id="9a4a8-256">Se o valor for inválido, retorne **MF \_ E \_ formato de \_ hora \_ sem suporte**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="9a4a8-257">Verifique o tipo de dados do **PROPVARIANT** que contém a posição inicial.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="9a4a8-258">Validar a posição inicial.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-258">Validate the start position.</span></span> <span data-ttu-id="9a4a8-259">Se for inválido, retorne **MF \_ E \_ INVALIDREQUEST**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="9a4a8-260">Se a origem tiver sido desligada, retorne o **MF \_ E o \_ desligamento**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="9a4a8-261">Se nenhum erro ocorrer na etapa 1, enfileirar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="9a4a8-262">Tudo depois dessa etapa ocorre em um thread de fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="9a4a8-263">Para cada fluxo:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-263">For each stream:</span></span>
    1.  <span data-ttu-id="9a4a8-264">Verifique se o fluxo já está ativo de uma solicitação de [**início**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) anterior.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="9a4a8-265">Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para verificar se o aplicativo selecionou ou desselecionou o fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="9a4a8-266">Se um fluxo selecionado anteriormente agora estiver desmarcado, libere quaisquer amostras não entregues para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="9a4a8-267">Se o fluxo estiver ativo, a origem da mídia (não o fluxo) enviará um dos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="9a4a8-268">Ele envia [MEUpdatedStream](meupdatedstream.md) se o fluxo estava ativo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="9a4a8-269">Caso contrário, ele envia [MENewStream](menewstream.md).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="9a4a8-270">Para ambos os eventos, os dados do evento são o ponteiro [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="9a4a8-271">Se a origem estiver reiniciando no estado pausado, pode haver solicitações de exemplo pendentes.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="9a4a8-272">Nesse caso, entregue-os agora.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="9a4a8-273">Se a origem estiver buscando uma nova posição, cada objeto de fluxo enviará um evento [MEStreamSeeked](mestreamseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="9a4a8-274">Caso contrário, cada fluxo envia um evento [MEStreamStarted](mestreamstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="9a4a8-275">Se a origem estiver buscando uma nova posição, a origem da mídia enviará um evento [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="9a4a8-276">Caso contrário, ele envia um evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="9a4a8-277">Se ocorrer um erro a qualquer momento após a etapa 2, a origem enviará um evento [MESourceStarted](mesourcestarted.md) com um código de erro.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="9a4a8-278">Isso alerta o aplicativo de que o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) falhou de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="9a4a8-279">O código a seguir mostra as etapas 1 a 2:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-279">The following code shows steps 1–2:</span></span>


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="9a4a8-280">As etapas restantes são mostradas no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-280">The remaining steps are shown in the next example:</span></span>


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a><span data-ttu-id="9a4a8-281">Pausar</span><span class="sxs-lookup"><span data-stu-id="9a4a8-281">Pause</span></span>

<span data-ttu-id="9a4a8-282">O método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) faz uma pausa na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="9a4a8-283">Implemente esse método da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="9a4a8-284">Enfileirar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="9a4a8-285">Cada fluxo ativo envia um evento [MEStreamPaused](mestreampaused.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="9a4a8-286">A origem de mídia envia um evento [MESourcePaused](mesourcepaused.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="9a4a8-287">Enquanto está em pausa, as filas de origem são solicitações de amostra sem processá-las.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="9a4a8-288">(Consulte [exemplos de solicitações](#sample-requests).)</span><span class="sxs-lookup"><span data-stu-id="9a4a8-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="9a4a8-289">Stop</span><span class="sxs-lookup"><span data-stu-id="9a4a8-289">Stop</span></span>

<span data-ttu-id="9a4a8-290">O método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) interrompe a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="9a4a8-291">Implemente esse método da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="9a4a8-292">Enfileirar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="9a4a8-293">Cada fluxo ativo envia um evento [MEStreamStopped](mestreamstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="9a4a8-294">Limpe todas as amostras em fila e as solicitações de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="9a4a8-295">A origem de mídia envia um evento [MESourceStopped](mesourcestopped.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="9a4a8-296">Enquanto é interrompido, a origem rejeita todas as solicitações de exemplos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="9a4a8-297">Se a origem for interrompida enquanto uma solicitação de e/s estiver em andamento, a solicitação de e/s poderá ser concluída depois que a origem entrar no estado parado.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="9a4a8-298">Nesse caso, a origem deve descartar o resultado dessa solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="9a4a8-299">Solicitações de Amostra</span><span class="sxs-lookup"><span data-stu-id="9a4a8-299">Sample Requests</span></span>

<span data-ttu-id="9a4a8-300">Media Foundation usar um modelo de *pull* , no qual o pipeline solicita amostras da origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="9a4a8-301">Isso difere do modelo usado pelo DirectShow, no qual as fontes "enviam" exemplos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="9a4a8-302">Para solicitar um novo exemplo, o pipeline de Media Foundation chama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="9a4a8-303">Esse método usa um ponteiro **IUnknown** que representa um objeto de *token* .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="9a4a8-304">A implementação do objeto de token é até o chamador; Ele simplesmente fornece uma maneira para o chamador controlar as solicitações de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="9a4a8-305">O parâmetro de token também pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="9a4a8-306">Supondo que a origem use solicitações de e/s assíncronas para ler dados, a geração de amostra não será sincronizada com solicitações de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="9a4a8-307">Para sincronizar as solicitações de exemplo com a geração de exemplo, uma fonte de mídia faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="9a4a8-308">Os tokens de solicitação são colocados em uma fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="9a4a8-309">Como os exemplos são gerados, eles são colocados em uma segunda fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="9a4a8-310">A origem da mídia conclui uma solicitação de exemplo, obtendo um token de solicitação da primeira fila e um exemplo da segunda fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="9a4a8-311">A origem de mídia envia um evento MEMediaSample.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="9a4a8-312">O evento contém um ponteiro para o exemplo, e o exemplo contém um ponteiro para o token.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="9a4a8-313">O diagrama a seguir mostra a relação entre o evento [MEMediaSample](memediasample.md) , o exemplo e o token de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![diagrama mostrando memediasample e uma fila de exemplo apontando para imfsample; imfsample e o ponto da fila de solicitação para IUnknown](images/mediasourceimpl01.png)

<span data-ttu-id="9a4a8-315">O exemplo de origem MPEG-1 implementa esse processo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="9a4a8-316">O método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) coloca a solicitação em uma fila FIFO.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="9a4a8-317">À medida que as solicitações de e/s são concluídas, a origem da mídia cria novos exemplos e os coloca em uma segunda fila FIFO.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="9a4a8-318">(Essa fila tem um tamanho máximo, para impedir que a origem leia muito bem.)</span><span class="sxs-lookup"><span data-stu-id="9a4a8-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="9a4a8-319">Sempre que ambas as filas tiverem pelo menos um item (uma solicitação e uma amostra), a origem da mídia concluirá a primeira solicitação da fila de solicitações enviando a primeira amostra da fila de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="9a4a8-320">Para fornecer um exemplo, o objeto de fluxo (não o objeto de origem) envia um evento [MEMediaSample](memediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="9a4a8-321">Os dados do evento são um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="9a4a8-322">Se a solicitação incluir um token, anexe o token ao exemplo definindo o atributo de [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) no exemplo.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="9a4a8-323">Neste ponto, há três possibilidades:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="9a4a8-324">Há outro exemplo na fila de exemplo, mas nenhuma solicitação correspondente.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="9a4a8-325">Há uma solicitação, mas nenhuma amostra.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="9a4a8-326">Ambas as filas estão vazias; Não há amostras e nenhuma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="9a4a8-327">Se a fila de exemplo estiver vazia, a origem verificará o fim do fluxo (consulte [fim do fluxo](#end-of-stream)).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="9a4a8-328">Caso contrário, ele iniciará outra solicitação de e/s para dados.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="9a4a8-329">Se ocorrer algum erro durante esse processo, o fluxo enviará um evento [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="9a4a8-330">O código a seguir implementa o método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :</span><span class="sxs-lookup"><span data-stu-id="9a4a8-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



<span data-ttu-id="9a4a8-331">O `DispatchSamples` método extrai amostras da fila de exemplo, corresponde a elas com solicitações de exemplo pendentes e enfileira eventos de [MEMediaSample](memediasample.md) :</span><span class="sxs-lookup"><span data-stu-id="9a4a8-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



<span data-ttu-id="9a4a8-332">O `DispatchSamples` método é chamado nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="9a4a8-333">Dentro do método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="9a4a8-334">Quando a origem da mídia é reiniciada a partir do estado em pausa.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="9a4a8-335">Quando uma solicitação de e/s é concluída.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="9a4a8-336">Fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="9a4a8-336">End of Stream</span></span>

<span data-ttu-id="9a4a8-337">Quando um fluxo não tem mais dados, e todos os exemplos desse fluxo foram entregues, os objetos de fluxo enviam um evento [MEEndOfStream](meendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="9a4a8-338">Quando todos os fluxos ativos são concluídos, a origem da mídia envia um evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="9a4a8-339">Operações assíncronas</span><span class="sxs-lookup"><span data-stu-id="9a4a8-339">Asynchronous Operations</span></span>

<span data-ttu-id="9a4a8-340">Talvez a parte mais difícil de escrever uma fonte de mídia esteja compreendendo o modelo assíncrono Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="9a4a8-341">Todos os métodos em uma fonte de mídia que controlam o streaming são assíncronos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="9a4a8-342">Em cada caso, o método faz alguma validação inicial, como verificar parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="9a4a8-343">A origem, em seguida, distribui o restante do trabalho para uma fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="9a4a8-344">Após a conclusão da operação, a origem da mídia envia um evento de volta para o chamador, por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="9a4a8-345">Portanto, é importante entender as filas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="9a4a8-346">Para colocar um item em uma fila de trabalho, você pode chamar [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="9a4a8-347">A origem MPEG-1 acontece com o uso de **MFPutWorkItem**, mas as duas funções fazem a mesma coisa.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="9a4a8-348">A função **MFPutWorkItem** usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="9a4a8-349">Um valor **DWORD** que identifica a fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="9a4a8-350">Você pode criar uma fila de trabalho particular ou usar o **\_ padrão de fila de retorno de chamada \_ \_ MFASYNC**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="9a4a8-351">Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="9a4a8-352">Essa interface de retorno de chamada é invocada para executar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="9a4a8-353">Um objeto de estado opcional, que deve implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="9a4a8-354">A fila de trabalho é atendida por um ou mais threads de trabalho que recebem continuamente o próximo item de trabalho da fila e invocam o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) da interface de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="9a4a8-355">Não há garantia de que os itens de trabalho sejam executados na mesma ordem em que você os coloca na fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="9a4a8-356">Lembre-se de que mais de um thread pode atender à mesma fila de trabalho, portanto, [**invocar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) chamadas pode se sobrepor ou ocorrer fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="9a4a8-357">Portanto, cabe à origem da mídia manter o estado interno correto, enviando itens da fila de trabalho na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="9a4a8-358">Somente quando a operação anterior for concluída, a origem iniciará a próxima operação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="9a4a8-359">Para representar operações pendentes, a origem MPEG-1 define uma classe chamada `SourceOp` :</span><span class="sxs-lookup"><span data-stu-id="9a4a8-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



<span data-ttu-id="9a4a8-360">A `Operation` enumeração identifica qual operação está pendente.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="9a4a8-361">A classe também contém um **PROPVARIANT** para transmitir quaisquer dados adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="9a4a8-362">Fila de operações</span><span class="sxs-lookup"><span data-stu-id="9a4a8-362">Operation Queue</span></span>

<span data-ttu-id="9a4a8-363">Para serializar operações, a origem da mídia mantém uma fila de `SourceOp` objetos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="9a4a8-364">Ele usa uma classe auxiliar para gerenciar a fila:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-364">It uses a helper class to manage the queue:</span></span>


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



<span data-ttu-id="9a4a8-365">A `OpQueue` classe foi projetada para ser herdada pelo componente que executa itens de trabalho assíncronos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="9a4a8-366">O parâmetro de modelo de *\_ tipo OP* é o tipo de objeto usado para representar itens de trabalho na fila — nesse caso, o *\_ tipo OP* será `SourceOp` .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="9a4a8-367">A `OpQueue` classe implementa os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="9a4a8-368">`QueueOperation` coloca um novo item na fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="9a4a8-369">`ProcessQueue` Despacha a próxima operação da fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="9a4a8-370">Esse método é assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="9a4a8-371">`ProcessQueueAsync` conclui o método assíncrono `ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="9a4a8-372">Outros dois métodos devem ser implementados pela classe derivada:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="9a4a8-373">`ValidateOperation` verifica se é válido executar uma operação especificada, considerando o estado atual da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="9a4a8-374">`DispatchOperation` executa o item de trabalho assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="9a4a8-375">A fila de operação é usada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="9a4a8-376">O pipeline de Media Foundation chama um método assíncrono na origem da mídia, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="9a4a8-377">As chamadas de método assíncrono `QueueOperation` , que coloca a operação de [**inicialização**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) na fila e as chama `ProcessQueue` (na forma de um `SourceOp` objeto).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="9a4a8-378">`ProcessQueue` chama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="9a4a8-379">O thread de fila de trabalho chama `ProcessQueueAsync` .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="9a4a8-380">O `ProcessQueueAsync` método chama `ValidateOperation` e `DispatchOperation` .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="9a4a8-381">O código a seguir enfileira uma nova operação na fonte MPEG-1:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-381">The following code queues a new operation on the MPEG-1 source:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



<span data-ttu-id="9a4a8-382">O código a seguir processa a fila:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-382">The following code processes the queue:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



<span data-ttu-id="9a4a8-383">O `ValidateOperation` método verifica se a origem MPEG-1 pode enviar a próxima operação na fila.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="9a4a8-384">Se outra operação estiver em andamento, `ValidateOperation` retornará **MF \_ E não \_ aceitar**.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="9a4a8-385">Isso garante que o `DispatchOperation` não seja chamado enquanto houver outra operação pendente.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



<span data-ttu-id="9a4a8-386">O método DispatchOperation alterna para o tipo de operação:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-386">The DispatchOperation method switches on the operation type:</span></span>


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="9a4a8-387">Para resumir:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-387">To summarize:</span></span>

1.  <span data-ttu-id="9a4a8-388">O pipeline chama um método assíncrono, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="9a4a8-389">O método assíncrono chama `OpQueue::QueueOperation` , passando um ponteiro para um `SourceOp` objeto.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="9a4a8-390">O `QueueOperation` método coloca a operação na fila *m \_ OpQueue* e chama `OpQueue::ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="9a4a8-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="9a4a8-391">O `ProcessQueue` método chama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="9a4a8-392">A partir desse ponto, tudo acontece em um thread de fila de trabalho Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="9a4a8-393">O método assíncrono retorna ao chamador.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="9a4a8-394">O thread de fila de trabalho chama o `OpQueue::ProcessQueueAsync` método.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="9a4a8-395">O `ProcessQueueAsync` método chama `MPEG1Source:ValidateOperation` para validar a operação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="9a4a8-396">O `ProcessQueueAsync` método chama `MPEG1Source::DispatchOperation` para processar a operação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="9a4a8-397">Há vários benefícios para esse design:</span><span class="sxs-lookup"><span data-stu-id="9a4a8-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="9a4a8-398">Os métodos são assíncronos, portanto, não bloqueiam o thread do aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="9a4a8-399">As operações são expedidas em um Media Foundation thread de fila de trabalho, que é compartilhado entre componentes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="9a4a8-400">Portanto, a origem da mídia não cria seu próprio thread, reduzindo o número total de threads que são criados.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="9a4a8-401">A origem da mídia não é bloqueada enquanto aguarda a conclusão das operações.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="9a4a8-402">Isso reduz a chance de que uma fonte de mídia cause acidentalmente um deadlock e ajuda a reduzir a alternância de contexto.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="9a4a8-403">A origem da mídia pode usar e/s assíncrona para ler o arquivo de origem (chamando [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span><span class="sxs-lookup"><span data-stu-id="9a4a8-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="9a4a8-404">A origem da mídia não precisa ser bloqueada enquanto aguarda a conclusão da rotina de e/s.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="9a4a8-405">Se você seguir o padrão mostrado no exemplo de SDK, poderá se concentrar nos detalhes específicos de sua fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a4a8-406">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a4a8-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a4a8-407">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="9a4a8-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="9a4a8-408">Gravando uma fonte de mídia personalizada</span><span class="sxs-lookup"><span data-stu-id="9a4a8-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



