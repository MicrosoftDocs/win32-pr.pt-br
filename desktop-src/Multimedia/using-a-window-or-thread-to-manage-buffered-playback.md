---
title: Usando uma janela ou thread para gerenciar a reprodução em buffer
description: Usando uma janela ou thread para gerenciar a reprodução em buffer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- MIDI (interface digital de instrumento musical), reprodução em buffer
- MIDI (interface digital de instrumentos musicais), reprodução em buffer
- executando arquivos MIDI, reprodução em buffer
- reprodução em buffer
- MM_MOM_CLOSE mensagem
- MM_MOM_DONE mensagem
- MM_MOM_OPEN mensagem
- MIDI (interface digital de instrumento musical), enviando mensagens
- MIDI (interface digital de instrumentos musicais), enviando mensagens
- executando arquivos MIDI, enviando mensagens
- enviando mensagens MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294019"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Usando uma janela ou thread para gerenciar a reprodução em buffer

As mensagens a seguir podem ser enviadas para uma janela ou thread para gerenciar a reprodução de mensagens exclusivas do sistema MIDI ou buffers de fluxo.



| Valor                                  | Significado                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_fechamento do MOM mm \_**](mm-mom-close.md) | Enviado quando o dispositivo é fechado usando a função [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**\_Mom mm \_ concluído**](mm-mom-done.md)   | Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a função [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) ou [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**\_Mom mm \_ aberto**](mm-mom-open.md)   | Enviado quando o dispositivo é aberto usando a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Um parâmetro *wParam* e um parâmetro *lParam* são associados a cada uma dessas mensagens. O parâmetro *wParam* sempre especifica o identificador de um dispositivo MIDI aberto. Para [**o \_ Mom mm \_ concluído**](mm-mom-done.md), *lParam* especifica um endereço de uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o bloco de dados concluído. O parâmetro *lParam* não é usado para Mom [**mm do MOM de \_ \_ fechamento**](mm-mom-close.md) e [**mm \_ \_ aberto**](mm-mom-open.md).

A mensagem mais útil é provavelmente MM \_ Mom \_ concluído. A menos que você precise alocar memória ou inicializar variáveis, provavelmente não precisa processar MM \_ Mom \_ Open e mm \_ Mom \_ Close. Quando a reprodução de um bloco de dados é concluída, você pode limpar e liberar o bloco de dados.

 

 