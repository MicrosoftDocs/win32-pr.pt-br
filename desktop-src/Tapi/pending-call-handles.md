---
description: Um provedor de serviços é necessário para criar um ou mais identificador de chamada (variáveis do tipo HDRVCALL) sempre que a TAPI chama uma das funções a seguir.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Alças de chamada pendentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d082c0b9111d6d58debacec01d20ffe9af2d024aafd61b3f1085267e62d3d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518580"
---
# <a name="pending-call-handles"></a>Alças de chamada pendentes

Um provedor de serviços é necessário para criar um ou mais identificadores de chamada (variáveis do tipo [HDRVCALL](hdrvline.md)) sempre que TAPI chama uma destas funções: [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI \_ lineSetupTransfer e**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer) [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Quando um provedor de serviços recebe essa chamada, o provedor de serviços deve definir a variável fornecida pela TAPI como o valor do handle antes de retornar da chamada. A TAPI considera esse "manipulador de chamada pendente" como provisamente válido. Quando o provedor de serviços realmente cria a chamada, ele deve chamar o retorno de [**chamada ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) para validar formalmente o handle.

Se TAPI chamar a função [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) antes que o provedor de serviços valide formalmente um alça de chamada pendente, o provedor de serviços deverá interromper todo o processamento posterior associado ao handle de chamada e chamar a função de retorno de chamada [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) usando o valor de erro LINEERR \_ OPERATIONFAILED.

 

 
