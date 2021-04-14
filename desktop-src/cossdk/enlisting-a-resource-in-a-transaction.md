---
description: Inlistando um recurso em uma transação
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Inlistando um recurso em uma transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370505"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="94164-103">Inlistando um recurso em uma transação</span><span class="sxs-lookup"><span data-stu-id="94164-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="94164-104">Depois que um recurso é alocado, mas antes de retornar o recurso para o dispensador de recurso, o Gerenciador do dispensador verifica com COM+ para ver se o objeto de chamada está sendo executado dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="94164-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="94164-105">Se o objeto de chamada estiver sendo executado em uma transação, o Gerenciador do dispensador chamará de volta para o dispensador de recursos e solicitará que ele inscreva o recurso na transação.</span><span class="sxs-lookup"><span data-stu-id="94164-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="94164-106">Em seguida, o recurso é retornado para o dispensador de recursos, que o retorna para a instância de chamada.</span><span class="sxs-lookup"><span data-stu-id="94164-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="94164-107">O dispensador de recursos deve ser capaz de se inscrever em uma transação OLE com o Coordenador de Transações Distribuídas (DTC).</span><span class="sxs-lookup"><span data-stu-id="94164-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="94164-108">A inscrição de transação é opcional quando um dispensador de recurso dispensa recursos não transacionais, como memória ou threads.</span><span class="sxs-lookup"><span data-stu-id="94164-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="94164-109">Quando uma transação é concluída, o COM+ notifica o Gerenciador do dispensador sobre se ele foi confirmado ou anulado.</span><span class="sxs-lookup"><span data-stu-id="94164-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="94164-110">Em seguida, o Gerenciador do dispensador notifica o detentor de cada dispensador de recursos de que todos os recursos inscritos nesta transação agora podem ser movidos para o inventário geral.</span><span class="sxs-lookup"><span data-stu-id="94164-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94164-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94164-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94164-112">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="94164-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="94164-113">Estados de recursos em pool disponíveis para o dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="94164-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="94164-114">Processo de alocação de recursos do dispensador de recursos</span><span class="sxs-lookup"><span data-stu-id="94164-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



