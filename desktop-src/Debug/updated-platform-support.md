---
description: Quando necessário, a biblioteca DbgHelp foi ampliada para dar suporte às janelas de 32 e 64 bits.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Suporte atualizado à plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500954"
---
# <a name="updated-platform-support"></a><span data-ttu-id="be909-103">Suporte atualizado à plataforma</span><span class="sxs-lookup"><span data-stu-id="be909-103">Updated Platform Support</span></span>

<span data-ttu-id="be909-104">Quando necessário, a biblioteca DbgHelp foi ampliada para dar suporte às janelas de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be909-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="be909-105">As definições de função e estrutura originais ainda estão em DbgHelp. h, mas também há versões atualizadas dessas definições que são compatíveis com o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be909-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="be909-106">Se você usar as funções atualizadas em seu código, ele poderá ser compilado para o Windows de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be909-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="be909-107">Seu código também será mais eficiente, pois as funções originais simplesmente chamam as funções atualizadas para executar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="be909-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="be909-108">Por exemplo, DbgHelp. h contém definições para **SymUnloadModule** (função original) e **SymUnloadModule64** (função Updated).</span><span class="sxs-lookup"><span data-stu-id="be909-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="be909-109">Essas definições são quase idênticas, mas usam tipos diferentes para o parâmetro *BaseOfDll* .</span><span class="sxs-lookup"><span data-stu-id="be909-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="be909-110">(**SymUnloadModule** usa o tipo **DWORD** , enquanto **SymUnloadModule64** usa o tipo **DWORD64** .) Se você escrever seu código para usar o **SymUnloadModule64**, ele poderá ser compilado para o Windows de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be909-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="be909-111">O código também é mais eficiente do que se fosse chamar **SymUnloadModule**.</span><span class="sxs-lookup"><span data-stu-id="be909-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="be909-112">Veja a seguir uma lista das funções atualizadas:</span><span class="sxs-lookup"><span data-stu-id="be909-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="be909-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="be909-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="be909-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="be909-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="be909-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="be909-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="be909-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="be909-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="be909-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="be909-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="be909-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="be909-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="be909-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="be909-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="be909-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="be909-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="be909-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="be909-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="be909-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="be909-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="be909-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="be909-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="be909-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="be909-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="be909-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="be909-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="be909-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="be909-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="be909-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="be909-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="be909-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="be909-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="be909-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="be909-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="be909-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="be909-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="be909-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="be909-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="be909-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="be909-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="be909-133">Veja a seguir uma lista das estruturas atualizadas:</span><span class="sxs-lookup"><span data-stu-id="be909-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="be909-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="be909-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="be909-135">**\_Símbolo DEferido de imagehlp \_ \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="be909-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="be909-136">**\_SYMBOL64 duplicado do imagehlp \_**</span><span class="sxs-lookup"><span data-stu-id="be909-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="be909-137">**LINE64 de IMAGEHLP \_**</span><span class="sxs-lookup"><span data-stu-id="be909-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="be909-138">**MODULE64 de IMAGEHLP \_**</span><span class="sxs-lookup"><span data-stu-id="be909-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="be909-139">**SYMBOL64 de IMAGEHLP \_**</span><span class="sxs-lookup"><span data-stu-id="be909-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="be909-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="be909-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="be909-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="be909-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



