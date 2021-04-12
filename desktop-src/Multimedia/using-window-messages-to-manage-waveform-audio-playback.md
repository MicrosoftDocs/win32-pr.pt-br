---
title: Usando mensagens de janela para gerenciar Waveform-Audio reprodução
description: Usando mensagens de janela para gerenciar Waveform-Audio reprodução
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- áudio de onda, gerenciamento de reprodução com mensagens
- Wave-interface de áudio, gerenciando a reprodução com mensagens
- reprodução de formato de onda-arquivos de áudio, gerenciamento de reprodução com mensagens
- áudio de onda, mensagens
- Wave-interface de áudio, mensagens
- executando a onda-arquivos de áudio, mensagens
- MM_WOM_CLOSE mensagem
- MM_WOM_DONE mensagem
- MM_WOM_OPEN mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293966"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Usando mensagens de janela para gerenciar Waveform-Audio reprodução

As mensagens a seguir podem ser enviadas a uma função de procedimento de janela para gerenciar a reprodução de formato wave-áudio.



| Mensagem                                | Descrição                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ wom \_ fechar**](mm-wom-close.md) | Enviado quando o dispositivo é fechado usando a função [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .                                 |
| [**MM \_ wom \_ concluído**](mm-wom-done.md)   | Enviado quando o driver de dispositivo é concluído com um bloco de dados enviado usando a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . |
| [**MM \_ wom \_ abertos**](mm-wom-open.md)   | Enviado quando o dispositivo é aberto usando a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .                                   |



 

Um parâmetro *wParam* e *lParam* está associado a cada uma dessas mensagens. O parâmetro *wParam* sempre especifica um identificador do dispositivo Open Wave-Audio. Para a mensagem [**mm \_ wom \_ concluído**](mm-wom-done.md) , *lParam* especifica um ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o bloco de dados concluído. O parâmetro *lParam* não é usado para as mensagens [**mm \_ wom \_ Close**](mm-wom-close.md) e [**mm \_ wom \_ Open**](mm-wom-open.md) .

A mensagem mais útil é provavelmente MM \_ wom \_ concluído. Quando essa mensagem sinaliza que a reprodução de um bloco de dados é concluída, você pode limpar e liberar o bloco de dados. A menos que você precise alocar memória ou inicializar variáveis, provavelmente não precisará processar as \_ mensagens mm wom \_ abrir e mm \_ wom \_ fechar.

A função de retorno de chamada para dispositivos de saída de wave-áudio é fornecida pelo aplicativo. Para obter informações sobre essa função de retorno de chamada, consulte a função [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .

 

 