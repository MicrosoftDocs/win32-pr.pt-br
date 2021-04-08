---
description: 'A API de gráfico usa os seguintes retornos de chamada:'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Retornos de chamada da API de gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011026"
---
# <a name="graphing-api-callbacks"></a><span data-ttu-id="3948e-103">Retornos de chamada da API de gráfico</span><span class="sxs-lookup"><span data-stu-id="3948e-103">Graphing API Callbacks</span></span>

<span data-ttu-id="3948e-104">A API de gráfico usa os seguintes retornos de chamada:</span><span class="sxs-lookup"><span data-stu-id="3948e-104">The Graphing API uses the following callbacks:</span></span>



| <span data-ttu-id="3948e-105">Callback</span><span class="sxs-lookup"><span data-stu-id="3948e-105">Callback</span></span>                                                          | <span data-ttu-id="3948e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3948e-106">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3948e-107">*PFNPEER \_ \_ dados de segurança gratuitos \_*</span><span class="sxs-lookup"><span data-stu-id="3948e-107">*PFNPEER\_FREE\_SECURITY\_DATA*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | <span data-ttu-id="3948e-108">Especifica a função que a infraestrutura de grafo de pares chama para liberar dados retornados [*pelo \_ \_ registro seguro de PFNPEER*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) e retornos de chamada de [*PFNPEER \_ Validate \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) .</span><span class="sxs-lookup"><span data-stu-id="3948e-108">Specifies the function that the Peer Graphing Infrastructure calls to free data returned by [*PFNPEER\_SECURE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) and [*PFNPEER\_VALIDATE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) callbacks.</span></span> |
| [<span data-ttu-id="3948e-109">*\_registro seguro do PFNPEER \_*</span><span class="sxs-lookup"><span data-stu-id="3948e-109">*PFNPEER\_SECURE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | <span data-ttu-id="3948e-110">Especifica a função que a infraestrutura de gráfico de pares chama para proteger registros.</span><span class="sxs-lookup"><span data-stu-id="3948e-110">Specifies the function that the Peer Graphing Infrastructure calls to secure records.</span></span>                                                                                                                                        |
| [<span data-ttu-id="3948e-111">*PFNPEER \_ validar \_ registro*</span><span class="sxs-lookup"><span data-stu-id="3948e-111">*PFNPEER\_VALIDATE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | <span data-ttu-id="3948e-112">Especifica a função que a infraestrutura de grafo de pares chama para validar registros.</span><span class="sxs-lookup"><span data-stu-id="3948e-112">Specifies the function that the Peer Graphing Infrastructure calls to validate records.</span></span>                                                                                                                                      |



 

 

 



