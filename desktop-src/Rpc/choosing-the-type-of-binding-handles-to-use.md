---
title: Escolhendo o tipo de identificadores de associação a ser usado
description: Escolhendo o tipo de identificadores de associação a ser usado
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005232"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="2e9af-103">Escolhendo o tipo de identificadores de associação a ser usado</span><span class="sxs-lookup"><span data-stu-id="2e9af-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="2e9af-104">**Prática recomendada:** Se você souber qual servidor será usado pelo aplicativo, use identificadores explícitos.</span><span class="sxs-lookup"><span data-stu-id="2e9af-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="2e9af-105">Se você não fizer isso, use identificadores explícitos constructos todas as vezes ou use identificadores genéricos com rotinas de **\_ associar** e **\_ desassociar** .</span><span class="sxs-lookup"><span data-stu-id="2e9af-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="2e9af-106">Não use identificadores implícitos ou identificadores automáticos.</span><span class="sxs-lookup"><span data-stu-id="2e9af-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="2e9af-107">Os identificadores implícitos não são thread-safe e, embora a segurança de thread possa parecer desnecessária, ela pode ser necessária mais tarde.</span><span class="sxs-lookup"><span data-stu-id="2e9af-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="2e9af-108">Os identificadores automáticos têm grande sobrecarga e exigem muita configuração para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="2e9af-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="2e9af-109">Seus recursos de pesquisa foram substituídos por serviços Active Directorys.</span><span class="sxs-lookup"><span data-stu-id="2e9af-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="2e9af-110">Os identificadores explícitos são altamente eficientes e muitos recursos atraentes estão disponíveis apenas para identificadores explícitos.</span><span class="sxs-lookup"><span data-stu-id="2e9af-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="2e9af-111">Por exemplo, se várias chamadas RPC forem para o mesmo servidor, você poderá construir o identificador de associação uma vez e fazer todas as chamadas com ele.</span><span class="sxs-lookup"><span data-stu-id="2e9af-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="2e9af-112">Essa abordagem é muito mais eficiente do que qualquer outro método.</span><span class="sxs-lookup"><span data-stu-id="2e9af-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="2e9af-113">Se o servidor ao qual a chamada será desconhecido, construa um identificador de ligação explícito para cada chamada ou use identificadores de associação genéricos.</span><span class="sxs-lookup"><span data-stu-id="2e9af-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="2e9af-114">No Microsoft™ Windows XP, o tempo de execução de RPC é bastante eficiente na reutilização e no cache de chamadas, portanto, se a chamada *n*+ 1º terminar no mesmo servidor que a chamada *n* th, o RPC reutilizará os recursos alocados para a chamada *n*, burlando a necessidade de armazenar em cache identificadores de associação para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2e9af-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




