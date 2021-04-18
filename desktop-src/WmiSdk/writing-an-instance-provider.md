---
description: Um provedor de instância fornece instâncias de uma ou mais classes fornecidas.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Gravando um provedor de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764508"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="b65b0-103">Gravando um provedor de instância</span><span class="sxs-lookup"><span data-stu-id="b65b0-103">Writing an Instance Provider</span></span>

<span data-ttu-id="b65b0-104">Um provedor de instância fornece instâncias de uma ou mais classes fornecidas.</span><span class="sxs-lookup"><span data-stu-id="b65b0-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="b65b0-105">Por exemplo, um provedor de instância pode fornecer informações sobre uma CPU ou outro tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="b65b0-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="b65b0-106">Como os objetos gerenciados por um provedor de instância tendem a ser alterados regularmente, todos os provedores de instância são considerados provedores de pull; ou seja, um provedor que recupera dinamicamente informações sobre um objeto gerenciado sempre que o WMI faz uma solicitação para as informações.</span><span class="sxs-lookup"><span data-stu-id="b65b0-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="b65b0-107">O nome vem da ideia de que o WMI "recebe" as informações do provedor em nome de uma solicitação do cliente.</span><span class="sxs-lookup"><span data-stu-id="b65b0-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="b65b0-108">Usando a tecnologia pull, um provedor de instância pode dar suporte a recuperação, enumeração, modificação, exclusão e processamento de consulta de uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="b65b0-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="b65b0-109">Provedores de alto desempenho podem aumentar a eficiência de um provedor de instância ou acessar programaticamente os dados que aparecem no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="b65b0-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="b65b0-110">Para obter mais informações, consulte [criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="b65b0-111">O procedimento a seguir descreve como gravar um provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="b65b0-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="b65b0-112">**Para gravar um provedor de instância**</span><span class="sxs-lookup"><span data-stu-id="b65b0-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="b65b0-113">[Registre seu provedor com o WMI](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="b65b0-114">Os provedores de instância se registram com o WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="b65b0-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="b65b0-115">[Inicialize seu provedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="b65b0-116">O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor.</span><span class="sxs-lookup"><span data-stu-id="b65b0-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="b65b0-117">Essa é uma tarefa comum a todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="b65b0-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="b65b0-118">Os provedores de instância são altamente incentivados a usar o modelo de vários threads "both".</span><span class="sxs-lookup"><span data-stu-id="b65b0-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="b65b0-119">[Implemente a interface IWbemServices para seu provedor](implementing-the-primary-interface-for-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="b65b0-120">A interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) é a interface principal para um provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="b65b0-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="b65b0-121">Adicione qualquer código adicional necessário para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="b65b0-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="b65b0-122">Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="b65b0-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="b65b0-123">Para obter mais informações, consulte [fazendo chamadas para o WMI](making-calls-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="b65b0-124">Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="b65b0-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="b65b0-125">Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="b65b0-126">Se necessário, [implemente a interface de alto desempenho](improving-the-efficiency-of-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="b65b0-127">A interface de alto desempenho aumenta a velocidade na qual o provedor pode reagir às solicitações do WMI.</span><span class="sxs-lookup"><span data-stu-id="b65b0-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="b65b0-128">Se necessário, [implemente o suporte para atualizações de instância parcial](supporting-partial-instance-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="b65b0-129">Como o nome indica, uma atualização de instância parcial é uma técnica usada para atualizar apenas parte de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b65b0-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="b65b0-130">Para obter mais informações sobre como chamar uma instância parcial de um cliente, consulte [atualizando parte de uma instância](updating-part-of-an-instance.md) e [recuperando parte de uma instância do WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="b65b0-131">Substitua o provedor preexistente pelo seu novo código.</span><span class="sxs-lookup"><span data-stu-id="b65b0-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="b65b0-132">Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar.</span><span class="sxs-lookup"><span data-stu-id="b65b0-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="b65b0-133">Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65b0-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



