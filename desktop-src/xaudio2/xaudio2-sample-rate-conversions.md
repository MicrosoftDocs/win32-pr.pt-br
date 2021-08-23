---
description: As vozes XAudio2 poderão executar conversões automáticas de taxa de amostragem se a taxa de amostra de entrada for diferente da taxa de exemplo de entrada de suas vozes de saída.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversões de taxa de amostra XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82983d1d9307551e516f1b8b60676b4b250450da65f416c340446c5a906f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962507"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversões de taxa de amostra XAudio2

As vozes XAudio2 poderão executar conversões automáticas de taxa de amostragem se a taxa de amostra de entrada for diferente da taxa de exemplo de entrada de suas vozes de saída.

As conversões de taxa de exemplo seguem estas regras:

-   A taxa de exemplo de entrada de voz é fixa.

    As vozes só podem lidar com a taxa de exemplo de entrada especificada quando foram criadas. Para [**o**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) domínio de vozes e vozes [**de submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice), a taxa de exemplo de entrada é especificada com o argumento *InputSampleRate* para as funções [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) e [**IXAudio2::CreateSubmixVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) Para vozes de origem, a taxa de exemplo de entrada da voz é especificada pelo argumento pSourceFormat para a [**função IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)

-   Todas as vozes de saída de uma voz devem ter a mesma taxa de exemplo de entrada.

    As vozes podem converter de sua taxa de exemplo de entrada em qualquer taxa de exemplo de saída, mas todas as vozes de saída da voz devem ter a mesma taxa de exemplo de entrada. Por exemplo, uma voz pode ser saída para qualquer número de vozes com uma taxa de exemplo de entrada de 22 kHz. No entanto, se essa mesma voz tivesse várias vozes de saída, cada uma com uma taxa de exemplo de entrada diferente, o grafo de áudio não seria válido.

-   O processamento de conversão de taxa de exemplo ocorre somente quando necessário.

    Converter dados de áudio em uma taxa de exemplo diferente incorre em mais sobrecarga de processamento, o que é preferível evitar. Se a taxa de exemplo de entrada de uma voz corresponde à taxa de amostra de entrada de suas vozes de saída, essa conversão não é feita e o tempo de processamento é reduzido.

-   A taxa de exemplo de saída pode variar durante a vida útil de uma voz.

    A taxa de amostra de saída de uma voz não é fixa. Desde que todas as suas vozes de saída tenham a mesma taxa de exemplo de entrada, o grafo de áudio será válido. Se uma voz for alterada para saída para novas vozes com uma taxa de exemplo de entrada diferente, a voz será convertida na taxa de exemplo de entrada das novas vozes.

Há alguns cenários em que é necessário adicionar uma voz de submix para executar a conversão de taxa de exemplo entre vozes. Se uma voz precisar ser saída para vozes com várias taxas de exemplo de entrada, apenas uma das vozes poderá ser uma saída direta da voz original. Como todas as vozes de saída de uma voz devem ter a mesma taxa de exemplo de entrada, as outras vozes recebem a saída indiretamente. Deve haver uma voz submix com a taxa de exemplo de entrada correta que vem entre a voz original e a voz de saída pretendido.

Por exemplo, considere uma voz de origem com uma taxa de exemplo de entrada de 22 kHz, que precisa ser saída para uma voz de submix com uma taxa de amostra de entrada de 11 kHz e uma voz mestra com uma taxa de amostra de entrada de 44,1 kHz. Como as duas vozes de saída têm taxas de exemplo de entrada diferentes, você precisa inserir mais vozes de submix entre a voz original e suas vozes de saída pretendidas. Para manter a fidelidade da voz de origem e evitar conversões desnecessárias dispendiosas em taxas de exemplo mais altas, você precisa inserir duas vozes de submix com 22 taxas de entrada de exemplo no grafo. Uma voz de submix seria saída em 11 kz para a voz da submix com o efeito reverb, e a outra voz de submix seria saída para a voz mestra em 44,1 kz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Exemplos de conversão de taxa de exemplo em grafos de áudio

Todas as vozes têm a mesma taxa de entrada de exemplo; nenhuma conversão de taxa de exemplo é feita no grafo de áudio.![nenhuma conversão de taxa de exemplo é feita no grafo de áudio.](images/xaudio2-sample-rate-conversions-1.png)

Todas as vozes têm a mesma taxa de entrada de exemplo, exceto a voz mestra; A conversão de taxa de amostra só é executada nos dados que vão para a voz de mestre. ![A conversão de taxa de amostra só é executada nos dados que vão para a voz de mestre.](images/xaudio2-sample-rate-conversions-2.png)

As vozes têm taxas de entrada de exemplo diferentes e exigem mais vozes de submix para executar conversões de taxa de exemplo; A conversão de taxa de amostra é executada em vários locais no grafo de áudio. ![A conversão de taxa de amostra é executada em vários locais no grafo de áudio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vozes](voices.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 
