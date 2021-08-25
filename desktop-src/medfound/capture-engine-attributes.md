---
description: Os atributos a seguir podem ser usados para configurar o Mecanismo de Captura.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Atributos do Mecanismo de Captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e79d0410407d12b46c0577615088f0f925b8558169d02140486b9fdc8fb303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959146"
---
# <a name="capture-engine-attributes"></a>Atributos do Mecanismo de Captura

Os atributos a seguir podem ser usados para configurar o Mecanismo de Captura.

Os seguintes atributos estão relacionados à captura de dispositivos:



| Atributo                                                                                                                              | Descrição                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [FLUXO DE CÂMERA DO MECANISMO DE CAPTURA DE MF \_ \_ \_ \_ \_ BLOQUEADO](mf-capture-engine-camera-stream-blocked.md)                                            | Sinaliza que a captura de vídeo está sendo bloqueada pelo driver.                                                         |
| [FLUXO DE CÂMERA DO MECANISMO DE CAPTURA DE MF \_ \_ \_ \_ \_ DESBLOQUEADO](mf-capture-engine-camera-stream-unblocked.md)                                        | Sinaliza que a captura de vídeo é restaurada após ser bloqueada.                                                        |
| [MF \_ CAPTURE \_ ENGINE \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md)                                                                 | Define um ponteiro para o Gerenciador de Dispositivos DXGI no mecanismo de captura.                                                   |
| [MF \_ CAPTURE \_ ENGINE \_ DECODER \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ ATTRIBUTE](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Permite que o mecanismo de captura use um decodificador que tenha restrições de campo de uso.                                    |
| [MF \_ CAPTURE \_ ENGINE \_ DISABLE \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Especifica se o mecanismo de captura usa a DXVA (Aceleração de Vídeo) do DirectX para decodificação de vídeo.                    |
| [CAPTURA DE MF \_ \_ DESABILITAR \_ AS \_ TRANSFORMAÇÃOS DE HARDWARE](mf-capture-engine-disable-hardware-transforms.md)                                        | Desabilita o uso de MFTs (transformaçãos Media Foundation hardware) no mecanismo de captura.                       |
| [NOTIFICAÇÃO DO \_ \_ \_ \_ \_ STREAMSTATE DO \_ MECANISMO DE CAPTURA DE MF](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indica se as notificações de estado de fluxo devem ser habilitadas.                                                    |
| [ATRIBUTO \_ \_ \_ \_ MFT \_ FIELDOFUSE \_ UNLOCK \_ DO CODIFICADOR DO MECANISMO DE CAPTURA MF](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Permite que o mecanismo de captura use um codificador que tenha restrições de campo de uso.                                   |
| [GUID DO GERADOR DE EVENTOS DO MECANISMO DE CAPTURA \_ \_ \_ \_ DE \_ MF](mf-capture-engine-event-generator-guid.md)                                              | Identifica o componente que gerou um evento de captura.                                                           |
| [ÍNDICE DE FLUXO DE \_ \_ EVENTOS DO MECANISMO \_ DE \_ \_ CAPTURA DE MF](mf-capture-engine-event-stream-index.md)                                                  | Identifica qual fluxo gerou um evento de captura.                                                                 |
| [MF \_ CAPTURE \_ ENGINE \_ MEDIASOURCE \_ CONFIG](mf-capture-engine-mediasource-config.md)                                                   | Contém propriedades de configuração para a origem da captura.                                                          |
| [AMOSTRAS \_ PROCESSADAS MÁXIMAS DE \_ ÁUDIO \_ \_ PROCESSADAS \_ \_ \_ \_ DO RECORD DO MECANISMO DE CAPTURA DE MF](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Define o número máximo de amostras processadas que podem ser armazenados em buffer no caminho de áudio do sink de registro.                   |
| [AMOSTRAS DE ÁUDIO MÁX. DE ÁUDIO \_ \_ \_ \_ \_ \_ MÁX. \_ \_ DE REGISTRO DO MECANISMO DE CAPTURA MF](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Define o número máximo de amostras não processadas que podem ser armazenados em buffer para processamento no caminho de áudio do record sink.. |
| [EXEMPLOS MÁXIMO \_ DE AMOSTRAS PROCESSADAS DO VÍDEO DO RECORD \_ \_ SINK \_ DO \_ \_ \_ \_ MECANISMO DE CAPTURA DE MF](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Define o número máximo de amostras processadas que podem ser armazenados em buffer no caminho de vídeo do sink de registro.                   |
| [EXEMPLOS MÁXIMO DE AMOSTRAS NÃO PROCESSADAS DO RECORD SINK DO MECANISMO DE CAPTURA \_ \_ \_ \_ \_ \_ \_ \_ DE MF](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Define o número máximo de amostras não processadas que podem ser armazenados em buffer para processamento no caminho de vídeo do record sink.  |
| [TIPO DE SINK \_ DO MECANISMO DE CAPTURA \_ \_ DE \_ MF](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Especifica um tipo de sink de captura.                                                                                  |
| [O MECANISMO DE CAPTURA DE MF \_ USA APENAS O DISPOSITIVO DE \_ \_ \_ \_ \_ ÁUDIO](mf-capture-engine-use-audio-device-only.md)                                           | Especifica se o mecanismo de captura captura o áudio, mas não o vídeo.                                                 |
| [O MECANISMO DE CAPTURA DE MF \_ USA APENAS O DISPOSITIVO DE \_ \_ \_ \_ \_ VÍDEO](mf-capture-engine-use-video-device-only.md)                                           | Especifica se o mecanismo de captura captura o vídeo, mas não o áudio.                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



