---
title: Enviando mensagens MIDI individuais
description: Enviando mensagens MIDI individuais
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (Interface Digital do Instrument Instrument), enviando mensagens
- MIDI (Interface Digital do Instrument Instrument), enviando mensagens
- reprodução de arquivos MIDI, envio de mensagens
- enviando mensagens MIDI
- MIDI (Interface Digital do Instrument Instrument), mensagens individuais
- MIDI (Interface Digital do Instrument Instrument), mensagens individuais
- reprodução de arquivos MIDI, mensagens individuais
- mensagens MIDI individuais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1f73d0956004f90644ce2e8b0e41b368137a7b61fd04e6d17302619980336d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037446"
---
# <a name="sending-individual-midi-messages"></a>Enviando mensagens MIDI individuais

Você pode trabalhar com mensagens MIDI individuais usando as funções a seguir.



| Valor                                      | Significado                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envia um buffer de dados MIDI para o dispositivo de saída MIDI especificado. Use essa função para enviar mensagens exclusivas do sistema para um dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Desliga todas as observações em todos os canais de um dispositivo de saída MIDI especificado. Quaisquer buffers exclusivos do sistema e buffers de fluxo pendentes são marcados como feitos e retornados ao aplicativo. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envia uma mensagem MIDI para um dispositivo de saída MIDI especificado.                                                                                                                             |



 

Para enviar qualquer mensagem MIDI (exceto para mensagens exclusivas do sistema), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 