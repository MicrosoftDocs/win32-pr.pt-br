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
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386855"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="3bd20-106">atributo ms-DFS-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="3bd20-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="3bd20-107">Caminho de link DFS relativo ao compartilhamento de destino de raiz DFS (ou seja, sem os componentes de nome de namespace de servidor/domínio e DFS).</span><span class="sxs-lookup"><span data-stu-id="3bd20-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="3bd20-108">Use barras (/) em vez de barras invertidas ( \\ ), para que as pesquisas LDAP possam ser feitas sem a necessidade de usar escapes.</span><span class="sxs-lookup"><span data-stu-id="3bd20-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="3bd20-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3bd20-109">Entry</span></span> | <span data-ttu-id="3bd20-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd20-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3bd20-111">CN</span><span class="sxs-lookup"><span data-stu-id="3bd20-111">CN</span></span>                | <span data-ttu-id="3bd20-112">MS-DFS-link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="3bd20-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="3bd20-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3bd20-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3bd20-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="3bd20-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="3bd20-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3bd20-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3bd20-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3bd20-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3bd20-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3bd20-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3bd20-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3bd20-118">Attribute-Id</span></span>      | <span data-ttu-id="3bd20-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="3bd20-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="3bd20-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3bd20-120">System-Id-Guid</span></span>    | <span data-ttu-id="3bd20-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="3bd20-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="3bd20-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bd20-122">Syntax</span></span>            | [<span data-ttu-id="3bd20-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3bd20-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3bd20-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="3bd20-124">Implementations</span></span>

-   [<span data-ttu-id="3bd20-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3bd20-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3bd20-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3bd20-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3bd20-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="3bd20-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bd20-128">Windows Server 2008</span></span>



| <span data-ttu-id="3bd20-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="3bd20-129">Entry</span></span> | <span data-ttu-id="3bd20-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd20-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd20-131">ID do link</span><span class="sxs-lookup"><span data-stu-id="3bd20-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3bd20-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3bd20-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3bd20-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="3bd20-133">System-Only</span></span>            | <span data-ttu-id="3bd20-134">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-135">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3bd20-135">Is-Single-Valued</span></span>       | <span data-ttu-id="3bd20-136">True</span><span class="sxs-lookup"><span data-stu-id="3bd20-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="3bd20-137">É indexado</span><span class="sxs-lookup"><span data-stu-id="3bd20-137">Is Indexed</span></span>             | <span data-ttu-id="3bd20-138">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-139">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3bd20-139">In Global Catalog</span></span>      | <span data-ttu-id="3bd20-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3bd20-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="3bd20-142">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3bd20-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3bd20-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3bd20-143">Range-Lower</span></span>            | <span data-ttu-id="3bd20-144">0</span><span class="sxs-lookup"><span data-stu-id="3bd20-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="3bd20-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3bd20-145">Range-Upper</span></span>            | <span data-ttu-id="3bd20-146">32766</span><span class="sxs-lookup"><span data-stu-id="3bd20-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3bd20-147">Search-Flags</span></span>           | <span data-ttu-id="3bd20-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3bd20-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3bd20-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3bd20-149">System-Flags</span></span>           | <span data-ttu-id="3bd20-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3bd20-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3bd20-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3bd20-151">Classes used in</span></span>        | [<span data-ttu-id="3bd20-152">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3bd20-153">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3bd20-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3bd20-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3bd20-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="3bd20-155">Entry</span></span> | <span data-ttu-id="3bd20-156">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd20-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd20-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="3bd20-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3bd20-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3bd20-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3bd20-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3bd20-159">System-Only</span></span>            | <span data-ttu-id="3bd20-160">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3bd20-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3bd20-162">True</span><span class="sxs-lookup"><span data-stu-id="3bd20-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="3bd20-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="3bd20-163">Is Indexed</span></span>             | <span data-ttu-id="3bd20-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3bd20-165">In Global Catalog</span></span>      | <span data-ttu-id="3bd20-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3bd20-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3bd20-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3bd20-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3bd20-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3bd20-169">Range-Lower</span></span>            | <span data-ttu-id="3bd20-170">0</span><span class="sxs-lookup"><span data-stu-id="3bd20-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="3bd20-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3bd20-171">Range-Upper</span></span>            | <span data-ttu-id="3bd20-172">32766</span><span class="sxs-lookup"><span data-stu-id="3bd20-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3bd20-173">Search-Flags</span></span>           | <span data-ttu-id="3bd20-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3bd20-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3bd20-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3bd20-175">System-Flags</span></span>           | <span data-ttu-id="3bd20-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3bd20-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3bd20-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3bd20-177">Classes used in</span></span>        | [<span data-ttu-id="3bd20-178">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3bd20-179">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3bd20-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bd20-180">Windows Server 2012</span></span>



| <span data-ttu-id="3bd20-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="3bd20-181">Entry</span></span> | <span data-ttu-id="3bd20-182">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd20-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd20-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="3bd20-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3bd20-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3bd20-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="3bd20-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3bd20-185">System-Only</span></span>            | <span data-ttu-id="3bd20-186">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3bd20-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3bd20-188">True</span><span class="sxs-lookup"><span data-stu-id="3bd20-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="3bd20-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="3bd20-189">Is Indexed</span></span>             | <span data-ttu-id="3bd20-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3bd20-191">In Global Catalog</span></span>      | <span data-ttu-id="3bd20-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3bd20-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3bd20-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3bd20-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3bd20-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="3bd20-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3bd20-195">Range-Lower</span></span>            | <span data-ttu-id="3bd20-196">0</span><span class="sxs-lookup"><span data-stu-id="3bd20-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="3bd20-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3bd20-197">Range-Upper</span></span>            | <span data-ttu-id="3bd20-198">32766</span><span class="sxs-lookup"><span data-stu-id="3bd20-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="3bd20-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3bd20-199">Search-Flags</span></span>           | <span data-ttu-id="3bd20-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3bd20-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="3bd20-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3bd20-201">System-Flags</span></span>           | <span data-ttu-id="3bd20-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3bd20-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="3bd20-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3bd20-203">Classes used in</span></span>        | [<span data-ttu-id="3bd20-204">**MS-DFS-Deleted-link-v2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="3bd20-205">**MS-DFS-link-v2**</span><span class="sxs-lookup"><span data-stu-id="3bd20-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





