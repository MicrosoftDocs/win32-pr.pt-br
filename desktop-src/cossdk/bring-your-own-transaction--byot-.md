---
description: Traga sua própria transação (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Traga sua própria transação (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764595"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="d1cc3-103">Traga sua própria transação (BYOT)</span><span class="sxs-lookup"><span data-stu-id="d1cc3-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="d1cc3-104">O BYOT permite que um componente seja criado com ou para herdar uma transação externa.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="d1cc3-105">Ou seja, um componente que ainda não tem uma transação associada pode adquirir uma transação.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="d1cc3-106">Atualmente, as transações MTS são automáticas; se uma instância de componente reside em uma transação é determinada no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="d1cc3-107">Os atributos transacionais de um componente e seu criador determinam qual transação está associada a uma determinada instância.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="d1cc3-108">Em todos os casos, o MTS controla os tempos de vida das transações.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="d1cc3-109">O COM+ estende isso para permitir a definição de uma transação do DTC ou TIP preexistente arbitrária como a propriedade Transaction do contexto de um novo componente.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="d1cc3-110">Isso permite que os componentes configurados sejam associados a transações cujos tempos de vida são controlados por um monitor TP, OTS ou DBMS.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="d1cc3-111">As transações de BYOT devem ser usadas com cautela.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="d1cc3-112">Em determinadas situações, eles podem resultar em uma transação que abrange vários domínios de sincronização, ou seja, eles permitem paralelismo com uma transação, causando uma condição de deadlock.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="d1cc3-113">Transações automáticas, em vez de transações de BYOT, são o modelo de programação preferencial para escritores de componentes comerciais.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="d1cc3-114">As interfaces para transações de BYOT incluem a interface [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e a interface [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) .</span><span class="sxs-lookup"><span data-stu-id="d1cc3-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="d1cc3-115">A interface **ICreateWithTransactionEx** cria um objeto que é inscrito em uma transação manual.</span><span class="sxs-lookup"><span data-stu-id="d1cc3-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="d1cc3-116">A interface **ICreateWithTipTransactionEx** cria um objeto que é inscrito em uma transação manual usando o TIP (protocolo de Internet de transação).</span><span class="sxs-lookup"><span data-stu-id="d1cc3-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1cc3-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1cc3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1cc3-118">Herdando transações manuais</span><span class="sxs-lookup"><span data-stu-id="d1cc3-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 



