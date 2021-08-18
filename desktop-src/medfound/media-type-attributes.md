---
description: Atributos de tipo de mídia
ms.assetid: e84ba3f6-4857-4340-baca-5847650ea7b8
title: Atributos de tipo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52e906baa7bbac14d33dbc263e3a1edfa43b65851d96d0573032784c0149425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827456"
---
# <a name="media-type-attributes"></a>Atributos de tipo de mídia

Os atributos a seguir se aplicam aos tipos de mídia. Alguns desses atributos destinam-se apenas à conversão de formatos de tipo de mídia herdados em tipos de mídia Media Foundation.

## <a name="general-format-attributes"></a>Atributos de formato geral

Esses atributos podem ser aplicados a todos os tipos de mídia.



| Atributo                                                                            | Descrição                                                                            |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**](mf-mt-all-samples-independent-attribute.md) | Especifica se cada amostra é independente dos outros exemplos no fluxo.       |
| [**\_tipo de formato MF MT \_ am \_ \_**](mf-mt-am-format-type-attribute.md)                   | GUID de formato.                                                                           |
| [**MF \_ MT \_ compactado**](mf-mt-compressed-attribute.md)                             | Especifica se os dados de mídia estão compactados                                         |
| [**\_amostras de \_ \_ tamanho fixo MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           | Especifica se os exemplos têm um tamanho fixo.                                       |
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                            | GUID de tipo principal.                                                                       |
| [**tamanho de amostra do MF \_ MT \_ \_**](mf-mt-sample-size-attribute.md)                          | Tamanho de cada amostra, em bytes.                                                         |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                   | GUID de subtipo.                                                                          |
| [**dados de usuário do MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                              | Contém dados de usuário para um tipo de mídia que foi convertido de uma estrutura de formato herdado. |
| [**\_ \_ tipo empacotado do MF MT \_**](mf-mt-wrapped-type-attribute.md)                        | Contém um tipo de mídia que foi encapsulado em outro tipo de mídia.                     |



 

## <a name="audio-format-attributes"></a>Atributos de formato de áudio

Esses atributos podem ser aplicados a tipos de mídia cujo tipo principal é igual a MFMediaType \_ áudio.



| Atributo                                                                                            | Descrição                                                                                 |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [\_indicação de \_ \_ nível de \_ perfil de áudio \_ \_ MF MT AAC](mf-mt-aac-audio-profile-level-indication.md)       | Especifica o perfil de áudio e o nível de um fluxo AAC (codificação de áudio avançado).             |
| [\_tipo de conteúdo MF MT \_ AAC \_ \_](mf-mt-aac-payload-type.md)                                             | Especifica o tipo de carga para um fluxo AAC (codificação de áudio avançado).                       |
| [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)         | Número médio de bytes por segundo.                                                         |
| [**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md)                    | Número de bits por amostra de áudio.                                                            |
| [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)                     | Alinhamento de bloco, em bytes.                                                                  |
| [**\_máscara de \_ canal de áudio MF MT \_ \_**](mf-mt-audio-channel-mask-attribute.md)                           | Especifica a atribuição de canais de áudio a posições do orador.                            |
| [**\_ \_ amostras float de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-float-samples-per-second-attribute.md) | Número de amostras de áudio por segundo (valor de ponto flutuante).                                  |
| [**\_matriz de \_ áudio \_ FOLDDOWN MF MT \_**](mf-mt-audio-folddown-matrix-attribute.md)                     | Especifica como um decodificador de áudio deve transformar áudio de multicanal em saída de estéreo.        |
| [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                           | Número de canais de áudio.                                                                   |
| [**\_áudio MF \_ MT \_ preferir \_ WAVEFORMATEX**](mf-mt-audio-prefer-waveformatex-attribute.md)             | Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio. |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ bloco**](mf-mt-audio-samples-per-block-attribute.md)                | Número de amostras de áudio contidas em um bloco compactado de dados de áudio.                    |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)              | Número de amostras de áudio por segundo (valor inteiro).                                         |
| [**\_áudio MF \_ MT \_ \_ bits válidos \_ por \_ amostra**](mf-mt-audio-valid-bits-per-sample-attribute.md)       | Número de bits válidos de dados de áudio em cada amostra de áudio.                                    |
| [**\_áudio MF \_ MT \_ WMADRC \_ AVGREF**](mf-mt-audio-wmadrc-avgref-attribute.md)                         | nível de volume médio de referência de um Windows arquivo de áudio de mídia.                               |
| [**\_áudio MF \_ MT \_ WMADRC \_ AVGTARGET**](mf-mt-audio-wmadrc-avgtarget-attribute.md)                   | nível de volume médio de destino de um Windows arquivo de áudio de mídia.                                  |
| [**\_áudio MF \_ MT \_ WMADRC \_ PEAKREF**](mf-mt-audio-wmadrc-peakref-attribute.md)                       | faça referência ao nível de volume de pico de um arquivo de áudio de mídia Windows.                                  |
| [**\_áudio MF \_ MT \_ WMADRC \_ PEAKTARGET**](mf-mt-audio-wmadrc-peaktarget-attribute.md)                 | nível de volume de pico de destino de um arquivo de áudio de mídia Windows.                                     |
| [\_marca de \_ \_ formato Wave \_ original \_ MF MT](mf-mt-original-wave-format-tag.md)                            | Contém a marca de formato WAVE original para um fluxo de áudio.                                  |



 

## <a name="video-format-attributes"></a>Atributos de formato de vídeo

Esses atributos podem ser aplicados a tipos de mídia cujo tipo principal é igual a MFMediaType \_ vídeo.



| Atributo                                                                              | Descrição                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_taxa de \_ \_ erros de \_ bit \_ do MF MT**](mf-mt-avg-bit-error-rate-attribute.md)            | Taxa de erros de dados.                                                                                                                        |
| [**\_taxa de \_ \_ bits média de MF MT**](mf-mt-avg-bitrate-attribute.md)                            | Taxa de dados aproximada do fluxo de vídeo.                                                                                              |
| [**\_ \_ \_ primários de vídeo \_ personalizado MF MT**](mf-mt-custom-video-primaries-attribute.md)     | Primárias de cores personalizadas.                                                                                                                 |
| [**\_ \_ Stride padrão MF \_ MT**](mf-mt-default-stride-attribute.md)                      | Stride de superfície padrão.                                                                                                                 |
| [**sinalizadores de DRM do MF \_ MT \_ \_**](mf-mt-drm-flags-attribute.md)                                | Especifica se o vídeo requer a imposição da proteção de cópia.                                                                         |
| [**\_taxa de \_ quadros MF MT \_**](mf-mt-frame-rate-attribute.md)                              | Taxa de quadros.                                                                                                                             |
| [intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ máx.](mf-mt-frame-rate-range-max.md)                      | A taxa máxima de quadros suportada por um dispositivo de captura de vídeo.                                                                             |
| [intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md)                      | A taxa mínima de quadros suportada por um dispositivo de captura de vídeo.                                                                             |
| [**\_tamanho do \_ quadro MF MT \_**](mf-mt-frame-size-attribute.md)                              | Largura e altura do quadro de vídeo.                                                                                                    |
| [**\_ \_ abertura geométrica do MF MT \_**](mf-mt-geometric-aperture-attribute.md)              | Abertura geométrica.                                                                                                                     |
| [**\_modo de \_ entrelaçamento do MF MT \_**](mf-mt-interlace-mode-attribute.md)                      | Descreve como os quadros são entrelaçados.                                                                                                |
| [**\_ \_ \_ espaçamento do quadro-chave máximo MF MT \_**](mf-mt-max-keyframe-spacing-attribute.md)         | Número máximo de quadros de um quadro-chave para o próximo.                                                                                |
| [**\_abertura de \_ \_ exibição mínima \_ de MF MT**](mf-mt-minimum-display-aperture-attribute.md) | Abertura de exibição mínima.                                                                                                               |
| [**cabeçalho de sequência do MF \_ MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)         | Cabeçalho de sequência MPEG-1 ou MPEG-2.                                                                                                       |
| [**código de hora de início do MF \_ MT \_ MPEG \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md)        | Código de hora de início do grupo de imagens (GOP).                                                                                                |
| [**Sinalizadores de MPEG2 do MF \_ MT \_ \_**](mf-mt-mpeg2-flags-attribute.md)                            | Sinalizadores diversos para vídeo MPEG-2.                                                                                                   |
| [**Nível de MPEG2 do MF \_ MT \_ \_**](mf-mt-mpeg2-level-attribute.md)                            | Nível MPEG-2 ou H. 264.                                                                                                                  |
| [**\_Perfil MF \_ MT \_**](mf-mt-mpeg2-profile-attribute.md)                        | Perfil MPEG-2 ou H. 264.                                                                                                                |
| [\_ \_ 4cc original MF \_ MT](mf-mt-original-4cc.md)                                        | Contém o codec original FOURCC para um fluxo de vídeo.                                                                                  |
| [**\_sinalizadores de \_ controle de pad MF MT \_ \_**](mf-mt-pad-control-flags-attribute.md)               | Taxa de proporção do retângulo de saída.                                                                                                   |
| [**\_paleta MF MT \_**](mf-mt-palette-attribute.md)                                     | Entradas da paleta.                                                                                                                        |
| [**\_abertura de \_ digitalização de Pan MT \_ MF \_**](mf-mt-pan-scan-aperture-attribute.md)               | Define a região de vídeo de 4 × 3 que deve ser exibida no modo de panorâmica/digitalização.                                                              |
| [**\_exame de Pan MT do MF \_ \_ \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md)                 | Especifica se o modo de panorâmica/verificação está habilitado.                                                                                             |
| [**taxa de proporção de pixel do MF \_ MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)             | Taxa de proporção de pixel.                                                                                                                     |
| [**\_dica de \_ conteúdo de origem MF MT \_ \_**](mf-mt-source-content-hint-attribute.md)           | Taxa de proporção pretendida.                                                                                                                  |
| [**função de transferência do MF \_ MT \_ \_**](mf-mt-transfer-function-attribute.md)                | Função de conversão de RGB para R'G'B '.                                                                                                 |
| [\_ \_ Vídeo 3D MF \_ MT](mf-mt-video-3d.md)                                                | Especifica se um fluxo de vídeo contém conteúdo 3D.                                                                                   |
| [**\_vídeo MF \_ MT \_ croma \_ localizando**](mf-mt-video-chroma-siting-attribute.md)           | Descreve como o croma foi amostrado para o vídeo de Y'Cb'Cr.                                                                                    |
| [**\_iluminação de \_ vídeo MF MT \_**](mf-mt-video-lighting-attribute.md)                      | Condições de iluminação ideais para exibição.                                                                                                |
| [**\_ \_ intervalo nominal de vídeo MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md)           | Intervalo nominal das informações de cor                                                                                                  |
| [**\_ \_ primários de vídeo MF MT \_**](mf-mt-video-primaries-attribute.md)                    | Primárias de cores.                                                                                                                        |
| [\_rotação de \_ vídeo MF MT \_](mf-mt-video-rotation.md)                                    | Especifica a rotação de um quadro de vídeo na direção do sentido anti-horário.                                                             |
| [**\_ \_ matriz YUV do MF MT \_**](mf-mt-yuv-matrix-attribute.md)                              | Matriz de conversão do espaço de cores Y'Cb'Cr para o espaço de cores R'G'B.                                                              |
| [o \_ chamador XVP do MF \_ \_ aloca a \_ saída](mf-xvp-caller-allocates-output.md)               | Especifica se o chamador vai alocar as texturas usadas para a saída pela [**MFT do processador de vídeo**](video-processor-mft.md). |
| [MF \_ XVP \_ desabilitar \_ FRC](mf-xvp-disable-frc.md)                                        | Desabilita a conversão de taxa de quadros na [**MFT do processador de vídeo**](video-processor-mft.md).                                               |



 

