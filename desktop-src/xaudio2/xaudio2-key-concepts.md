---
description: Esta visão geral apresenta alguns conceitos importantes para usar o XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Principais conceitos do XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762209"
---
# <a name="xaudio2-key-concepts"></a>Principais conceitos do XAudio2

Esta visão geral apresenta alguns conceitos importantes para usar o XAudio2.

-   [Mecanismo de XAudio2](#xaudio2-engine)
-   [Vozes](#voices)
-   [Grafo de áudio](#audio-graph)
-   [Retornos de chamada](#callbacks)
-   [Tópicos relacionados](#related-topics)

## <a name="xaudio2-engine"></a>Mecanismo de XAudio2

A interface do [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) é o núcleo do mecanismo XAudio2. A criação de uma instância da interface **IXAudio2** permite que o cliente enumere os dispositivos de áudio disponíveis, configure as propriedades da API global, crie vozes e monitore o desempenho. A função auxiliar [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) executa tarefas de instanciação e inicialização para XAudio2.

Você pode criar instâncias do XAudio2 várias vezes em um único processo. Cada objeto XAudio2 Opera de forma independente e tem seu próprio thread de processamento de áudio. Somente as configurações de depuração são compartilhadas. Isso é importante no Windows, onde vários componentes diferentes podem ser carregados em um único processo. Por exemplo, o Internet Explorer pode usar vários componentes do XAudio2 simultaneamente. Embora seja possível criar vários objetos do mecanismo XAudio2 em um único aplicativo cliente, você não deve passar informações entre seus respectivos grafos.

Para obter um exemplo de inicialização do mecanismo XAudio2, consulte [como: inicializar o XAudio2](how-to--initialize-xaudio2.md).

## <a name="voices"></a>Vozes

As vozes são os objetos XAudio2 usados para processar, manipular e reproduzir dados de áudio. Há três tipos de vozes em XAudio2.

-   [**Vozes de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    As vozes de origem representam um fluxo de dados de áudio. As vozes de origem enviam seus dados para outros tipos de vozes.

-   [**Submix vozes**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    As vozes submix executam alguma manipulação dos dados de áudio recebidos. Um exemplo de manipulação de dados de áudio pode ser a conversão de taxa de amostra. Depois que uma voz submix processa dados, ela passa esses dados para outra voz submix ou para uma voz mestra.

-   [**Vozes de dominar**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    As vozes de controle de voz recebem dados de vozes de origem e vozes submix e envia esses dados para o hardware de áudio.

Consulte [XAudio2 vozes](voices.md) para obter uma visão geral das vozes XAudio2.

## <a name="audio-graph"></a>Grafo de áudio

Um grafo de áudio é uma coleção de vozes XAudio2. O áudio começa em um lado de um gráfico de áudio em vozes de origem, e opcionalmente passa por uma ou mais vozes submix e termina em uma voz de mestre. Um grafo de áudio conterá uma voz de origem para cada som atualmente em execução, zero ou mais vozes submix e uma voz de mestre. O grafo de áudio mais simples, e o mínimo necessário para fazer um ruído em XAudio2, é uma saída de voz de origem única diretamente para uma voz de mestre. Consulte [como: reproduzir um som com XAudio2](how-to--play-a-sound-with-xaudio2.md) para obter um exemplo das etapas mínimas necessárias para tocar um som com XAudio2.

Consulte [grafo de áudio XAudio2](audio-graphs.md) para obter uma visão geral dos grafos de áudio do XAudio2.

## <a name="callbacks"></a>Retornos de chamada

Os retornos de chamada são o mecanismo que o XAudio2 usa para sinalizar o código do cliente que ocorreu algum evento em uma voz ou no objeto do mecanismo. Como a reprodução de áudio é assíncrona no mecanismo de XAudio2, os retornos de chamada fornecem a única maneira de determinar quando um som acaba sendo executado.

Consulte [retornos de chamada do XAudio2](callbacks.md) para obter uma visão geral dos retornos de chamada do XAudio2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Versões do XAudio2](xaudio2-versions.md)
</dt> <dt>

[Como: Inicializar o XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Como: tocar um som com XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



