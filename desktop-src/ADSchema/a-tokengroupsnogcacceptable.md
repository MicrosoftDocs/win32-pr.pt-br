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
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="b46d1-106">Token-groups-no-GC-atributo aceitável</span><span class="sxs-lookup"><span data-stu-id="b46d1-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="b46d1-107">Esse atributo contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="b46d1-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="b46d1-108">Os grupos de tokens não poderão ser recuperados se um catálogo global não estiver presente para recuperar as associações inversas transitivas.</span><span class="sxs-lookup"><span data-stu-id="b46d1-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="b46d1-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-109">Entry</span></span> | <span data-ttu-id="b46d1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b46d1-111">CN</span><span class="sxs-lookup"><span data-stu-id="b46d1-111">CN</span></span>                | <span data-ttu-id="b46d1-112">Token-groups-no-GC-aceitável</span><span class="sxs-lookup"><span data-stu-id="b46d1-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="b46d1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b46d1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b46d1-114">tokenGroupsNoGCAcceptable</span><span class="sxs-lookup"><span data-stu-id="b46d1-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="b46d1-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b46d1-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b46d1-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b46d1-116">Update Privilege</span></span>  | <span data-ttu-id="b46d1-117">O sistema define esse valor.</span><span class="sxs-lookup"><span data-stu-id="b46d1-117">The system sets this value.</span></span>          |
| <span data-ttu-id="b46d1-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b46d1-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b46d1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-119">Attribute-Id</span></span>      | <span data-ttu-id="b46d1-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="b46d1-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="b46d1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b46d1-121">System-Id-Guid</span></span>    | <span data-ttu-id="b46d1-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b46d1-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="b46d1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b46d1-123">Syntax</span></span>            | [<span data-ttu-id="b46d1-124">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="b46d1-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="b46d1-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="b46d1-125">Implementations</span></span>

