---
description: Buffers de vídeo descompactados
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Buffers de vídeo descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772898"
---
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="2f374-103">Buffers de vídeo descompactados</span><span class="sxs-lookup"><span data-stu-id="2f374-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="2f374-104">Este artigo descreve como trabalhar com buffers de mídia que contêm quadros de vídeo descompactados.</span><span class="sxs-lookup"><span data-stu-id="2f374-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="2f374-105">Em ordem de preferência, as opções a seguir estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2f374-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="2f374-106">Nem todo buffer de mídia dá suporte a cada opção.</span><span class="sxs-lookup"><span data-stu-id="2f374-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="2f374-107">Use a superfície do Direct3D subjacente.</span><span class="sxs-lookup"><span data-stu-id="2f374-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="2f374-108">(Aplica-se somente a quadros de vídeo armazenados em superfícies do Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="2f374-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="2f374-109">Use a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="2f374-110">Use a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="2f374-111">Usar a superfície do Direct3D subjacente</span><span class="sxs-lookup"><span data-stu-id="2f374-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="2f374-112">O quadro de vídeo pode ser armazenado dentro de uma superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2f374-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="2f374-113">Nesse caso, você pode obter um ponteiro para a superfície chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ou [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) no objeto de buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f374-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="2f374-114">Use o serviço de buffer do identificador de serviço MR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2f374-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="2f374-115">Essa abordagem é recomendada quando o componente que acessa o quadro de vídeo é projetado para usar o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2f374-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="2f374-116">Por exemplo, um decodificador de vídeo que dá suporte à aceleração de vídeo do DirectX deve usar essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="2f374-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="2f374-117">O código a seguir mostra como obter o ponteiro **IDirect3DSurface9** de um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f374-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



<span data-ttu-id="2f374-118">Os seguintes objetos oferecem suporte ao serviço de **\_ \_ buffer do Mr** :</span><span class="sxs-lookup"><span data-stu-id="2f374-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="2f374-119">Buffer de superfície DirectX</span><span class="sxs-lookup"><span data-stu-id="2f374-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="2f374-120">Exemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="2f374-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="2f374-121">Usar a interface IMF2DBuffer</span><span class="sxs-lookup"><span data-stu-id="2f374-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="2f374-122">Se o quadro de vídeo não estiver armazenado dentro de uma superfície do Direct3D ou se o componente não for projetado para usar o Direct3D, a próxima maneira recomendada para acessar o quadro de vídeo é consultar o buffer para a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="2f374-123">Essa interface é projetada especificamente para dados de imagem.</span><span class="sxs-lookup"><span data-stu-id="2f374-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="2f374-124">Para obter um ponteiro para essa interface, chame **QueryInterface** no buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f374-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="2f374-125">Nem todos os objetos de buffer de mídia expõem essa interface.</span><span class="sxs-lookup"><span data-stu-id="2f374-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="2f374-126">Mas se um buffer de mídia expor a interface **IMF2DBuffer** , você deverá usar essa interface para acessar os dados, se possível, em vez de usar [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span><span class="sxs-lookup"><span data-stu-id="2f374-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="2f374-127">Você ainda pode usar a interface **IMFMediaBuffer** , mas pode ser menos eficiente.</span><span class="sxs-lookup"><span data-stu-id="2f374-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="2f374-128">Chame **QueryInterface** no buffer de mídia para obter a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="2f374-129">Chame [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para acessar a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="2f374-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="2f374-130">Esse método retorna um ponteiro para o primeiro byte da linha superior de pixels.</span><span class="sxs-lookup"><span data-stu-id="2f374-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="2f374-131">Ele também retorna o stride da imagem, que é o número de bytes desde o início de uma linha de pixels até o início da próxima linha.</span><span class="sxs-lookup"><span data-stu-id="2f374-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="2f374-132">O buffer pode conter bytes de preenchimento após cada linha de pixels, portanto, o stride pode ser mais largo do que a largura da imagem em bytes.</span><span class="sxs-lookup"><span data-stu-id="2f374-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="2f374-133">O stride também pode ser negativo se a imagem for orientada de baixo para cima na memória.</span><span class="sxs-lookup"><span data-stu-id="2f374-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="2f374-134">Para obter mais informações, consulte [Stride de imagem](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="2f374-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="2f374-135">Mantenha o buffer bloqueado somente enquanto você precisa acessar a memória.</span><span class="sxs-lookup"><span data-stu-id="2f374-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="2f374-136">Desbloqueie o buffer chamando [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span><span class="sxs-lookup"><span data-stu-id="2f374-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="2f374-137">Nem todo buffer de mídia implementa a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="2f374-138">Se o buffer de mídia não implementar essa interface (ou seja, o objeto de buffer retornará E \_ nointerface na etapa 1), você deverá usar a interface de interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , descrita a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f374-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="2f374-139">Usar a interface IMFMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="2f374-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="2f374-140">Se um buffer de mídia não expor a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="2f374-141">A semântica geral dessa interface é descrita no tópico [trabalhando com buffers de mídia](working-with-media-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="2f374-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="2f374-142">Chame **QueryInterface** no buffer de mídia para obter a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="2f374-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="2f374-143">Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para acessar a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="2f374-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="2f374-144">Esse método retorna um ponteiro para a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="2f374-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="2f374-145">Quando o método **Lock** é usado, o stride é sempre o stride mínimo para o formato de vídeo em questão, sem nenhum byte de preenchimento extra.</span><span class="sxs-lookup"><span data-stu-id="2f374-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="2f374-146">Mantenha o buffer bloqueado somente enquanto você precisa acessar a memória.</span><span class="sxs-lookup"><span data-stu-id="2f374-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="2f374-147">Desbloqueie o buffer chamando [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="2f374-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="2f374-148">Você sempre deve evitar chamar [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) se o buffer expõe [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), pois o método **Lock** pode forçar o objeto buffer para o quadro de vídeo em um bloco de memória contíguo e, em seguida, voltar novamente.</span><span class="sxs-lookup"><span data-stu-id="2f374-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="2f374-149">Por outro lado, se o buffer não oferecer suporte a **IMF2DBuffer**, então **IMFMediaBuffer:: Lock** provavelmente não resultará em uma cópia.</span><span class="sxs-lookup"><span data-stu-id="2f374-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="2f374-150">Calcule o stride mínimo do tipo de mídia da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2f374-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="2f374-151">O stride mínimo pode ser armazenado no atributo [**\_ Stride do \_ padrão \_ MF MT**](mf-mt-default-stride-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2f374-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="2f374-152">Se o **atributo \_ \_ \_ Stride do padrão MF MT** não estiver definido, chame a função [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) para calcular o stride para os formatos de vídeo mais comuns.</span><span class="sxs-lookup"><span data-stu-id="2f374-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="2f374-153">Se a função [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) não reconhecer o formato, você deverá calcular o stride com base na definição do formato.</span><span class="sxs-lookup"><span data-stu-id="2f374-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="2f374-154">Nesse caso, não há nenhuma regra geral; Você precisa saber os detalhes da definição de formato.</span><span class="sxs-lookup"><span data-stu-id="2f374-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="2f374-155">O código a seguir mostra como obter o stride padrão para os formatos de vídeo mais comuns.</span><span class="sxs-lookup"><span data-stu-id="2f374-155">The following code shows how to get the default stride for the most common video formats.</span></span>


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



<span data-ttu-id="2f374-156">Dependendo do seu aplicativo, você pode saber com antecedência se um determinado buffer de mídia dá suporte a [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (por exemplo, se você criou o buffer).</span><span class="sxs-lookup"><span data-stu-id="2f374-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="2f374-157">Caso contrário, você deve estar preparado para usar qualquer uma das duas interfaces de buffer.</span><span class="sxs-lookup"><span data-stu-id="2f374-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="2f374-158">O exemplo a seguir mostra uma classe auxiliar que oculta alguns desses detalhes.</span><span class="sxs-lookup"><span data-stu-id="2f374-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="2f374-159">Essa classe tem um método LockBuffer que chama [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) ou [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) e retorna um ponteiro para o início da primeira linha de pixels.</span><span class="sxs-lookup"><span data-stu-id="2f374-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="2f374-160">(Esse comportamento corresponde ao método **Lock2D** .) O método LockBuffer usa o stride padrão como um parâmetro de entrada e retorna a Stride real como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="2f374-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a><span data-ttu-id="2f374-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f374-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f374-162">Stride da imagem</span><span class="sxs-lookup"><span data-stu-id="2f374-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="2f374-163">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="2f374-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



