---
description: 'Etapa 1: Criando um componente transacional'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Etapa 1: Criando um componente transacional'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f5c87fb5c5f615ee04a3233f1a563d5ae5230e4dd18908c78e94092ff0f5c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305401"
---
# <a name="step-1-creating-a-transactional-component"></a>Etapa 1: Criando um componente transacional

## <a name="objectives"></a>Objetivos

Nesta etapa, você aprenderá o seguinte:

-   Como escrever um componente transacional no Microsoft Visual Basic
-   Quais são as configurações padrão dos serviços COM+
-   Como configurar serviços COM+

## <a name="description"></a>Descrição

O componente UpdateAuthorAddress, o componente a ser criado nesta seção, atualiza o endereço de um autor existente no banco de dados pubs. O banco de dados pubs é um banco de dados de exemplo fornecido com Microsoft SQL Server. Ele contém informações de publicação, como nomes de autor, endereços e títulos de livros.

> [!Note]  
> Pubs é o armazenamento de dados que é usado em todo esse primo.

 

Como o UpdateAuthorAddress atualiza um armazenamento de dados, é aconselhável incluir o trabalho em uma transação, conforme mostrado na ilustração a seguir, de modo que, quando um cliente chama o componente, o COM+ inicia automaticamente uma transação e lista o banco de dados (Resource Manager) nessa transação. (Para obter informações detalhadas sobre transações em COM+, consulte [Transações com+](com--transactions.md).)

![Diagrama que mostra uma transação COM+ com UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Para tornar o UpdateAuthorAddress um componente transacional, as etapas a seguir são necessárias:

1.  O componente deve ser gravado. Para proteção extra, uma sub-rotina é adicionada, verificando se o COM+ criou o objeto em uma transação. Além disso, o tratamento de erros básico é incluído no componente para simplificar a recuperação de erros. A verificação de transações e o tratamento de erros aumentam a confiabilidade do componente. (Consulte a etapa 1 código de exemplo para obter uma lista completa do componente UpdateAuthorAddress.)
2.  Depois de adicionar o componente a um aplicativo COM+ e instalar o aplicativo, o atributo Transaction deve ser definido como **Required**, o que garante que o com+ crie cada objeto UpdateAuthorAddress em uma transação. Para obter instruções sobre como definir o atributo de transação para um componente, consulte [Configurando o atributo Transaction](setting-the-transaction-attribute.md).
    > [!Note]  
    > Definir o atributo Transaction em um componente define como o COM+ cria cada objeto em relação às transações. Os valores de atributo de transação são **ignorados**, **não têm suporte**, **têm suporte**, são **necessários** e **exigem novos**. O valor **necessário** não é um dos valores de atributo padrão de um componente.

     

O COM+ associa o serviço de transação com ativação e simultaneidade JIT (just-in-time). Quando você declara um componente para ser transacional, o COM+ também impõe a ativação JIT e a proteção de simultaneidade (sincronização).

## <a name="sample-code"></a>Código de exemplo

O componente UpdateAuthorAddress abre uma conexão com o banco de dados pubs, permitindo que o usuário modifique o nome, o endereço ou o status do contrato de um autor. Ele também chama um segundo componente, que é discutido na [etapa 2: estendendo uma transação entre vários componentes](step-2--extending-a-transaction-across-multiple-components.md).

para usar o código a seguir em um projeto do microsoft Visual Basic, abra um novo projeto de ActiveX.dll e adicione referências à biblioteca do microsoft ActiveX Data Objects e à biblioteca de tipos de serviços COM+.

> [!Note]  
> O código de exemplo neste primer é para fins de ilustração e pode não ser o mais eficiente para preparo e produção reais.

 


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



## <a name="summary"></a>Resumo

-   O COM+ atribui valores de atributo padrão. Você pode reconfigurar a maioria dos atributos de serviço.
-   Definir o atributo Transaction de um componente como **necessário** garante que o com+ deve criar cada instância desse componente em uma transação, mas não necessariamente inicia uma nova transação.
-   Verificar a presença de uma transação confirma que o valor do atributo de transação do componente não foi redefinido inadvertidamente para um valor não transacional, como **ignorar** ou **não suportado**.
-   Lidar com erros torna seu componente mais confiável e mais fácil de solucionar.
-   O COM+ impõe a [ativação JIT](com--just-in-time-activation.md) e os serviços de [proteção de simultaneidade](com--synchronization.md) para componentes transacionais.
-   Ao fechar a conexão de banco de dados quando você terminar, ele permitirá que outro componente na mesma transação reutilize a conexão do pool de conexões. (O pool de conexões não deve ser confundido com o [pool de objetos](com--object-pooling.md).)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Etapa 2: estendendo uma transação entre vários componentes](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Etapa 3: reutilizando os componentes](step-3--reusing-components.md)
</dt> <dt>

[Ativação Just-in-time COM+](com--just-in-time-activation.md)
</dt> <dt>

[Sincronização COM+](com--synchronization.md)
</dt> <dt>

[Configurando transações](configuring-transactions.md)
</dt> <dt>

[Criando aplicativos COM+](creating-com--applications.md)
</dt> <dt>

[Configurando o atributo de transação](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



