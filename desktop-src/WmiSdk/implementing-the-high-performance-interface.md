---
description: Como o WMI carrega um provedor de alto desempenho em processo para o WMI ou um aplicativo cliente, você deve projetar seu provedor de alto desempenho como um servidor em processo.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementando a interface High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813519"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="c2bfe-103">Implementando a interface High-Performance</span><span class="sxs-lookup"><span data-stu-id="c2bfe-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="c2bfe-104">Como o WMI carrega um provedor de alto desempenho em processo para o WMI ou um aplicativo cliente, você deve projetar seu provedor de alto desempenho como um servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="c2bfe-105">Além disso, você deve implementar os métodos de provedor de alto desempenho nas interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .</span><span class="sxs-lookup"><span data-stu-id="c2bfe-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="c2bfe-106">Você deve implementar um provedor de alto desempenho como um servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="c2bfe-107">Um recurso que você deve estar atento ao implementar a segurança de um servidor em processo é como o provedor identifica seu próprio local.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="c2bfe-108">Quando carregado em processo para WMI, o WMI instancia o provedor usando um CLSID.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="c2bfe-109">Quando carregado em processo para um aplicativo cliente, o aplicativo cliente cria uma instância do provedor com a propriedade **ClientLoadableCLSID** .</span><span class="sxs-lookup"><span data-stu-id="c2bfe-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="c2bfe-110">Ao conceder valores diferentes a um CLSID e a um **ClientLoadableCLSID**, você permite que o provedor determine se ele está carregado em processo para WMI ou para um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="c2bfe-111">Se estiver localizado em um processo WMI, o provedor deverá fazer qualquer representação de cliente necessária usando **ClientLoadableCLSID**.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="c2bfe-112">Se estiver localizado em um processo de cliente, o provedor herdará o token de acesso do thread em que ele é chamado.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="c2bfe-113">Para obter mais informações sobre como implementar um servidor em processo, consulte a [seção com](https://msdn.microsoft.com/library/aa139695.aspx) do MSDN.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="c2bfe-114">Como um servidor em processo, um provedor de alto desempenho usa um objeto de atualização para manter os dados atuais para o cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="c2bfe-115">A tabela a seguir lista os métodos que você deve implementar para um provedor de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="c2bfe-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="c2bfe-116">Método</span><span class="sxs-lookup"><span data-stu-id="c2bfe-116">Method</span></span>                                                                                              | <span data-ttu-id="c2bfe-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="c2bfe-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="c2bfe-118">**IWbemHiPerfProvider::QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="c2bfe-119">Consultas</span><span class="sxs-lookup"><span data-stu-id="c2bfe-119">Queries</span></span>                                           |
| [<span data-ttu-id="c2bfe-120">**IWbemHiPerfProvider:: GetObjects**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="c2bfe-121">Recuperação de objeto</span><span class="sxs-lookup"><span data-stu-id="c2bfe-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="c2bfe-122">**IWbemHiPerfProvider:: createrefresher**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="c2bfe-123">Cria um atualizador</span><span class="sxs-lookup"><span data-stu-id="c2bfe-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="c2bfe-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="c2bfe-125">Cria um objeto de instância atualizável</span><span class="sxs-lookup"><span data-stu-id="c2bfe-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="c2bfe-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="c2bfe-127">Cria um enumerador atualizável</span><span class="sxs-lookup"><span data-stu-id="c2bfe-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="c2bfe-128">**IWbemHiPerfProvider::StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="c2bfe-129">Para a atualização de um enumerador ou objeto de instância</span><span class="sxs-lookup"><span data-stu-id="c2bfe-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="c2bfe-130">**IWbemRefresher:: atualizar**</span><span class="sxs-lookup"><span data-stu-id="c2bfe-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="c2bfe-131">Cria um atualizador</span><span class="sxs-lookup"><span data-stu-id="c2bfe-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="c2bfe-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2bfe-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2bfe-133">Criando um provedor de instância em um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="c2bfe-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



