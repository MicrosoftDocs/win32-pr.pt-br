---
description: A ativação JIT do COM+ essencialmente atinge um comprometimento entre os clientes de ávido e os servidores de velocidade para obter o desempenho ideal. Os clientes obtêm a manutenção de referências de objeto, enquanto os servidores podem gerenciar mais de forma mais minuciosa a utilização de memória.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Pooling de objetos e ativação JIT do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370502"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="9046c-104">Pooling de objetos e ativação JIT do COM+</span><span class="sxs-lookup"><span data-stu-id="9046c-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="9046c-105">A ativação JIT do COM+ essencialmente atinge um comprometimento entre os clientes de ávido e os servidores de velocidade para obter o desempenho ideal.</span><span class="sxs-lookup"><span data-stu-id="9046c-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="9046c-106">Os clientes obtêm a manutenção de referências de objeto, enquanto os servidores podem gerenciar mais de forma mais minuciosa a utilização de memória.</span><span class="sxs-lookup"><span data-stu-id="9046c-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="9046c-107">Você pode refinar isso ainda mais usando o [pool de objetos com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="9046c-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="9046c-108">Ao agrupar objetos que são ativados por JIT, você pode dedicar uma determinada quantidade de memória para manter um determinado número de objetos ativos na memória, prontos para reutilização imediata.</span><span class="sxs-lookup"><span data-stu-id="9046c-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="9046c-109">Isso faz mais sentido quando os objetos são caros de criar, como no caso em que contêm vários recursos.</span><span class="sxs-lookup"><span data-stu-id="9046c-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="9046c-110">Pooling de objetos ativados por JIT dessa maneira, você pode obter os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="9046c-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="9046c-111">Tempos de reativação de objetos muito acelerados.</span><span class="sxs-lookup"><span data-stu-id="9046c-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="9046c-112">Reutilização de recursos caros que os objetos estão mantendo.</span><span class="sxs-lookup"><span data-stu-id="9046c-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="9046c-113">Controle mais preciso da memória e do uso de recursos para os objetos em pool.</span><span class="sxs-lookup"><span data-stu-id="9046c-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="9046c-114">Retenção de flexibilidade administrativa para que seu aplicativo possa ser dimensionado para usar os recursos disponíveis e adaptar-se aos requisitos de desempenho em constante mudança.</span><span class="sxs-lookup"><span data-stu-id="9046c-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9046c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9046c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9046c-116">Conceitos de ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="9046c-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="9046c-117">Pool de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="9046c-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="9046c-118">Habilitando a ativação JIT para um componente</span><span class="sxs-lookup"><span data-stu-id="9046c-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="9046c-119">Transações e ativação JIT do COM+</span><span class="sxs-lookup"><span data-stu-id="9046c-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



