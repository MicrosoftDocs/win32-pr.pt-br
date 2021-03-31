---
description: Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em um filtro de decodificador do DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Suporte a DXVA 2,0 no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827533"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="9c362-103">Suporte a DXVA 2,0 no DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c362-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="9c362-104">Este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em um filtro de decodificador do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9c362-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="9c362-105">Especificamente, ele descreve a comunicação entre o decodificador e o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c362-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="9c362-106">Este tópico não descreve como implementar a decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="9c362-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9c362-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="9c362-108">Notas de migração</span><span class="sxs-lookup"><span data-stu-id="9c362-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="9c362-109">Encontrando uma configuração de decodificador</span><span class="sxs-lookup"><span data-stu-id="9c362-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="9c362-110">Notificando o renderizador de vídeo</span><span class="sxs-lookup"><span data-stu-id="9c362-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="9c362-111">Alocando buffers descompactados</span><span class="sxs-lookup"><span data-stu-id="9c362-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="9c362-112">Decodificação</span><span class="sxs-lookup"><span data-stu-id="9c362-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="9c362-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c362-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="9c362-114">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9c362-114">Prerequisites</span></span>

<span data-ttu-id="9c362-115">Este tópico pressupõe que você esteja familiarizado com a gravação de filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9c362-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="9c362-116">Para obter mais informações, consulte o tópico [escrevendo filtros do DirectShow](../directshow/writing-directshow-filters.md) na documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9c362-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="9c362-117">Os exemplos de código neste tópico pressupõem que o filtro de decodificador seja derivado da classe [**CTransformFilter**](../directshow/ctransformfilter.md) , com a seguinte definição de classe:</span><span class="sxs-lookup"><span data-stu-id="9c362-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="9c362-118">No restante deste tópico, o termo *decodificador* refere-se ao filtro do decodificador, que recebe vídeo compactado e gera vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="9c362-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="9c362-119">O termo *dispositivo decodificador* refere-se a um acelerador de vídeo de hardware implementado pelo driver de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9c362-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="9c362-120">Aqui estão as etapas básicas que um filtro de decodificador deve executar para dar suporte a DXVA 2,0:</span><span class="sxs-lookup"><span data-stu-id="9c362-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="9c362-121">Negocie um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9c362-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="9c362-122">Localize uma configuração de decodificador DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="9c362-123">Notifique o renderizador de vídeo que o decodificador está usando a decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="9c362-124">Forneça um alocador personalizado que aloque superfícies do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9c362-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="9c362-125">Essas etapas são descritas mais detalhadamente no restante deste tópico.</span><span class="sxs-lookup"><span data-stu-id="9c362-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="9c362-126">Notas de migração</span><span class="sxs-lookup"><span data-stu-id="9c362-126">Migration Notes</span></span>

