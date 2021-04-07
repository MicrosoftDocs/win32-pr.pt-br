---
title: atributo ms-PKI-Enroll-Flag
description: Contém os sinalizadores relacionados ao registro.
ms.assetid: e854acb1-75f4-4379-b404-8fa096419ee6
ms.tgt_platform: multiple
keywords:
- MS-PKI-registro-Flag atributo AD Schema
- msPKI-registro-sinalizador de atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-Enrollment-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2df092e28633bd5825c422e306bf7a65982b32a8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919469"
---
# <a name="ms-pki-enrollment-flag-attribute"></a><span data-ttu-id="16ccf-105">atributo ms-PKI-Enroll-Flag</span><span class="sxs-lookup"><span data-stu-id="16ccf-105">ms-PKI-Enrollment-Flag attribute</span></span>

<span data-ttu-id="16ccf-106">Contém os sinalizadores relacionados ao registro.</span><span class="sxs-lookup"><span data-stu-id="16ccf-106">Contains the enrollment related flags.</span></span>



| <span data-ttu-id="16ccf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="16ccf-107">Entry</span></span> | <span data-ttu-id="16ccf-108">Valor</span><span class="sxs-lookup"><span data-stu-id="16ccf-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16ccf-109">CN</span><span class="sxs-lookup"><span data-stu-id="16ccf-109">CN</span></span>                | <span data-ttu-id="16ccf-110">MS-PKI-Enrollment-Flag</span><span class="sxs-lookup"><span data-stu-id="16ccf-110">ms-PKI-Enrollment-Flag</span></span>                                                                            |
| <span data-ttu-id="16ccf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="16ccf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="16ccf-112">msPKI-sinalizador de registro</span><span class="sxs-lookup"><span data-stu-id="16ccf-112">msPKI-Enrollment-Flag</span></span>                                                                             |
| <span data-ttu-id="16ccf-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="16ccf-113">Size</span></span>              | <span data-ttu-id="16ccf-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="16ccf-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="16ccf-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="16ccf-115">Update Privilege</span></span>  | <span data-ttu-id="16ccf-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="16ccf-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="16ccf-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="16ccf-117">Update Frequency</span></span>  | <span data-ttu-id="16ccf-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="16ccf-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="16ccf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="16ccf-119">Attribute-Id</span></span>      | <span data-ttu-id="16ccf-120">1.2.840.113556.1.4.1430</span><span class="sxs-lookup"><span data-stu-id="16ccf-120">1.2.840.113556.1.4.1430</span></span>                                                                           |
| <span data-ttu-id="16ccf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="16ccf-121">System-Id-Guid</span></span>    | <span data-ttu-id="16ccf-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span><span class="sxs-lookup"><span data-stu-id="16ccf-122">d15ef7d8-f226-46db-ae79-b34e560bd12c</span></span>                                                              |
| <span data-ttu-id="16ccf-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="16ccf-123">Syntax</span></span>            | [<span data-ttu-id="16ccf-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="16ccf-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="16ccf-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="16ccf-125">Implementations</span></span>

