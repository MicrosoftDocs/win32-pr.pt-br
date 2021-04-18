---
description: Mixers personalizados
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mixers personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793650"
---
# <a name="custom-mixers"></a>Mixers personalizados

Este tópico descreve como gravar um mixer personalizado para o processador de vídeo avançado (EVR). Você pode usar um mixer personalizado com o coletor de mídia do Media Foundation EVR ou o filtro EVR do DirectShow. Para obter mais informações sobre mixers e apresentadores, consulte [processador de vídeo aprimorado](enhanced-video-renderer.md).

O Mixer é uma Media Foundation de transformação (MFT) com uma ou mais entradas (o fluxo de referência mais os subfluxos) e uma saída. O fluxo de entrada recebe amostras de upstream. O fluxo de saída fornece amostras para o apresentador. O EVR é responsável por chamar [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) no mixer, e o apresentador é responsável por chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

No mínimo, um mixer EVR deve implementar as seguintes interfaces:



| Interface                                                                | Descrição                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Fornece a funcionalidade de MFT base.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permite que o mixer obtenha interfaces do EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Permite que o mixer obtenha interfaces do EVR.                                                |
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Usado para expor o atributo de [**\_ \_ \_ reconhecimento de D3D SA do MF**](mf-sa-d3d-aware-attribute.md) para o EVR. |



 

Opcionalmente, um MFT pode implementar qualquer uma das seguintes interfaces:



| Interface                                                | Descrição                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Necessário para reproduzir conteúdo protegido.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Expõe interfaces como [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) e [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) ao aplicativo. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Permite que o Gerenciador de qualidade ajuste a qualidade do vídeo.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Permite que o aplicativo Misture um bitmap estático no vídeo.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mapeia coordenadas no quadro de vídeo de saída para coordenadas no quadro de vídeo de entrada.                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Expõe alguns recursos de processamento de vídeo de DXVA ao aplicativo.                                                                                      |



 

A negociação de formato com o mixer funciona da seguinte maneira:

1.  O EVR define o tipo de mídia no fluxo de referência.
2.  O EVR chama [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) no apresentador com a mensagem **MFVP \_ Message \_ INVALIDATEMEDIATYPE** .

3.  O apresentador define o tipo de mídia no fluxo de saída do mixer.
4.  O EVR define o tipo de mídia nos subfluxos.

Se o tipo de mídia no fluxo de referência for alterado, os outros tipos de mídia do mixer não serão mais válidos. O método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer falhará e retornará a **\_ alteração do \_ \_ fluxo \_ de MF e de transformação**. O apresentador não deve fazer nada neste ponto. O EVR iniciará o processo de negociação de formato novamente.

Quando qualquer fluxo de entrada atinge o final do fluxo, o EVR chama [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) no mixer com o [**\_ \_ \_ fim \_ da notificação de mensagem \_ de MFT**](mft-message-notify-end-of-stream.md).

O mixer envia os eventos a seguir para o EVR, usando a interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) do EVR. Essa interface está documentada na documentação do SDK do DirectShow.



| Evento                                            | Descrição                            |
|--------------------------------------------------|----------------------------------------|
| [**exemplo de EC \_ \_ necessário**](../directshow/ec-sample-needed.md) | O mixer requer um novo exemplo de entrada. |



 

O EVR pode chamar [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer antes de o streaming começar. O mixer não deve reprovar essas chamadas. Em vez disso, ele deve preencher a superfície de saída com pixels pretos. O mixer deve continuar a amostras de saída de preenchimento de cor até receber uma mensagem de [**MFT \_ \_ notificar \_ início \_**](mft-message-notify-begin-streaming.md) de mensagem de streaming ou o método [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) é chamado. Se o mixer receber uma mensagem de [**MFT \_ \_ notificar \_ término de \_ transmissão de mensagem**](mft-message-notify-end-streaming.md) , ele deverá retornar ao modo de preenchimento de cor.

## <a name="implementing-imfvideodeviceid"></a>Implementando IMFVideoDeviceID

A interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contém um método, [**DeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), que retorna um GUID de dispositivo. O GUID do dispositivo garante que o apresentador e o mixer usem tecnologias compatíveis. Se os GUIDs do dispositivo não corresponderem, o EVR não será inicializado.

O mixer e o apresentador padrão usam o Direct3D 9, com o GUID do dispositivo igual ao IID \_ IDirect3DDevice9. Se você pretende usar seu apresentador personalizado com o mixer padrão, o GUID do dispositivo do apresentador deve ser IID \_ IDirect3DDevice9. Se você substituir ambos os componentes, poderá definir um novo GUID de dispositivo.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementando IMFTopologyServiceLookupClient

O mixer deve implementar a interface [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) . Antes de o streaming começar, o EVR chama [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e passa um ponteiro para a interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) do EVR. O mixer usa esse ponteiro para obter ponteiros de interface do EVR.

No mínimo, o mixer deve consultar a seguinte interface:

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Quando EVR chama [**IMFTopologyServiceLookupClient:: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), o mixer deve liberar todos os ponteiros obtidos da chamada para [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).

## <a name="mixer-attributes"></a>Atributos do mixer

Um mixer deve dar suporte aos seguintes atributos.



| Atributo                                                                        | Descrição                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Reconhecimento de \_ D3D \_ SA do MF**](mf-sa-d3d-aware-attribute.md)                          | Especifica se o mixer dá suporte a DXVA (aceleração de vídeo do DirectX).                                                                                                                                                                               |
| [**\_contagem de \_ \_ amostra necessária da SA \_ MF**](mf-sa-required-sample-count-attribute.md) | O número de amostras de vídeo que o EVR deve alocar para cada fluxo de mixer. Esse atributo se aplica a fluxos individuais; Use o repositório de atributos retornado por [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes). |



 

## <a name="setting-the-mixer-on-the-evr"></a>Configurando o mixer no EVR

Para definir um mixer personalizado no EVR, chame [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). O filtro EVR do DirectShow e o coletor de mídia EVR implementam esse método.

**Objeto de ativação EVR**. Se você estiver usando o objeto de ativação EVR, poderá fornecer um mixer personalizado definindo um dos seguintes atributos no objeto de ativação EVR:



| Atributo                                                                                                 | Descrição                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**ativar \_ \_ mixer de \_ vídeo \_ personalizado \_ do MF ativar**](mf-activate-custom-video-mixer-activate-attribute.md) | Ponteiro para um objeto de ativação para o mixer. O objeto de ativação deve implementar a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . |
| [**\_Ativar \_ CLSID do \_ mixer de vídeo personalizado \_ \_ MF**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID do mixer.                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> </dl>

 

 
