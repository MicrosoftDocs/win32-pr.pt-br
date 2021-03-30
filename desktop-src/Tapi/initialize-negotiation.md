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
# <a name="initialize_negotiation"></a><span data-ttu-id="f5f9f-103">INICIALIZAR \_ negociação</span><span class="sxs-lookup"><span data-stu-id="f5f9f-103">INITIALIZE\_NEGOTIATION</span></span>

<span data-ttu-id="f5f9f-104">O DataType da **\_ negociação de inicialização** é um valor especial do tipo **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f5f9f-104">The **INITIALIZE\_NEGOTIATION** datatype is a special value of type **DWORD**.</span></span> <span data-ttu-id="f5f9f-105">Ele pode ser passado como o parâmetro *dwDeviceID* nas funções [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) e [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) .</span><span class="sxs-lookup"><span data-stu-id="f5f9f-105">It can be passed as the *dwDeviceID* parameter in the [**TSPI\_lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) and [**TSPI\_phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) functions.</span></span> <span data-ttu-id="f5f9f-106">Isso indica que a TAPI pode negociar um número de versão de interface TSPI independente de quaisquer dispositivos específicos.</span><span class="sxs-lookup"><span data-stu-id="f5f9f-106">Doing so indicates that TAPI can negotiate a TSPI interface version number independent of any specific devices.</span></span>

 

 
