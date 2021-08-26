---
description: Retornos de chamada de componentes hospedados são o que possibilitam a hospedagem. No entanto, é possível que o componente que você está hospedando tenha ativado outro contexto de ativação que ele usa para acessar plug-ins ou componentes próprios.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Usando retornos de chamada de componentes hospedados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb13e61b83ba52f0f8dd5265b11585e8366c0e8558d45c5738f179d43df2eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884596"
---
# <a name="using-callbacks-from-hosted-components"></a>Usando retornos de chamada de componentes hospedados

Retornos de chamada de componentes hospedados são o que possibilitam a hospedagem. No entanto, é possível que o componente que você está hospedando tenha ativado outro contexto de ativação que ele usa para acessar plug-ins ou componentes próprios. Nesse caso, se o componente hospedado deixar um contexto de ativação na pilha que se refere ao seu próprio objeto COM, o aplicativo de hospedagem poderá chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto que ele espera ser sua própria implementação e, em vez disso, receber o objeto do componente hospedado. Para evitar essa herança de contextos de ativação, um bom aplicativo de hospedagem deve ativar seu próprio contexto de ativação conhecido primeiro durante um retorno de chamada.

Considere o exemplo a seguir que protege o código do aplicativo de hospedagem:

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

Isso garante que um contexto de ativação adequado seja definido antes de passar a solicitação para alguma implementação interna do **Funct.** Sua própria implementação pode ter a implementação real em linha, mas o método anterior garante uma interoperabilidade mais fácil apenas criando wrappers delegados. É recomendável usar um método semelhante ao expor retornos de chamada normais (não COM).

 

 
