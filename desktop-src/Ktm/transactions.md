---
description: Uma transação é um objeto que define uma unidade lógica de trabalho.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transações (kernel Transaction Manager)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778425"
---
# <a name="transactions"></a><span data-ttu-id="b33be-103">Transactions</span><span class="sxs-lookup"><span data-stu-id="b33be-103">Transactions</span></span>

<span data-ttu-id="b33be-104">Uma transação é um objeto que define uma unidade lógica de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b33be-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="b33be-105">A transação estará ativa contanto que haja um identificador que referencie a transação e ela será considerada ativa se a transação ainda não tiver sido confirmada ou revertida.</span><span class="sxs-lookup"><span data-stu-id="b33be-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="b33be-106">Se uma transação for criada e todos os identificadores tiverem sido fechados antes de uma confirmação ou reversão ocorrer, a transação será revertida.</span><span class="sxs-lookup"><span data-stu-id="b33be-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="b33be-107">Considere o caso de um cliente transacional de modo de usuário que cria uma transação para o escopo de suas operações e, em seguida, executa atualizações em um ou mais gerenciadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="b33be-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="b33be-108">Ocorre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b33be-108">The following occurs:</span></span>

1.  <span data-ttu-id="b33be-109">O cliente chama a função [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) para criar a transação e recebe um identificador para essa transação como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b33be-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="b33be-110">A transação pode ser aberta ou herdada por qualquer número de processos; cada processo é, portanto, envolvido na transação.</span><span class="sxs-lookup"><span data-stu-id="b33be-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="b33be-111">A falha de qualquer um desses processos fará com que a transação seja anulada.</span><span class="sxs-lookup"><span data-stu-id="b33be-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="b33be-112">Esta transação ainda não pode ser persistente.</span><span class="sxs-lookup"><span data-stu-id="b33be-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="b33be-113">Somente as transações que atingiram o estado preparado devem ser recuperadas entre falhas do sistema se a transação usar o registro em log de anulação presumido.</span><span class="sxs-lookup"><span data-stu-id="b33be-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="b33be-114">O cliente deve passar uma transação para o Gerenciador de recursos explicitamente.</span><span class="sxs-lookup"><span data-stu-id="b33be-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="b33be-115">O cliente executa todas as suas operações transacionais com um ou mais RMs, como sistemas de arquivos transacionados.</span><span class="sxs-lookup"><span data-stu-id="b33be-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="b33be-116">O cliente chama a função [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .</span><span class="sxs-lookup"><span data-stu-id="b33be-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="b33be-117">O Gerenciador de recursos recebe notificações do KTM para preparar e confirmar seus dados.</span><span class="sxs-lookup"><span data-stu-id="b33be-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="b33be-118">Transações e threads</span><span class="sxs-lookup"><span data-stu-id="b33be-118">Transactions and Threads</span></span>

<span data-ttu-id="b33be-119">As transações não são as mesmas que os threads.</span><span class="sxs-lookup"><span data-stu-id="b33be-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="b33be-120">Vários threads ou processos podem fazer parte de uma única transação.</span><span class="sxs-lookup"><span data-stu-id="b33be-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="b33be-121">Por outro lado, um thread pode fazer parte de várias transações diferentes em momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="b33be-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="b33be-122">Funções de transação</span><span class="sxs-lookup"><span data-stu-id="b33be-122">Transaction Functions</span></span>

<span data-ttu-id="b33be-123">As funções a seguir são usadas com transações.</span><span class="sxs-lookup"><span data-stu-id="b33be-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="b33be-124">Função</span><span class="sxs-lookup"><span data-stu-id="b33be-124">Function</span></span>                                                            | <span data-ttu-id="b33be-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="b33be-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b33be-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="b33be-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="b33be-127">Solicita que a transação especificada seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="b33be-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="b33be-128">**CommitTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="b33be-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="b33be-129">Solicita que a transação especificada seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="b33be-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="b33be-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="b33be-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="b33be-131">Cria um novo objeto de transação.</span><span class="sxs-lookup"><span data-stu-id="b33be-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="b33be-132">**GetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="b33be-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="b33be-133">Retorna as informações solicitadas sobre a transação especificada.</span><span class="sxs-lookup"><span data-stu-id="b33be-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="b33be-134">**OpenTransaction**</span><span class="sxs-lookup"><span data-stu-id="b33be-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="b33be-135">Abre uma transação existente.</span><span class="sxs-lookup"><span data-stu-id="b33be-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="b33be-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="b33be-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="b33be-137">Solicita que a transação especificada seja revertida.</span><span class="sxs-lookup"><span data-stu-id="b33be-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="b33be-138">**RollbackTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="b33be-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="b33be-139">Solicita que a transação especificada seja revertida.</span><span class="sxs-lookup"><span data-stu-id="b33be-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="b33be-140">Essa função retorna de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b33be-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="b33be-141">**SetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="b33be-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="b33be-142">Define as informações da transação para a transação especificada.</span><span class="sxs-lookup"><span data-stu-id="b33be-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 



