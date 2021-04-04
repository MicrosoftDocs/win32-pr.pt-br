---
description: Uma das primeiras tarefas que você deve codificar para um provedor é o processo de inicialização, que abrange todas as tarefas que o seu provedor deve executar, permitindo que ele envie e receba informações do WMI, controle um objeto gerenciado e execute outras tarefas.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inicializando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837255"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="d9ae7-103">Inicializando um provedor</span><span class="sxs-lookup"><span data-stu-id="d9ae7-103">Initializing a Provider</span></span>

<span data-ttu-id="d9ae7-104">Uma das primeiras tarefas que você deve codificar para um provedor é o processo de inicialização, que abrange todas as tarefas que o seu provedor deve executar, permitindo que ele envie e receba informações do WMI, controle um objeto gerenciado e execute outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="d9ae7-105">Cada tipo de provedor tem um conjunto diferente de tarefas que ele deve executar e tem um conjunto complementar de interfaces exclusivas.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="d9ae7-106">No entanto, todos os provedores são inicializados por meio da interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e informam o WMI sobre o status de inicialização por meio da interface [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .</span><span class="sxs-lookup"><span data-stu-id="d9ae7-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="d9ae7-107">O procedimento a seguir descreve como inicializar um provedor.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="d9ae7-108">**Para inicializar um provedor**</span><span class="sxs-lookup"><span data-stu-id="d9ae7-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="d9ae7-109">Implemente [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="d9ae7-110">Quando o WMI determina que um cliente requer os serviços de um provedor, o WMI carrega o provedor chamando o método [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="d9ae7-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="d9ae7-111">Implemente qualquer interface exclusiva para seu tipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="d9ae7-112">Informe ao WMI que seu provedor foi concluído com a inicialização chamando [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="d9ae7-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="d9ae7-113">Todas as implementações de [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) devem chamar [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para relatar o status de inicialização para o WMI.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="d9ae7-114">O método **SetStatus** permite que o WMI determine se um provedor está pronto para receber solicitações e o tipo de solicitações que o provedor está pronto para receber.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="d9ae7-115">O procedimento a seguir descreve como relatar uma inicialização bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="d9ae7-116">**Para relatar uma inicialização bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="d9ae7-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="d9ae7-117">Defina o parâmetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para **WBEM \_ S \_ INITIALIZED**.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="d9ae7-118">Ao retornar o **WBEM \_ S \_ inicializado**, um provedor indica uma prontidão para lidar com solicitações de aplicativos, WMI e outros provedores.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="d9ae7-119">Depois de receber \_ o WBEM S \_ inicializado, o WMI faz uma chamada para o método [**IWbemProviderInit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) no provedor.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="d9ae7-120">Essa consulta recupera um ponteiro para a interface primária do provedor.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="d9ae7-121">O procedimento a seguir descreve como relatar um erro durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="d9ae7-122">**Para relatar um erro durante a inicialização**</span><span class="sxs-lookup"><span data-stu-id="d9ae7-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="d9ae7-123">Defina o parâmetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) como **WBEM \_ E \_ falhou**.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="d9ae7-124">Os provedores de exibições WMI que retornam **WBEM \_ E \_ falharam** como não funcionais.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="d9ae7-125">O WMI libera o ponteiro [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) após o WMI ter obtido um ponteiro para a interface primária do provedor ou após a inicialização falhar.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9ae7-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9ae7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9ae7-127">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="d9ae7-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="d9ae7-128">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="d9ae7-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="d9ae7-129">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="d9ae7-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



