---
description: O TSPI inclui várias operações que iniciam o tempo de vida de um identificador de chamada.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Respostas assíncronas versus eventos em novos identificadores de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829131"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a>Respostas assíncronas versus eventos em novos identificadores de chamada

O TSPI inclui várias operações que iniciam o tempo de vida de um identificador de chamada. Se o provedor de serviços retornar o sucesso para tal operação, ele deverá preencher o identificador opaco do tipo **HDRVCALL**, que ele usa para a nova chamada antes de retornar. A TAPI nunca executa operações na chamada antes que o [*\_ procedimento de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondente seja recebido. Se o provedor de serviços retornar uma falha, o identificador se tornará automaticamente inválido (ou seja, sem [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)). Na verdade, a TAPI trata o identificador como "ainda não válido" até a conclusão assíncrona.

O provedor de serviços também deve tratar o identificador como "ainda não válido" até que o [*\_ procedimento de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondente seja recebido. Em outras palavras, ele não deve emitir nenhuma função de [*\_ evento de linha*](/windows/win32/api/tspi/nc-tspi-lineevent) para a nova chamada ou incluí-lo em contagens de chamadas em mensagens ou estruturas de dados de status para a linha.

O nível de TAPI também está em conformidade com essas restrições de ciclo de vida; um novo identificador de chamada não é retornado ou válido até a mensagem de [**\_ resposta de linha**](./line-reply.md) correspondente, e nenhum evento para a nova chamada é entregue ao aplicativo até depois da mensagem de resposta de linha \_ .

As operações de TSPI para as quais esse princípio de "tempo de vida de início" aplicam-se são as seguintes:

-   [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
