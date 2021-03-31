---
title: Usando uma função de retorno de chamada para gerenciar a reprodução em buffer
description: Usando uma função de retorno de chamada para gerenciar a reprodução em buffer
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- MIDI (interface digital de instrumento musical), reprodução em buffer
- MIDI (interface digital de instrumentos musicais), reprodução em buffer
- executando arquivos MIDI, reprodução em buffer
- reprodução em buffer
- MOM_CLOSE mensagem
- MOM_DONE mensagem
- MOM_OPEN mensagem
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), funções de retorno de chamada
- MIDI (interface digital de instrumentos musicais), funções de retorno de chamada
- executando arquivos MIDI, funções de retorno de chamada
- Função de retorno de chamada MidiOutProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640848"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>Usando uma função de retorno de chamada para gerenciar a reprodução em buffer

Você pode definir sua própria função de retorno de chamada para gerenciar a reprodução em buffer de dispositivos de saída de MIDI. A função de retorno de chamada está documentada como [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).

As mensagens a seguir podem ser enviadas para o parâmetro *wMsg* da função de retorno de chamada **MidiOutProc** .



| Valor                           | Significado                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**fechamento do MOM \_**](mom-close.md) | Enviado quando o dispositivo é fechado usando a função [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MOM \_ concluído**](mom-done.md)   | Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a função [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**MOM \_ aberto**](mom-open.md)   | Enviado quando o dispositivo é aberto usando a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Essas mensagens são semelhantes àquelas enviadas para funções de procedimento de janela, mas os parâmetros são diferentes. Um identificador do dispositivo MIDI aberto é passado como um parâmetro para a função de retorno de chamada, junto com o doubleword dos dados da instância passados usando **midiOutOpen**.

Depois que o driver for concluído com um bloco de dados, você poderá limpar e liberar o bloco de dados. Devido às restrições sugeridas nas funções de retorno de chamada, é melhor não fazer isso de dentro da função de retorno de chamada.

 

 