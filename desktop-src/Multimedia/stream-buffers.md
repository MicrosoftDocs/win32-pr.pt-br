---
title: Buffers de fluxo
description: Buffers de fluxo
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimídia, buffers de fluxo
- multimídia, buffers de fluxo
- áudio de multimídia, buffers de fluxo
- áudio, buffers de fluxo
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- buffers de fluxo, sobre
- Estrutura MIDIHDR
- Estrutura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac10d024089a856880097c5d87ae501d62655f858030535ff4128f1fd9d31447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037066"
---
# <a name="stream-buffers"></a>Buffers de fluxo

Os aplicativos podem usar buffers de fluxo para enviar fluxos de eventos MIDI para um dispositivo. Cada buffer de fluxo é um bloco de memória apontado por uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) . Esse bloco de memória contém dados para um ou mais eventos de MIDI, cada um deles definido por uma estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . Um aplicativo controla o buffer chamando as funções de manipulação de fluxo, como [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)e [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).

-   [Formato de buffer de fluxo](stream-buffer-format.md)
-   [Informações de tempo](timing-information.md)
-   [Tipos de evento MIDI](midi-event-types.md)
-   [Fluxos MIDI](midi-streams.md)

 

 