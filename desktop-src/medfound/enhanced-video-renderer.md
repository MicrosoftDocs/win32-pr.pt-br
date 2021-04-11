---
description: O processador de vídeo avançado (EVR) é um componente que exibe o vídeo no monitor dos usuários.
ms.assetid: 1c985558-d25d-4f51-978a-58c05943dab9
title: Processador de vídeo aprimorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0881da0827e6cc757a0ea855bcb51864dd98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296147"
---
# <a name="enhanced-video-renderer"></a>Processador de vídeo aprimorado

O processador de vídeo avançado (EVR) é um componente que exibe o vídeo no monitor do usuário. Existem duas versões do EVR:

-   O coletor de mídia do EVR, para aplicativos Media Foundation.
-   O filtro EVR, para aplicativos do DirectShow.

Ambas as versões usam os mesmos objetos internos para renderizar vídeo e compartilham muitas das mesmas interfaces.

O EVR pode misturar até 16 fluxos de vídeo. O primeiro fluxo de entrada é chamado de *fluxo de referência*. O fluxo de referência sempre aparece primeiro na ordem z. Quaisquer fluxos adicionais são chamados de *subfluxos* e misturados na parte superior do fluxo de referência. O aplicativo pode alterar a ordem z dos subfluxos, mas nenhum Subfluxo pode ser o primeiro na ordem z.

O driver de gráficos determina quais formatos de vídeo têm suporte, mas normalmente eles são limitados ao seguinte:

-   Fluxo de referência: YUV progressivo ou entrelaçado sem alfa por pixel (como NV12 ou YUY2); ou RGB progressivo.
-   Subfluxos: YUV progressivo com per-pixel-Alpha, como AYUV ou AI44.

Os formatos de Subfluxo disponíveis podem depender do formato do fluxo de referência. Para obter mais informações, consulte [negociação de tipo de mídia EVR](evr-media-type-negotiation.md).

Internamente, o EVR usa um objeto chamado *mixer* para compor os quadros dos fluxos de entrada em uma superfície para renderização. O mixer também executa a desentrelaçamento e a correção de cores. A saída do mixer é o quadro de vídeo composto final. Um segundo objeto chamado *apresentador* renderiza o quadro de vídeo para a exibição. O apresentador agenda quando os quadros são renderizados e gerencia o dispositivo Direct3D. Um aplicativo pode fornecer uma implementação personalizada do mixer ou do apresentador.

A taxa de quadros de saída está bloqueada para o fluxo de referência. Sempre que os subfluxos recebem novos quadros, o mixer os mantém. Quando o fluxo de referência recebe um novo quadro, o mixer compõe esse quadro com os quadros de Subfluxo. (Se o fluxo de referência for entrelaçado, um quadro de referência completo poderá exigir mais de um exemplo de mídia.) É possível que um subfluxo receba mais de um quadro enquanto o mixer está aguardando um quadro de referência. Nesse caso, o mixer simplesmente descarta o quadro do Subfluxo anterior.

Como o apresentador cria o dispositivo Direct3D, ele também é responsável por compartilhar o dispositivo com outros objetos de pipeline que precisam acessar os serviços de aceleração de vídeo do DirectX (DXVA). Em particular, o mixer EVR usa os serviços de processamento de vídeo de DXVA para desentrelaçar e misturar o vídeo. Externamente ao EVR, os decodificadores de software podem usar o DXVA para decodificação de vídeo acelerada. O apresentador compartilha o dispositivo Direct3D por meio do [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md). O diagrama a seguir mostra a arquitetura interna do EVR. (O decodificador de software, sombreado em cinza, não faz parte do EVR.)

![diagrama arquitetônico mostrando o EVR.](images/5d4a1fd9-25ff-4cc5-a486-0d22f34bbfd7.gif)

## <a name="evr-interfaces"></a>Interfaces EVR

O EVR dá suporte às seguintes interfaces. Algumas dessas interfaces são implementadas pelo mixer ou apresentador. Para cada interface, o tópico de referência descreve como obter um ponteiro para a interface.

| Interface                                                    | Descrição                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)                 | Define o número de Pins de entrada no filtro EVR (somente DirectShow).                                |
| [**IEVRFilterConfigEx**](/windows/desktop/api/evr/nn-evr-ievrfilterconfigex)             | Configura o filtro EVR (somente DirectShow).                                                      |
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin)     | Permite que um plug-in EVR processe vídeo protegido.                                                 |
| [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)                 | Permite que o apresentador EVR solicite um quadro específico do mixer.                             |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                 | Permite que o Gerenciador de qualidade ajuste a qualidade do vídeo EVR.                                      |
| [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) | Habilita um mixer ou apresentador personalizado para obter ponteiros de interface do EVR.                       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                 | Retorna o identificador de dispositivo de um mixer ou apresentador EVR.                                       |
| [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)     | Controla como o EVR exibe vídeo.                                                              |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)           | Alfa-combina uma imagem de bitmap estática com o vídeo.                                                |
| [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)         | Controla como o processador de vídeo aprimorado (EVR) combina os subfluxos de vídeo.                            |
| [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2)       | Controla as preferências de desentrelaçamento de vídeo.                                                     |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)     | Mapeia uma posição em um fluxo de vídeo de entrada para a posição correspondente em um fluxo de vídeo de saída. |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)               | Exposto pelo apresentador EVR.                                                                     |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)               | Controla o processamento de vídeo, incluindo ajuste, filtros de ruído e filtros detalhados.               |
| [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)                 | Define um mixer ou apresentador no EVR.                                                             |
| [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)   | Aloca amostras de vídeo.                                                                          |



 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                    | Descrição                                                                           |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Usando o filtro EVR do DirectShow](using-the-directshow-evr-filter.md)   | Como usar o EVR em um aplicativo do DirectShow.                                       |
| [Usando o coletor de mídia do EVR](using-the-evr-media-sink.md)                 | Como usar o EVR em um aplicativo Media Foundation.                                 |
| [Usando os controles de exibição de vídeo](using-the-video-display-controls.md) | Como controlar a maneira como o EVR exibe vídeo dentro da janela do aplicativo. |
| [Usando os controles do mixer de vídeo](using-the-video-mixer-controls.md)     | Como controlar a maneira como o mixer EVR Opera.                               |
| [Negociação de tipo de mídia EVR](evr-media-type-negotiation.md)             | Descreve como o EVR determina quais formatos de vídeo ele pode aceitar como entrada.          |
| [Mixers personalizados](custom-mixers.md)                                       | Como escrever um mixer personalizado para o EVR.                                              |
| [Como escrever um apresentador EVR](how-to-write-an-evr-presenter.md)       | Como escrever um apresentador personalizado para o EVR.                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 



