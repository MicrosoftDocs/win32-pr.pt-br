---
description: Os aplicativos podem gerenciar um contexto de ativação chamando diretamente as funções de contexto de ativação.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Usando a API de contexto de ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090201"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="50259-103">Usando a API de contexto de ativação</span><span class="sxs-lookup"><span data-stu-id="50259-103">Using the Activation Context API</span></span>

<span data-ttu-id="50259-104">Os aplicativos podem gerenciar um [contexto de ativação](activation-contexts.md) chamando diretamente as funções de contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="50259-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="50259-105">Contextos de ativação são estruturas de dados na memória.</span><span class="sxs-lookup"><span data-stu-id="50259-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="50259-106">O sistema pode usar as informações no contexto de ativação para redirecionar um aplicativo para carregar uma versão de DLL específica, instância de objeto COM ou versão de janela personalizada.</span><span class="sxs-lookup"><span data-stu-id="50259-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="50259-107">Para obter mais informações, consulte [referência de contexto de ativação](activation-context-reference.md).</span><span class="sxs-lookup"><span data-stu-id="50259-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="50259-108">A API (interface de programação de aplicativo) pode ser usada para gerenciar o contexto de ativação e criar objetos com nome de versão com [manifestos](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="50259-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="50259-109">Os dois cenários a seguir ilustram como um aplicativo pode gerenciar um contexto de ativação chamando diretamente as funções de contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="50259-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="50259-110">Na maioria dos casos, no entanto, o contexto de ativação é gerenciado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="50259-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="50259-111">Os desenvolvedores de aplicativos e os provedores de assembly normalmente não precisam fazer chamadas para a pilha para gerenciar o contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="50259-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="50259-112">Processos e aplicativos que implementam as camadas de indireção ou de expedição.</span><span class="sxs-lookup"><span data-stu-id="50259-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="50259-113">Por exemplo, um usuário Gerenciando contextos de ativação no loop de eventos.</span><span class="sxs-lookup"><span data-stu-id="50259-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="50259-114">Cada vez que a janela é acessada, como movendo o mouse sobre a janela, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) é chamado, o que ativa o contexto de ativação atual para o recurso, conforme mostrado no fragmento de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="50259-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="50259-115">MANIPULAR hActCtx;</span><span class="sxs-lookup"><span data-stu-id="50259-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="50259-116">CreateWindow ();</span><span class="sxs-lookup"><span data-stu-id="50259-116">CreateWindow();</span></span>  
    <span data-ttu-id="50259-117">...</span><span class="sxs-lookup"><span data-stu-id="50259-117">...</span></span>  
    <span data-ttu-id="50259-118">GetCurrentActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="50259-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="50259-119">...</span><span class="sxs-lookup"><span data-stu-id="50259-119">...</span></span>  
    <span data-ttu-id="50259-120">ReleaseActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="50259-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="50259-121">No fragmento de código a seguir, a função de API ativa os contextos de ativação apropriados antes de chamar [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span><span class="sxs-lookup"><span data-stu-id="50259-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="50259-122">Quando **CallWindowProc** é chamado, ele usa esse contexto para passar uma mensagem para o Windows.</span><span class="sxs-lookup"><span data-stu-id="50259-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="50259-123">Quando todas as operações de recurso forem concluídas, a função desativará o contexto.</span><span class="sxs-lookup"><span data-stu-id="50259-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="50259-124">ULONG \_ PTR ulpCookie;</span><span class="sxs-lookup"><span data-stu-id="50259-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="50259-125">MANIPULAR hActCtx;</span><span class="sxs-lookup"><span data-stu-id="50259-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="50259-126">If (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="50259-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="50259-127">{</span><span class="sxs-lookup"><span data-stu-id="50259-127">{</span></span>  
    <span data-ttu-id="50259-128">...</span><span class="sxs-lookup"><span data-stu-id="50259-128">...</span></span>  
    <span data-ttu-id="50259-129">CallWindowProc(...);</span><span class="sxs-lookup"><span data-stu-id="50259-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="50259-130">...</span><span class="sxs-lookup"><span data-stu-id="50259-130">...</span></span>  
    <span data-ttu-id="50259-131">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="50259-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="50259-132">}</span><span class="sxs-lookup"><span data-stu-id="50259-132">}</span></span>  
    </dl>

-   <span data-ttu-id="50259-133">Camada de expedição do delegante.</span><span class="sxs-lookup"><span data-stu-id="50259-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="50259-134">Esse cenário se aplica a gerentes que gerenciam várias entidades com uma camada de API comum, como um Gerenciador de driver.</span><span class="sxs-lookup"><span data-stu-id="50259-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="50259-135">Embora ainda não tenha sido implementado, um exemplo disso seria o driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="50259-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="50259-136">Nesse cenário, a camada intermediária torna-se capaz de processar associações de assembly.</span><span class="sxs-lookup"><span data-stu-id="50259-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="50259-137">Para obter o driver de associação específico à versão, os editores devem fornecer um manifesto e especificar dependências em componentes específicos nesse manifesto.</span><span class="sxs-lookup"><span data-stu-id="50259-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="50259-138">O aplicativo base não se vincula dinamicamente aos componentes; no tempo de execução, o Gerenciador de driver gerencia as chamadas.</span><span class="sxs-lookup"><span data-stu-id="50259-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="50259-139">Quando o driver ODBC é chamado com base na cadeia de conexão, ele carrega o driver apropriado.</span><span class="sxs-lookup"><span data-stu-id="50259-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="50259-140">Em seguida, ele cria o contexto de ativação usando as informações no arquivo de manifesto do assembly.</span><span class="sxs-lookup"><span data-stu-id="50259-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="50259-141">Sem o manifesto, a ação padrão para o driver é usar o mesmo contexto que o especificado pelo aplicativo — neste exemplo, versão 2 do MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="50259-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="50259-142">Como existe um manifesto, um contexto de ativação separado é estabelecido.</span><span class="sxs-lookup"><span data-stu-id="50259-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="50259-143">Quando o driver ODBC é executado, ele é associado à versão 1 do assembly MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="50259-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="50259-144">Cada vez que o Gerenciador de driver chama a camada de expedição, por exemplo, para obter o próximo conjunto de dados, ele usa os assemblies apropriados com base no contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="50259-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="50259-145">O fragmento de código a seguir ilustra isso.</span><span class="sxs-lookup"><span data-stu-id="50259-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="50259-146">MANIPULAR hActCtx;</span><span class="sxs-lookup"><span data-stu-id="50259-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="50259-147">ULONG \_ PTR ulpCookie;</span><span class="sxs-lookup"><span data-stu-id="50259-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="50259-148">ACTCTX ActCtxToCreate = {...};</span><span class="sxs-lookup"><span data-stu-id="50259-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="50259-149">hActCtx = CreateActCtx (&ActCtxToCreate);</span><span class="sxs-lookup"><span data-stu-id="50259-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="50259-150">...;</span><span class="sxs-lookup"><span data-stu-id="50259-150">...;</span></span>  
    <span data-ttu-id="50259-151">If (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="50259-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="50259-152">{</span><span class="sxs-lookup"><span data-stu-id="50259-152">{</span></span>  
    <span data-ttu-id="50259-153">...</span><span class="sxs-lookup"><span data-stu-id="50259-153">...</span></span>  
    <span data-ttu-id="50259-154">ConnectDb(...);</span><span class="sxs-lookup"><span data-stu-id="50259-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="50259-155">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="50259-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="50259-156">}</span><span class="sxs-lookup"><span data-stu-id="50259-156">}</span></span>  
    <span data-ttu-id="50259-157">...</span><span class="sxs-lookup"><span data-stu-id="50259-157">...</span></span>  
    <span data-ttu-id="50259-158">ReleaseActCtx(hActCtx);</span><span class="sxs-lookup"><span data-stu-id="50259-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
