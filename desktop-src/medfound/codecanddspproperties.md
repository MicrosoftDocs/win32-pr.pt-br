---
description: Constantes Codec e DSP IPropertyBag.
ms.assetid: 078b0eea-16dd-4427-b984-9e52a43de559
title: Constantes Codec e DSP IPropertyBag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a6aa7d9b597b797cb242e3656d8f9f6b36a28ed1a3bec8648dea0674e33039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959136"
---
# <a name="codec-and-dsp-ipropertybag-constants"></a>Constantes Codec e DSP IPropertyBag

Há dois métodos para definir propriedades nos objetos codec e DSP programaticamente, usando a interface **IPropertyBag** ou a interface **IPropertyStore.** As propriedades mais comuns estão disponíveis por meio de ambas as interfaces. O uso da interface **IPropertyStore** é preferencial em vez **de IPropertyBag.**



| Constante de cadeia de caracteres IPropertyBag          | Chave de propriedade IPropertyStore                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| g \_ wszAvgFrameRate                    | [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md)                               |
| g \_ wszWMACAvgBytesPerSecond           | [MFPKEY \_ WMAENC \_ AVGBYTESPERSEC](mfpkey-wmaenc-avgbytespersecproperty.md)                          |
| g \_ wszWMACDRCSetting                  | [MFPKEY \_ WKEY \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md)                                        |
| g \_ wszWMACHiResOutput                 | [MFPKEY \_ WALTC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md)                                |
| g \_ wszWMACMusicSpeechClassMode        | [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) |
| g \_ wszWMACOriginalWaveFormat          | [MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT](mfpkey-wmaenc-origwaveformatproperty.md)                          |
| g \_ wszWMACSpeakerConfig               | [\_SPKRCFG MFPKEY \_ WIÇOC](mfpkey-wmadec-spkrcfgproperty.md)                                        |
| g \_ wszWMACVoiceBuffer                 | [Buffer ENC MFPKEY \_ \_ WMAVOICEWindow \_](mfpkey-wmavoice-enc-bufferwindowproperty.md)                 |
| g \_ wszWMACVoiceBuffer                 | [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md)                                   |
| g \_ wszWMADRCAverageReference          | [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)                                          |
| g \_ wszWMADRCAverageTarget             | [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)                                    |
| g \_ wszWMADRCPeakReference             | [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)                                        |
| g \_ wszWMADRCPeakTarget                | [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)                                  |
| g \_ wszWMCPAudioVBRQuality             | [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszWMCPAudioVBRSupported           | [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszWMCPMaxPasses                   | [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszWMVCAvgBitrate                  | [MFPKEY \_ LTDG](mfpkey-ravgproperty.md)                                                             |
| g \_ wszWMVCBAvg                        | [MFPKEY \_ BAVG](mfpkey-bavgproperty.md)                                                             |
| g \_ wszWMVCBDeltaQP                    | [MFPKEY \_ BDELTAQP](mfpkey-bdeltaqpproperty.md)                                                     |
| g \_ wszWMVCBMax                        | [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)                                                             |
| g \_ wszWMVCBufferFullnessInFirstByte   | [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)                   |
| g \_ wszWMVCCodedFrames                 | [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)                                               |
| g \_ wszWMVCComplexityEx                | [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md)                                             |
| g \_ wszWMVCComplexityMode              | [COMPLEXIDADE DE \_ MFPKEY](mfpkey-complexityproperty.md)                                                 |
| g \_ wszWMVCCompressionOptimizationType | [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md)               |
| g \_ wszWMVCCrisp                       | [MFPKEY \_ CRISP](mfpkey-crispproperty.md)                                                           |
| g \_ wszWMVCDecoderComplexityProfile    | [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md)                     |
| g \_ wszWMVCDecoderComplexityRequested  | [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md)                 |
| g \_ wszWMVCDecoderDeinterlacing        | [DECODIFICADOR MFPKEY \_ \_ DEINTERLACING](mfpkey-decoder-deinterlacingproperty.md)                          |
| g \_ wszWMVCDenoiseOption               | [MFPKEY \_ DENOISEOPTION](mfpkey-denoiseoptionproperty.md)                                           |
| g \_ wszWMVCEndOfPass                   | [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md)                                                   |
| g \_ wszWMVCForceFrameHeight            | [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md)                                     |
| g \_ wszWMVCForceFrameWidth             | [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md)                                       |
| g \_ wszWMVCForceMedianSetting          | [MFPKEY \_ FORCEMEDIANSETTING](mfpkey-forcemediansettingproperty.md)                                 |
| g \_ wszWMVCVCVCCC                      | [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md)                                                         |
| g \_ wszWMVCInterlacedCodingEnabled     | [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md)                       |
| g \_ wszWMVCLookAhead                   | [MFPKEY \_ LOOKAHEAD](mfpkey-lookaheadproperty.md)                                                   |
| g \_ wszWMVCLoopFilter                  | [MFPKEY \_ LOOPFILTER](mfpkey-loopfilterproperty.md)                                                 |
| g \_ wszWMVCMacroblockModeCostMethod    | [MFPKEY \_ MACROBLOCKMODECOSTMETHOD](mfpkey-macroblockmodecostmethodproperty.md)                     |
| g \_ wszWMVCMaxBitrate                  | [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)                                                             |
| g \_ wszWMVCMotionMatchMethod           | [MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)                                   |
| g \_ wszWMVCMotionSearchLevel           | [MFPKEY \_ MOTIONSEARCHLEVEL](mfpkey-motionsearchlevelproperty.md)                                   |
| g \_ wszWMVCMotionSearchRange           | [MFPKEY \_ MOTIONSEARCHRANGE](mfpkey-motionsearchrangeproperty.md)                                   |
| g \_ wszWMVCNoiseEdgeRemoval            | [MFPKEY \_ NOISEEDGEREMOVAL](mfpkey-noiseedgeremovalproperty.md)                                     |
| g \_ wszWMVCNumThreads                  | [MFPKEY \_ NUMTHREADS](mfpkey-numthreadsproperty.md)                                                 |
| g \_ wszWMVCPassesRecommended           | [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszWMVCPassesUsed                  | [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md)                                                 |
| g \_ wszWMVCPerceptualOptLevel          | [MFPKEY \_ PERCEPTUATUATLEVEL](mfpkey-perceptualoptlevelproperty.md)                                 |
| g \_ wszWMVCProduceDummyFrames          | [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md)                                 |
| g \_ wszWMVCRangeRedux                  | [MFPKEY \_ RANGEREDUX](mfpkey-rangereduxproperty.md)                                                 |
| g \_ wszWMVCTotalFrames                 | [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)                                               |
| g \_ wszWMVCVBREnabled                  | [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszWMVCVBRQuality                  | [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszWMVCVideoScaling                | [MFPKEY \_ VIDEOSCALING](mfpkey-videoscalingproperty.md)                                             |
| g \_ wszWMVCVType                       | [MFPKEY \_ VTYPE](mfpkey-vtypeproperty.md)                                                           |
| g \_ wszWMVCZeroByteFrames              | [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md)                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 



