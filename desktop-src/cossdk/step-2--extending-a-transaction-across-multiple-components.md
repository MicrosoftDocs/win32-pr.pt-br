---
description: 'Etapa 2: estendendo uma transação entre vários componentes'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Etapa 2: estendendo uma transação entre vários componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104297836"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="4c6ac-103">Etapa 2: estendendo uma transação entre componentes</span><span class="sxs-lookup"><span data-stu-id="4c6ac-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="4c6ac-104">Objetivos</span><span class="sxs-lookup"><span data-stu-id="4c6ac-104">Objectives</span></span>

<span data-ttu-id="4c6ac-105">Nesta etapa, você aprenderá sobre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4c6ac-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="4c6ac-106">Fluxo de transações</span><span class="sxs-lookup"><span data-stu-id="4c6ac-106">Transaction flow</span></span>
-   <span data-ttu-id="4c6ac-107">Como vários objetos votam em uma transação</span><span class="sxs-lookup"><span data-stu-id="4c6ac-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="4c6ac-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c6ac-108">Description</span></span>

<span data-ttu-id="4c6ac-109">[Etapa 1: a criação de um componente transacional](step-1--creating-a-transactional-component.md) mostra como escrever um componente transacional simples que atualiza informações de autor no banco de dados de Microsoft SQL Server pubs.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="4c6ac-110">A etapa 2 mostra o que acontece quando uma transação é estendida entre vários componentes.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="4c6ac-111">Ao manter o modelo de programação COM+, o `UpdateAuthorAddress` chama outro componente no decorrer de concluir seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="4c6ac-112">O segundo componente, `ValidateAuthorAddress` , valida o endereço do autor e retorna os resultados para seu chamador, `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="4c6ac-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="4c6ac-113">Ao contrário de seu chamador, `ValidateAuthorAddress` o não requer uma transação, mas ainda pode participar da transação do chamador.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="4c6ac-114">Nesta etapa, seu valor de atributo de transação é definido como **com suporte**, conforme mostrado na ilustração a seguir, que estende a transação existente para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![Diagrama que mostra a extensão da transação existente para o novo objeto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="4c6ac-116">O valor de atributo **com suporte** estende (ou flui) uma transação existente somente quando o chamador é transacional.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="4c6ac-117">Quando `UpdateAuthorAddress` chamadas `ValidateAuthorAddress` , o com+ primeiro examina o contexto do chamador para ver se ele é transacional.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="4c6ac-118">Em seguida, o COM+ examina os atributos de serviço definidos em `ValidateAuthorAddress` e atribui o novo objeto ao mesmo identificador de transação atribuído ao objeto chamador.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="4c6ac-119">Para entender melhor esse processo, consulte [ativação de contexto](context-activation.md).</span><span class="sxs-lookup"><span data-stu-id="4c6ac-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="4c6ac-120">Como eles compartilham o mesmo identificador de transação, os dois objetos devem concluir o trabalho com êxito ou o COM+ anula a transação (desfazendo as alterações feitas no banco de dados pubs).</span><span class="sxs-lookup"><span data-stu-id="4c6ac-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="4c6ac-121">Todos os objetos que participam de uma transação votam para confirmar ou anular a transação.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="4c6ac-122">A votação ocorre explicitamente quando você inclui instruções de votação em seu código, conforme mostrado na seguinte extração do código de exemplo da etapa 1, que cria o `UpdateAuthorAddress` componente:</span><span class="sxs-lookup"><span data-stu-id="4c6ac-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="4c6ac-123">A votação também ocorre implicitamente, como é feito no `ValidateAuthorAddress` componente.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="4c6ac-124">A menos que o objeto declare de outra forma, o COM+ pressupõe que um objeto concluiu seu trabalho com êxito, mas que ele não está pronto para ser desativado.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="4c6ac-125">O COM+ faz a seguinte suposição:</span><span class="sxs-lookup"><span data-stu-id="4c6ac-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="4c6ac-126">Quando `ValidateAuthorAddress` retorna ao chamador, o com+ lê seu voto como uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="4c6ac-127">O COM+ não conta os votos até que ele desative o objeto raiz, que é o primeiro objeto na transação, nesse caso, o `UpdateAuthorAddress` objeto.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="4c6ac-128">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="4c6ac-128">Sample code</span></span>

<span data-ttu-id="4c6ac-129">O `ValidateAuthorAddress` componente faz uma verificação simples do endereço do autor.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="4c6ac-130">Como o `UpdateAuthorAddress` não votar explicitamente, o com+ usa as configurações de voto padrão.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="4c6ac-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="4c6ac-131">Summary</span></span>

-   <span data-ttu-id="4c6ac-132">Definir o atributo Transaction de um componente como **com suporte** pode resultar no novo objeto que está sendo criado na transação do objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="4c6ac-133">COM+ examina o contexto do chamador para determinar o status transacional do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="4c6ac-134">Se o chamador for transacional, o COM+ fluirá a transação para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="4c6ac-135">Todos os objetos que participam da mesma transação compartilham um identificador de transação comum, que é lido pelo COM+ do contexto do objeto.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="4c6ac-136">Cada objeto em uma transação é votos independentemente de outros objetos.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="4c6ac-137">COM+ conta os votos quando o objeto raiz é desativado.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="4c6ac-138">Você pode alternar o voto de transação de um objeto entre Commit e Abort até que o COM+ desative o objeto ou até que COM+ desative o objeto raiz e termine a transação.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="4c6ac-139">Somente a configuração do último voto conta.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-139">Only the last vote setting counts.</span></span> <span data-ttu-id="4c6ac-140">As interfaces [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) e [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) fornecem métodos e produzem resultados semelhantes de votação, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="4c6ac-141">Você pode usar qualquer interface para votar explicitamente em uma transação.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="4c6ac-142">Métodos de combinação de [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="4c6ac-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="4c6ac-143">Método equivalente de [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="4c6ac-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="4c6ac-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="4c6ac-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="4c6ac-146">**SetComplete**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="4c6ac-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="4c6ac-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="4c6ac-149">**EnableCommit**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="4c6ac-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="4c6ac-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="4c6ac-152">**SetAbort**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="4c6ac-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="4c6ac-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="4c6ac-155">**DisableCommit**</span><span class="sxs-lookup"><span data-stu-id="4c6ac-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="4c6ac-156">COM+ define o voto de um objeto para o equivalente de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , a menos que o componente seja explicitamente votado.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="4c6ac-157">A votação explicitamente pode reduzir a duração geral da transação e liberar bloqueios de recursos caros.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c6ac-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c6ac-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c6ac-159">Etapa 1: Criando um componente transacional</span><span class="sxs-lookup"><span data-stu-id="4c6ac-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="4c6ac-160">Etapa 3: reutilizando os componentes</span><span class="sxs-lookup"><span data-stu-id="4c6ac-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="4c6ac-161">Ativação de contexto</span><span class="sxs-lookup"><span data-stu-id="4c6ac-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="4c6ac-162">Gerenciando transações automáticas no COM+</span><span class="sxs-lookup"><span data-stu-id="4c6ac-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




