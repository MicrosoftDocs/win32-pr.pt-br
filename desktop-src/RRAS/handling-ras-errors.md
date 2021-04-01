---
title: Manipulando erros de RAS
description: Quando ocorre um erro, o Gerenciador de conexões de acesso remoto invoca o manipulador de notificação do cliente.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS do serviço de acesso remoto, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636691"
---
# <a name="handling-ras-errors"></a><span data-ttu-id="509c5-104">Manipulando erros de RAS</span><span class="sxs-lookup"><span data-stu-id="509c5-104">Handling RAS Errors</span></span>

<span data-ttu-id="509c5-105">Quando ocorre um erro, o Gerenciador de conexões de acesso remoto invoca o manipulador de notificação do cliente.</span><span class="sxs-lookup"><span data-stu-id="509c5-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="509c5-106">A notificação indica o estado da conexão quando o erro ocorreu e um código que identifica o erro.</span><span class="sxs-lookup"><span data-stu-id="509c5-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="509c5-107">Nesses casos, o manipulador de notificação deve chamar [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para encerrar a conexão RAS.</span><span class="sxs-lookup"><span data-stu-id="509c5-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="509c5-108">Os códigos de erro que identificam erros de RAS são definidos no arquivo Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="509c5-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="509c5-109">O cliente RAS pode usar a função [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) para obter uma cadeia de caracteres de exibição que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="509c5-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="509c5-110">Consulte [códigos de erro de roteamento e acesso remoto](routing-and-remote-access-error-codes.md) para obter uma descrição desses erros.</span><span class="sxs-lookup"><span data-stu-id="509c5-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




