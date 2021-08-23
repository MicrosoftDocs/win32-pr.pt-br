---
description: Mixers personalizados
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mixers personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587206f7bc34d1fad4a64a12aeff9ab8ad21e18a84c92c8f2302776fdc126a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605986"
---
# <a name="custom-mixers"></a>Mixers personalizados

Este tópico descreve como escrever um mixer personalizado para o renderização de vídeo aprimorado (EVR). Você pode usar um mixer personalizado com o Media Foundation de mídia EVR ou o filtro DirectShow EVR. Para obter mais informações sobre mixers e apresentadores, consulte [Renderização de vídeo aprimorada.](enhanced-video-renderer.md)

O mixer é uma Media Foundation (MFT) com uma ou mais entradas (o fluxo de referência mais os substreams) e uma saída. O fluxo de entrada recebe exemplos de upstream. O fluxo de saída fornece exemplos para o apresentador. O EVR é responsável por chamar [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) no mixer e o apresentador é responsável por chamar [**IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)

No mínimo, um mixer EVR deve implementar as seguintes interfaces:



| Interface                                                                | Descrição                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Fornece a funcionalidade base do MFT.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permite que o mixer receba interfaces do EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Permite que o mixer receba interfaces do EVR.                                                |
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Usado para expor o [**atributo \_ MF SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) ao EVR. |



 

Opcionalmente, um MFT pode implementar qualquer uma das seguintes interfaces:



| Interface                                                | Descrição                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Necessário para reproduzir conteúdo protegido.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Expõe interfaces como [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) e [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) ao aplicativo. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Permite que o gerenciador de qualidade ajuste a qualidade do vídeo.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Permite que o aplicativo misture um bitmap estático no vídeo.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mapas coordenadas no quadro de vídeo de saída para coordenadas no quadro de vídeo de entrada.                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Expõe alguns recursos de processamento de vídeo DXVA para o aplicativo.                                                                                      |



 

A negociação de formato com o mixer funciona da seguinte forma:

1.  O EVR define o tipo de mídia no fluxo de referência.
2.  O EVR chama [**IMFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) no apresentador com a mensagem **MFVP \_ \_ INVALIDATEMEDIATYPE.**

3.  O apresentador define o tipo de mídia no fluxo de saída do mixer.
4.  O EVR define o tipo de mídia nos substreams.

Se o tipo de mídia no fluxo de referência mudar, os outros tipos de mídia do mixer não serão mais válidos. O método [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer falhará e retornará **MF \_ E TRANSFORM \_ STREAM \_ \_ CHANGE.** O apresentador não deve fazer nada neste momento. O EVR iniciará o processo de negociação de formato novamente.

Quando qualquer fluxo de entrada atinge o final do fluxo, o EVR chama [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) no mixer com [**MFT \_ MESSAGE NOTIFY END OF \_ \_ \_ \_ STREAM**](mft-message-notify-end-of-stream.md).

O mixer envia os seguintes eventos para o EVR, usando a interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) da EVR. Essa interface está documentada na documentação DirectShow SDK.



| Evento                                            | Descrição                            |
|--------------------------------------------------|----------------------------------------|
| [**EXEMPLO \_ DE EC \_ NECESSÁRIO**](../directshow/ec-sample-needed.md) | O mixer requer um novo exemplo de entrada. |



 

O EVR pode chamar [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer antes do início do streaming. O mixer não deve falhar nessas chamadas. Em vez disso, ele deve preencher a superfície de saída com pixels pretos. O mixer deve continuar a preencher as cores das amostras de saída até receber uma mensagem DE NOTIFICAÇÃO DE MENSAGEM [**MFT \_ BEGIN \_ \_ \_ STREAMING**](mft-message-notify-begin-streaming.md) ou o [**método ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ser chamado. Se o mixer receber uma mensagem DE STREAMING FINAL [**\_ \_ NOTIFICAÇÃO \_ \_**](mft-message-notify-end-streaming.md) DE MENSAGEM MFT, ele deverá alternar de volta para o modo de preenchimento de cores.

## <a name="implementing-imfvideodeviceid"></a>Implementando IMFVideoDeviceID

A interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contém um método, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)que retorna um GUID do dispositivo. O GUID do dispositivo garante que o apresentador e o mixer usem tecnologias compatíveis. Se os GUIDs do dispositivo não corresponderem, o EVR não será inicializado.

O mixer e o apresentador padrão usam o Direct3D 9, com o GUID do dispositivo igual a IID \_ IDirect3DDevice9. Se você pretende usar seu apresentador personalizado com o mixer padrão, o GUID do dispositivo do apresentador deve ser \_ IID IDirect3DDevice9. Se você substituir ambos os componentes, poderá definir um novo GUID do dispositivo.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementando IMFTopologyServiceLookupClient

O mixer deve implementar a interface [**IMFTopologyServiceLookupClient.**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) Antes do início do streaming, o EVR chama [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e passa um ponteiro para a interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) da EVR. O mixer usa esse ponteiro para obter ponteiros de interface do EVR.

No mínimo, o mixer deve consultar a seguinte interface:

-   [**Imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Quando o EVR chama [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), o mixer deve liberar quaisquer ponteiros obtidos da chamada para [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).

## <a name="mixer-attributes"></a>Mixer Atributos

Um mixer deve dar suporte aos atributos a seguir.



| Atributo                                                                        | Descrição                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                          | Especifica se o mixer dá suporte à DXVA (Aceleração de Vídeo DirectX).                                                                                                                                                                               |
| [**CONTAGEM DE \_ \_ AMOSTRAS \_ EXIGIDAS PELO \_ MF SA**](mf-sa-required-sample-count-attribute.md) | O número de amostras de vídeo que o EVR deve alocar para cada fluxo de mixer. Esse atributo se aplica a fluxos individuais; use o armazenamento de atributos retornado [**por IMFTransform::GetInputStreamAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) |



 

## <a name="setting-the-mixer-on-the-evr"></a>Definindo o Mixer no EVR

Para definir um mixer personalizado no EVR, chame [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). O filtro DirectShow EVR e o sink de mídia EVR implementam esse método.

**Objeto de ativação EVR**. Se você estiver usando o objeto de ativação EVR, poderá fornecer um mixer personalizado definindo um dos seguintes atributos no objeto de ativação EVR:



| Atributo                                                                                                 | Descrição                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**ATIVAR O MIXER \_ \_ DE VÍDEO \_ \_ PERSONALIZADO \_ DO MF**](mf-activate-custom-video-mixer-activate-attribute.md) | Ponteiro para um objeto de ativação para o mixer. O objeto de ativação deve implementar a interface [**IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID do mixer.                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo aprimorada](enhanced-video-renderer.md)
</dt> </dl>

 

 
