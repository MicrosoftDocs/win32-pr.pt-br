---
title: Atributo Primary-Group-token
description: Um atributo calculado que é usado na recuperação da lista de membros de um grupo, como usuários de domínio. A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Grupo de identificadores primários de atributos de token
- Esquema de AD do atributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086865"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="840cf-106">Atributo Primary-Group-token</span><span class="sxs-lookup"><span data-stu-id="840cf-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="840cf-107">Um atributo calculado que é usado na recuperação da lista de membros de um grupo, como usuários de domínio.</span><span class="sxs-lookup"><span data-stu-id="840cf-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="840cf-108">A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="840cf-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="840cf-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-109">Entry</span></span> | <span data-ttu-id="840cf-110">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="840cf-111">CN</span><span class="sxs-lookup"><span data-stu-id="840cf-111">CN</span></span>                | <span data-ttu-id="840cf-112">Token de grupo primário</span><span class="sxs-lookup"><span data-stu-id="840cf-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="840cf-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="840cf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="840cf-114">primaryGroupToken</span><span class="sxs-lookup"><span data-stu-id="840cf-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="840cf-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="840cf-115">Size</span></span>              | <span data-ttu-id="840cf-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="840cf-116">4 bytes</span></span>                                    |
| <span data-ttu-id="840cf-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="840cf-117">Update Privilege</span></span>  | <span data-ttu-id="840cf-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="840cf-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="840cf-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="840cf-119">Update Frequency</span></span>  | <span data-ttu-id="840cf-120">Sempre que um grupo primário de objetos é alterado.</span><span class="sxs-lookup"><span data-stu-id="840cf-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="840cf-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-121">Attribute-Id</span></span>      | <span data-ttu-id="840cf-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="840cf-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="840cf-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="840cf-123">System-Id-Guid</span></span>    | <span data-ttu-id="840cf-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="840cf-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="840cf-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="840cf-125">Syntax</span></span>            | [<span data-ttu-id="840cf-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="840cf-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="840cf-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="840cf-127">Implementations</span></span>

