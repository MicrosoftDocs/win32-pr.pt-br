---
description: Para impedir que chamadas sem proprietário estejam no sistema de telefonia, a TAPI descartará chamadas que tenham sido sinalizadas de um provedor de serviços se não for possível identificar um aplicativo para ser o proprietário inicial da chamada.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Chamadas sem proprietário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757195"
---
# <a name="unowned-calls"></a><span data-ttu-id="39e11-103">Chamadas sem proprietário</span><span class="sxs-lookup"><span data-stu-id="39e11-103">Unowned Calls</span></span>

<span data-ttu-id="39e11-104">Para impedir que chamadas sem proprietário estejam no sistema de telefonia, a TAPI descartará chamadas que tenham sido sinalizadas de um provedor de serviços se não for possível identificar um aplicativo para ser o proprietário inicial da chamada.</span><span class="sxs-lookup"><span data-stu-id="39e11-104">To prevent unowned calls from being in the telephony system, TAPI drops calls that have been signaled up from a service provider if it cannot identify an application to be the initial owner of the call.</span></span> <span data-ttu-id="39e11-105">Na TAPI versão 2,0 e posterior, a TAPI chama a função [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) para descartar a chamada.</span><span class="sxs-lookup"><span data-stu-id="39e11-105">In TAPI version 2.0 and later, TAPI calls the [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) function to drop the call.</span></span>

<span data-ttu-id="39e11-106">O provedor de serviços pode saber com antecedência se há um aplicativo disponível para apropriar-se de uma nova chamada.</span><span class="sxs-lookup"><span data-stu-id="39e11-106">The service provider can know in advance whether or not there is an application available to take ownership of a new call.</span></span> <span data-ttu-id="39e11-107">A TAPI sempre informa ao provedor de serviços os tipos de mídia para os quais há um aplicativo disponível usando a função [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .</span><span class="sxs-lookup"><span data-stu-id="39e11-107">TAPI always informs the service provider of the media types for which there is an application available by using the [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) function.</span></span>

<span data-ttu-id="39e11-108">Por exemplo, se um provedor de serviços determinar que há uma chamada ativa na linha que tem o \_ modo LINEMEDIAMODE INTERACTIVEVOICE, ele deverá verificar a detecção de mídia padrão antes de gerar as mensagens [**\_ NewCall de linha**](line-newcall.md) e [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="39e11-108">For example, if a service provider determines that there is an active call on the line having LINEMEDIAMODE\_INTERACTIVEVOICE mode, it should check the default media detection before generating the [**LINE\_NEWCALL**](line-newcall.md) and [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span></span> <span data-ttu-id="39e11-109">Se a detecção de mídia padrão mostrar que nenhum aplicativo está procurando uma \_ chamada LINEMEDIAMODE INTERACTIVEVOICE, o provedor de serviços não deverá enviar as mensagens, pois a TAPI a removerá imediatamente.</span><span class="sxs-lookup"><span data-stu-id="39e11-109">If the default media detection shows that no application is looking for a LINEMEDIAMODE\_INTERACTIVEVOICE call, the service provider should not send the messages because TAPI will immediately drop it.</span></span>

 

 
