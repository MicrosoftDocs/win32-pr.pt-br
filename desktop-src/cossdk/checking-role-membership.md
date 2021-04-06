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
# <a name="checking-role-membership"></a>Verificando a associação de função

Você pode chamar o método [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para determinar se o chamador direto de um objeto é membro de uma função específica. Essa funcionalidade é útil quando você deseja garantir que um determinado bloco de código não seja executado, a menos que o chamador seja membro de uma função específica.

Por exemplo, você pode usar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) para garantir que as transações em um valor especificado, como $1000, sejam executadas somente por membros de uma função de gerentes. Se o chamador não for um gerente e a transação estiver acima de $1000, a transação não será executada e uma mensagem de erro será exibida.

A maneira preferida de acessar o [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) é por meio do objeto de contexto de chamada de segurança, pois você pode usar a mesma referência ao objeto de contexto de chamada de segurança para obter as propriedades de segurança. No entanto, você também pode acessar o método **IsCallerInRole** do objeto **ObjectContext** . (Consulte [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) ou [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para obter mais informações.)

Se você estiver desenvolvendo componentes para um aplicativo Microsoft Visual Basic, chame a função [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) e, em seguida, use o contexto de chamada de segurança para chamar [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), conforme mostrado no exemplo a seguir:


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



Se você estiver desenvolvendo um aplicativo C ou C++, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar um ponteiro para a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) . Em seguida, você chama [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), conforme mostrado no exemplo a seguir:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando informações de contexto de chamada de segurança](accessing-security-call-context-information.md)
</dt> <dt>

[Determinando se a segurança do Role-Based está habilitada](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> </dl>

 

 