-   [<span data-ttu-id="16ccf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="16ccf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="16ccf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="16ccf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="16ccf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="16ccf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="16ccf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="16ccf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="16ccf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="16ccf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="16ccf-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16ccf-131">Windows Server 2003</span></span>



| <span data-ttu-id="16ccf-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="16ccf-132">Entry</span></span> | <span data-ttu-id="16ccf-133">Valor</span><span class="sxs-lookup"><span data-stu-id="16ccf-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="16ccf-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="16ccf-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16ccf-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="16ccf-136">System-Only</span></span>            | <span data-ttu-id="16ccf-137">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-137">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16ccf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="16ccf-139">True</span><span class="sxs-lookup"><span data-stu-id="16ccf-139">True</span></span>                                                                    |
| <span data-ttu-id="16ccf-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="16ccf-140">Is Indexed</span></span>             | <span data-ttu-id="16ccf-141">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-141">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16ccf-142">In Global Catalog</span></span>      | <span data-ttu-id="16ccf-143">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-143">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16ccf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="16ccf-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16ccf-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="16ccf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16ccf-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16ccf-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-148">Search-Flags</span></span>           | <span data-ttu-id="16ccf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16ccf-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="16ccf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-150">System-Flags</span></span>           | <span data-ttu-id="16ccf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16ccf-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="16ccf-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16ccf-152">Classes used in</span></span>        | [<span data-ttu-id="16ccf-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="16ccf-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="16ccf-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="16ccf-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="16ccf-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="16ccf-155">Entry</span></span> | <span data-ttu-id="16ccf-156">Valor</span><span class="sxs-lookup"><span data-stu-id="16ccf-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="16ccf-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="16ccf-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16ccf-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="16ccf-159">System-Only</span></span>            | <span data-ttu-id="16ccf-160">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-160">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16ccf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="16ccf-162">True</span><span class="sxs-lookup"><span data-stu-id="16ccf-162">True</span></span>                                                                    |
| <span data-ttu-id="16ccf-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="16ccf-163">Is Indexed</span></span>             | <span data-ttu-id="16ccf-164">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-164">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16ccf-165">In Global Catalog</span></span>      | <span data-ttu-id="16ccf-166">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-166">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16ccf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="16ccf-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16ccf-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="16ccf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16ccf-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16ccf-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-171">Search-Flags</span></span>           | <span data-ttu-id="16ccf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16ccf-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="16ccf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-173">System-Flags</span></span>           | <span data-ttu-id="16ccf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16ccf-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="16ccf-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16ccf-175">Classes used in</span></span>        | [<span data-ttu-id="16ccf-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="16ccf-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="16ccf-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16ccf-177">Windows Server 2008</span></span>



| <span data-ttu-id="16ccf-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="16ccf-178">Entry</span></span> | <span data-ttu-id="16ccf-179">Valor</span><span class="sxs-lookup"><span data-stu-id="16ccf-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="16ccf-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="16ccf-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16ccf-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="16ccf-182">System-Only</span></span>            | <span data-ttu-id="16ccf-183">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-183">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16ccf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="16ccf-185">True</span><span class="sxs-lookup"><span data-stu-id="16ccf-185">True</span></span>                                                                    |
| <span data-ttu-id="16ccf-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="16ccf-186">Is Indexed</span></span>             | <span data-ttu-id="16ccf-187">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-187">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16ccf-188">In Global Catalog</span></span>      | <span data-ttu-id="16ccf-189">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-189">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16ccf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="16ccf-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16ccf-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="16ccf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16ccf-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16ccf-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-194">Search-Flags</span></span>           | <span data-ttu-id="16ccf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16ccf-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="16ccf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-196">System-Flags</span></span>           | <span data-ttu-id="16ccf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16ccf-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="16ccf-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16ccf-198">Classes used in</span></span>        | [<span data-ttu-id="16ccf-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="16ccf-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="16ccf-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16ccf-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="16ccf-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="16ccf-201">Entry</span></span> | <span data-ttu-id="16ccf-202">Valor</span><span class="sxs-lookup"><span data-stu-id="16ccf-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="16ccf-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="16ccf-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16ccf-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="16ccf-205">System-Only</span></span>            | <span data-ttu-id="16ccf-206">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-206">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16ccf-207">Is-Single-Valued</span></span>       | <span data-ttu-id="16ccf-208">True</span><span class="sxs-lookup"><span data-stu-id="16ccf-208">True</span></span>                                                                    |
| <span data-ttu-id="16ccf-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="16ccf-209">Is Indexed</span></span>             | <span data-ttu-id="16ccf-210">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-210">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16ccf-211">In Global Catalog</span></span>      | <span data-ttu-id="16ccf-212">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-212">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16ccf-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="16ccf-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16ccf-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="16ccf-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16ccf-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16ccf-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-217">Search-Flags</span></span>           | <span data-ttu-id="16ccf-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16ccf-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="16ccf-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-219">System-Flags</span></span>           | <span data-ttu-id="16ccf-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16ccf-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="16ccf-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16ccf-221">Classes used in</span></span>        | [<span data-ttu-id="16ccf-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="16ccf-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="16ccf-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16ccf-223">Windows Server 2012</span></span>



| <span data-ttu-id="16ccf-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="16ccf-224">Entry</span></span> | <span data-ttu-id="16ccf-225">Valor</span><span class="sxs-lookup"><span data-stu-id="16ccf-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="16ccf-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="16ccf-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16ccf-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="16ccf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="16ccf-228">System-Only</span></span>            | <span data-ttu-id="16ccf-229">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-229">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="16ccf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="16ccf-231">True</span><span class="sxs-lookup"><span data-stu-id="16ccf-231">True</span></span>                                                                    |
| <span data-ttu-id="16ccf-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="16ccf-232">Is Indexed</span></span>             | <span data-ttu-id="16ccf-233">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-233">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="16ccf-234">In Global Catalog</span></span>      | <span data-ttu-id="16ccf-235">Falso</span><span class="sxs-lookup"><span data-stu-id="16ccf-235">False</span></span>                                                                   |
| <span data-ttu-id="16ccf-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="16ccf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="16ccf-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="16ccf-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="16ccf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16ccf-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16ccf-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="16ccf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-240">Search-Flags</span></span>           | <span data-ttu-id="16ccf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16ccf-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="16ccf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16ccf-242">System-Flags</span></span>           | <span data-ttu-id="16ccf-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16ccf-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="16ccf-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="16ccf-244">Classes used in</span></span>        | [<span data-ttu-id="16ccf-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="16ccf-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





