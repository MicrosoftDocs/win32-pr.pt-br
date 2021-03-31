---
description: Etapa 3 implementar a função Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Etapa 3 implementar a função Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829374"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a><span data-ttu-id="5f809-103">Etapa 3: implementar a função Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="5f809-103">Step 3: Implement the Frame-Grabbing Function</span></span>

<span data-ttu-id="5f809-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="5f809-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5f809-105">Este tópico é a etapa 3 de [captar um quadro de cartaz](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="5f809-105">This topic is Step 3 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="5f809-106">A próxima etapa é implementar a função getbitmap, que usa o detector de mídia para pegar um quadro de pôster.</span><span class="sxs-lookup"><span data-stu-id="5f809-106">The next step is to implement the GetBitmap function, which uses the Media Detector to grab a poster frame.</span></span> <span data-ttu-id="5f809-107">Dentro dessa função, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5f809-107">Inside this function, perform the following steps:</span></span>

1.  <span data-ttu-id="5f809-108">Crie o detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="5f809-108">Create the Media Detector.</span></span>
2.  <span data-ttu-id="5f809-109">Especifique um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5f809-109">Specify a media file.</span></span>
3.  <span data-ttu-id="5f809-110">Examine cada fluxo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5f809-110">Examine each stream in the file.</span></span> <span data-ttu-id="5f809-111">Se for um fluxo de vídeo, obtenha as dimensões nativas do vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f809-111">If it is a video stream, get the native dimensions of the video.</span></span>
4.  <span data-ttu-id="5f809-112">Obtenha um quadro de cartaz, especificando o tempo de busca e a dimensão de destino.</span><span class="sxs-lookup"><span data-stu-id="5f809-112">Obtain a poster frame, specifying the seek time and the target dimension.</span></span>

<span data-ttu-id="5f809-113">Crie o objeto do detector de mídia chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span><span class="sxs-lookup"><span data-stu-id="5f809-113">Create the Media Detector object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span></span>


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



<span data-ttu-id="5f809-114">Especifique um nome de arquivo, usando o método [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="5f809-114">Specify a file name, using the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method.</span></span> <span data-ttu-id="5f809-115">Esse método usa um parâmetro **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="5f809-115">This method takes a **BSTR** parameter.</span></span>


```C++
hr = pDet->put_Filename(bstrFilename);
```



<span data-ttu-id="5f809-116">Obtenha o número de fluxos e execute um loop em cada fluxo verificando o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5f809-116">Get the number of streams, and loop through each stream checking the media type.</span></span> <span data-ttu-id="5f809-117">O método [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) recupera o número de fluxos e o método [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) especifica qual fluxo examinar.</span><span class="sxs-lookup"><span data-stu-id="5f809-117">The [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) method retrieves the number of streams, and the [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) method specifies which stream to examine.</span></span> <span data-ttu-id="5f809-118">Saia do loop no primeiro fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f809-118">Exit the loop on the first video stream.</span></span>


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



<span data-ttu-id="5f809-119">Se nenhum fluxo de vídeo for encontrado, a função será encerrada.</span><span class="sxs-lookup"><span data-stu-id="5f809-119">If no video stream was found, the function exits.</span></span>

<span data-ttu-id="5f809-120">No código anterior, o método [**\_ streamtype IMediaDet:: Get**](imediadet-get-streamtype.md) retorna apenas o GUID de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="5f809-120">In the previous code, the [**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md) method returns just the major type GUID.</span></span> <span data-ttu-id="5f809-121">Isso é conveniente se você não precisar examinar o tipo de mídia completo.</span><span class="sxs-lookup"><span data-stu-id="5f809-121">This is convenient if you do not need to examine the complete media type.</span></span> <span data-ttu-id="5f809-122">No entanto, para obter as dimensões de vídeo, é necessário examinar o bloco de formato para que o tipo de mídia completo seja necessário.</span><span class="sxs-lookup"><span data-stu-id="5f809-122">To get the video dimensions, however, it is necessary to examine the format block, so the full media type is needed.</span></span> <span data-ttu-id="5f809-123">Você pode recuperar isso chamando o método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) , que preenche uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5f809-123">You can retrieve that by calling the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method, which fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="5f809-124">O detector de mídia converte todos os fluxos de vídeo em formato descompactado, com um bloco de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="5f809-124">The Media Detector converts all video streams into uncompressed format, with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format block.</span></span>


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



<span data-ttu-id="5f809-125">O método [**Get \_ StreamMediaType**](imediadet-get-streammediatype.md) aloca o bloco de formato, que o chamador deve liberar.</span><span class="sxs-lookup"><span data-stu-id="5f809-125">The [**get\_StreamMediaType**](imediadet-get-streammediatype.md) method allocates the format block, which the caller must free.</span></span> <span data-ttu-id="5f809-126">Este exemplo usa a função [**FreeMediaType**](freemediatype.md) da biblioteca de classes base.</span><span class="sxs-lookup"><span data-stu-id="5f809-126">This example uses the [**FreeMediaType**](freemediatype.md) function from the base class library.</span></span>

<span data-ttu-id="5f809-127">Agora você está pronto para obter o quadro do pôster.</span><span class="sxs-lookup"><span data-stu-id="5f809-127">Now you are ready to get the poster frame.</span></span> <span data-ttu-id="5f809-128">Primeiro, chame o método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) com um ponteiro **nulo** para o buffer:</span><span class="sxs-lookup"><span data-stu-id="5f809-128">First call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method with a **NULL** pointer for the buffer:</span></span>


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



<span data-ttu-id="5f809-129">Essa chamada retorna o tamanho de buffer necessário no parâmetro *lSize* .</span><span class="sxs-lookup"><span data-stu-id="5f809-129">This call returns the required buffer size in the *lSize* parameter.</span></span> <span data-ttu-id="5f809-130">O primeiro parâmetro especifica o tempo de transmissão a ser buscado; Este exemplo usa o tempo zero.</span><span class="sxs-lookup"><span data-stu-id="5f809-130">The first parameter specifies the stream time to seek to; this example uses time zero.</span></span> <span data-ttu-id="5f809-131">Para a largura e a altura, este exemplo usa as dimensões de vídeo nativa obtidas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5f809-131">For the width and height, this example uses the native video dimensions obtained earlier.</span></span> <span data-ttu-id="5f809-132">Se você especificar outros valores, o detector de mídia irá alongar o bitmap para corresponder.</span><span class="sxs-lookup"><span data-stu-id="5f809-132">If you specify other values, the Media Detector will stretch the bitmap to match.</span></span>

<span data-ttu-id="5f809-133">Se o método for bem sucedido, aloque o buffer e chame [**GetBitmapBits**](imediadet-getbitmapbits.md) novamente:</span><span class="sxs-lookup"><span data-stu-id="5f809-133">If the method succeeds, allocate the buffer and call [**GetBitmapBits**](imediadet-getbitmapbits.md) again:</span></span>


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



<span data-ttu-id="5f809-134">Esta é a função completa, com tratamento de erros um pouco melhor.</span><span class="sxs-lookup"><span data-stu-id="5f809-134">Here is the complete function, with somewhat better error handling.</span></span>


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



<span data-ttu-id="5f809-135">Em seguida: [etapa 4: desenhar o bitmap na área do cliente](step-4--draw-the-bitmap-on-the-client-area.md)</span><span class="sxs-lookup"><span data-stu-id="5f809-135">Next: [Step 4: Draw the Bitmap on the Client Area](step-4--draw-the-bitmap-on-the-client-area.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f809-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f809-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f809-137">Capturando um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="5f809-137">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
