---
title: Usando mensagens de janela para gerenciar Waveform-Audio reprodução
description: Usando mensagens de janela para gerenciar Waveform-Audio reprodução
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- waveform audio, gerenciando a reprodução com mensagens
- interface waveform-audio, gerenciando a reprodução com mensagens
- reproduzindo arquivos waveform-audio, gerenciando a reprodução com mensagens
- waveform audio,messages
- interface waveform-audio,messages
- reprodução de arquivos de forma de onda de áudio, mensagens
- MM_WOM_CLOSE mensagem
- MM_WOM_DONE mensagem
- MM_WOM_OPEN mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31d8a88cb74953a1d38285a77b18ac25cd7495c3e29e71c5259551b5c2c3453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135881"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Usando mensagens de janela para gerenciar Waveform-Audio reprodução

As mensagens a seguir podem ser enviadas a uma função de procedimento de janela para gerenciar a reprodução de áudio de forma de onda.



| Mensagem                                | Descrição                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ CLOSE**](mm-wom-close.md) | Enviado quando o dispositivo é fechado usando a [**função waveOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)                                 |
| [**MM \_ WOM \_ DONE**](mm-wom-done.md)   | Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a [**função waveOutWrite.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) |
| [**MM \_ WOM \_ OPEN**](mm-wom-open.md)   | Enviado quando o dispositivo é aberto usando a [**função waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)                                   |



 

Um *parâmetro wParam* *e lParam* está associado a cada uma dessas mensagens. O *parâmetro wParam* sempre especifica uma alça do dispositivo open waveform-audio. Para a [**mensagem MM \_ WOM \_ DONE,**](mm-wom-done.md) *lParam* especifica um ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o bloco de dados concluído. O *parâmetro lParam* não éusado para as mensagens [**MM \_ WOM \_ CLOSE**](mm-wom-close.md) e [**MM \_ WOM \_ OPEN.**](mm-wom-open.md)

A mensagem mais útil provavelmente é MM \_ WOM \_ DONE. Quando essa mensagem sinaliza que a reprodução de um bloco de dados está concluída, você pode limpar e liberar o bloco de dados. A menos que você precise alocar memória ou inicializar variáveis, provavelmente não será necessário processar as mensagens MM WOM OPEN e \_ \_ MM \_ WOM \_ CLOSE.

A função de retorno de chamada para dispositivos de saída waveform-audio é fornecida pelo aplicativo. Para obter informações sobre essa função de retorno de chamada, consulte a [**função waveOutProc.**](/previous-versions//dd743869(v=vs.85))

 

 