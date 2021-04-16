---
description: 'Há três tipos de objetos de voz XAudio2: origem, submix e vozes de mestre.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Vozes XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782608"
---
# <a name="xaudio2-voices"></a>Vozes XAudio2

Há três tipos de objetos de voz XAudio2: *origem*, *submix* e vozes de *mestre* . As vozes de origem operam em dados de áudio fornecidos pelo cliente. As vozes de origem e submixagem enviam sua saída para uma ou mais vozes de submixagem ou masterização. As vozes de submixagem e masterização combinam o áudio de todas as vozes que as alimentam e operam no resultado. As vozes de masterização gravam dados de áudio em um dispositivo de áudio.

## <a name="actions-performed-by-all-voices"></a>Ações executadas por todas as vozes

Todas as vozes executam as seguintes ações na ordem no áudio que viaja por meio deles.

1.  Ajuste de volume geral, afetando todos os canais de áudio. Consulte [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Uma cadeia especificada pelo cliente opcional de um ou mais efeitos de DSP, como o verbo interno de reverberação ou um efeito de usuário definido pela interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) . Consulte [efeitos de áudio XAudio2](xaudio2-audio-effects.md).
3.  Ajuste do volume de saída por canal. Consulte [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Combinação de matriz separada para cada uma das vozes de destino ou para o dispositivo de saída de áudio para dominar as vozes. Essa combinação altera o número de canais no áudio, se necessário.

## <a name="source-voices"></a>Vozes de origem

Use as vozes de origem para enviar dados de áudio para o pipeline de processamento XAudio2. Eles são os pontos de entrada no [grafo de áudio XAudio2](xaudio2-audio-graph.md). Você deve enviar dados de voz para uma voz de mestre para ser ouvido, seja diretamente ou por meio de vozes submixs intermediárias.

Além das ações executadas por todas as vozes, as vozes de origem executam as seguintes ações.

-   Se necessário, um decodificador é executado primeiro para converter dados de origem codificados em PCM (modulação de código de pulso).
-   Uma conversão de taxa de amostragem (SRC) de taxa variável converte os dados de áudio de origem da voz na taxa de amostra esperada por suas vozes de destino, se necessário, e também dá suporte a alterações de densidade dinâmica.
-   Um filtro de variável de estado opcional pode ser usado para colorir o som de várias maneiras. Consulte [**IXAudio2Voice:: Setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Um filtro opcional pode ser aplicado às saídas da voz. Consulte [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Submix vozes

Uma voz submix é usada principalmente para melhorias de desempenho e processamento de efeitos. Você não pode enviar buffers de dados diretamente para vozes submix. Não será audível, a menos que você o envie para uma voz de mestre. Você pode usar uma voz submix para garantir que um determinado conjunto de dados de voz seja convertido no mesmo formato e tenha uma cadeia de efeitos específica processada no resultado coletivo.

Além das ações executadas por todas as vozes, as vozes submix executam as seguintes ações.

-   Uma SRC de taxa fixa é executada na saída da voz, se necessário, para converter o áudio para a taxa de amostra esperada por suas vozes de destino.
-   Um filtro de variável de estado opcional pode ser usado para colorir o som de várias maneiras. Consulte [**IXAudio2Voice:: Setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Um filtro opcional pode ser aplicado às saídas da voz. Consulte [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Vozes de dominar

Use uma voz de mestre para representar o dispositivo de saída de áudio. Você não pode enviar buffers de dados diretamente para as vozes de dominar, mas os dados enviados para outros tipos de vozes devem ir para uma voz de mestre a ser ouvido.

Além das ações executadas por todas as vozes, as vozes de dominar executam as seguintes ações.

-   Se você criar a voz de mestre com um valor *InputSampleRate* explícito que não tenha suporte do dispositivo de áudio, uma src de taxa fixa será usada para converter a taxa de amostra mais próxima com suporte pelo dispositivo.
-   Recorte o áudio final de saída, se for exigido pelo dispositivo de saída.

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

 

 
