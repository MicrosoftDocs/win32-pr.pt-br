---
title: Como um serviço compõe seus SPNs
description: Um serviço pode usar duas funções para compor seus SPNs DsGetSpn é uma função de finalidade geral para compor SPNs e DsServerRegisterSpn é uma função especializada para compor e registrar SPNs simples para um serviço baseado em host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nome da entidade de serviço AD, como um serviço compõe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822274"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="686a5-104">Como um serviço compõe seus SPNs</span><span class="sxs-lookup"><span data-stu-id="686a5-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="686a5-105">Um serviço pode usar duas funções para compor seus SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) é uma função de finalidade geral para compor SPNs e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) é uma função especializada para compor e registrar SPNs simples para um serviço baseado em host.</span><span class="sxs-lookup"><span data-stu-id="686a5-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="686a5-106">Um instalador de serviço normalmente usa a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para compor SPNs, que, em seguida, registra na conta de logon do serviço usando a função [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) .</span><span class="sxs-lookup"><span data-stu-id="686a5-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="686a5-107">O **DsGetSpn** pode executar as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="686a5-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="686a5-108">Crie um SPN simples com o <service class> / <host> formato "" para um serviço baseado em host.</span><span class="sxs-lookup"><span data-stu-id="686a5-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="686a5-109">Crie um SPN complexo que inclui o &lt; componente "nome do serviço &gt; " usado por serviços replicáveis ou pelo &lt; componente "porta &gt; " que distingue várias instâncias de um serviço em um único host.</span><span class="sxs-lookup"><span data-stu-id="686a5-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="686a5-110">Crie um único SPN com o &lt; componente "host &gt; " definido como o nome de um host especificado ou o nome do computador local por padrão.</span><span class="sxs-lookup"><span data-stu-id="686a5-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="686a5-111">Crie uma matriz de SPNs para várias instâncias de serviço que serão executadas em vários hosts em toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="686a5-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="686a5-112">Cada SPN especifica o nome do host para uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="686a5-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="686a5-113">Crie uma matriz de SPNs para várias instâncias de serviço que serão executadas no mesmo host.</span><span class="sxs-lookup"><span data-stu-id="686a5-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="686a5-114">Cada SPN especifica o nome do host e um número de porta para uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="686a5-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="686a5-115">A matriz de nomes retornada por [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) deve ser liberada chamando a função [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .</span><span class="sxs-lookup"><span data-stu-id="686a5-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="686a5-116">Lembre-se de que as funções [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)e [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) não verificam se os SPNs são exclusivos.</span><span class="sxs-lookup"><span data-stu-id="686a5-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="686a5-117">Como a autenticação mútua falhará se um cliente apresentar um SPN que não é exclusivo, verifique a exclusividade antes de registrar um SPN.</span><span class="sxs-lookup"><span data-stu-id="686a5-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="686a5-118">Para fazer isso, pesquise o catálogo global (GC) em busca de atributos de **servicePrincipalName** que correspondam ao seu SPN.</span><span class="sxs-lookup"><span data-stu-id="686a5-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="686a5-119">Para obter mais informações sobre como pesquisar o GC, consulte [pesquisando o catálogo global](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="686a5-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