-   [<span data-ttu-id="b46d1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b46d1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b46d1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b46d1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b46d1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b46d1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b46d1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b46d1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b46d1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b46d1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b46d1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b46d1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b46d1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b46d1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b46d1-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-133">Entry</span></span> | <span data-ttu-id="b46d1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b46d1-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="b46d1-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b46d1-137">System-Only</span></span>            | <span data-ttu-id="b46d1-138">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-138">False</span></span>                                                        |
| <span data-ttu-id="b46d1-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b46d1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b46d1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-140">False</span></span>                                                        |
| <span data-ttu-id="b46d1-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="b46d1-141">Is Indexed</span></span>             | <span data-ttu-id="b46d1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-142">False</span></span>                                                        |
| <span data-ttu-id="b46d1-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b46d1-143">In Global Catalog</span></span>      | <span data-ttu-id="b46d1-144">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-144">False</span></span>                                                        |
| <span data-ttu-id="b46d1-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b46d1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b46d1-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b46d1-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b46d1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b46d1-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b46d1-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-149">Search-Flags</span></span>           | <span data-ttu-id="b46d1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b46d1-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="b46d1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-151">System-Flags</span></span>           | <span data-ttu-id="b46d1-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b46d1-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="b46d1-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b46d1-153">Classes used in</span></span>        | [<span data-ttu-id="b46d1-154">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b46d1-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b46d1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b46d1-155">Windows Server 2003</span></span>



| <span data-ttu-id="b46d1-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-156">Entry</span></span> | <span data-ttu-id="b46d1-157">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b46d1-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="b46d1-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b46d1-160">System-Only</span></span>            | <span data-ttu-id="b46d1-161">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-161">False</span></span>                                                        |
| <span data-ttu-id="b46d1-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b46d1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b46d1-163">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-163">False</span></span>                                                        |
| <span data-ttu-id="b46d1-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="b46d1-164">Is Indexed</span></span>             | <span data-ttu-id="b46d1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-165">False</span></span>                                                        |
| <span data-ttu-id="b46d1-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b46d1-166">In Global Catalog</span></span>      | <span data-ttu-id="b46d1-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-167">False</span></span>                                                        |
| <span data-ttu-id="b46d1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b46d1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b46d1-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b46d1-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b46d1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b46d1-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b46d1-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-172">Search-Flags</span></span>           | <span data-ttu-id="b46d1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b46d1-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="b46d1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-174">System-Flags</span></span>           | <span data-ttu-id="b46d1-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b46d1-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="b46d1-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b46d1-176">Classes used in</span></span>        | [<span data-ttu-id="b46d1-177">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b46d1-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b46d1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b46d1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b46d1-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-179">Entry</span></span> | <span data-ttu-id="b46d1-180">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b46d1-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="b46d1-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b46d1-183">System-Only</span></span>            | <span data-ttu-id="b46d1-184">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-184">False</span></span>                                                        |
| <span data-ttu-id="b46d1-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b46d1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b46d1-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-186">False</span></span>                                                        |
| <span data-ttu-id="b46d1-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="b46d1-187">Is Indexed</span></span>             | <span data-ttu-id="b46d1-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-188">False</span></span>                                                        |
| <span data-ttu-id="b46d1-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b46d1-189">In Global Catalog</span></span>      | <span data-ttu-id="b46d1-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-190">False</span></span>                                                        |
| <span data-ttu-id="b46d1-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b46d1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b46d1-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b46d1-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b46d1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b46d1-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b46d1-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-195">Search-Flags</span></span>           | <span data-ttu-id="b46d1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b46d1-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="b46d1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-197">System-Flags</span></span>           | <span data-ttu-id="b46d1-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b46d1-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="b46d1-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b46d1-199">Classes used in</span></span>        | [<span data-ttu-id="b46d1-200">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b46d1-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b46d1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b46d1-201">Windows Server 2008</span></span>



| <span data-ttu-id="b46d1-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-202">Entry</span></span> | <span data-ttu-id="b46d1-203">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b46d1-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="b46d1-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b46d1-206">System-Only</span></span>            | <span data-ttu-id="b46d1-207">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-207">False</span></span>                                                        |
| <span data-ttu-id="b46d1-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b46d1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b46d1-209">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-209">False</span></span>                                                        |
| <span data-ttu-id="b46d1-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="b46d1-210">Is Indexed</span></span>             | <span data-ttu-id="b46d1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-211">False</span></span>                                                        |
| <span data-ttu-id="b46d1-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b46d1-212">In Global Catalog</span></span>      | <span data-ttu-id="b46d1-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-213">False</span></span>                                                        |
| <span data-ttu-id="b46d1-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b46d1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b46d1-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b46d1-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b46d1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b46d1-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b46d1-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-218">Search-Flags</span></span>           | <span data-ttu-id="b46d1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b46d1-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="b46d1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-220">System-Flags</span></span>           | <span data-ttu-id="b46d1-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b46d1-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="b46d1-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b46d1-222">Classes used in</span></span>        | [<span data-ttu-id="b46d1-223">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b46d1-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b46d1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b46d1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b46d1-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-225">Entry</span></span> | <span data-ttu-id="b46d1-226">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b46d1-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="b46d1-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b46d1-229">System-Only</span></span>            | <span data-ttu-id="b46d1-230">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-230">False</span></span>                                                        |
| <span data-ttu-id="b46d1-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b46d1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b46d1-232">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-232">False</span></span>                                                        |
| <span data-ttu-id="b46d1-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="b46d1-233">Is Indexed</span></span>             | <span data-ttu-id="b46d1-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-234">False</span></span>                                                        |
| <span data-ttu-id="b46d1-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b46d1-235">In Global Catalog</span></span>      | <span data-ttu-id="b46d1-236">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-236">False</span></span>                                                        |
| <span data-ttu-id="b46d1-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b46d1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b46d1-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b46d1-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b46d1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b46d1-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b46d1-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-241">Search-Flags</span></span>           | <span data-ttu-id="b46d1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b46d1-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="b46d1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-243">System-Flags</span></span>           | <span data-ttu-id="b46d1-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b46d1-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="b46d1-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b46d1-245">Classes used in</span></span>        | [<span data-ttu-id="b46d1-246">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b46d1-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b46d1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b46d1-247">Windows Server 2012</span></span>



| <span data-ttu-id="b46d1-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="b46d1-248">Entry</span></span> | <span data-ttu-id="b46d1-249">Valor</span><span class="sxs-lookup"><span data-stu-id="b46d1-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b46d1-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="b46d1-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b46d1-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b46d1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b46d1-252">System-Only</span></span>            | <span data-ttu-id="b46d1-253">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-253">False</span></span>                                                        |
| <span data-ttu-id="b46d1-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b46d1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b46d1-255">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-255">False</span></span>                                                        |
| <span data-ttu-id="b46d1-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="b46d1-256">Is Indexed</span></span>             | <span data-ttu-id="b46d1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-257">False</span></span>                                                        |
| <span data-ttu-id="b46d1-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b46d1-258">In Global Catalog</span></span>      | <span data-ttu-id="b46d1-259">Falso</span><span class="sxs-lookup"><span data-stu-id="b46d1-259">False</span></span>                                                        |
| <span data-ttu-id="b46d1-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b46d1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b46d1-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b46d1-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b46d1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b46d1-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b46d1-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b46d1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-264">Search-Flags</span></span>           | <span data-ttu-id="b46d1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b46d1-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="b46d1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b46d1-266">System-Flags</span></span>           | <span data-ttu-id="b46d1-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b46d1-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="b46d1-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b46d1-268">Classes used in</span></span>        | [<span data-ttu-id="b46d1-269">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="b46d1-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





