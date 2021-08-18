---
description: 'Há três tipos de objetos de voz XAudio2: vozes de origem, submix e mestre.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Vozes XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b756033be5b64dbf03e3b3756902014774a53c9aebc8f41a1df1f982685cca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025934"
---
# <a name="xaudio2-voices"></a>Vozes XAudio2

Há três tipos de objetos de voz XAudio2: origem, *submix* e *vozes mestras.* As vozes de origem operam em dados de áudio fornecidos pelo cliente. As vozes de origem e submixagem enviam sua saída para uma ou mais vozes de submixagem ou masterização. As vozes de submixagem e masterização combinam o áudio de todas as vozes que as alimentam e operam no resultado. As vozes de masterização gravam dados de áudio em um dispositivo de áudio.

## <a name="actions-performed-by-all-voices"></a>Ações executadas por todas as vozes

Todas as vozes executam as ações a seguir em ordem no áudio que as percorre.

1.  Ajuste geral do volume, afetando todos os canais de áudio. Consulte [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Uma cadeia opcional especificada pelo cliente de um ou mais efeitos DSP, como o reverb integrado ou um efeito de usuário definido pela interface [**IXAPO.**](/windows/desktop/api/XAPO/nn-xapo-ixapo) Consulte [Efeitos de áudio XAudio2](xaudio2-audio-effects.md).
3.  Ajuste de volume de saída por canal. Consulte [**IXAudio2Voice::SetChannelVolumes.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
4.  Separe a combinação de matrizes para cada uma das vozes de destino ou para o dispositivo de saída de áudio para dominar vozes. Essa combinação altera o número de canais no áudio, se necessário.

## <a name="source-voices"></a>Vozes de Origem

Use vozes de origem para enviar dados de áudio para o pipeline de processamento XAudio2. Eles são os pontos de entrada no arquivo [de áudio XAudio2 Graph](xaudio2-audio-graph.md). Você deve enviar dados de voz para uma voz mestra a ser escutada, diretamente ou por meio de vozes de submix intermediárias.

Além das ações executadas por todas as vozes, as vozes de origem executam as seguintes ações.

-   Se necessário, um decodificador é executado primeiro para converter dados de origem codificados em PCM (Pulse Code Modulartion).
-   Uma SRC (conversão de taxa de amostragem de taxa variável) converte os dados de áudio de origem da voz para a taxa de amostra esperada por suas vozes de destino, se necessário, e também dá suporte a alterações dinâmicas de tom.
-   Um filtro opcional de variável de estado pode ser usado para colorir o som de várias maneiras. Consulte [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Um filtro opcional pode ser aplicado às saídas da voz. Consulte [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Vozes de submix

Uma voz de submix é usada principalmente para melhorias de desempenho e processamento de efeitos. Você não pode enviar buffers de dados diretamente para vozes de submix. Ele não será audível, a menos que você o envie para uma voz de mestre. Você pode usar uma voz de submix para garantir que um determinado conjunto de dados de voz seja convertido no mesmo formato e ter uma cadeia de efeito específica processada no resultado coletivo.

Além das ações executadas por todas as vozes, as vozes de submix executam as ações a seguir.

-   Um SRC de taxa fixa é executado na saída da voz, se necessário, para converter o áudio na taxa de exemplo esperada por suas vozes de destino.
-   Um filtro opcional de variável de estado pode ser usado para colorir o som de várias maneiras. Consulte [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Um filtro opcional pode ser aplicado às saídas da voz. Consulte [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Mastering Voices

Use uma voz mestra para representar o dispositivo de saída de áudio. Você não pode enviar buffers de dados diretamente para as vozes mestras, mas os dados enviados para outros tipos de vozes devem ir para uma voz mestra a ser escutada.

Além das ações executadas por todas as vozes, as vozes mestras executam as ações a seguir.

-   Se você criar a voz mestra com um valor *InputSampleRate* explícito que não é suportado pelo dispositivo de áudio, um SRC de taxa fixa será usado para converter para a taxa de amostra mais próxima com suporte pelo dispositivo.
-   Corte o áudio de saída final, se for exigido pelo dispositivo de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vozes](voices.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
