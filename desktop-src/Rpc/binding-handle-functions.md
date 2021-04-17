---
title: Funções de identificador de associação
description: A tabela a seguir contém a lista de rotinas de tempo de execução RPC que operam em identificadores de associação e especifica o tipo de identificador de associação permitido.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790000"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="a59ea-103">Funções de identificador de associação</span><span class="sxs-lookup"><span data-stu-id="a59ea-103">Binding Handle Functions</span></span>

<span data-ttu-id="a59ea-104">A tabela a seguir contém a lista de rotinas de tempo de execução RPC que operam em identificadores de associação e especifica o tipo de identificador de associação permitido.</span><span class="sxs-lookup"><span data-stu-id="a59ea-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="a59ea-105">Rotina</span><span class="sxs-lookup"><span data-stu-id="a59ea-105">Routine</span></span>                                                            | <span data-ttu-id="a59ea-106">Argumento de entrada</span><span class="sxs-lookup"><span data-stu-id="a59ea-106">Input argument</span></span>   | <span data-ttu-id="a59ea-107">Argumento de saída</span><span class="sxs-lookup"><span data-stu-id="a59ea-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="a59ea-108">**RpcBindingCopy**</span><span class="sxs-lookup"><span data-stu-id="a59ea-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="a59ea-109">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-109">Server</span></span>           | <span data-ttu-id="a59ea-110">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-110">Server</span></span>          |
| [<span data-ttu-id="a59ea-111">**RpcBindingFree**</span><span class="sxs-lookup"><span data-stu-id="a59ea-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="a59ea-112">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-112">Server</span></span>           | <span data-ttu-id="a59ea-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-113">None</span></span>            |
| [<span data-ttu-id="a59ea-114">**RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="a59ea-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="a59ea-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-115">None</span></span>             | <span data-ttu-id="a59ea-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-116">Server</span></span>          |
| [<span data-ttu-id="a59ea-117">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="a59ea-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="a59ea-118">Cliente</span><span class="sxs-lookup"><span data-stu-id="a59ea-118">Client</span></span>           | <span data-ttu-id="a59ea-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-119">None</span></span>            |
| [<span data-ttu-id="a59ea-120">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="a59ea-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="a59ea-121">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-121">Server</span></span>           | <span data-ttu-id="a59ea-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-122">None</span></span>            |
| [<span data-ttu-id="a59ea-123">**RpcBindingInqObject**</span><span class="sxs-lookup"><span data-stu-id="a59ea-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="a59ea-124">Servidor ou cliente</span><span class="sxs-lookup"><span data-stu-id="a59ea-124">Server or client</span></span> | <span data-ttu-id="a59ea-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-125">None</span></span>            |
| [<span data-ttu-id="a59ea-126">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="a59ea-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="a59ea-127">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-127">Server</span></span>           | <span data-ttu-id="a59ea-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-128">None</span></span>            |
| [<span data-ttu-id="a59ea-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="a59ea-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="a59ea-130">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-130">Server</span></span>           | <span data-ttu-id="a59ea-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-131">None</span></span>            |
| [<span data-ttu-id="a59ea-132">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="a59ea-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="a59ea-133">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-133">Server</span></span>           | <span data-ttu-id="a59ea-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-134">None</span></span>            |
| [<span data-ttu-id="a59ea-135">**RpcBindingToStringBinding**</span><span class="sxs-lookup"><span data-stu-id="a59ea-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="a59ea-136">Servidor ou cliente</span><span class="sxs-lookup"><span data-stu-id="a59ea-136">Server or client</span></span> | <span data-ttu-id="a59ea-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-137">None</span></span>            |
| [<span data-ttu-id="a59ea-138">**RpcBindingVectorFree**</span><span class="sxs-lookup"><span data-stu-id="a59ea-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="a59ea-139">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-139">Server</span></span>           | <span data-ttu-id="a59ea-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-140">None</span></span>            |
| [<span data-ttu-id="a59ea-141">**RpcNsBindingExport**</span><span class="sxs-lookup"><span data-stu-id="a59ea-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="a59ea-142">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-142">Server</span></span>           | <span data-ttu-id="a59ea-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-143">None</span></span>            |
| [<span data-ttu-id="a59ea-144">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="a59ea-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="a59ea-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-145">None</span></span>             | <span data-ttu-id="a59ea-146">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-146">Server</span></span>          |
| [<span data-ttu-id="a59ea-147">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="a59ea-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="a59ea-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-148">None</span></span>             | <span data-ttu-id="a59ea-149">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-149">Server</span></span>          |
| [<span data-ttu-id="a59ea-150">**RpcNsBindingSelect**</span><span class="sxs-lookup"><span data-stu-id="a59ea-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="a59ea-151">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-151">Server</span></span>           | <span data-ttu-id="a59ea-152">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-152">Server</span></span>          |
| [<span data-ttu-id="a59ea-153">**RpcServerInqBindings**</span><span class="sxs-lookup"><span data-stu-id="a59ea-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="a59ea-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a59ea-154">None</span></span>             | <span data-ttu-id="a59ea-155">Servidor</span><span class="sxs-lookup"><span data-stu-id="a59ea-155">Server</span></span>          |



 

 

 




