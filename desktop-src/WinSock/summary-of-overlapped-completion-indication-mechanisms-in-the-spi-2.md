---
description: Resumo dos mecanismos de indicação de conclusão sobressalo na SPI Windows (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Resumo dos mecanismos de indicação de conclusão sobressalo na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cb7cc0f354c018ab7a766ea5b71877877fbae6b36cdd86e95f6d1bf9998140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993246"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Resumo dos mecanismos de indicação de conclusão sobressalo na SPI

A tabela a seguir resume a semântica de conclusão para um soquete sobressalo, mostrando a combinação de *lpOverlapped*, **hEvent** e *lpCompletionRoutine.*



| *Lpoverlapped* | **Hevent**     | *Lpcompletionroutine* | Indicação de conclusão                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULO           | Não se aplica | Ignored               | A operação é concluída de forma síncrona, ou seja, ela se comporta como se fosse um soquete não mapeado.                                                                                                                                 |
| not NULL       | NULO           | NULO                  | A operação é concluída sobrecarro, mas não há Windows mecanismo de conclusão com suporte para Soquetes 2. O mecanismo de porta de conclusão (se houver suporte) pode ser usado nesse caso; caso contrário, não haverá notificação de conclusão. |
| not NULL       | not NULL       | NULO                  | A operação é concluída sobrecarrada, notificação sinalizando o objeto de evento.                                                                                                                                                      |
| not NULL       | Ignored        | not NULL              | A operação é concluída sobrecarrada, notificação agendando a rotina de conclusão.                                                                                                                                               |



 

 

 



