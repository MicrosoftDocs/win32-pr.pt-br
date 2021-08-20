---
description: Determinando se a segurança do Role-Based está habilitada
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Determinando se a segurança do Role-Based está habilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895c2f3c5e77d0f3629644b7d7638c1b818900773469d7f2a5ac110bde76692e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102232"
---
# <a name="determining-whether-role-based-security-is-enabled"></a>Determinando se a segurança do Role-Based está habilitada

Usando o método [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponível no objeto de contexto de chamada de segurança, você pode determinar se a segurança está habilitada para o objeto atual. Você deve chamar **IsSecurityEnabled** antes de usar ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para verificar a associação de função porque **IsCallerInRole** retornará true se a segurança não estiver habilitada.

os desenvolvedores do Microsoft Visual Basic chamam [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) para obter uma referência a um objeto [**SecurityCallContext**](securitycallcontext.md) e, em seguida, chamar [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), conforme mostrado no exemplo a seguir:


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ os desenvolvedores podem chamar [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obter um ponteiro para [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) e, em seguida, chamar **IsSecurityEnabled**. Segue um breve exemplo:


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



Embora a maneira preferida de chamar [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) seja usando o objeto de contexto de chamada de segurança, você também pode chamar **IsSecurityEnabled** por meio do contexto do objeto. (Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obter mais informações.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando informações de contexto de chamada de segurança](accessing-security-call-context-information.md)
</dt> <dt>

[Verificando a associação de função](checking-role-membership.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> </dl>

 

 
