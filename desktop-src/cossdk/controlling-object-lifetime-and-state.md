---
description: Controlando o tempo de vida e o estado do objeto
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controlando o tempo de vida e o estado do objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784584"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="afb9c-103">Controlando o tempo de vida e o estado do objeto</span><span class="sxs-lookup"><span data-stu-id="afb9c-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="afb9c-104">Um objeto em pool pode participar de como o COM+ gerencia sua atividade no pool implementando [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="afb9c-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="afb9c-105">Quando um objeto em pool é criado, ele é agregado em um objeto maior que gerenciará o objeto chamando os seguintes métodos em **controledeobjetoi** em pontos regulares no ciclo de vida do objeto:</span><span class="sxs-lookup"><span data-stu-id="afb9c-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="afb9c-106">[**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)— chamado sempre que o objeto é retornado a um cliente, ativado em um contexto específico.</span><span class="sxs-lookup"><span data-stu-id="afb9c-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="afb9c-107">[**Desativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)— chamado sempre que um objeto é liberado pelo cliente ou, no caso de um objeto ativado por JIT, quando é desativado.</span><span class="sxs-lookup"><span data-stu-id="afb9c-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="afb9c-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)— chamado sempre que um objeto deve ser retornado para o pool geral.</span><span class="sxs-lookup"><span data-stu-id="afb9c-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="afb9c-109">A implementação de [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) é opcional, exceto para objetos transacionais, que sempre devem implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) para monitorar o estado dos recursos que eles contêm.</span><span class="sxs-lookup"><span data-stu-id="afb9c-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="afb9c-110">No entanto, é aconselhável implementar **controledeobjetoi** na maioria dos casos porque ele fornece uma maneira eficiente de gerenciar o comportamento de um objeto em pool, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="afb9c-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="afb9c-111">Executando inicialização de Context-Specific</span><span class="sxs-lookup"><span data-stu-id="afb9c-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="afb9c-112">Usando [**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), você pode inicializar o objeto no contexto no qual ele é ativado para um determinado cliente.</span><span class="sxs-lookup"><span data-stu-id="afb9c-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="afb9c-113">Por exemplo, para determinar se o objeto tem afinidade de transação (seus recursos já podem estar inscritos), você pode obter a ID de transação associada ao contexto.</span><span class="sxs-lookup"><span data-stu-id="afb9c-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="afb9c-114">Normalmente, você usaria [**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)para executar a inicialização consistente em todos os métodos expostos pelo objeto, tratando-o como a parte específica do contexto do construtor do objeto.</span><span class="sxs-lookup"><span data-stu-id="afb9c-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="afb9c-115">Limpando qualquer estado do cliente</span><span class="sxs-lookup"><span data-stu-id="afb9c-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="afb9c-116">Usando [**desativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), você pode livrar-se de qualquer estado específico do cliente que possa existir para que seu objeto retorne ao pool em um estado completamente genérico e possa ser usado por qualquer cliente sem comprometer a segurança ou o isolamento.</span><span class="sxs-lookup"><span data-stu-id="afb9c-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="afb9c-117">Controlando a reutilização do objeto</span><span class="sxs-lookup"><span data-stu-id="afb9c-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="afb9c-118">Usando o [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), você pode monitorar o estado interno do seu objeto e relatar se ele se ajusta à sua reutilização.</span><span class="sxs-lookup"><span data-stu-id="afb9c-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="afb9c-119">Se **CanBePooled** retornar true e o máximo do pool não tiver sido atingido, o objeto será colocado de volta no pool geral.</span><span class="sxs-lookup"><span data-stu-id="afb9c-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="afb9c-120">Se **CanBePooled** retornar false, o objeto será Descartado.</span><span class="sxs-lookup"><span data-stu-id="afb9c-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="afb9c-121">No caso de componentes transacionais, retornar false irá destruição a transação atual.</span><span class="sxs-lookup"><span data-stu-id="afb9c-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="afb9c-122">Normalmente, você manteria algum membro de dados globais para o objeto e, se detectar uma conexão como insatisfatório ou um recurso de algum tipo para estar em um estado inadequado, defina isso para refletir a situação atual e retorná-la por meio de [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="afb9c-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="afb9c-123">Se um objeto não implementar [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), as instâncias continuarão sendo reutilizadas até que o nível máximo do pool seja atingido.</span><span class="sxs-lookup"><span data-stu-id="afb9c-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afb9c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="afb9c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afb9c-125">Cadeias de caracteres do construtor do objeto COM+</span><span class="sxs-lookup"><span data-stu-id="afb9c-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="afb9c-126">Como o pool de objetos funciona</span><span class="sxs-lookup"><span data-stu-id="afb9c-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="afb9c-127">Melhorando o desempenho com o pooling de objetos</span><span class="sxs-lookup"><span data-stu-id="afb9c-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="afb9c-128">Pooling de objetos transacionais</span><span class="sxs-lookup"><span data-stu-id="afb9c-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="afb9c-129">Requisitos para objetos pooling</span><span class="sxs-lookup"><span data-stu-id="afb9c-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



