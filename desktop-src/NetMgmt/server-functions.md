---
title: Funções de servidor (gerenciamento de rede)
description: As funções do servidor de gerenciamento de rede executam tarefas administrativas em um servidor local ou remoto. As funções de servidor são listadas a seguir.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008768"
---
# <a name="server-functions-network-management"></a><span data-ttu-id="840d1-104">Funções de servidor (gerenciamento de rede)</span><span class="sxs-lookup"><span data-stu-id="840d1-104">Server Functions (Network Management)</span></span>

<span data-ttu-id="840d1-105">As funções do servidor de gerenciamento de rede executam tarefas administrativas em um servidor local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="840d1-105">The network management server functions perform administrative tasks on a local or remote server.</span></span> <span data-ttu-id="840d1-106">As funções de servidor são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="840d1-106">The server functions are listed following.</span></span>



| <span data-ttu-id="840d1-107">Função</span><span class="sxs-lookup"><span data-stu-id="840d1-107">Function</span></span>                                       | <span data-ttu-id="840d1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="840d1-108">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="840d1-109">**NetServerDiskEnum**</span><span class="sxs-lookup"><span data-stu-id="840d1-109">**NetServerDiskEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | <span data-ttu-id="840d1-110">Retorna uma lista de unidades de disco locais em um servidor.</span><span class="sxs-lookup"><span data-stu-id="840d1-110">Returns a list of local disk drives on a server.</span></span>                                   |
| [<span data-ttu-id="840d1-111">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="840d1-111">**NetServerEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | <span data-ttu-id="840d1-112">Lista todos os servidores visíveis de um tipo específico (ou tipos) no domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="840d1-112">Lists all visible servers of a particular type (or types) in the specified domain.</span></span> |
| [<span data-ttu-id="840d1-113">**NetServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="840d1-113">**NetServerGetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | <span data-ttu-id="840d1-114">Retorna informações de configuração sobre um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="840d1-114">Returns configuration information about a specified server.</span></span>                        |
| [<span data-ttu-id="840d1-115">**NetServerSetInfo**</span><span class="sxs-lookup"><span data-stu-id="840d1-115">**NetServerSetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | <span data-ttu-id="840d1-116">Define os parâmetros operacionais de um servidor.</span><span class="sxs-lookup"><span data-stu-id="840d1-116">Sets the operating parameters for a server.</span></span>                                        |



 

<span data-ttu-id="840d1-117">Somente um usuário ou aplicativo com associação de grupo de administrador em um servidor local ou remoto pode executar tarefas administrativas nesse servidor para controlar a operação, o acesso do usuário e o compartilhamento de recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="840d1-117">Only a user or application with admin group membership on a local or remote server can perform administrative tasks on that server to control the server's operation, user access, and resource sharing.</span></span> <span data-ttu-id="840d1-118">Os parâmetros de nível baixo que afetam a operação de um servidor podem ser examinados e modificados chamando as funções [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) e [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) .</span><span class="sxs-lookup"><span data-stu-id="840d1-118">The low-level parameters that affect a server's operation can be examined and modified by calling the [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) and [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) functions.</span></span> <span data-ttu-id="840d1-119">Esses parâmetros são definidos no arquivo de LANMAN.INI do servidor.</span><span class="sxs-lookup"><span data-stu-id="840d1-119">These parameters are defined in the server's LANMAN.INI file.</span></span>

<span data-ttu-id="840d1-120">A maioria das funções do servidor de gerenciamento de rede é executada somente em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="840d1-120">Most network management server functions execute only on a remote server.</span></span> <span data-ttu-id="840d1-121">A função [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) é executada em uma estação de trabalho local ou em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="840d1-121">The [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) function executes on either a local workstation or a remote server.</span></span> <span data-ttu-id="840d1-122">Se você tentar executar outras funções de servidor em uma estação de trabalho local, as funções retornarão o erro NERR \_ RemoteOnly.</span><span class="sxs-lookup"><span data-stu-id="840d1-122">If you attempt to execute other server functions on a local workstation, the functions return the error NERR\_RemoteOnly.</span></span>

<span data-ttu-id="840d1-123">As informações específicas do servidor estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="840d1-123">Server-specific information is available at the following levels:</span></span>

-   [<span data-ttu-id="840d1-124">**Informações do servidor \_ \_ 100**</span><span class="sxs-lookup"><span data-stu-id="840d1-124">**SERVER\_INFO\_100**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [<span data-ttu-id="840d1-125">**Informações do servidor \_ \_ 101**</span><span class="sxs-lookup"><span data-stu-id="840d1-125">**SERVER\_INFO\_101**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [<span data-ttu-id="840d1-126">**Informações do servidor \_ \_ 102**</span><span class="sxs-lookup"><span data-stu-id="840d1-126">**SERVER\_INFO\_102**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [<span data-ttu-id="840d1-127">**Informações do servidor \_ \_ 402**</span><span class="sxs-lookup"><span data-stu-id="840d1-127">**SERVER\_INFO\_402**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [<span data-ttu-id="840d1-128">**Informações do servidor \_ \_ 403**</span><span class="sxs-lookup"><span data-stu-id="840d1-128">**SERVER\_INFO\_403**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [<span data-ttu-id="840d1-129">**Informações do servidor \_ \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="840d1-129">**SERVER\_INFO\_1501**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [<span data-ttu-id="840d1-130">**Informações do servidor \_ \_ 1502**</span><span class="sxs-lookup"><span data-stu-id="840d1-130">**SERVER\_INFO\_1502**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [<span data-ttu-id="840d1-131">**Informações do servidor \_ \_ 1503**</span><span class="sxs-lookup"><span data-stu-id="840d1-131">**SERVER\_INFO\_1503**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [<span data-ttu-id="840d1-132">**Informações do servidor \_ \_ 1506**</span><span class="sxs-lookup"><span data-stu-id="840d1-132">**SERVER\_INFO\_1506**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [<span data-ttu-id="840d1-133">**Informações do servidor \_ \_ 1509**</span><span class="sxs-lookup"><span data-stu-id="840d1-133">**SERVER\_INFO\_1509**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [<span data-ttu-id="840d1-134">**Informações do servidor \_ \_ 1510**</span><span class="sxs-lookup"><span data-stu-id="840d1-134">**SERVER\_INFO\_1510**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [<span data-ttu-id="840d1-135">**Informações do servidor \_ \_ 1511**</span><span class="sxs-lookup"><span data-stu-id="840d1-135">**SERVER\_INFO\_1511**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [<span data-ttu-id="840d1-136">**Informações do servidor \_ \_ 1512**</span><span class="sxs-lookup"><span data-stu-id="840d1-136">**SERVER\_INFO\_1512**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [<span data-ttu-id="840d1-137">**Informações do servidor \_ \_ 1513**</span><span class="sxs-lookup"><span data-stu-id="840d1-137">**SERVER\_INFO\_1513**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [<span data-ttu-id="840d1-138">**Informações do servidor \_ \_ 1515**</span><span class="sxs-lookup"><span data-stu-id="840d1-138">**SERVER\_INFO\_1515**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [<span data-ttu-id="840d1-139">**Informações do servidor \_ \_ 1516**</span><span class="sxs-lookup"><span data-stu-id="840d1-139">**SERVER\_INFO\_1516**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [<span data-ttu-id="840d1-140">**Informações do servidor \_ \_ 1518**</span><span class="sxs-lookup"><span data-stu-id="840d1-140">**SERVER\_INFO\_1518**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [<span data-ttu-id="840d1-141">**Informações do servidor \_ \_ 1523**</span><span class="sxs-lookup"><span data-stu-id="840d1-141">**SERVER\_INFO\_1523**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [<span data-ttu-id="840d1-142">**Informações do servidor \_ \_ 1528**</span><span class="sxs-lookup"><span data-stu-id="840d1-142">**SERVER\_INFO\_1528**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [<span data-ttu-id="840d1-143">**Informações do servidor \_ \_ 1529**</span><span class="sxs-lookup"><span data-stu-id="840d1-143">**SERVER\_INFO\_1529**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [<span data-ttu-id="840d1-144">**Informações do servidor \_ \_ 1530**</span><span class="sxs-lookup"><span data-stu-id="840d1-144">**SERVER\_INFO\_1530**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [<span data-ttu-id="840d1-145">**Informações do servidor \_ \_ 1533**</span><span class="sxs-lookup"><span data-stu-id="840d1-145">**SERVER\_INFO\_1533**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [<span data-ttu-id="840d1-146">**Informações do servidor \_ \_ 1536**</span><span class="sxs-lookup"><span data-stu-id="840d1-146">**SERVER\_INFO\_1536**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [<span data-ttu-id="840d1-147">**Informações do servidor \_ \_ 1538**</span><span class="sxs-lookup"><span data-stu-id="840d1-147">**SERVER\_INFO\_1538**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [<span data-ttu-id="840d1-148">**Informações do servidor \_ \_ 1539**</span><span class="sxs-lookup"><span data-stu-id="840d1-148">**SERVER\_INFO\_1539**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [<span data-ttu-id="840d1-149">**Informações do servidor \_ \_ 1540**</span><span class="sxs-lookup"><span data-stu-id="840d1-149">**SERVER\_INFO\_1540**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [<span data-ttu-id="840d1-150">**Informações do servidor \_ \_ 1541**</span><span class="sxs-lookup"><span data-stu-id="840d1-150">**SERVER\_INFO\_1541**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [<span data-ttu-id="840d1-151">**Informações do servidor \_ \_ 1542**</span><span class="sxs-lookup"><span data-stu-id="840d1-151">**SERVER\_INFO\_1542**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [<span data-ttu-id="840d1-152">**Informações do servidor \_ \_ 1544**</span><span class="sxs-lookup"><span data-stu-id="840d1-152">**SERVER\_INFO\_1544**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [<span data-ttu-id="840d1-153">**Informações do servidor \_ \_ 1550**</span><span class="sxs-lookup"><span data-stu-id="840d1-153">**SERVER\_INFO\_1550**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [<span data-ttu-id="840d1-154">**Informações do servidor \_ \_ 1552**</span><span class="sxs-lookup"><span data-stu-id="840d1-154">**SERVER\_INFO\_1552**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

<span data-ttu-id="840d1-155">Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções do servidor de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="840d1-155">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions.</span></span> <span data-ttu-id="840d1-156">Para obter mais informações, consulte [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="840d1-156">For more information, see [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span></span>

<span data-ttu-id="840d1-157">Para obter mais informações, consulte as [funções de transporte de servidor e estação de trabalho](server-and-workstation-transport-functions.md).</span><span class="sxs-lookup"><span data-stu-id="840d1-157">For more information, see the [Server and Workstation Transport Functions](server-and-workstation-transport-functions.md).</span></span>

 

 
