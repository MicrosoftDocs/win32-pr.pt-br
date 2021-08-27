---
description: Filtro de renderização de combinação de vídeo 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtro de renderização de combinação de vídeo 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e20418aad6b9648835665fff98f894eeed1386
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986239"
---
# <a name="video-mixing-renderer-filter-9"></a>Filtro de renderização de combinação de vídeo 9

No DirectX 9, o filtro VMR-9 (Video Mixing Renderer 9) oferece recursos avançados de renderização de vídeo em todas as plataformas com suporte do DirectX. Ele é totalmente integrado aos recursos 3D do DirectX 9. Por exemplo, que você pode adicionar facilmente vídeo a jogos e outros ambientes 3D ou transformar imagens de vídeo usando sombreadores de pixel Direct3D e outros efeitos.

Esse filtro não dá suporte a portas de vídeo.

Para manter a compatibilidade com backward, a VMR-9 não é o renderador padrão em nenhum sistema. Para usar esse filtro, adicione-o ao grafo de filtro explicitamente e configure-o antes de conectar qualquer um de seus pinos de entrada. A VMR-9 usa seu próprio conjunto de interfaces, estruturas e enumerações, que nem sempre são idênticas aos tipos de dados correspondentes usados com a VMR-7.

A VMR-9 dá suporte a até 16 monitores.




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | A VMR-9 dá suporte a vários modos de renderização distintos. Ele dá suporte a um conjunto diferente de interfaces, dependendo do modo de renderização:<br /><ul><li>Todos os modos: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeintercontrol9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Modo sem renderização: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>Modo de janela: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>Modo sem janela: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>Para definir o modo de renderização, <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>chame IVMRFilterConfig9::SetRenderingMode.</strong></a> Para obter mais informações, consulte <a href="vmr-modes-of-operation.md">Modos de VMR da operação</a>.<br /> | 
| Tipos de mídia de pino de entrada | Os pinos de entrada se conectarão a qualquer tipo com suporte pelo hardware de vídeo subjacente. | 
| Interfaces de pino de entrada | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | 
| Tipos de mídia de pino de saída | Não aplicável. | 
| Interfaces de pino de saída | Não aplicável. | 
| Filtrar CLSID | CLSID_VideoMixingRenderer9 | 
| CLSID da página de propriedades | N/D | 
| Executável | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

Um aplicativo pode fornecer um objeto allocator-presenter personalizado que expõe as seguintes interfaces:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (opcional)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (opcional)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (opcional)

Para obter mais informações sobre allocator-presenters personalizados, consulte Fornecendo um Allocator-Presenter [personalizado para VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Um aplicativo também pode fornecer um compositor de plug-in personalizado que expõe a seguinte interface:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Para configurar a VMR com um compositor personalizado, chame [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Usando o renderador de combinação de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




