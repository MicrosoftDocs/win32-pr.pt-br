---
description: Chamando fora de um assembly
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Chamando fora de um assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748555"
---
# <a name="calling-outside-an-assembly"></a><span data-ttu-id="f2bd9-103">Chamando fora de um assembly</span><span class="sxs-lookup"><span data-stu-id="f2bd9-103">Calling Outside An Assembly</span></span>

<span data-ttu-id="f2bd9-104">Os componentes hospedados devem garantir que o contexto de ativação correto esteja ativo ao chamar fora do componente.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-104">Hosted components should ensure that the correct activation context is active when calling outside the component.</span></span> <span data-ttu-id="f2bd9-105">Chamadas para o código externo que foi encontrado chamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) e, em seguida, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), devem ser chamadas com o mesmo contexto que foi usado para encontrá-lo.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-105">Calls into outside code that was found by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) and then [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), should be called with the same context that was used to find it.</span></span> <span data-ttu-id="f2bd9-106">Chamadas para o código que foi encontrado fora dos contextos de ativação ou chamadas de volta para o aplicativo de hospedagem devem ser chamadas com o contexto de ativação padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-106">Calls into code that was found outside of activation contexts, or calls back into the hosting application should be called with the application default activation context.</span></span>

<span data-ttu-id="f2bd9-107">A compilação com \_ reconhecimento \_ de isolamento habilitado pode ser útil ao chamar fora de componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-107">Compiling with ISOLATION\_AWARE\_ENABLED defined may be useful when calling outside of hosted components.</span></span> <span data-ttu-id="f2bd9-108">No entanto, isso significa que somente as chamadas para APIs do Windows são isoladas para o contexto de ativação do componente.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-108">However this means that only calls to Windows APIs are isolated to the component's activation context.</span></span> <span data-ttu-id="f2bd9-109">Isso é suficiente para a maioria dos casos porque as chamadas para funções de terceiros não têm um contexto ativado antes de serem chamadas.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-109">This is sufficient for most cases because calls to third-party functions do not have a context activated before being called.</span></span> <span data-ttu-id="f2bd9-110">A compilação com \_ habilitado para isolamento \_ definido não ajuda se o seu componente usa vários contextos de ativação com várias APIs de plataforma.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-110">Compiling with ISOLATION\_AWARE\_ENABLED defined does not help if your component uses several activation contexts with various platform APIs.</span></span>

<span data-ttu-id="f2bd9-111">Para implementar isso, use um ativador de contexto de ativação como o exemplo apresentado em [isolando componentes](isolating-components.md).</span><span class="sxs-lookup"><span data-stu-id="f2bd9-111">To implement this, use an activation context activator like the example presented in [Isolating Components](isolating-components.md).</span></span> <span data-ttu-id="f2bd9-112">Aqui estão as externas. o manifesto é o conjunto de dependências fora dos quais o componente foi criado; Talvez ele contenha uma lista extensível de componentes que devem ser carregados e usados durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-112">Here externals.manifest is the set of dependencies outside those the component was built with; perhaps it contains some extendable list of components that are to be loaded and used during runtime.</span></span> <span data-ttu-id="f2bd9-113">O internalcontext. manifest contém o conjunto de dependências que o componente usa durante seu tempo de vida e que deve ser definido em todos os entryPoints de fora.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-113">The internalcontext.manifest contains the set of dependencies that the component is sure to use during its lifetime, and which should be set in all entrypoints from the outside.</span></span> <span data-ttu-id="f2bd9-114">Observe que esse contexto interno é ativado em todos os entryPoints, enquanto o ativador de contexto é usado com o escopo do C++ para que o contexto apropriado seja definido ao chamar os vários códigos externos que esse componente usa.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-114">Notice that this internal context is activated in all entrypoints, while the context activator is used with C++ scoping so that the proper context is set when calling out to the various outside code that this component uses.</span></span>

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
