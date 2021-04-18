---
description: Os componentes transacionais que devem ser agrupados têm requisitos especiais.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Pooling de objetos transacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807903"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="27674-103">Pooling de objetos transacionais</span><span class="sxs-lookup"><span data-stu-id="27674-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="27674-104">Os componentes transacionais que devem ser agrupados têm requisitos especiais.</span><span class="sxs-lookup"><span data-stu-id="27674-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="27674-105">Listando manualmente os recursos</span><span class="sxs-lookup"><span data-stu-id="27674-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="27674-106">Objetos com pooláveis que participam de transações devem inscrever manualmente os recursos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="27674-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="27674-107">Se um objeto mantiver recursos gerenciados entre clientes, não haverá nenhuma maneira para o Gerenciador de recursos se inscrever automaticamente em uma transação quando o objeto for ativado em um determinado contexto.</span><span class="sxs-lookup"><span data-stu-id="27674-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="27674-108">O próprio objeto deve lidar com a lógica de detecção da transação, desativando a inscrição automática do Resource Manager e inscrita manualmente todos os recursos que ele contém.</span><span class="sxs-lookup"><span data-stu-id="27674-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="27674-109">As etapas para fazer isso são específicas do Gerenciador de recursos que você está usando.</span><span class="sxs-lookup"><span data-stu-id="27674-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="27674-110">Se você precisar fazer inscrição manual, consulte a documentação do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="27674-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="27674-111">Conforme descrito abaixo, os objetos podem ser agrupados com afinidade de transação enquanto uma transação está ativa e pode ser ativada com afinidade de transação, se chamada por um cliente associado a essa transação.</span><span class="sxs-lookup"><span data-stu-id="27674-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="27674-112">Antes de inscrever os recursos, primeiro você deve verificar a afinidade de transação.</span><span class="sxs-lookup"><span data-stu-id="27674-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="27674-113">Se o objeto tiver sido extraído do pool específico para essa transação, ele já terá feito trabalho nessa transação e inscrito em seus recursos.</span><span class="sxs-lookup"><span data-stu-id="27674-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="27674-114">Desativando inscrição automática</span><span class="sxs-lookup"><span data-stu-id="27674-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="27674-115">A inscrição automática deve ser desativada após o recurso ser adquirido, geralmente no construtor do objeto.</span><span class="sxs-lookup"><span data-stu-id="27674-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="27674-116">Ou seja, você desabilita a inscrição automática e, em seguida, se conecta.</span><span class="sxs-lookup"><span data-stu-id="27674-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="27674-117">Desabilitar a inscrição automática às vezes pode ser um procedimento sutil, especialmente no caso de provedores de acesso a dados em camadas.</span><span class="sxs-lookup"><span data-stu-id="27674-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="27674-118">Às vezes, a inscrição automática é acoplada ao pool de conexões, como com o ODBC e, às vezes, não, assim como ocorre com OLE DB.</span><span class="sxs-lookup"><span data-stu-id="27674-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="27674-119">Talvez seja necessário garantir que a inscrição automática esteja desativada em vários níveis de provedores.</span><span class="sxs-lookup"><span data-stu-id="27674-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="27674-120">Implementando Controledeobjetoi</span><span class="sxs-lookup"><span data-stu-id="27674-120">Implementing IObjectControl</span></span>

<span data-ttu-id="27674-121">Objetos com pooláveis que participam de transações devem monitorar o estado atual dos recursos que eles estão mantendo.</span><span class="sxs-lookup"><span data-stu-id="27674-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="27674-122">Se o objeto detectar que está em um estado não reutilizável — por exemplo, se uma conexão for inadequada, ela deverá retornar false para [**controledeobjetoi:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="27674-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="27674-123">Isso terá o efeito de descartar a instância do objeto e decretado por a transação atual.</span><span class="sxs-lookup"><span data-stu-id="27674-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="27674-124">Pools de Transaction-Specific</span><span class="sxs-lookup"><span data-stu-id="27674-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="27674-125">Um pool de objetos é geralmente homogêneo e qualquer objeto em pool que não esteja em uso no momento é bom retornar a qualquer cliente.</span><span class="sxs-lookup"><span data-stu-id="27674-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="27674-126">A única exceção a essa regra é no caso de objetos transacionais, para os quais o pool de objetos é otimizado.</span><span class="sxs-lookup"><span data-stu-id="27674-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="27674-127">Quando o cliente que solicita um objeto tiver uma transação associada, o COM+ verificará o pool em busca de um objeto disponível que já esteja associado a essa transação.</span><span class="sxs-lookup"><span data-stu-id="27674-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="27674-128">Se um objeto com afinidade de transação for encontrado, ele será retornado para o cliente; caso contrário, um objeto do pool geral será retornado.</span><span class="sxs-lookup"><span data-stu-id="27674-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="27674-129">Dessa maneira, os subpools especiais são mantidos contendo objetos com afinidade para uma transação específica.</span><span class="sxs-lookup"><span data-stu-id="27674-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="27674-130">Quando a transação é confirmada ou anulada, esses objetos são retornados ao pool geral sem afinidade de transação, prontos para serem usados por qualquer cliente.</span><span class="sxs-lookup"><span data-stu-id="27674-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="27674-131">Por esse motivo, quando o componente inscreve manualmente seus recursos gerenciados em uma transação, ele deve primeiro verificar se eles já estão inscritos.</span><span class="sxs-lookup"><span data-stu-id="27674-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="27674-132">Nesse caso, não há necessidade de se inscrever.</span><span class="sxs-lookup"><span data-stu-id="27674-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27674-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27674-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27674-134">Cadeias de caracteres do construtor do objeto COM+</span><span class="sxs-lookup"><span data-stu-id="27674-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="27674-135">Controlando o tempo de vida e o estado do objeto</span><span class="sxs-lookup"><span data-stu-id="27674-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="27674-136">Como o pool de objetos funciona</span><span class="sxs-lookup"><span data-stu-id="27674-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="27674-137">Melhorando o desempenho com o pooling de objetos</span><span class="sxs-lookup"><span data-stu-id="27674-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="27674-138">Requisitos para objetos pooling</span><span class="sxs-lookup"><span data-stu-id="27674-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



