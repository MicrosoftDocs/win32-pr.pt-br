---
description: Filtro de processador de mixagem de vídeo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro de processador de mixagem de vídeo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502242"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="2abeb-103">Filtro de processador de mixagem de vídeo 7</span><span class="sxs-lookup"><span data-stu-id="2abeb-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="2abeb-104">Este tópico aplica-se ao Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2abeb-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="2abeb-105">No Windows XP e posterior, o processador de mixagem de vídeo 7 (VMR-7) é o renderizador de vídeo padrão.</span><span class="sxs-lookup"><span data-stu-id="2abeb-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="2abeb-106">Ele é chamado de VMR-7 porque usa internamente o DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="2abeb-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="2abeb-107">No DirectX 9, um filtro semelhante, mas separado, o VMR-9, está disponível para redistribuição em sistemas não XP.</span><span class="sxs-lookup"><span data-stu-id="2abeb-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="2abeb-108">O VMR-9 usa o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="2abeb-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="2abeb-109">O VMR está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="2abeb-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="2abeb-110">Ele não está disponível por meio de pacotes redistribuíveis do DirectX ou em versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="2abeb-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="2abeb-111">Para a maioria dos cenários, os aplicativos devem usar o [processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md).</span><span class="sxs-lookup"><span data-stu-id="2abeb-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="2abeb-112">Os recursos do VMR incluem:</span><span class="sxs-lookup"><span data-stu-id="2abeb-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="2abeb-113">Mistura alfa verdadeira de até 16 fluxos de entrada</span><span class="sxs-lookup"><span data-stu-id="2abeb-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="2abeb-114">Acesso à imagem compostada antes de ser renderizada</span><span class="sxs-lookup"><span data-stu-id="2abeb-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="2abeb-115">Um modelo de plug-in que permite que terceiros implementem efeitos de vídeo personalizados.</span><span class="sxs-lookup"><span data-stu-id="2abeb-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="2abeb-116">Suporte para até 15 monitores.</span><span class="sxs-lookup"><span data-stu-id="2abeb-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="2abeb-117">Durante a criação do grafo no Windows XP e versões posteriores, o Gerenciador do grafo de filtro não usará os filtros mais antigos do mixer de vídeo ou de sobreposição, a menos que o aplicativo os crie explicitamente e adicione ao grafo.</span><span class="sxs-lookup"><span data-stu-id="2abeb-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="2abeb-118">Para obter mais informações, consulte [usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="2abeb-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2abeb-119">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="2abeb-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="2abeb-120">Todos os modos:</span><span class="sxs-lookup"><span data-stu-id="2abeb-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="2abeb-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="2abeb-133">Modo em janela:</span><span class="sxs-lookup"><span data-stu-id="2abeb-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="2abeb-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="2abeb-138">Modo sem janela:</span><span class="sxs-lookup"><span data-stu-id="2abeb-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="2abeb-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="2abeb-141">Modo de renderização:</span><span class="sxs-lookup"><span data-stu-id="2abeb-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="2abeb-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="2abeb-143">Modo de mixer:</span><span class="sxs-lookup"><span data-stu-id="2abeb-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="2abeb-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="2abeb-145">Para obter informações sobre os vários modos do VMR-7, consulte <a href="vmr-modes-of-operation.md">modos de operação do VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="2abeb-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2abeb-146">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="2abeb-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="2abeb-147">Tipo principal: MEDIATYPE_VideoSubtype: depende do hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="2abeb-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="2abeb-148">Deve ser um vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="2abeb-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2abeb-149">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="2abeb-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="2abeb-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (consulte comentários)</span><span class="sxs-lookup"><span data-stu-id="2abeb-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="2abeb-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="2abeb-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2abeb-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2abeb-157">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="2abeb-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="2abeb-158">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="2abeb-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2abeb-159">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="2abeb-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="2abeb-160">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="2abeb-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2abeb-161">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="2abeb-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="2abeb-162">Há dois CLSIDs associados a este filtro:</span><span class="sxs-lookup"><span data-stu-id="2abeb-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="2abeb-163">CLSID_VideoMixingRenderer: cria o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="2abeb-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="2abeb-164">Se não houver recursos suficientes do sistema para criar o VMR-7, a chamada para <strong>CoCreateInstance</strong> falhará.</span><span class="sxs-lookup"><span data-stu-id="2abeb-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="2abeb-165">CLSID_VideoRendererDefault: cria o VMR-7 se os recursos do sistema estiverem disponíveis ou criará o filtro de <a href="video-renderer-filter.md">processamento de vídeo</a> antigo.</span><span class="sxs-lookup"><span data-stu-id="2abeb-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="2abeb-166">Use CLSID_VideoMixingRenderer se você precisar dos recursos específicos do VMR-7.</span><span class="sxs-lookup"><span data-stu-id="2abeb-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="2abeb-167">Caso contrário, use CLSID_VideoRendererDefault, que é quase certo para não falhar, pois ele volta ao filtro de processamento de vídeo antigo.</span><span class="sxs-lookup"><span data-stu-id="2abeb-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2abeb-168">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="2abeb-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="2abeb-169">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="2abeb-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2abeb-170">Executável</span><span class="sxs-lookup"><span data-stu-id="2abeb-170">Executable</span></span></td>
<td><span data-ttu-id="2abeb-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2abeb-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2abeb-172"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="2abeb-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="2abeb-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="2abeb-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2abeb-174"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="2abeb-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="2abeb-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2abeb-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2abeb-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="2abeb-176">Remarks</span></span>

<span data-ttu-id="2abeb-177">O PIN de entrada expõe a interface **IOverlay** somente quando o filtro VMR-7 está no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="2abeb-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="2abeb-178">O único método **IOverlay** que o PIN implementa é **GetWindowHandle**, que permite que um aplicativo obtenha um identificador para a janela de vídeo do filtro.</span><span class="sxs-lookup"><span data-stu-id="2abeb-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="2abeb-179">Todos os outros métodos **IOverlay** retornam E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="2abeb-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="2abeb-180">No modo sem janela, o filtro não cria uma janela de vídeo, portanto, o PIN não expõe a interface.</span><span class="sxs-lookup"><span data-stu-id="2abeb-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="2abeb-181">Um aplicativo pode fornecer um objeto de apresentador de alocador personalizado que expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="2abeb-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="2abeb-182">**IVMRImagePresenter**</span><span class="sxs-lookup"><span data-stu-id="2abeb-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="2abeb-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (opcional)</span><span class="sxs-lookup"><span data-stu-id="2abeb-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="2abeb-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (opcional)</span><span class="sxs-lookup"><span data-stu-id="2abeb-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="2abeb-185">**IVMRSurfaceAllocator**</span><span class="sxs-lookup"><span data-stu-id="2abeb-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="2abeb-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (opcional)</span><span class="sxs-lookup"><span data-stu-id="2abeb-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="2abeb-187">Para obter mais informações sobre os apresentadores de alocadores personalizados, consulte [fornecendo um Allocator-Presenter personalizado para o VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span><span class="sxs-lookup"><span data-stu-id="2abeb-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="2abeb-188">Um aplicativo também pode fornecer um compositor de plug-in personalizado que expõe a seguinte interface:</span><span class="sxs-lookup"><span data-stu-id="2abeb-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="2abeb-189">**IVMRImageCompositor**</span><span class="sxs-lookup"><span data-stu-id="2abeb-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="2abeb-190">Para configurar o VMR com um compositor personalizado, chame [**IVMRFilterConfig:: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="2abeb-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2abeb-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2abeb-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2abeb-192">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="2abeb-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




