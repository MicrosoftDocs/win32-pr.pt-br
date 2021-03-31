---
title: atributo ms-PKI-Certificate-Policy
description: Contém a lista de OIDs de política e seus CSPs opcionais no certificado emitido.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-PKI-Certificate-Policy
- Esquema de msPKI de atributo de política de certificado
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2d6857b6035cc72271c7276b679b8a497aaab9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825155"
---
# <a name="ms-pki-certificate-policy-attribute"></a><span data-ttu-id="cd543-105">atributo ms-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="cd543-105">ms-PKI-Certificate-Policy attribute</span></span>

<span data-ttu-id="cd543-106">Contém a lista de OIDs de política e seus CSPs opcionais no certificado emitido.</span><span class="sxs-lookup"><span data-stu-id="cd543-106">Contains the list of policy OIDs and their optional CSPs in the issued certificate.</span></span>



| <span data-ttu-id="cd543-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd543-107">Entry</span></span> | <span data-ttu-id="cd543-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cd543-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd543-109">CN</span><span class="sxs-lookup"><span data-stu-id="cd543-109">CN</span></span>                | <span data-ttu-id="cd543-110">MS-PKI-Certificate-Policy</span><span class="sxs-lookup"><span data-stu-id="cd543-110">ms-PKI-Certificate-Policy</span></span>                                                                         |
| <span data-ttu-id="cd543-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cd543-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cd543-112">msPKI-certificado-política</span><span class="sxs-lookup"><span data-stu-id="cd543-112">msPKI-Certificate-Policy</span></span>                                                                          |
| <span data-ttu-id="cd543-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cd543-113">Size</span></span>              | <span data-ttu-id="cd543-114">64 bytes vezes o número de entradas.</span><span class="sxs-lookup"><span data-stu-id="cd543-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="cd543-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="cd543-115">Update Privilege</span></span>  | <span data-ttu-id="cd543-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="cd543-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="cd543-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="cd543-117">Update Frequency</span></span>  | <span data-ttu-id="cd543-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="cd543-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="cd543-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd543-119">Attribute-Id</span></span>      | <span data-ttu-id="cd543-120">1.2.840.113556.1.4.1439</span><span class="sxs-lookup"><span data-stu-id="cd543-120">1.2.840.113556.1.4.1439</span></span>                                                                           |
| <span data-ttu-id="cd543-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cd543-121">System-Id-Guid</span></span>    | <span data-ttu-id="cd543-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span><span class="sxs-lookup"><span data-stu-id="cd543-122">38942346-cc5b-424b-a7d8-6ffd12029c5f</span></span>                                                              |
| <span data-ttu-id="cd543-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd543-123">Syntax</span></span>            | [<span data-ttu-id="cd543-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cd543-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="cd543-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="cd543-125">Implementations</span></span>

-   [<span data-ttu-id="cd543-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cd543-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cd543-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cd543-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cd543-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd543-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd543-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd543-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd543-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd543-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cd543-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd543-131">Windows Server 2003</span></span>



| <span data-ttu-id="cd543-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd543-132">Entry</span></span> | <span data-ttu-id="cd543-133">Valor</span><span class="sxs-lookup"><span data-stu-id="cd543-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cd543-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="cd543-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd543-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd543-136">System-Only</span></span>            | <span data-ttu-id="cd543-137">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-137">False</span></span>                                                                   |
| <span data-ttu-id="cd543-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cd543-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cd543-139">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-139">False</span></span>                                                                   |
| <span data-ttu-id="cd543-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="cd543-140">Is Indexed</span></span>             | <span data-ttu-id="cd543-141">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-141">False</span></span>                                                                   |
| <span data-ttu-id="cd543-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd543-142">In Global Catalog</span></span>      | <span data-ttu-id="cd543-143">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-143">False</span></span>                                                                   |
| <span data-ttu-id="cd543-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd543-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd543-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cd543-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cd543-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd543-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd543-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-148">Search-Flags</span></span>           | <span data-ttu-id="cd543-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd543-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="cd543-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-150">System-Flags</span></span>           | <span data-ttu-id="cd543-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd543-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="cd543-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cd543-152">Classes used in</span></span>        | [<span data-ttu-id="cd543-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="cd543-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cd543-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cd543-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cd543-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd543-155">Entry</span></span> | <span data-ttu-id="cd543-156">Valor</span><span class="sxs-lookup"><span data-stu-id="cd543-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cd543-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="cd543-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd543-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd543-159">System-Only</span></span>            | <span data-ttu-id="cd543-160">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-160">False</span></span>                                                                   |
| <span data-ttu-id="cd543-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cd543-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cd543-162">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-162">False</span></span>                                                                   |
| <span data-ttu-id="cd543-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="cd543-163">Is Indexed</span></span>             | <span data-ttu-id="cd543-164">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-164">False</span></span>                                                                   |
| <span data-ttu-id="cd543-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd543-165">In Global Catalog</span></span>      | <span data-ttu-id="cd543-166">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-166">False</span></span>                                                                   |
| <span data-ttu-id="cd543-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd543-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd543-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cd543-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cd543-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd543-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd543-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-171">Search-Flags</span></span>           | <span data-ttu-id="cd543-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd543-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="cd543-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-173">System-Flags</span></span>           | <span data-ttu-id="cd543-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd543-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="cd543-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cd543-175">Classes used in</span></span>        | [<span data-ttu-id="cd543-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="cd543-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cd543-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd543-177">Windows Server 2008</span></span>



| <span data-ttu-id="cd543-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd543-178">Entry</span></span> | <span data-ttu-id="cd543-179">Valor</span><span class="sxs-lookup"><span data-stu-id="cd543-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cd543-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="cd543-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd543-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd543-182">System-Only</span></span>            | <span data-ttu-id="cd543-183">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-183">False</span></span>                                                                   |
| <span data-ttu-id="cd543-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cd543-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cd543-185">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-185">False</span></span>                                                                   |
| <span data-ttu-id="cd543-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="cd543-186">Is Indexed</span></span>             | <span data-ttu-id="cd543-187">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-187">False</span></span>                                                                   |
| <span data-ttu-id="cd543-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd543-188">In Global Catalog</span></span>      | <span data-ttu-id="cd543-189">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-189">False</span></span>                                                                   |
| <span data-ttu-id="cd543-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd543-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd543-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cd543-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cd543-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd543-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd543-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-194">Search-Flags</span></span>           | <span data-ttu-id="cd543-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd543-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="cd543-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-196">System-Flags</span></span>           | <span data-ttu-id="cd543-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd543-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="cd543-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cd543-198">Classes used in</span></span>        | [<span data-ttu-id="cd543-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="cd543-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd543-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd543-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd543-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd543-201">Entry</span></span> | <span data-ttu-id="cd543-202">Valor</span><span class="sxs-lookup"><span data-stu-id="cd543-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cd543-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="cd543-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd543-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd543-205">System-Only</span></span>            | <span data-ttu-id="cd543-206">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-206">False</span></span>                                                                   |
| <span data-ttu-id="cd543-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cd543-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cd543-208">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-208">False</span></span>                                                                   |
| <span data-ttu-id="cd543-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="cd543-209">Is Indexed</span></span>             | <span data-ttu-id="cd543-210">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-210">False</span></span>                                                                   |
| <span data-ttu-id="cd543-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd543-211">In Global Catalog</span></span>      | <span data-ttu-id="cd543-212">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-212">False</span></span>                                                                   |
| <span data-ttu-id="cd543-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd543-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd543-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cd543-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cd543-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd543-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd543-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-217">Search-Flags</span></span>           | <span data-ttu-id="cd543-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd543-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="cd543-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-219">System-Flags</span></span>           | <span data-ttu-id="cd543-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd543-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="cd543-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cd543-221">Classes used in</span></span>        | [<span data-ttu-id="cd543-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="cd543-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd543-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd543-223">Windows Server 2012</span></span>



| <span data-ttu-id="cd543-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd543-224">Entry</span></span> | <span data-ttu-id="cd543-225">Valor</span><span class="sxs-lookup"><span data-stu-id="cd543-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cd543-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="cd543-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd543-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cd543-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd543-228">System-Only</span></span>            | <span data-ttu-id="cd543-229">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-229">False</span></span>                                                                   |
| <span data-ttu-id="cd543-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cd543-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cd543-231">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-231">False</span></span>                                                                   |
| <span data-ttu-id="cd543-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="cd543-232">Is Indexed</span></span>             | <span data-ttu-id="cd543-233">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-233">False</span></span>                                                                   |
| <span data-ttu-id="cd543-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cd543-234">In Global Catalog</span></span>      | <span data-ttu-id="cd543-235">Falso</span><span class="sxs-lookup"><span data-stu-id="cd543-235">False</span></span>                                                                   |
| <span data-ttu-id="cd543-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cd543-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd543-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cd543-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cd543-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd543-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd543-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cd543-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-240">Search-Flags</span></span>           | <span data-ttu-id="cd543-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cd543-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="cd543-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd543-242">System-Flags</span></span>           | <span data-ttu-id="cd543-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd543-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="cd543-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cd543-244">Classes used in</span></span>        | [<span data-ttu-id="cd543-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="cd543-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





