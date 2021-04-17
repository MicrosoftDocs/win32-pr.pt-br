---
description: Um componente COM configurado geralmente é ativado em seu próprio contexto; ou seja, o COM+ faz referência às informações do catálogo de componentes para fornecer quaisquer serviços configurados.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Impondo ativação no contexto padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501128"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="72957-103">Impondo ativação no contexto padrão</span><span class="sxs-lookup"><span data-stu-id="72957-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="72957-104">Um componente COM configurado geralmente é ativado em seu próprio contexto; ou seja, COM+ faz referência às informações de catálogo do componente para fornecer quaisquer serviços configurados.</span><span class="sxs-lookup"><span data-stu-id="72957-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="72957-105">No entanto, você pode optar por ativar um componente configurado no contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="72957-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="72957-106">Um componente COM base — um componente registrado que não tem informações de catálogo COM+ — geralmente é ativado no contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="72957-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="72957-107">Ativar um componente COM no contexto padrão fornece três principais benefícios de desempenho, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="72957-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="72957-108">Você salva os recursos do sistema limitando o número de contextos que são criados.</span><span class="sxs-lookup"><span data-stu-id="72957-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="72957-109">Você aumenta o desempenho limitando o número de chamadas de contexto cruzado.</span><span class="sxs-lookup"><span data-stu-id="72957-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="72957-110">Como as chamadas entre contextos exigem marshaling, é muito mais rápida para um objeto COM ativado no contexto padrão para fazer chamadas para outros objetos no contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="72957-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="72957-111">O desempenho nesse caso (de chamadas dentro do mesmo contexto) é semelhante ao de chamar uma sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="72957-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="72957-112">Você pode importar aplicativos COM mais antigos para o COM+ e executá-los sem problemas.</span><span class="sxs-lookup"><span data-stu-id="72957-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="72957-113">Por exemplo, você pode ter vários aplicativos COM mais antigos implementados sob a suposição de que era possível passar referências de objeto em um apartamento sem realizar marshaling das referências.</span><span class="sxs-lookup"><span data-stu-id="72957-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="72957-114">Esses aplicativos COM não funcionam quando importados para o COM+ porque as referências de objeto são passadas entre limites de contexto.</span><span class="sxs-lookup"><span data-stu-id="72957-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="72957-115">No entanto, você pode fazer COM que esse tipo de aplicativo COM seja executado quando importado se você usar a ferramenta administrativa serviços de componentes para marcar todas as classes no aplicativo como **deve ser ativado no contexto padrão**.</span><span class="sxs-lookup"><span data-stu-id="72957-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="72957-116">A principal desvantagem de ativar um componente configurado no contexto padrão é que o COM+ não fornece nenhum dos serviços configurados do componente.</span><span class="sxs-lookup"><span data-stu-id="72957-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="72957-117">Há uma compensação entre o desempenho aprimorado e a capacidade de usar os serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="72957-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="72957-118">Por exemplo, suponha que um componente COM não exija serviços COM+ (como [Transações](com--transactions.md), [ativação Just-in-time](com--just-in-time-activation.md), [eventos](com--events.md), [componentes enfileirados](com--queued-components.md), [sincronização](com--synchronization.md)ou [pool de objetos](com--object-pooling.md)) e que o componente faça várias chamadas para outros componentes com que possam ser ativados no contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="72957-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="72957-119">Nesse caso, seria uma boa ideia ativar o componente de chamada no contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="72957-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="72957-120">Se o componente COM exigir serviços COM+, ele não poderá ser marcado como **deve ser ativado no contexto padrão**.</span><span class="sxs-lookup"><span data-stu-id="72957-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="72957-121">Além disso, não haverá nenhum benefício de desempenho real se um objeto COM ativado no contexto padrão fizer várias chamadas para objetos em outros contextos.</span><span class="sxs-lookup"><span data-stu-id="72957-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="72957-122">(Para obter mais detalhes, consulte [contextos](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="72957-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="72957-123">**Para impor a ativação no contexto padrão**</span><span class="sxs-lookup"><span data-stu-id="72957-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="72957-124">No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente (localizado na pasta **componentes** de qualquer aplicativo com+ selecionado) que você deseja ativar no contexto padrão e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="72957-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="72957-125">Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="72957-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="72957-126">Selecione a caixa de seleção **deve ser ativada no contexto padrão**.</span><span class="sxs-lookup"><span data-stu-id="72957-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="72957-127">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="72957-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="72957-128">Quando você executa um componente configurado no contexto padrão, o COM+ não ativa nenhum dos serviços configurados para esse componente.</span><span class="sxs-lookup"><span data-stu-id="72957-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="72957-129">Esses serviços estão disponíveis novamente quando você desmarca a caixa de seleção **deve ser ativada no contexto padrão** e, posteriormente, executa o componente configurado em seu próprio contexto.</span><span class="sxs-lookup"><span data-stu-id="72957-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="72957-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72957-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72957-131">Conceitos de ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="72957-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="72957-132">Impondo a ativação no contexto do chamador</span><span class="sxs-lookup"><span data-stu-id="72957-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



