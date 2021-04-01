---
title: Token-groups-no-GC-atributo aceitável
description: Esse atributo contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador. Os grupos de tokens não poderão ser recuperados se um catálogo global não estiver presente para recuperar as associações inversas transitivas.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Token-groups-no-GC-esquema de AD do atributo aceitável
- Esquema de AD do atributo tokenGroupsNoGCAcceptable
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c4b8996586c8c35ed4c815b954dad02b5db03
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825073"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="79c35-106">Token-groups-no-GC-atributo aceitável</span><span class="sxs-lookup"><span data-stu-id="79c35-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="79c35-107">Esse atributo contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="79c35-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="79c35-108">Os grupos de tokens não poderão ser recuperados se um catálogo global não estiver presente para recuperar as associações inversas transitivas.</span><span class="sxs-lookup"><span data-stu-id="79c35-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="79c35-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-109">Entry</span></span> | <span data-ttu-id="79c35-110">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="79c35-111">CN</span><span class="sxs-lookup"><span data-stu-id="79c35-111">CN</span></span>                | <span data-ttu-id="79c35-112">Token-groups-no-GC-aceitável</span><span class="sxs-lookup"><span data-stu-id="79c35-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="79c35-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="79c35-113">Ldap-Display-Name</span></span> | <span data-ttu-id="79c35-114">tokenGroupsNoGCAcceptable</span><span class="sxs-lookup"><span data-stu-id="79c35-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="79c35-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="79c35-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="79c35-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="79c35-116">Update Privilege</span></span>  | <span data-ttu-id="79c35-117">O sistema define esse valor.</span><span class="sxs-lookup"><span data-stu-id="79c35-117">The system sets this value.</span></span>          |
| <span data-ttu-id="79c35-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="79c35-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="79c35-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-119">Attribute-Id</span></span>      | <span data-ttu-id="79c35-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="79c35-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="79c35-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="79c35-121">System-Id-Guid</span></span>    | <span data-ttu-id="79c35-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="79c35-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="79c35-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c35-123">Syntax</span></span>            | [<span data-ttu-id="79c35-124">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="79c35-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="79c35-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="79c35-125">Implementations</span></span>

