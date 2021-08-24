---
description: Falhas podem ocorrer no XAudio2, este tópico aborda como elas são relatadas e algumas abordagens para corrigi-las.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Depurando falhas de áudio no XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8856defc67bc9453b9d83f5ed369bfb96f48b8c2c16c92ea535a0c1b648402b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703616"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>Depurando falhas de áudio no XAudio2

Falhas podem ocorrer no XAudio2, este tópico aborda como elas são relatadas e algumas abordagens para corrigi-las.

Esta visão geral aborda os seguintes tópicos:

-   [Causas de problemas de saída de áudio ou falhas](#causes-of-audio-output-problems-or-glitches)
-   [Como o XAudio2 relata problemas](#how-xaudio2-reports-problems)
-   [Abordagens para corrigir problemas](#approaches-to-fixing-problems)
-   [Tópicos relacionados](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>Causas de problemas de saída de áudio ou falhas

Falhas podem ocorrer na saída XAudio2 por vários motivos.

-   Uma voz de origem XAudio2 está sem energia. O cliente não está enviando áudio novo para ele com rapidez suficiente. Você tem silêncio porque ele não tem dados a reproduzir.
-   XAudio2 como um todo é sobrecarregado. Demora mais do que *X* ms para produzir *X* ms de áudio. Você recebe os dropouts porque o XAudio2 não pode produzir dados tão rápido quanto o dispositivo de áudio precisa. Você pode estar executando muitas vozes ou efeitos por vez, fazendo muito trabalho em retornos de chamada XAudio2 ou fazendo chamadas à API XAudio2 com muita frequência.
-   O thread de processamento de áudio está parando porque a implementação do cliente de algum retorno de chamada XAudio2 está fazendo coisas que podem bloquear o thread. Por exemplo, ele pode estar acessando o disco, sincronizando com outros threads ou chamando outras funções que podem bloquear. Use um thread em segundo plano de prioridade mais baixa que o retorno de chamada possa sinalizar para executar essas tarefas.
-   O sistema como um todo está sobrecarregado. Outros threads em execução com a mesma prioridade ou maior que xAudio2 estão fazendo muito trabalho. Eles estão competindo com o thread de áudio pelo tempo de CPU.

## <a name="how-xaudio2-reports-problems"></a>Como o XAudio2 relata problemas

O XAudio2 pode comunicar falhas no build de depuração de várias maneiras.

-   Se uma voz estiver passando por uma falta, xAudio2 mostrará uma mensagem nesse formulário.

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   Se o thread de áudio for executado por muito tempo, o XAudio2 mostrará uma mensagem nesse formulário.

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    Normalmente, essa mensagem ocorre com a próxima mensagem.

-   Se o driver de áudio não puder ser alimentado com novos dados de áudio no horário, o XAudio2 mostrará uma mensagem nesse formulário.

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   Chamar [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fornece dados de desempenho XAudio2, incluindo o número total de falhas desde o início do mecanismo XAudio2.

## <a name="approaches-to-fixing-problems"></a>Abordagens para corrigir problemas

As possíveis maneiras de reduzir falhas de áudio incluem o seguinte.

-   No caso de falta de voz: aumente a quantidade de dados de áudio que estão na fila em uma voz. Você pode usar [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) para descobrir o número de buffers na fila a qualquer momento. Se você ainda vir erros de falta de voz, mas não puder ouvir nenhuma falha, certifique-se de que está configurando [**\_ o BUFFER XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Sinaliza para** XAUDIO2 \_ END OF STREAM no buffer final de um \_ \_ som. Isso informa ao XAudio2 para não esperar que mais buffers necessariamente estarão disponíveis assim que esse terminar.

    Nos outros casos:

    -   Reduza o número de vozes e efeitos ativos no grafo, especialmente efeitos caros, como o reverb.
    -   Desabilite vozes e efeitos que você não está usando.
    -   Use os sinalizadores \_ \_ XAUDIO2 VOICE NOSRC e XAUDIO2 \_ VOICE \_ NOPITCH [**em IXAudio2::CreateSourceVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)sempre que possível. A conversão de taxa de exemplo é caro.
    -   Reduza a taxa de amostra de vozes individuais. Por exemplo, uma voz submix que hospeda um efeito de reverb pode ter uma taxa de amostra menor do que a voz de origem enviando para ela. Sons como explosão e ruídos que não precisam de alta fidelidade também podem ser registrados com taxas de amostra menores.
    -   Certifique-se de que as implementações de retorno de chamada trabalhem o menos possível e nunca bloqueiem.
    -   Faça menos chamadas para XAudio2. Os parâmetros de áudio geralmente não precisam ser atualizados para cada quadro de vídeo. A cada 30 ms ou mais, é suficiente. Você deve eliminar chamadas redundantes, como definir o volume várias vezes em sucessão rápida.
    -   Reduza o uso geral da CPU do jogo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de depuração](debugging-facilities.md)
</dt> <dt>

[Referência de programação em XAudio2](programming-reference.md)
</dt> </dl>

 

 
