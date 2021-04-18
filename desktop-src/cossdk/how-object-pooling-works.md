---
description: Quando você configura um componente a ser agrupado, o COM+ manterá instâncias dele em um pool, pronto para ser ativado para qualquer cliente que solicite o componente. Qualquer solicitação de criação de objeto será manipulada por meio do Gerenciador de pool.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Como o pool de objetos funciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793972"
---
# <a name="how-object-pooling-works"></a><span data-ttu-id="7d7f0-104">Como o pool de objetos funciona</span><span class="sxs-lookup"><span data-stu-id="7d7f0-104">How Object Pooling Works</span></span>

<span data-ttu-id="7d7f0-105">Quando você configura um componente a ser agrupado, o COM+ manterá instâncias dele em um pool, pronto para ser ativado para qualquer cliente que solicite o componente.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-105">When you configure a component to be pooled, COM+ will maintain instances of it in a pool, ready to be activated for any client requesting the component.</span></span> <span data-ttu-id="7d7f0-106">Qualquer solicitação de criação de objeto será manipulada por meio do Gerenciador de pool.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-106">Any object creation requests will be handled through the pool manager.</span></span>

<span data-ttu-id="7d7f0-107">Os pools são configurados e mantidos em uma base por componente.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-107">Pools are configured and maintained on a per-component basis.</span></span> <span data-ttu-id="7d7f0-108">Um pool consiste em objetos homogêneos que compartilham o mesmo CLSID.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-108">A pool consists of homogeneous objects that share the same CLSID.</span></span> <span data-ttu-id="7d7f0-109">A única exceção é para objetos transacionais, para os quais os subpools são mantidos contendo objetos que têm afinidade de transação enquanto uma transação está pendente.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-109">The only exception is for transactional objects, for which subpools are maintained containing objects that have transaction affinity while a transaction is pending.</span></span>

<span data-ttu-id="7d7f0-110">Quando o aplicativo for iniciado, o pool será preenchido até o nível mínimo que você especificou administrativamente, desde que a criação do objeto seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-110">When the application starts, the pool will be populated up to the minimum level that you have administratively specified, as long as object creation succeeds.</span></span> <span data-ttu-id="7d7f0-111">À medida que as solicitações de cliente para o componente entram, elas são satisfeitas de acordo com a primeira base atendidas do pool.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-111">As client requests for the component come in, they are satisfied on a first-come first-served basis from the pool.</span></span> <span data-ttu-id="7d7f0-112">Se nenhum objeto em pool estiver disponível e o pool ainda não estiver no nível máximo especificado, um novo objeto será criado e ativado para o cliente.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-112">If no pooled objects are available and the pool is not yet at its specified maximum level, a new object is created and activated for the client.</span></span>

<span data-ttu-id="7d7f0-113">Quando o pool atingir seu nível máximo, as solicitações de cliente serão enfileiradas e receberão o primeiro objeto disponível do pool.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-113">When the pool reaches its maximum level, client requests are queued and will receive the first available object from the pool.</span></span> <span data-ttu-id="7d7f0-114">O número de objetos, incluindo ativado e desativado, nunca excederá o valor máximo do pool.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-114">The number of objects, including both activated and deactivated, will never exceed the maximum pool value.</span></span> <span data-ttu-id="7d7f0-115">As solicitações de criação de objeto atingirão o tempo limite após um período especificado administrativamente para que você possa controlar por quanto tempo os clientes aguardarão a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-115">Object creation requests will time out after an administratively specified period so that you can control how long clients will wait for object creation.</span></span> <span data-ttu-id="7d7f0-116">Após uma falha de tempo limite, o cliente obterá o erro E o \_ tempo limite de retorno de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7d7f0-116">Upon a time-out failure, the client will get back the error E\_TIMEOUT from [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="7d7f0-117">Sempre que possível, o COM+ tentará reutilizar um objeto depois que um cliente o liberar, até que o pool atinja seu nível máximo.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-117">Whenever possible, COM+ will attempt to reuse an object after a client releases it, until the pool reaches its maximum level.</span></span> <span data-ttu-id="7d7f0-118">O objeto é responsável por monitorar seu estado para determinar se ele pode ser reutilizado e deve retornar um valor apropriado para [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="7d7f0-118">The object is responsible for monitoring its state to determine whether it can be reused and should return an appropriate value for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="7d7f0-119">Quando um objeto em pool é criado, ele é agregado em um objeto maior que gerenciará o tempo de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-119">When a pooled object is created, it is aggregated into a larger object that will manage the object's lifetime.</span></span> <span data-ttu-id="7d7f0-120">O objeto externo chama métodos em [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) em momentos apropriados no ciclo de vida do objeto, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7d7f0-120">The outer object calls methods on [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) at appropriate times in the object's life cycle, as follows:</span></span>

-   <span data-ttu-id="7d7f0-121">O método [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) é chamado sempre que o objeto é retornado a um cliente, ativado em um contexto específico.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-121">The [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) method is called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="7d7f0-122">O método [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) é chamado sempre que um objeto é liberado pelo cliente ou, no caso de um objeto ativado por JIT, quando ele é desativado.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-122">The [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) method is called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="7d7f0-123">O método [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) é chamado sempre que um objeto deve ser retornado para o pool geral.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-123">The [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) method is called whenever an object is to be returned to the general pool.</span></span> <span data-ttu-id="7d7f0-124">Se o objeto detectar que algum recurso reutilizável está em um estado inadequado, ele deverá retornar **false** para esse método e o Gerenciador de pool descartará o objeto.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-124">If the object detects that some reusable resource is in a bad state, it should return **FALSE** for this method and the pool manager will discard the object.</span></span>

<span data-ttu-id="7d7f0-125">Um objeto não necessariamente precisa implementar [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="7d7f0-125">An object does not necessarily need to implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="7d7f0-126">Caso contrário, as instâncias serão sempre reutilizadas até que o nível máximo do pool seja atingido.</span><span class="sxs-lookup"><span data-stu-id="7d7f0-126">If it does not, instances will always be reused, until the pool maximum level is reached.</span></span>

<span data-ttu-id="7d7f0-127">Para obter detalhes sobre como configurar os componentes a serem agrupados, consulte [Configurando um componente a ser agrupado](configuring-a-component-to-be-pooled.md).</span><span class="sxs-lookup"><span data-stu-id="7d7f0-127">For details about how to configure components to be pooled, see [Configuring a Component to Be Pooled](configuring-a-component-to-be-pooled.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d7f0-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d7f0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d7f0-129">Cadeias de caracteres do construtor do objeto COM+</span><span class="sxs-lookup"><span data-stu-id="7d7f0-129">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="7d7f0-130">Controlando o tempo de vida e o estado do objeto</span><span class="sxs-lookup"><span data-stu-id="7d7f0-130">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="7d7f0-131">Melhorando o desempenho com o pooling de objetos</span><span class="sxs-lookup"><span data-stu-id="7d7f0-131">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="7d7f0-132">Pooling de objetos transacionais</span><span class="sxs-lookup"><span data-stu-id="7d7f0-132">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="7d7f0-133">Requisitos para objetos pooling</span><span class="sxs-lookup"><span data-stu-id="7d7f0-133">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
