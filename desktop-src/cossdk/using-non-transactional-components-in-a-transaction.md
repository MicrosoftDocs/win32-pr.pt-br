---
description: Usando componentes não transacionais em uma transação
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Usando componentes não transacionais em uma transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646522"
---
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="78de9-103">Usando componentes não transacionais em uma transação</span><span class="sxs-lookup"><span data-stu-id="78de9-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="78de9-104">Geralmente, é útil colocar componentes não transacionais em uma transação para aproveitar as [Propriedades Acid](acid-properties.md) de transações.</span><span class="sxs-lookup"><span data-stu-id="78de9-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="78de9-105">Por exemplo, se você tiver componentes herdados não transacionais que você usa para atualizar senhas em uma rede, poderá colocá-los em uma transação para garantir que as atualizações de senha sejam consistentes na rede.</span><span class="sxs-lookup"><span data-stu-id="78de9-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="78de9-106">O *objeto de contexto de transação* é um objeto genérico que permite que clientes não transacionais combinem o trabalho de vários objetos com em uma única transação, sem exigir que você desenvolva um novo componente especificamente para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="78de9-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="78de9-107">Ao contrário de uma transação automática, o objeto de contexto de transação exige que seu cliente confirme ou anule explicitamente a transação.</span><span class="sxs-lookup"><span data-stu-id="78de9-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="78de9-108">Por padrão, o valor do atributo Transaction do objeto de contexto de transação é definido como Required.</span><span class="sxs-lookup"><span data-stu-id="78de9-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="78de9-109">O COM+ anulará a transação se o cliente liberar o objeto de contexto de transação sem emitir explicitamente uma chamada Commit ou Abort.</span><span class="sxs-lookup"><span data-stu-id="78de9-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="78de9-110">O exemplo a seguir Visual Basic mostra como um cliente não transacional pode compor o trabalho feito por mais de um objeto em uma única transação:</span><span class="sxs-lookup"><span data-stu-id="78de9-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="78de9-111">Limitações do objeto de contexto de transação</span><span class="sxs-lookup"><span data-stu-id="78de9-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="78de9-112">A seguir estão algumas limitações importantes do objeto de contexto de transação:</span><span class="sxs-lookup"><span data-stu-id="78de9-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="78de9-113">Ao usar um objeto de contexto de transação, a lógica do aplicativo que combina o trabalho de vários objetos em uma única transação é vinculada a uma implementação de cliente não transacional específica e algumas vantagens de usar componentes COM são perdidas.</span><span class="sxs-lookup"><span data-stu-id="78de9-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="78de9-114">Essas vantagens perdidas incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="78de9-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="78de9-115">Capacidade de reutilizar a lógica do aplicativo como parte de uma transação ainda maior</span><span class="sxs-lookup"><span data-stu-id="78de9-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="78de9-116">Imposição de segurança declarativa</span><span class="sxs-lookup"><span data-stu-id="78de9-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="78de9-117">Flexibilidade para executar a lógica remotamente do cliente</span><span class="sxs-lookup"><span data-stu-id="78de9-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="78de9-118">O objeto de contexto de transação é executado em processo com o cliente não transacional, o que significa que o COM+ deve estar disponível no computador cliente não transacional.</span><span class="sxs-lookup"><span data-stu-id="78de9-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="78de9-119">Isso pode não ser um problema, por exemplo, quando o objeto de contexto de transação é usado em uma página de Active Server páginas (ASP) que está sendo executada no mesmo servidor que o COM+.</span><span class="sxs-lookup"><span data-stu-id="78de9-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="78de9-120">Você não obtém um contexto para o cliente não transacional quando cria um objeto de contexto de transação.</span><span class="sxs-lookup"><span data-stu-id="78de9-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="78de9-121">O trabalho transacional só pode ser feito indiretamente, por meio de objetos COM criados com o uso do objeto de contexto de transação.</span><span class="sxs-lookup"><span data-stu-id="78de9-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="78de9-122">Em particular, o cliente não transacional não pode usar dispensadores de recursos COM+ (como ODBC) e ter o trabalho incluído na transação.</span><span class="sxs-lookup"><span data-stu-id="78de9-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="78de9-123">Por exemplo, os desenvolvedores podem estar familiarizados com a seguinte sintaxe para fazer trabalhos transacionais em sistemas de banco de dados relacionais:</span><span class="sxs-lookup"><span data-stu-id="78de9-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="78de9-124">Usar o objeto de contexto de transação de forma semelhante não produz o resultado desejado:</span><span class="sxs-lookup"><span data-stu-id="78de9-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="78de9-125">A chamada para DoWork neste exemplo não está inscrito em uma transação.</span><span class="sxs-lookup"><span data-stu-id="78de9-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="78de9-126">Em vez disso, você deve criar um componente COM que chama DoWork, criar uma instância de objeto desse componente usando o objeto de contexto de transação e, em seguida, chamar esse objeto do cliente não transacional para que o trabalho faça parte da transação controlada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="78de9-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



