---
description: O Gerenciador do dispensador fornece o pool de recursos para os dispensadores de recursos e garante que um recurso fornecido por um dispensador de recursos seja inscrito corretamente na transação de objetos de aplicativo.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Gerenciador do dispensador COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500932"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="b0449-103">Gerenciador do dispensador COM+</span><span class="sxs-lookup"><span data-stu-id="b0449-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="b0449-104">O Gerenciador do dispensador fornece o pool de recursos para os dispensadores de recursos e garante que um recurso fornecido por um dispensador de recursos seja inscrito corretamente na transação do objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0449-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="b0449-105">O Gerenciador do dispensador recupera automaticamente os recursos que ainda estão reservados no final do tempo de vida de um objeto, eliminando a possibilidade de "vazamentos" de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0449-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="b0449-106">O Gerenciador do dispensador pode pedir que um dispensador de recursos crie um novo recurso ou destrua recursos ociosos quando necessário para ajustar os níveis de inventário, em vez de usar configurações estáticas.</span><span class="sxs-lookup"><span data-stu-id="b0449-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="b0449-107">Como as interfaces do dispensador de recursos expostas ao aplicativo não precisam ser interfaces COM, o Gerenciador do dispensador pode ser usado em um processo sem inicializar COM, por exemplo, para dar suporte ao dispensador de recursos ODBC.</span><span class="sxs-lookup"><span data-stu-id="b0449-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="b0449-108">Após a criação do recurso, o dispensador de recursos pode especificar quanto tempo um recurso ocioso tem permissão para permanecer no pool antes de ser destruído.</span><span class="sxs-lookup"><span data-stu-id="b0449-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="b0449-109">Um thread que é executado no Gerenciador do dispensador está sempre procurando esses recursos ociosos.</span><span class="sxs-lookup"><span data-stu-id="b0449-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="b0449-110">O Gerenciador de estatísticas de inventário</span><span class="sxs-lookup"><span data-stu-id="b0449-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="b0449-111">O Gerenciador do dispensador usa o *Gerenciador de estatísticas de inventário* para gerenciar os níveis de inventário de recursos de pool.</span><span class="sxs-lookup"><span data-stu-id="b0449-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="b0449-112">O Gerenciador de estatísticas de inventário mantém um registro de quando cada recurso foi usado e remove recursos do inventário quando eles não são usados por *x* segundos, em que o valor de *x* é definido por recurso quando o recurso é criado.</span><span class="sxs-lookup"><span data-stu-id="b0449-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="b0449-113">O componente de detentor</span><span class="sxs-lookup"><span data-stu-id="b0449-113">The Holder Component</span></span>

<span data-ttu-id="b0449-114">O gerente do dispensador sonda cada *portador*, um componente criado pelo Gerenciador do dispensador que lista o inventário de recursos para cada dispensador de recursos, a cada 10 segundos, para permitir que ele reajuste seu inventário de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0449-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="b0449-115">Cada portador chama o Gerenciador de estatísticas de inventário para sugerir os níveis de estoque para cada tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b0449-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="b0449-116">Como resultado, o detentor pode pedir que o dispensador de recursos crie ou destrua algum inventário.</span><span class="sxs-lookup"><span data-stu-id="b0449-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="b0449-117">O detentor e o dispensador de recursos se comunicam com os recursos de solicitação de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="b0449-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="b0449-118">As seguintes relações existem entre o detentor e o dispensador de recursos:</span><span class="sxs-lookup"><span data-stu-id="b0449-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="b0449-119">O detentor pode solicitar um recurso do dispensador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0449-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="b0449-120">O dispensador de recursos retorna um recurso disponível ou cria um novo.</span><span class="sxs-lookup"><span data-stu-id="b0449-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="b0449-121">O detentor pode notificar o dispensador de recursos de que um aplicativo não precisa mais de um recurso e, em seguida, retorná-lo ao pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0449-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="b0449-122">O detentor e o dispensador de recursos trabalham juntos para manter o tamanho do pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0449-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0449-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0449-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0449-124">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="b0449-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



