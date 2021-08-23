---
description: 'Etapa 3: Reutilizando componentes'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Etapa 3: Reutilizando componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf500746e7c9052a421691299903437e129108405b49c7753a841e8ca505518
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895797"
---
# <a name="step-3-reusing-components"></a>Etapa 3: Reutilizando componentes

## <a name="objectives"></a>Objetivos

Nesta etapa, você aprenderá sobre o seguinte:

-   Componentes reutilizáveis.
-   Como planejar a reutilização.

## <a name="description"></a>Descrição

Duas partes anteriores deste primer de serviços COM+, Etapa [1:](step-1--creating-a-transactional-component.md) Criando um componente transacional e Etapa [2:](step-2--extending-a-transaction-across-multiple-components.md) Estender uma transação entre vários componentes mostram como escrever um componente que chama um segundo componente para ajudar a concluir algum trabalho, atualizando informações de autor no banco de dados do Microsoft SQL Server Pubs; todo o trabalho é protegido por uma única transação. Os componentes de exemplo se concentraram no trabalho de atualizar os dados de um autor e verificar o endereço do autor e o processamento de transação fornecido pelo COM+, a ativação [JIT](com--just-in-time-activation.md)e a proteção de [simultância.](com--synchronization.md)

Esta etapa demonstra como reutilizar os componentes criados nas etapas 1 e 2 e analisa o que isso significa para o design desses componentes. Conforme mostrado na ilustração a seguir, isso significa criar um novo componente, , que adiciona novos autores ao banco de `AddNewAuthor` dados chamando `UpdateAuthorAddress` .

![Diagrama que mostra o fluxo ao reutilar componentes.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

Além de reutilar a funcionalidade de componente existente, `AddNewAuthor` chama outro novo componente chamado `ValidateAuthorName` . Como mostra a ilustração anterior, `ValidateAuthorName` é não transacional. O valor do atributo de transação para esse componente é deixado em sua configuração padrão (**Sem** Suporte ) para excluir seu trabalho da transação. Conforme mostrado no código de exemplo da etapa 3, o executa consultas somente leitura no banco de dados e a falha dessa tarefa secundária não deve ter o potencial de anular a `ValidateAuthorName` transação. No entanto, o valor do atributo de transação `AddNewAuthor` do componente é definido como **Obrigatório.**

Todos `AddNewAuthor` os `UpdateAuthorAddress` componentes , e `ValidateAuthorAddress` votam na transação. Nessa transação, `AddNewAuthor` é o objeto raiz. O COM+ sempre torna o primeiro objeto criado na transação o objeto raiz.

Neste exemplo, a reutilação do `UpdateAuthorAddress` componente é fácil— o COM+ fornece automaticamente os serviços esperados. No entanto, os resultados seriam diferentes se o valor do atributo de transação do componente fosse inicialmente `UpdateAuthorAddress` definido como Requires **New** em vez **de Required**. Na superfície, as duas configurações são semelhantes; ambos garantem uma transação. **Requer New**, no entanto, sempre  inicia uma nova transação, enquanto Obrigatório inicia uma nova transação somente quando o chamador do objeto é não transacional. Você pode ver com isso o quão importante era configurar `UpdateAuthorAddress` com cuidado e atenção. Caso contrário, COM+ pode ter interpretado a solicitação de serviço de forma diferente, gerando duas transações não relacionadas, conforme mostrado na ilustração a seguir, em vez de uma.

![Diagrama que mostra o fluxo ao reutilar componentes com "Requer Novo".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Ao reutilizar componentes, certifique-se de que os serviços estão configurados para dar suporte ao resultado desejado.

 

## <a name="sample-code"></a>Código de exemplo

O componente AddNewAuthor executa adições em lote de novos autores, permitindo que o objeto permaneça ativo até que o cliente libere sua referência ao objeto .


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



O `ValidateAuthorName` componente valida os nomes de autor antes de adiciona o nome ao banco de `AddNewAuthor` dados. Esse componente lançará um erro de volta para seu chamador se algo inesperado acontecer.


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



## <a name="summary"></a>Resumo

-   Há ocasiões em que você não deseja que um componente vote na transação.
-   O COM+ não impõe a ativação JIT nem a proteção de simultânea em componentes não transacionais. Você pode configurar esses serviços separadamente.
-   A configuração de um componente de chamada afeta como o COM+ interpreta as solicitações de serviço do componente chamado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Etapa 1: Criando um componente transacional](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Etapa 2: Estendendo uma transação entre vários componentes](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Configurando transações](configuring-transactions.md)
</dt> <dt>

[Projetando para escalabilidade](designing-for-scalability.md)
</dt> </dl>

 

 



