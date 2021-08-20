---
title: Usando mensagens de janela para gerenciar a gravação de Waveform-Audio
description: Usando mensagens de janela para gerenciar a gravação de Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- áudio de formato de onda, gerenciando a gravação com mensagens
- Wave-interface de áudio, gerenciando a gravação com mensagens
- gravando áudio de onda, gerenciando a gravação com mensagens
- áudio de onda, mensagens
- Wave-interface de áudio, mensagens
- gravando áudio de onda, mensagens
- MM_WIM_CLOSE mensagem
- MM_WIM_DATA mensagem
- MM_WIM_OPEN mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c709df27be25a8a3f4c5a9be6528e28b4e8bab9251b04b6c397a7ef3fc8efd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135648"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Usando mensagens de janela para gerenciar a gravação de Waveform-Audio

As mensagens a seguir podem ser enviadas a uma função de procedimento de janela para gerenciar a gravação de formato wave-áudio.



| Mensagem                                | Descrição                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ de \_ fechamento de Wim**](mm-wim-close.md) | Enviado quando o dispositivo é fechado usando a função [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .                                     |
| [**\_dados wim \_ mm**](mm-wim-data.md)   | Enviado quando o driver de dispositivo é concluído com um buffer enviado usando a função [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) . |
| [**Wim de MM \_ \_ aberto**](mm-wim-open.md)   | Enviado quando o dispositivo é aberto usando a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .                                       |



 

O parâmetro *lParam* de [**\_ \_ dados wim mm**](mm-wim-data.md) especifica um ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o buffer. Esse buffer pode não estar completamente cheio com dados de wave-áudio; a gravação pode parar antes de o buffer ser preenchido. Use o membro **dwBytesRecorded** da estrutura **WAVEHDR** para determinar a quantidade de dados válidos presentes no buffer.

A mensagem mais útil é, provavelmente, [**\_ \_ dados de Wim mm**](mm-wim-data.md). Quando o aplicativo terminar de usar o bloco de dados enviado pelo driver de dispositivo, você poderá limpar e liberar o bloco de dados. A menos que você precise alocar memória ou inicializar variáveis, provavelmente não precisará usar as mensagens de [**\_ \_ fechamento**](mm-wim-close.md) do WIM Open e mm do [**\_ \_ wim mm**](mm-wim-open.md) .

A função de retorno de chamada para dispositivos de entrada de wave-áudio é fornecida pelo aplicativo. Para obter informações sobre essa função de retorno de chamada, consulte a função [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 