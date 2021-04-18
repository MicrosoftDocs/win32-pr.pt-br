---
description: Os atributos a seguir podem ser usados para configurar o mecanismo de captura.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Atributos do mecanismo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105788863"
---
# <a name="capture-engine-attributes"></a>Atributos do mecanismo de captura

Os atributos a seguir podem ser usados para configurar o mecanismo de captura.

Os seguintes atributos estão relacionados a dispositivos de captura:



| Atributo                                                                                                                              | Descrição                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [\_fluxo de câmera do mecanismo de captura MF \_ \_ \_ \_ bloqueado](mf-capture-engine-camera-stream-blocked.md)                                            | Sinaliza que a captura de vídeo está sendo bloqueada pelo driver.                                                         |
| [\_fluxo de câmera do mecanismo de captura MF \_ \_ \_ \_ desbloqueado](mf-capture-engine-camera-stream-unblocked.md)                                        | Sinaliza que a captura de vídeo é restaurada após ser bloqueada.                                                        |
| [\_Gerenciador de \_ D3D do mecanismo de captura MF \_ \_](mf-capture-engine-d3d-manager.md)                                                                 | Define um ponteiro para o Gerenciador de Dispositivos DXGI no mecanismo de captura.                                                   |
| [\_FIELDOFUSE de \_ \_ \_ \_ \_ desbloqueio de MFT do decodificador do mecanismo de captura \_ MF](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Permite que o mecanismo de captura use um decodificador com restrições de campo de uso.                                    |
| [\_mecanismo de captura MF \_ \_ desabilitar \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Especifica se o mecanismo de captura usa a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo.                    |
| [captura de MF \_ \_ desabilitar \_ \_ transformações de hardware](mf-capture-engine-disable-hardware-transforms.md)                                        | Desabilita o uso de transformações de Media Foundation baseadas em hardware (MFTs) no mecanismo de captura.                       |
| [\_mecanismo de captura MF \_ \_ habilitar notificação do \_ \_ streamstate da câmera \_](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indica se as notificações de estado do fluxo devem ser habilitadas.                                                    |
| [\_atributo de \_ \_ \_ \_ \_ desbloqueio de MFT FIELDOFUSE do CODIFICAdor do mecanismo \_ de captura MF](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Permite que o mecanismo de captura use um codificador com restrições de campo de uso.                                   |
| [\_GUID do \_ gerador de eventos do mecanismo de captura MF \_ \_ \_](mf-capture-engine-event-generator-guid.md)                                              | Identifica o componente que gerou um evento de captura.                                                           |
| [\_índice de \_ fluxo de eventos do mecanismo de captura MF \_ \_ \_](mf-capture-engine-event-stream-index.md)                                                  | Identifica qual fluxo gerou um evento de captura.                                                                 |
| [\_configuração da \_ mediaização do mecanismo de captura MF \_ \_](mf-capture-engine-mediasource-config.md)                                                   | Contém propriedades de configuração para a origem de captura.                                                          |
| [o \_ mecanismo de captura MF \_ \_ registrou o \_ áudio do coletor \_ máximo de \_ \_ amostras processadas \_](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Define o número máximo de amostras processadas que podem ser armazenadas em buffer no caminho de áudio do coletor de registros.                   |
| [o \_ mecanismo de captura MF \_ registro de áudio do \_ \_ coletor máximo de \_ \_ \_ amostras não processadas \_](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de áudio do coletor de registros. |
| [vídeo do coletor de gravação do mecanismo de captura do MF \_ \_ máximo de \_ \_ \_ \_ \_ amostras processadas \_](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Define o número máximo de amostras processadas que podem ser armazenadas em buffer no caminho de vídeo do coletor de registros.                   |
| [\_vídeo do mecanismo de captura MF \_ \_ registro máximo de amostras não \_ \_ \_ \_ processadas \_](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de vídeo do coletor de registros.  |
| [\_tipo de \_ coletor do mecanismo de captura MF \_ \_](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Especifica um tipo de coletor de captura.                                                                                  |
| [o \_ mecanismo de captura MF \_ \_ usa \_ apenas o dispositivo de áudio \_ \_](mf-capture-engine-use-audio-device-only.md)                                           | Especifica se o mecanismo de captura captura áudio, mas não vídeo.                                                 |
| [o \_ mecanismo de captura MF \_ \_ usa \_ somente o dispositivo de vídeo \_ \_](mf-capture-engine-use-video-device-only.md)                                           | Especifica se o mecanismo de captura captura vídeo, mas não áudio.                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



