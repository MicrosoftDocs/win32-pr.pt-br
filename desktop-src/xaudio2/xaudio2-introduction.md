---
description: XAudio2 é uma API de áudio de baixo nível. Ele fornece um processamento de sinal e uma base de combinação para jogos que são semelhantes a seus predecessores, DirectSound e XAudio.
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: Introdução ao XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7cde958256d9126746a07764dc0c792e88289c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772682"
---
# <a name="xaudio2-introduction"></a>Introdução ao XAudio2

XAudio2 é uma API de áudio de baixo nível. Ele fornece um processamento de sinal e uma base de combinação para jogos que são semelhantes a seus predecessores, DirectSound e XAudio.

XAudio2 é a substituição longa esperada para DirectSound. Ele aborda vários problemas pendentes e solicitações de recursos.

## <a name="xaudio2-features"></a>Recursos do XAudio2

Veja a seguir uma lista de recursos do XAudio2 e novas funcionalidades que permitem aos desenvolvedores melhorar o desempenho em seus jogos.

-   Efeitos de DSP e filtragem por voz

    Os efeitos do DSP (processamento de sinal digital) são os sombreadores de pixel do áudio. Eles lidam com tudo, desde transformar um som, transformando um ruído de Pig em um Monster Sound pequeno, assustador, para colocar sons no ambiente do jogo usando a filtragem de reverberação e de oclusão ou obstrução. O XAudio2 fornece uma estrutura DSP flexível e poderosa. Ele também fornece um filtro interno em cada voz, para efeitos eficientes de filtragem de baixa/alta/faixa.

    Consulte [XAudio2 Audio Effects](xaudio2-audio-effects.md) e [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para obter mais informações sobre efeitos de DSP e filtragem por voz.

-   Submisturando

    A submistura combina vários sons em um único fluxo de áudio — por exemplo, um som de mecanismo composto por partes compostas, todos que estão sendo reproduzidos simultaneamente. Além disso, você pode usar a subcombinação para processar e combinar partes semelhantes de um jogo. Por exemplo, você pode combinar todos os efeitos de som do jogo para permitir que uma configuração de volume do usuário seja aplicada enquanto uma configuração separada controla o volume de música. Combinado com o DSP, a submixagem fornece o tipo de roteamento e processamento de dados necessários para os jogos de hoje. O XAudio2 permite níveis arbitrários de submistura, permitindo a criação de sons complexos e combinações de jogos.

    Consulte [grafo de áudio XAudio2](xaudio2-audio-graph.md) e [vozes XAudio2](xaudio2-voices.md) para obter mais informações sobre a subcombinação.

-   Suporte a áudio compactado

    Uma das principais solicitações de recursos para o DirectSound é o suporte a áudio compactado. O XAudio2 dá suporte a formatos compactados — ADPCM – nativamente com descompactação de tempo de execução.

-   Suporte avançado a multichannels e Surround Sound

    Suporte a Multichannel, 3D e Surround Sound é expandido. 3D e Surround Sound agora são muito mais flexíveis e transparentes. XAudio2 remove o limite de 6 canais em sons multicanal e dá suporte a áudio multicanal em qualquer placa de áudio com capacidade para multicanal. O cartão não precisa ser acelerado por hardware.

-   Processamento de multitaxa

    Para ajudar a minimizar o uso da CPU, o XAudio2 fornece a tecnologia para criar vários grafos de processamento de áudio de baixa taxa. Isso pode reduzir significativamente o uso da CPU, permitindo que um jogo processe áudio na taxa do material de origem se a taxa for menor que 48 kHz.

-   Modelo de API de não bloqueio

    Com poucas exceções, uma chamada de método XAudio2 não bloqueará o mecanismo de processamento de áudio. Isso significa que um cliente pode fazer com segurança um conjunto de chamadas de método a qualquer momento sem bloquear chamadas de longa execução, causando atrasos. As exceções são o método [**IXAudio2Voice::D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) (que pode bloquear o mecanismo até que a voz que está sendo destruída termine o processamento) e os métodos que encerram o thread de áudio: [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) e [**IXAudio2:: Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release). Observe que, embora as chamadas de método XAudio2 não bloqueiem o mecanismo de processamento de áudio, os métodos XAudio2 contêm seções críticas e podem se tornar bloqueados em algumas circunstâncias.

## <a name="when-to-use-xaudio2"></a>Quando usar o XAudio2

O XAudio2 destina-se principalmente ao desenvolvimento de mecanismos de áudio de alto desempenho para jogos. Para os desenvolvedores de jogos que desejam adicionar efeitos sonoros e música de fundo aos jogos modernos, o XAudio2 oferece um mecanismo de gráfico e mixagem de áudio com baixa latência e suporte para buffers dinâmicos, reprodução precisa de amostra síncrona e conversão implícita de taxa de origem. Em comparação com WASAPI, o XAudio2 requer apenas uma quantidade mínima de código, mesmo para soluções de áudio complexas. Em comparação com o mecanismo de Media Foundation, o XAudio2 é uma API C++ de baixo nível e baixa latência projetada para uso em jogos.

Para aplicativos que simplesmente precisam de reprodução de música regular, o mecanismo de Media Foundation pode ser uma correspondência melhor para os requisitos do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Referência de programação em XAudio2](programming-reference.md)
</dt> </dl>

 

 
