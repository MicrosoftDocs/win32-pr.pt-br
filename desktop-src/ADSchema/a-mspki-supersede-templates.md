---
title: MS-PKI-precedência-atributo-templates
description: Especifica os nomes dos modelos de certificado que são substituídos pelo modelo atual.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- MS-PKI-precedência-templates atributo AD Schema
- msPKI-esquema de atributos do atributo de substituição-modelos
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd11ac2b96846912b0c6b1e8d01c6fd558f5f6db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499976"
---
# <a name="ms-pki-supersede-templates-attribute"></a><span data-ttu-id="92807-105">MS-PKI-precedência-atributo-templates</span><span class="sxs-lookup"><span data-stu-id="92807-105">ms-PKI-Supersede-Templates attribute</span></span>

<span data-ttu-id="92807-106">Especifica os nomes dos modelos de certificado que são substituídos pelo modelo atual.</span><span class="sxs-lookup"><span data-stu-id="92807-106">Specifies the names of the certificate templates that are superseded by the current template.</span></span>



| <span data-ttu-id="92807-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="92807-107">Entry</span></span> | <span data-ttu-id="92807-108">Valor</span><span class="sxs-lookup"><span data-stu-id="92807-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92807-109">CN</span><span class="sxs-lookup"><span data-stu-id="92807-109">CN</span></span>                | <span data-ttu-id="92807-110">MS-PKI-precedência-modelos</span><span class="sxs-lookup"><span data-stu-id="92807-110">ms-PKI-Supersede-Templates</span></span>                                                                        |
| <span data-ttu-id="92807-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="92807-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92807-112">msPKI-substituir-modelos</span><span class="sxs-lookup"><span data-stu-id="92807-112">msPKI-Supersede-Templates</span></span>                                                                         |
| <span data-ttu-id="92807-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="92807-113">Size</span></span>              | <span data-ttu-id="92807-114">64 bytes</span><span class="sxs-lookup"><span data-stu-id="92807-114">64 bytes</span></span>                                                                                          |
| <span data-ttu-id="92807-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="92807-115">Update Privilege</span></span>  | <span data-ttu-id="92807-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="92807-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="92807-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="92807-117">Update Frequency</span></span>  | <span data-ttu-id="92807-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="92807-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="92807-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92807-119">Attribute-Id</span></span>      | <span data-ttu-id="92807-120">1.2.840.113556.1.4.1437</span><span class="sxs-lookup"><span data-stu-id="92807-120">1.2.840.113556.1.4.1437</span></span>                                                                           |
| <span data-ttu-id="92807-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92807-121">System-Id-Guid</span></span>    | <span data-ttu-id="92807-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span><span class="sxs-lookup"><span data-stu-id="92807-122">9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7</span></span>                                                              |
| <span data-ttu-id="92807-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="92807-123">Syntax</span></span>            | [<span data-ttu-id="92807-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="92807-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                       |



## <a name="implementations"></a><span data-ttu-id="92807-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="92807-125">Implementations</span></span>

