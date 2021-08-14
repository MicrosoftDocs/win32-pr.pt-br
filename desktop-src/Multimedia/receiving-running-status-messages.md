---
title: Recebendo Running-Status mensagens
description: Recebendo Running-Status mensagens
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (Interface Digital) do Instrument Instrument, executando o status
- MIDI (Interface Digital do Instrument Instrument), executando o status
- gravação de áudio MIDI, status de execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371341"
---
# <a name="receiving-running-status-messages"></a>Recebendo Running-Status mensagens

A *especificação Standard MIDI Files 1.0* permite o uso do *status* de execução quando uma mensagem tem o mesmo byte de status da mensagem anterior. Quando o status de execução é usado, o byte de status das mensagens subsequentes pode ser omitido. Todos os drivers de dispositivo de entrada MIDI são necessários para expandir mensagens usando o status de execução em mensagens completas, para que você sempre receba mensagens MIDI completas de um driver de dispositivo de entrada MIDI.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravação de áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 




