---
description: Este tópico descreve o controle de volume e tom XAudio2.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Controle de volume e tom XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6376ad599b496a640b49d7eb539e1da774e31c71a3bf2a8e0c863fc140e19b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962485"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Controle de volume e tom XAudio2

Este tópico descreve o controle de volume e tom XAudio2.

## <a name="volume-control"></a>Controle de volume

Os níveis de volume são expressos como multiplicadores de amplitude de ponto flutuante entre -XAUDIO2 MAX VOLUME LEVEL e \_ \_ \_ XAUDIO2 MAX VOLUME LEVEL (-224 a 224), com um ganho máximo de \_ \_ \_ 144,5 dB. Um volume de 1,0 significa que não há atenuação ou ganho; 0 significa silêncio; e níveis negativos podem ser usados para inverter a fase do áudio. Duas funções em linha são fornecidas em XAudio2.h para converter entre unidades de volume: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) e [**XAudio2AmplitudeRatioToDecibels.**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)

Você pode aplicar um nível de volume ao áudio em vários pontos à medida que ele flui pelo grafo XAudio2:

-   Todos os tipos de voz aplicam um nível de volume geral à entrada, que eles controlam usando o método [**IXAudio2Voice::SetVolume.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) Em vozes de submix e mestre, o nível de volume geral é aplicado logo antes da cadeia de filtros e efeito integrados da voz. Em vozes de origem, o nível de volume geral é aplicado após a cadeia interna de filtros e efeitos da voz.
-   As vozes aplicam um nível de volume por canal à saída, que elas controlam usando o método [**IXAudio2Voice::SetChannelVolumes.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) O nível de volume por canal é aplicado logo após a conversão final da taxa de amostragem da voz e antes de ser enviado para outras vozes.
-   Cada conexão entre uma voz e outra tem uma tabela de níveis usada para enviar áudio de cada canal de origem para cada canal de destino, que é controlada usando o método [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)

Todos os volumes gerais e volumes de canais assumem como padrão 1.0 inicialmente. Todas as matrizes de nível de envio assumem como padrão os valores apropriados que preservam a potência do sinal e o posicionamento do canal da maneira mais precisa possível. Confira a Visão geral do Mapeamento [de Canal Padrão XAudio2](xaudio2-default-channel-mapping.md) para obter detalhes.

> [!Note]  
> O XAudio2 ajusta automaticamente os níveis de volume com base nas configurações do locutor do usuário para manter um nível de volume consistente entre as configurações. Se as configurações do usuário não corresponderem à configuração física, o volume será muito alto ou muito suave em comparação com um sistema com configurações precisas. Por exemplo, um sistema configurado para alto-falantes de som surround 5.1 que tem apenas dois alto-falantes conectados soa muito suave. O XAudio2 não consegue detectar se as configurações do locutor do usuário corresponderão corretamente à sua configuração física.

 

## <a name="pitch-control"></a>Controle de tom

Os lançamentos são expressos como taxa de entrada/taxa de saída entre 1/1.024 e 1.024/1, inclusive. Uma taxa de 1/1.024 reduz o tom em 10 octaves, enquanto uma taxa de 1.024/1 a eleva em 10 octaves. Você só pode usar o método [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar ajustes de tom às vozes de origem e somente se elas não foram criadas com o sinalizador NOPITCH de VOZ XAUDIO2. \_ \_ A taxa de frequência padrão é 1/1: ou seja, nenhuma alteração de tom. Duas funções em linha são fornecidas em XAudio2.h para converter entre taxas de frequência e semitons: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) e [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de volume e tom](volume-and-pitch-control.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como alterar o tom de voz](how-to--change-voice-pitch.md)
</dt> <dt>

[Como alterar o volume de voz](how-to--change-voice-volume.md)
</dt> </dl>

 

 
