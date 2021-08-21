---
description: Usando o filtro DirectShow EVR
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Usando o filtro DirectShow EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc454b6d298546afdbb5a06b7081505d9ddd7c2ab87a816e79bdb13836e9a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737309"
---
# <a name="using-the-directshow-evr-filter"></a>Usando o filtro DirectShow EVR

Para criar o filtro EVR (renderização de vídeo) aprimorado, chame **CoCreateInstance**. O CLSID é CLSID \_ EnhancedVideoRenderer, definido em uuids.h. Você não precisa chamar [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ou [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para usar o filtro EVR.

Para obter mais informações sobre como usar o filtro EVR em um aplicativo DirectShow, consulte [Reprodução de áudio/vídeo no DirectShow](../directshow/audio-video-playback-in-directshow.md).

O filtro EVR começa com um pino de entrada, que corresponde ao fluxo de referência. Para adicionar pinos para substreams, consulte o filtro para a interface [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) e chame [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Chame esse método antes de conectar quaisquer pinos de entrada. O pino 0 é sempre o fluxo de referência. Conexão fixar antes de qualquer outro pin, porque o formato do fluxo de referência pode limitar quais formatos de substream estão disponíveis.

Antes de iniciar o grafo, de definir a janela de recorte de vídeo e o retângulo de destino. Para obter mais informações, consulte [Usando os controles de exibição de vídeo](using-the-video-display-controls.md).

Ao contrário do VMR (Video Mixing Renderer), o EVR não tem modos operacionais (janelas, sem janelas e assim por diante). Especialmente:

-   O EVR não dá suporte ao modo em janelas. O aplicativo deve fornecer a janela de recorte.
-   O EVR não tem um modo sem renderização. Para substituir o apresentador padrão, chame [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   O EVR não tem um modo de combinação. O EVR sempre cria o mixer. Se você tiver um fluxo de entrada, não será necessário chamar [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) para forçar o EVR a usar o mixer.

## <a name="filter-interfaces"></a>Interfaces de filtro

O filtro EVR expõe as interfaces a seguir. Algumas dessas interfaces estão documentadas no SDK do DirectShow. Use **QueryInterface** para recuperar ponteiros para estas interfaces:

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **Ipersiststream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **Ispecifypropertypages**

## <a name="input-pin-interfaces"></a>Interfaces de pino de entrada

Os pinos de entrada no filtro EVR expõem as interfaces a seguir. Use **QueryInterface** para recuperar ponteiros para estas interfaces:

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Além disso, você pode usar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para recuperar a seguinte interface:

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Renderização de vídeo aprimorada](enhanced-video-renderer.md)
</dt> </dl>

 

 
