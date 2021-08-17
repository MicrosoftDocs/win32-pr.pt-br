---
title: Blocos de dados de áudio
description: Blocos de dados de áudio
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- áudio de multimídia, blocos de dados
- áudio, blocos de dados
- áudio de onda, blocos de dados
- blocos de dados de áudio, sobre
- Estrutura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a4a0c7236c52854911b51677cf792fa504371fb18900ac947e8fdf1391bd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941750"
---
# <a name="audio-data-blocks"></a>Blocos de dados de áudio

As funções [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) e [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) exigem que os aplicativos aloquem blocos de dados para passar para os drivers de dispositivo para fins de gravação ou reprodução. Ambas as funções usam a estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para descrever seu bloco de dados.

Antes de usar uma dessas funções para passar um bloco de dados para um driver de dispositivo, você deve alocar memória para o bloco de dados e a estrutura de cabeçalho que descreve o bloco de dados. Os cabeçalhos podem ser preparados e despreparados usando as funções a seguir.



| Função                                                 | Descrição                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Prepara um bloco de dados de entrada de wave-áudio.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Limpa a preparação em um bloco de dados de entrada de forma de onda-áudio.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Prepara um bloco de dados de saída de wave-áudio.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Limpa a preparação em um bloco de dados de saída de wave-áudio. |



 

Antes de passar um bloco de dados de áudio para um driver de dispositivo, você deve preparar o bloco de dados passando-o para [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) ou [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader). Quando o driver de dispositivo for concluído com o bloco de dados e o retornar, você deverá limpar essa preparação passando o bloco de dados para [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) ou [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) antes que qualquer memória alocada possa ser liberada.

A menos que os dados de entrada e saída de wave-áudio sejam pequenos o suficiente para serem contidos em um único bloco de dados, os aplicativos devem fornecer continuamente o driver de dispositivo com blocos de dados até que a reprodução ou gravação seja concluída.

Mesmo que um único bloco de dados seja usado, um aplicativo deve ser capaz de determinar quando um driver de dispositivo é concluído com o bloco de dados para que o aplicativo possa liberar a memória associada ao bloco de dados e à estrutura de cabeçalho. Há várias maneiras de determinar quando um driver de dispositivo é concluído com um bloco de dados:

-   Especificando uma função de retorno de chamada para receber uma mensagem enviada pelo driver quando ela é concluída com um bloco de dados
-   Usando um retorno de chamada de evento
-   Especificando uma janela ou thread para receber uma mensagem enviada pelo driver quando ele é concluído com um bloco de dados
-   Sondando o \_ bit WHDR realizado no membro **dwFlags** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) enviada com cada bloco de dados

Se um aplicativo não obtiver um bloco de dados para o driver de dispositivo quando necessário, poderá haver uma lacuna audível na reprodução ou uma perda de informações registradas de entrada. Isso requer pelo menos um esquema de buffer duplo — mantendo pelo menos um bloco de dados à frente do driver de dispositivo.

Os tópicos a seguir descrevem maneiras de determinar quando um driver de dispositivo é concluído com um bloco de dados:

Usando uma função de retorno de chamada para processar mensagens de driver

-   [Usando uma função de retorno de chamada para processar mensagens de driver](using-a-callback-function-to-process-driver-messages.md)
-   [Usando um retorno de chamada de evento para processar mensagens de driver](using-an-callback-to-process-driver-messages.md)
-   [Usando uma janela ou thread para processar mensagens do driver](using-a-window-or-thread-to-process-driver-messages.md)
-   [Gerenciando blocos de dados por sondagem](managing-data-blocks-by-polling.md)

 

 