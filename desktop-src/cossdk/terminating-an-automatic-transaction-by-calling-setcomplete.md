---
description: Finalizando uma transação automática chamando SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Finalizando uma transação automática chamando SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d84d18b45309d750864d514728b8e23a3326e5edeba0bf144105bcbaa4797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499656"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Finalizando uma transação automática chamando SetComplete

Para usar transações automáticas com eficiência, cada componente transacional deve indicar que concluiu seu trabalho. Quando uma instância de objeto conclui sua tarefa com êxito, ela deve definir seus sinalizadores consistentes e concluídos como true chamando o método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , que é exposto por meio da interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) e do objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

A maneira mais eficiente de concluir uma transação automática é desativar explicitamente o objeto raiz usando o método [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Ao indicar explicitamente que um objeto raiz concluiu seu trabalho, você pode reduzir o tamanho da transação.

o exemplo a seguir Visual Basic mostra como indicar que um objeto transacional concluiu seu trabalho com êxito:


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sinalizadores consistentes e concluídos](consistent-and-done-flags.md)
</dt> <dt>

[Gerenciando transações automáticas no COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



