---
description: Um processo pode monitorar um conjunto de eventos que ocorrem em um recurso de comunicação. Por exemplo, um aplicativo pode usar o monitoramento de eventos para determinar quando os sinais CTS (clear-to-send) e DSR (pronto para conjunto de dados) mudam de estado.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bcb257652723a2464ff66c862f574f6aeae621bc6459b55d250f785d0b0895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815486"
---
# <a name="communications-events"></a>Eventos de comunicação

Um processo pode monitorar um conjunto de eventos que ocorrem em um recurso de comunicação. Por exemplo, um aplicativo pode usar o monitoramento de eventos para determinar quando os sinais CTS (clear-to-send) e DSR (pronto para conjunto de dados) mudam de estado.

Um processo pode monitorar eventos em um determinado recurso de comunicação usando a [**função SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para criar uma máscara de evento. Para determinar a máscara de evento atual para um recurso de comunicação, um processo pode usar a [**função GetCommMask.**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) Os valores a seguir especificam eventos que podem ser monitorados.



| Valor           | Significado                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **QUEBRA \_ DE EV**   | Uma quebra na entrada foi detectada.                                                                                                                                                                                                                    |
| **CTS de EV \_**     | O sinal CTS (clear-to-send) mudou de estado.                                                                                                                                                                                                     |
| **EV \_ DSR**     | O sinal DSR (pronto para conjunto de dados) mudou de estado.                                                                                                                                                                                                    |
| **EV \_ ERR**     | Ocorreu um erro de status de linha. Os erros de status de linha **são CE \_ FRAME,** **CE \_ OVERRUN** e **CE \_ RXPARITY.**                                                                                                                                        |
| **EV \_ RING**    | Um indicador de anel foi detectado.                                                                                                                                                                                                                    |
| **\_RLSD de EV**    | O estado do sinal RLSD (receive-line-signal-detect) foi alterado.                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | Um caractere foi recebido e colocado no buffer de entrada.                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | O caractere de evento foi recebido e colocado no buffer de entrada. O caractere de evento é especificado na estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) do dispositivo, que é aplicada a uma porta serial usando a [**função SetCommState.**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) |
| **EV \_ TXEMPTY** | O último caractere no buffer de saída foi enviado.                                                                                                                                                                                                 |



 

Depois que um conjunto de eventos é especificado, um processo usa a [**função WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) para aguardar que um dos eventos ocorra. **WaitCommEvent** pode ser usado de forma síncrona ou como uma operação sobreposição. Para obter informações adicionais sobre como executar uma função como uma operação sobrecarada, consulte [Synchronization](/windows/desktop/Sync/synchronization).

Quando um dos eventos especificados na máscara de evento ocorre, o processo conclui a operação de espera e define uma variável de máscara de evento para indicar o tipo de evento detectado. Se [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) for chamado para um recurso de comunicação enquanto uma espera estiver pendente para esse recurso, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) retornará um erro.

A [**função WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) detecta eventos que ocorreram desde a última chamada para [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) ou **WaitCommEvent.** Por exemplo, se você especificar o evento **\_ RXCHAR** de EV como um evento de espera, uma chamada para **WaitCommEvent** será atendida se houver caracteres no buffer de entrada do driver que chegaram desde a última chamada para **WaitCommEvent** ou **SetCommMask**. Portanto, considerando o pseudocódigo a seguir, todos os caracteres recebidos entre T1 e T2 atenderão à próxima chamada para **WaitCommEvent.**


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Ao monitorar um evento que ocorre quando um sinal (CTS, DSR e assim por diante) altera o estado, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) relata a alteração, mas não o estado atual. Para consultar o estado atual dos sinais CTS (clear-to-send), DSR (data-set-ready), RLSD (receive-line-signal-detect) e indicador de anel, um processo pode usar a [**função GetCommModemStatus.**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)

 

 
