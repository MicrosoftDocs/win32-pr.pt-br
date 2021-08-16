---
description: O DataType da negociação de inicialização \_ é um valor especial do tipo DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24763b9214dcffab99c83f24028e451a33d70dd7e4210f4eff64b0c39306d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762773"
---
# <a name="initialize_negotiation"></a>INICIALIZAR \_ negociação

O DataType da **\_ negociação de inicialização** é um valor especial do tipo **DWORD**. Ele pode ser passado como o parâmetro *dwDeviceID* nas funções [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) e [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) . Isso indica que a TAPI pode negociar um número de versão de interface TSPI independente de quaisquer dispositivos específicos.

 

 
