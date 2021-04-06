---
description: Os componentes bem autorizados não perturbarm o ambiente do aplicativo de hospedagem, nem vazam contextos de ativação.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826999"
---
# <a name="isolating-components"></a><span data-ttu-id="a2148-103">Isolando componentes</span><span class="sxs-lookup"><span data-stu-id="a2148-103">Isolating Components</span></span>

<span data-ttu-id="a2148-104">Os componentes bem autorizados não perturbarm o ambiente do aplicativo de hospedagem, nem vazam contextos de ativação.</span><span class="sxs-lookup"><span data-stu-id="a2148-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="a2148-105">Os componentes bem autorizados executam seu próprio gerenciamento de contexto em vez de depender do ambiente do aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="a2148-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="a2148-106">O autor do componente hospedado está na melhor posição para saber exatamente quais outros assemblies o componente requer.</span><span class="sxs-lookup"><span data-stu-id="a2148-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="a2148-107">Depender do aplicativo host para fornecer o ambiente correto para seu componente hospedado é uma provável fonte de erros.</span><span class="sxs-lookup"><span data-stu-id="a2148-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="a2148-108">Em vez disso, crie um manifesto para seu componente hospedado que especifique todas as suas dependências e, em seguida, compile usando o reconhecimento de isolamento \_ \_ habilitado.</span><span class="sxs-lookup"><span data-stu-id="a2148-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="a2148-109">Isso garante que as chamadas externas feitas por seu componente sejam isoladas e usem as versões corretas.</span><span class="sxs-lookup"><span data-stu-id="a2148-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="a2148-110">Como o contexto de ativação \_ \_ habilitado para isolamento usa o é por dll, é seguro usá-lo em várias DLLs, cada um com seu próprio manifesto chamando dependências.</span><span class="sxs-lookup"><span data-stu-id="a2148-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="a2148-111">Se não for possível compilar com \_ reconhecimento \_ de isolamento habilitado, use uma solução como a apresentada em [usando retornos de chamada de componentes hospedados](using-callbacks-from-hosted-components.md).</span><span class="sxs-lookup"><span data-stu-id="a2148-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="a2148-112">Você deve ativar seu próprio contexto de ativação em todos os pontos de entrada que o aplicativo de hospedagem pode chamar para garantir que seu componente hospedado seja executado inteiramente com o contexto de ativação correto.</span><span class="sxs-lookup"><span data-stu-id="a2148-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="a2148-113">Você pode usar um objeto auxiliar do C++ para facilitar a alteração de todos os entryPoints.</span><span class="sxs-lookup"><span data-stu-id="a2148-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="a2148-114">Por exemplo, você pode usar uma classe C++, como a seguinte:</span><span class="sxs-lookup"><span data-stu-id="a2148-114">For example, you could use a C++ class such as the following:</span></span>


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



<span data-ttu-id="a2148-115">Isso pode ser usado em seu componente, usando uma variável global para armazenar o contexto de ativação que deve ser ativado em cada ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2148-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="a2148-116">Dessa forma, você pode isolar o componente do seu aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="a2148-116">In this way, you can isolate your component from your hosting application.</span></span>


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



