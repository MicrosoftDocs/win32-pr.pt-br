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
ms.openlocfilehash: 4a536abdf13bed7acc99c1036d3c259493994b28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105751005"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="29e74-106">atributo ms-DFS-Short-Name-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="29e74-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="29e74-107">Caminho de link DFS de nome curto relativo ao compartilhamento de destino de raiz DFS (ou seja, sem os componentes de nome de namespace de servidor/domínio e DFS).</span><span class="sxs-lookup"><span data-stu-id="29e74-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="29e74-108">Use barras (/) em vez de barras invertidas ( \) para que as pesquisas LDAP possam ser feitas sem a necessidade de usar escapes.</span><span class="sxs-lookup"><span data-stu-id="29e74-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="29e74-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="29e74-109">Entry</span></span> | <span data-ttu-id="29e74-110">Valor</span><span class="sxs-lookup"><span data-stu-id="29e74-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="29e74-111">CN</span><span class="sxs-lookup"><span data-stu-id="29e74-111">CN</span></span>                | <span data-ttu-id="29e74-112">MS-DFS-Short-Name-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="29e74-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="29e74-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="29e74-113">Ldap-Display-Name</span></span> | <span data-ttu-id="29e74-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="29e74-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="29e74-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="29e74-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="29e74-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="29e74-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="29e74-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="29e74-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="29e74-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29e74-118">Attribute-Id</span></span>      | <span data-ttu-id="29e74-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="29e74-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="29e74-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="29e74-120">System-Id-Guid</span></span>    | <span data-ttu-id="29e74-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="29e74-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="29e74-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="29e74-122">Syntax</span></span>            | [<span data-ttu-id="29e74-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="29e74-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="29e74-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="29e74-124">Implementations</span></span>

-   [<span data-ttu-id="29e74-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29e74-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29e74-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29e74-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29e74-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29e74-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="29e74-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29e74-128">Windows Server 2008</span></span>



| <span data-ttu-id="29e74-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="29e74-129">Entry</span></span> | <span data-ttu-id="29e74-130">Valor</span><span class="sxs-lookup"><span data-stu-id="29e74-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e74-131">ID do link</span><span class="sxs-lookup"><span data-stu-id="29e74-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="29e74-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29e74-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="29e74-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="29e74-133">System-Only</span></span>            | <span data-ttu-id="29e74-134">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-135">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29e74-135">Is-Single-Valued</span></span>       | <span data-ttu-id="29e74-136">True</span><span class="sxs-lookup"><span data-stu-id="29e74-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="29e74-137">É indexado</span><span class="sxs-lookup"><span data-stu-id="29e74-137">Is Indexed</span></span>             | <span data-ttu-id="29e74-138">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-139">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29e74-139">In Global Catalog</span></span>      | <span data-ttu-id="29e74-140">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29e74-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="29e74-142">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29e74-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="29e74-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29e74-143">Range-Lower</span></span>            | <span data-ttu-id="29e74-144">0</span><span class="sxs-lookup"><span data-stu-id="29e74-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="29e74-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29e74-145">Range-Upper</span></span>            | <span data-ttu-id="29e74-146">32766</span><span class="sxs-lookup"><span data-stu-id="29e74-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29e74-147">Search-Flags</span></span>           | <span data-ttu-id="29e74-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29e74-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="29e74-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29e74-149">System-Flags</span></span>           | <span data-ttu-id="29e74-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29e74-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="29e74-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29e74-151">Classes used in</span></span>        | [<span data-ttu-id="29e74-152">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="29e74-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="29e74-153">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="29e74-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29e74-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29e74-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29e74-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="29e74-155">Entry</span></span> | <span data-ttu-id="29e74-156">Valor</span><span class="sxs-lookup"><span data-stu-id="29e74-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e74-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="29e74-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="29e74-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29e74-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="29e74-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="29e74-159">System-Only</span></span>            | <span data-ttu-id="29e74-160">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29e74-161">Is-Single-Valued</span></span>       | <span data-ttu-id="29e74-162">True</span><span class="sxs-lookup"><span data-stu-id="29e74-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="29e74-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="29e74-163">Is Indexed</span></span>             | <span data-ttu-id="29e74-164">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29e74-165">In Global Catalog</span></span>      | <span data-ttu-id="29e74-166">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29e74-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="29e74-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29e74-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="29e74-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29e74-169">Range-Lower</span></span>            | <span data-ttu-id="29e74-170">0</span><span class="sxs-lookup"><span data-stu-id="29e74-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="29e74-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29e74-171">Range-Upper</span></span>            | <span data-ttu-id="29e74-172">32766</span><span class="sxs-lookup"><span data-stu-id="29e74-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29e74-173">Search-Flags</span></span>           | <span data-ttu-id="29e74-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29e74-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="29e74-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29e74-175">System-Flags</span></span>           | <span data-ttu-id="29e74-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29e74-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="29e74-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29e74-177">Classes used in</span></span>        | [<span data-ttu-id="29e74-178">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="29e74-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="29e74-179">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="29e74-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29e74-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29e74-180">Windows Server 2012</span></span>



| <span data-ttu-id="29e74-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="29e74-181">Entry</span></span> | <span data-ttu-id="29e74-182">Valor</span><span class="sxs-lookup"><span data-stu-id="29e74-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e74-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="29e74-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="29e74-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29e74-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="29e74-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="29e74-185">System-Only</span></span>            | <span data-ttu-id="29e74-186">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="29e74-187">Is-Single-Valued</span></span>       | <span data-ttu-id="29e74-188">True</span><span class="sxs-lookup"><span data-stu-id="29e74-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="29e74-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="29e74-189">Is Indexed</span></span>             | <span data-ttu-id="29e74-190">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="29e74-191">In Global Catalog</span></span>      | <span data-ttu-id="29e74-192">Falso</span><span class="sxs-lookup"><span data-stu-id="29e74-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="29e74-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="29e74-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="29e74-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="29e74-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29e74-195">Range-Lower</span></span>            | <span data-ttu-id="29e74-196">0</span><span class="sxs-lookup"><span data-stu-id="29e74-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="29e74-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29e74-197">Range-Upper</span></span>            | <span data-ttu-id="29e74-198">32766</span><span class="sxs-lookup"><span data-stu-id="29e74-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="29e74-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29e74-199">Search-Flags</span></span>           | <span data-ttu-id="29e74-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29e74-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="29e74-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29e74-201">System-Flags</span></span>           | <span data-ttu-id="29e74-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29e74-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="29e74-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="29e74-203">Classes used in</span></span>        | [<span data-ttu-id="29e74-204">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="29e74-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="29e74-205">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="29e74-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





