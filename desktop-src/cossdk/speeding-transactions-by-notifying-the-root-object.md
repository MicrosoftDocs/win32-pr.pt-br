---
description: Acelerando as transações notificando o objeto raiz
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Acelerando as transações notificando o objeto raiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163994"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Acelerando as transações notificando o objeto raiz

Para usar transações automáticas com eficiência, cada componente transacional deve indicar que concluiu seu trabalho. Quando uma instância de objeto conclui sua tarefa com êxito, ela deve definir seus sinalizadores consistentes e concluídos como true chamando o método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Quando todos os objetos interiores da transação tiverem chamado **SetComplete**, a transação poderá ser encerrada desativando explicitamente o objeto raiz chamando seu método **SetComplete** . Ao indicar explicitamente que um objeto raiz concluiu seu trabalho, você pode reduzir o tamanho da transação.

Quando um método de objeto transacional falha, o objeto deve definir seu sinalizador consistente como false e seu sinalizador Done para true chamando o método [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) . Ao chamar o método **SetAbort** , um objeto retorna o controle para seu chamador e garante que a transação seja eventualmente anulada.

No entanto, a menos que o objeto que chama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) seja a raiz da transação, a transação continua a ser executada, embora nada possa salvá-la eventualmente anulando. Para acelerar o encerramento de uma transação com falha, você pode gerar um erro para alertar o objeto raiz para também chamar **SetAbort**. Para a conclusão, o objeto raiz deve enviar uma mensagem de erro para seu cliente.

Embora existam muitas abordagens diferentes que você pode tomar para lidar com erros, sua abordagem deve coordenar claramente as comunicações entre objetos interiores e o objeto raiz.

Os fragmentos de código Visual Basic a seguir mostram uma abordagem para o tratamento de erros. No primeiro fragmento, um objeto interior chama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), gera um erro e gera uma mensagem de erro, da seguinte maneira:

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

No segundo fragmento, o objeto raiz manipula o erro e passa a mensagem para seu cliente, da seguinte maneira:

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando transações automáticas no COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



