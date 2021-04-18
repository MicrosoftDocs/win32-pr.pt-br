---
description: Este tutorial usa o gravador de coletor para codificar um arquivo de vídeo.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Tutorial: usando o gravador de coletor para codificar vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764043"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="71865-103">Tutorial: usando o gravador de coletor para codificar vídeo</span><span class="sxs-lookup"><span data-stu-id="71865-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="71865-104">Este tutorial usa o [gravador de coletor](sink-writer.md) para codificar um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71865-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="71865-105">Definir o formato de vídeo</span><span class="sxs-lookup"><span data-stu-id="71865-105">Define the Video Format</span></span>

<span data-ttu-id="71865-106">Para simplificar, este tutorial usa um formato de vídeo fixo, definido pelas seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="71865-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="71865-107">Essas constantes especificam os seguintes parâmetros do formato de vídeo:</span><span class="sxs-lookup"><span data-stu-id="71865-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="71865-108">Tamanho do quadro (largura e altura)</span><span class="sxs-lookup"><span data-stu-id="71865-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="71865-109">Quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="71865-109">Frames per second.</span></span>
-   <span data-ttu-id="71865-110">Taxa de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="71865-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="71865-111">Formato de codificação, que é o Windows Media Video 9 (**MFVideoFormat \_ WMV3**).</span><span class="sxs-lookup"><span data-stu-id="71865-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="71865-112">Formato de entrada, que é RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="71865-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="71865-113">Duração do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="71865-113">Duration of the output file.</span></span>

