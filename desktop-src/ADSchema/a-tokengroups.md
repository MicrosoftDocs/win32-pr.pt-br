---
title: Token-Groups atributo
description: Um atributo computado que contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador. Os grupos de tokens não poderão ser recuperados se nenhum catálogo global estiver presente para recuperar as associações inversas transitivas.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Esquema de Token-Groups do atributo AD
- Esquema de AD do atributo tokenGroups
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769099"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="71530-106">Token-Groups atributo</span><span class="sxs-lookup"><span data-stu-id="71530-106">Token-Groups attribute</span></span>

<span data-ttu-id="71530-107">Um atributo computado que contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="71530-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="71530-108">Os grupos de tokens não poderão ser recuperados se nenhum catálogo global estiver presente para recuperar as associações inversas transitivas.</span><span class="sxs-lookup"><span data-stu-id="71530-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="71530-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-109">Entry</span></span> | <span data-ttu-id="71530-110">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="71530-111">CN</span><span class="sxs-lookup"><span data-stu-id="71530-111">CN</span></span>                | <span data-ttu-id="71530-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="71530-112">Token-Groups</span></span>                         |
| <span data-ttu-id="71530-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="71530-113">Ldap-Display-Name</span></span> | <span data-ttu-id="71530-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="71530-114">tokenGroups</span></span>                          |
| <span data-ttu-id="71530-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="71530-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="71530-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="71530-116">Update Privilege</span></span>  | <span data-ttu-id="71530-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="71530-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="71530-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="71530-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="71530-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="71530-119">Attribute-Id</span></span>      | <span data-ttu-id="71530-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="71530-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="71530-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="71530-121">System-Id-Guid</span></span>    | <span data-ttu-id="71530-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="71530-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="71530-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="71530-123">Syntax</span></span>            | [<span data-ttu-id="71530-124">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="71530-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="71530-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="71530-125">Implementations</span></span>

-   [<span data-ttu-id="71530-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="71530-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="71530-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="71530-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="71530-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="71530-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="71530-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="71530-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="71530-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="71530-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="71530-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="71530-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="71530-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="71530-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="71530-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71530-133">Windows 2000 Server</span></span>



| <span data-ttu-id="71530-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-134">Entry</span></span> | <span data-ttu-id="71530-135">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-138">System-Only</span></span>            | <span data-ttu-id="71530-139">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-139">False</span></span>                                                        |
| <span data-ttu-id="71530-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-140">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-141">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-141">False</span></span>                                                        |
| <span data-ttu-id="71530-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-142">Is Indexed</span></span>             | <span data-ttu-id="71530-143">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-143">False</span></span>                                                        |
| <span data-ttu-id="71530-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-144">In Global Catalog</span></span>      | <span data-ttu-id="71530-145">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-145">False</span></span>                                                        |
| <span data-ttu-id="71530-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-150">Search-Flags</span></span>           | <span data-ttu-id="71530-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-152">System-Flags</span></span>           | <span data-ttu-id="71530-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-154">Classes used in</span></span>        | [<span data-ttu-id="71530-155">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="71530-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71530-156">Windows Server 2003</span></span>



| <span data-ttu-id="71530-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-157">Entry</span></span> | <span data-ttu-id="71530-158">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-161">System-Only</span></span>            | <span data-ttu-id="71530-162">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-162">False</span></span>                                                        |
| <span data-ttu-id="71530-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-163">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-164">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-164">False</span></span>                                                        |
| <span data-ttu-id="71530-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-165">Is Indexed</span></span>             | <span data-ttu-id="71530-166">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-166">False</span></span>                                                        |
| <span data-ttu-id="71530-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-167">In Global Catalog</span></span>      | <span data-ttu-id="71530-168">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-168">False</span></span>                                                        |
| <span data-ttu-id="71530-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-173">Search-Flags</span></span>           | <span data-ttu-id="71530-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-175">System-Flags</span></span>           | <span data-ttu-id="71530-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-177">Classes used in</span></span>        | [<span data-ttu-id="71530-178">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="71530-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="71530-179">ADAM</span></span>



| <span data-ttu-id="71530-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-180">Entry</span></span> | <span data-ttu-id="71530-181">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-184">System-Only</span></span>            | <span data-ttu-id="71530-185">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-185">False</span></span>                                                        |
| <span data-ttu-id="71530-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-186">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-187">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-187">False</span></span>                                                        |
| <span data-ttu-id="71530-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-188">Is Indexed</span></span>             | <span data-ttu-id="71530-189">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-189">False</span></span>                                                        |
| <span data-ttu-id="71530-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-190">In Global Catalog</span></span>      | <span data-ttu-id="71530-191">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-191">False</span></span>                                                        |
| <span data-ttu-id="71530-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-196">Search-Flags</span></span>           | <span data-ttu-id="71530-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-198">System-Flags</span></span>           | <span data-ttu-id="71530-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-200">Classes used in</span></span>        | [<span data-ttu-id="71530-201">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="71530-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="71530-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="71530-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-203">Entry</span></span> | <span data-ttu-id="71530-204">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-207">System-Only</span></span>            | <span data-ttu-id="71530-208">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-208">False</span></span>                                                        |
| <span data-ttu-id="71530-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-209">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-210">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-210">False</span></span>                                                        |
| <span data-ttu-id="71530-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-211">Is Indexed</span></span>             | <span data-ttu-id="71530-212">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-212">False</span></span>                                                        |
| <span data-ttu-id="71530-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-213">In Global Catalog</span></span>      | <span data-ttu-id="71530-214">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-214">False</span></span>                                                        |
| <span data-ttu-id="71530-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-219">Search-Flags</span></span>           | <span data-ttu-id="71530-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-221">System-Flags</span></span>           | <span data-ttu-id="71530-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-223">Classes used in</span></span>        | [<span data-ttu-id="71530-224">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="71530-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71530-225">Windows Server 2008</span></span>



| <span data-ttu-id="71530-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-226">Entry</span></span> | <span data-ttu-id="71530-227">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-230">System-Only</span></span>            | <span data-ttu-id="71530-231">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-231">False</span></span>                                                        |
| <span data-ttu-id="71530-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-232">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-233">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-233">False</span></span>                                                        |
| <span data-ttu-id="71530-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-234">Is Indexed</span></span>             | <span data-ttu-id="71530-235">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-235">False</span></span>                                                        |
| <span data-ttu-id="71530-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-236">In Global Catalog</span></span>      | <span data-ttu-id="71530-237">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-237">False</span></span>                                                        |
| <span data-ttu-id="71530-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-242">Search-Flags</span></span>           | <span data-ttu-id="71530-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-244">System-Flags</span></span>           | <span data-ttu-id="71530-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-246">Classes used in</span></span>        | [<span data-ttu-id="71530-247">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="71530-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71530-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="71530-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-249">Entry</span></span> | <span data-ttu-id="71530-250">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-253">System-Only</span></span>            | <span data-ttu-id="71530-254">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-254">False</span></span>                                                        |
| <span data-ttu-id="71530-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-255">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-256">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-256">False</span></span>                                                        |
| <span data-ttu-id="71530-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-257">Is Indexed</span></span>             | <span data-ttu-id="71530-258">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-258">False</span></span>                                                        |
| <span data-ttu-id="71530-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-259">In Global Catalog</span></span>      | <span data-ttu-id="71530-260">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-260">False</span></span>                                                        |
| <span data-ttu-id="71530-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-265">Search-Flags</span></span>           | <span data-ttu-id="71530-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-267">System-Flags</span></span>           | <span data-ttu-id="71530-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-269">Classes used in</span></span>        | [<span data-ttu-id="71530-270">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="71530-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71530-271">Windows Server 2012</span></span>



| <span data-ttu-id="71530-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="71530-272">Entry</span></span> | <span data-ttu-id="71530-273">Valor</span><span class="sxs-lookup"><span data-stu-id="71530-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="71530-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="71530-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71530-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="71530-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="71530-276">System-Only</span></span>            | <span data-ttu-id="71530-277">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-277">False</span></span>                                                        |
| <span data-ttu-id="71530-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71530-278">Is-Single-Valued</span></span>       | <span data-ttu-id="71530-279">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-279">False</span></span>                                                        |
| <span data-ttu-id="71530-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="71530-280">Is Indexed</span></span>             | <span data-ttu-id="71530-281">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-281">False</span></span>                                                        |
| <span data-ttu-id="71530-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71530-282">In Global Catalog</span></span>      | <span data-ttu-id="71530-283">Falso</span><span class="sxs-lookup"><span data-stu-id="71530-283">False</span></span>                                                        |
| <span data-ttu-id="71530-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71530-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="71530-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71530-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="71530-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71530-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="71530-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71530-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="71530-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-288">Search-Flags</span></span>           | <span data-ttu-id="71530-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71530-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="71530-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71530-290">System-Flags</span></span>           | <span data-ttu-id="71530-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="71530-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="71530-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71530-292">Classes used in</span></span>        | [<span data-ttu-id="71530-293">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="71530-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





