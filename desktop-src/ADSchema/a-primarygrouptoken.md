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
# <a name="primary-group-token-attribute"></a><span data-ttu-id="023f9-106">Atributo Primary-Group-token</span><span class="sxs-lookup"><span data-stu-id="023f9-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="023f9-107">Um atributo calculado que é usado na recuperação da lista de membros de um grupo, como usuários de domínio.</span><span class="sxs-lookup"><span data-stu-id="023f9-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="023f9-108">A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="023f9-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="023f9-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-109">Entry</span></span> | <span data-ttu-id="023f9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="023f9-111">CN</span><span class="sxs-lookup"><span data-stu-id="023f9-111">CN</span></span>                | <span data-ttu-id="023f9-112">Token de grupo primário</span><span class="sxs-lookup"><span data-stu-id="023f9-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="023f9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="023f9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="023f9-114">primaryGroupToken</span><span class="sxs-lookup"><span data-stu-id="023f9-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="023f9-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="023f9-115">Size</span></span>              | <span data-ttu-id="023f9-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="023f9-116">4 bytes</span></span>                                    |
| <span data-ttu-id="023f9-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="023f9-117">Update Privilege</span></span>  | <span data-ttu-id="023f9-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="023f9-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="023f9-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="023f9-119">Update Frequency</span></span>  | <span data-ttu-id="023f9-120">Sempre que um grupo primário de objetos é alterado.</span><span class="sxs-lookup"><span data-stu-id="023f9-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="023f9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-121">Attribute-Id</span></span>      | <span data-ttu-id="023f9-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="023f9-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="023f9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="023f9-123">System-Id-Guid</span></span>    | <span data-ttu-id="023f9-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="023f9-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="023f9-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="023f9-125">Syntax</span></span>            | [<span data-ttu-id="023f9-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="023f9-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="023f9-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="023f9-127">Implementations</span></span>