<span data-ttu-id="71865-114">O programa usa essas constantes para criar os tipos de mídia que descrevem o formato.</span><span class="sxs-lookup"><span data-stu-id="71865-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="71865-115">Em um aplicativo real, você normalmente ofereceria suporte a um intervalo de perfis de codificação.</span><span class="sxs-lookup"><span data-stu-id="71865-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="71865-116">Criar um quadro de vídeo descompactado</span><span class="sxs-lookup"><span data-stu-id="71865-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="71865-117">Também para simplificar, este tutorial usa um quadro de vídeo estático como entrada.</span><span class="sxs-lookup"><span data-stu-id="71865-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="71865-118">O quadro de vídeo contém um retângulo verde sólido e é gerado programaticamente.</span><span class="sxs-lookup"><span data-stu-id="71865-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="71865-119">O quadro de vídeo é armazenado em uma variável global como uma matriz de **DWORD** s:</span><span class="sxs-lookup"><span data-stu-id="71865-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="71865-120">O código a seguir define cada pixel no quadro como verde:</span><span class="sxs-lookup"><span data-stu-id="71865-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="71865-121">Inicializar o gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="71865-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="71865-122">Para inicializar o gravador de coletor, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="71865-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="71865-123">Chame [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) para criar uma nova instância do gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="71865-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="71865-124">Crie um tipo de mídia que descreva o vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="71865-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="71865-125">Passe este tipo de mídia para o método [**IMFSinkWriter:: AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) .</span><span class="sxs-lookup"><span data-stu-id="71865-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="71865-126">Crie um segundo tipo de mídia que descreva a entrada não compactada.</span><span class="sxs-lookup"><span data-stu-id="71865-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="71865-127">Passe o tipo de mídia descompactado para o método [**IMFSinkWriter:: SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .</span><span class="sxs-lookup"><span data-stu-id="71865-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="71865-128">Chame o método [**IMFSinkWriter:: BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) .</span><span class="sxs-lookup"><span data-stu-id="71865-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="71865-129">O gravador do coletor agora está pronto para aceitar exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="71865-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="71865-130">O código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="71865-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="71865-131">A maioria das etapas no exemplo de código anterior é definir os atributos do tipo de mídia para os dois tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="71865-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="71865-132">Os detalhes dos tipos de mídia dependerão do seu conteúdo de origem e do perfil de codificação desejado.</span><span class="sxs-lookup"><span data-stu-id="71865-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="71865-133">Enviar quadros de vídeo para o gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="71865-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="71865-134">Para enviar um quadro de vídeo para o gravador do coletor, chame o método [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="71865-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="71865-135">O método **WriteSample** usa um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , que representa um objeto de *exemplo de mídia* .</span><span class="sxs-lookup"><span data-stu-id="71865-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="71865-136">O exemplo de mídia contém um objeto de *buffer de mídia* que, por sua vez, contém um ponteiro para o quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71865-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="71865-137">Para obter mais informações sobre exemplos de mídia e buffer, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="71865-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="71865-138">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="71865-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="71865-139">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="71865-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="71865-140">Dependendo do seu aplicativo, você pode obter os exemplos de mídia do [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="71865-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="71865-141">Como alternativa, você pode criar os exemplos de mídia e manipular diretamente os dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="71865-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="71865-142">O código a seguir mostra a segunda abordagem.</span><span class="sxs-lookup"><span data-stu-id="71865-142">The following code shows the second approach.</span></span> <span data-ttu-id="71865-143">Ele cria um buffer de memória e grava um único quadro de vídeo no buffer.</span><span class="sxs-lookup"><span data-stu-id="71865-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="71865-144">Em seguida, ele adiciona esse buffer a um exemplo de mídia e envia o exemplo de mídia para o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="71865-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="71865-145">Esse código executa as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="71865-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="71865-146">Chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para criar um objeto de buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="71865-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="71865-147">Essa função aloca a memória para o buffer.</span><span class="sxs-lookup"><span data-stu-id="71865-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="71865-148">Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para bloquear o buffer e obter um ponteiro para a memória.</span><span class="sxs-lookup"><span data-stu-id="71865-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="71865-149">Chame [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) para copiar o quadro de vídeo para o buffer.</span><span class="sxs-lookup"><span data-stu-id="71865-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="71865-150">Neste exemplo específico, usar **memcpy** também funcionaria.</span><span class="sxs-lookup"><span data-stu-id="71865-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="71865-151">No entanto, a função [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) manipula corretamente o caso em que o stride da imagem de origem não corresponde ao buffer de destino.</span><span class="sxs-lookup"><span data-stu-id="71865-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="71865-152">Para obter mais informações, consulte [Stride de imagem](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="71865-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="71865-153">Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer.</span><span class="sxs-lookup"><span data-stu-id="71865-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="71865-154">Chame [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) para atualizar o comprimento dos dados válidos no buffer.</span><span class="sxs-lookup"><span data-stu-id="71865-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="71865-155">(Caso contrário, esse valor assume zero como padrão.)</span><span class="sxs-lookup"><span data-stu-id="71865-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="71865-156">Chame [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) para criar um objeto de exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="71865-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="71865-157">Chame [**IMFSample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para adicionar o buffer de mídia ao exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="71865-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="71865-158">Chame [**IMFSample:: Setamostratime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) para definir o carimbo de data/hora para o quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71865-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="71865-159">Chame [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) para definir a duração do quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71865-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="71865-160">Chame [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) para enviar o exemplo de mídia para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="71865-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="71865-161">Gravar a função main</span><span class="sxs-lookup"><span data-stu-id="71865-161">Write the main Function</span></span>

<span data-ttu-id="71865-162">Dentro da `main` função, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="71865-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="71865-163">Chame [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="71865-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="71865-164">Chame [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="71865-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="71865-165">Crie o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="71865-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="71865-166">Enviar quadros de vídeo para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="71865-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="71865-167">Chame [**IMFSinkWriter:: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) para finalizar o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="71865-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="71865-168">Libere o ponteiro para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="71865-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="71865-169">Chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="71865-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="71865-170">Chame [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="71865-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="71865-171">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="71865-171">Example Code</span></span>

<span data-ttu-id="71865-172">O código a seguir mostra o programa completo.</span><span class="sxs-lookup"><span data-stu-id="71865-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="71865-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71865-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71865-174">Gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="71865-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
