---
description: Enumerações de API do codec
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Enumerações de API do codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c97da1fe45aba1d81e7036fa7ba6e75fc225a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919898"
---
# <a name="codec-api-enumerations"></a>Enumerações de API do codec



| Enumeração                                                                              | Descrição                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Especifica a configuração do alto-falante para os canais de áudio no fluxo de bits de áudio.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Especifica se o áudio é codificado em Dolby Surround.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Especifica se um decodificador AAC usa equações de downmix estéreo MPEG-2/MPEG-4.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Especifica se o fluxo de áudio de entrada é estéreo ou duplo mono.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Especifica como o decodificador Reproduz áudio mono duplo.                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Especifica o modo de controle de compactação para um fluxo de áudio Dolby AC-3.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Especifica se um decodificador AAC executa o controle de intervalo dinâmico.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Especifica como o fluxo de vídeo decodificado é entrelaçado.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Especifica o modo de desentrelaçamento de software de um decodificador de vídeo.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Especifica o nível de economia de energia de um decodificador de vídeo.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Especifica se a equalização de intensidade está habilitada em um decodificador de áudio ou em um processador de sinais digitais (DSP). |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Especifica se o preenchimento do orador está habilitado em um decodificador de áudio ou DSP.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.                                      |
| [**Enumeração eAVEncAudioInputContent**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Especifica se o conteúdo de áudio contém música ou voz.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Especifica o modo de controle de taxa.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Especifica se o codificador descarta grupos parciais de imagens (GOPS segundos) no final do fluxo.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Especifica o tipo de conversão de analógico para digital (A/D) para um fluxo de áudio Dolby Digital.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Especifica o perfil de controle de intervalo dinâmico em um fluxo de áudio Dolby Digital.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Especifica o modo de fone de ouvido para um fluxo de áudio Dolby Digital.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Especifica o modo de downmix de estéreo preferencial para um fluxo de áudio Dolby Digital.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Especifica o tipo de sala para um fluxo de áudio Dolby Digital.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Especifica o serviço de áudio contido em um fluxo de áudio Dolby Digital.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Especifica se um fluxo de áudio Dolby Digital é codificado no Dolby Digital Surround EX.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Especifica o intervalo nominal para uma fonte de vídeo.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Especifica o modo de codificação de áudio MPEG.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Especifica o tipo de filtro de ênfase que deve ser usado ao decodificar.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Especifica a camada de áudio MPEG.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Especifica se o codificador produz campos codificados ou quadros codificados.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Especifica a tabela de codificação de comprimento variável (VLC) a ser usada para codificação de entropia.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Especifica o perfil MPEG-2.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Especifica o perfil MPEG-2.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Especifica se a escala de quantizador é linear ou não linear.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Especifica o padrão de verificação de macrobloco.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Especifica como o codificador se comporta quando detecta uma nova cena.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Especifica o tipo de fluxo de saída produzido por um multiplexador.                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Especifica a resolução de croma.                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Especifica croma localizando.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Especifica as condições de iluminação pretendidas para exibir uma fonte de vídeo.                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Especifica o intervalo nominal para uma fonte de vídeo.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Especifica os primários de cor do vídeo.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Especifica a função de conversão de R'G'B ' para RGB.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Especifica a matriz de conversão do espaço de cores Y'Cb'Cr para o espaço de cores R'G'B.                  |
| [**eAVEncVideoFilmContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Especifica se a origem original do vídeo de entrada foi filme ou vídeo.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Especifica se o codificador converte a taxa de quadros.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Especifica como o codificador entrelaça o vídeo de saída.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Especifica se os quadros de entrada para um codificador são progressivos ou entrelaçados.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Especifica a velocidade de decodificação de vídeo.                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de codec](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
