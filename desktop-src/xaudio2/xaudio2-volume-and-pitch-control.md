---
description: Este tópico descreve o controle de volume e de densidade XAudio2.
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: Controle de volume e densidade XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2526cfa50c0260e90e1aae9e2bce21d507dc2e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170437"
---
# <a name="xaudio2-volume-and-pitch-control"></a>Controle de volume e densidade XAudio2

Este tópico descreve o controle de volume e de densidade XAudio2.

## <a name="volume-control"></a>Controle de volume

Os níveis de volume são expressos como multiplicadores de amplitude de ponto flutuante entre o \_ nível máximo de volume-XAudio2 \_ \_ e \_ \_ o nível de volume máximo XAUDIO2 \_ (-224 a 224), com um máximo de lucro de 144,5 dB. Um volume de 1,0 significa que não há atenuação ou lucro; 0 significa silêncio; e os níveis negativos podem ser usados para inverter a fase de áudio. Duas funções embutidas são fornecidas em XAudio2. h para converter entre unidades de volume: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) e [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).

Você pode aplicar um nível de volume ao áudio em vários pontos conforme ele flui pelo grafo XAudio2:

-   Todos os tipos de voz aplicam um nível de volume geral à sua entrada, que controlam usando o método [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) . No submix e nas vozes de mestre, o nível de volume geral é aplicado logo antes do filtro interno da voz e da cadeia de efeitos. Nas vozes de origem, o nível de volume geral é aplicado após o filtro interno da voz e a cadeia de efeitos.
-   As vozes aplicam um nível de volume por canal à sua saída, que controlam usando o método [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) . O nível de volume por canal é aplicado logo após a conversão da taxa de amostragem final da voz e antes de ser enviado para outras vozes.
-   Cada conexão entre uma voz e outra tem uma tabela de níveis usados para enviar áudio de cada canal de origem para cada canal de destino, que é controlado usando o método [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) .

Todos os volumes gerais e volumes de canal são padronizados inicialmente para 1,0. Todas as matrizes de nível de envio assumem como padrão os valores apropriados que preservam a potência de sinal e o posicionamento do canal da maneira mais precisa. Consulte a visão geral de [mapeamento de canal padrão do XAudio2](xaudio2-default-channel-mapping.md) para obter detalhes.

> [!Note]  
> O XAudio2 ajusta automaticamente os níveis de volume com base nas configurações de alto-falante do usuário para manter um nível de volume consistente entre as configurações. Se as configurações do usuário não corresponderem à configuração física, o volume será muito alto ou muito simples em comparação com um sistema com configurações precisas. Por exemplo, um sistema configurado para 5,1 alto-falantes surround sound que tem apenas dois alto-falantes conectados soará muito soft. O XAudio2 não pode detectar se as configurações de alto-falante do usuário correspondem corretamente à configuração física.

 

## <a name="pitch-control"></a>Controle de densidade

As densidades são expressas como taxas de taxa de entrada/taxa de saída entre 1/1024 e 1024/1, inclusive. Uma taxa de 1/1024 diminui o Tom em 10 octaves, enquanto uma taxa de 1024/1 eleva-a por 10 octaves. Você só pode usar o método [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar ajustes de inclinação às vozes de origem e somente se eles não tiverem sido criados com \_ o \_ sinalizador de ispitch de voz XAudio2. A taxa de frequência padrão é 1/1: ou seja, sem alteração de Tom. Duas funções embutidas são fornecidas em XAudio2. h para converter entre as taxas de frequência e semitones: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) e [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de volume e densidade](volume-and-pitch-control.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: alterar a densidade da voz](how-to--change-voice-pitch.md)
</dt> <dt>

[Como: alterar o volume de voz](how-to--change-voice-volume.md)
</dt> </dl>

 

 
