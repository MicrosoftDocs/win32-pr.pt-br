---
title: Atributo Certificate-Authority-Object
description: Referência à autoridade de certificação associada a um ponto de distribuição de lista de certificados revogados.
ms.assetid: 8dfd4441-6b45-4dc4-aed8-e33aa7fd099f
ms.tgt_platform: multiple
keywords:
- Certificado-autoridade-esquema de atributo de objeto do AD
- Esquema de AD do atributo certificateAuthorityObject
topic_type:
- apiref
api_name:
- Certificate-Authority-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65ffceb810cd6a4ef3033834dbf0f3c489f1506e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825429"
---
# <a name="certificate-authority-object-attribute"></a><span data-ttu-id="121ba-105">Atributo Certificate-Authority-Object</span><span class="sxs-lookup"><span data-stu-id="121ba-105">Certificate-Authority-Object attribute</span></span>

<span data-ttu-id="121ba-106">Referência à autoridade de certificação associada a um ponto de distribuição de lista de certificados revogados.</span><span class="sxs-lookup"><span data-stu-id="121ba-106">Reference to the certification authority associated with a Certificate Revocation List distribution point.</span></span>



| <span data-ttu-id="121ba-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-107">Entry</span></span> | <span data-ttu-id="121ba-108">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="121ba-109">CN</span><span class="sxs-lookup"><span data-stu-id="121ba-109">CN</span></span>                | <span data-ttu-id="121ba-110">Certificado-autoridade-objeto</span><span class="sxs-lookup"><span data-stu-id="121ba-110">Certificate-Authority-Object</span></span>            |
| <span data-ttu-id="121ba-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="121ba-111">Ldap-Display-Name</span></span> | <span data-ttu-id="121ba-112">certificateAuthorityObject</span><span class="sxs-lookup"><span data-stu-id="121ba-112">certificateAuthorityObject</span></span>              |
| <span data-ttu-id="121ba-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="121ba-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="121ba-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="121ba-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="121ba-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="121ba-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="121ba-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-116">Attribute-Id</span></span>      | <span data-ttu-id="121ba-117">1.2.840.113556.1.4.684</span><span class="sxs-lookup"><span data-stu-id="121ba-117">1.2.840.113556.1.4.684</span></span>                  |
| <span data-ttu-id="121ba-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="121ba-118">System-Id-Guid</span></span>    | <span data-ttu-id="121ba-119">963d2732-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="121ba-119">963d2732-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="121ba-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="121ba-120">Syntax</span></span>            | [<span data-ttu-id="121ba-121">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="121ba-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="121ba-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="121ba-122">Implementations</span></span>

-   [<span data-ttu-id="121ba-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="121ba-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="121ba-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="121ba-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="121ba-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="121ba-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="121ba-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="121ba-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="121ba-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="121ba-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="121ba-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="121ba-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="121ba-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="121ba-129">Windows 2000 Server</span></span>



| <span data-ttu-id="121ba-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-130">Entry</span></span> | <span data-ttu-id="121ba-131">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="121ba-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="121ba-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="121ba-134">System-Only</span></span>            | <span data-ttu-id="121ba-135">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-135">False</span></span>                                                               |
| <span data-ttu-id="121ba-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="121ba-136">Is-Single-Valued</span></span>       | <span data-ttu-id="121ba-137">True</span><span class="sxs-lookup"><span data-stu-id="121ba-137">True</span></span>                                                                |
| <span data-ttu-id="121ba-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="121ba-138">Is Indexed</span></span>             | <span data-ttu-id="121ba-139">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-139">False</span></span>                                                               |
| <span data-ttu-id="121ba-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="121ba-140">In Global Catalog</span></span>      | <span data-ttu-id="121ba-141">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-141">False</span></span>                                                               |
| <span data-ttu-id="121ba-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="121ba-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="121ba-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="121ba-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="121ba-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="121ba-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="121ba-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-146">Search-Flags</span></span>           | <span data-ttu-id="121ba-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="121ba-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="121ba-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-148">System-Flags</span></span>           | <span data-ttu-id="121ba-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="121ba-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="121ba-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="121ba-150">Classes used in</span></span>        | [<span data-ttu-id="121ba-151">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="121ba-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="121ba-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="121ba-152">Windows Server 2003</span></span>



| <span data-ttu-id="121ba-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-153">Entry</span></span> | <span data-ttu-id="121ba-154">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="121ba-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="121ba-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="121ba-157">System-Only</span></span>            | <span data-ttu-id="121ba-158">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-158">False</span></span>                                                               |
| <span data-ttu-id="121ba-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="121ba-159">Is-Single-Valued</span></span>       | <span data-ttu-id="121ba-160">True</span><span class="sxs-lookup"><span data-stu-id="121ba-160">True</span></span>                                                                |
| <span data-ttu-id="121ba-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="121ba-161">Is Indexed</span></span>             | <span data-ttu-id="121ba-162">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-162">False</span></span>                                                               |
| <span data-ttu-id="121ba-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="121ba-163">In Global Catalog</span></span>      | <span data-ttu-id="121ba-164">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-164">False</span></span>                                                               |
| <span data-ttu-id="121ba-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="121ba-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="121ba-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="121ba-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="121ba-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="121ba-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="121ba-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-169">Search-Flags</span></span>           | <span data-ttu-id="121ba-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="121ba-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="121ba-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-171">System-Flags</span></span>           | <span data-ttu-id="121ba-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="121ba-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="121ba-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="121ba-173">Classes used in</span></span>        | [<span data-ttu-id="121ba-174">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="121ba-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="121ba-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="121ba-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="121ba-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-176">Entry</span></span> | <span data-ttu-id="121ba-177">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="121ba-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="121ba-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="121ba-180">System-Only</span></span>            | <span data-ttu-id="121ba-181">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-181">False</span></span>                                                               |
| <span data-ttu-id="121ba-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="121ba-182">Is-Single-Valued</span></span>       | <span data-ttu-id="121ba-183">True</span><span class="sxs-lookup"><span data-stu-id="121ba-183">True</span></span>                                                                |
| <span data-ttu-id="121ba-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="121ba-184">Is Indexed</span></span>             | <span data-ttu-id="121ba-185">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-185">False</span></span>                                                               |
| <span data-ttu-id="121ba-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="121ba-186">In Global Catalog</span></span>      | <span data-ttu-id="121ba-187">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-187">False</span></span>                                                               |
| <span data-ttu-id="121ba-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="121ba-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="121ba-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="121ba-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="121ba-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="121ba-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="121ba-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-192">Search-Flags</span></span>           | <span data-ttu-id="121ba-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="121ba-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="121ba-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-194">System-Flags</span></span>           | <span data-ttu-id="121ba-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="121ba-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="121ba-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="121ba-196">Classes used in</span></span>        | [<span data-ttu-id="121ba-197">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="121ba-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="121ba-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="121ba-198">Windows Server 2008</span></span>



| <span data-ttu-id="121ba-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-199">Entry</span></span> | <span data-ttu-id="121ba-200">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="121ba-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="121ba-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="121ba-203">System-Only</span></span>            | <span data-ttu-id="121ba-204">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-204">False</span></span>                                                               |
| <span data-ttu-id="121ba-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="121ba-205">Is-Single-Valued</span></span>       | <span data-ttu-id="121ba-206">True</span><span class="sxs-lookup"><span data-stu-id="121ba-206">True</span></span>                                                                |
| <span data-ttu-id="121ba-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="121ba-207">Is Indexed</span></span>             | <span data-ttu-id="121ba-208">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-208">False</span></span>                                                               |
| <span data-ttu-id="121ba-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="121ba-209">In Global Catalog</span></span>      | <span data-ttu-id="121ba-210">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-210">False</span></span>                                                               |
| <span data-ttu-id="121ba-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="121ba-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="121ba-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="121ba-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="121ba-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="121ba-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="121ba-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-215">Search-Flags</span></span>           | <span data-ttu-id="121ba-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="121ba-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="121ba-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-217">System-Flags</span></span>           | <span data-ttu-id="121ba-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="121ba-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="121ba-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="121ba-219">Classes used in</span></span>        | [<span data-ttu-id="121ba-220">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="121ba-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="121ba-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="121ba-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="121ba-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-222">Entry</span></span> | <span data-ttu-id="121ba-223">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="121ba-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="121ba-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="121ba-226">System-Only</span></span>            | <span data-ttu-id="121ba-227">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-227">False</span></span>                                                               |
| <span data-ttu-id="121ba-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="121ba-228">Is-Single-Valued</span></span>       | <span data-ttu-id="121ba-229">True</span><span class="sxs-lookup"><span data-stu-id="121ba-229">True</span></span>                                                                |
| <span data-ttu-id="121ba-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="121ba-230">Is Indexed</span></span>             | <span data-ttu-id="121ba-231">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-231">False</span></span>                                                               |
| <span data-ttu-id="121ba-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="121ba-232">In Global Catalog</span></span>      | <span data-ttu-id="121ba-233">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-233">False</span></span>                                                               |
| <span data-ttu-id="121ba-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="121ba-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="121ba-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="121ba-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="121ba-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="121ba-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="121ba-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-238">Search-Flags</span></span>           | <span data-ttu-id="121ba-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="121ba-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="121ba-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-240">System-Flags</span></span>           | <span data-ttu-id="121ba-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="121ba-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="121ba-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="121ba-242">Classes used in</span></span>        | [<span data-ttu-id="121ba-243">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="121ba-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="121ba-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="121ba-244">Windows Server 2012</span></span>



| <span data-ttu-id="121ba-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="121ba-245">Entry</span></span> | <span data-ttu-id="121ba-246">Valor</span><span class="sxs-lookup"><span data-stu-id="121ba-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="121ba-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="121ba-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="121ba-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="121ba-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="121ba-249">System-Only</span></span>            | <span data-ttu-id="121ba-250">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-250">False</span></span>                                                               |
| <span data-ttu-id="121ba-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="121ba-251">Is-Single-Valued</span></span>       | <span data-ttu-id="121ba-252">True</span><span class="sxs-lookup"><span data-stu-id="121ba-252">True</span></span>                                                                |
| <span data-ttu-id="121ba-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="121ba-253">Is Indexed</span></span>             | <span data-ttu-id="121ba-254">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-254">False</span></span>                                                               |
| <span data-ttu-id="121ba-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="121ba-255">In Global Catalog</span></span>      | <span data-ttu-id="121ba-256">Falso</span><span class="sxs-lookup"><span data-stu-id="121ba-256">False</span></span>                                                               |
| <span data-ttu-id="121ba-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="121ba-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="121ba-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="121ba-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="121ba-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="121ba-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="121ba-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="121ba-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-261">Search-Flags</span></span>           | <span data-ttu-id="121ba-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="121ba-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="121ba-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="121ba-263">System-Flags</span></span>           | <span data-ttu-id="121ba-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="121ba-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="121ba-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="121ba-265">Classes used in</span></span>        | [<span data-ttu-id="121ba-266">**CRL-ponto de distribuição**</span><span class="sxs-lookup"><span data-stu-id="121ba-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 





