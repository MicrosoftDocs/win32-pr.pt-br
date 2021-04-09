---
description: Determinando se a segurança do Role-Based está habilitada
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Determinando se a segurança do Role-Based está habilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089572"
---
# <a name="determining-whether-role-based-security-is-enabled"></a><span data-ttu-id="c920e-103">Determinando se a segurança do Role-Based está habilitada</span><span class="sxs-lookup"><span data-stu-id="c920e-103">Determining Whether Role-Based Security Is Enabled</span></span>

<span data-ttu-id="c920e-104">Usando o método [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponível no objeto de contexto de chamada de segurança, você pode determinar se a segurança está habilitada para o objeto atual.</span><span class="sxs-lookup"><span data-stu-id="c920e-104">By using the [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) method available from the security call context object, you can determine whether security is enabled for the current object.</span></span> <span data-ttu-id="c920e-105">Você deve chamar **IsSecurityEnabled** antes de usar ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para verificar a associação de função porque **IsCallerInRole** retornará true se a segurança não estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="c920e-105">You should call **IsSecurityEnabled** before you use ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to check role membership because **IsCallerInRole** returns True if security is not enabled.</span></span>

<span data-ttu-id="c920e-106">Os desenvolvedores do Microsoft Visual Basic chamam [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) para obter uma referência a um objeto [**SecurityCallContext**](securitycallcontext.md) e, em seguida, chamar [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="c920e-106">Microsoft Visual Basic developers call [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) to obtain a reference to a [**SecurityCallContext**](securitycallcontext.md) object and then call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), as shown in the following example:</span></span>


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



<span data-ttu-id="c920e-107">Microsoft Visual C++ os desenvolvedores podem chamar [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obter um ponteiro para [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) e, em seguida, chamar **IsSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="c920e-107">Microsoft Visual C++ developers can call [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) and then calling **IsSecurityEnabled**.</span></span> <span data-ttu-id="c920e-108">Segue um breve exemplo:</span><span class="sxs-lookup"><span data-stu-id="c920e-108">A brief example follows:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



<span data-ttu-id="c920e-109">Embora a maneira preferida de chamar [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) seja usando o objeto de contexto de chamada de segurança, você também pode chamar **IsSecurityEnabled** por meio do contexto do objeto.</span><span class="sxs-lookup"><span data-stu-id="c920e-109">Although the preferred way to call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) is by using the security call context object, you can also call **IsSecurityEnabled** through the object context.</span></span> <span data-ttu-id="c920e-110">(Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="c920e-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c920e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c920e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c920e-112">Acessando informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="c920e-112">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="c920e-113">Verificando a associação de função</span><span class="sxs-lookup"><span data-stu-id="c920e-113">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="c920e-114">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="c920e-114">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
