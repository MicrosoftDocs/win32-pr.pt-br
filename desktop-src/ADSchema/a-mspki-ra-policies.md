---
title: atributo ms-PKI-RA-Policies
description: Contém a lista de OIDs de política necessária de autoridades de registro que assinam a solicitação de registro.
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-PKI-RA-Policies
- atributo msPKI-RA-Policies do AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919597"
---
# <a name="ms-pki-ra-policies-attribute"></a><span data-ttu-id="7e819-105">atributo ms-PKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="7e819-105">ms-PKI-RA-Policies attribute</span></span>

<span data-ttu-id="7e819-106">Contém a lista de OIDs de política necessária de autoridades de registro que assinam a solicitação de registro.</span><span class="sxs-lookup"><span data-stu-id="7e819-106">Contains the list of required policy OIDs from registration authorities who sign the enrollment request.</span></span>



| <span data-ttu-id="7e819-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e819-107">Entry</span></span> | <span data-ttu-id="7e819-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7e819-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e819-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e819-109">CN</span></span>                | <span data-ttu-id="7e819-110">MS-PKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="7e819-110">ms-PKI-RA-Policies</span></span>                                                                                |
| <span data-ttu-id="7e819-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7e819-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e819-112">msPKI-RA-Policies</span><span class="sxs-lookup"><span data-stu-id="7e819-112">msPKI-RA-Policies</span></span>                                                                                 |
| <span data-ttu-id="7e819-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7e819-113">Size</span></span>              | <span data-ttu-id="7e819-114">64 bytes vezes o número de entradas.</span><span class="sxs-lookup"><span data-stu-id="7e819-114">64 bytes times the number of entries.</span></span>                                                             |
| <span data-ttu-id="7e819-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7e819-115">Update Privilege</span></span>  | <span data-ttu-id="7e819-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="7e819-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="7e819-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7e819-117">Update Frequency</span></span>  | <span data-ttu-id="7e819-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="7e819-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="7e819-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e819-119">Attribute-Id</span></span>      | <span data-ttu-id="7e819-120">1.2.840.113556.1.4.1438</span><span class="sxs-lookup"><span data-stu-id="7e819-120">1.2.840.113556.1.4.1438</span></span>                                                                           |
| <span data-ttu-id="7e819-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e819-121">System-Id-Guid</span></span>    | <span data-ttu-id="7e819-122">d546ae22-0951-4d47-817e-1c9f96faad46</span><span class="sxs-lookup"><span data-stu-id="7e819-122">d546ae22-0951-4d47-817e-1c9f96faad46</span></span>                                                              |
| <span data-ttu-id="7e819-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e819-123">Syntax</span></span>            | [<span data-ttu-id="7e819-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7e819-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="7e819-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="7e819-125">Implementations</span></span>

-   [<span data-ttu-id="7e819-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e819-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e819-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e819-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e819-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e819-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e819-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e819-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e819-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e819-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7e819-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e819-131">Windows Server 2003</span></span>



| <span data-ttu-id="7e819-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e819-132">Entry</span></span> | <span data-ttu-id="7e819-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7e819-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7e819-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="7e819-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e819-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e819-136">System-Only</span></span>            | <span data-ttu-id="7e819-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-137">False</span></span>                                                                   |
| <span data-ttu-id="7e819-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7e819-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7e819-139">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-139">False</span></span>                                                                   |
| <span data-ttu-id="7e819-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="7e819-140">Is Indexed</span></span>             | <span data-ttu-id="7e819-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-141">False</span></span>                                                                   |
| <span data-ttu-id="7e819-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e819-142">In Global Catalog</span></span>      | <span data-ttu-id="7e819-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-143">False</span></span>                                                                   |
| <span data-ttu-id="7e819-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7e819-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e819-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7e819-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7e819-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e819-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e819-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-148">Search-Flags</span></span>           | <span data-ttu-id="7e819-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e819-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="7e819-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-150">System-Flags</span></span>           | <span data-ttu-id="7e819-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e819-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="7e819-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7e819-152">Classes used in</span></span>        | [<span data-ttu-id="7e819-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7e819-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e819-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e819-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e819-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e819-155">Entry</span></span> | <span data-ttu-id="7e819-156">Valor</span><span class="sxs-lookup"><span data-stu-id="7e819-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7e819-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="7e819-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e819-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e819-159">System-Only</span></span>            | <span data-ttu-id="7e819-160">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-160">False</span></span>                                                                   |
| <span data-ttu-id="7e819-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7e819-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7e819-162">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-162">False</span></span>                                                                   |
| <span data-ttu-id="7e819-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="7e819-163">Is Indexed</span></span>             | <span data-ttu-id="7e819-164">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-164">False</span></span>                                                                   |
| <span data-ttu-id="7e819-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e819-165">In Global Catalog</span></span>      | <span data-ttu-id="7e819-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-166">False</span></span>                                                                   |
| <span data-ttu-id="7e819-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7e819-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e819-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7e819-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7e819-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e819-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e819-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-171">Search-Flags</span></span>           | <span data-ttu-id="7e819-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e819-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="7e819-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-173">System-Flags</span></span>           | <span data-ttu-id="7e819-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e819-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="7e819-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7e819-175">Classes used in</span></span>        | [<span data-ttu-id="7e819-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7e819-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e819-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e819-177">Windows Server 2008</span></span>



| <span data-ttu-id="7e819-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e819-178">Entry</span></span> | <span data-ttu-id="7e819-179">Valor</span><span class="sxs-lookup"><span data-stu-id="7e819-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7e819-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="7e819-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e819-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e819-182">System-Only</span></span>            | <span data-ttu-id="7e819-183">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-183">False</span></span>                                                                   |
| <span data-ttu-id="7e819-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7e819-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7e819-185">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-185">False</span></span>                                                                   |
| <span data-ttu-id="7e819-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="7e819-186">Is Indexed</span></span>             | <span data-ttu-id="7e819-187">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-187">False</span></span>                                                                   |
| <span data-ttu-id="7e819-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e819-188">In Global Catalog</span></span>      | <span data-ttu-id="7e819-189">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-189">False</span></span>                                                                   |
| <span data-ttu-id="7e819-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7e819-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e819-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7e819-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7e819-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e819-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e819-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-194">Search-Flags</span></span>           | <span data-ttu-id="7e819-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e819-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="7e819-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-196">System-Flags</span></span>           | <span data-ttu-id="7e819-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e819-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="7e819-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7e819-198">Classes used in</span></span>        | [<span data-ttu-id="7e819-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7e819-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e819-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e819-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e819-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e819-201">Entry</span></span> | <span data-ttu-id="7e819-202">Valor</span><span class="sxs-lookup"><span data-stu-id="7e819-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7e819-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="7e819-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e819-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e819-205">System-Only</span></span>            | <span data-ttu-id="7e819-206">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-206">False</span></span>                                                                   |
| <span data-ttu-id="7e819-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7e819-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7e819-208">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-208">False</span></span>                                                                   |
| <span data-ttu-id="7e819-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="7e819-209">Is Indexed</span></span>             | <span data-ttu-id="7e819-210">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-210">False</span></span>                                                                   |
| <span data-ttu-id="7e819-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e819-211">In Global Catalog</span></span>      | <span data-ttu-id="7e819-212">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-212">False</span></span>                                                                   |
| <span data-ttu-id="7e819-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7e819-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e819-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7e819-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7e819-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e819-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e819-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-217">Search-Flags</span></span>           | <span data-ttu-id="7e819-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e819-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="7e819-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-219">System-Flags</span></span>           | <span data-ttu-id="7e819-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e819-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="7e819-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7e819-221">Classes used in</span></span>        | [<span data-ttu-id="7e819-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7e819-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e819-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e819-223">Windows Server 2012</span></span>



| <span data-ttu-id="7e819-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e819-224">Entry</span></span> | <span data-ttu-id="7e819-225">Valor</span><span class="sxs-lookup"><span data-stu-id="7e819-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7e819-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="7e819-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e819-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7e819-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e819-228">System-Only</span></span>            | <span data-ttu-id="7e819-229">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-229">False</span></span>                                                                   |
| <span data-ttu-id="7e819-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7e819-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7e819-231">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-231">False</span></span>                                                                   |
| <span data-ttu-id="7e819-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="7e819-232">Is Indexed</span></span>             | <span data-ttu-id="7e819-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-233">False</span></span>                                                                   |
| <span data-ttu-id="7e819-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e819-234">In Global Catalog</span></span>      | <span data-ttu-id="7e819-235">Falso</span><span class="sxs-lookup"><span data-stu-id="7e819-235">False</span></span>                                                                   |
| <span data-ttu-id="7e819-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7e819-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e819-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7e819-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7e819-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e819-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e819-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7e819-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-240">Search-Flags</span></span>           | <span data-ttu-id="7e819-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e819-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="7e819-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e819-242">System-Flags</span></span>           | <span data-ttu-id="7e819-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e819-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="7e819-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7e819-244">Classes used in</span></span>        | [<span data-ttu-id="7e819-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7e819-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





