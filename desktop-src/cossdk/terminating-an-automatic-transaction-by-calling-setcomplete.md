---
description: Finalizando uma transação automática chamando SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Finalizando uma transação automática chamando SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757453"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="1b6b7-103">Finalizando uma transação automática chamando SetComplete</span><span class="sxs-lookup"><span data-stu-id="1b6b7-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="1b6b7-104">Para usar transações automáticas com eficiência, cada componente transacional deve indicar que concluiu seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b6b7-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="1b6b7-105">Quando uma instância de objeto conclui sua tarefa com êxito, ela deve definir seus sinalizadores consistentes e concluídos como true chamando o método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , que é exposto por meio da interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) e do objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .</span><span class="sxs-lookup"><span data-stu-id="1b6b7-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="1b6b7-106">A maneira mais eficiente de concluir uma transação automática é desativar explicitamente o objeto raiz usando o método [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="1b6b7-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="1b6b7-107">Ao indicar explicitamente que um objeto raiz concluiu seu trabalho, você pode reduzir o tamanho da transação.</span><span class="sxs-lookup"><span data-stu-id="1b6b7-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="1b6b7-108">O exemplo a seguir Visual Basic mostra como indicar que um objeto transacional concluiu seu trabalho com êxito:</span><span class="sxs-lookup"><span data-stu-id="1b6b7-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1b6b7-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b6b7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b6b7-110">Sinalizadores consistentes e concluídos</span><span class="sxs-lookup"><span data-stu-id="1b6b7-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="1b6b7-111">Gerenciando transações automáticas no COM+</span><span class="sxs-lookup"><span data-stu-id="1b6b7-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



