---
title: Desenvolvendo aplicativos RPC do Windows
description: Quando você instala o SDK (Software Development Kit) da plataforma, o seguinte ambiente de desenvolvimento RPC, as bibliotecas de tempo de execução e as ferramentas são instaladas automaticamente
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008055"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="388ba-103">Desenvolvendo aplicativos RPC do Windows</span><span class="sxs-lookup"><span data-stu-id="388ba-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="388ba-104">Quando você instala o SDK (Software Development Kit) da plataforma, o seguinte ambiente de desenvolvimento RPC, as bibliotecas de tempo de execução e as ferramentas são instaladas automaticamente:</span><span class="sxs-lookup"><span data-stu-id="388ba-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="388ba-105">Cabeçalho da linguagem C/C++ (. H) arquivos</span><span class="sxs-lookup"><span data-stu-id="388ba-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="388ba-106">Arquivos de bibliotecas de importação RPC (. lib)</span><span class="sxs-lookup"><span data-stu-id="388ba-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="388ba-107">Programas de exemplo</span><span class="sxs-lookup"><span data-stu-id="388ba-107">Sample programs</span></span>
-   <span data-ttu-id="388ba-108">Arquivos de ajuda de referência RPC</span><span class="sxs-lookup"><span data-stu-id="388ba-108">RPC reference Help files</span></span>
-   <span data-ttu-id="388ba-109">O utilitário **Uuidgen**</span><span class="sxs-lookup"><span data-stu-id="388ba-109">The **uuidgen** utility</span></span>

<span data-ttu-id="388ba-110">Quando você instala o Windows, os seguintes itens são instalados:</span><span class="sxs-lookup"><span data-stu-id="388ba-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="388ba-111">DLLs de tempo de execução RPC</span><span class="sxs-lookup"><span data-stu-id="388ba-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="388ba-112">Microsoft Locator (sem suporte no Windows Vista e posterior)</span><span class="sxs-lookup"><span data-stu-id="388ba-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="388ba-113">Ponto de extremidade RPC-serviços de mapeamento</span><span class="sxs-lookup"><span data-stu-id="388ba-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="388ba-114">As seguintes bibliotecas de importação RPC.</span><span class="sxs-lookup"><span data-stu-id="388ba-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="388ba-115">Biblioteca de importação</span><span class="sxs-lookup"><span data-stu-id="388ba-115">Import library</span></span> | <span data-ttu-id="388ba-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="388ba-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="388ba-117">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="388ba-117">Rpcns4.lib</span></span>     | <span data-ttu-id="388ba-118">Funções de nome-serviço</span><span class="sxs-lookup"><span data-stu-id="388ba-118">Name-service functions</span></span>     |
| <span data-ttu-id="388ba-119">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="388ba-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="388ba-120">Funções de tempo de execução do Windows</span><span class="sxs-lookup"><span data-stu-id="388ba-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="388ba-121">Rpcns4. lib está obsoleto e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="388ba-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="388ba-122">As bibliotecas RPC a seguir estão incluídas para o suporte de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="388ba-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="388ba-123">Biblioteca de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="388ba-123">Dynamic-link library</span></span> | <span data-ttu-id="388ba-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="388ba-124">Description</span></span>                 | <span data-ttu-id="388ba-125">Plataforma</span><span class="sxs-lookup"><span data-stu-id="388ba-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="388ba-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="388ba-127">Transporte de pipe nomeado do cliente</span><span class="sxs-lookup"><span data-stu-id="388ba-127">Client named-pipe transport</span></span> | <span data-ttu-id="388ba-128">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-129">Rpclts1.dll</span></span>          | <span data-ttu-id="388ba-130">Servidor denominado-transporte de pipe</span><span class="sxs-lookup"><span data-stu-id="388ba-130">Server named-pipe transport</span></span> | <span data-ttu-id="388ba-131">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="388ba-133">Transporte TCP/IP do cliente</span><span class="sxs-lookup"><span data-stu-id="388ba-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="388ba-134">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-135">Rpclts3.dll</span></span>          | <span data-ttu-id="388ba-136">Transporte TCP/IP do servidor</span><span class="sxs-lookup"><span data-stu-id="388ba-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="388ba-137">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="388ba-139">Transporte NetBIOS de cliente</span><span class="sxs-lookup"><span data-stu-id="388ba-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="388ba-140">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-141">Rpclts5.dll</span></span>          | <span data-ttu-id="388ba-142">Transporte NetBIOS do servidor</span><span class="sxs-lookup"><span data-stu-id="388ba-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="388ba-143">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="388ba-145">Transporte SPX de cliente</span><span class="sxs-lookup"><span data-stu-id="388ba-145">Client SPX transport</span></span>        | <span data-ttu-id="388ba-146">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-147">Rpclts6.dll</span></span>          | <span data-ttu-id="388ba-148">Transporte SPX do servidor</span><span class="sxs-lookup"><span data-stu-id="388ba-148">Server SPX transport</span></span>        | <span data-ttu-id="388ba-149">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="388ba-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="388ba-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="388ba-151">Transporte IPX do cliente</span><span class="sxs-lookup"><span data-stu-id="388ba-151">Client IPX transport</span></span>        | <span data-ttu-id="388ba-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="388ba-152">Windows NT</span></span>                         |
| <span data-ttu-id="388ba-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="388ba-154">Transporte IPX do servidor</span><span class="sxs-lookup"><span data-stu-id="388ba-154">Server IPX transport</span></span>        | <span data-ttu-id="388ba-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="388ba-155">Windows NT</span></span>                         |
| <span data-ttu-id="388ba-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="388ba-157">Transporte UDP de cliente</span><span class="sxs-lookup"><span data-stu-id="388ba-157">Client UDP transport</span></span>        | <span data-ttu-id="388ba-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="388ba-158">Windows NT</span></span>                         |
| <span data-ttu-id="388ba-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="388ba-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="388ba-160">Transporte UDP do servidor</span><span class="sxs-lookup"><span data-stu-id="388ba-160">Server UDP transport</span></span>        | <span data-ttu-id="388ba-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="388ba-161">Windows NT</span></span>                         |



 

<span data-ttu-id="388ba-162">Você também precisará do compilador linguagem IDL da Microsoft (MIDL).</span><span class="sxs-lookup"><span data-stu-id="388ba-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="388ba-163">Para obter mais informações, consulte [usando o compilador MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).</span><span class="sxs-lookup"><span data-stu-id="388ba-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 