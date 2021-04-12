---
description: 'Etapa 1: Criando um componente transacional'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Etapa 1: Criando um componente transacional'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104297835"
---
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="65636-103">Etapa 1: Criando um componente transacional</span><span class="sxs-lookup"><span data-stu-id="65636-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="65636-104">Objetivos</span><span class="sxs-lookup"><span data-stu-id="65636-104">Objectives</span></span>

<span data-ttu-id="65636-105">Nesta etapa, você aprenderá o seguinte:</span><span class="sxs-lookup"><span data-stu-id="65636-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="65636-106">Como escrever um componente transacional no Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="65636-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="65636-107">Quais são as configurações padrão dos serviços COM+</span><span class="sxs-lookup"><span data-stu-id="65636-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="65636-108">Como configurar serviços COM+</span><span class="sxs-lookup"><span data-stu-id="65636-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="65636-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="65636-109">Description</span></span>

<span data-ttu-id="65636-110">O componente UpdateAuthorAddress, o componente a ser criado nesta seção, atualiza o endereço de um autor existente no banco de dados pubs.</span><span class="sxs-lookup"><span data-stu-id="65636-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="65636-111">O banco de dados pubs é um banco de dados de exemplo fornecido com Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="65636-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="65636-112">Ele contém informações de publicação, como nomes de autor, endereços e títulos de livros.</span><span class="sxs-lookup"><span data-stu-id="65636-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="65636-113">Pubs é o armazenamento de dados que é usado em todo esse primo.</span><span class="sxs-lookup"><span data-stu-id="65636-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="65636-114">Como o UpdateAuthorAddress atualiza um armazenamento de dados, é aconselhável incluir o trabalho em uma transação, conforme mostrado na ilustração a seguir, de modo que, quando um cliente chama o componente, o COM+ inicia automaticamente uma transação e lista o banco de dados (Resource Manager) nessa transação.</span><span class="sxs-lookup"><span data-stu-id="65636-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="65636-115">(Para obter informações detalhadas sobre transações em COM+, consulte [Transações com+](com--transactions.md).)</span><span class="sxs-lookup"><span data-stu-id="65636-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![Diagrama que mostra uma transação COM+ com UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="65636-117">Para tornar o UpdateAuthorAddress um componente transacional, as etapas a seguir são necessárias:</span><span class="sxs-lookup"><span data-stu-id="65636-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="65636-118">O componente deve ser gravado.</span><span class="sxs-lookup"><span data-stu-id="65636-118">The component must be written.</span></span> <span data-ttu-id="65636-119">Para proteção extra, uma sub-rotina é adicionada, verificando se o COM+ criou o objeto em uma transação.</span><span class="sxs-lookup"><span data-stu-id="65636-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="65636-120">Além disso, o tratamento de erros básico é incluído no componente para simplificar a recuperação de erros.</span><span class="sxs-lookup"><span data-stu-id="65636-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="65636-121">A verificação de transações e o tratamento de erros aumentam a confiabilidade do componente.</span><span class="sxs-lookup"><span data-stu-id="65636-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="65636-122">(Consulte a etapa 1 código de exemplo para obter uma lista completa do componente UpdateAuthorAddress.)</span><span class="sxs-lookup"><span data-stu-id="65636-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="65636-123">Depois de adicionar o componente a um aplicativo COM+ e instalar o aplicativo, o atributo Transaction deve ser definido como **Required**, o que garante que o com+ crie cada objeto UpdateAuthorAddress em uma transação.</span><span class="sxs-lookup"><span data-stu-id="65636-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="65636-124">Para obter instruções sobre como definir o atributo de transação para um componente, consulte [Configurando o atributo Transaction](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="65636-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="65636-125">Definir o atributo Transaction em um componente define como o COM+ cria cada objeto em relação às transações.</span><span class="sxs-lookup"><span data-stu-id="65636-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="65636-126">Os valores de atributo de transação são **ignorados**, **não têm suporte**, **têm suporte**, são **necessários** e **exigem novos**.</span><span class="sxs-lookup"><span data-stu-id="65636-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="65636-127">O valor **necessário** não é um dos valores de atributo padrão de um componente.</span><span class="sxs-lookup"><span data-stu-id="65636-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="65636-128">O COM+ associa o serviço de transação com ativação e simultaneidade JIT (just-in-time).</span><span class="sxs-lookup"><span data-stu-id="65636-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="65636-129">Quando você declara um componente para ser transacional, o COM+ também impõe a ativação JIT e a proteção de simultaneidade (sincronização).</span><span class="sxs-lookup"><span data-stu-id="65636-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="65636-130">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="65636-130">Sample code</span></span>

<span data-ttu-id="65636-131">O componente UpdateAuthorAddress abre uma conexão com o banco de dados pubs, permitindo que o usuário modifique o nome, o endereço ou o status do contrato de um autor.</span><span class="sxs-lookup"><span data-stu-id="65636-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="65636-132">Ele também chama um segundo componente, que é discutido na [etapa 2: estendendo uma transação entre vários componentes](step-2--extending-a-transaction-across-multiple-components.md).</span><span class="sxs-lookup"><span data-stu-id="65636-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="65636-133">Para usar o código a seguir em um projeto do Microsoft Visual Basic, abra um novo projeto de ActiveX.dll e adicione referências à biblioteca do Microsoft ActiveX Data Objects e à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="65636-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="65636-134">O código de exemplo neste primer é para fins de ilustração e pode não ser o mais eficiente para preparo e produção reais.</span><span class="sxs-lookup"><span data-stu-id="65636-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a><span data-ttu-id="65636-135">Resumo</span><span class="sxs-lookup"><span data-stu-id="65636-135">Summary</span></span>

-   <span data-ttu-id="65636-136">O COM+ atribui valores de atributo padrão.</span><span class="sxs-lookup"><span data-stu-id="65636-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="65636-137">Você pode reconfigurar a maioria dos atributos de serviço.</span><span class="sxs-lookup"><span data-stu-id="65636-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="65636-138">Definir o atributo Transaction de um componente como **necessário** garante que o com+ deve criar cada instância desse componente em uma transação, mas não necessariamente inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="65636-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="65636-139">Verificar a presença de uma transação confirma que o valor do atributo de transação do componente não foi redefinido inadvertidamente para um valor não transacional, como **ignorar** ou **não suportado**.</span><span class="sxs-lookup"><span data-stu-id="65636-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="65636-140">Lidar com erros torna seu componente mais confiável e mais fácil de solucionar.</span><span class="sxs-lookup"><span data-stu-id="65636-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="65636-141">O COM+ impõe a [ativação JIT](com--just-in-time-activation.md) e os serviços de [proteção de simultaneidade](com--synchronization.md) para componentes transacionais.</span><span class="sxs-lookup"><span data-stu-id="65636-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="65636-142">Ao fechar a conexão de banco de dados quando você terminar, ele permitirá que outro componente na mesma transação reutilize a conexão do pool de conexões.</span><span class="sxs-lookup"><span data-stu-id="65636-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="65636-143">(O pool de conexões não deve ser confundido com o [pool de objetos](com--object-pooling.md).)</span><span class="sxs-lookup"><span data-stu-id="65636-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="65636-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65636-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65636-145">Etapa 2: estendendo uma transação entre vários componentes</span><span class="sxs-lookup"><span data-stu-id="65636-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="65636-146">Etapa 3: reutilizando os componentes</span><span class="sxs-lookup"><span data-stu-id="65636-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="65636-147">Ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="65636-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="65636-148">Sincronização COM+</span><span class="sxs-lookup"><span data-stu-id="65636-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="65636-149">Configurando transações</span><span class="sxs-lookup"><span data-stu-id="65636-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="65636-150">Criando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="65636-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="65636-151">Configurando o atributo de transação</span><span class="sxs-lookup"><span data-stu-id="65636-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



