---
title: Usando um retorno de chamada de evento para processar mensagens de driver
description: Usando um retorno de chamada de evento para processar mensagens de driver
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- áudio de onda, retorno de chamada de evento
- blocos de dados de áudio, retorno de chamada de evento
- áudio de onda, mensagens de driver de processamento
- blocos de dados de áudio, processando mensagens de driver
- Processando mensagens do driver
- Função CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640628"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Usando um retorno de chamada de evento para processar mensagens de driver

Para usar um retorno de chamada de evento, use a função [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para criar um evento de redefinição manual. Na chamada para a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , especifique o **\_ evento de retorno de chamada** para o parâmetro *fdwOpen* . Depois de chamar a função [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , mas antes de enviar dados de formato de onda-áudio para o dispositivo, coloque o evento em um estado não sinalizado chamando a função [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) . Em seguida, dentro de um loop que verifica se o sinalizador **WHDR \_ concluído** está definido no membro **dwFlags** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , chame a função [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , especificando como parâmetros o identificador de evento e um valor de tempo limite.

Como os retornos de chamada de evento não recebem notificações específicas de fechamento, conclusão ou abertura, um aplicativo pode ter que verificar o status do processo que está aguardando após o evento ocorrer. É possível que várias tarefas tenham sido concluídas no momento em que [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) retorna.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Blocos de dados de áudio](audio-data-blocks.md)
</dt> </dl>

 

 