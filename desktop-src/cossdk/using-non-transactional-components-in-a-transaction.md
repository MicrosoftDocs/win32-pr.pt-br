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
# <a name="using-non-transactional-components-in-a-transaction"></a>Usando componentes não transacionais em uma transação

Geralmente, é útil colocar componentes não transacionais em uma transação para aproveitar as [Propriedades Acid](acid-properties.md) de transações. Por exemplo, se você tiver componentes herdados não transacionais que você usa para atualizar senhas em uma rede, poderá colocá-los em uma transação para garantir que as atualizações de senha sejam consistentes na rede.

O *objeto de contexto de transação* é um objeto genérico que permite que clientes não transacionais combinem o trabalho de vários objetos com em uma única transação, sem exigir que você desenvolva um novo componente especificamente para essa finalidade. Ao contrário de uma transação automática, o objeto de contexto de transação exige que seu cliente confirme ou anule explicitamente a transação.

Por padrão, o valor do atributo Transaction do objeto de contexto de transação é definido como Required. O COM+ anulará a transação se o cliente liberar o objeto de contexto de transação sem emitir explicitamente uma chamada Commit ou Abort.

O exemplo a seguir Visual Basic mostra como um cliente não transacional pode compor o trabalho feito por mais de um objeto em uma única transação:


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



## <a name="limitations-of-the-transaction-context-object"></a>Limitações do objeto de contexto de transação

A seguir estão algumas limitações importantes do objeto de contexto de transação:

-   Ao usar um objeto de contexto de transação, a lógica do aplicativo que combina o trabalho de vários objetos em uma única transação é vinculada a uma implementação de cliente não transacional específica e algumas vantagens de usar componentes COM são perdidas. Essas vantagens perdidas incluem o seguinte:
    -   Capacidade de reutilizar a lógica do aplicativo como parte de uma transação ainda maior
    -   Imposição de segurança declarativa
    -   Flexibilidade para executar a lógica remotamente do cliente
-   O objeto de contexto de transação é executado em processo com o cliente não transacional, o que significa que o COM+ deve estar disponível no computador cliente não transacional. Isso pode não ser um problema, por exemplo, quando o objeto de contexto de transação é usado em uma página de Active Server páginas (ASP) que está sendo executada no mesmo servidor que o COM+.
-   Você não obtém um contexto para o cliente não transacional quando cria um objeto de contexto de transação. O trabalho transacional só pode ser feito indiretamente, por meio de objetos COM criados com o uso do objeto de contexto de transação. Em particular, o cliente não transacional não pode usar dispensadores de recursos COM+ (como ODBC) e ter o trabalho incluído na transação. Por exemplo, os desenvolvedores podem estar familiarizados com a seguinte sintaxe para fazer trabalhos transacionais em sistemas de banco de dados relacionais:

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    Usar o objeto de contexto de transação de forma semelhante não produz o resultado desejado:

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    A chamada para DoWork neste exemplo não está inscrito em uma transação. Em vez disso, você deve criar um componente COM que chama DoWork, criar uma instância de objeto desse componente usando o objeto de contexto de transação e, em seguida, chamar esse objeto do cliente não transacional para que o trabalho faça parte da transação controlada pelo cliente.

 

 



