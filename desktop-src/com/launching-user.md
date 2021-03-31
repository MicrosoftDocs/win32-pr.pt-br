---
title: Iniciando usuário
description: Iniciando usuário
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824004"
---
# <a name="launching-user"></a><span data-ttu-id="1466a-103">Iniciando usuário</span><span class="sxs-lookup"><span data-stu-id="1466a-103">Launching User</span></span>

<span data-ttu-id="1466a-104">Essa é a configuração padrão para a identidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1466a-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="1466a-105">Quando o usuário de inicialização é escolhido para a identidade do aplicativo, cada conta de cliente obtém uma nova instância do servidor e cada servidor obtém sua própria [estação de janela](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="1466a-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="1466a-106">Devido às instâncias de servidor separadas, iniciar usuário é a configuração de identidade de proteção de segurança de nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="1466a-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="1466a-107">No entanto, há limites finitos de consumo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1466a-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="1466a-108">Além disso, qualquer GUI que o servidor exibe não será vista pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="1466a-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="1466a-109">Se o aplicativo tiver a identidade do usuário que está iniciando, ele será executado com um token de representação.</span><span class="sxs-lookup"><span data-stu-id="1466a-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="1466a-110">Para obter mais informações sobre representação e tokens de acesso, consulte [níveis de representação](impersonation-levels.md) e [encobrimento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="1466a-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1466a-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1466a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1466a-112">Identidade do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="1466a-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="1466a-113">Usuário interativo</span><span class="sxs-lookup"><span data-stu-id="1466a-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="1466a-114">Identidade do serviço</span><span class="sxs-lookup"><span data-stu-id="1466a-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="1466a-115">Usuário especificado</span><span class="sxs-lookup"><span data-stu-id="1466a-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 