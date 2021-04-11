---
description: Os retornos de chamada de componentes hospedados são o que tornam a hospedagem possível. No entanto, é possível que o componente que você está hospedando tenha ativado outro contexto de ativação que ele usa para acessar os plug-ins ou componentes próprios.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Usando retornos de chamada de componentes hospedados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090203"
---
# <a name="using-callbacks-from-hosted-components"></a>Usando retornos de chamada de componentes hospedados

Os retornos de chamada de componentes hospedados são o que tornam a hospedagem possível. No entanto, é possível que o componente que você está hospedando tenha ativado outro contexto de ativação que ele usa para acessar os plug-ins ou componentes próprios. Nesse caso, se o componente hospedado deixar um contexto de ativação na pilha que se refere a seu próprio objeto COM, o aplicativo de hospedagem poderá chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto que espera ser sua própria implementação e, em vez disso, receber o objeto do componente hospedado. Para evitar essa herança de contextos de ativação, um bom aplicativo de hospedagem deve ativar seu próprio contexto de ativação bem conhecido primeiro durante um retorno de chamada.

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

Isso garante que um contexto de ativação adequado seja definido antes de passar a solicitação para alguma implementação interna de **funct**. Sua própria implementação pode ter a implementação real embutida, mas o método anterior garante a interoperabilidade mais fácil criando apenas wrappers delegados. É recomendável usar um método semelhante ao expor retornos de chamada normais (não COM).

 

 
