---
title: Enviando mensagens de System-Exclusive
description: Enviando mensagens de System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
- MIDI (interface digital de instrumento musical), mensagens exclusivas do sistema
- MIDI (interface digital de instrumentos musicais), mensagens exclusivas do sistema
- executando arquivos MIDI, mensagens exclusivas do sistema
- mensagens MIDI exclusivas do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823680"
---
# <a name="sending-system-exclusive-messages"></a>Enviando mensagens de System-Exclusive

As mensagens exclusivas do sistema MIDI são as únicas mensagens de MIDI que não se ajustarão a um único valor doubleword. As mensagens exclusivas do sistema podem ter qualquer comprimento. O Windows fornece a função [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensagens exclusivas do sistema para dispositivos de saída de Midi. Para especificar os blocos de dados exclusivos do sistema MIDI, use a estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

Depois de enviar um bloco de dados exclusivo do sistema usando o **midiOutLongMsg**, você deve aguardar até que o driver do dispositivo seja concluído com o bloco de dados antes de liberá-lo. Se você estiver enviando vários blocos de dados, deverá monitorar a conclusão de cada bloco de dados para saber quando enviar blocos adicionais. Para obter informações sobre as diferentes técnicas para o monitoramento da conclusão do bloco de dados, consulte [Gerenciando blocos de dados MIDI](managing-midi-data-blocks.md).

> [!Note]  
> Qualquer byte de status de MIDI diferente de uma mensagem de sistema-em tempo real encerrará uma mensagem exclusiva do sistema. Se você estiver usando vários blocos de dados para enviar uma única mensagem exclusiva do sistema, não envie mensagens MIDI além das mensagens do sistema em tempo real entre os blocos de dados.

 

 

 