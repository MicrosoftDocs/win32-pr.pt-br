---
description: O filtro EVR (processador de vídeo avançado) é um processador e mixer de vídeo de 16 canais. Ele tem a mesma funcionalidade básica e modelo de plug-in que o coletor de mídia Media Foundation EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro de processador de vídeo aprimorado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009974"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="d6f29-104">Filtro de processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="d6f29-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="d6f29-105">Este tópico aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="d6f29-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="d6f29-106">O filtro EVR (processador de vídeo avançado) é um processador e mixer de vídeo de 16 canais.</span><span class="sxs-lookup"><span data-stu-id="d6f29-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="d6f29-107">Ele tem a mesma funcionalidade básica e modelo de plug-in que o coletor de mídia Media Foundation EVR.</span><span class="sxs-lookup"><span data-stu-id="d6f29-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="d6f29-108">O filtro EVR do DirectShow está documentado na documentação do SDK do Media Foundation; para obter mais informações, consulte [processador de vídeo aprimorado](../medfound/enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="d6f29-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6f29-109">Filtrar interfaces (por meio de <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="d6f29-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="d6f29-110">Interfaces do DirectShow:</span><span class="sxs-lookup"><span data-stu-id="d6f29-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="d6f29-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="d6f29-119">Interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="d6f29-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="d6f29-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f29-124">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="d6f29-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="d6f29-125">, Dependendo do driver de gráficos.</span><span class="sxs-lookup"><span data-stu-id="d6f29-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6f29-126">Interfaces de pino de entrada (por meio de <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="d6f29-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="d6f29-127">Interfaces do DirectShow:</span><span class="sxs-lookup"><span data-stu-id="d6f29-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="d6f29-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="d6f29-131">Interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="d6f29-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="d6f29-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="d6f29-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6f29-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f29-135">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="d6f29-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="d6f29-136">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d6f29-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6f29-137">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="d6f29-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="d6f29-138">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d6f29-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f29-139">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="d6f29-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="d6f29-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="d6f29-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6f29-141">Executável</span><span class="sxs-lookup"><span data-stu-id="d6f29-141">Executable</span></span></td>
<td><span data-ttu-id="d6f29-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="d6f29-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f29-143"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="d6f29-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="d6f29-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="d6f29-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6f29-145"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="d6f29-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="d6f29-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="d6f29-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d6f29-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6f29-147">Remarks</span></span>

<span data-ttu-id="d6f29-148">Além das interfaces expostas por meio de **QueryInterface**, o EVR expõe outras interfaces por meio do método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="d6f29-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="d6f29-149">Algumas dessas interfaces são implementadas pelo apresentador EVR ou o mixer EVR, em vez do EVR em si.</span><span class="sxs-lookup"><span data-stu-id="d6f29-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="d6f29-150">Se o aplicativo definir um apresentador ou mixer personalizado no EVR, as versões personalizadas poderão expor um conjunto diferente de interfaces.</span><span class="sxs-lookup"><span data-stu-id="d6f29-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="d6f29-151">Objeto</span><span class="sxs-lookup"><span data-stu-id="d6f29-151">Object</span></span>     | <span data-ttu-id="d6f29-152">Identificador de serviço</span><span class="sxs-lookup"><span data-stu-id="d6f29-152">Service Identifier</span></span>                                              | <span data-ttu-id="d6f29-153">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d6f29-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f29-154">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="d6f29-154">EVR filter</span></span> | <span data-ttu-id="d6f29-155">\_ \_ \_ Serviço de RENDERIZAÇÃO de vídeo Mr (consultas EVR ou Presenter)</span><span class="sxs-lookup"><span data-stu-id="d6f29-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="d6f29-156">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d6f29-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="d6f29-157">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="d6f29-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="d6f29-158">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="d6f29-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="d6f29-159">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="d6f29-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="d6f29-160">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="d6f29-160">EVR filter</span></span> | <span data-ttu-id="d6f29-161">\_ \_ \_ Serviço de aceleração de vídeo do Mr (apresentador de consultas)</span><span class="sxs-lookup"><span data-stu-id="d6f29-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="d6f29-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="d6f29-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d6f29-163">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="d6f29-163">EVR filter</span></span> | <span data-ttu-id="d6f29-164">\_ \_ \_ Serviço de mixer de vídeo Mr (mixer de consultas)</span><span class="sxs-lookup"><span data-stu-id="d6f29-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="d6f29-165">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d6f29-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="d6f29-166">**IMFVideoMixerBitmap**</span><span class="sxs-lookup"><span data-stu-id="d6f29-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="d6f29-167">**IMFVideoMixerControl**</span><span class="sxs-lookup"><span data-stu-id="d6f29-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="d6f29-168">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="d6f29-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="d6f29-169">**IMFVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="d6f29-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="d6f29-170">Pins de entrada</span><span class="sxs-lookup"><span data-stu-id="d6f29-170">Input pins</span></span> | <span data-ttu-id="d6f29-171">\_serviço de \_ aceleração de vídeo Mr \_</span><span class="sxs-lookup"><span data-stu-id="d6f29-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="d6f29-172">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d6f29-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="d6f29-173">O EVR pode misturar até 16 fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d6f29-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="d6f29-174">O primeiro fluxo de entrada (pino 0) é chamado de *fluxo de referência*.</span><span class="sxs-lookup"><span data-stu-id="d6f29-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="d6f29-175">O fluxo de referência sempre aparece primeiro na ordem z.</span><span class="sxs-lookup"><span data-stu-id="d6f29-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="d6f29-176">Quaisquer fluxos adicionais são chamados de subfluxos e misturados na parte superior do fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="d6f29-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="d6f29-177">O aplicativo pode alterar a ordem z dos subfluxos, mas nenhum Subfluxo pode ser o primeiro na ordem z.</span><span class="sxs-lookup"><span data-stu-id="d6f29-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="d6f29-178">O driver de gráficos determina quais formatos de vídeo têm suporte, mas normalmente eles são limitados ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="d6f29-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="d6f29-179">Fluxo de referência: YUV progressivo ou entrelaçado sem alfa por pixel (como NV12 ou YUY2); ou RGB progressivo.</span><span class="sxs-lookup"><span data-stu-id="d6f29-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="d6f29-180">Subfluxos: YUV progressivo com per-pixel-Alpha, como AYUV ou AI44.</span><span class="sxs-lookup"><span data-stu-id="d6f29-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="d6f29-181">Os formatos de Subfluxo disponíveis podem depender do formato do fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="d6f29-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="d6f29-182">O EVR encaminha os comandos de busca upstream por meio do pino 0.</span><span class="sxs-lookup"><span data-stu-id="d6f29-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="d6f29-183">Os Pins de Subfluxo não encaminham os comandos de busca.</span><span class="sxs-lookup"><span data-stu-id="d6f29-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="d6f29-184">É responsabilidade do filtro de origem ou de Splitter manter os subfluxos sincronizados com o fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="d6f29-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f29-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f29-185">Requirements</span></span>



| <span data-ttu-id="d6f29-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f29-186">Requirement</span></span> | <span data-ttu-id="d6f29-187">Valor</span><span class="sxs-lookup"><span data-stu-id="d6f29-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6f29-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f29-188">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f29-189">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6f29-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6f29-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f29-190">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f29-191">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6f29-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6f29-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6f29-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f29-193">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d6f29-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

