---
title: Funções XAudio2
description: Esta seção contém informações sobre as funções fornecidas pela API do Microsoft XAudio2.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b950ce33f55a4b834f3ee7a068f613e144c2e30633c67e887b8a24789140a618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109646"
---
# <a name="xaudio2-functions"></a>Funções XAudio2

Esta seção contém informações sobre as funções fornecidas pela API do Microsoft XAudio2.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                       | Descrição                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Cria uma instância do efeito [xapofx](xapofx-overview.md) solicitado.<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Cria uma instância da interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) para processamento HRTF (função de transferência relacionada à carga).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Função embutida que converte parâmetros de I3DL2 (diretrizes de renderização de áudio 3D interativo nível 2,0) para parâmetros XAudio2 nativos.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Calcula as configurações do DSP com relação aos parâmetros 3D.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Define todas as constantes de áudio 3D globais.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Função embutida que converte um valor de taxa de amplitude em um valor de decibéi.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Cria um novo objeto **XAudio2** e retorna um ponteiro para sua interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Cria um novo objeto de processamento de áudio de reverberação (APO) e retorna um ponteiro para ele.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Cria um novo objeto de processamento de áudio de medidor de volume (APO) e retorna um ponteiro para ele.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Função embutida que converte de frequências de corte de filtro expressas em Hertz para os coeficientes de filtro usados com o membro **Frequency** da estrutura de [**\_ \_ parâmetros de filtro XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Função embutida que converte de frequências de corte de filtro expressas em Hertz para os valores de frequência de radianos usados no membro **Frequency** da estrutura de [**\_ \_ parâmetros de filtro XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Função embutida que converte um valor decibéi em um valor de taxa de amplitude.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Função embutida que converte um valor de taxa de frequência em um valor semitone.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Função embutida que converte das frequências de radianos usadas nos [**\_ \_ parâmetros de filtro XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) de volta para frequências absolutas em Hertz.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Função embutida que converte um valor de semitone para um valor de taxa de frequência.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[XAudio2: referência de rogramming de:P](programming-reference.md)
</dt> </dl>

 

 




