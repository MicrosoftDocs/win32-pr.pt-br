---
description: Propriedades da API do codec
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Propriedades da API do codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06269591c8ddf087b83146ed72a62f4565b8340a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456491"
---
# <a name="codec-api-properties"></a>Propriedades da API do codec

-   [Propriedades de áudio comuns](#common-audio-properties)
-   [Propriedades comuns do decodificador](#common-decoder-properties)
-   [Propriedades comuns do codificador](#common-encoder-properties)
-   [Propriedades do decodificador de vídeo](#video-decoder-properties)
-   [Propriedades do decodificador de áudio](#audio-decoder-properties)
-   [Propriedades do codificador de vídeo](#video-encoder-properties)
-   [Propriedades do codificador de áudio](#audio-encoder-properties)
-   [Propriedades do codificador de vídeo MPEG](#mpeg-video-encoder-properties)
-   [Propriedades do codificador de áudio MPEG](#mpeg-audio-encoder-properties)
-   [Propriedades do decodificador de áudio Dolby Digital](#dolby-digital-audio-decoder-properties)
-   [Propriedades do codificador de áudio Dolby Digital](#dolby-digital-audio-encoder-properties)
-   [Propriedades do DSP (processamento de sinal digital)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Propriedades de áudio comuns

Essas propriedades se aplicam a codificadores de áudio e decodificadores de áudio.



| Propriedade                                                      | Descrição                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Obtém a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Obtém o número de canais no fluxo de bits de áudio.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Obtém a taxa de amostragem do fluxo de bits de áudio, em amostras por segundo.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Especifica se o áudio é codificado em Dolby Surround.                      |



 

### <a name="common-decoder-properties"></a>Propriedades comuns do decodificador

Essas propriedades se aplicam a decodificadores de áudio e decodificadores de vídeo.



| Propriedade                                                            | Descrição                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Especifica o formato de entrada atual para o decodificador.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Obtém a taxa de bits média atual do decodificador.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Especifica o formato de saída para o decodificador.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Especifica a classe do serviço do Agendador de classes de multimídia (MMCSS) para o thread de decodificação. |



 

### <a name="common-encoder-properties"></a>Propriedades comuns do codificador

Essas propriedades se aplicam a codificadores de áudio e codificadores de vídeo.



| Propriedade                                                                          | Descrição                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Especifica o esquema de codificação.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Especifica o nível inicial do buffer de codificação.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Especifica o nível final do buffer de codificação no final do processo de codificação.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Especifica o tamanho do buffer usado durante a codificação.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Especifica o formato de destino para um codificador.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Especifica se o fluxo de saída deve ser estruturado para que o fluxo codificado tenha uma latência de decodificação baixa. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Especifica a taxa máxima de bits.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Especifica a taxa média de bits.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Especifica o intervalo de tempo durante o qual a taxa de bits média se aplica.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Especifica a taxa mínima de bits.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Especifica o número de aprovações de codificação que o codificador suporta.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Inicia a primeira passagem de codificação.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Especifica o nível de qualidade para codificação.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Especifica a compensação entre a qualidade de codificação e a velocidade.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Especifica o modo de controle de taxa.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Especifica se o aplicativo requer desempenho de codificação em tempo real.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Especifica se o codificador descarta grupos parciais de imagens (GOPS segundos) no final do fluxo.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Especifica o tipo de fluxo de saída produzido por um multiplexador.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Especifica o número de passagens de codificação concluídas.                                                              |



 

### <a name="video-decoder-properties"></a>Propriedades do decodificador de vídeo



| Propriedade                                                                                | Descrição                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Habilita ou desabilita a aceleração de hardware para decodificação de vídeo H. 264.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Habilita ou desabilita a aceleração de hardware para decodificação de vídeo MPEG-2.            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Habilita ou desabilita a aceleração de hardware para decodificação de vídeo VC-1.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Especifica se o decodificador cai intra frames com quadros de referência ausentes. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Obtém ou define a velocidade de decodificação de vídeo.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Obtém o tamanho da imagem decodificada, em pixels.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Especifica como o fluxo de vídeo decodificado é entrelaçado.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Especifica a taxa de proporção de pixel do fluxo de vídeo decodificado.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Especifica o modo de desentrelaçamento de software do decodificador.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Especifica o nível de economia de energia.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Habilita ou desabilita o modo de geração de miniatura.                                  |



 

### <a name="audio-decoder-properties"></a>Propriedades do decodificador de áudio



| Propriedade                                                                        | Descrição                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Especifica se um decodificador AAC usa equações de downmix estéreo MPEG-2/MPEG-4 ou usa um downmix não padrão. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Especifica como o decodificador Reproduz áudio mono duplo.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Habilita ou desabilita o controle de intervalo dinâmico em um decodificador AAC.                                                           |



 

### <a name="video-encoder-properties"></a>Propriedades do codificador de vídeo



| Propriedade                                                                                        | Descrição                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Especifica o sistema de vídeo do conteúdo de origem.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Retorna o número de quadros de vídeo que foram codificados.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Retorna a taxa média de quadros do conteúdo do vídeo.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Retorna o número de quadros de vídeo recebidos pelo codificador.                                                         |
| [**AVEncVideoCBRMotionTradeoff**](avencvideocbrmotiontradeoff-property.md)                     | Especifica a compensação entre o movimento e as imagens ainda.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Especifica o tamanho das unidades de acesso ao vídeo.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Especifica qual campo é exibido primeiro.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Especifica o tamanho do fluxo de vídeo quando ele é decodificado.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Especifica a largura e a altura do vídeo codificado, se o vídeo for cortado.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Especifica os cantos esquerdo e superior do retângulo de recorte, se o vídeo for cortado.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Inverte a ordem dos campos entrelaçados no vídeo de origem.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Especifica se os quadros de entrada são progressivos ou entrelaçados.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Especifica o valor do sinalizador de descarte de quadros no cabeçalho GOP.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Especifica o número do quadro inicial no cabeçalho GOP.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Especifica o número de hora inicial no cabeçalho GOP.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Especifica o número de minutos inicial no cabeçalho GOP.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Especifica o segundo número inicial no cabeçalho GOP.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Especifica a resolução de croma do vídeo de entrada.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Especifica o croma localizando para o vídeo de entrada.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Especifica as condições de iluminação pretendidas para exibir o vídeo de entrada.                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | Especifica o intervalo nominal para o vídeo de entrada.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Especifica os primários de cor para o vídeo de entrada.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Especifica a função de conversão de RGB para R'G'B ' para vídeo de entrada                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Especifica a matriz de conversão do espaço de cores Y'Cb'Cr para o espaço de cores R'G'B para o vídeo de entrada.         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | Especifica se o codificador executa o telecineon inverso.                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | Define o limite no qual o codificador considera um campo de vídeo redundante.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Especifica o número máximo de quadros entre quadros-chave.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Especifica o número de campos a serem codificados.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Especifica o número de campos a serem ignorados durante a codificação.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Especifica a resolução de croma do vídeo codificado.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Especifica o croma localizando para o vídeo codificado.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Especifica as condições de iluminação pretendidas para exibir o vídeo codificado.                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | Especifica o intervalo nominal para o vídeo codificado.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Especifica os primários de cor para o vídeo codificado.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Especifica a função de conversão de RGB para R'G'B ' para vídeo codificado.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Especifica a matriz de conversão do espaço de cores Y'Cb'Cr para o espaço de cores R'G'B para o vídeo codificado.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Especifica a taxa de quadros no fluxo de saída do codificador, em quadros por segundo.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Especifica se o codificador converte a taxa de quadros quando a taxa de quadros de saída não corresponde à taxa de quadros de entrada. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Especifica como o codificador entrelaça o vídeo de saída.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Especifica a taxa de proporção de pixel.                                                                                     |
| [**AVEncVideoSourceFilmContent**](avencvideosourcefilmcontent-property.md)                     | Especifica se a origem original do vídeo de entrada foi filme ou vídeo.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Especifica se o vídeo é monocromático (preto e branco) ou contém a cor.                                        |



 

### <a name="audio-encoder-properties"></a>Propriedades do codificador de áudio



| Propriedade                                                                        | Descrição                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Especifica se o conteúdo de áudio contém música ou voz.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Especifica o número de amostras de áudio a serem codificadas.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Especifica o número de amostras de áudio para o codificador ignorar.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Especifica qual canal de áudio é mapeado para o canal *N* no fluxo de áudio codificado. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Especifica a taxa média de bits do fluxo de áudio codificado.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Retorna a média de bits por segundo do áudio codificado.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Retorna o nível médio de volume do conteúdo de áudio.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Retorna o nível de volume mais alto que estava presente no conteúdo de áudio.             |



 

### <a name="mpeg-video-encoder-properties"></a>Propriedades do codificador de vídeo MPEG



| Propriedade                                                                                    | Descrição                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Especifica se o codificador adiciona um código de extremidade de sequência ao final do fluxo.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Especifica o número padrão de quadros B consecutivos entre quadros I e P.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Especifica se o codificador produz campos codificados ou quadros codificados.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Especifica se o codificador gera cabeçalhos de extensão de exibição de imagem.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Especifica se o codificador gera cabeçalhos de extensão de imagem.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Especifica se o codificador gera cabeçalhos de extensão de exibição de sequência.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Especifica se o codificador gera cabeçalhos de extensão de sequência.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Especifica se o codificador gera cabeçalhos de extensão escalonáveis de sequência.         |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                         | Especifica se o codificador produz GOPS segundos aberto ou fechado GOPS segundos.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Especifica o número de GOPS segundos entre cabeçalhos de sequência.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Especifica o número máximo de imagens de um cabeçalho GOP para o próximo cabeçalho GOP. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Especifica a precisão dos coeficientes de DC.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Especifica a tabela de codificação de comprimento variável (VLC) a ser usada para codificação de entropia.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Especifica o nível MPEG-2.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Especifica o perfil MPEG-2.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Especifica se a escala de quantizador é linear ou não linear.                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | Especifica a matriz de quantização croma para intra macroblocos.                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Especifica a matriz de quantização croma para não-intra macroblocos.                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Especifica a matriz de quantização Luma para intra macroblocos.                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Especifica a matriz de quantização Luma para não-intra macroblocos.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Especifica o padrão de verificação de macrobloco.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Especifica como o codificador se comporta quando detecta uma nova cena.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Especifica se o codificador usa vetores de movimento de ocultação.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>Propriedades do codificador de áudio MPEG



| Propriedade                                                                                  | Descrição                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Especifica o modo de codificação de áudio MPEG-1.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Especifica a configuração padrão para o bit de direitos autorais.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Especifica o tipo de filtro de ênfase que deve ser usado ao decodificar.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Especifica a camada de áudio MPEG.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Especifica a configuração padrão para o bit original.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Define o valor do bit de usuário privado.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Propriedades do decodificador de áudio Dolby Digital



| Propriedade                                                                      | Descrição                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Especifica o recorte de alto nível quando o decodificador executa o controle de intervalo dinâmico.  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Especifica o aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Especifica o modo de controle de compactação.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Propriedades do codificador de áudio Dolby Digital



| Propriedade                                                                                        | Descrição                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | Especifica o tipo de conversão de analógico para digital (A/D).                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Especifica o nível de downmix Center.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Especifica se um filtro de passagem baixa é aplicado aos canais de entrada principais.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Especifica o sinalizador de direitos autorais.                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Especifica se um filtro de alta passagem de bloqueio de DC é aplicado.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Especifica o nível de normalização da caixa de diálogo.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Especifica se a remoção de ênfase digital.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Especifica o perfil de controle de intervalo dinâmico.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Especifica o modo de fone de ouvido.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Especifica se um filtro de passagem baixa é aplicado ao canal de baixo efeito de frequência (LFE). |
| [**AVEncDDLoRoCenterMixLvl \_ x**](avencddlorocentermixlvl-x10-property.md)                    | Especifica a mudança de nível que é aplicada ao canal central para downmixing de lo/ro.     |
| [**AVEncDDLoRoSurroundMixLvl \_ x**](avencddlorosurroundmixlvl-x10-property.md)                | Especifica a mudança de nível que é aplicada aos canais surround para downmixing de lo/ro.  |
| [**AVEncDDLtRtCenterMixLvl \_ x**](avencddltrtcentermixlvl-x10-property.md)                    | Especifica a mudança de nível que é aplicada ao canal central para lt/RT downmixing.     |
| [**AVEncDDLtRtSurroundMixLvl \_ x**](avencddltrtsurroundmixlvl-x10-property.md)                | Especifica a mudança de nível que é aplicada aos canais surround para lt/RT downmixing.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Especifica o sinalizador fragmentado original.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Especifica o modo de downmix de estéreo preferencial.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Especifica o sinalizador de informações de produção de áudio.                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Especifica o nível de combinação.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Especifica o tipo de sala.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Especifica a configuração de proteção de sobremodulação RF.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Especifica o serviço de áudio.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Especifica se os canais surround são atenuados antes da codificação.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Especifica se uma mudança de fase de 90 graus é aplicada aos canais surround.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Especifica o nível de combinação subjacente.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Especifica se o fluxo de áudio é codificado em surround EX.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Propriedades do DSP (processamento de sinal digital)



| Propriedade                                                                | Descrição                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | Habilita ou desabilita a equalização de intensidade |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Habilita ou desabilita o preenchimento do alto-falante          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de codec](codec-api-reference.md)
</dt> </dl>

 

 



