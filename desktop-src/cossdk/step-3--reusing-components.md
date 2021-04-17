---
description: 'Etapa 3: reutilizando os componentes'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Etapa 3: reutilizando os componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568068"
---
# <a name="step-3-reusing-components"></a><span data-ttu-id="030ce-103">Etapa 3: reutilizando os componentes</span><span class="sxs-lookup"><span data-stu-id="030ce-103">Step 3: Reusing Components</span></span>

## <a name="objectives"></a><span data-ttu-id="030ce-104">Objetivos</span><span class="sxs-lookup"><span data-stu-id="030ce-104">Objectives</span></span>

<span data-ttu-id="030ce-105">Nesta etapa, você aprenderá sobre o seguinte:</span><span class="sxs-lookup"><span data-stu-id="030ce-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="030ce-106">Componentes reutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="030ce-106">Reusable components.</span></span>
-   <span data-ttu-id="030ce-107">Como planejar a reusabilidade.</span><span class="sxs-lookup"><span data-stu-id="030ce-107">How to plan for reusability.</span></span>

## <a name="description"></a><span data-ttu-id="030ce-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="030ce-108">Description</span></span>

<span data-ttu-id="030ce-109">Duas partes anteriores deste primo de serviços COM+, [etapa 1: Criando um componente transacional](step-1--creating-a-transactional-component.md) e [etapa 2: estendendo uma transação em vários componentes](step-2--extending-a-transaction-across-multiple-components.md) mostram como escrever um componente que chama um segundo componente para ajudar a concluir algum trabalho, atualizar informações de autor no banco de dados Microsoft SQL Server pubs; todo o trabalho é protegido por uma única transação.</span><span class="sxs-lookup"><span data-stu-id="030ce-109">Two previous parts of this COM+ services primer, [Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) and [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md) show how to write one component that calls a second component to assist in completing some work, updating author information in the Microsoft SQL Server Pubs database; all work is protected by a single transaction.</span></span> <span data-ttu-id="030ce-110">Os componentes de exemplo se concentraram no trabalho de atualizar os dados de um autor e verificar o endereço do autor e o processamento de transações fornecido pelo COM+, [ativação JIT](com--just-in-time-activation.md)e [proteção de simultaneidade](com--synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="030ce-110">The sample components focused on the work of updating an author's data and verifying the author's address, and COM+ provided transaction processing, [JIT activation](com--just-in-time-activation.md), and [concurrency protection](com--synchronization.md).</span></span>

<span data-ttu-id="030ce-111">Esta etapa demonstra como reutilizar os componentes criados nas etapas 1 e 2 e analisa o que isso significa para o design desses componentes.</span><span class="sxs-lookup"><span data-stu-id="030ce-111">This step demonstrates how to reuse the components created in steps 1 and 2 and looks at what this means to the design of those components.</span></span> <span data-ttu-id="030ce-112">Conforme mostrado na ilustração a seguir, isso significa criar um novo componente, `AddNewAuthor` , que adiciona novos autores ao banco de dados chamando `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="030ce-112">As shown in the following illustration, this means creating a new component, `AddNewAuthor`, that adds new authors to the database by calling `UpdateAuthorAddress`.</span></span>

![Diagrama que mostra o fluxo ao reutilizar componentes.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

<span data-ttu-id="030ce-114">Além de reutilizar a funcionalidade de componente existente, o `AddNewAuthor` chama outro novo componente chamado `ValidateAuthorName` .</span><span class="sxs-lookup"><span data-stu-id="030ce-114">In addition to reusing existing component functionality, `AddNewAuthor` calls another new component called `ValidateAuthorName`.</span></span> <span data-ttu-id="030ce-115">Como mostra a ilustração anterior, `ValidateAuthorName` é não transacional.</span><span class="sxs-lookup"><span data-stu-id="030ce-115">As the preceding illustration shows, `ValidateAuthorName` is non-transactional.</span></span> <span data-ttu-id="030ce-116">O valor do atributo Transaction para esse componente é deixado em sua configuração padrão (**sem suporte**) para excluir seu trabalho da transação.</span><span class="sxs-lookup"><span data-stu-id="030ce-116">The transaction attribute value for this component is left at its default setting (**Not Supported**) to exclude its work from the transaction.</span></span> <span data-ttu-id="030ce-117">Conforme mostrado no código de exemplo da etapa 3, o `ValidateAuthorName` executa consultas somente leitura no banco de dados e a falha dessa tarefa secundária não deve ter o potencial de anular a transação.</span><span class="sxs-lookup"><span data-stu-id="030ce-117">As shown in the step 3 sample code, `ValidateAuthorName` performs read-only queries on the database, and the failure of this minor task should not have the potential to abort the transaction.</span></span> <span data-ttu-id="030ce-118">No entanto, o valor do atributo Transaction do `AddNewAuthor` componente é definido como **Required**.</span><span class="sxs-lookup"><span data-stu-id="030ce-118">However, the transaction attribute value of the `AddNewAuthor` component is set to **Required**.</span></span>

<span data-ttu-id="030ce-119">`AddNewAuthor`Todos os `UpdateAuthorAddress` componentes, e são `ValidateAuthorAddress` votados na transação.</span><span class="sxs-lookup"><span data-stu-id="030ce-119">The `AddNewAuthor`, `UpdateAuthorAddress`, and `ValidateAuthorAddress` components all vote in the transaction.</span></span> <span data-ttu-id="030ce-120">Nessa transação, `AddNewAuthor` é o objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="030ce-120">In this transaction, `AddNewAuthor` is the root object.</span></span> <span data-ttu-id="030ce-121">O COM+ sempre torna o primeiro objeto criado na transação do objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="030ce-121">COM+ always makes the first object created in the transaction the root object.</span></span>

<span data-ttu-id="030ce-122">Neste exemplo, reutilizar o `UpdateAuthorAddress` componente é fácil – o com + fornece automaticamente os serviços esperados.</span><span class="sxs-lookup"><span data-stu-id="030ce-122">In this example, reusing the `UpdateAuthorAddress` component is easy—COM+ automatically delivers the expected services.</span></span> <span data-ttu-id="030ce-123">No entanto, os resultados seriam diferentes se o valor do atributo Transaction do `UpdateAuthorAddress` componente estivesse inicialmente definido como **requer New** , em vez de **Required**.</span><span class="sxs-lookup"><span data-stu-id="030ce-123">However, the results would be different if the transaction attribute value of the `UpdateAuthorAddress` component were initially set to **Requires New** instead of **Required**.</span></span> <span data-ttu-id="030ce-124">Na superfície, ambas as configurações são semelhantes; ambos garantem uma transação.</span><span class="sxs-lookup"><span data-stu-id="030ce-124">On the surface, both settings appear similar; both guarantee a transaction.</span></span> <span data-ttu-id="030ce-125">**Requer que New**, no entanto, sempre inicie uma nova transação, enquanto **necessário** inicia uma nova transação somente quando o chamador do objeto não é transacional.</span><span class="sxs-lookup"><span data-stu-id="030ce-125">**Requires New**, however, always starts a new transaction, while **Required** starts a new transaction only when the object's caller is non-transactional.</span></span> <span data-ttu-id="030ce-126">Você pode ver a partir desse quão importante ele foi configurado com `UpdateAuthorAddress` cautela e consideração.</span><span class="sxs-lookup"><span data-stu-id="030ce-126">You can see from this how important it was to configure `UpdateAuthorAddress` carefully and thoughtfully.</span></span> <span data-ttu-id="030ce-127">Caso contrário, o COM+ pode ter interpretado a solicitação de serviço de forma diferente, gerando duas transações não relacionadas, conforme mostrado na ilustração a seguir, em vez de uma.</span><span class="sxs-lookup"><span data-stu-id="030ce-127">Otherwise, COM+ might have interpreted the service request differently, generating two unrelated transactions, as shown in the following illustration, instead of one.</span></span>

![Diagrama que mostra o fluxo ao reutilizar componentes com "requer novo".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> <span data-ttu-id="030ce-129">Ao reutilizar componentes, verifique se os serviços estão configurados para dar suporte ao resultado desejado.</span><span class="sxs-lookup"><span data-stu-id="030ce-129">When you reuse components, make sure the services are configured to support your desired outcome.</span></span>

 

## <a name="sample-code"></a><span data-ttu-id="030ce-130">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="030ce-130">Sample code</span></span>

<span data-ttu-id="030ce-131">O componente AddNewAuthor executa adições em lote de novos autores, permitindo que o objeto permaneça ativo até que o cliente Libere sua referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="030ce-131">The AddNewAuthor component performs batch additions of new authors by allowing the object to remain active until the client releases its reference to the object.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



<span data-ttu-id="030ce-132">O `ValidateAuthorName` componente valida nomes de autor antes de `AddNewAuthor` Adicionar o nome ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="030ce-132">The `ValidateAuthorName` component validates author names before `AddNewAuthor` adds the name to the database.</span></span> <span data-ttu-id="030ce-133">Esse componente gera um erro de volta para seu chamador se algo inesperado ocorrer.</span><span class="sxs-lookup"><span data-stu-id="030ce-133">This component throws an error back to its caller if something unexpected happens.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a><span data-ttu-id="030ce-134">Resumo</span><span class="sxs-lookup"><span data-stu-id="030ce-134">Summary</span></span>

-   <span data-ttu-id="030ce-135">Há ocasiões em que você não quer que um componente Vote na transação.</span><span class="sxs-lookup"><span data-stu-id="030ce-135">There are times when you don't want a component to vote in the transaction.</span></span>
-   <span data-ttu-id="030ce-136">O COM+ não impõe a ativação JIT ou a proteção de simultaneidade em componentes não transacionais.</span><span class="sxs-lookup"><span data-stu-id="030ce-136">COM+ does not enforce JIT activation or concurrency protection on non-transactional components.</span></span> <span data-ttu-id="030ce-137">Você pode configurar esses serviços separadamente.</span><span class="sxs-lookup"><span data-stu-id="030ce-137">You may configure these services separately.</span></span>
-   <span data-ttu-id="030ce-138">A configuração de um componente de chamada afeta como o COM+ interpreta as solicitações de serviço do componente chamado.</span><span class="sxs-lookup"><span data-stu-id="030ce-138">A calling component's configuration affects how COM+ interprets the service requests of the called component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="030ce-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="030ce-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030ce-140">Etapa 1: Criando um componente transacional</span><span class="sxs-lookup"><span data-stu-id="030ce-140">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="030ce-141">Etapa 2: estendendo uma transação entre vários componentes</span><span class="sxs-lookup"><span data-stu-id="030ce-141">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="030ce-142">Configurando transações</span><span class="sxs-lookup"><span data-stu-id="030ce-142">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="030ce-143">Projetando para escalabilidade</span><span class="sxs-lookup"><span data-stu-id="030ce-143">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> </dl>

 

 



