---
description: Usando o filtro EVR do DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Usando o filtro EVR do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782864"
---
# <a name="using-the-directshow-evr-filter"></a>Usando o filtro EVR do DirectShow

Para criar o filtro EVR (processador de vídeo avançado), chame **CoCreateInstance**. O CLSID é CLSID \_ EnhancedVideoRenderer, definido em UUIDs. h. Você não precisa chamar [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ou [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para usar o filtro EVR.

Para obter mais informações sobre como usar o filtro EVR em um aplicativo do DirectShow, consulte [reprodução de áudio/vídeo no DirectShow](../directshow/audio-video-playback-in-directshow.md).

O filtro EVR começa com um PIN de entrada, que corresponde ao fluxo de referência. Para adicionar Pins para subfluxos, consulte o filtro para a interface [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) e chame [**IEVRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Chame esse método antes de conectar qualquer pino de entrada. O PIN 0 é sempre o fluxo de referência. Conecte este pin antes de quaisquer outros Pins, pois o formato do fluxo de referência pode limitar quais formatos de Subfluxo estão disponíveis.

Antes de iniciar o grafo, defina a janela de recorte de vídeo e o retângulo de destino. Para obter mais informações, consulte [usando os controles de exibição de vídeo](using-the-video-display-controls.md).

Ao contrário do VMR (Video Misturation Renderer), o EVR não tem modos operacionais (janelas, sem janelas e assim por diante). Especialmente:

-   O EVR não dá suporte ao modo de janela. O aplicativo deve fornecer a janela de recorte.
-   O EVR não tem um modo sem processamento. Para substituir o apresentador padrão, chame [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   O EVR não tem um modo de combinação. O EVR sempre cria o mixer. Se você tiver um fluxo de entrada, não será necessário chamar [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) para forçar o EVR a usar o mixer.

## <a name="filter-interfaces"></a>Filtrar interfaces

O filtro EVR expõe as interfaces a seguir. Algumas dessas interfaces estão documentadas no SDK do DirectShow. Use **QueryInterface** para recuperar ponteiros para essas interfaces:

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **IPersistStream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>Interfaces de pino de entrada

Os Pins de entrada no filtro EVR expõem as interfaces a seguir. Use **QueryInterface** para recuperar ponteiros para essas interfaces:

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Além disso, você pode usar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para recuperar a seguinte interface:

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo no DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> </dl>

 

 