<span data-ttu-id="9c362-127">Se estiver migrando do DXVA 1,0, você deve estar ciente de algumas diferenças significativas entre as duas versões:</span><span class="sxs-lookup"><span data-stu-id="9c362-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="9c362-128">O DXVA 2,0 não usa as interfaces [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) e [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , porque o decodificador pode acessar as APIs de DXVA 2,0 diretamente por meio da interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="9c362-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="9c362-129">Durante a negociação do tipo de mídia, o decodificador não usa um GUID de aceleração de vídeo como o subtipo.</span><span class="sxs-lookup"><span data-stu-id="9c362-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="9c362-130">Em vez disso, o subtipo é apenas o formato de vídeo descompactado (como NV12), assim como com a decodificação de software.</span><span class="sxs-lookup"><span data-stu-id="9c362-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="9c362-131">O procedimento para configurar o acelerador foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9c362-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="9c362-132">No DXVA 1,0, o decodificador chama **Execute** com uma estrutura de **\_ ConfigPictureDecode de DXVA** para configurar o accerlator.</span><span class="sxs-lookup"><span data-stu-id="9c362-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="9c362-133">No DXVA 2,0, o decodificador usa a interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , conforme descrito na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="9c362-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="9c362-134">O decodificador aloca os buffers descompactados.</span><span class="sxs-lookup"><span data-stu-id="9c362-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="9c362-135">O renderizador de vídeo não os aloca.</span><span class="sxs-lookup"><span data-stu-id="9c362-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="9c362-136">Em vez de chamar [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) para exibir o quadro decodificado, o decodificador entrega o quadro ao renderizador chamando [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), assim como com a decodificação de software.</span><span class="sxs-lookup"><span data-stu-id="9c362-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="9c362-137">O decodificador não é mais responsável por verificar quando os buffers de dados são seguros para atualizações.</span><span class="sxs-lookup"><span data-stu-id="9c362-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="9c362-138">Portanto, o DXVA 2,0 não tem nenhum método equivalente a [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span><span class="sxs-lookup"><span data-stu-id="9c362-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="9c362-139">A mesclagem de subimagem é feita pelo processador de vídeo, usando as APIs do processador de vídeo DXVA 2.0.</span><span class="sxs-lookup"><span data-stu-id="9c362-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="9c362-140">Os decodificadores que fornecem subfiguras (por exemplo, decodificadores de DVD) devem enviar dados de subimagem em um pino de saída separado.</span><span class="sxs-lookup"><span data-stu-id="9c362-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="9c362-141">Para operações de decodificação, o DXVA 2,0 usa as mesmas estruturas de dados que a DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="9c362-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="9c362-142">O filtro EVR (processador de vídeo avançado) dá suporte a DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="9c362-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="9c362-143">Os filtros de processador de mixagem de vídeo (VMR-7 e VMR-9) dão suporte apenas a DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="9c362-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="9c362-144">Encontrando uma configuração de decodificador</span><span class="sxs-lookup"><span data-stu-id="9c362-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="9c362-145">Depois que o decodificador negociar o tipo de mídia de saída, ele deverá encontrar uma configuração compatível para o dispositivo de decodificador DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="9c362-146">Você pode executar essa etapa dentro do método [**CBaseOutputPin:: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="9c362-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="9c362-147">Essa etapa garante que o driver de gráficos dê suporte aos recursos necessários para o decodificador, antes que o decodificador confirme o uso de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="9c362-148">Para localizar uma configuração para o dispositivo decodificador, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9c362-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="9c362-149">Consulte o PIN de entrada do renderizador para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="9c362-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="9c362-150">Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="9c362-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="9c362-151">O GUID do serviço é \_ o \_ serviço de aceleração de vídeo Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="9c362-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="9c362-152">Chame [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obter um identificador para o dispositivo Direct3D do renderizador.</span><span class="sxs-lookup"><span data-stu-id="9c362-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="9c362-153">Chame [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passe o identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c362-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="9c362-154">Esse método retorna um ponteiro para a interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="9c362-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="9c362-155">Chame [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span><span class="sxs-lookup"><span data-stu-id="9c362-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="9c362-156">Esse método retorna uma matriz de GUIDs de dispositivo do decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="9c362-157">Faça um loop através da matriz de GUIDs do decodificador para localizar os que o filtro de decodificador suporta.</span><span class="sxs-lookup"><span data-stu-id="9c362-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="9c362-158">Por exemplo, para um decodificador MPEG-2, você procurará **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou **DXVA2 \_ ModeMPEG2 \_** VLD.</span><span class="sxs-lookup"><span data-stu-id="9c362-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="9c362-159">Quando você encontrar um GUID de dispositivo de decodificador candidato, passe o GUID para o método [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) .</span><span class="sxs-lookup"><span data-stu-id="9c362-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="9c362-160">Esse método retorna uma matriz de formatos de destino de renderização, especificados como valores de **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="9c362-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="9c362-161">Faça um loop pelos formatos de destino de renderização e procure um que corresponda ao formato de saída.</span><span class="sxs-lookup"><span data-stu-id="9c362-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="9c362-162">Normalmente, um dispositivo decodificador dá suporte a um único formato de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9c362-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="9c362-163">O filtro do decodificador deve se conectar ao renderizador usando esse subtipo.</span><span class="sxs-lookup"><span data-stu-id="9c362-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="9c362-164">Na primeira chamada para [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), o decodificador pode destermos o formato de destino de renderização e, em seguida, retornar esse formato como um tipo de saída preferencial.</span><span class="sxs-lookup"><span data-stu-id="9c362-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="9c362-165">Chame [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span><span class="sxs-lookup"><span data-stu-id="9c362-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="9c362-166">Passe o mesmo GUID do dispositivo decodificador, junto com uma estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que descreve o formato proposto.</span><span class="sxs-lookup"><span data-stu-id="9c362-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="9c362-167">O método retorna uma matriz de estruturas [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) .</span><span class="sxs-lookup"><span data-stu-id="9c362-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="9c362-168">Cada estrutura descreve uma configuração possível para o dispositivo decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="9c362-169">Supondo que as etapas anteriores sejam bem-sucedidas, armazene o identificador do dispositivo Direct3D, o GUID do dispositivo do decodificador e a estrutura de configuração.</span><span class="sxs-lookup"><span data-stu-id="9c362-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="9c362-170">O filtro usará essas informações para criar o dispositivo decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="9c362-171">O código a seguir mostra como localizar uma configuração de decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="9c362-172">Como esse exemplo é genérico, parte da lógica foi colocada em funções auxiliares que precisariam ser implementadas pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="9c362-173">O código a seguir mostra as declarações para essas funções:</span><span class="sxs-lookup"><span data-stu-id="9c362-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="9c362-174">Notificando o renderizador de vídeo</span><span class="sxs-lookup"><span data-stu-id="9c362-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="9c362-175">Se o decodificador encontrar uma configuração de decodificador, a próxima etapa será notificar o renderizador de vídeo de que o decodificador usará aceleração de hardware.</span><span class="sxs-lookup"><span data-stu-id="9c362-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="9c362-176">Você pode executar essa etapa dentro do método [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="9c362-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="9c362-177">Esta etapa deve ocorrer antes da seleção do alocador, pois afeta como o alocador é selecionado.</span><span class="sxs-lookup"><span data-stu-id="9c362-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="9c362-178">Consulte o PIN de entrada do renderizador para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="9c362-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="9c362-179">Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="9c362-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="9c362-180">O GUID do serviço é o **\_ \_ \_ serviço de aceleração de vídeo Mr**.</span><span class="sxs-lookup"><span data-stu-id="9c362-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="9c362-181">Chame [**IDirectXVideoMemoryConfiguration:: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) em um loop, incrementando a variável *dwTypeIndex* de zero.</span><span class="sxs-lookup"><span data-stu-id="9c362-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="9c362-182">Pare quando o método retornar o valor **DXVA2 \_ surfacetype \_ DecoderRenderTarget** no parâmetro *pdwType* .</span><span class="sxs-lookup"><span data-stu-id="9c362-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="9c362-183">Essa etapa garante que o processador de vídeo dê suporte à decodificação acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="9c362-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="9c362-184">Esta etapa sempre terá sucesso para o filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="9c362-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="9c362-185">Se a etapa anterior tiver sido bem-sucedida, chame [**IDirectXVideoMemoryConfiguration:: Setsurfacetype**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) com o valor DXVA2 \_ surfacetype \_ DecoderRenderTarget.</span><span class="sxs-lookup"><span data-stu-id="9c362-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="9c362-186">Chamar **Setsurfacetype** com esse valor coloca o processador de vídeo no modo DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="9c362-187">Quando o processador de vídeo está nesse modo, o decodificador deve fornecer seu próprio alocador.</span><span class="sxs-lookup"><span data-stu-id="9c362-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="9c362-188">O código a seguir mostra como notificar o renderizador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c362-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="9c362-189">Se o decodificador encontrar uma configuração válida e notificar com êxito o processador de vídeo, o decodificador poderá usar o DXVA para decodificação.</span><span class="sxs-lookup"><span data-stu-id="9c362-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="9c362-190">O decodificador deve implementar um alocador personalizado para seu pino de saída, conforme descrito na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="9c362-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="9c362-191">Alocando buffers descompactados</span><span class="sxs-lookup"><span data-stu-id="9c362-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="9c362-192">No DXVA 2,0, o decodificador é responsável por alocar superfícies do Direct3D para usar como buffers de vídeo não compactados.</span><span class="sxs-lookup"><span data-stu-id="9c362-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="9c362-193">Portanto, o decodificador deve implementar um alocador personalizado que criará as superfícies.</span><span class="sxs-lookup"><span data-stu-id="9c362-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="9c362-194">Os exemplos de mídia fornecidos por esse alocador manterão ponteiros para as superfícies do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9c362-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="9c362-195">O EVR recupera um ponteiro para a superfície chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9c362-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="9c362-196">O identificador de serviço é o **\_ \_ serviço de buffer do Mr**.</span><span class="sxs-lookup"><span data-stu-id="9c362-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="9c362-197">Para fornecer o alocador personalizado, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="9c362-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="9c362-198">Defina uma classe para os exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="9c362-198">Define a class for the media samples.</span></span> <span data-ttu-id="9c362-199">Essa classe pode derivar da classe [**CMediaSample**](../directshow/cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="9c362-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="9c362-200">Dentro dessa classe, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9c362-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="9c362-201">Armazene um ponteiro para a superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9c362-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="9c362-202">Implemente a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="9c362-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="9c362-203">No método [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , se o GUID do serviço for **o \_ \_ serviço de buffer do Mr**, consulte a superfície do Direct3D para obter a interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="9c362-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="9c362-204">Caso contrário, o **GetService** pode retornar o **\_ serviço MF E \_ sem suporte \_**.</span><span class="sxs-lookup"><span data-stu-id="9c362-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="9c362-205">Substitua o método [**CMediaSample:: Getapontarr**](../directshow/cmediasample-getpointer.md) para retornar E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9c362-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="9c362-206">Defina uma classe para o alocador.</span><span class="sxs-lookup"><span data-stu-id="9c362-206">Define a class for the allocator.</span></span> <span data-ttu-id="9c362-207">O alocador pode derivar da classe [**CBaseAllocator**](../directshow/cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="9c362-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="9c362-208">Dentro dessa classe, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9c362-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="9c362-209">Substitua o método [**CBaseAllocator:: Alloc**](../directshow/cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="9c362-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="9c362-210">Dentro desse método, chame [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) para criar as superfícies.</span><span class="sxs-lookup"><span data-stu-id="9c362-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="9c362-211">(A interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) herda esse método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span><span class="sxs-lookup"><span data-stu-id="9c362-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="9c362-212">Substitua o método [**CBaseAllocator:: Free**](../directshow/cbaseallocator-free.md) para liberar as superfícies.</span><span class="sxs-lookup"><span data-stu-id="9c362-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="9c362-213">No PIN de saída do filtro, substitua o método [**CBaseOutputPin:: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="9c362-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="9c362-214">Dentro desse método, crie uma instância do seu alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="9c362-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="9c362-215">No filtro, implemente o método [**CTransformFilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="9c362-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="9c362-216">O parâmetro *pProperties* indica o número de superfícies que o EVR exige.</span><span class="sxs-lookup"><span data-stu-id="9c362-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="9c362-217">Adicione a esse valor o número de superfícies exigidas pelo decodificador e chame [**IMemAllocator:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) no alocador.</span><span class="sxs-lookup"><span data-stu-id="9c362-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="9c362-218">O código a seguir mostra como implementar a classe de exemplo de mídia:</span><span class="sxs-lookup"><span data-stu-id="9c362-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="9c362-219">O código a seguir mostra como implementar o método [**Alloc**](../directshow/cbaseallocator-alloc.md) no alocador.</span><span class="sxs-lookup"><span data-stu-id="9c362-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="9c362-220">Este é o código para o método [**gratuito**](../directshow/cbaseallocator-free.md) :</span><span class="sxs-lookup"><span data-stu-id="9c362-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="9c362-221">Para obter mais informações sobre como implementar os alocadores personalizados, consulte o tópico [fornecendo um alocador personalizado](../directshow/providing-a-custom-allocator.md) na documentação do SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9c362-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="9c362-222">Decodificação</span><span class="sxs-lookup"><span data-stu-id="9c362-222">Decoding</span></span>

<span data-ttu-id="9c362-223">Para criar o dispositivo decodificador, chame [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span><span class="sxs-lookup"><span data-stu-id="9c362-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="9c362-224">O método retorna um ponteiro para a interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) do dispositivo decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="9c362-225">Em cada quadro, chame [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para testar o identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c362-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="9c362-226">Se o dispositivo tiver sido alterado, o método retornará DXVA2 \_ E \_ novo dispositivo de \_ vídeo \_ .</span><span class="sxs-lookup"><span data-stu-id="9c362-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="9c362-227">Se isso ocorrer, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9c362-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="9c362-228">Feche o identificador do dispositivo chamando [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span><span class="sxs-lookup"><span data-stu-id="9c362-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="9c362-229">Libere os ponteiros [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="9c362-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="9c362-230">Abra um novo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c362-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="9c362-231">Negocie uma nova configuração de decodificador, conforme descrito na seção [encontrando uma configuração de decodificador](#finding-a-decoder-configuration).</span><span class="sxs-lookup"><span data-stu-id="9c362-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="9c362-232">Crie um novo dispositivo de decodificador.</span><span class="sxs-lookup"><span data-stu-id="9c362-232">Create a new decoder device.</span></span>

<span data-ttu-id="9c362-233">Supondo que o identificador do dispositivo seja válido, o processo de decodificação funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9c362-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="9c362-234">Chame [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span><span class="sxs-lookup"><span data-stu-id="9c362-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="9c362-235">Faça o seguinte uma ou mais vezes:</span><span class="sxs-lookup"><span data-stu-id="9c362-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="9c362-236">Chame [**IDirectXVideoDecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obter um buffer de decodificador de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="9c362-237">Preencha o buffer.</span><span class="sxs-lookup"><span data-stu-id="9c362-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="9c362-238">Chame [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span><span class="sxs-lookup"><span data-stu-id="9c362-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="9c362-239">Chame [**IDirectXVideoDecoder:: execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para executar as operações de decodificação no quadro.</span><span class="sxs-lookup"><span data-stu-id="9c362-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="9c362-240">O DXVA 2,0 usa as mesmas estruturas de dados que a DXVA 1,0 para operações de decodificação.</span><span class="sxs-lookup"><span data-stu-id="9c362-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="9c362-241">Para o conjunto original de perfis de DXVA (para H. 261, H. 263 e MPEG-2), essas estruturas de dados são descritas na [especificação DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="9c362-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="9c362-242">Em cada par de [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / chamadas de [**execução**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) BeginFrame, você pode chamar [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) várias vezes, mas apenas uma vez para cada tipo de buffer de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9c362-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="9c362-243">Se você chamá-lo duas vezes com o mesmo tipo de buffer, os dados serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="9c362-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="9c362-244">Depois de chamar [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), chame [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) para entregar o quadro ao processador de vídeo, assim como com a decodificação de software.</span><span class="sxs-lookup"><span data-stu-id="9c362-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="9c362-245">O método **Receive** é assíncrono; Depois de retornar, o decodificador pode continuar decodificando o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="9c362-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="9c362-246">O driver de vídeo impede que qualquer comando de decodificação substitua o buffer enquanto o buffer está em uso.</span><span class="sxs-lookup"><span data-stu-id="9c362-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="9c362-247">O decodificador não deve reutilizar uma superfície para decodificar outro quadro até que o renderizador tenha liberado o exemplo.</span><span class="sxs-lookup"><span data-stu-id="9c362-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="9c362-248">Quando o renderizador libera o exemplo, o alocador coloca o exemplo de volta em seu pool de exemplos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9c362-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="9c362-249">Para obter o próximo exemplo disponível, chame [**CBaseOutputPin:: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), que por sua vez chama [**IMemAllocator:: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="9c362-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="9c362-250">Para obter mais informações, consulte o tópico [visão geral do fluxo de dados no DirectShow](../directshow/overview-of-data-flow-in-directshow.md) na documentação do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9c362-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c362-251">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c362-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c362-252">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="9c362-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
