---
description: O XAudio2 pode chamar funções fornecidas pelo cliente para notificá-lo de forma assíncrona de determinados eventos que ocorrem no thread de processamento de áudio.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Retorno de chamadas XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee191ad8c15d238a065c837c6fb192befbe7a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297611"
---
# <a name="xaudio2-callbacks"></a>Retorno de chamadas XAudio2

O XAudio2 pode chamar funções fornecidas pelo cliente para notificá-lo de forma assíncrona de determinados eventos que ocorrem no thread de processamento de áudio. Esses retornos de chamada podem ser globais ou específicos para uma determinada voz de origem. Para receber retornos de chamada do mecanismo global, o cliente deve fornecer uma instância de uma classe que implementa a interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) ao inicializar XAudio2. Para receber retornos de chamada de voz de origem, o cliente deve fornecer uma instância de uma classe que implementa a interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) ao criar vozes de origem. Para obter mais detalhes, consulte **IXAudio2EngineCallback** e **IXAudio2VoiceCallback**.

Você deve implementar os retornos de chamada com cuidado para evitar causar interrupções no áudio. Sempre que um retorno de chamada estiver em execução, o XAudio2 não poderá gerar nenhum áudio. Os atrasos de mais de alguns milissegundos podem causar um problema de áudio. Os atrasos dessa natureza também geram a saída do depurador. Isso indica possíveis problemas de desempenho. No mínimo, as funções de retorno de chamada não devem fazer o seguinte:

-   Acessar o disco rígido ou outro armazenamento permanente
-   Fazer chamadas de API caras ou de bloqueio
-   Sincronizar com outras partes do código do cliente
-   Exigir uso significativo da CPU

Se o design do cliente exigir um retorno de chamada para disparar ações como aquelas listadas anteriormente, o retorno de chamada deverá sinalizar um thread de cliente diferente para fazer o trabalho. Você pode fazer isso com **um mecanismo simples** ou mecanismos mais sofisticados, como uma fila de comandos sem bloqueio consumida por outro thread.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

A classe [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) contém métodos que notificam o cliente quando determinados eventos acontecem no mecanismo XAudio2. Esses métodos devem ser implementados pelo cliente XAudio2. XAudio2 chama esses métodos por meio de um ponteiro de interface fornecido pelo cliente usando o método [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) . Todos esses métodos retornam **void**, em vez de um **HRESULT**.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

A classe [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contém métodos que notificam o cliente quando determinados eventos acontecem em uma voz de origem XAudio2 específica. XAudio2 chama esses métodos por meio de um ponteiro de interface fornecido pelo cliente em [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice). Assim como com [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), esses métodos devem ser implementados pelo cliente XAudio2 e retornar **void** em vez de um **HRESULT**.

Conforme mencionado anteriormente, é crucial que as implementações fornecidas pelo cliente desses retornos de chamada retornam o mais rápido possível, preferivelmente em um milissegundo. Os retornos de chamada são executados no thread de processamento de áudio, e todo o processamento é interrompido até que o retorno de chamada seja retornado. Um atraso em um retorno de chamada pode causar facilmente um problema de áudio.

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

 

 
