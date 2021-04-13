---
description: Este tópico descreve como criar uma topologia de transcodificação no TopoEdit.
ms.assetid: 9a7b57f9-f606-4874-9fd3-aa37215f6f20
title: Criando uma topologia de transcodificação com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ef750b4dd54ef05ab7733cc861d7a09dd5d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501199"
---
# <a name="building-a-transcode-topology-with-topoedit"></a>Criando uma topologia de transcodificação com TopoEdit

Este tópico descreve como criar uma topologia de transcodificação no TopoEdit.

> [!Note]  
> Este recurso requer o Windows 7

 

## <a name="to-build-a-transcoding-topology"></a>Para criar uma topologia de transcodificação

1.  No menu **arquivo** , clique em **renderizar transcodificação**.

2.  Na caixa de diálogo **selecionar origem da mídia** , selecione o arquivo de origem para transcodificação.
3.  Clique em **Abrir**.
4.  Na caixa de diálogo **escolher perfil transcodificar** , selecione um dos perfis de codificação na lista suspensa.
    > [!Note]  
    > Os perfis são carregados do arquivo TranscodeProfiles.xml.

     

5.  Na caixa de diálogo **escolher arquivo de destino** , selecione o nome do arquivo de saída.
6.  TopoEdit cria a topologia de transcodificação e exibe os nós de topologia na janela principal do aplicativo.
7.  Clique no botão **reproduzir** na barra de ferramentas para executar a sessão de mídia. Aguarde a conclusão da codificação.

## <a name="transcodeprofilesxml"></a>TranscodeProfiles.xml

TopoEdit carrega os perfis de codificação do arquivo TranscodeProfiles.xml. Esse arquivo está localizado no diretório bin do SDK do Windows.

O arquivo começa com um elemento **TedTranscodeProfiles** . Cada perfil começa com um elemento **TedTranscodeProfile** . Cada perfil consiste em um conjunto de valores do formato `<VALUE_NAME Value="VALUE"/>` . Os seguintes valores são definidos:



