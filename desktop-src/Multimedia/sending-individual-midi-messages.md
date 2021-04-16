---
title: Enviando mensagens individuais de MIDI
description: Enviando mensagens individuais de MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), mensagens individuais
- MIDI (interface digital de instrumentos musicais), mensagens individuais
- executando arquivos MIDI, mensagens individuais
- mensagens individuais de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105757505"
---
# <a name="sending-individual-midi-messages"></a>Enviando mensagens individuais de MIDI

Você pode trabalhar com mensagens MIDI individuais usando as funções a seguir.



| Valor                                      | Significado                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envia um buffer de dados MIDI para o dispositivo de saída MIDI especificado. Use essa função para enviar mensagens exclusivas do sistema para um dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Desativa todas as notas em todos os canais para um dispositivo de saída MIDI especificado. Qualquer buffer exclusivo do sistema pendente e buffers de fluxo são marcados como concluídos e retornados para o aplicativo. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envia uma mensagem MIDI para um dispositivo de saída MIDI especificado.                                                                                                                             |



 

Para enviar qualquer mensagem MIDI (exceto para mensagens exclusivas do sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 