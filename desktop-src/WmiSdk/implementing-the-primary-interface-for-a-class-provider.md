---
description: 'Há duas maneiras de implementar um provedor de classe: implemente a interface como um provedor de Push ou como um provedor de pull.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296994"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="5a7cd-103">Implementando a interface primária para um provedor de classe</span><span class="sxs-lookup"><span data-stu-id="5a7cd-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="5a7cd-104">Há duas maneiras de implementar um provedor de classe: implemente a interface como um provedor de Push ou como um provedor de pull.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="5a7cd-105">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="5a7cd-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="5a7cd-106">Implementando a interface primária para um provedor de classe push</span><span class="sxs-lookup"><span data-stu-id="5a7cd-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="5a7cd-107">Implementando a interface primária para um provedor de classe pull</span><span class="sxs-lookup"><span data-stu-id="5a7cd-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="5a7cd-108">Implementando a interface primária para um provedor de classe push</span><span class="sxs-lookup"><span data-stu-id="5a7cd-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="5a7cd-109">Enquanto todos os provedores implementam [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para inicialização e pelo menos uma outra interface como sua interface primária, um provedor de push implementa apenas **IWbemProviderInit**.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="5a7cd-110">Certifique-se de que sua implementação execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="5a7cd-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="5a7cd-111">Recupera os dados de classe apropriados.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="5a7cd-112">Coloca os dados no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="5a7cd-113">Exclui dados obsoletos.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-113">Deletes obsolete data.</span></span>

<span data-ttu-id="5a7cd-114">Depois de concluir o processo de inicialização, o WMI manipula todas as solicitações de aplicativo para classes que pertencem ao provedor de push sem nenhuma interação adicional do provedor.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="5a7cd-115">Depois disso, o provedor de push atua efetivamente como um cliente do WMI em vez de um provedor.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="5a7cd-116">Para obter mais informações sobre como implementar [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), consulte [inicializando um provedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5a7cd-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="5a7cd-117">Ao chamar o WMI para criar, atualizar ou remover dados em um provedor de push, defina o parâmetro *lFlags* para incluir o sinalizador de **atualização do \_ proprietário do sinalizador \_ \_ WBEM** em todas as chamadas para métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="5a7cd-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="5a7cd-118">Implementando a interface primária para um provedor de classe pull</span><span class="sxs-lookup"><span data-stu-id="5a7cd-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="5a7cd-119">Um provedor de pull de classe deve implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="5a7cd-120">A interface **IWbemServices** dá suporte à recuperação de dados, à atualização de dados, à remoção de dados, à enumeração e ao processamento de consultas.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="5a7cd-121">No entanto, como **IWbemServices** também é usado por aplicativos e provedores para solicitar serviços de WMI, **IWbemServices** contém muitos métodos que são irrelevantes para um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="5a7cd-122">Sua implementação deve dar suporte à recuperação e à enumeração de classe, por meio dos métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="5a7cd-123">A tabela a seguir lista os métodos de **IWbemServices** assíncronos adicionais que você pode implementar para um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="5a7cd-124">Método</span><span class="sxs-lookup"><span data-stu-id="5a7cd-124">Method</span></span>                                                     | <span data-ttu-id="5a7cd-125">Recurso</span><span class="sxs-lookup"><span data-stu-id="5a7cd-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="5a7cd-126">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="5a7cd-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="5a7cd-127">Modification</span><span class="sxs-lookup"><span data-stu-id="5a7cd-127">Modification</span></span> |
| [<span data-ttu-id="5a7cd-128">**DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="5a7cd-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="5a7cd-129">Exclusão</span><span class="sxs-lookup"><span data-stu-id="5a7cd-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="5a7cd-130">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="5a7cd-131">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5a7cd-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="5a7cd-132">Seu provedor de classe deve fornecer uma implementação de stub que retorne o **\_ provedor WBEM E \_ \_ não \_ compatível** com todos os outros métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que não dão suporte ao seu conjunto de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="5a7cd-133">Especificamente, o WMI não dá suporte ao processamento de consultas para provedores de classe.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="5a7cd-134">Como tal, um provedor de classe deve retornar o **\_ provedor WBEM E \_ \_ não \_ capaz** de sua implementação de [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), definir sua propriedade de registro **QuerySupportLevels** como **NULL** ou ambos.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="5a7cd-135">As interfaces que um provedor de classe implementa são muito semelhantes às interfaces para um provedor de instância e um provedor de método.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="5a7cd-136">Na verdade, um único provedor pode atuar como todos os três tipos de provedor implementando todos os métodos e registrando-se corretamente.</span><span class="sxs-lookup"><span data-stu-id="5a7cd-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



