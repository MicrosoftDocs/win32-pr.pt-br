---
description: A maioria das operações Get e Set lidam apenas com um componente de informações. A função phoneGetStatus retorna informações de status completas sobre um dispositivo de telefone para um aplicativo.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Status (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828329"
---
# <a name="status-telephony-api"></a><span data-ttu-id="bd935-104">Status (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="bd935-104">Status (Telephony API)</span></span>

<span data-ttu-id="bd935-105">A maioria das operações Get e Set lidam apenas com um componente de informações.</span><span class="sxs-lookup"><span data-stu-id="bd935-105">Most of the get and set operations deal with one component of information only.</span></span> <span data-ttu-id="bd935-106">A função [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) retorna informações de status completas sobre um dispositivo de telefone para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd935-106">The [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) function returns complete status information about a phone device to an application.</span></span>

<span data-ttu-id="bd935-107">Como mencionado anteriormente, sempre que um item de status é alterado no dispositivo de telefone, uma mensagem de [**\_ estado do telefone**](phone-state.md) é enviada para a função do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd935-107">As mentioned earlier, whenever a status item changes on the phone device, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function.</span></span> <span data-ttu-id="bd935-108">Os parâmetros dessa mensagem incluem um identificador para o dispositivo de telefone e uma indicação do item de status que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="bd935-108">This message's parameters include a handle to the phone device and an indication of the status item that changed.</span></span>

<span data-ttu-id="bd935-109">Um aplicativo pode usar [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) para selecionar as alterações de status específicas para as quais deseja ser notificado.</span><span class="sxs-lookup"><span data-stu-id="bd935-109">An application can use [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) to select the specific status changes for which it wants to be notified.</span></span> <span data-ttu-id="bd935-110">De modo correspondente, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) retorna as alterações de status para as quais o aplicativo deseja ser notificado.</span><span class="sxs-lookup"><span data-stu-id="bd935-110">Correspondingly, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) returns the status changes for which the application wants to be notified.</span></span>

 

 



