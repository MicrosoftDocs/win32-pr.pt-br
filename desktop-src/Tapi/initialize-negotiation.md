---
description: O DataType da negociação de inicialização \_ é um valor especial do tipo DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647629"
---
# <a name="initialize_negotiation"></a>INICIALIZAR \_ negociação

O DataType da **\_ negociação de inicialização** é um valor especial do tipo **DWORD**. Ele pode ser passado como o parâmetro *dwDeviceID* nas funções [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) e [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) . Isso indica que a TAPI pode negociar um número de versão de interface TSPI independente de quaisquer dispositivos específicos.

 

 
