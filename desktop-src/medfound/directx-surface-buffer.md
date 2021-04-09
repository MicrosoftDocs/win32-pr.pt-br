---
description: Buffer de superfície DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Buffer de superfície DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089748"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="05458-103">Buffer de superfície DirectX</span><span class="sxs-lookup"><span data-stu-id="05458-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="05458-104">O objeto de buffer da superfície DirectX é um buffer de mídia que gerencia uma superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="05458-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="05458-105">Para criar uma instância desse objeto, chame [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) e passe um ponteiro para a superfície DirectX.</span><span class="sxs-lookup"><span data-stu-id="05458-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="05458-106">O buffer de superfície do DirectX expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="05458-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="05458-107">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="05458-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="05458-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="05458-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="05458-109">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="05458-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="05458-110">Há várias maneiras de acessar a memória da superfície do objeto de buffer:</span><span class="sxs-lookup"><span data-stu-id="05458-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="05458-111">Recomendado: chamar [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no buffer.</span><span class="sxs-lookup"><span data-stu-id="05458-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="05458-112">Use o **\_ \_ serviço de buffer** do identificador de serviço Mr.</span><span class="sxs-lookup"><span data-stu-id="05458-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="05458-113">O método retorna um ponteiro para a superfície do Direct3D subjacente.</span><span class="sxs-lookup"><span data-stu-id="05458-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="05458-114">Chame [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span><span class="sxs-lookup"><span data-stu-id="05458-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="05458-115">Esse método chama **IDirect3DSurface9:: LockRect** diretamente na superfície.</span><span class="sxs-lookup"><span data-stu-id="05458-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="05458-116">O método [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) chama **UnlockRect** na superfície.</span><span class="sxs-lookup"><span data-stu-id="05458-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="05458-117">Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="05458-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="05458-118">Em geral, isso não é recomendado, pois força o objeto a copiar a memória da superfície do Direct3D e, em seguida, voltar a usar.</span><span class="sxs-lookup"><span data-stu-id="05458-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="05458-119">O método [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="05458-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="05458-120">[**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) e [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) podem falhar se a superfície subjacente não for bloqueáveis.</span><span class="sxs-lookup"><span data-stu-id="05458-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="05458-121">O buffer de superfície do DirectX implementa esses dois métodos principalmente para componentes que não são projetados para funcionar com superfícies do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="05458-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="05458-122">O processador de vídeo avançado (EVR) cria buffers de superfície do DirectX quando o decodificador não está configurado para a DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="05458-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="05458-123">Para obter mais informações, consulte [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span><span class="sxs-lookup"><span data-stu-id="05458-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="05458-124">Obtendo a superfície do Direct3D</span><span class="sxs-lookup"><span data-stu-id="05458-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="05458-125">Para obter uma superfície do Direct3D de um exemplo de vídeo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="05458-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="05458-126">Chame [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) com um valor de índice igual a zero.</span><span class="sxs-lookup"><span data-stu-id="05458-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="05458-127">Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e especifique o identificador do serviço de **\_ \_ buffer do Mr** .</span><span class="sxs-lookup"><span data-stu-id="05458-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="05458-128">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="05458-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="05458-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05458-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05458-130">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="05458-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="05458-131">Exemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="05458-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



