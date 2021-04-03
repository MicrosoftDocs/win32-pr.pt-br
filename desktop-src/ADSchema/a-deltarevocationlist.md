---
title: Atributo Delta-Revocation-List
description: Lista de certificados que foram revogados desde a última atualização Delta.
ms.assetid: fc755c22-6d4f-4509-abb8-47c4f2f37545
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo Delta-Revocation-List
- Esquema de AD do atributo deltaRevocationList
topic_type:
- apiref
api_name:
- Delta-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e866090dfb754c11fb4a25bbe904d5922a8fafd6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086708"
---
# <a name="delta-revocation-list-attribute"></a><span data-ttu-id="117f0-105">Atributo Delta-Revocation-List</span><span class="sxs-lookup"><span data-stu-id="117f0-105">Delta-Revocation-List attribute</span></span>

<span data-ttu-id="117f0-106">Lista de certificados que foram revogados desde a última atualização Delta.</span><span class="sxs-lookup"><span data-stu-id="117f0-106">List of certificates that have been revoked since the last delta update.</span></span>



| <span data-ttu-id="117f0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-107">Entry</span></span> | <span data-ttu-id="117f0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="117f0-109">CN</span><span class="sxs-lookup"><span data-stu-id="117f0-109">CN</span></span>                | <span data-ttu-id="117f0-110">Delta-lista de revogação</span><span class="sxs-lookup"><span data-stu-id="117f0-110">Delta-Revocation-List</span></span>                                 |
| <span data-ttu-id="117f0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="117f0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="117f0-112">deltaRevocationList</span><span class="sxs-lookup"><span data-stu-id="117f0-112">deltaRevocationList</span></span>                                   |
| <span data-ttu-id="117f0-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="117f0-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="117f0-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="117f0-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="117f0-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="117f0-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="117f0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-116">Attribute-Id</span></span>      | <span data-ttu-id="117f0-117">2.5.4.53</span><span class="sxs-lookup"><span data-stu-id="117f0-117">2.5.4.53</span></span>                                              |
| <span data-ttu-id="117f0-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="117f0-118">System-Id-Guid</span></span>    | <span data-ttu-id="117f0-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="117f0-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="117f0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="117f0-120">Syntax</span></span>            | [<span data-ttu-id="117f0-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="117f0-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="117f0-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="117f0-122">Implementations</span></span>

-   [<span data-ttu-id="117f0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="117f0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="117f0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="117f0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="117f0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="117f0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="117f0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="117f0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="117f0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="117f0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="117f0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="117f0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="117f0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="117f0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="117f0-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-130">Entry</span></span> | <span data-ttu-id="117f0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f0-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="117f0-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="117f0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-133">MAPI-Id</span></span>                | <span data-ttu-id="117f0-134">0x8C46</span><span class="sxs-lookup"><span data-stu-id="117f0-134">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="117f0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="117f0-135">System-Only</span></span>            | <span data-ttu-id="117f0-136">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="117f0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="117f0-138">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="117f0-139">Is Indexed</span></span>             | <span data-ttu-id="117f0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="117f0-141">In Global Catalog</span></span>      | <span data-ttu-id="117f0-142">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="117f0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="117f0-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="117f0-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="117f0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="117f0-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="117f0-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-147">Search-Flags</span></span>           | <span data-ttu-id="117f0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-149">System-Flags</span></span>           | <span data-ttu-id="117f0-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-150">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="117f0-151">Classes used in</span></span>        | [<span data-ttu-id="117f0-152">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="117f0-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="117f0-153">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="117f0-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="117f0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="117f0-154">Windows Server 2003</span></span>



| <span data-ttu-id="117f0-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-155">Entry</span></span> | <span data-ttu-id="117f0-156">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f0-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="117f0-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="117f0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-158">MAPI-Id</span></span>                | <span data-ttu-id="117f0-159">0x8C46</span><span class="sxs-lookup"><span data-stu-id="117f0-159">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="117f0-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="117f0-160">System-Only</span></span>            | <span data-ttu-id="117f0-161">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="117f0-162">Is-Single-Valued</span></span>       | <span data-ttu-id="117f0-163">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="117f0-164">Is Indexed</span></span>             | <span data-ttu-id="117f0-165">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="117f0-166">In Global Catalog</span></span>      | <span data-ttu-id="117f0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="117f0-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="117f0-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="117f0-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="117f0-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="117f0-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="117f0-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-172">Search-Flags</span></span>           | <span data-ttu-id="117f0-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-174">System-Flags</span></span>           | <span data-ttu-id="117f0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-175">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="117f0-176">Classes used in</span></span>        | [<span data-ttu-id="117f0-177">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="117f0-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="117f0-178">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="117f0-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="117f0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="117f0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="117f0-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-180">Entry</span></span> | <span data-ttu-id="117f0-181">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f0-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="117f0-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="117f0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-183">MAPI-Id</span></span>                | <span data-ttu-id="117f0-184">0x8C46</span><span class="sxs-lookup"><span data-stu-id="117f0-184">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="117f0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="117f0-185">System-Only</span></span>            | <span data-ttu-id="117f0-186">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="117f0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="117f0-188">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="117f0-189">Is Indexed</span></span>             | <span data-ttu-id="117f0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="117f0-191">In Global Catalog</span></span>      | <span data-ttu-id="117f0-192">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="117f0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="117f0-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="117f0-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="117f0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="117f0-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="117f0-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-197">Search-Flags</span></span>           | <span data-ttu-id="117f0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-199">System-Flags</span></span>           | <span data-ttu-id="117f0-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="117f0-201">Classes used in</span></span>        | [<span data-ttu-id="117f0-202">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="117f0-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="117f0-203">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="117f0-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="117f0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="117f0-204">Windows Server 2008</span></span>



| <span data-ttu-id="117f0-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-205">Entry</span></span> | <span data-ttu-id="117f0-206">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f0-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="117f0-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="117f0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-208">MAPI-Id</span></span>                | <span data-ttu-id="117f0-209">0x8C46</span><span class="sxs-lookup"><span data-stu-id="117f0-209">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="117f0-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="117f0-210">System-Only</span></span>            | <span data-ttu-id="117f0-211">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="117f0-212">Is-Single-Valued</span></span>       | <span data-ttu-id="117f0-213">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="117f0-214">Is Indexed</span></span>             | <span data-ttu-id="117f0-215">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="117f0-216">In Global Catalog</span></span>      | <span data-ttu-id="117f0-217">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="117f0-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="117f0-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="117f0-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="117f0-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="117f0-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="117f0-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-222">Search-Flags</span></span>           | <span data-ttu-id="117f0-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-224">System-Flags</span></span>           | <span data-ttu-id="117f0-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-225">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="117f0-226">Classes used in</span></span>        | [<span data-ttu-id="117f0-227">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="117f0-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="117f0-228">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="117f0-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="117f0-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="117f0-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="117f0-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-230">Entry</span></span> | <span data-ttu-id="117f0-231">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f0-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="117f0-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="117f0-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-233">MAPI-Id</span></span>                | <span data-ttu-id="117f0-234">0x8C46</span><span class="sxs-lookup"><span data-stu-id="117f0-234">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="117f0-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="117f0-235">System-Only</span></span>            | <span data-ttu-id="117f0-236">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="117f0-237">Is-Single-Valued</span></span>       | <span data-ttu-id="117f0-238">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="117f0-239">Is Indexed</span></span>             | <span data-ttu-id="117f0-240">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="117f0-241">In Global Catalog</span></span>      | <span data-ttu-id="117f0-242">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="117f0-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="117f0-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="117f0-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="117f0-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="117f0-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="117f0-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-247">Search-Flags</span></span>           | <span data-ttu-id="117f0-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-249">System-Flags</span></span>           | <span data-ttu-id="117f0-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="117f0-251">Classes used in</span></span>        | [<span data-ttu-id="117f0-252">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="117f0-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="117f0-253">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="117f0-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="117f0-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="117f0-254">Windows Server 2012</span></span>



| <span data-ttu-id="117f0-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="117f0-255">Entry</span></span> | <span data-ttu-id="117f0-256">Valor</span><span class="sxs-lookup"><span data-stu-id="117f0-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="117f0-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="117f0-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="117f0-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="117f0-258">MAPI-Id</span></span>                | <span data-ttu-id="117f0-259">0x8C46</span><span class="sxs-lookup"><span data-stu-id="117f0-259">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="117f0-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="117f0-260">System-Only</span></span>            | <span data-ttu-id="117f0-261">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="117f0-262">Is-Single-Valued</span></span>       | <span data-ttu-id="117f0-263">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="117f0-264">Is Indexed</span></span>             | <span data-ttu-id="117f0-265">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="117f0-266">In Global Catalog</span></span>      | <span data-ttu-id="117f0-267">Falso</span><span class="sxs-lookup"><span data-stu-id="117f0-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="117f0-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="117f0-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="117f0-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="117f0-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="117f0-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="117f0-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="117f0-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="117f0-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-272">Search-Flags</span></span>           | <span data-ttu-id="117f0-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="117f0-274">System-Flags</span></span>           | <span data-ttu-id="117f0-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="117f0-275">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="117f0-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="117f0-276">Classes used in</span></span>        | [<span data-ttu-id="117f0-277">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="117f0-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="117f0-278">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="117f0-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





