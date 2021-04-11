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
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="c493e-104">Usando retornos de chamada de componentes hospedados</span><span class="sxs-lookup"><span data-stu-id="c493e-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="c493e-105">Os retornos de chamada de componentes hospedados são o que tornam a hospedagem possível.</span><span class="sxs-lookup"><span data-stu-id="c493e-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="c493e-106">No entanto, é possível que o componente que você está hospedando tenha ativado outro contexto de ativação que ele usa para acessar os plug-ins ou componentes próprios.</span><span class="sxs-lookup"><span data-stu-id="c493e-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="c493e-107">Nesse caso, se o componente hospedado deixar um contexto de ativação na pilha que se refere a seu próprio objeto COM, o aplicativo de hospedagem poderá chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto que espera ser sua própria implementação e, em vez disso, receber o objeto do componente hospedado.</span><span class="sxs-lookup"><span data-stu-id="c493e-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="c493e-108">Para evitar essa herança de contextos de ativação, um bom aplicativo de hospedagem deve ativar seu próprio contexto de ativação bem conhecido primeiro durante um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c493e-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="c493e-109">Considere o exemplo a seguir que protege o código do aplicativo de hospedagem:</span><span class="sxs-lookup"><span data-stu-id="c493e-109">Consider the following example that protects the hosting application's code:</span></span>

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

<span data-ttu-id="c493e-110">Isso garante que um contexto de ativação adequado seja definido antes de passar a solicitação para alguma implementação interna de **funct**.</span><span class="sxs-lookup"><span data-stu-id="c493e-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="c493e-111">Sua própria implementação pode ter a implementação real embutida, mas o método anterior garante a interoperabilidade mais fácil criando apenas wrappers delegados.</span><span class="sxs-lookup"><span data-stu-id="c493e-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="c493e-112">É recomendável usar um método semelhante ao expor retornos de chamada normais (não COM).</span><span class="sxs-lookup"><span data-stu-id="c493e-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