## <a name="other-format-attributes"></a>Outros atributos de formato

Os atributos a seguir se aplicam ao vídeo intercalado do DV.



| Atributo                                                                      | Descrição                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MF \_ MT \_ DV \_ AAUX \_ Ctrl \_ Pack \_ 0**](mf-mt-dv-aaux-ctrl-pack-0-attribute.md) | Pacote de controle do código-fonte auxiliar de áudio (AAUX) para o primeiro bloco de áudio. |
| [**MF \_ MT \_ DV \_ AAUX \_ Ctrl \_ Pack \_ 1**](mf-mt-dv-aaux-ctrl-pack-1-attribute.md) | Pacote de controle do código-fonte AAUX para o segundo bloco de áudio.                  |
| [**MF \_ MT \_ DV \_ AAUX \_ src \_ Pack \_ 0**](mf-mt-dv-aaux-src-pack-0-attribute.md)   | AAUX o pacote de origem para o primeiro bloco de áudio.                           |
| [**MF \_ MT \_ DV \_ AAUX \_ src \_ Pack \_ 1**](mf-mt-dv-aaux-src-pack-1-attribute.md)   | AAUX o pacote de origem para o segundo bloco de áudio.                          |
| [**pacote do MF \_ MT \_ DV \_ Vaux \_ Ctrl \_**](mf-mt-dv-vaux-ctrl-pack-attribute.md)      | Pacote de controle do código-fonte do VAUX (vídeo Auxiliary).                           |
| [**\_pacote de origem MF MT \_ DV \_ Vaux \_ \_**](mf-mt-dv-vaux-src-pack-attribute.md)        | VAUX o pacote de origem.                                                     |



 

Os atributos a seguir se aplicam aos arquivos ASF (Advanced Streaming Format).



| Atributo                                                      | Descrição                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [\_ \_ formato ARBITRÁRIO do MF MT \_](mf-mt-arbitrary-format.md)        | Dados de formato adicionais para um fluxo binário em um arquivo ASF.       |
| [\_ \_ cabeçalho ARBITRÁRIO do MF MT \_](mf-mt-arbitrary-header.md)        | Dados específicos de tipo para um fluxo binário em um arquivo ASF.           |
| [\_tolerante a \_ perdas de imagem MF MT \_ \_](mf-mt-image-loss-tolerant.md) | Especifica se um fluxo de imagem ASF é um tipo de JPEG degradado. |



 

Os atributos a seguir se aplicam a arquivos MPEG-4.



| Atributo                                                                     | Descrição                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [\_Entrada de \_ \_ exemplo atual \_ \_ do MF MT MPEG4](mf-mt-mpeg4-current-sample-entry.md) | O índice da entrada atual na caixa de descrição de exemplo. |
| [\_Descrição de \_ exemplo de MPEG4 \_ \_ do MF MT](mf-mt-mpeg4-sample-description.md)      | A caixa de descrição de exemplo.                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 



