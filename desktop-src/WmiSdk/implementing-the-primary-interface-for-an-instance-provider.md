---
title: Implementando uma interface primária do provedor de instância
description: Um provedor de instância usa os métodos assíncronos de IWbemServices como a interface primária para o WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814170"
---
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="5070d-103">Implementando uma interface primária do provedor de instância</span><span class="sxs-lookup"><span data-stu-id="5070d-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="5070d-104">Um provedor de instância usa os métodos assíncronos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária para o WMI.</span><span class="sxs-lookup"><span data-stu-id="5070d-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="5070d-105">Ao implementar apenas os métodos que atendem às necessidades do seu provedor de instância, você pode reduzir a quantidade de recursos gastos com codificação.</span><span class="sxs-lookup"><span data-stu-id="5070d-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="5070d-106">No entanto, ao implementar métodos reservados para outros tipos de provedores, você pode reduzir o número de provedores que escreve.</span><span class="sxs-lookup"><span data-stu-id="5070d-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="5070d-107">Como ele também é usado por aplicativos e provedores para solicitar serviços de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contém muitos métodos que são irrelevantes para um provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="5070d-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="5070d-108">A tabela a seguir lista os métodos de **IWbemServices** que você pode implementar para um provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="5070d-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="5070d-109">Método</span><span class="sxs-lookup"><span data-stu-id="5070d-109">Method</span></span>                                                                   | <span data-ttu-id="5070d-110">Recurso</span><span class="sxs-lookup"><span data-stu-id="5070d-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="5070d-111">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="5070d-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="5070d-112">Recuperação</span><span class="sxs-lookup"><span data-stu-id="5070d-112">Retrieval</span></span>        |
| [<span data-ttu-id="5070d-113">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="5070d-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="5070d-114">Modification</span><span class="sxs-lookup"><span data-stu-id="5070d-114">Modification</span></span>     |
| [<span data-ttu-id="5070d-115">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="5070d-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="5070d-116">Exclusão</span><span class="sxs-lookup"><span data-stu-id="5070d-116">Deletion</span></span>         |
| [<span data-ttu-id="5070d-117">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="5070d-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="5070d-118">Enumeração</span><span class="sxs-lookup"><span data-stu-id="5070d-118">Enumeration</span></span>      |
| [<span data-ttu-id="5070d-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5070d-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="5070d-120">Processamento de consulta</span><span class="sxs-lookup"><span data-stu-id="5070d-120">Query processing</span></span> |



 

<span data-ttu-id="5070d-121">Para métodos que você não usa, seu provedor pode fornecer uma implementação de stub que retorne o **\_ provedor WBEM E \_ \_ não \_ compatível**.</span><span class="sxs-lookup"><span data-stu-id="5070d-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="5070d-122">Isso inclui todos os métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) não listados na tabela acima.</span><span class="sxs-lookup"><span data-stu-id="5070d-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="5070d-123">Um único provedor pode agir simultaneamente como uma classe, instância e provedor de métodos por registro e implementação adequados de todos os métodos relevantes.</span><span class="sxs-lookup"><span data-stu-id="5070d-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="5070d-124">Para obter mais informações, consulte [escrevendo um provedor de classe](writing-a-class-provider.md) e [escrevendo um provedor de método](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5070d-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



