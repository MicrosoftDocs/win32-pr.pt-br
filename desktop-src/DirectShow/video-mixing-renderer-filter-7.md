---
description: Filtro de renderização de combinação de vídeo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro de renderização de combinação de vídeo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac39dfeab90fe97085c97b3a767f06d348a0f02
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466033"
---
# <a name="video-mixing-renderer-filter-7"></a>Filtro de renderização de combinação de vídeo 7

Este tópico se aplica ao Windows XP ou posterior.

No Windows XP e posterior, o Renderização de Combinação de Vídeo 7 (VMR-7) é o renderador de vídeo padrão. Ele é chamado de VMR-7 porque, internamente, ele usa o DirectDraw 7. No DirectX 9, um filtro semelhante, mas separado, a VMR-9, está disponível para redistribuição em sistemas não XP. A VMR-9 usa o Direct3D 9.

> [!Note]  
> A VMR está disponível no Windows XP e posterior. Ele não está disponível por meio do directX redistribuível ou em versões anteriores do Windows. Para a maioria dos cenários, os aplicativos devem usar o [Renderização de Mistura de Vídeo 9.](video-mixing-renderer-filter-9.md)

 

Os recursos da VMR incluem:

-   Verdadeira combinação alfa de até 16 fluxos de entrada
-   Acesso à imagem composta antes de ser renderizada
-   Um modelo de plug-in que permite que terceiros implementem efeitos de vídeo personalizados.
-   Suporte para até 15 monitores.

Durante a criação de grafo no Windows XP e posterior, o Gerenciador de Filtros do Graph não usará os filtros mais antigos de Renderização de Vídeo ou sobreposição Mixer, a menos que o aplicativo os crie explicitamente e os adiciona ao grafo.

Para obter mais informações, [consulte Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).




| | | Interfaces de filtro | Todos os modos:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeintercontrol</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li></ul>Modo em janelas:<br /><ul><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>Ibasicvideo</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>Ivideowindow</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Modo sem janela:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Modo sem renderização:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li></ul>Mixer modo:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li></ul>Para obter informações sobre os vários modos de VMR-7, consulte <a href="vmr-modes-of-operation.md">Modos de VMR da operação</a>.<br /> | | Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_VideoSubtype: depende do hardware gráfico. Deve ser um vídeo descompactado.<br /> | | Interfaces de pino de entrada | <ul><li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Imeminputpin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (consulte Comentários)</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li></ul> | | Tipos de mídia de pino de | Não aplicável. | | Interfaces de pino de | Não aplicável. | | Filtrar CLSID | Há duas CLSIDs associadas a este filtro:<ul><li>CLSID_VideoMixingRenderer: cria a VMR-7. Se não houver recursos de sistema suficientes para criar a VMR-7, a chamada para <strong>CoCreateInstance falhará.</strong></li><li>CLSID_VideoRendererDefault: cria a VMR-7 se os recursos do sistema estão disponíveis ou cria o filtro antigo <a href="video-renderer-filter.md">do Video Renderer.</a></li></ul>Use CLSID_VideoMixingRenderer se precisar das funcionalidades específicas da VMR-7. Caso contrário, use CLSID_VideoRendererDefault, o que é quase certo para não falhar, pois ele volta para o filtro antigo do Video Renderer.<br /> | | ClSID da página de propriedades | Não aplicável. | | Arquivo executável | Quartz.dll | | <a href="merit.md">|</a> MERIT_PREFERRED + 1 | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

O pino de entrada expõe a interface **IOverlay** somente quando o filtro VMR-7 está no modo de janela. O único **método IOverlay** que o pino implementa é **GetWindowHandle**, que permite que um aplicativo obtenha um alça para a janela de vídeo do filtro. Todos os **outros métodos IOverlay** retornam E \_ NOTIMPL. No modo sem janela, o filtro não cria uma janela de vídeo, portanto, o pino não expõe a interface.

Um aplicativo pode fornecer um objeto allocator-presenter personalizado que expõe as seguintes interfaces:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (opcional)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (opcional)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (opcional)

Para obter mais informações sobre allocator-presenters personalizados, consulte Fornecendo um Allocator-Presenter [personalizado para VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Um aplicativo também pode fornecer um compositor de plug-in personalizado que expõe a seguinte interface:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Para configurar a VMR com um compositor personalizado, chame [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




