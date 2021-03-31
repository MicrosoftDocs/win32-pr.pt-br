---
title: Verifique se o servidor é quem alega ser
description: É melhor usar a autenticação mútua e, assim, verificar a identidade do servidor.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635927"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="98a1f-103">Verifique se o servidor é quem alega ser</span><span class="sxs-lookup"><span data-stu-id="98a1f-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="98a1f-104">É melhor usar a autenticação mútua e, assim, verificar a identidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="98a1f-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="98a1f-105">Um exemplo de um erro comum que não faz isso é os aplicativos que têm um serviço local no qual os clientes chamam.</span><span class="sxs-lookup"><span data-stu-id="98a1f-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="98a1f-106">Em algumas configurações, um administrador pode decidir que o serviço do sistema não é realmente útil e pode optar por interrompê-lo.</span><span class="sxs-lookup"><span data-stu-id="98a1f-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="98a1f-107">Um invasor inventivo em um computador do Terminal Server pode iniciar um processo que escuta no mesmo ponto de extremidade e, quando um cliente se conecta a um ponto de extremidade, permitindo a representação no servidor sem autenticar mutuamente o servidor, o invasor pode representar o cliente e acessar os dados do cliente ou fazer chamadas de rede em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="98a1f-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="98a1f-108">A maioria dos serviços do sistema é executada em uma conta bem conhecida, como LocalSysyem, LocalService ou NetworkService, que pode ser verificada usando a autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="98a1f-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 




