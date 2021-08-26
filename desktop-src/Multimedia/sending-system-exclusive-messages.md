---
title: Enviando System-Exclusive mensagens
description: Enviando System-Exclusive mensagens
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (Interface Digital do Instrument Instrument), enviando mensagens
- MIDI (Interface Digital do Instrument Instrument), enviando mensagens
- reprodução de arquivos MIDI, envio de mensagens
- enviando mensagens MIDI
- MIDI (Interface Digital do Instrument Instrument), mensagens exclusivas do sistema
- MIDI (Interface Digital do Instrument Instrument), mensagens exclusivas do sistema
- reprodução de arquivos MIDI, mensagens exclusivas do sistema
- mensagens MIDI exclusivas do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad97371f56c042e5acd230aba6144f5f9734a594b370a791422b2e8f8148861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037256"
---
# <a name="sending-system-exclusive-messages"></a>Enviando System-Exclusive mensagens

Mensagens exclusivas do sistema MIDI são as únicas mensagens MIDI que não se ajustarão a um único valor doubleword. Mensagens exclusivas do sistema podem ter qualquer comprimento. Windows fornece a [**função midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensagens exclusivas do sistema para dispositivos de saída MIDI. Para especificar blocos de dados exclusivos do sistema MIDI, use a [**estrutura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

Depois de enviar um bloco de dados exclusivo do sistema usando **midiOutLongMsg,** você deve aguardar até que o driver de dispositivo seja concluído com o bloco de dados antes de libera-lo. Se você estiver enviando vários blocos de dados, deverá monitorar a conclusão de cada bloco de dados para saber quando enviar blocos adicionais. Para obter informações sobre técnicas diferentes para monitorar a conclusão de blocos de dados, consulte [Gerenciando blocos de dados MIDI](managing-midi-data-blocks.md).

> [!Note]  
> Qualquer byte de status MIDI diferente de uma mensagem em tempo real do sistema encerrará uma mensagem exclusiva do sistema. Se você estiver usando vários blocos de dados para enviar uma única mensagem exclusiva do sistema, não envie mensagens MIDI diferentes de mensagens em tempo real do sistema entre blocos de dados.

 

 

 