-   [<span data-ttu-id="840cf-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="840cf-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="840cf-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="840cf-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="840cf-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="840cf-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="840cf-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="840cf-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="840cf-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="840cf-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="840cf-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="840cf-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="840cf-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="840cf-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="840cf-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="840cf-135">Windows 2000 Server</span></span>



| <span data-ttu-id="840cf-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-136">Entry</span></span> | <span data-ttu-id="840cf-137">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-140">System-Only</span></span>            | <span data-ttu-id="840cf-141">True</span><span class="sxs-lookup"><span data-stu-id="840cf-141">True</span></span>                                |
| <span data-ttu-id="840cf-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-142">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-143">True</span><span class="sxs-lookup"><span data-stu-id="840cf-143">True</span></span>                                |
| <span data-ttu-id="840cf-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-144">Is Indexed</span></span>             | <span data-ttu-id="840cf-145">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-145">False</span></span>                               |
| <span data-ttu-id="840cf-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-146">In Global Catalog</span></span>      | <span data-ttu-id="840cf-147">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-147">False</span></span>                               |
| <span data-ttu-id="840cf-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-152">Search-Flags</span></span>           | <span data-ttu-id="840cf-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-153">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-154">System-Flags</span></span>           | <span data-ttu-id="840cf-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-155">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-156">Classes used in</span></span>        | [<span data-ttu-id="840cf-157">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="840cf-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="840cf-158">Windows Server 2003</span></span>



| <span data-ttu-id="840cf-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-159">Entry</span></span> | <span data-ttu-id="840cf-160">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-163">System-Only</span></span>            | <span data-ttu-id="840cf-164">True</span><span class="sxs-lookup"><span data-stu-id="840cf-164">True</span></span>                                |
| <span data-ttu-id="840cf-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-165">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-166">True</span><span class="sxs-lookup"><span data-stu-id="840cf-166">True</span></span>                                |
| <span data-ttu-id="840cf-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-167">Is Indexed</span></span>             | <span data-ttu-id="840cf-168">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-168">False</span></span>                               |
| <span data-ttu-id="840cf-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-169">In Global Catalog</span></span>      | <span data-ttu-id="840cf-170">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-170">False</span></span>                               |
| <span data-ttu-id="840cf-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-175">Search-Flags</span></span>           | <span data-ttu-id="840cf-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-176">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-177">System-Flags</span></span>           | <span data-ttu-id="840cf-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-178">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-179">Classes used in</span></span>        | [<span data-ttu-id="840cf-180">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="840cf-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="840cf-181">ADAM</span></span>



| <span data-ttu-id="840cf-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-182">Entry</span></span> | <span data-ttu-id="840cf-183">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-186">System-Only</span></span>            | <span data-ttu-id="840cf-187">True</span><span class="sxs-lookup"><span data-stu-id="840cf-187">True</span></span>                                |
| <span data-ttu-id="840cf-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-188">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-189">True</span><span class="sxs-lookup"><span data-stu-id="840cf-189">True</span></span>                                |
| <span data-ttu-id="840cf-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-190">Is Indexed</span></span>             | <span data-ttu-id="840cf-191">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-191">False</span></span>                               |
| <span data-ttu-id="840cf-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-192">In Global Catalog</span></span>      | <span data-ttu-id="840cf-193">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-193">False</span></span>                               |
| <span data-ttu-id="840cf-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-198">Search-Flags</span></span>           | <span data-ttu-id="840cf-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-199">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-200">System-Flags</span></span>           | <span data-ttu-id="840cf-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-201">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-202">Classes used in</span></span>        | [<span data-ttu-id="840cf-203">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="840cf-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="840cf-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="840cf-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-205">Entry</span></span> | <span data-ttu-id="840cf-206">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-209">System-Only</span></span>            | <span data-ttu-id="840cf-210">True</span><span class="sxs-lookup"><span data-stu-id="840cf-210">True</span></span>                                |
| <span data-ttu-id="840cf-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-211">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-212">True</span><span class="sxs-lookup"><span data-stu-id="840cf-212">True</span></span>                                |
| <span data-ttu-id="840cf-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-213">Is Indexed</span></span>             | <span data-ttu-id="840cf-214">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-214">False</span></span>                               |
| <span data-ttu-id="840cf-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-215">In Global Catalog</span></span>      | <span data-ttu-id="840cf-216">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-216">False</span></span>                               |
| <span data-ttu-id="840cf-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-221">Search-Flags</span></span>           | <span data-ttu-id="840cf-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-222">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-223">System-Flags</span></span>           | <span data-ttu-id="840cf-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-224">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-225">Classes used in</span></span>        | [<span data-ttu-id="840cf-226">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="840cf-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="840cf-227">Windows Server 2008</span></span>



| <span data-ttu-id="840cf-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-228">Entry</span></span> | <span data-ttu-id="840cf-229">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-232">System-Only</span></span>            | <span data-ttu-id="840cf-233">True</span><span class="sxs-lookup"><span data-stu-id="840cf-233">True</span></span>                                |
| <span data-ttu-id="840cf-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-234">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-235">True</span><span class="sxs-lookup"><span data-stu-id="840cf-235">True</span></span>                                |
| <span data-ttu-id="840cf-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-236">Is Indexed</span></span>             | <span data-ttu-id="840cf-237">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-237">False</span></span>                               |
| <span data-ttu-id="840cf-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-238">In Global Catalog</span></span>      | <span data-ttu-id="840cf-239">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-239">False</span></span>                               |
| <span data-ttu-id="840cf-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-244">Search-Flags</span></span>           | <span data-ttu-id="840cf-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-245">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-246">System-Flags</span></span>           | <span data-ttu-id="840cf-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-247">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-248">Classes used in</span></span>        | [<span data-ttu-id="840cf-249">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="840cf-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="840cf-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="840cf-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-251">Entry</span></span> | <span data-ttu-id="840cf-252">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-255">System-Only</span></span>            | <span data-ttu-id="840cf-256">True</span><span class="sxs-lookup"><span data-stu-id="840cf-256">True</span></span>                                |
| <span data-ttu-id="840cf-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-257">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-258">True</span><span class="sxs-lookup"><span data-stu-id="840cf-258">True</span></span>                                |
| <span data-ttu-id="840cf-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-259">Is Indexed</span></span>             | <span data-ttu-id="840cf-260">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-260">False</span></span>                               |
| <span data-ttu-id="840cf-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-261">In Global Catalog</span></span>      | <span data-ttu-id="840cf-262">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-262">False</span></span>                               |
| <span data-ttu-id="840cf-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-267">Search-Flags</span></span>           | <span data-ttu-id="840cf-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-268">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-269">System-Flags</span></span>           | <span data-ttu-id="840cf-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-270">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-271">Classes used in</span></span>        | [<span data-ttu-id="840cf-272">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="840cf-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="840cf-273">Windows Server 2012</span></span>



| <span data-ttu-id="840cf-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="840cf-274">Entry</span></span> | <span data-ttu-id="840cf-275">Valor</span><span class="sxs-lookup"><span data-stu-id="840cf-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="840cf-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="840cf-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="840cf-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="840cf-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="840cf-278">System-Only</span></span>            | <span data-ttu-id="840cf-279">True</span><span class="sxs-lookup"><span data-stu-id="840cf-279">True</span></span>                                |
| <span data-ttu-id="840cf-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="840cf-280">Is-Single-Valued</span></span>       | <span data-ttu-id="840cf-281">True</span><span class="sxs-lookup"><span data-stu-id="840cf-281">True</span></span>                                |
| <span data-ttu-id="840cf-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="840cf-282">Is Indexed</span></span>             | <span data-ttu-id="840cf-283">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-283">False</span></span>                               |
| <span data-ttu-id="840cf-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="840cf-284">In Global Catalog</span></span>      | <span data-ttu-id="840cf-285">Falso</span><span class="sxs-lookup"><span data-stu-id="840cf-285">False</span></span>                               |
| <span data-ttu-id="840cf-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="840cf-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="840cf-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="840cf-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="840cf-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="840cf-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="840cf-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="840cf-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="840cf-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-290">Search-Flags</span></span>           | <span data-ttu-id="840cf-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="840cf-291">0x00000000</span></span>                          |
| <span data-ttu-id="840cf-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="840cf-292">System-Flags</span></span>           | <span data-ttu-id="840cf-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="840cf-293">0x00000014</span></span>                          |
| <span data-ttu-id="840cf-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="840cf-294">Classes used in</span></span>        | [<span data-ttu-id="840cf-295">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="840cf-295">**Group**</span></span>](c-group.md)<br/> |



 

 





