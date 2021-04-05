---
description: Transações e ativação JIT do COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transações e ativação JIT do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826605"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="31266-103">Transações e ativação JIT do COM+</span><span class="sxs-lookup"><span data-stu-id="31266-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="31266-104">A ativação JIT do COM+ está fortemente ligada a transações automáticas.</span><span class="sxs-lookup"><span data-stu-id="31266-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="31266-105">Quando você configura um componente para que ele exija uma transação ou requer uma nova transação, a ativação JIT também é habilitada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="31266-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="31266-106">Os dois recursos funcionam naturalmente em conjunto.</span><span class="sxs-lookup"><span data-stu-id="31266-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="31266-107">Os componentes transacionais ativados por JIT compartilham as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="31266-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="31266-108">Sem estado.</span><span class="sxs-lookup"><span data-stu-id="31266-108">Statelessness.</span></span> <span data-ttu-id="31266-109">Você não manteria um estado que poderia violar o isolamento da transação, ou você manteria um estado que seria perdido na desativação do objeto.</span><span class="sxs-lookup"><span data-stu-id="31266-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="31266-110">Uso rápido.</span><span class="sxs-lookup"><span data-stu-id="31266-110">Rapid use.</span></span> <span data-ttu-id="31266-111">O padrão de uso canônico para um objeto que executa o trabalho em uma transação automática é fazer alguma pequena unidade de trabalho, votar e sair.</span><span class="sxs-lookup"><span data-stu-id="31266-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="31266-112">As maneiras de votar em transações COM+ e no sentido de sinal para ativação JIT também estão ligadas em conjunto.</span><span class="sxs-lookup"><span data-stu-id="31266-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="31266-113">Para obter mais informações, consulte [definindo o bit concluído](setting-the-done-bit.md).</span><span class="sxs-lookup"><span data-stu-id="31266-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="31266-114">Uso repetido.</span><span class="sxs-lookup"><span data-stu-id="31266-114">Repeated use.</span></span> <span data-ttu-id="31266-115">Quando o trabalho transacional é dividido corretamente, os clientes usam os mesmos objetos várias vezes para executar pequenos totais de trabalho atômico.</span><span class="sxs-lookup"><span data-stu-id="31266-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="31266-116">Desativado na confirmação ou anulação.</span><span class="sxs-lookup"><span data-stu-id="31266-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="31266-117">No COM+, todos os objetos dentro do limite de transação são desativados quando a transação é confirmada ou anulada.</span><span class="sxs-lookup"><span data-stu-id="31266-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="31266-118">Em conjunto com componentes transacionais COM+, a ativação JIT serve como um aprimoramento de grande desempenho mantendo o canal aberto, pois os clientes mantêm referências de longa duração a objetos transacionais.</span><span class="sxs-lookup"><span data-stu-id="31266-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="31266-119">Como aprimoramentos adicionais, você pode optar por agrupar os objetos transacionais para reutilizar os recursos que eles contêm, acelerar o tempo de reativação do objeto e gerenciar de maneira minuciosa como você usa os recursos de memória para determinados objetos.</span><span class="sxs-lookup"><span data-stu-id="31266-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31266-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31266-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31266-121">Conceitos de ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="31266-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="31266-122">Habilitando a ativação JIT para um componente</span><span class="sxs-lookup"><span data-stu-id="31266-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="31266-123">Pooling de objetos e ativação JIT do COM+</span><span class="sxs-lookup"><span data-stu-id="31266-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



