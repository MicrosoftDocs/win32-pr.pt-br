---
description: Um provedor de serviços é necessário para criar um ou mais identificadores de chamada (variáveis do tipo HDRVCALL) sempre que a TAPI chama uma das funções a seguir.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Identificadores de chamada pendentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c021ff10f2a1a812c46fb77663ac1a3a3a8d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779449"
---
# <a name="pending-call-handles"></a>Identificadores de chamada pendentes

Um provedor de serviços é necessário para criar um ou mais identificadores de chamada (variáveis do tipo [HDRVCALL](hdrvline.md)) sempre que a TAPI chama uma dessas funções: [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)e [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Quando um provedor de serviços recebe tal chamada, o provedor de serviços deve definir a variável fornecida pela TAPI para o valor do identificador antes de retornar da chamada. A TAPI considera que o "identificador de chamada pendente" é válido provisoriamente. Quando o provedor de serviços realmente cria a chamada, ele deve chamar o retorno de chamada de [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) para validar formalmente o identificador.

Se a TAPI chamar a função [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) antes de o provedor de serviços validar formalmente um identificador de chamada pendente, o provedor de serviços deverá interromper todo o processamento adicional associado ao identificador de chamada e chamar a função de retorno de chamadas de [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) usando o valor de erro LINEERR \_ OPERATIONFAILED.

 

 
