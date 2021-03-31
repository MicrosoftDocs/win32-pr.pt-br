---
title: Enviando mensagens MIDI com buffers de fluxo
description: Enviando mensagens MIDI com buffers de fluxo
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- executando arquivos MIDI, buffers de fluxo
- buffers de fluxo, enviando mensagens de MIDI
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640614"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Enviando mensagens MIDI com buffers de fluxo

Quando seu aplicativo funciona com buffers de fluxo, ele usa a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) para enviar todas as mensagens de Midi (curto e longo) para o dispositivo. Para especificar blocos de dados de fluxo, use as estruturas [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) e [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . A estrutura **MIDIHDR** contém um endereço de um bloco de dados bloqueados, o comprimento do bloco de dados e alguns sinalizadores sortidos. Os dados são armazenados na forma de estruturas **MIDIEVENT** . O sistema impõe um limite de tamanho de 64K em buffers de fluxo.

Depois de usar o **midiStreamOut** para enviar um buffer de fluxo de dados, você deve aguardar até que o driver de dispositivo seja concluído com o bloco de dados antes de liberá-lo. Se você estiver enviando vários blocos de dados, deverá monitorar a conclusão de cada bloco de dados para saber quando enviar blocos adicionais. Para obter informações sobre as diferentes técnicas para o monitoramento da conclusão do bloco de dados, consulte [Gerenciando blocos de dados MIDI](managing-midi-data-blocks.md).

 

 