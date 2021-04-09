---
description: Cunhado por pioneiros no processamento de transações, o acrônimo ACID significa Atomic, consistente, isolado e durável.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Propriedades ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089138"
---
# <a name="acid-properties"></a><span data-ttu-id="3c611-103">Propriedades ACID</span><span class="sxs-lookup"><span data-stu-id="3c611-103">ACID Properties</span></span>

<span data-ttu-id="3c611-104">Cunhado por pioneiros no processamento de transações, o acrônimo ACID significa Atomic, consistente, isolado e durável.</span><span class="sxs-lookup"><span data-stu-id="3c611-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="3c611-105">Para garantir um comportamento previsível, todas as transações devem possuir essas propriedades básicas, reforçando a função de transações críticas como proposições de todas as-ou-nenhuma.</span><span class="sxs-lookup"><span data-stu-id="3c611-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="3c611-106">A lista a seguir contém uma definição e uma descrição de cada propriedade ACID:</span><span class="sxs-lookup"><span data-stu-id="3c611-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="3c611-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atômica</span><span class="sxs-lookup"><span data-stu-id="3c611-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="3c611-108">Uma transação deve ser executada exatamente uma vez e deve ser atômica – qualquer trabalho é feito ou nenhum deles é.</span><span class="sxs-lookup"><span data-stu-id="3c611-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="3c611-109">As operações em uma transação geralmente compartilham uma intenção comum e são interdependentes.</span><span class="sxs-lookup"><span data-stu-id="3c611-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="3c611-110">Ao executar apenas um subconjunto dessas operações, o sistema pode comprometer a intenção geral da transação.</span><span class="sxs-lookup"><span data-stu-id="3c611-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="3c611-111">A atomicidade elimina a chance de processar apenas um subconjunto de operações.</span><span class="sxs-lookup"><span data-stu-id="3c611-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="3c611-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente</span><span class="sxs-lookup"><span data-stu-id="3c611-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="3c611-113">Uma transação deve preservar a consistência dos dados, transformando um estado consistente de dados em outro estado consistente de dados.</span><span class="sxs-lookup"><span data-stu-id="3c611-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="3c611-114">Grande parte da responsabilidade de manter a consistência cai ao desenvolvedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c611-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="3c611-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolados</span><span class="sxs-lookup"><span data-stu-id="3c611-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="3c611-116">Uma transação deve ser uma unidade de isolamento, o que significa que as transações simultâneas devem se comportar como se cada uma fosse a única transação em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="3c611-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="3c611-117">Como um alto grau de isolamento pode limitar o número de transações simultâneas, alguns aplicativos reduzem o nível de isolamento no Exchange para melhorar a taxa de transferência.</span><span class="sxs-lookup"><span data-stu-id="3c611-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="3c611-118">Consulte [Configurando níveis de isolamento da transação](configuring-transaction-isolation-levels.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3c611-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="3c611-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Permanente</span><span class="sxs-lookup"><span data-stu-id="3c611-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="3c611-120">Uma transação deve ser recuperável e, portanto, deve ter durabilidade.</span><span class="sxs-lookup"><span data-stu-id="3c611-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="3c611-121">Se uma transação for confirmada, o sistema garante que suas atualizações possam persistir mesmo se o computador falhar imediatamente após a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3c611-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="3c611-122">O log especializado permite que o procedimento de reinicialização do sistema conclua as operações não concluídas exigidas pela transação, tornando a transação durável.</span><span class="sxs-lookup"><span data-stu-id="3c611-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



