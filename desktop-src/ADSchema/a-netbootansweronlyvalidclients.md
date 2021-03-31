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
# <a name="netboot-answer-only-valid-clients-attribute"></a><span data-ttu-id="d41d5-105">netboot-somente resposta-atributo de clientes válidos</span><span class="sxs-lookup"><span data-stu-id="d41d5-105">netboot-Answer-Only-Valid-Clients attribute</span></span>

<span data-ttu-id="d41d5-106">Determina se o servidor responde a todos os computadores cliente ou somente em pré-teste.</span><span class="sxs-lookup"><span data-stu-id="d41d5-106">Determines whether the server answers all, or only pre-staged, client computers.</span></span>



| <span data-ttu-id="d41d5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-107">Entry</span></span> | <span data-ttu-id="d41d5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d41d5-109">CN</span><span class="sxs-lookup"><span data-stu-id="d41d5-109">CN</span></span>                | <span data-ttu-id="d41d5-110">netboot-somente resposta-clientes válidos</span><span class="sxs-lookup"><span data-stu-id="d41d5-110">netboot-Answer-Only-Valid-Clients</span></span>    |
| <span data-ttu-id="d41d5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d41d5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d41d5-112">netbootAnswerOnlyValidClients</span><span class="sxs-lookup"><span data-stu-id="d41d5-112">netbootAnswerOnlyValidClients</span></span>        |
| <span data-ttu-id="d41d5-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d41d5-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d41d5-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d41d5-114">Update Privilege</span></span>  | <span data-ttu-id="d41d5-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d41d5-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="d41d5-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d41d5-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d41d5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-117">Attribute-Id</span></span>      | <span data-ttu-id="d41d5-118">1.2.840.113556.1.4.854</span><span class="sxs-lookup"><span data-stu-id="d41d5-118">1.2.840.113556.1.4.854</span></span>               |
| <span data-ttu-id="d41d5-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d41d5-119">System-Id-Guid</span></span>    | <span data-ttu-id="d41d5-120">0738307b-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d41d5-120">0738307b-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="d41d5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d41d5-121">Syntax</span></span>            | [<span data-ttu-id="d41d5-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d41d5-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="d41d5-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="d41d5-123">Implementations</span></span>

