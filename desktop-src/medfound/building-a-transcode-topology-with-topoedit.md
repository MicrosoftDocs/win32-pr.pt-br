---
description: Este tópico descreve como criar uma topologia de transcodificação no TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Criando uma topologia de transcodificar com TopEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5386af09b04f155295b807523cdb1c5519c946b45228df51d767e9d2a3aabe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959456"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Criando uma topologia de transcodificar com TopEdit

Este tópico descreve como criar uma topologia de transcodificação no TopoEdit.

> [!Note]  
> Esse recurso requer Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Para criar uma topologia de transcodificação

1.  No menu **Arquivo,** clique em **Renderizar Transcodificar**.

2.  Na caixa **de diálogo Selecionar Fonte de** Mídia , selecione o arquivo de origem para transcodificação.
3.  Clique em **Abrir**.
4.  Na caixa **de diálogo Escolher Perfil** de Código, selecione um dos perfis de codificação na lista lista listada.
    > [!Note]  
    > Os perfis são carregados do arquivo TranscodeProfiles.xml.

     

5.  Na caixa **de diálogo Escolher arquivo de** destino, selecione o nome do arquivo de saída.
6.  TopEdit cria a topologia de transcódigo e exibe os nós de topologia na janela principal do aplicativo.
7.  Clique no **botão Reproduzir** na barra de ferramentas para executar a sessão de mídia. Aguarde a conclusão da codificação.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopEdit carrega os perfis de codificação do arquivo TranscodeProfiles.xml. Esse arquivo está localizado no diretório Bin do SDK do Windows.

O arquivo começa com um **elemento TedTranscodeProfiles.** Cada perfil começa com um **elemento TedTranscodeProfile.** Cada perfil consiste em um conjunto de valores do formato `<VALUE_NAME Value="VALUE"/>` . Os seguintes valores são definidos:



| Valor                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | A média de bytes por segundo para o fluxo de áudio. Equivalente ao atributo [**\_ MF MT \_ AUDIO \_ AVG \_ BYTES PER \_ \_ SECOND.**](mf-mt-audio-avg-bytes-per-second-attribute.md)<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | O número de bits por exemplo para o fluxo de áudio. Equivalente ao atributo [**\_ MF MT \_ AUDIO BITS PER \_ \_ \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | O alinhamento de bloco para o fluxo de áudio. Equivalente ao atributo [**MF \_ MT \_ AUDIO BLOCK \_ \_ ALIGNMENT.**](mf-mt-audio-block-alignment-attribute.md)<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Um valor específico do codec que define o perfil de áudio. Equivalente ao [atributo MF \_ TRANSCODE \_ ENCODINGPROFILE.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**Audioformat**<br/>                                                                                     | O subtipo de áudio codificado. Equivalente ao [**atributo MF \_ MT \_ SUBTYPE.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | O número de canais no fluxo de áudio. Equivalente ao atributo [**MF \_ MT \_ AUDIO NUM \_ \_ CHANNELS.**](mf-mt-audio-num-channels-attribute.md)<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | A taxa de amostra do fluxo de áudio, em amostras por segundo. Equivalente ao [**atributo \_ MF MT \_ AUDIO \_ SAMPLES PER \_ \_ SECOND.**](mf-mt-audio-samples-per-second-attribute.md)<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**Containertype**<br/>                                                                             | O tipo de contêiner de arquivo. Equivalente ao atributo [MF \_ TRANSCODE \_ CONTAINERTYPE.](mf-transcode-containertype.md) <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**Profilename**<br/>                                                                                     | O nome de exibição do perfil.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Especifique 1 se os metadados não devem ser transferidos para o arquivo de saída ou 0 se os metadados devem ser transferidos. Equivalente ao atributo [MF \_ TRANSCODE \_ SKIP \_ METADATA \_ TRANSFER.](mf-transcode-skip-metadata-transfer.md)<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | A taxa de bits média do vídeo. Equivalente ao atributo [**\_ MT \_ AVG \_ BITRATE.**](mf-mt-avg-bitrate-attribute.md) <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Um valor específico de codec que define a qualidade da codificação. Equivalente ao [atributo MF \_ TRANSCODE \_ QUALITYVSSPEED.](mf-transcode-qualityvsspeed.md) <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Um valor específico de codec que define o perfil de vídeo. Equivalente ao [atributo MF \_ TRANSCODE \_ ENCODINGPROFILE.](mf-transcode-encodingprofile.md) <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | O subtipo de vídeo codificado. Equivalente ao [**atributo MF \_ MT \_ SUBTYPE.**](mf-mt-subtype-attribute.md)<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | A altura do vídeo de saída. Equivalente ao atributo MT FRAME SIZE do [**\_ MF. \_ \_**](mf-mt-frame-size-attribute.md)<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | O denominador da taxa de quadros do vídeo de saída. Equivalente ao atributo [**\_ MF MT \_ FRAME \_ RATE.**](mf-mt-frame-rate-attribute.md)<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | O numerador da taxa de quadros do vídeo de saída. Equivalente ao atributo [**\_ MF MT \_ FRAME \_ RATE.**](mf-mt-frame-rate-attribute.md)<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | A largura do vídeo de saída. Equivalente ao atributo MT FRAME SIZE do [**\_ MF. \_ \_**](mf-mt-frame-size-attribute.md)<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | O denominador da PAR (taxa de proporção de pixel) do vídeo de saída. Equivalente ao atributo [**\_ MF MT \_ PIXEL ASPECT \_ \_ RATIO.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | O numerador do PAR do vídeo de saída. Equivalente ao atributo [**\_ MF MT \_ PIXEL ASPECT \_ \_ RATIO.**](mf-mt-pixel-aspect-ratio-attribute.md) <br/>                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TopEdit](topoedit.md)
</dt> </dl>

 

 




