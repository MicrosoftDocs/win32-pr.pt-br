---
description: Como o COM+ modifica valores de retorno
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Como o COM+ modifica valores de retorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089313"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="c286e-103">Como o COM+ modifica valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c286e-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="c286e-104">COM+ nunca altera o valor de retorno de um **HRESULT** que indica falha, como e \_ inesperado ou \_ falha.</span><span class="sxs-lookup"><span data-stu-id="c286e-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="c286e-105">No entanto, quando um objeto que usa a funcionalidade COM+ retorna um valor **HRESULT** que indica êxito (como s \_ OK, s \_ false ou NOERROR), o com+ às vezes converte o **HRESULT** em um código de erro com+ antes que ele retorne ao chamador.</span><span class="sxs-lookup"><span data-stu-id="c286e-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="c286e-106">Por exemplo, quando um aplicativo retorna S \_ OK após chamar [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), se o objeto for a raiz de uma transação que não é confirmada, o **HRESULT** será convertido em Context \_ E \_ abortado.</span><span class="sxs-lookup"><span data-stu-id="c286e-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="c286e-107">Quando o COM+ converte um valor **HRESULT** , ele limpa todos os parâmetros de saída do método.</span><span class="sxs-lookup"><span data-stu-id="c286e-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="c286e-108">As referências retornadas são liberadas e os valores dos ponteiros de objeto retornados são definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c286e-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c286e-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c286e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c286e-110">Política de FailFast e isolamento de falhas</span><span class="sxs-lookup"><span data-stu-id="c286e-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="c286e-111">Localizando a origem de um erro</span><span class="sxs-lookup"><span data-stu-id="c286e-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="c286e-112">Interpretando códigos de erro</span><span class="sxs-lookup"><span data-stu-id="c286e-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="c286e-113">Estratégias para lidar com erros no COM+</span><span class="sxs-lookup"><span data-stu-id="c286e-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="c286e-114">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="c286e-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



