---
description: Processo de alocação de recursos do dispensador de recursos
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processo de alocação de recursos do dispensador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164017"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="0a0c3-103">Processo de alocação de recursos do dispensador de recursos</span><span class="sxs-lookup"><span data-stu-id="0a0c3-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="0a0c3-104">Cada vez que um dispensador de recursos aloca um recurso do seu detentor, ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0a0c3-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="0a0c3-105">O dispensador de recurso declara um identificador de tipo de recurso (**RESTYPID**), que descreve o tipo de recurso necessário.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="0a0c3-106">O dispensador de recurso chama o método [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) do titular, passando esse **RESTYPID**.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="0a0c3-107">O detentor gera uma lista de candidatos dos recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="0a0c3-108">Os candidatos são recursos que não estão inscritos em uma transação ou já inscritos na transação do objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="0a0c3-109">Esses candidatos são passados individualmente para o método [**IDispenserDriver:: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , onde são classificados (em uma escala de 0 a 100) por quão bem o recurso candidato corresponde ao **RESTYPID** desejado.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="0a0c3-110">O detentor escolhe o recurso que o dispensador de recurso classifica como mais alto.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="0a0c3-111">O dispensador de recursos pode encerrar o loop de classificação no início, atribuindo ao candidato uma classificação de recursos de 100 (um ajuste perfeito).</span><span class="sxs-lookup"><span data-stu-id="0a0c3-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="0a0c3-112">Uma classificação de 100 normalmente seria reservada para os recursos candidatos que já estão inscritos corretamente, a menos que o dispensador de recursos conclua que a inscrição é uma operação barata.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="0a0c3-113">Se todos os recursos candidatos (se houver) forem classificados como 0 (inutilizável), um novo recurso será criado chamando [**IDispenserDriver:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span><span class="sxs-lookup"><span data-stu-id="0a0c3-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="0a0c3-114">Se o recurso escolhido anteriormente ainda não estiver inscrito na transação do objeto de chamada, o método [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) do dispensador de recursos será chamado.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="0a0c3-115">A chamada do método [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) retorna ao dispensador de recurso com o recurso inscrito.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a0c3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a0c3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a0c3-117">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="0a0c3-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="0a0c3-118">Inlistando um recurso em uma transação</span><span class="sxs-lookup"><span data-stu-id="0a0c3-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="0a0c3-119">Controlando recursos não alocados</span><span class="sxs-lookup"><span data-stu-id="0a0c3-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



