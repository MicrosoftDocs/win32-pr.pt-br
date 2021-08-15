---
title: Usando um retorno de chamada de evento para processar mensagens de driver
description: Usando um retorno de chamada de evento para processar mensagens de driver
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- waveform audio,event callback
- blocos de dados de áudio, retorno de chamada de evento
- áudio waveform, ing driver messages
- blocos de dados de áudio, mensagens de driver de processamento
- ing driver messages
- Função CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5bdbfe46fed9fa9124a031e90af3bfefb983caf6743415d90c645afc42c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801196"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Usando um retorno de chamada de evento para processar mensagens de driver

Para usar um retorno de chamada de evento, use a [**função CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para criar um evento de redefinição manual. Na chamada para a [**função waveOutOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) especifique **CALLBACK \_ EVENT** para o *parâmetro fdwOpen.* Depois de chamar a função [**waveOutPrepareHeader,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) mas antes de enviar dados waveform-audio para o dispositivo, coloque o evento em um estado sem sinal chamando a [**função ResetEvent.**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) Em seguida, dentro de um loop que verifica se o sinalizador **WHDR \_ DONE** está definido no membro **dwFlags** da estrutura [**WAVEHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) chame a função [WaitForSingleObject,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) especificando como parâmetros o handle de evento e um valor de tempo-out.

Como os retornos de chamada de evento não recebem notificações específicas próximas, feitas ou abertas, um aplicativo pode ter que verificar o status do processo que está aguardando após o evento ocorrer. É possível que várias tarefas tenham sido concluídas pelo tempo [**que WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) retorna.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Blocos de dados de áudio](audio-data-blocks.md)
</dt> </dl>

 

 