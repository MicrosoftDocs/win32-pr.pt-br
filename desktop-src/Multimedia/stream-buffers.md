---
title: Buffers de fluxo
description: Buffers de fluxo
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Multimídia do Windows, buffers de fluxo
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
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640612"
---
# <a name="stream-buffers"></a>Buffers de fluxo

Os aplicativos podem usar buffers de fluxo para enviar fluxos de eventos MIDI para um dispositivo. Cada buffer de fluxo é um bloco de memória apontado por uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) . Esse bloco de memória contém dados para um ou mais eventos de MIDI, cada um deles definido por uma estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . Um aplicativo controla o buffer chamando as funções de manipulação de fluxo, como [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)e [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).

-   [Formato de buffer de fluxo](stream-buffer-format.md)
-   [Informações de tempo](timing-information.md)
-   [Tipos de evento MIDI](midi-event-types.md)
-   [Fluxos de MIDI](midi-streams.md)

 

 