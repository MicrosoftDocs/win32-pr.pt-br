---
description: Verificando a associação de função
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Verificando a associação de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646442"
---
# <a name="checking-role-membership"></a><span data-ttu-id="02ea5-103">Verificando a associação de função</span><span class="sxs-lookup"><span data-stu-id="02ea5-103">Checking Role Membership</span></span>

<span data-ttu-id="02ea5-104">Você pode chamar o método [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para determinar se o chamador direto de um objeto é membro de uma função específica.</span><span class="sxs-lookup"><span data-stu-id="02ea5-104">You can call the [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) method to determine whether an object's direct caller is a member of a particular role.</span></span> <span data-ttu-id="02ea5-105">Essa funcionalidade é útil quando você deseja garantir que um determinado bloco de código não seja executado, a menos que o chamador seja membro de uma função específica.</span><span class="sxs-lookup"><span data-stu-id="02ea5-105">This functionality is useful when you want to ensure that a certain block of code is not executed unless the caller is a member of a particular role.</span></span>

<span data-ttu-id="02ea5-106">Por exemplo, você pode usar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para garantir que as transações em um valor especificado, como $1000, sejam executadas somente por membros de uma função de gerentes.</span><span class="sxs-lookup"><span data-stu-id="02ea5-106">For example, you could use [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to ensure that transactions over a specified amount, such as $1000, are performed only by members of a Managers role.</span></span> <span data-ttu-id="02ea5-107">Se o chamador não for um gerente e a transação estiver acima de $1000, a transação não será executada e uma mensagem de erro será exibida.</span><span class="sxs-lookup"><span data-stu-id="02ea5-107">If the caller is not a Manager and the transaction is over $1000, the transaction is not performed and an error message is displayed.</span></span>

<span data-ttu-id="02ea5-108">A maneira preferida de acessar o [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) é por meio do objeto de contexto de chamada de segurança, pois você pode usar a mesma referência ao objeto de contexto de chamada de segurança para obter as propriedades de segurança.</span><span class="sxs-lookup"><span data-stu-id="02ea5-108">The preferred way to access [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) is through the security call context object because you can use the same reference to the security call context object to obtain security properties.</span></span> <span data-ttu-id="02ea5-109">No entanto, você também pode acessar o método **IsCallerInRole** do objeto **ObjectContext** .</span><span class="sxs-lookup"><span data-stu-id="02ea5-109">However, you can also access the **IsCallerInRole** method from the **ObjectContext** object.</span></span> <span data-ttu-id="02ea5-110">(Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="02ea5-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

<span data-ttu-id="02ea5-111">Se você estiver desenvolvendo componentes para um aplicativo Microsoft Visual Basic, chame a função [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) e, em seguida, use o contexto de chamada de segurança para chamar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="02ea5-111">If you are developing components for a Microsoft Visual Basic application, you call the [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) function and then use the security call context to call [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



<span data-ttu-id="02ea5-112">Se você estiver desenvolvendo um aplicativo C ou C++, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar um ponteiro para a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) .</span><span class="sxs-lookup"><span data-stu-id="02ea5-112">If you are developing a C or C++ application, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to retrieve a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface.</span></span> <span data-ttu-id="02ea5-113">Em seguida, você chama [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="02ea5-113">Then you call [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="02ea5-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02ea5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ea5-115">Acessando informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="02ea5-115">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="02ea5-116">Determinando se a segurança do Role-Based está habilitada</span><span class="sxs-lookup"><span data-stu-id="02ea5-116">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="02ea5-117">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="02ea5-117">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