-   [<span data-ttu-id="79c35-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="79c35-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="79c35-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79c35-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79c35-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79c35-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79c35-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79c35-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79c35-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79c35-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79c35-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79c35-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="79c35-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79c35-132">Windows 2000 Server</span></span>



| <span data-ttu-id="79c35-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-133">Entry</span></span> | <span data-ttu-id="79c35-134">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="79c35-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="79c35-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c35-137">System-Only</span></span>            | <span data-ttu-id="79c35-138">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-138">False</span></span>                                                        |
| <span data-ttu-id="79c35-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79c35-139">Is-Single-Valued</span></span>       | <span data-ttu-id="79c35-140">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-140">False</span></span>                                                        |
| <span data-ttu-id="79c35-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="79c35-141">Is Indexed</span></span>             | <span data-ttu-id="79c35-142">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-142">False</span></span>                                                        |
| <span data-ttu-id="79c35-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79c35-143">In Global Catalog</span></span>      | <span data-ttu-id="79c35-144">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-144">False</span></span>                                                        |
| <span data-ttu-id="79c35-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79c35-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c35-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79c35-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="79c35-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c35-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c35-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-149">Search-Flags</span></span>           | <span data-ttu-id="79c35-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79c35-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="79c35-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-151">System-Flags</span></span>           | <span data-ttu-id="79c35-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79c35-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="79c35-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79c35-153">Classes used in</span></span>        | [<span data-ttu-id="79c35-154">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="79c35-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="79c35-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79c35-155">Windows Server 2003</span></span>



| <span data-ttu-id="79c35-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-156">Entry</span></span> | <span data-ttu-id="79c35-157">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="79c35-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="79c35-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c35-160">System-Only</span></span>            | <span data-ttu-id="79c35-161">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-161">False</span></span>                                                        |
| <span data-ttu-id="79c35-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79c35-162">Is-Single-Valued</span></span>       | <span data-ttu-id="79c35-163">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-163">False</span></span>                                                        |
| <span data-ttu-id="79c35-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="79c35-164">Is Indexed</span></span>             | <span data-ttu-id="79c35-165">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-165">False</span></span>                                                        |
| <span data-ttu-id="79c35-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79c35-166">In Global Catalog</span></span>      | <span data-ttu-id="79c35-167">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-167">False</span></span>                                                        |
| <span data-ttu-id="79c35-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79c35-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c35-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79c35-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="79c35-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c35-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c35-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-172">Search-Flags</span></span>           | <span data-ttu-id="79c35-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79c35-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="79c35-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-174">System-Flags</span></span>           | <span data-ttu-id="79c35-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79c35-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="79c35-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79c35-176">Classes used in</span></span>        | [<span data-ttu-id="79c35-177">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="79c35-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79c35-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79c35-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79c35-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-179">Entry</span></span> | <span data-ttu-id="79c35-180">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="79c35-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="79c35-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c35-183">System-Only</span></span>            | <span data-ttu-id="79c35-184">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-184">False</span></span>                                                        |
| <span data-ttu-id="79c35-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79c35-185">Is-Single-Valued</span></span>       | <span data-ttu-id="79c35-186">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-186">False</span></span>                                                        |
| <span data-ttu-id="79c35-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="79c35-187">Is Indexed</span></span>             | <span data-ttu-id="79c35-188">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-188">False</span></span>                                                        |
| <span data-ttu-id="79c35-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79c35-189">In Global Catalog</span></span>      | <span data-ttu-id="79c35-190">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-190">False</span></span>                                                        |
| <span data-ttu-id="79c35-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79c35-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c35-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79c35-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="79c35-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c35-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c35-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-195">Search-Flags</span></span>           | <span data-ttu-id="79c35-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79c35-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="79c35-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-197">System-Flags</span></span>           | <span data-ttu-id="79c35-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79c35-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="79c35-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79c35-199">Classes used in</span></span>        | [<span data-ttu-id="79c35-200">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="79c35-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79c35-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79c35-201">Windows Server 2008</span></span>



| <span data-ttu-id="79c35-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-202">Entry</span></span> | <span data-ttu-id="79c35-203">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="79c35-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="79c35-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c35-206">System-Only</span></span>            | <span data-ttu-id="79c35-207">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-207">False</span></span>                                                        |
| <span data-ttu-id="79c35-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79c35-208">Is-Single-Valued</span></span>       | <span data-ttu-id="79c35-209">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-209">False</span></span>                                                        |
| <span data-ttu-id="79c35-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="79c35-210">Is Indexed</span></span>             | <span data-ttu-id="79c35-211">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-211">False</span></span>                                                        |
| <span data-ttu-id="79c35-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79c35-212">In Global Catalog</span></span>      | <span data-ttu-id="79c35-213">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-213">False</span></span>                                                        |
| <span data-ttu-id="79c35-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79c35-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c35-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79c35-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="79c35-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c35-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c35-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-218">Search-Flags</span></span>           | <span data-ttu-id="79c35-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79c35-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="79c35-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-220">System-Flags</span></span>           | <span data-ttu-id="79c35-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79c35-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="79c35-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79c35-222">Classes used in</span></span>        | [<span data-ttu-id="79c35-223">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="79c35-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79c35-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79c35-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79c35-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-225">Entry</span></span> | <span data-ttu-id="79c35-226">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="79c35-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="79c35-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c35-229">System-Only</span></span>            | <span data-ttu-id="79c35-230">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-230">False</span></span>                                                        |
| <span data-ttu-id="79c35-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79c35-231">Is-Single-Valued</span></span>       | <span data-ttu-id="79c35-232">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-232">False</span></span>                                                        |
| <span data-ttu-id="79c35-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="79c35-233">Is Indexed</span></span>             | <span data-ttu-id="79c35-234">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-234">False</span></span>                                                        |
| <span data-ttu-id="79c35-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79c35-235">In Global Catalog</span></span>      | <span data-ttu-id="79c35-236">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-236">False</span></span>                                                        |
| <span data-ttu-id="79c35-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79c35-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c35-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79c35-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="79c35-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c35-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c35-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-241">Search-Flags</span></span>           | <span data-ttu-id="79c35-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79c35-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="79c35-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-243">System-Flags</span></span>           | <span data-ttu-id="79c35-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79c35-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="79c35-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79c35-245">Classes used in</span></span>        | [<span data-ttu-id="79c35-246">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="79c35-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79c35-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79c35-247">Windows Server 2012</span></span>



| <span data-ttu-id="79c35-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="79c35-248">Entry</span></span> | <span data-ttu-id="79c35-249">Valor</span><span class="sxs-lookup"><span data-stu-id="79c35-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="79c35-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="79c35-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79c35-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="79c35-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="79c35-252">System-Only</span></span>            | <span data-ttu-id="79c35-253">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-253">False</span></span>                                                        |
| <span data-ttu-id="79c35-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79c35-254">Is-Single-Valued</span></span>       | <span data-ttu-id="79c35-255">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-255">False</span></span>                                                        |
| <span data-ttu-id="79c35-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="79c35-256">Is Indexed</span></span>             | <span data-ttu-id="79c35-257">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-257">False</span></span>                                                        |
| <span data-ttu-id="79c35-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79c35-258">In Global Catalog</span></span>      | <span data-ttu-id="79c35-259">Falso</span><span class="sxs-lookup"><span data-stu-id="79c35-259">False</span></span>                                                        |
| <span data-ttu-id="79c35-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79c35-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="79c35-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79c35-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="79c35-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79c35-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79c35-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="79c35-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-264">Search-Flags</span></span>           | <span data-ttu-id="79c35-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79c35-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="79c35-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79c35-266">System-Flags</span></span>           | <span data-ttu-id="79c35-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="79c35-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="79c35-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79c35-268">Classes used in</span></span>        | [<span data-ttu-id="79c35-269">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="79c35-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





