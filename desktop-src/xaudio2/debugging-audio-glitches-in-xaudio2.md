---
description: Os problemas podem ocorrer em XAudio2, este tópico aborda como eles são relatados e algumas abordagens para corrigi-los.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Depurando falhas de áudio no XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829077"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Depurando falhas de áudio no XAudio2

Os problemas podem ocorrer em XAudio2, este tópico aborda como eles são relatados e algumas abordagens para corrigi-los.

Esta visão geral aborda os seguintes tópicos:

-   [Causas de problemas de saída de áudio ou falhas](#causes-of-audio-output-problems-or-glitches)
-   [Como o XAudio2 relata problemas](#how-xaudio2-reports-problems)
-   [Abordagens para corrigir problemas](#approaches-to-fixing-problems)
-   [Tópicos relacionados](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Causas de problemas de saída de áudio ou falhas

As falhas podem ocorrer na saída do XAudio2 por vários motivos.

-   Uma voz de origem XAudio2 está em falta. O cliente não está enviando um novo áudio para ele com rapidez suficiente. Você obtém silêncio porque não há dados a serem reproduzidos.
-   XAudio2 como um todo é sobrecarregado. Demora mais de *x* MS para produzir *X* MS de áudio. Você obtém dropouts porque o XAudio2 não pode produzir dados tão rápidos quanto o dispositivo de áudio precisar. Você pode estar executando muitas vozes ou efeitos por vez, fazendo muito trabalho em retornos de chamada XAudio2 ou fazendo chamadas de API do XAudio2 com muita frequência.
-   O thread de processamento de áudio está paralisando porque a implementação do cliente de algum retorno de chamada do XAudio2 está fazendo coisas que podem bloquear o thread. Por exemplo, ele pode estar acessando o disco, sincronizando com outros threads ou chamando outras funções que possam bloquear. Use um thread em segundo plano de prioridade mais baixa que o retorno de chamada pode sinalizar para executar essas tarefas.
-   O sistema como um todo está sobrecarregado. Outros threads em execução no mesmo ou em uma prioridade mais alta do que XAudio2 estão fazendo muito trabalho. Eles estão competindo com o thread de áudio por tempo de CPU.

## <a name="how-xaudio2-reports-problems"></a>Como o XAudio2 relata problemas

O XAudio2 pode comunicar problemas na compilação da depuração de várias maneiras.

-   Se uma voz estiver sendo privada, XAudio2 mostrará uma mensagem neste formulário.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Se o thread de áudio for executado por muito tempo, o XAudio2 mostrará uma mensagem neste formulário.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    Normalmente, essa mensagem ocorre com a próxima mensagem.

-   Se o driver de áudio não puder ser alimentado com novos dados de áudio na hora, XAudio2 mostrará uma mensagem nesse formulário.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   Chamar [**IXAudio2:: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fornece dados de desempenho de XAudio2, incluindo o número total de falhas desde que o mecanismo de XAudio2 foi iniciado.

## <a name="approaches-to-fixing-problems"></a>Abordagens para corrigir problemas

As maneiras possíveis de reduzir as falhas de áudio incluem as seguintes.

-   No caso de consumo de voz: aumente a quantidade de dados de áudio que são enfileirados antecipadamente em uma voz. Você pode usar [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) para descobrir o número de buffers em fila a qualquer momento. Se você ainda vir erros de consumo de voz, mas não puder ouvir nenhum problema, certifique-se de que você está configurando o [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Sinalizadores** para XAudio2 \_ fim \_ do \_ fluxo no buffer final de um som. Isso informa ao XAudio2 para não esperar que mais buffers estejam disponíveis assim que isso for concluído.

    Nos outros casos:

    -   Reduza o número de vozes e efeitos ativos no grafo, especialmente efeitos caros como reverberação.
    -   Desabilite as vozes e os efeitos que você não está usando.
    -   Use os sinalizadores de XAUDIO2 de \_ voz \_ NOSRC e XAudio2 \_ de voz \_ em [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), sempre que possível. A conversão de taxa de amostra é dispendiosa.
    -   Reduza a taxa de amostra de vozes individuais. Por exemplo, uma voz submix que hospeda um efeito de reverberação pode ter uma taxa de amostragem mais baixa do que a voz de origem enviando a ela. Sons como explosões e gunshots que não precisam de alta fidelidade também podem ser registrados em taxas de exemplo mais baixas.
    -   Certifique-se de que as implementações de retorno de chamada façam o mínimo de trabalho possível e nunca bloqueiem.
    -   Faça menos chamadas para XAudio2. Normalmente, os parâmetros de áudio não precisam ser atualizados para cada quadro de vídeo. A cada 30 ms, isso é suficiente. Você deve eliminar as chamadas redundantes, como a configuração de volume várias vezes em sucessão rápida.
    -   Reduza o uso geral da CPU do jogo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depuração de instalações](debugging-facilities.md)
</dt> <dt>

[Referência de programação em XAudio2](programming-reference.md)
</dt> </dl>

 

 
