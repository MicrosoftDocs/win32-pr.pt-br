---
description: O XAudio2 pode chamar funções fornecidas pelo cliente para notificá-lo de forma assíncrona de determinados eventos que ocorrem no thread de processamento de áudio.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Retorno de chamadas XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3377bd029cc2e21971748eaca7309dd44390a5bd3420d772c45264dfdbd075c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054286"
---
# <a name="xaudio2-callbacks"></a>Retorno de chamadas XAudio2

O XAudio2 pode chamar funções fornecidas pelo cliente para notificá-lo de forma assíncrona de determinados eventos que ocorrem no thread de processamento de áudio. Esses retornos de chamada podem ser globais ou específicos para uma determinada voz de origem. Para receber retornos de chamada de mecanismo global, o cliente deve fornecer uma instância de uma classe que implemente a interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) ao inicializar o XAudio2. Para receber retornos de chamada de voz de origem, o cliente deve fornecer uma instância de uma classe que implemente a interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) ao criar vozes de origem. Para obter mais detalhes, **consulte IXAudio2EngineCallback** **e IXAudio2VoiceCallback.**

Você deve implementar retornos de chamada com cuidado para evitar causar quebras no áudio. Sempre que um retorno de chamada estiver em execução, xAudio2 não poderá gerar nenhum áudio. Atrasos de mais de alguns milissegundos podem causar um problema de áudio. Atrasos dessa natureza também geram a saída do depurador. Isso indica possíveis problemas de desempenho. No mínimo, as funções de retorno de chamada não devem fazer o seguinte:

-   Acessar o disco rígido ou outro armazenamento permanente
-   Fazer chamadas de API caras ou de bloqueio
-   Sincronizar com outras partes do código do cliente
-   Exigir uso significativo da CPU

Se o design do cliente exigir um retorno de chamada para disparar ações como aquelas listadas anteriormente, o retorno de chamada deverá sinalizar um thread de cliente diferente para fazer o trabalho. Você pode fazer isso com um mecanismo **SetEvent** simples ou mecanismos mais sofisticados, como uma fila de comandos sem bloqueio que é consumida por outro thread.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

A [**classe IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) contém métodos que notificam o cliente quando determinados eventos ocorrem no mecanismo XAudio2. Esses métodos devem ser implementados pelo cliente XAudio2. XAudio2 chama esses métodos por meio de um ponteiro de interface fornecido pelo cliente usando o [**método IXAudio2::RegisterForCallbacks.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) Todos esses métodos retornam **void**, em vez de **um HRESULT**.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

A [**classe IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contém métodos que notificam o cliente quando determinados eventos ocorrem em uma voz de origem XAudio2 específica. XAudio2 chama esses métodos por meio de um ponteiro de interface fornecido pelo cliente [**em IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice). Assim como [**com IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), esses métodos devem ser implementados pelo cliente XAudio2 e retornar **void** em vez de **um HRESULT**.

Conforme mencionado anteriormente, é crucial que as implementações fornecidas pelo cliente desses retornos de chamada retornem o mais rápido possível, preferencialmente dentro de um milissegundo. Os retornos de chamada são executados no thread de processamento de áudio e todo o processamento é interrompido até que o retorno de chamada retorne. Um atraso em um retorno de chamada pode facilmente causar um problema de áudio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Retornos de chamada](callbacks.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Usar retornos de chamadas de voz de origem](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[Como: Usar retornos de chamadas de dispositivo](how-to--use-engine-callbacks.md)
</dt> <dt>

[Como: Fazer o streaming de um som do disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
