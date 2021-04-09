---
description: Um processo pode monitorar um conjunto de eventos que ocorrem em um recurso de comunicação. Por exemplo, um aplicativo pode usar o monitoramento de eventos para determinar quando os sinais CTS (Clear-to-send) e DSR (conjunto de dados prontos) mudam de estado.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089206"
---
# <a name="communications-events"></a>Eventos de comunicação

Um processo pode monitorar um conjunto de eventos que ocorrem em um recurso de comunicação. Por exemplo, um aplicativo pode usar o monitoramento de eventos para determinar quando os sinais CTS (Clear-to-send) e DSR (conjunto de dados prontos) mudam de estado.

Um processo pode monitorar eventos em um determinado recurso de comunicação usando a função [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para criar uma máscara de evento. Para determinar a máscara de evento atual para um recurso de comunicação, um processo pode usar a função [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) . Os valores a seguir especificam eventos que podem ser monitorados.



| Valor           | Significado                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **interrupção de EV \_**   | Uma quebra na entrada foi detectada.                                                                                                                                                                                                                    |
| **\_CTS EV**     | O estado de alteração do sinal CTS (Clear-to-send).                                                                                                                                                                                                     |
| **EV \_ DSR**     | O estado do DSR (Data-Set-Ready) foi alterado.                                                                                                                                                                                                    |
| **\_erro EV**     | Ocorreu um erro de status de linha. Os erros de status de linha são **\_ quadros CE**, **\_ saturação de CE** e **CE \_ RXPARITY**.                                                                                                                                        |
| **\_anel EV**    | Um indicador de anel foi detectado.                                                                                                                                                                                                                    |
| **\_RLSD EV**    | O estado do sinal de RLSD (recebimento-linha-sinal-detecção) mudou.                                                                                                                                                                                       |
| **\_RXCHAR EV**  | Um caractere foi recebido e colocado no buffer de entrada.                                                                                                                                                                                          |
| **\_RXFLAG EV**  | O caractere do evento foi recebido e colocado no buffer de entrada. O caractere do evento é especificado na estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) do dispositivo, que é aplicada a uma porta serial usando a função [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) . |
| **\_TXEMPTY EV** | O último caractere no buffer de saída foi enviado.                                                                                                                                                                                                 |



 

Depois que um conjunto de eventos é especificado, um processo usa a função [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) para aguardar a ocorrência de um dos eventos. **WaitCommEvent** pode ser usado de forma síncrona ou como uma operação sobreposta. Para obter informações adicionais sobre como executar uma função como uma operação sobreposta, consulte [sincronização](/windows/desktop/Sync/synchronization).

Quando um dos eventos especificados na máscara de evento ocorre, o processo conclui a operação de espera e define uma variável de máscara de evento para indicar o tipo de evento detectado. Se o [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) for chamado para um recurso de comunicação enquanto uma espera estiver pendente para esse recurso, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) retornará um erro.

A função [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) detecta eventos que ocorreram desde a última chamada para [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) ou **WaitCommEvent**. Por exemplo, se você especificar o **evento \_ RXCHAR de EV** como um evento de satisfação de espera, uma chamada para **WaitCommEvent** será satisfeita se houver caracteres no buffer de entrada do driver que chegaram desde a última chamada para **WaitCommEvent** ou **SetCommMask**. Assim, considerando o pseudocódigo a seguir, todos os caracteres recebidos entre T1 e T2 atenderão à próxima chamada para **WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Ao monitorar um evento que ocorre quando um sinal (CTS, DSR e assim por diante) muda de estado, o [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) relata a alteração, mas não o estado atual. Para consultar o estado atual dos sinais CTS (Clear-to-send), DSR (conjunto de dados pronto), RLSD (Receive-line-Signal-Detect) e Ring Indicator, um processo pode usar a função [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) .

 

 