-   [<span data-ttu-id="d41d5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d41d5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d41d5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d41d5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d41d5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d41d5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d41d5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d41d5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d41d5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d41d5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d41d5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d41d5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d41d5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d41d5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d41d5-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-131">Entry</span></span> | <span data-ttu-id="d41d5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d41d5-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="d41d5-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d41d5-135">System-Only</span></span>            | <span data-ttu-id="d41d5-136">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-136">False</span></span>                                                      |
| <span data-ttu-id="d41d5-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d41d5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d41d5-138">True</span><span class="sxs-lookup"><span data-stu-id="d41d5-138">True</span></span>                                                       |
| <span data-ttu-id="d41d5-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="d41d5-139">Is Indexed</span></span>             | <span data-ttu-id="d41d5-140">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-140">False</span></span>                                                      |
| <span data-ttu-id="d41d5-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d41d5-141">In Global Catalog</span></span>      | <span data-ttu-id="d41d5-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-142">False</span></span>                                                      |
| <span data-ttu-id="d41d5-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d41d5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d41d5-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d41d5-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d41d5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d41d5-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d41d5-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-147">Search-Flags</span></span>           | <span data-ttu-id="d41d5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41d5-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="d41d5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-149">System-Flags</span></span>           | <span data-ttu-id="d41d5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d41d5-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="d41d5-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d41d5-151">Classes used in</span></span>        | [<span data-ttu-id="d41d5-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d41d5-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d41d5-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d41d5-153">Windows Server 2003</span></span>



| <span data-ttu-id="d41d5-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-154">Entry</span></span> | <span data-ttu-id="d41d5-155">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d41d5-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="d41d5-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d41d5-158">System-Only</span></span>            | <span data-ttu-id="d41d5-159">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-159">False</span></span>                                                      |
| <span data-ttu-id="d41d5-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d41d5-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d41d5-161">True</span><span class="sxs-lookup"><span data-stu-id="d41d5-161">True</span></span>                                                       |
| <span data-ttu-id="d41d5-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="d41d5-162">Is Indexed</span></span>             | <span data-ttu-id="d41d5-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-163">False</span></span>                                                      |
| <span data-ttu-id="d41d5-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d41d5-164">In Global Catalog</span></span>      | <span data-ttu-id="d41d5-165">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-165">False</span></span>                                                      |
| <span data-ttu-id="d41d5-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d41d5-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d41d5-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d41d5-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d41d5-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d41d5-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d41d5-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-170">Search-Flags</span></span>           | <span data-ttu-id="d41d5-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41d5-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="d41d5-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-172">System-Flags</span></span>           | <span data-ttu-id="d41d5-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d41d5-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="d41d5-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d41d5-174">Classes used in</span></span>        | [<span data-ttu-id="d41d5-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d41d5-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d41d5-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d41d5-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d41d5-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-177">Entry</span></span> | <span data-ttu-id="d41d5-178">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d41d5-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="d41d5-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d41d5-181">System-Only</span></span>            | <span data-ttu-id="d41d5-182">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-182">False</span></span>                                                      |
| <span data-ttu-id="d41d5-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d41d5-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d41d5-184">True</span><span class="sxs-lookup"><span data-stu-id="d41d5-184">True</span></span>                                                       |
| <span data-ttu-id="d41d5-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="d41d5-185">Is Indexed</span></span>             | <span data-ttu-id="d41d5-186">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-186">False</span></span>                                                      |
| <span data-ttu-id="d41d5-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d41d5-187">In Global Catalog</span></span>      | <span data-ttu-id="d41d5-188">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-188">False</span></span>                                                      |
| <span data-ttu-id="d41d5-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d41d5-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d41d5-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d41d5-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d41d5-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d41d5-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d41d5-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-193">Search-Flags</span></span>           | <span data-ttu-id="d41d5-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41d5-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="d41d5-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-195">System-Flags</span></span>           | <span data-ttu-id="d41d5-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d41d5-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="d41d5-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d41d5-197">Classes used in</span></span>        | [<span data-ttu-id="d41d5-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d41d5-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d41d5-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d41d5-199">Windows Server 2008</span></span>



| <span data-ttu-id="d41d5-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-200">Entry</span></span> | <span data-ttu-id="d41d5-201">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d41d5-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="d41d5-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d41d5-204">System-Only</span></span>            | <span data-ttu-id="d41d5-205">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-205">False</span></span>                                                      |
| <span data-ttu-id="d41d5-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d41d5-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d41d5-207">True</span><span class="sxs-lookup"><span data-stu-id="d41d5-207">True</span></span>                                                       |
| <span data-ttu-id="d41d5-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="d41d5-208">Is Indexed</span></span>             | <span data-ttu-id="d41d5-209">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-209">False</span></span>                                                      |
| <span data-ttu-id="d41d5-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d41d5-210">In Global Catalog</span></span>      | <span data-ttu-id="d41d5-211">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-211">False</span></span>                                                      |
| <span data-ttu-id="d41d5-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d41d5-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d41d5-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d41d5-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d41d5-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d41d5-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d41d5-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-216">Search-Flags</span></span>           | <span data-ttu-id="d41d5-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41d5-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="d41d5-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-218">System-Flags</span></span>           | <span data-ttu-id="d41d5-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d41d5-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="d41d5-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d41d5-220">Classes used in</span></span>        | [<span data-ttu-id="d41d5-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d41d5-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d41d5-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d41d5-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d41d5-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-223">Entry</span></span> | <span data-ttu-id="d41d5-224">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d41d5-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="d41d5-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d41d5-227">System-Only</span></span>            | <span data-ttu-id="d41d5-228">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-228">False</span></span>                                                      |
| <span data-ttu-id="d41d5-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d41d5-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d41d5-230">True</span><span class="sxs-lookup"><span data-stu-id="d41d5-230">True</span></span>                                                       |
| <span data-ttu-id="d41d5-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="d41d5-231">Is Indexed</span></span>             | <span data-ttu-id="d41d5-232">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-232">False</span></span>                                                      |
| <span data-ttu-id="d41d5-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d41d5-233">In Global Catalog</span></span>      | <span data-ttu-id="d41d5-234">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-234">False</span></span>                                                      |
| <span data-ttu-id="d41d5-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d41d5-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d41d5-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d41d5-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d41d5-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d41d5-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d41d5-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-239">Search-Flags</span></span>           | <span data-ttu-id="d41d5-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41d5-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="d41d5-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-241">System-Flags</span></span>           | <span data-ttu-id="d41d5-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d41d5-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="d41d5-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d41d5-243">Classes used in</span></span>        | [<span data-ttu-id="d41d5-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d41d5-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d41d5-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d41d5-245">Windows Server 2012</span></span>



| <span data-ttu-id="d41d5-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="d41d5-246">Entry</span></span> | <span data-ttu-id="d41d5-247">Valor</span><span class="sxs-lookup"><span data-stu-id="d41d5-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d41d5-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="d41d5-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d41d5-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d41d5-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d41d5-250">System-Only</span></span>            | <span data-ttu-id="d41d5-251">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-251">False</span></span>                                                      |
| <span data-ttu-id="d41d5-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d41d5-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d41d5-253">True</span><span class="sxs-lookup"><span data-stu-id="d41d5-253">True</span></span>                                                       |
| <span data-ttu-id="d41d5-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="d41d5-254">Is Indexed</span></span>             | <span data-ttu-id="d41d5-255">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-255">False</span></span>                                                      |
| <span data-ttu-id="d41d5-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d41d5-256">In Global Catalog</span></span>      | <span data-ttu-id="d41d5-257">Falso</span><span class="sxs-lookup"><span data-stu-id="d41d5-257">False</span></span>                                                      |
| <span data-ttu-id="d41d5-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d41d5-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d41d5-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d41d5-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d41d5-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d41d5-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d41d5-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d41d5-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-262">Search-Flags</span></span>           | <span data-ttu-id="d41d5-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d41d5-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="d41d5-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d41d5-264">System-Flags</span></span>           | <span data-ttu-id="d41d5-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d41d5-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="d41d5-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d41d5-266">Classes used in</span></span>        | [<span data-ttu-id="d41d5-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d41d5-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





