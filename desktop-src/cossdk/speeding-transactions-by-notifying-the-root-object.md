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
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="0ed3c-103">Acelerando as transações notificando o objeto raiz</span><span class="sxs-lookup"><span data-stu-id="0ed3c-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="0ed3c-104">Para usar transações automáticas com eficiência, cada componente transacional deve indicar que concluiu seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="0ed3c-105">Quando uma instância de objeto conclui sua tarefa com êxito, ela deve definir seus sinalizadores consistentes e concluídos como true chamando o método [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="0ed3c-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="0ed3c-106">Quando todos os objetos interiores da transação tiverem chamado **SetComplete**, a transação poderá ser encerrada desativando explicitamente o objeto raiz chamando seu método **SetComplete** .</span><span class="sxs-lookup"><span data-stu-id="0ed3c-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="0ed3c-107">Ao indicar explicitamente que um objeto raiz concluiu seu trabalho, você pode reduzir o tamanho da transação.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="0ed3c-108">Quando um método de objeto transacional falha, o objeto deve definir seu sinalizador consistente como false e seu sinalizador Done para true chamando o método [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) .</span><span class="sxs-lookup"><span data-stu-id="0ed3c-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="0ed3c-109">Ao chamar o método **SetAbort** , um objeto retorna o controle para seu chamador e garante que a transação seja eventualmente anulada.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="0ed3c-110">No entanto, a menos que o objeto que chama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) seja a raiz da transação, a transação continua a ser executada, embora nada possa salvá-la eventualmente anulando.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="0ed3c-111">Para acelerar o encerramento de uma transação com falha, você pode gerar um erro para alertar o objeto raiz para também chamar **SetAbort**.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="0ed3c-112">Para a conclusão, o objeto raiz deve enviar uma mensagem de erro para seu cliente.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="0ed3c-113">Embora existam muitas abordagens diferentes que você pode tomar para lidar com erros, sua abordagem deve coordenar claramente as comunicações entre objetos interiores e o objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="0ed3c-114">Os fragmentos de código Visual Basic a seguir mostram uma abordagem para o tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="0ed3c-115">No primeiro fragmento, um objeto interior chama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), gera um erro e gera uma mensagem de erro, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0ed3c-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="0ed3c-116">No segundo fragmento, o objeto raiz manipula o erro e passa a mensagem para seu cliente, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0ed3c-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0ed3c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ed3c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed3c-118">Gerenciando transações automáticas no COM+</span><span class="sxs-lookup"><span data-stu-id="0ed3c-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



