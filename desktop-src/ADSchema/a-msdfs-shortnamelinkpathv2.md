---
title: atributo ms-DFS-Short-Name-link-Path-v2
description: Caminho de link DFS de nome curto relativo ao compartilhamento de destino de raiz DFS (ou seja, sem os componentes de nome de namespace de servidor/domínio e DFS). Use barras (/) em vez de barras invertidas ( \) para que as pesquisas LDAP possam ser feitas sem a necessidade de usar escapes.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- MS-DFS-Short-Name-link-Path-v2 atributo AD Schema
- Esquema de AD do atributo msDFS-ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386845"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="9f3d8-106">atributo ms-DFS-Short-Name-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="9f3d8-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="9f3d8-107">Caminho de link DFS de nome curto relativo ao compartilhamento de destino de raiz DFS (ou seja, sem os componentes de nome de namespace de servidor/domínio e DFS).</span><span class="sxs-lookup"><span data-stu-id="9f3d8-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="9f3d8-108">Use barras (/) em vez de barras invertidas ( \\ ), para que as pesquisas LDAP possam ser feitas sem a necessidade de usar escapes.</span><span class="sxs-lookup"><span data-stu-id="9f3d8-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="9f3d8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f3d8-109">Entry</span></span> | <span data-ttu-id="9f3d8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9f3d8-111">CN</span><span class="sxs-lookup"><span data-stu-id="9f3d8-111">CN</span></span>                | <span data-ttu-id="9f3d8-112">MS-DFS-Short-Name-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="9f3d8-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="9f3d8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9f3d8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9f3d8-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="9f3d8-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="9f3d8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9f3d8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9f3d8-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9f3d8-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9f3d8-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9f3d8-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9f3d8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f3d8-118">Attribute-Id</span></span>      | <span data-ttu-id="9f3d8-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="9f3d8-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="9f3d8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9f3d8-120">System-Id-Guid</span></span>    | <span data-ttu-id="9f3d8-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="9f3d8-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="9f3d8-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f3d8-122">Syntax</span></span>            | [<span data-ttu-id="9f3d8-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9f3d8-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="9f3d8-124">Implementations</span></span>

-   [<span data-ttu-id="9f3d8-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f3d8-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f3d8-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="9f3d8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f3d8-128">Windows Server 2008</span></span>



| <span data-ttu-id="9f3d8-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f3d8-129">Entry</span></span> | <span data-ttu-id="9f3d8-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3d8-131">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f3d8-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="9f3d8-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f3d8-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="9f3d8-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f3d8-133">System-Only</span></span>            | <span data-ttu-id="9f3d8-134">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-135">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f3d8-135">Is-Single-Valued</span></span>       | <span data-ttu-id="9f3d8-136">True</span><span class="sxs-lookup"><span data-stu-id="9f3d8-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="9f3d8-137">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f3d8-137">Is Indexed</span></span>             | <span data-ttu-id="9f3d8-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-139">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f3d8-139">In Global Catalog</span></span>      | <span data-ttu-id="9f3d8-140">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f3d8-142">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f3d8-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="9f3d8-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f3d8-143">Range-Lower</span></span>            | <span data-ttu-id="9f3d8-144">0</span><span class="sxs-lookup"><span data-stu-id="9f3d8-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="9f3d8-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f3d8-145">Range-Upper</span></span>            | <span data-ttu-id="9f3d8-146">32766</span><span class="sxs-lookup"><span data-stu-id="9f3d8-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f3d8-147">Search-Flags</span></span>           | <span data-ttu-id="9f3d8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f3d8-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="9f3d8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f3d8-149">System-Flags</span></span>           | <span data-ttu-id="9f3d8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f3d8-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="9f3d8-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f3d8-151">Classes used in</span></span>        | [<span data-ttu-id="9f3d8-152">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="9f3d8-153">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f3d8-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f3d8-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f3d8-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f3d8-155">Entry</span></span> | <span data-ttu-id="9f3d8-156">Valor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3d8-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f3d8-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="9f3d8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f3d8-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="9f3d8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f3d8-159">System-Only</span></span>            | <span data-ttu-id="9f3d8-160">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f3d8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9f3d8-162">True</span><span class="sxs-lookup"><span data-stu-id="9f3d8-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="9f3d8-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f3d8-163">Is Indexed</span></span>             | <span data-ttu-id="9f3d8-164">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f3d8-165">In Global Catalog</span></span>      | <span data-ttu-id="9f3d8-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f3d8-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f3d8-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="9f3d8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f3d8-169">Range-Lower</span></span>            | <span data-ttu-id="9f3d8-170">0</span><span class="sxs-lookup"><span data-stu-id="9f3d8-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="9f3d8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f3d8-171">Range-Upper</span></span>            | <span data-ttu-id="9f3d8-172">32766</span><span class="sxs-lookup"><span data-stu-id="9f3d8-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f3d8-173">Search-Flags</span></span>           | <span data-ttu-id="9f3d8-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f3d8-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="9f3d8-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f3d8-175">System-Flags</span></span>           | <span data-ttu-id="9f3d8-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f3d8-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="9f3d8-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f3d8-177">Classes used in</span></span>        | [<span data-ttu-id="9f3d8-178">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="9f3d8-179">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f3d8-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f3d8-180">Windows Server 2012</span></span>



| <span data-ttu-id="9f3d8-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f3d8-181">Entry</span></span> | <span data-ttu-id="9f3d8-182">Valor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3d8-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="9f3d8-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="9f3d8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f3d8-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="9f3d8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f3d8-185">System-Only</span></span>            | <span data-ttu-id="9f3d8-186">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9f3d8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="9f3d8-188">True</span><span class="sxs-lookup"><span data-stu-id="9f3d8-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="9f3d8-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="9f3d8-189">Is Indexed</span></span>             | <span data-ttu-id="9f3d8-190">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9f3d8-191">In Global Catalog</span></span>      | <span data-ttu-id="9f3d8-192">Falso</span><span class="sxs-lookup"><span data-stu-id="9f3d8-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9f3d8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f3d8-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9f3d8-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="9f3d8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f3d8-195">Range-Lower</span></span>            | <span data-ttu-id="9f3d8-196">0</span><span class="sxs-lookup"><span data-stu-id="9f3d8-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="9f3d8-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f3d8-197">Range-Upper</span></span>            | <span data-ttu-id="9f3d8-198">32766</span><span class="sxs-lookup"><span data-stu-id="9f3d8-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="9f3d8-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f3d8-199">Search-Flags</span></span>           | <span data-ttu-id="9f3d8-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f3d8-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="9f3d8-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f3d8-201">System-Flags</span></span>           | <span data-ttu-id="9f3d8-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f3d8-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="9f3d8-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9f3d8-203">Classes used in</span></span>        | [<span data-ttu-id="9f3d8-204">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="9f3d8-205">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="9f3d8-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





