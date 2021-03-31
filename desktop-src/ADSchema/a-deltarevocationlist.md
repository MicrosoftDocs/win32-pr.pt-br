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
# <a name="delta-revocation-list-attribute"></a><span data-ttu-id="10245-105">Atributo Delta-Revocation-List</span><span class="sxs-lookup"><span data-stu-id="10245-105">Delta-Revocation-List attribute</span></span>

<span data-ttu-id="10245-106">Lista de certificados que foram revogados desde a última atualização Delta.</span><span class="sxs-lookup"><span data-stu-id="10245-106">List of certificates that have been revoked since the last delta update.</span></span>



| <span data-ttu-id="10245-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-107">Entry</span></span> | <span data-ttu-id="10245-108">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="10245-109">CN</span><span class="sxs-lookup"><span data-stu-id="10245-109">CN</span></span>                | <span data-ttu-id="10245-110">Delta-lista de revogação</span><span class="sxs-lookup"><span data-stu-id="10245-110">Delta-Revocation-List</span></span>                                 |
| <span data-ttu-id="10245-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="10245-111">Ldap-Display-Name</span></span> | <span data-ttu-id="10245-112">deltaRevocationList</span><span class="sxs-lookup"><span data-stu-id="10245-112">deltaRevocationList</span></span>                                   |
| <span data-ttu-id="10245-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="10245-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="10245-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="10245-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="10245-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="10245-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="10245-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="10245-116">Attribute-Id</span></span>      | <span data-ttu-id="10245-117">2.5.4.53</span><span class="sxs-lookup"><span data-stu-id="10245-117">2.5.4.53</span></span>                                              |
| <span data-ttu-id="10245-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="10245-118">System-Id-Guid</span></span>    | <span data-ttu-id="10245-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="10245-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="10245-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="10245-120">Syntax</span></span>            | [<span data-ttu-id="10245-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="10245-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="10245-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="10245-122">Implementations</span></span>

-   [<span data-ttu-id="10245-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="10245-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="10245-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="10245-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="10245-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="10245-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="10245-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="10245-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="10245-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="10245-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="10245-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="10245-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="10245-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10245-129">Windows 2000 Server</span></span>



| <span data-ttu-id="10245-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-130">Entry</span></span> | <span data-ttu-id="10245-131">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10245-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="10245-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="10245-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10245-133">MAPI-Id</span></span>                | <span data-ttu-id="10245-134">0x8C46</span><span class="sxs-lookup"><span data-stu-id="10245-134">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="10245-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="10245-135">System-Only</span></span>            | <span data-ttu-id="10245-136">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10245-137">Is-Single-Valued</span></span>       | <span data-ttu-id="10245-138">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="10245-139">Is Indexed</span></span>             | <span data-ttu-id="10245-140">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10245-141">In Global Catalog</span></span>      | <span data-ttu-id="10245-142">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10245-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="10245-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10245-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="10245-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10245-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10245-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-147">Search-Flags</span></span>           | <span data-ttu-id="10245-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-149">System-Flags</span></span>           | <span data-ttu-id="10245-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-150">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10245-151">Classes used in</span></span>        | [<span data-ttu-id="10245-152">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="10245-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="10245-153">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="10245-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="10245-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10245-154">Windows Server 2003</span></span>



| <span data-ttu-id="10245-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-155">Entry</span></span> | <span data-ttu-id="10245-156">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10245-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="10245-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="10245-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10245-158">MAPI-Id</span></span>                | <span data-ttu-id="10245-159">0x8C46</span><span class="sxs-lookup"><span data-stu-id="10245-159">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="10245-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="10245-160">System-Only</span></span>            | <span data-ttu-id="10245-161">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10245-162">Is-Single-Valued</span></span>       | <span data-ttu-id="10245-163">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="10245-164">Is Indexed</span></span>             | <span data-ttu-id="10245-165">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10245-166">In Global Catalog</span></span>      | <span data-ttu-id="10245-167">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10245-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="10245-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10245-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="10245-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10245-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10245-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-172">Search-Flags</span></span>           | <span data-ttu-id="10245-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-174">System-Flags</span></span>           | <span data-ttu-id="10245-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-175">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10245-176">Classes used in</span></span>        | [<span data-ttu-id="10245-177">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="10245-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="10245-178">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="10245-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="10245-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10245-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="10245-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-180">Entry</span></span> | <span data-ttu-id="10245-181">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10245-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="10245-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="10245-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10245-183">MAPI-Id</span></span>                | <span data-ttu-id="10245-184">0x8C46</span><span class="sxs-lookup"><span data-stu-id="10245-184">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="10245-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="10245-185">System-Only</span></span>            | <span data-ttu-id="10245-186">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10245-187">Is-Single-Valued</span></span>       | <span data-ttu-id="10245-188">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="10245-189">Is Indexed</span></span>             | <span data-ttu-id="10245-190">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10245-191">In Global Catalog</span></span>      | <span data-ttu-id="10245-192">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10245-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="10245-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10245-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="10245-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10245-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10245-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-197">Search-Flags</span></span>           | <span data-ttu-id="10245-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-199">System-Flags</span></span>           | <span data-ttu-id="10245-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10245-201">Classes used in</span></span>        | [<span data-ttu-id="10245-202">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="10245-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="10245-203">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="10245-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="10245-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10245-204">Windows Server 2008</span></span>



| <span data-ttu-id="10245-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-205">Entry</span></span> | <span data-ttu-id="10245-206">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10245-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="10245-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="10245-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10245-208">MAPI-Id</span></span>                | <span data-ttu-id="10245-209">0x8C46</span><span class="sxs-lookup"><span data-stu-id="10245-209">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="10245-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="10245-210">System-Only</span></span>            | <span data-ttu-id="10245-211">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10245-212">Is-Single-Valued</span></span>       | <span data-ttu-id="10245-213">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="10245-214">Is Indexed</span></span>             | <span data-ttu-id="10245-215">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10245-216">In Global Catalog</span></span>      | <span data-ttu-id="10245-217">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10245-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="10245-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10245-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="10245-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10245-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10245-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-222">Search-Flags</span></span>           | <span data-ttu-id="10245-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-224">System-Flags</span></span>           | <span data-ttu-id="10245-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-225">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10245-226">Classes used in</span></span>        | [<span data-ttu-id="10245-227">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="10245-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="10245-228">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="10245-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="10245-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10245-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="10245-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-230">Entry</span></span> | <span data-ttu-id="10245-231">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10245-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="10245-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="10245-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10245-233">MAPI-Id</span></span>                | <span data-ttu-id="10245-234">0x8C46</span><span class="sxs-lookup"><span data-stu-id="10245-234">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="10245-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="10245-235">System-Only</span></span>            | <span data-ttu-id="10245-236">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10245-237">Is-Single-Valued</span></span>       | <span data-ttu-id="10245-238">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="10245-239">Is Indexed</span></span>             | <span data-ttu-id="10245-240">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10245-241">In Global Catalog</span></span>      | <span data-ttu-id="10245-242">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10245-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="10245-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10245-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="10245-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10245-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10245-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-247">Search-Flags</span></span>           | <span data-ttu-id="10245-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-249">System-Flags</span></span>           | <span data-ttu-id="10245-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10245-251">Classes used in</span></span>        | [<span data-ttu-id="10245-252">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="10245-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="10245-253">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="10245-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="10245-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10245-254">Windows Server 2012</span></span>



| <span data-ttu-id="10245-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="10245-255">Entry</span></span> | <span data-ttu-id="10245-256">Valor</span><span class="sxs-lookup"><span data-stu-id="10245-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10245-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="10245-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="10245-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10245-258">MAPI-Id</span></span>                | <span data-ttu-id="10245-259">0x8C46</span><span class="sxs-lookup"><span data-stu-id="10245-259">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="10245-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="10245-260">System-Only</span></span>            | <span data-ttu-id="10245-261">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="10245-262">Is-Single-Valued</span></span>       | <span data-ttu-id="10245-263">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="10245-264">Is Indexed</span></span>             | <span data-ttu-id="10245-265">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="10245-266">In Global Catalog</span></span>      | <span data-ttu-id="10245-267">Falso</span><span class="sxs-lookup"><span data-stu-id="10245-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="10245-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="10245-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="10245-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="10245-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="10245-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10245-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10245-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="10245-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-272">Search-Flags</span></span>           | <span data-ttu-id="10245-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10245-274">System-Flags</span></span>           | <span data-ttu-id="10245-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10245-275">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="10245-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="10245-276">Classes used in</span></span>        | [<span data-ttu-id="10245-277">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="10245-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="10245-278">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="10245-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