| Valor                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AudioAvgBytesPerSecond"></span><span id="audioavgbytespersecond"></span><span id="AUDIOAVGBYTESPERSECOND"></span>**AudioAvgBytesPerSecond**<br/>                                         | A média de bytes por segundo para o fluxo de áudio. Equivalente ao atributo [**de \_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) .<br/>                                                |
| <span id="AudioBitsPerSample"></span><span id="audiobitspersample"></span><span id="AUDIOBITSPERSAMPLE"></span>**AudioBitsPerSample**<br/>                                                         | O número de bits por amostra para o fluxo de áudio. Equivalente ao atributo [**MF \_ MT \_ Audio \_ bits \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) .<br/>                                                          |
| <span id="AudioBlockAlignment"></span><span id="audioblockalignment"></span><span id="AUDIOBLOCKALIGNMENT"></span>**AudioBlockAlignment**<br/>                                                     | O alinhamento de bloco para o fluxo de áudio. Equivalente ao atributo [**de \_ \_ alinhamento de \_ bloco \_ de áudio MF MT**](mf-mt-audio-block-alignment-attribute.md) .<br/>                                                                     |
| <span id="AudioEncodingProfile"></span><span id="audioencodingprofile"></span><span id="AUDIOENCODINGPROFILE"></span>**AudioEncodingProfile**<br/>                                                 | Um valor específico de codec que define o perfil de áudio. Equivalente ao atributo [ \_ \_ ENCODINGPROFILE de rescodificação MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="AudioFormat"></span><span id="audioformat"></span><span id="AUDIOFORMAT"></span>**AudioFormat**<br/>                                                                                     | O subtipo de áudio codificado. Equivalente ao atributo [**de \_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="AudioNumChannels"></span><span id="audionumchannels"></span><span id="AUDIONUMCHANNELS"></span>**AudioNumChannels**<br/>                                                                 | O número de canais no fluxo de áudio. Equivalente ao atributo [**MF \_ MT \_ Audio \_ num \_ Channels**](mf-mt-audio-num-channels-attribute.md) .<br/>                                                                         |
| <span id="AudioSamplesPerSecond"></span><span id="audiosamplespersecond"></span><span id="AUDIOSAMPLESPERSECOND"></span>**AudioSamplesPerSecond**<br/>                                             | A taxa de amostra do fluxo de áudio, em amostras por segundo. Equivalente ao atributo [**MF \_ MT \_ Audio \_ Samples \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) .<br/>                                            |
| <span id="ContainerType"></span><span id="containertype"></span><span id="CONTAINERTYPE"></span>**Contêinertype**<br/>                                                                             | O tipo de contêiner de arquivo. Equivalente ao atributo [ \_ \_ contêinertype de transcodificação MF](mf-transcode-containertype.md) . <br/>                                                                                                       |
| <span id="ProfileName"></span><span id="profilename"></span><span id="PROFILENAME"></span>**ProfileName**<br/>                                                                                     | O nome de exibição do perfil.<br/>                                                                                                                                                                                            |
| <span id="SkipMetadataTransfer"></span><span id="skipmetadatatransfer"></span><span id="SKIPMETADATATRANSFER"></span>**SkipMetadataTransfer**<br/>                                                 | Especifique 1 se os metadados não devem ser transferidos para o arquivo de saída ou 0 se os metadados devem ser transferidos. Equivalente ao atributo de [transferência de metadados do MF \_ transcodificar \_ Skip \_ \_ ](mf-transcode-skip-metadata-transfer.md) .<br/> |
| <span id="VideoBitrate"></span><span id="videobitrate"></span><span id="VIDEOBITRATE"></span>**VideoBitrate**<br/>                                                                                 | A média de taxa de bits de vídeo. Equivalente ao atributo [**de \_ \_ taxa de \_ bits média MF MT**](mf-mt-avg-bitrate-attribute.md) . <br/>                                                                                                        |
| <span id="VideoEncodeComplexity"></span><span id="videoencodecomplexity"></span><span id="VIDEOENCODECOMPLEXITY"></span>**VideoEncodeComplexity**<br/>                                             | Um valor específico de codec que define a qualidade de codificação. Equivalente ao atributo [ \_ \_ QUALITYVSSPEED de rescodificação MF](mf-transcode-qualityvsspeed.md) . <br/>                                                                      |
| <span id="VideoEncodingProfile"></span><span id="videoencodingprofile"></span><span id="VIDEOENCODINGPROFILE"></span>**VideoEncodingProfile**<br/>                                                 | Um valor específico de codec que define o perfil de vídeo. Equivalente ao atributo [ \_ \_ ENCODINGPROFILE de rescodificação MF](mf-transcode-encodingprofile.md) . <br/>                                                                     |
| <span id="VideoFormat"></span><span id="videoformat"></span><span id="VIDEOFORMAT"></span>**VideoFormat**<br/>                                                                                     | O subtipo de vídeo codificado. Equivalente ao atributo [**de \_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) .<br/>                                                                                                                  |
| <span id="VideoFrameHeight"></span><span id="videoframeheight"></span><span id="VIDEOFRAMEHEIGHT"></span>**VideoFrameHeight**<br/>                                                                 | A altura do vídeo de saída. Equivalente ao atributo [**de \_ \_ \_ tamanho de quadro MF MT**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                      |
| <span id="VideoFrameRateDenominator"></span><span id="videoframeratedenominator"></span><span id="VIDEOFRAMERATEDENOMINATOR"></span>**VideoFrameRateDenominator**<br/>                             | O denominador da taxa de quadros do vídeo de saída. Equivalente ao atributo [**de \_ \_ \_ taxa de quadros MF MT**](mf-mt-frame-rate-attribute.md) .<br/>                                                                               |
| <span id="VideoFrameRateNumerator"></span><span id="videoframeratenumerator"></span><span id="VIDEOFRAMERATENUMERATOR"></span>**VideoFrameRateNumerator**<br/>                                     | O numerador da taxa de quadros do vídeo de saída. Equivalente ao atributo [**de \_ \_ \_ taxa de quadros MF MT**](mf-mt-frame-rate-attribute.md) .<br/>                                                                                 |
| <span id="VideoFrameWidth"></span><span id="videoframewidth"></span><span id="VIDEOFRAMEWIDTH"></span>**VideoFrameWidth**<br/>                                                                     | A largura do vídeo de saída. Equivalente ao atributo [**de \_ \_ \_ tamanho de quadro MF MT**](mf-mt-frame-size-attribute.md) .<br/>                                                                                                       |
| <span id="VideoPixelAspectRatioDenominator"></span><span id="videopixelaspectratiodenominator"></span><span id="VIDEOPIXELASPECTRATIODENOMINATOR"></span>**VideoPixelAspectRatioDenominator**<br/> | O denominador da taxa de proporção de pixel (PAR) do vídeo de saída. Equivalente ao atributo [**de \_ \_ taxa de \_ proporção \_ MF MT pixel**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                               |
| <span id="VideoPixelAspectRatioNumerator"></span><span id="videopixelaspectrationumerator"></span><span id="VIDEOPIXELASPECTRATIONUMERATOR"></span>**VideoPixelAspectRatioNumerator**<br/>         | O numerador do PAR do vídeo de saída. Equivalente ao atributo [**de \_ \_ taxa de \_ proporção \_ MF MT pixel**](mf-mt-pixel-aspect-ratio-attribute.md) . <br/>                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




