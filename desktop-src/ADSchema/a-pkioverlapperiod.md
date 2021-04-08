---
title: PKI – atributo de período de sobreposição
description: O período pelo qual o certificado deve ser renovado antes de expirar.
ms.assetid: 394c78b2-7476-4c2d-9a95-f781c779ea4d
ms.tgt_platform: multiple
keywords:
- PKI-sobrepor-atributo de período esquema do AD
- Esquema de AD do atributo pKIOverlapPeriod
topic_type:
- apiref
api_name:
- PKI-Overlap-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad34a30086c4a6de8f96ae18e99c2f8a71682ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825102"
---
# <a name="pki-overlap-period-attribute"></a><span data-ttu-id="64f61-105">PKI – atributo de período de sobreposição</span><span class="sxs-lookup"><span data-stu-id="64f61-105">PKI-Overlap-Period attribute</span></span>

<span data-ttu-id="64f61-106">O período pelo qual o certificado deve ser renovado antes de expirar.</span><span class="sxs-lookup"><span data-stu-id="64f61-106">The period by when the certificate should be renewed before it is expired.</span></span>



| <span data-ttu-id="64f61-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-107">Entry</span></span> | <span data-ttu-id="64f61-108">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="64f61-109">CN</span><span class="sxs-lookup"><span data-stu-id="64f61-109">CN</span></span>                | <span data-ttu-id="64f61-110">PKI-sobreposição-período</span><span class="sxs-lookup"><span data-stu-id="64f61-110">PKI-Overlap-Period</span></span>                                    |
| <span data-ttu-id="64f61-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64f61-111">Ldap-Display-Name</span></span> | <span data-ttu-id="64f61-112">pKIOverlapPeriod</span><span class="sxs-lookup"><span data-stu-id="64f61-112">pKIOverlapPeriod</span></span>                                      |
| <span data-ttu-id="64f61-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="64f61-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="64f61-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="64f61-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="64f61-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="64f61-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="64f61-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-116">Attribute-Id</span></span>      | <span data-ttu-id="64f61-117">1.2.840.113556.1.4.1332</span><span class="sxs-lookup"><span data-stu-id="64f61-117">1.2.840.113556.1.4.1332</span></span>                               |
| <span data-ttu-id="64f61-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64f61-118">System-Id-Guid</span></span>    | <span data-ttu-id="64f61-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="64f61-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="64f61-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f61-120">Syntax</span></span>            | [<span data-ttu-id="64f61-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="64f61-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="64f61-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="64f61-122">Implementations</span></span>

-   [<span data-ttu-id="64f61-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64f61-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64f61-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64f61-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64f61-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64f61-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64f61-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64f61-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64f61-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64f61-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64f61-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64f61-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64f61-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64f61-129">Windows 2000 Server</span></span>



| <span data-ttu-id="64f61-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-130">Entry</span></span> | <span data-ttu-id="64f61-131">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="64f61-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="64f61-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f61-134">System-Only</span></span>            | <span data-ttu-id="64f61-135">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-135">False</span></span>                                                                   |
| <span data-ttu-id="64f61-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64f61-136">Is-Single-Valued</span></span>       | <span data-ttu-id="64f61-137">True</span><span class="sxs-lookup"><span data-stu-id="64f61-137">True</span></span>                                                                    |
| <span data-ttu-id="64f61-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="64f61-138">Is Indexed</span></span>             | <span data-ttu-id="64f61-139">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-139">False</span></span>                                                                   |
| <span data-ttu-id="64f61-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64f61-140">In Global Catalog</span></span>      | <span data-ttu-id="64f61-141">True</span><span class="sxs-lookup"><span data-stu-id="64f61-141">True</span></span>                                                                    |
| <span data-ttu-id="64f61-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64f61-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f61-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64f61-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="64f61-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f61-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f61-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-146">Search-Flags</span></span>           | <span data-ttu-id="64f61-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f61-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="64f61-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-148">System-Flags</span></span>           | <span data-ttu-id="64f61-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f61-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="64f61-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64f61-150">Classes used in</span></span>        | [<span data-ttu-id="64f61-151">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="64f61-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64f61-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64f61-152">Windows Server 2003</span></span>



| <span data-ttu-id="64f61-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-153">Entry</span></span> | <span data-ttu-id="64f61-154">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="64f61-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="64f61-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f61-157">System-Only</span></span>            | <span data-ttu-id="64f61-158">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-158">False</span></span>                                                                   |
| <span data-ttu-id="64f61-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64f61-159">Is-Single-Valued</span></span>       | <span data-ttu-id="64f61-160">True</span><span class="sxs-lookup"><span data-stu-id="64f61-160">True</span></span>                                                                    |
| <span data-ttu-id="64f61-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="64f61-161">Is Indexed</span></span>             | <span data-ttu-id="64f61-162">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-162">False</span></span>                                                                   |
| <span data-ttu-id="64f61-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64f61-163">In Global Catalog</span></span>      | <span data-ttu-id="64f61-164">True</span><span class="sxs-lookup"><span data-stu-id="64f61-164">True</span></span>                                                                    |
| <span data-ttu-id="64f61-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64f61-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f61-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64f61-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="64f61-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f61-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f61-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-169">Search-Flags</span></span>           | <span data-ttu-id="64f61-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f61-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="64f61-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-171">System-Flags</span></span>           | <span data-ttu-id="64f61-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f61-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="64f61-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64f61-173">Classes used in</span></span>        | [<span data-ttu-id="64f61-174">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="64f61-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64f61-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64f61-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64f61-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-176">Entry</span></span> | <span data-ttu-id="64f61-177">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="64f61-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="64f61-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f61-180">System-Only</span></span>            | <span data-ttu-id="64f61-181">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-181">False</span></span>                                                                   |
| <span data-ttu-id="64f61-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64f61-182">Is-Single-Valued</span></span>       | <span data-ttu-id="64f61-183">True</span><span class="sxs-lookup"><span data-stu-id="64f61-183">True</span></span>                                                                    |
| <span data-ttu-id="64f61-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="64f61-184">Is Indexed</span></span>             | <span data-ttu-id="64f61-185">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-185">False</span></span>                                                                   |
| <span data-ttu-id="64f61-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64f61-186">In Global Catalog</span></span>      | <span data-ttu-id="64f61-187">True</span><span class="sxs-lookup"><span data-stu-id="64f61-187">True</span></span>                                                                    |
| <span data-ttu-id="64f61-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64f61-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f61-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64f61-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="64f61-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f61-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f61-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-192">Search-Flags</span></span>           | <span data-ttu-id="64f61-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f61-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="64f61-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-194">System-Flags</span></span>           | <span data-ttu-id="64f61-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f61-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="64f61-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64f61-196">Classes used in</span></span>        | [<span data-ttu-id="64f61-197">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="64f61-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64f61-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64f61-198">Windows Server 2008</span></span>



| <span data-ttu-id="64f61-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-199">Entry</span></span> | <span data-ttu-id="64f61-200">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="64f61-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="64f61-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f61-203">System-Only</span></span>            | <span data-ttu-id="64f61-204">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-204">False</span></span>                                                                   |
| <span data-ttu-id="64f61-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64f61-205">Is-Single-Valued</span></span>       | <span data-ttu-id="64f61-206">True</span><span class="sxs-lookup"><span data-stu-id="64f61-206">True</span></span>                                                                    |
| <span data-ttu-id="64f61-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="64f61-207">Is Indexed</span></span>             | <span data-ttu-id="64f61-208">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-208">False</span></span>                                                                   |
| <span data-ttu-id="64f61-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64f61-209">In Global Catalog</span></span>      | <span data-ttu-id="64f61-210">True</span><span class="sxs-lookup"><span data-stu-id="64f61-210">True</span></span>                                                                    |
| <span data-ttu-id="64f61-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64f61-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f61-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64f61-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="64f61-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f61-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f61-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-215">Search-Flags</span></span>           | <span data-ttu-id="64f61-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f61-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="64f61-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-217">System-Flags</span></span>           | <span data-ttu-id="64f61-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f61-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="64f61-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64f61-219">Classes used in</span></span>        | [<span data-ttu-id="64f61-220">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="64f61-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64f61-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64f61-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64f61-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-222">Entry</span></span> | <span data-ttu-id="64f61-223">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="64f61-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="64f61-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f61-226">System-Only</span></span>            | <span data-ttu-id="64f61-227">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-227">False</span></span>                                                                   |
| <span data-ttu-id="64f61-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64f61-228">Is-Single-Valued</span></span>       | <span data-ttu-id="64f61-229">True</span><span class="sxs-lookup"><span data-stu-id="64f61-229">True</span></span>                                                                    |
| <span data-ttu-id="64f61-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="64f61-230">Is Indexed</span></span>             | <span data-ttu-id="64f61-231">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-231">False</span></span>                                                                   |
| <span data-ttu-id="64f61-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64f61-232">In Global Catalog</span></span>      | <span data-ttu-id="64f61-233">True</span><span class="sxs-lookup"><span data-stu-id="64f61-233">True</span></span>                                                                    |
| <span data-ttu-id="64f61-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64f61-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f61-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64f61-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="64f61-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f61-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f61-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-238">Search-Flags</span></span>           | <span data-ttu-id="64f61-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f61-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="64f61-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-240">System-Flags</span></span>           | <span data-ttu-id="64f61-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f61-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="64f61-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64f61-242">Classes used in</span></span>        | [<span data-ttu-id="64f61-243">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="64f61-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64f61-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64f61-244">Windows Server 2012</span></span>



| <span data-ttu-id="64f61-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="64f61-245">Entry</span></span> | <span data-ttu-id="64f61-246">Valor</span><span class="sxs-lookup"><span data-stu-id="64f61-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="64f61-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="64f61-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f61-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="64f61-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f61-249">System-Only</span></span>            | <span data-ttu-id="64f61-250">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-250">False</span></span>                                                                   |
| <span data-ttu-id="64f61-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64f61-251">Is-Single-Valued</span></span>       | <span data-ttu-id="64f61-252">True</span><span class="sxs-lookup"><span data-stu-id="64f61-252">True</span></span>                                                                    |
| <span data-ttu-id="64f61-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="64f61-253">Is Indexed</span></span>             | <span data-ttu-id="64f61-254">Falso</span><span class="sxs-lookup"><span data-stu-id="64f61-254">False</span></span>                                                                   |
| <span data-ttu-id="64f61-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64f61-255">In Global Catalog</span></span>      | <span data-ttu-id="64f61-256">True</span><span class="sxs-lookup"><span data-stu-id="64f61-256">True</span></span>                                                                    |
| <span data-ttu-id="64f61-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64f61-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f61-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64f61-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="64f61-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f61-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f61-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="64f61-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-261">Search-Flags</span></span>           | <span data-ttu-id="64f61-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f61-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="64f61-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f61-263">System-Flags</span></span>           | <span data-ttu-id="64f61-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f61-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="64f61-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64f61-265">Classes used in</span></span>        | [<span data-ttu-id="64f61-266">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="64f61-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





