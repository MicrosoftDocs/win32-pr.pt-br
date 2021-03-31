---
description: As vozes XAudio2 podem executar conversões de taxa de amostragem automáticas se a taxa de amostragem de entrada for diferente da taxa de amostra de entrada de suas vozes de saída.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversões de taxa de exemplo XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d437a45f9e896826bedc1418382fb257201722d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172040"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversões de taxa de exemplo XAudio2

As vozes XAudio2 podem executar conversões de taxa de amostragem automáticas se a taxa de amostragem de entrada for diferente da taxa de amostra de entrada de suas vozes de saída.

As conversões de taxa de amostra seguem estas regras:

-   A taxa de amostra de entrada de voz é fixa.

    As vozes só podem manipular a taxa de amostra de entrada especificada quando foram criadas. Para [**vozes de mestre**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) e [**vozes submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice), a taxa de amostra de entrada é especificada com o argumento *InputSampleRate* para as funções [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) e [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) . Para as vozes de origem, a taxa de amostra de entrada da voz é especificada pelo argumento pSourceFormat para a função [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

-   Todas as vozes de saída de uma voz devem ter a mesma taxa de amostragem de entrada.

    As vozes podem converter de sua taxa de amostra de entrada para qualquer taxa de amostragem de saída, mas todas as vozes de saída da voz devem ter a mesma taxa de amostra de entrada. Por exemplo, uma voz pode gerar uma saída para qualquer número de vozes com uma taxa de amostragem de entrada de 22 kHz. No entanto, se essa mesma voz tivesse várias vozes de saída, cada uma com uma taxa de amostra de entrada diferente, o grafo de áudio não seria válido.

-   O processamento de conversão de taxa de amostra só ocorre quando necessário.

    Converter dados de áudio em uma taxa de amostra diferente incorre em mais sobrecarga de processamento, o que é preferível evitar. Se a taxa de amostra de entrada de uma voz corresponder à taxa de amostra de entrada de suas vozes de saída, essa conversão não será feita e o tempo de processamento será reduzido.

-   A taxa de amostragem de saída pode variar ao longo da vida útil de uma voz.

    A taxa de amostra de saída de uma voz não é fixa. Desde que todas as suas vozes de saída tenham a mesma taxa de amostragem de entrada, o grafo de áudio será válido. Se uma voz for alterada para saída para novas vozes com uma taxa de amostra de entrada diferente, a voz será convertida para a taxa de amostra de entrada das novas vozes.

Há alguns cenários em que é necessário adicionar uma voz submix para executar a conversão de taxa de amostra entre as vozes. Se uma voz precisar de saída para vozes com várias taxas de amostra de entrada, somente uma das vozes poderá ser uma saída direta da voz original. Como todas as vozes de saída de uma voz devem ter a mesma taxa de amostra de entrada, as outras vozes recebem a saída indiretamente. Deve haver uma voz submix com a taxa de amostra de entrada correta que vem entre a voz original e a voz de saída pretendida.

Por exemplo, considere uma voz de origem com uma taxa de amostra de entrada de 22 kHz, que precisa gerar saída para uma voz submix com uma taxa de amostra de entrada de 11 kHz e uma voz de mestre com uma taxa de amostragem de entrada de 44,1 kHz. Como as duas vozes de saída têm taxas de amostra de entrada diferentes, você precisa inserir mais vozes submix entre a voz original e suas vozes de saída pretendidas. Para manter a fidelidade da voz de origem e evitar conversões caras desnecessárias para taxas de exemplo mais altas, você precisa inserir duas vozes submix com taxas de entrada de exemplo de 22 kHz no grafo. Uma voz submix seria transformada em 11 kHz à voz submix com o efeito de reverberação, e a outra voz submix seria a saída para a voz de mestre em 44,1 kHz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Exemplos de conversão de taxa de exemplo em grafos de áudio

Todas as vozes têm a mesma taxa de entrada de exemplo; nenhuma conversão de taxa de amostragem é feita no grafo de áudio.![nenhuma conversão de taxa de amostragem é feita no grafo de áudio.](images/xaudio2-sample-rate-conversions-1.png)

Todas as vozes têm a mesma taxa de entrada de exemplo, exceto a voz de mestre; a conversão de taxa de amostra só é executada em dados que vão para a voz de mestre. ![a conversão de taxa de amostra só é executada em dados que vão para a voz de mestre.](images/xaudio2-sample-rate-conversions-2.png)

As vozes têm taxas de entrada de exemplo diferentes e exigem mais vozes submix para executar conversões de taxas de amostra; a conversão de taxa de amostra é executada em vários locais no grafo de áudio. ![a conversão de taxa de amostra é executada em vários locais no grafo de áudio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vozes](voices.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 
