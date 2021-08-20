---
description: Interfaces para renderização e sobreposição de vídeo
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Interfaces para renderização e sobreposição de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40a8fcfa2d5e848c0e33fda14828c868cead28b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482572"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a>Interfaces para renderização e sobreposição de vídeo

Essas interfaces são suportadas pelo controle do aplicativo sobre a renderização de vídeo. Observe que algumas dessas interfaces agora foram preterida, porque o filtro renderização de combinação de vídeo fornece renderização superior e controle de sobreposição.




| Interface | Descrição | 
|-----------|-------------|
| <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a> | Fornece acesso a configurações e informações com legenda fechada. | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a> | Aplique efeitos de sobreposição à superfície de vídeo. (Preterido.) | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a> | Controle como DirectShow dimensiona uma imagem de vídeo se a janela de vídeo for menor que o tamanho nativo do vídeo. (Preterido.) | 
| <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a> | Definir propriedades de vídeo. | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> | Renderizar vídeo no modo de tela inteira exclusivo do Microsoft DirectDraw. (Preterido.) | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a> | Interface de retorno de chamada para receber notificação sobre alterações na posição de sobreposição, tamanho e visibilidade. (Preterido.) | 
| <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>Idirectdrawvideo</strong></a> | Desabilite os recursos especificados do DirectDraw. (Preterido.) | 
| <a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a> | Acesse uma superfície directDraw alocada pelo filtro <a href="overlay-mixer-filter.md">Sobreposição Mixer.</a> (Preterido.) | 
| <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a> | Implementado na camada de sobreposição Mixer. Permite que clientes sem janela, como ActiveX® controles, recebam e deem um conjunto de propriedades do retângulo de vídeo e aconselham o filtro de eventos. | 
| <a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a> | Implementado por clientes sem janela e chamado pelo Mixer para enviar notificações de eventos que afetam o retângulo de exibição de vídeo. | 
| <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a> | Definir controles de cores de vídeo no filtro sobreposição Mixer ao misturar vários fluxos de vídeo. (Preterido.) | 
| <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a> | Consulte um renderador de vídeo para obter informações de desempenho. | 
| <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>Ivideowindow</strong></a> | Definir propriedades da janela de vídeo. | 
| <ul><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeintercontrol9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul> | Interfaces do Renderização de Combinação de Vídeo 9. | 
| <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeintercontrol</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li></ul> | Interfaces do Renderização de Combinação de Vídeo 7. | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o renderador de combinação de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



