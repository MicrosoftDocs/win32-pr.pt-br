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
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="f29c0-104">atributo msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="f29c0-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="f29c0-105">Indica se a conta tem permissão para fazer a conexão com o servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="f29c0-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="f29c0-106">Não modifique esse valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="f29c0-106">Do not modify this value directly.</span></span> <span data-ttu-id="f29c0-107">Use a [função de administração RAS](/windows/desktop/RRAS/ras-administration-functions) apropriada para modificar esse valor.</span><span class="sxs-lookup"><span data-stu-id="f29c0-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="f29c0-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-108">Entry</span></span> | <span data-ttu-id="f29c0-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f29c0-110">CN</span><span class="sxs-lookup"><span data-stu-id="f29c0-110">CN</span></span>                | <span data-ttu-id="f29c0-111">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="f29c0-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="f29c0-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f29c0-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f29c0-113">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="f29c0-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="f29c0-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f29c0-114">Size</span></span>              | <span data-ttu-id="f29c0-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f29c0-115">4 bytes</span></span>                              |
| <span data-ttu-id="f29c0-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f29c0-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f29c0-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f29c0-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f29c0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-118">Attribute-Id</span></span>      | <span data-ttu-id="f29c0-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="f29c0-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="f29c0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f29c0-120">System-Id-Guid</span></span>    | <span data-ttu-id="f29c0-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="f29c0-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="f29c0-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f29c0-122">Syntax</span></span>            | [<span data-ttu-id="f29c0-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f29c0-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="f29c0-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f29c0-124">Implementations</span></span>

-   [<span data-ttu-id="f29c0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f29c0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f29c0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f29c0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f29c0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f29c0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f29c0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f29c0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f29c0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f29c0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f29c0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f29c0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f29c0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f29c0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f29c0-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-132">Entry</span></span> | <span data-ttu-id="f29c0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f29c0-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f29c0-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29c0-136">System-Only</span></span>            | <span data-ttu-id="f29c0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-137">False</span></span>                             |
| <span data-ttu-id="f29c0-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f29c0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f29c0-139">True</span><span class="sxs-lookup"><span data-stu-id="f29c0-139">True</span></span>                              |
| <span data-ttu-id="f29c0-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f29c0-140">Is Indexed</span></span>             | <span data-ttu-id="f29c0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-141">False</span></span>                             |
| <span data-ttu-id="f29c0-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f29c0-142">In Global Catalog</span></span>      | <span data-ttu-id="f29c0-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-143">False</span></span>                             |
| <span data-ttu-id="f29c0-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f29c0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29c0-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f29c0-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f29c0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29c0-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f29c0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29c0-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f29c0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-148">Search-Flags</span></span>           | <span data-ttu-id="f29c0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29c0-149">0x00000000</span></span>                        |
| <span data-ttu-id="f29c0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-150">System-Flags</span></span>           | <span data-ttu-id="f29c0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-151">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f29c0-152">Classes used in</span></span>        | [<span data-ttu-id="f29c0-153">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f29c0-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f29c0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f29c0-154">Windows Server 2003</span></span>



| <span data-ttu-id="f29c0-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-155">Entry</span></span> | <span data-ttu-id="f29c0-156">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f29c0-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="f29c0-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29c0-159">System-Only</span></span>            | <span data-ttu-id="f29c0-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-160">False</span></span>                             |
| <span data-ttu-id="f29c0-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f29c0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f29c0-162">True</span><span class="sxs-lookup"><span data-stu-id="f29c0-162">True</span></span>                              |
| <span data-ttu-id="f29c0-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="f29c0-163">Is Indexed</span></span>             | <span data-ttu-id="f29c0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-164">False</span></span>                             |
| <span data-ttu-id="f29c0-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f29c0-165">In Global Catalog</span></span>      | <span data-ttu-id="f29c0-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-166">False</span></span>                             |
| <span data-ttu-id="f29c0-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f29c0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29c0-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f29c0-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f29c0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29c0-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f29c0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29c0-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f29c0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-171">Search-Flags</span></span>           | <span data-ttu-id="f29c0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29c0-172">0x00000000</span></span>                        |
| <span data-ttu-id="f29c0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-173">System-Flags</span></span>           | <span data-ttu-id="f29c0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-174">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f29c0-175">Classes used in</span></span>        | [<span data-ttu-id="f29c0-176">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f29c0-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f29c0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f29c0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f29c0-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-178">Entry</span></span> | <span data-ttu-id="f29c0-179">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f29c0-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="f29c0-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29c0-182">System-Only</span></span>            | <span data-ttu-id="f29c0-183">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-183">False</span></span>                             |
| <span data-ttu-id="f29c0-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f29c0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f29c0-185">True</span><span class="sxs-lookup"><span data-stu-id="f29c0-185">True</span></span>                              |
| <span data-ttu-id="f29c0-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="f29c0-186">Is Indexed</span></span>             | <span data-ttu-id="f29c0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-187">False</span></span>                             |
| <span data-ttu-id="f29c0-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f29c0-188">In Global Catalog</span></span>      | <span data-ttu-id="f29c0-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-189">False</span></span>                             |
| <span data-ttu-id="f29c0-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f29c0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29c0-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f29c0-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f29c0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29c0-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f29c0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29c0-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f29c0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-194">Search-Flags</span></span>           | <span data-ttu-id="f29c0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f29c0-195">0x00000000</span></span>                        |
| <span data-ttu-id="f29c0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-196">System-Flags</span></span>           | <span data-ttu-id="f29c0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-197">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f29c0-198">Classes used in</span></span>        | [<span data-ttu-id="f29c0-199">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f29c0-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f29c0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f29c0-200">Windows Server 2008</span></span>



| <span data-ttu-id="f29c0-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-201">Entry</span></span> | <span data-ttu-id="f29c0-202">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f29c0-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="f29c0-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29c0-205">System-Only</span></span>            | <span data-ttu-id="f29c0-206">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-206">False</span></span>                             |
| <span data-ttu-id="f29c0-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f29c0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f29c0-208">True</span><span class="sxs-lookup"><span data-stu-id="f29c0-208">True</span></span>                              |
| <span data-ttu-id="f29c0-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="f29c0-209">Is Indexed</span></span>             | <span data-ttu-id="f29c0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-210">False</span></span>                             |
| <span data-ttu-id="f29c0-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f29c0-211">In Global Catalog</span></span>      | <span data-ttu-id="f29c0-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-212">False</span></span>                             |
| <span data-ttu-id="f29c0-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f29c0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29c0-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f29c0-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f29c0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29c0-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f29c0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29c0-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f29c0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-217">Search-Flags</span></span>           | <span data-ttu-id="f29c0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-218">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-219">System-Flags</span></span>           | <span data-ttu-id="f29c0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-220">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f29c0-221">Classes used in</span></span>        | [<span data-ttu-id="f29c0-222">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f29c0-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f29c0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f29c0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f29c0-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-224">Entry</span></span> | <span data-ttu-id="f29c0-225">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f29c0-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="f29c0-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29c0-228">System-Only</span></span>            | <span data-ttu-id="f29c0-229">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-229">False</span></span>                             |
| <span data-ttu-id="f29c0-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f29c0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f29c0-231">True</span><span class="sxs-lookup"><span data-stu-id="f29c0-231">True</span></span>                              |
| <span data-ttu-id="f29c0-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="f29c0-232">Is Indexed</span></span>             | <span data-ttu-id="f29c0-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-233">False</span></span>                             |
| <span data-ttu-id="f29c0-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f29c0-234">In Global Catalog</span></span>      | <span data-ttu-id="f29c0-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-235">False</span></span>                             |
| <span data-ttu-id="f29c0-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f29c0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29c0-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f29c0-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f29c0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29c0-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f29c0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29c0-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f29c0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-240">Search-Flags</span></span>           | <span data-ttu-id="f29c0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-241">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-242">System-Flags</span></span>           | <span data-ttu-id="f29c0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-243">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f29c0-244">Classes used in</span></span>        | [<span data-ttu-id="f29c0-245">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f29c0-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f29c0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f29c0-246">Windows Server 2012</span></span>



| <span data-ttu-id="f29c0-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="f29c0-247">Entry</span></span> | <span data-ttu-id="f29c0-248">Valor</span><span class="sxs-lookup"><span data-stu-id="f29c0-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f29c0-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="f29c0-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f29c0-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f29c0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f29c0-251">System-Only</span></span>            | <span data-ttu-id="f29c0-252">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-252">False</span></span>                             |
| <span data-ttu-id="f29c0-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f29c0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f29c0-254">True</span><span class="sxs-lookup"><span data-stu-id="f29c0-254">True</span></span>                              |
| <span data-ttu-id="f29c0-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="f29c0-255">Is Indexed</span></span>             | <span data-ttu-id="f29c0-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-256">False</span></span>                             |
| <span data-ttu-id="f29c0-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f29c0-257">In Global Catalog</span></span>      | <span data-ttu-id="f29c0-258">Falso</span><span class="sxs-lookup"><span data-stu-id="f29c0-258">False</span></span>                             |
| <span data-ttu-id="f29c0-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f29c0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f29c0-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f29c0-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f29c0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f29c0-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f29c0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f29c0-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f29c0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-263">Search-Flags</span></span>           | <span data-ttu-id="f29c0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-264">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f29c0-265">System-Flags</span></span>           | <span data-ttu-id="f29c0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f29c0-266">0x00000010</span></span>                        |
| <span data-ttu-id="f29c0-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f29c0-267">Classes used in</span></span>        | [<span data-ttu-id="f29c0-268">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f29c0-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="f29c0-269">Confira também</span><span class="sxs-lookup"><span data-stu-id="f29c0-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29c0-270">Funções de administração de RAS</span><span class="sxs-lookup"><span data-stu-id="f29c0-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 

