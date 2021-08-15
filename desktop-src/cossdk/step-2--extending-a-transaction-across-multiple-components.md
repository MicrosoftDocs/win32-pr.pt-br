---
description: 'Etapa 2: estendendo uma transação entre vários componentes'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Etapa 2: estendendo uma transação entre vários componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aa168eca7bfba29a4b00a6cd24b45d06c7610c76d47a4d6454e77295e57bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915799"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Etapa 2: estendendo uma transação entre componentes

## <a name="objectives"></a>Objetivos

Nesta etapa, você aprenderá sobre o seguinte:

-   Fluxo de transações
-   Como vários objetos votam em uma transação

## <a name="description"></a>Description

[etapa 1: a criação de um componente transacional](step-1--creating-a-transactional-component.md) mostra como escrever um componente transacional simples que atualiza informações de autor no banco de dados de Microsoft SQL Server Pubs. A etapa 2 mostra o que acontece quando uma transação é estendida entre vários componentes.

Ao manter o modelo de programação COM+, o `UpdateAuthorAddress` chama outro componente no decorrer de concluir seu trabalho. O segundo componente, `ValidateAuthorAddress` , valida o endereço do autor e retorna os resultados para seu chamador, `UpdateAuthorAddress` .

Ao contrário de seu chamador, `ValidateAuthorAddress` o não requer uma transação, mas ainda pode participar da transação do chamador. Nesta etapa, seu valor de atributo de transação é definido como **com suporte**, conforme mostrado na ilustração a seguir, que estende a transação existente para o novo objeto.

![Diagrama que mostra a extensão da transação existente para o novo objeto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

O valor de atributo **com suporte** estende (ou flui) uma transação existente somente quando o chamador é transacional. Quando `UpdateAuthorAddress` chamadas `ValidateAuthorAddress` , o com+ primeiro examina o contexto do chamador para ver se ele é transacional. Em seguida, o COM+ examina os atributos de serviço definidos em `ValidateAuthorAddress` e atribui o novo objeto ao mesmo identificador de transação atribuído ao objeto chamador. Para entender melhor esse processo, consulte [ativação de contexto](context-activation.md).

Como eles compartilham o mesmo identificador de transação, os dois objetos devem concluir o trabalho com êxito ou o COM+ anula a transação (desfazendo as alterações feitas no banco de dados pubs).

Todos os objetos que participam de uma transação votam para confirmar ou anular a transação. A votação ocorre explicitamente quando você inclui instruções de votação em seu código, conforme mostrado na seguinte extração do código de exemplo da etapa 1, que cria o `UpdateAuthorAddress` componente:


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



A votação também ocorre implicitamente, como é feito no `ValidateAuthorAddress` componente. A menos que o objeto declare de outra forma, o COM+ pressupõe que um objeto concluiu seu trabalho com êxito, mas que ele não está pronto para ser desativado. O COM+ faz a seguinte suposição:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Quando `ValidateAuthorAddress` retorna ao chamador, o com+ lê seu voto como uma confirmação. O COM+ não conta os votos até que ele desative o objeto raiz, que é o primeiro objeto na transação, nesse caso, o `UpdateAuthorAddress` objeto.

## <a name="sample-code"></a>Código de exemplo

O `ValidateAuthorAddress` componente faz uma verificação simples do endereço do autor. Como o `UpdateAuthorAddress` não votar explicitamente, o com+ usa as configurações de voto padrão.


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



## <a name="summary"></a>Resumo

-   Definir o atributo Transaction de um componente como **com suporte** pode resultar no novo objeto que está sendo criado na transação do objeto de chamada. COM+ examina o contexto do chamador para determinar o status transacional do novo objeto. Se o chamador for transacional, o COM+ fluirá a transação para o novo objeto.
-   Todos os objetos que participam da mesma transação compartilham um identificador de transação comum, que é lido pelo COM+ do contexto do objeto.
-   Cada objeto em uma transação é votos independentemente de outros objetos. COM+ conta os votos quando o objeto raiz é desativado.
-   Você pode alternar o voto de transação de um objeto entre Commit e Abort até que o COM+ desative o objeto ou até que COM+ desative o objeto raiz e termine a transação. Somente a configuração do último voto conta. As interfaces [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) e [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) fornecem métodos e produzem resultados semelhantes de votação, conforme mostrado na tabela a seguir. Você pode usar qualquer interface para votar explicitamente em uma transação. 

    | Métodos de combinação de [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | Método equivalente de [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ define o voto de um objeto para o equivalente de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , a menos que o componente seja explicitamente votado.
-   A votação explicitamente pode reduzir a duração geral da transação e liberar bloqueios de recursos caros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Etapa 1: Criando um componente transacional](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Etapa 3: reutilizando os componentes](step-3--reusing-components.md)
</dt> <dt>

[Ativação de contexto](context-activation.md)
</dt> <dt>

[Gerenciando transações automáticas no COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




