---
title: atributo msNPAllowDialin
description: Indica se a conta tem permissão para fazer a conexão com o servidor RAS.
ms.assetid: 8e0d98b4-93b1-4a76-a8b7-d6017028b48a
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo msNPAllowDialin
topic_type:
- apiref
api_name:
- msNPAllowDialin
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e56f9fe3817053e3e1e49611fb76934acbbcba9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087054"
---
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="a1126-104">atributo msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="a1126-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="a1126-105">Indica se a conta tem permissão para fazer a conexão com o servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="a1126-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="a1126-106">Não modifique esse valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="a1126-106">Do not modify this value directly.</span></span> <span data-ttu-id="a1126-107">Use a [função de administração RAS](/windows/desktop/RRAS/ras-administration-functions) apropriada para modificar esse valor.</span><span class="sxs-lookup"><span data-stu-id="a1126-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="a1126-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-108">Entry</span></span> | <span data-ttu-id="a1126-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a1126-110">CN</span><span class="sxs-lookup"><span data-stu-id="a1126-110">CN</span></span>                | <span data-ttu-id="a1126-111">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="a1126-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="a1126-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1126-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a1126-113">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="a1126-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="a1126-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a1126-114">Size</span></span>              | <span data-ttu-id="a1126-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="a1126-115">4 bytes</span></span>                              |
| <span data-ttu-id="a1126-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a1126-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a1126-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a1126-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a1126-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-118">Attribute-Id</span></span>      | <span data-ttu-id="a1126-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="a1126-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="a1126-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1126-120">System-Id-Guid</span></span>    | <span data-ttu-id="a1126-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="a1126-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="a1126-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1126-122">Syntax</span></span>            | [<span data-ttu-id="a1126-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1126-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a1126-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="a1126-124">Implementations</span></span>

-   [<span data-ttu-id="a1126-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1126-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1126-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1126-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1126-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1126-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1126-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1126-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1126-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1126-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1126-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1126-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1126-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1126-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a1126-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-132">Entry</span></span> | <span data-ttu-id="a1126-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a1126-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1126-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1126-136">System-Only</span></span>            | <span data-ttu-id="a1126-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-137">False</span></span>                             |
| <span data-ttu-id="a1126-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1126-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a1126-139">True</span><span class="sxs-lookup"><span data-stu-id="a1126-139">True</span></span>                              |
| <span data-ttu-id="a1126-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1126-140">Is Indexed</span></span>             | <span data-ttu-id="a1126-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-141">False</span></span>                             |
| <span data-ttu-id="a1126-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1126-142">In Global Catalog</span></span>      | <span data-ttu-id="a1126-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-143">False</span></span>                             |
| <span data-ttu-id="a1126-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1126-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1126-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1126-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a1126-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1126-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a1126-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1126-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a1126-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-148">Search-Flags</span></span>           | <span data-ttu-id="a1126-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1126-149">0x00000000</span></span>                        |
| <span data-ttu-id="a1126-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-150">System-Flags</span></span>           | <span data-ttu-id="a1126-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-151">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1126-152">Classes used in</span></span>        | [<span data-ttu-id="a1126-153">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a1126-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1126-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1126-154">Windows Server 2003</span></span>



| <span data-ttu-id="a1126-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-155">Entry</span></span> | <span data-ttu-id="a1126-156">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a1126-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1126-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1126-159">System-Only</span></span>            | <span data-ttu-id="a1126-160">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-160">False</span></span>                             |
| <span data-ttu-id="a1126-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1126-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a1126-162">True</span><span class="sxs-lookup"><span data-stu-id="a1126-162">True</span></span>                              |
| <span data-ttu-id="a1126-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1126-163">Is Indexed</span></span>             | <span data-ttu-id="a1126-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-164">False</span></span>                             |
| <span data-ttu-id="a1126-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1126-165">In Global Catalog</span></span>      | <span data-ttu-id="a1126-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-166">False</span></span>                             |
| <span data-ttu-id="a1126-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1126-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1126-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1126-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a1126-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1126-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a1126-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1126-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a1126-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-171">Search-Flags</span></span>           | <span data-ttu-id="a1126-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1126-172">0x00000000</span></span>                        |
| <span data-ttu-id="a1126-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-173">System-Flags</span></span>           | <span data-ttu-id="a1126-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-174">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1126-175">Classes used in</span></span>        | [<span data-ttu-id="a1126-176">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a1126-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1126-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1126-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1126-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-178">Entry</span></span> | <span data-ttu-id="a1126-179">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a1126-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1126-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1126-182">System-Only</span></span>            | <span data-ttu-id="a1126-183">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-183">False</span></span>                             |
| <span data-ttu-id="a1126-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1126-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a1126-185">True</span><span class="sxs-lookup"><span data-stu-id="a1126-185">True</span></span>                              |
| <span data-ttu-id="a1126-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1126-186">Is Indexed</span></span>             | <span data-ttu-id="a1126-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-187">False</span></span>                             |
| <span data-ttu-id="a1126-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1126-188">In Global Catalog</span></span>      | <span data-ttu-id="a1126-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-189">False</span></span>                             |
| <span data-ttu-id="a1126-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1126-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1126-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1126-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a1126-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1126-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a1126-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1126-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a1126-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-194">Search-Flags</span></span>           | <span data-ttu-id="a1126-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1126-195">0x00000000</span></span>                        |
| <span data-ttu-id="a1126-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-196">System-Flags</span></span>           | <span data-ttu-id="a1126-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-197">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1126-198">Classes used in</span></span>        | [<span data-ttu-id="a1126-199">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a1126-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1126-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1126-200">Windows Server 2008</span></span>



| <span data-ttu-id="a1126-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-201">Entry</span></span> | <span data-ttu-id="a1126-202">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a1126-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1126-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1126-205">System-Only</span></span>            | <span data-ttu-id="a1126-206">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-206">False</span></span>                             |
| <span data-ttu-id="a1126-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1126-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a1126-208">True</span><span class="sxs-lookup"><span data-stu-id="a1126-208">True</span></span>                              |
| <span data-ttu-id="a1126-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1126-209">Is Indexed</span></span>             | <span data-ttu-id="a1126-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-210">False</span></span>                             |
| <span data-ttu-id="a1126-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1126-211">In Global Catalog</span></span>      | <span data-ttu-id="a1126-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-212">False</span></span>                             |
| <span data-ttu-id="a1126-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1126-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1126-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1126-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a1126-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1126-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a1126-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1126-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a1126-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-217">Search-Flags</span></span>           | <span data-ttu-id="a1126-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-218">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-219">System-Flags</span></span>           | <span data-ttu-id="a1126-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-220">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1126-221">Classes used in</span></span>        | [<span data-ttu-id="a1126-222">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a1126-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1126-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1126-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1126-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-224">Entry</span></span> | <span data-ttu-id="a1126-225">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a1126-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1126-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1126-228">System-Only</span></span>            | <span data-ttu-id="a1126-229">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-229">False</span></span>                             |
| <span data-ttu-id="a1126-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1126-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a1126-231">True</span><span class="sxs-lookup"><span data-stu-id="a1126-231">True</span></span>                              |
| <span data-ttu-id="a1126-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1126-232">Is Indexed</span></span>             | <span data-ttu-id="a1126-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-233">False</span></span>                             |
| <span data-ttu-id="a1126-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1126-234">In Global Catalog</span></span>      | <span data-ttu-id="a1126-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-235">False</span></span>                             |
| <span data-ttu-id="a1126-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1126-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1126-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1126-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a1126-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1126-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a1126-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1126-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a1126-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-240">Search-Flags</span></span>           | <span data-ttu-id="a1126-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-241">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-242">System-Flags</span></span>           | <span data-ttu-id="a1126-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-243">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1126-244">Classes used in</span></span>        | [<span data-ttu-id="a1126-245">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a1126-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1126-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1126-246">Windows Server 2012</span></span>



| <span data-ttu-id="a1126-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1126-247">Entry</span></span> | <span data-ttu-id="a1126-248">Valor</span><span class="sxs-lookup"><span data-stu-id="a1126-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a1126-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1126-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1126-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a1126-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1126-251">System-Only</span></span>            | <span data-ttu-id="a1126-252">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-252">False</span></span>                             |
| <span data-ttu-id="a1126-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1126-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a1126-254">True</span><span class="sxs-lookup"><span data-stu-id="a1126-254">True</span></span>                              |
| <span data-ttu-id="a1126-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1126-255">Is Indexed</span></span>             | <span data-ttu-id="a1126-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-256">False</span></span>                             |
| <span data-ttu-id="a1126-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1126-257">In Global Catalog</span></span>      | <span data-ttu-id="a1126-258">Falso</span><span class="sxs-lookup"><span data-stu-id="a1126-258">False</span></span>                             |
| <span data-ttu-id="a1126-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1126-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1126-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1126-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a1126-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1126-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a1126-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1126-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a1126-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-263">Search-Flags</span></span>           | <span data-ttu-id="a1126-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-264">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1126-265">System-Flags</span></span>           | <span data-ttu-id="a1126-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1126-266">0x00000010</span></span>                        |
| <span data-ttu-id="a1126-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1126-267">Classes used in</span></span>        | [<span data-ttu-id="a1126-268">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a1126-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="a1126-269">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1126-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1126-270">Funções de administração de RAS</span><span class="sxs-lookup"><span data-stu-id="a1126-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 

