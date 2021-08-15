---
title: Usando uma janela ou thread para gerenciar a reprodução em buffer
description: Usando uma janela ou thread para gerenciar a reprodução em buffer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- MIDI (Instrument Digital Interface Instrument), reprodução em buffer
- MIDI (Interface Digital do Instrument Instrument), reprodução em buffer
- reproduzindo arquivos MIDI, reprodução em buffer
- reprodução em buffer
- MM_MOM_CLOSE mensagem
- MM_MOM_DONE mensagem
- MM_MOM_OPEN mensagem
- MIDI (Interface Digital do Instrument Instrument), enviando mensagens
- MIDI (Interface Digital do Instrument Instrument), enviando mensagens
- reprodução de arquivos MIDI, envio de mensagens
- enviando mensagens MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc0acb39090a640d60539542a439111287faef246adf64aef7ee12ced3ae09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801250"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Usando uma janela ou thread para gerenciar a reprodução em buffer

As mensagens a seguir podem ser enviadas para uma janela ou thread para gerenciar a reprodução de mensagens exclusivas do sistema MIDI ou buffers de fluxo.



| Valor                                  | Significado                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MOM \_ CLOSE**](mm-mom-close.md) | Enviado quando o dispositivo é fechado usando a [**função midiOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)                                                                               |
| [**MM \_ MOM \_ DONE**](mm-mom-done.md)   | Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a [**função midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) |
| [**MM \_ MOM \_ OPEN**](mm-mom-open.md)   | Enviado quando o dispositivo é aberto usando a [**função midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)                                                                                 |



 

Um *parâmetro wParam* e *um parâmetro lParam* são associados a cada uma dessas mensagens. O *parâmetro wParam* sempre especifica o handle de um dispositivo MIDI aberto. Para [**MM \_ MOM \_ DONE,**](mm-mom-done.md) *lParam* especifica um endereço de uma [**estrutura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o bloco de dados concluído. O *parâmetro lParam* não éusado para [**MM MOM \_ \_ CLOSE**](mm-mom-close.md) e [**MM MOM \_ \_ OPEN.**](mm-mom-open.md)

A mensagem mais útil provavelmente é MM \_ MOM \_ DONE. A menos que você precise alocar memória ou inicializar variáveis, provavelmente não será necessário processar MM \_ MOM OPEN e MM MOM \_ \_ \_ CLOSE. Quando a reprodução de um bloco de dados for concluída, você poderá limpar e liberar o bloco de dados.

 

 