-   [<span data-ttu-id="92807-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92807-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92807-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92807-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92807-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92807-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92807-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92807-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92807-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92807-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="92807-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92807-131">Windows Server 2003</span></span>



| <span data-ttu-id="92807-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="92807-132">Entry</span></span> | <span data-ttu-id="92807-133">Valor</span><span class="sxs-lookup"><span data-stu-id="92807-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="92807-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="92807-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92807-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="92807-136">System-Only</span></span>            | <span data-ttu-id="92807-137">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-137">False</span></span>                                                                   |
| <span data-ttu-id="92807-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92807-138">Is-Single-Valued</span></span>       | <span data-ttu-id="92807-139">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-139">False</span></span>                                                                   |
| <span data-ttu-id="92807-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="92807-140">Is Indexed</span></span>             | <span data-ttu-id="92807-141">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-141">False</span></span>                                                                   |
| <span data-ttu-id="92807-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92807-142">In Global Catalog</span></span>      | <span data-ttu-id="92807-143">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-143">False</span></span>                                                                   |
| <span data-ttu-id="92807-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92807-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="92807-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92807-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="92807-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92807-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92807-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-148">Search-Flags</span></span>           | <span data-ttu-id="92807-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92807-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="92807-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-150">System-Flags</span></span>           | <span data-ttu-id="92807-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92807-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="92807-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92807-152">Classes used in</span></span>        | [<span data-ttu-id="92807-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="92807-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92807-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92807-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92807-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="92807-155">Entry</span></span> | <span data-ttu-id="92807-156">Valor</span><span class="sxs-lookup"><span data-stu-id="92807-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="92807-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="92807-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92807-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="92807-159">System-Only</span></span>            | <span data-ttu-id="92807-160">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-160">False</span></span>                                                                   |
| <span data-ttu-id="92807-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92807-161">Is-Single-Valued</span></span>       | <span data-ttu-id="92807-162">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-162">False</span></span>                                                                   |
| <span data-ttu-id="92807-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="92807-163">Is Indexed</span></span>             | <span data-ttu-id="92807-164">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-164">False</span></span>                                                                   |
| <span data-ttu-id="92807-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92807-165">In Global Catalog</span></span>      | <span data-ttu-id="92807-166">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-166">False</span></span>                                                                   |
| <span data-ttu-id="92807-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92807-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="92807-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92807-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="92807-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92807-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92807-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-171">Search-Flags</span></span>           | <span data-ttu-id="92807-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92807-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="92807-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-173">System-Flags</span></span>           | <span data-ttu-id="92807-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92807-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="92807-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92807-175">Classes used in</span></span>        | [<span data-ttu-id="92807-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="92807-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92807-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92807-177">Windows Server 2008</span></span>



| <span data-ttu-id="92807-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="92807-178">Entry</span></span> | <span data-ttu-id="92807-179">Valor</span><span class="sxs-lookup"><span data-stu-id="92807-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="92807-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="92807-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92807-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="92807-182">System-Only</span></span>            | <span data-ttu-id="92807-183">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-183">False</span></span>                                                                   |
| <span data-ttu-id="92807-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92807-184">Is-Single-Valued</span></span>       | <span data-ttu-id="92807-185">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-185">False</span></span>                                                                   |
| <span data-ttu-id="92807-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="92807-186">Is Indexed</span></span>             | <span data-ttu-id="92807-187">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-187">False</span></span>                                                                   |
| <span data-ttu-id="92807-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92807-188">In Global Catalog</span></span>      | <span data-ttu-id="92807-189">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-189">False</span></span>                                                                   |
| <span data-ttu-id="92807-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92807-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="92807-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92807-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="92807-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92807-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92807-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-194">Search-Flags</span></span>           | <span data-ttu-id="92807-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92807-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="92807-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-196">System-Flags</span></span>           | <span data-ttu-id="92807-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92807-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="92807-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92807-198">Classes used in</span></span>        | [<span data-ttu-id="92807-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="92807-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92807-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92807-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92807-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="92807-201">Entry</span></span> | <span data-ttu-id="92807-202">Valor</span><span class="sxs-lookup"><span data-stu-id="92807-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="92807-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="92807-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92807-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="92807-205">System-Only</span></span>            | <span data-ttu-id="92807-206">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-206">False</span></span>                                                                   |
| <span data-ttu-id="92807-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92807-207">Is-Single-Valued</span></span>       | <span data-ttu-id="92807-208">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-208">False</span></span>                                                                   |
| <span data-ttu-id="92807-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="92807-209">Is Indexed</span></span>             | <span data-ttu-id="92807-210">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-210">False</span></span>                                                                   |
| <span data-ttu-id="92807-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92807-211">In Global Catalog</span></span>      | <span data-ttu-id="92807-212">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-212">False</span></span>                                                                   |
| <span data-ttu-id="92807-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92807-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="92807-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92807-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="92807-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92807-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92807-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-217">Search-Flags</span></span>           | <span data-ttu-id="92807-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92807-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="92807-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-219">System-Flags</span></span>           | <span data-ttu-id="92807-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92807-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="92807-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92807-221">Classes used in</span></span>        | [<span data-ttu-id="92807-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="92807-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92807-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92807-223">Windows Server 2012</span></span>



| <span data-ttu-id="92807-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="92807-224">Entry</span></span> | <span data-ttu-id="92807-225">Valor</span><span class="sxs-lookup"><span data-stu-id="92807-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="92807-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="92807-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92807-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="92807-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="92807-228">System-Only</span></span>            | <span data-ttu-id="92807-229">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-229">False</span></span>                                                                   |
| <span data-ttu-id="92807-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92807-230">Is-Single-Valued</span></span>       | <span data-ttu-id="92807-231">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-231">False</span></span>                                                                   |
| <span data-ttu-id="92807-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="92807-232">Is Indexed</span></span>             | <span data-ttu-id="92807-233">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-233">False</span></span>                                                                   |
| <span data-ttu-id="92807-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92807-234">In Global Catalog</span></span>      | <span data-ttu-id="92807-235">Falso</span><span class="sxs-lookup"><span data-stu-id="92807-235">False</span></span>                                                                   |
| <span data-ttu-id="92807-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92807-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="92807-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92807-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="92807-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92807-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92807-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="92807-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-240">Search-Flags</span></span>           | <span data-ttu-id="92807-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92807-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="92807-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92807-242">System-Flags</span></span>           | <span data-ttu-id="92807-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92807-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="92807-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92807-244">Classes used in</span></span>        | [<span data-ttu-id="92807-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="92807-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





