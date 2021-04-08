---
title: netboot-somente resposta-atributo de clientes válidos
description: Determina se o servidor responde a todos os computadores cliente ou somente em pré-teste.
ms.assetid: b02438ba-11b3-497c-b57f-bd9a0045e6b0
ms.tgt_platform: multiple
keywords:
- netboot-somente resposta-esquema do AD do atributo válido-clients
- Esquema de AD do atributo netbootAnswerOnlyValidClients
topic_type:
- apiref
api_name:
- netboot-Answer-Only-Valid-Clients
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e28f7ecfaa569f47d79249606029760b914b5ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086881"
---
# <a name="netboot-answer-only-valid-clients-attribute"></a><span data-ttu-id="400ca-105">netboot-somente resposta-atributo de clientes válidos</span><span class="sxs-lookup"><span data-stu-id="400ca-105">netboot-Answer-Only-Valid-Clients attribute</span></span>

<span data-ttu-id="400ca-106">Determina se o servidor responde a todos os computadores cliente ou somente em pré-teste.</span><span class="sxs-lookup"><span data-stu-id="400ca-106">Determines whether the server answers all, or only pre-staged, client computers.</span></span>



| <span data-ttu-id="400ca-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-107">Entry</span></span> | <span data-ttu-id="400ca-108">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="400ca-109">CN</span><span class="sxs-lookup"><span data-stu-id="400ca-109">CN</span></span>                | <span data-ttu-id="400ca-110">netboot-somente resposta-clientes válidos</span><span class="sxs-lookup"><span data-stu-id="400ca-110">netboot-Answer-Only-Valid-Clients</span></span>    |
| <span data-ttu-id="400ca-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="400ca-111">Ldap-Display-Name</span></span> | <span data-ttu-id="400ca-112">netbootAnswerOnlyValidClients</span><span class="sxs-lookup"><span data-stu-id="400ca-112">netbootAnswerOnlyValidClients</span></span>        |
| <span data-ttu-id="400ca-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="400ca-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="400ca-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="400ca-114">Update Privilege</span></span>  | <span data-ttu-id="400ca-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="400ca-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="400ca-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="400ca-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="400ca-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-117">Attribute-Id</span></span>      | <span data-ttu-id="400ca-118">1.2.840.113556.1.4.854</span><span class="sxs-lookup"><span data-stu-id="400ca-118">1.2.840.113556.1.4.854</span></span>               |
| <span data-ttu-id="400ca-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="400ca-119">System-Id-Guid</span></span>    | <span data-ttu-id="400ca-120">0738307b-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="400ca-120">0738307b-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="400ca-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="400ca-121">Syntax</span></span>            | [<span data-ttu-id="400ca-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="400ca-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="400ca-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="400ca-123">Implementations</span></span>

-   [<span data-ttu-id="400ca-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="400ca-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="400ca-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="400ca-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="400ca-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="400ca-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="400ca-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="400ca-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="400ca-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="400ca-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="400ca-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="400ca-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="400ca-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="400ca-130">Windows 2000 Server</span></span>



| <span data-ttu-id="400ca-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-131">Entry</span></span> | <span data-ttu-id="400ca-132">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="400ca-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="400ca-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="400ca-135">System-Only</span></span>            | <span data-ttu-id="400ca-136">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-136">False</span></span>                                                      |
| <span data-ttu-id="400ca-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="400ca-137">Is-Single-Valued</span></span>       | <span data-ttu-id="400ca-138">True</span><span class="sxs-lookup"><span data-stu-id="400ca-138">True</span></span>                                                       |
| <span data-ttu-id="400ca-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="400ca-139">Is Indexed</span></span>             | <span data-ttu-id="400ca-140">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-140">False</span></span>                                                      |
| <span data-ttu-id="400ca-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="400ca-141">In Global Catalog</span></span>      | <span data-ttu-id="400ca-142">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-142">False</span></span>                                                      |
| <span data-ttu-id="400ca-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="400ca-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="400ca-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="400ca-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="400ca-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="400ca-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="400ca-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-147">Search-Flags</span></span>           | <span data-ttu-id="400ca-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="400ca-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="400ca-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-149">System-Flags</span></span>           | <span data-ttu-id="400ca-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="400ca-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="400ca-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="400ca-151">Classes used in</span></span>        | [<span data-ttu-id="400ca-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="400ca-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="400ca-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="400ca-153">Windows Server 2003</span></span>



| <span data-ttu-id="400ca-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-154">Entry</span></span> | <span data-ttu-id="400ca-155">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="400ca-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="400ca-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="400ca-158">System-Only</span></span>            | <span data-ttu-id="400ca-159">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-159">False</span></span>                                                      |
| <span data-ttu-id="400ca-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="400ca-160">Is-Single-Valued</span></span>       | <span data-ttu-id="400ca-161">True</span><span class="sxs-lookup"><span data-stu-id="400ca-161">True</span></span>                                                       |
| <span data-ttu-id="400ca-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="400ca-162">Is Indexed</span></span>             | <span data-ttu-id="400ca-163">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-163">False</span></span>                                                      |
| <span data-ttu-id="400ca-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="400ca-164">In Global Catalog</span></span>      | <span data-ttu-id="400ca-165">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-165">False</span></span>                                                      |
| <span data-ttu-id="400ca-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="400ca-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="400ca-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="400ca-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="400ca-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="400ca-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="400ca-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-170">Search-Flags</span></span>           | <span data-ttu-id="400ca-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="400ca-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="400ca-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-172">System-Flags</span></span>           | <span data-ttu-id="400ca-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="400ca-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="400ca-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="400ca-174">Classes used in</span></span>        | [<span data-ttu-id="400ca-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="400ca-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="400ca-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="400ca-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="400ca-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-177">Entry</span></span> | <span data-ttu-id="400ca-178">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="400ca-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="400ca-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="400ca-181">System-Only</span></span>            | <span data-ttu-id="400ca-182">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-182">False</span></span>                                                      |
| <span data-ttu-id="400ca-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="400ca-183">Is-Single-Valued</span></span>       | <span data-ttu-id="400ca-184">True</span><span class="sxs-lookup"><span data-stu-id="400ca-184">True</span></span>                                                       |
| <span data-ttu-id="400ca-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="400ca-185">Is Indexed</span></span>             | <span data-ttu-id="400ca-186">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-186">False</span></span>                                                      |
| <span data-ttu-id="400ca-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="400ca-187">In Global Catalog</span></span>      | <span data-ttu-id="400ca-188">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-188">False</span></span>                                                      |
| <span data-ttu-id="400ca-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="400ca-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="400ca-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="400ca-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="400ca-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="400ca-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="400ca-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-193">Search-Flags</span></span>           | <span data-ttu-id="400ca-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="400ca-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="400ca-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-195">System-Flags</span></span>           | <span data-ttu-id="400ca-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="400ca-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="400ca-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="400ca-197">Classes used in</span></span>        | [<span data-ttu-id="400ca-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="400ca-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="400ca-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="400ca-199">Windows Server 2008</span></span>



| <span data-ttu-id="400ca-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-200">Entry</span></span> | <span data-ttu-id="400ca-201">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="400ca-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="400ca-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="400ca-204">System-Only</span></span>            | <span data-ttu-id="400ca-205">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-205">False</span></span>                                                      |
| <span data-ttu-id="400ca-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="400ca-206">Is-Single-Valued</span></span>       | <span data-ttu-id="400ca-207">True</span><span class="sxs-lookup"><span data-stu-id="400ca-207">True</span></span>                                                       |
| <span data-ttu-id="400ca-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="400ca-208">Is Indexed</span></span>             | <span data-ttu-id="400ca-209">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-209">False</span></span>                                                      |
| <span data-ttu-id="400ca-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="400ca-210">In Global Catalog</span></span>      | <span data-ttu-id="400ca-211">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-211">False</span></span>                                                      |
| <span data-ttu-id="400ca-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="400ca-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="400ca-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="400ca-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="400ca-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="400ca-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="400ca-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-216">Search-Flags</span></span>           | <span data-ttu-id="400ca-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="400ca-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="400ca-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-218">System-Flags</span></span>           | <span data-ttu-id="400ca-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="400ca-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="400ca-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="400ca-220">Classes used in</span></span>        | [<span data-ttu-id="400ca-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="400ca-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="400ca-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="400ca-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="400ca-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-223">Entry</span></span> | <span data-ttu-id="400ca-224">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="400ca-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="400ca-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="400ca-227">System-Only</span></span>            | <span data-ttu-id="400ca-228">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-228">False</span></span>                                                      |
| <span data-ttu-id="400ca-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="400ca-229">Is-Single-Valued</span></span>       | <span data-ttu-id="400ca-230">True</span><span class="sxs-lookup"><span data-stu-id="400ca-230">True</span></span>                                                       |
| <span data-ttu-id="400ca-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="400ca-231">Is Indexed</span></span>             | <span data-ttu-id="400ca-232">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-232">False</span></span>                                                      |
| <span data-ttu-id="400ca-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="400ca-233">In Global Catalog</span></span>      | <span data-ttu-id="400ca-234">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-234">False</span></span>                                                      |
| <span data-ttu-id="400ca-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="400ca-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="400ca-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="400ca-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="400ca-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="400ca-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="400ca-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-239">Search-Flags</span></span>           | <span data-ttu-id="400ca-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="400ca-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="400ca-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-241">System-Flags</span></span>           | <span data-ttu-id="400ca-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="400ca-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="400ca-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="400ca-243">Classes used in</span></span>        | [<span data-ttu-id="400ca-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="400ca-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="400ca-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="400ca-245">Windows Server 2012</span></span>



| <span data-ttu-id="400ca-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="400ca-246">Entry</span></span> | <span data-ttu-id="400ca-247">Valor</span><span class="sxs-lookup"><span data-stu-id="400ca-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="400ca-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="400ca-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="400ca-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="400ca-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="400ca-250">System-Only</span></span>            | <span data-ttu-id="400ca-251">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-251">False</span></span>                                                      |
| <span data-ttu-id="400ca-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="400ca-252">Is-Single-Valued</span></span>       | <span data-ttu-id="400ca-253">True</span><span class="sxs-lookup"><span data-stu-id="400ca-253">True</span></span>                                                       |
| <span data-ttu-id="400ca-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="400ca-254">Is Indexed</span></span>             | <span data-ttu-id="400ca-255">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-255">False</span></span>                                                      |
| <span data-ttu-id="400ca-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="400ca-256">In Global Catalog</span></span>      | <span data-ttu-id="400ca-257">Falso</span><span class="sxs-lookup"><span data-stu-id="400ca-257">False</span></span>                                                      |
| <span data-ttu-id="400ca-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="400ca-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="400ca-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="400ca-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="400ca-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="400ca-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="400ca-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="400ca-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-262">Search-Flags</span></span>           | <span data-ttu-id="400ca-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="400ca-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="400ca-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="400ca-264">System-Flags</span></span>           | <span data-ttu-id="400ca-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="400ca-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="400ca-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="400ca-266">Classes used in</span></span>        | [<span data-ttu-id="400ca-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="400ca-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





