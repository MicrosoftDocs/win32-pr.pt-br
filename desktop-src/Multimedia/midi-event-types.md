---
title: Tipos de evento MIDI
description: Tipos de evento MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- MIDI (interface digital de instrumento musical), tipos de evento
- MIDI (interface digital de instrumentos musicais), tipos de evento
- Estrutura MIDIEVENT
- buffers de fluxo, tipos de evento MIDI
- Tipos de evento MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007527"
---
# <a name="midi-event-types"></a>Tipos de evento MIDI

O membro **dwEvent** da estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) descreve o evento MIDI que deve ocorrer. Eventos curtos se encaixam totalmente nesse membro. Eventos longos exigem um ou mais valores doubleword além do membro **dwEvent** para armazenar as descrições de eventos.

O byte alto do membro **dwEvent** contém informações sobre se o evento é longo ou curto e se um retorno de chamada é gerado junto com o evento. Além disso, esse byte é usado para descrever o tipo de evento. Os 24 bits restantes do membro **dwEvent** são usados para conter os parâmetros de evento (para mensagens curtas) ou para conter o comprimento dos parâmetros de evento (para mensagens longas). Para extrair informações do membro **dwEvent** , use as macros [**\_ EVENTTYPE MEVT**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) e [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .

Para obter uma descrição dos tipos de evento predefinidos, consulte o material de referência para a estrutura **MIDIEVENT** .

 

 