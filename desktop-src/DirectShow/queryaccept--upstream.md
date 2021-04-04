---
description: QueryAccept (upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646048"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="a7d76-103">QueryAccept (upstream)</span><span class="sxs-lookup"><span data-stu-id="a7d76-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="a7d76-104">Esse mecanismo permite que um PIN de entrada proponha uma alteração de formato ao seu ponto de upstream.</span><span class="sxs-lookup"><span data-stu-id="a7d76-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="a7d76-105">O filtro downstream deve anexar um tipo de mídia ao exemplo que o filtro upstream obterá em sua próxima chamada para [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="a7d76-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="a7d76-106">No entanto, para fazer isso, o filtro downstream deve fornecer um alocador personalizado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a7d76-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="a7d76-107">Esse alocador deve implementar um método privado que o filtro downstream possa usar para definir o tipo de mídia no próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="a7d76-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="a7d76-108">Ocorrem as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a7d76-108">The following steps occur:</span></span>

1.  <span data-ttu-id="a7d76-109">O filtro downstream verifica se a conexão do PIN usa o alocador personalizado do filtro.</span><span class="sxs-lookup"><span data-stu-id="a7d76-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="a7d76-110">Se o filtro upstream possuir o alocador, o filtro downstream não poderá alterar o formato.</span><span class="sxs-lookup"><span data-stu-id="a7d76-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="a7d76-111">O filtro downstream chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída upstream (veja A ilustração, etapa A).</span><span class="sxs-lookup"><span data-stu-id="a7d76-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="a7d76-112">Se `QueryAccept` o retornar S \_ OK, o filtro downstream chamará o método particular em seu alocador para definir o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a7d76-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="a7d76-113">Dentro desse método particular, o alocador chama [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) no próximo exemplo disponível (B).</span><span class="sxs-lookup"><span data-stu-id="a7d76-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="a7d76-114">O filtro upstream chama **GetBuffer** para obter um novo exemplo (C) e [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para obter o tipo de mídia (D).</span><span class="sxs-lookup"><span data-stu-id="a7d76-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="a7d76-115">Quando o filtro upstream entrega o exemplo, ele deve deixar o tipo de mídia anexado a esse exemplo.</span><span class="sxs-lookup"><span data-stu-id="a7d76-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="a7d76-116">Dessa forma, o filtro downstream pode confirmar que o tipo de mídia foi alterado (E).</span><span class="sxs-lookup"><span data-stu-id="a7d76-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="a7d76-117">Se o filtro upstream aceitar a alteração de formato, ele também deverá ser capaz de voltar para o tipo de mídia original, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7d76-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![QueryAccept (upstream)](images/dynformat4.png)

<span data-ttu-id="a7d76-119">Os principais exemplos desse tipo de alteração de formato envolvem os processadores de vídeo do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a7d76-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="a7d76-120">O filtro de [processamento de vídeo](video-renderer-filter.md) original pode alternar entre os tipos RGB e YUV durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="a7d76-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="a7d76-121">Quando o filtro se conecta, ele requer um formato RGB que corresponda às configurações de exibição atuais.</span><span class="sxs-lookup"><span data-stu-id="a7d76-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="a7d76-122">Isso garante que ele possa fazer fallback no GDI se precisar.</span><span class="sxs-lookup"><span data-stu-id="a7d76-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="a7d76-123">Após o streaming começar, se o DirectDraw estiver disponível, o processador de vídeo solicitará uma alteração de formato para um tipo YUV.</span><span class="sxs-lookup"><span data-stu-id="a7d76-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="a7d76-124">Posteriormente, ele poderá voltar para RGB se perder a superfície do DirectDraw por qualquer motivo.</span><span class="sxs-lookup"><span data-stu-id="a7d76-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="a7d76-125">O filtro de processador de mixagem de vídeo (VMR) mais recente se conectará a qualquer formato com suporte pelo hardware de gráficos, incluindo tipos YUV.</span><span class="sxs-lookup"><span data-stu-id="a7d76-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="a7d76-126">No entanto, o hardware de gráficos pode alterar o stride da superfície do DirectDraw subjacente para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a7d76-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="a7d76-127">O filtro VMR usa `QueryAccept` para relatar o novo Stride, que é especificado no membro de **bilargura** da estrutura **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="a7d76-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="a7d76-128">Os retângulos de origem e de destino na estrutura **VIDEOINFOHEADER** ou **VIDEOINFOHEADER2** identificam a região onde o vídeo deve ser decodificado.</span><span class="sxs-lookup"><span data-stu-id="a7d76-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="a7d76-129">**Observação de implementação**</span><span class="sxs-lookup"><span data-stu-id="a7d76-129">**Implementation Note**</span></span>

<span data-ttu-id="a7d76-130">É improvável que você escreva um filtro que precisa solicitar alterações no formato upstream, pois isso é principalmente um recurso de renderizadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a7d76-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="a7d76-131">No entanto, se você escrever um filtro de transformação de vídeo ou um decodificador de vídeo, o filtro deverá responder corretamente a solicitações do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a7d76-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="a7d76-132">Um filtro de trans-in-Place que fica entre o processador de vídeo e o decodificador deve passar todas as `QueryAccept` chamadas upstream.</span><span class="sxs-lookup"><span data-stu-id="a7d76-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="a7d76-133">Armazene as novas informações de formato quando ele chegar.</span><span class="sxs-lookup"><span data-stu-id="a7d76-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="a7d76-134">Um filtro de cópia/transformação (ou seja, um filtro não trans-in-Place) deve implementar um dos seguintes comportamentos:</span><span class="sxs-lookup"><span data-stu-id="a7d76-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="a7d76-135">O formato aprovado muda de fluxo e armazena as novas informações de formato quando ele chega.</span><span class="sxs-lookup"><span data-stu-id="a7d76-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="a7d76-136">O filtro deve usar um alocador personalizado para que ele possa anexar o formato ao exemplo de upstream.</span><span class="sxs-lookup"><span data-stu-id="a7d76-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="a7d76-137">Execute a conversão de formato dentro do filtro.</span><span class="sxs-lookup"><span data-stu-id="a7d76-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="a7d76-138">Isso é provavelmente mais fácil do que passar a alteração de formato upstream.</span><span class="sxs-lookup"><span data-stu-id="a7d76-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="a7d76-139">No entanto, pode ser menos eficiente do que permitir que o filtro do decodificador decodifique o formato correto.</span><span class="sxs-lookup"><span data-stu-id="a7d76-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="a7d76-140">Como último recurso, basta rejeitar a alteração do formato.</span><span class="sxs-lookup"><span data-stu-id="a7d76-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="a7d76-141">(Para obter mais informações, consulte o código-fonte para o método [**CTransInPlaceOutputPin:: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) na biblioteca de classes base do DirectShow.) A rejeição de uma alteração de formato pode reduzir o desempenho, no entanto, porque impede que o renderizador de vídeo Use o formato mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="a7d76-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="a7d76-142">O pseudocódigo a seguir mostra como você pode implementar um filtro de cópia/transformação (derivado de **CTransformFilter**) que pode alternar entre os tipos de saída YUV e RGB.</span><span class="sxs-lookup"><span data-stu-id="a7d76-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="a7d76-143">Este exemplo pressupõe que o filtro faz a conversão em si, em vez de passar a alteração de formato upstream.</span><span class="sxs-lookup"><span data-stu-id="a7d76-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



