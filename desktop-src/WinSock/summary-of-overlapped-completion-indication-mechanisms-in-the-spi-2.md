---
description: Resumo dos mecanismos de indicação de conclusão sobreposta no SPI do Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Resumo dos mecanismos de indicação de conclusão sobreposta no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090354"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Resumo dos mecanismos de indicação de conclusão sobreposta no SPI

A tabela a seguir resume a semântica de conclusão para um Soquete sobreposto, mostrando a várias combinações de *lpOverlapped*, **hEvent** e *lpCompletionRoutine*.



| *lpOverlapped* | **hEvent**     | *lpCompletionRoutine* | Indicação de conclusão                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULO           | Não aplicável | Ignored               | A operação é concluída de forma síncrona, ou seja, se comporta como se fosse um soquete não sobreposto.                                                                                                                                 |
| não nulo       | NULO           | NULO                  | A operação é concluída sobreposta, mas não há nenhum mecanismo de conclusão com suporte do Windows Sockets 2. O mecanismo de porta de conclusão (se houver suporte) pode ser usado nesse caso, caso contrário, não haverá nenhuma notificação de conclusão. |
| não nulo       | não nulo       | NULO                  | A operação é concluída sobreposta, notificação por objeto de evento de sinalização.                                                                                                                                                      |
| não nulo       | Ignored        | não nulo              | A operação é concluída sobreposta, notificação pela rotina de conclusão do agendamento.                                                                                                                                               |



 

 

 



