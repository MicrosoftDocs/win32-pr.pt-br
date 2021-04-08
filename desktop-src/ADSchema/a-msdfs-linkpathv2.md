---
title: atributo ms-DFS-link-Path-v2
description: Caminho de link DFS relativo ao compartilhamento de destino de raiz DFS (ou seja, sem os componentes de nome de namespace de servidor/domínio e DFS). Use barras (/) em vez de barras invertidas ( \) para que as pesquisas LDAP possam ser feitas sem a necessidade de usar escapes.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DFS-link-Path-v2
- Esquema de AD do atributo msDFS-LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087105"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="5618c-106">atributo ms-DFS-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="5618c-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="5618c-107">Caminho de link DFS relativo ao compartilhamento de destino de raiz DFS (ou seja, sem os componentes de nome de namespace de servidor/domínio e DFS).</span><span class="sxs-lookup"><span data-stu-id="5618c-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="5618c-108">Use barras (/) em vez de barras invertidas ( \) para que as pesquisas LDAP possam ser feitas sem a necessidade de usar escapes.</span><span class="sxs-lookup"><span data-stu-id="5618c-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="5618c-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5618c-109">Entry</span></span> | <span data-ttu-id="5618c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5618c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5618c-111">CN</span><span class="sxs-lookup"><span data-stu-id="5618c-111">CN</span></span>                | <span data-ttu-id="5618c-112">MS-DFS-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="5618c-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="5618c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5618c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5618c-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="5618c-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="5618c-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5618c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5618c-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5618c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5618c-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5618c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5618c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5618c-118">Attribute-Id</span></span>      | <span data-ttu-id="5618c-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="5618c-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="5618c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5618c-120">System-Id-Guid</span></span>    | <span data-ttu-id="5618c-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="5618c-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="5618c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5618c-122">Syntax</span></span>            | [<span data-ttu-id="5618c-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5618c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5618c-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="5618c-124">Implementations</span></span>

-   [<span data-ttu-id="5618c-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5618c-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5618c-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5618c-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5618c-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5618c-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="5618c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5618c-128">Windows Server 2008</span></span>



| <span data-ttu-id="5618c-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="5618c-129">Entry</span></span> | <span data-ttu-id="5618c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5618c-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5618c-131">ID do link</span><span class="sxs-lookup"><span data-stu-id="5618c-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5618c-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5618c-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5618c-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="5618c-133">System-Only</span></span>            | <span data-ttu-id="5618c-134">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-135">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5618c-135">Is-Single-Valued</span></span>       | <span data-ttu-id="5618c-136">True</span><span class="sxs-lookup"><span data-stu-id="5618c-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="5618c-137">É indexado</span><span class="sxs-lookup"><span data-stu-id="5618c-137">Is Indexed</span></span>             | <span data-ttu-id="5618c-138">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-139">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5618c-139">In Global Catalog</span></span>      | <span data-ttu-id="5618c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5618c-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="5618c-142">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5618c-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5618c-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5618c-143">Range-Lower</span></span>            | <span data-ttu-id="5618c-144">0</span><span class="sxs-lookup"><span data-stu-id="5618c-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="5618c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5618c-145">Range-Upper</span></span>            | <span data-ttu-id="5618c-146">32766</span><span class="sxs-lookup"><span data-stu-id="5618c-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5618c-147">Search-Flags</span></span>           | <span data-ttu-id="5618c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5618c-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5618c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5618c-149">System-Flags</span></span>           | <span data-ttu-id="5618c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5618c-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5618c-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5618c-151">Classes used in</span></span>        | [<span data-ttu-id="5618c-152">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="5618c-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5618c-153">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="5618c-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5618c-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5618c-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5618c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="5618c-155">Entry</span></span> | <span data-ttu-id="5618c-156">Valor</span><span class="sxs-lookup"><span data-stu-id="5618c-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5618c-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="5618c-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5618c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5618c-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5618c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5618c-159">System-Only</span></span>            | <span data-ttu-id="5618c-160">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5618c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5618c-162">True</span><span class="sxs-lookup"><span data-stu-id="5618c-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="5618c-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="5618c-163">Is Indexed</span></span>             | <span data-ttu-id="5618c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5618c-165">In Global Catalog</span></span>      | <span data-ttu-id="5618c-166">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5618c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5618c-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5618c-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5618c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5618c-169">Range-Lower</span></span>            | <span data-ttu-id="5618c-170">0</span><span class="sxs-lookup"><span data-stu-id="5618c-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="5618c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5618c-171">Range-Upper</span></span>            | <span data-ttu-id="5618c-172">32766</span><span class="sxs-lookup"><span data-stu-id="5618c-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5618c-173">Search-Flags</span></span>           | <span data-ttu-id="5618c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5618c-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5618c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5618c-175">System-Flags</span></span>           | <span data-ttu-id="5618c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5618c-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5618c-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5618c-177">Classes used in</span></span>        | [<span data-ttu-id="5618c-178">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="5618c-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5618c-179">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="5618c-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5618c-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5618c-180">Windows Server 2012</span></span>



| <span data-ttu-id="5618c-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="5618c-181">Entry</span></span> | <span data-ttu-id="5618c-182">Valor</span><span class="sxs-lookup"><span data-stu-id="5618c-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5618c-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="5618c-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5618c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5618c-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5618c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="5618c-185">System-Only</span></span>            | <span data-ttu-id="5618c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5618c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="5618c-188">True</span><span class="sxs-lookup"><span data-stu-id="5618c-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="5618c-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="5618c-189">Is Indexed</span></span>             | <span data-ttu-id="5618c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5618c-191">In Global Catalog</span></span>      | <span data-ttu-id="5618c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="5618c-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5618c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="5618c-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5618c-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5618c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5618c-195">Range-Lower</span></span>            | <span data-ttu-id="5618c-196">0</span><span class="sxs-lookup"><span data-stu-id="5618c-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="5618c-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5618c-197">Range-Upper</span></span>            | <span data-ttu-id="5618c-198">32766</span><span class="sxs-lookup"><span data-stu-id="5618c-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5618c-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5618c-199">Search-Flags</span></span>           | <span data-ttu-id="5618c-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5618c-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5618c-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5618c-201">System-Flags</span></span>           | <span data-ttu-id="5618c-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5618c-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5618c-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5618c-203">Classes used in</span></span>        | [<span data-ttu-id="5618c-204">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="5618c-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5618c-205">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="5618c-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