-   [<span data-ttu-id="023f9-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="023f9-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="023f9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="023f9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="023f9-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="023f9-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="023f9-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="023f9-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="023f9-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="023f9-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="023f9-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="023f9-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="023f9-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="023f9-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="023f9-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="023f9-135">Windows 2000 Server</span></span>



| <span data-ttu-id="023f9-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-136">Entry</span></span> | <span data-ttu-id="023f9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-140">System-Only</span></span>            | <span data-ttu-id="023f9-141">True</span><span class="sxs-lookup"><span data-stu-id="023f9-141">True</span></span>                                |
| <span data-ttu-id="023f9-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-142">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-143">True</span><span class="sxs-lookup"><span data-stu-id="023f9-143">True</span></span>                                |
| <span data-ttu-id="023f9-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-144">Is Indexed</span></span>             | <span data-ttu-id="023f9-145">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-145">False</span></span>                               |
| <span data-ttu-id="023f9-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-146">In Global Catalog</span></span>      | <span data-ttu-id="023f9-147">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-147">False</span></span>                               |
| <span data-ttu-id="023f9-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-152">Search-Flags</span></span>           | <span data-ttu-id="023f9-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-153">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-154">System-Flags</span></span>           | <span data-ttu-id="023f9-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-155">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-156">Classes used in</span></span>        | [<span data-ttu-id="023f9-157">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="023f9-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="023f9-158">Windows Server 2003</span></span>



| <span data-ttu-id="023f9-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-159">Entry</span></span> | <span data-ttu-id="023f9-160">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-163">System-Only</span></span>            | <span data-ttu-id="023f9-164">True</span><span class="sxs-lookup"><span data-stu-id="023f9-164">True</span></span>                                |
| <span data-ttu-id="023f9-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-165">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-166">True</span><span class="sxs-lookup"><span data-stu-id="023f9-166">True</span></span>                                |
| <span data-ttu-id="023f9-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-167">Is Indexed</span></span>             | <span data-ttu-id="023f9-168">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-168">False</span></span>                               |
| <span data-ttu-id="023f9-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-169">In Global Catalog</span></span>      | <span data-ttu-id="023f9-170">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-170">False</span></span>                               |
| <span data-ttu-id="023f9-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-175">Search-Flags</span></span>           | <span data-ttu-id="023f9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-176">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-177">System-Flags</span></span>           | <span data-ttu-id="023f9-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-178">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-179">Classes used in</span></span>        | [<span data-ttu-id="023f9-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="023f9-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="023f9-181">ADAM</span></span>



| <span data-ttu-id="023f9-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-182">Entry</span></span> | <span data-ttu-id="023f9-183">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-186">System-Only</span></span>            | <span data-ttu-id="023f9-187">True</span><span class="sxs-lookup"><span data-stu-id="023f9-187">True</span></span>                                |
| <span data-ttu-id="023f9-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-189">True</span><span class="sxs-lookup"><span data-stu-id="023f9-189">True</span></span>                                |
| <span data-ttu-id="023f9-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-190">Is Indexed</span></span>             | <span data-ttu-id="023f9-191">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-191">False</span></span>                               |
| <span data-ttu-id="023f9-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-192">In Global Catalog</span></span>      | <span data-ttu-id="023f9-193">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-193">False</span></span>                               |
| <span data-ttu-id="023f9-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-198">Search-Flags</span></span>           | <span data-ttu-id="023f9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-199">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-200">System-Flags</span></span>           | <span data-ttu-id="023f9-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-201">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-202">Classes used in</span></span>        | [<span data-ttu-id="023f9-203">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="023f9-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="023f9-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="023f9-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-205">Entry</span></span> | <span data-ttu-id="023f9-206">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-209">System-Only</span></span>            | <span data-ttu-id="023f9-210">True</span><span class="sxs-lookup"><span data-stu-id="023f9-210">True</span></span>                                |
| <span data-ttu-id="023f9-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-211">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-212">True</span><span class="sxs-lookup"><span data-stu-id="023f9-212">True</span></span>                                |
| <span data-ttu-id="023f9-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-213">Is Indexed</span></span>             | <span data-ttu-id="023f9-214">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-214">False</span></span>                               |
| <span data-ttu-id="023f9-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-215">In Global Catalog</span></span>      | <span data-ttu-id="023f9-216">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-216">False</span></span>                               |
| <span data-ttu-id="023f9-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-221">Search-Flags</span></span>           | <span data-ttu-id="023f9-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-222">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-223">System-Flags</span></span>           | <span data-ttu-id="023f9-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-224">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-225">Classes used in</span></span>        | [<span data-ttu-id="023f9-226">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="023f9-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="023f9-227">Windows Server 2008</span></span>



| <span data-ttu-id="023f9-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-228">Entry</span></span> | <span data-ttu-id="023f9-229">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-232">System-Only</span></span>            | <span data-ttu-id="023f9-233">True</span><span class="sxs-lookup"><span data-stu-id="023f9-233">True</span></span>                                |
| <span data-ttu-id="023f9-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-234">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-235">True</span><span class="sxs-lookup"><span data-stu-id="023f9-235">True</span></span>                                |
| <span data-ttu-id="023f9-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-236">Is Indexed</span></span>             | <span data-ttu-id="023f9-237">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-237">False</span></span>                               |
| <span data-ttu-id="023f9-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-238">In Global Catalog</span></span>      | <span data-ttu-id="023f9-239">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-239">False</span></span>                               |
| <span data-ttu-id="023f9-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-244">Search-Flags</span></span>           | <span data-ttu-id="023f9-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-245">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-246">System-Flags</span></span>           | <span data-ttu-id="023f9-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-247">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-248">Classes used in</span></span>        | [<span data-ttu-id="023f9-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="023f9-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="023f9-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="023f9-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-251">Entry</span></span> | <span data-ttu-id="023f9-252">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-255">System-Only</span></span>            | <span data-ttu-id="023f9-256">True</span><span class="sxs-lookup"><span data-stu-id="023f9-256">True</span></span>                                |
| <span data-ttu-id="023f9-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-257">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-258">True</span><span class="sxs-lookup"><span data-stu-id="023f9-258">True</span></span>                                |
| <span data-ttu-id="023f9-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-259">Is Indexed</span></span>             | <span data-ttu-id="023f9-260">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-260">False</span></span>                               |
| <span data-ttu-id="023f9-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-261">In Global Catalog</span></span>      | <span data-ttu-id="023f9-262">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-262">False</span></span>                               |
| <span data-ttu-id="023f9-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-267">Search-Flags</span></span>           | <span data-ttu-id="023f9-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-268">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-269">System-Flags</span></span>           | <span data-ttu-id="023f9-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-270">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-271">Classes used in</span></span>        | [<span data-ttu-id="023f9-272">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="023f9-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="023f9-273">Windows Server 2012</span></span>



| <span data-ttu-id="023f9-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="023f9-274">Entry</span></span> | <span data-ttu-id="023f9-275">Valor</span><span class="sxs-lookup"><span data-stu-id="023f9-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="023f9-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="023f9-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="023f9-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="023f9-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="023f9-278">System-Only</span></span>            | <span data-ttu-id="023f9-279">True</span><span class="sxs-lookup"><span data-stu-id="023f9-279">True</span></span>                                |
| <span data-ttu-id="023f9-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="023f9-280">Is-Single-Valued</span></span>       | <span data-ttu-id="023f9-281">True</span><span class="sxs-lookup"><span data-stu-id="023f9-281">True</span></span>                                |
| <span data-ttu-id="023f9-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="023f9-282">Is Indexed</span></span>             | <span data-ttu-id="023f9-283">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-283">False</span></span>                               |
| <span data-ttu-id="023f9-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="023f9-284">In Global Catalog</span></span>      | <span data-ttu-id="023f9-285">Falso</span><span class="sxs-lookup"><span data-stu-id="023f9-285">False</span></span>                               |
| <span data-ttu-id="023f9-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="023f9-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="023f9-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="023f9-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="023f9-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="023f9-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="023f9-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="023f9-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="023f9-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-290">Search-Flags</span></span>           | <span data-ttu-id="023f9-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="023f9-291">0x00000000</span></span>                          |
| <span data-ttu-id="023f9-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="023f9-292">System-Flags</span></span>           | <span data-ttu-id="023f9-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="023f9-293">0x00000014</span></span>                          |
| <span data-ttu-id="023f9-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="023f9-294">Classes used in</span></span>        | [<span data-ttu-id="023f9-295">**Group**</span><span class="sxs-lookup"><span data-stu-id="023f9-295">**Group**</span></span>](c-group.md)<br/> |



 

 





