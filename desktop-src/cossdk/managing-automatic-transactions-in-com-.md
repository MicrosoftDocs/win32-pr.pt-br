---
description: No modelo de programação COM+, você pode criar seus componentes para fazer o que eles fazem melhor&\# 8212; habilitar a lógica de negócios ou estabelecer uma conexão de banco de dados&\# 8212; e contar com a estrutura de processamento de transações do Microsoft Windows para automatizar transações.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Gerenciando transações automáticas no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501051"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="3e622-103">Gerenciando transações automáticas no COM+</span><span class="sxs-lookup"><span data-stu-id="3e622-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="3e622-104">No modelo de programação COM+, você pode projetar seus componentes para fazer o que eles fazem melhor — habilitar a lógica de negócios ou estabelecer uma conexão de banco de dados — e contar com a estrutura de processamento de transações do Microsoft Windows para automatizar transações.</span><span class="sxs-lookup"><span data-stu-id="3e622-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="3e622-105">Iniciando uma transação</span><span class="sxs-lookup"><span data-stu-id="3e622-105">Starting a Transaction</span></span>

<span data-ttu-id="3e622-106">O COM+ inicia automaticamente uma transação quando encontra uma das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="3e622-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="3e622-107">Quando um cliente não transacional chama um componente que requer uma transação ou requer uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="3e622-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="3e622-108">Quando um cliente transacional chama um componente que requer uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="3e622-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="3e622-109">Se o COM+ determinar que um objeto deve ter uma nova transação, ele iniciará a transação primeiro e, em seguida, colocará o objeto nela.</span><span class="sxs-lookup"><span data-stu-id="3e622-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="3e622-110">O processo inclui as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3e622-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="3e622-111">O COM+ cria um objeto de contexto, define os atributos de [ativação JIT](com--just-in-time-activation.md) e de [sincronização](com--synchronization.md) como Required e define os [sinalizadores consistentes e concluídos](consistent-and-done-flags.md) como true e false, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3e622-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="3e622-112">O COM+ se comunica com o Coordenador de Transações Distribuídas (DTC) para iniciar uma transação.</span><span class="sxs-lookup"><span data-stu-id="3e622-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="3e622-113">O DTC coordena a transação física.</span><span class="sxs-lookup"><span data-stu-id="3e622-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="3e622-114">O DTC gera um identificador de transação e o passa de volta para o COM+.</span><span class="sxs-lookup"><span data-stu-id="3e622-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="3e622-115">O identificador de transação estabelece um limite de transação.</span><span class="sxs-lookup"><span data-stu-id="3e622-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="3e622-116">Todos os objetos que participam da transação compartilham o mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="3e622-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="3e622-117">Quando o cliente cria o objeto, o COM+ o ativa dentro do limite da transação.</span><span class="sxs-lookup"><span data-stu-id="3e622-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="3e622-118">Finalizando uma transação</span><span class="sxs-lookup"><span data-stu-id="3e622-118">Ending a Transaction</span></span>

<span data-ttu-id="3e622-119">O COM+ encerra uma transação automática confirmando ou anulando-a quando uma das seguintes condições ocorre:</span><span class="sxs-lookup"><span data-stu-id="3e622-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="3e622-120">O objeto raiz da transação conclui seu trabalho e o COM+ o libera.</span><span class="sxs-lookup"><span data-stu-id="3e622-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="3e622-121">Depois que o objeto raiz é desativado, a transação tenta confirmar.</span><span class="sxs-lookup"><span data-stu-id="3e622-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="3e622-122">O cliente libera o objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="3e622-122">The client releases the root object.</span></span> <span data-ttu-id="3e622-123">Sem uma referência, o objeto raiz é desativado e a transação tenta confirmar.</span><span class="sxs-lookup"><span data-stu-id="3e622-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="3e622-124">A transação excede o limite de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="3e622-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="3e622-125">A transação é anulada automaticamente se não confirmada no período de tempo limite da transação, desativando todos os objetos associados à transação.</span><span class="sxs-lookup"><span data-stu-id="3e622-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="3e622-126">O período de tempo limite de transação padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="3e622-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e622-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e622-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e622-128">Sinalizadores consistentes e concluídos</span><span class="sxs-lookup"><span data-stu-id="3e622-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="3e622-129">Acelerando as transações notificando o objeto raiz</span><span class="sxs-lookup"><span data-stu-id="3e622-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="3e622-130">Finalizando uma transação automática chamando SetComplete</span><span class="sxs-lookup"><span data-stu-id="3e622-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



