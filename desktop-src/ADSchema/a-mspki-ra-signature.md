---
title: atributo ms-PKI-RA-Signature
description: Especifica o número de assinaturas de autoridade de registro de registro que são necessárias em uma solicitação de registro.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-PKI-RA-Signature
- msPKI-RA-atributo de assinatura esquema do AD
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 170793e46095e16a62d8e025ec16b67bf2be7131
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756478"
---
# <a name="ms-pki-ra-signature-attribute"></a><span data-ttu-id="62ed1-105">atributo ms-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="62ed1-105">ms-PKI-RA-Signature attribute</span></span>

<span data-ttu-id="62ed1-106">Especifica o número de assinaturas de autoridade de registro de registro que são necessárias em uma solicitação de registro.</span><span class="sxs-lookup"><span data-stu-id="62ed1-106">Specifies the number of enrollment registration authority signatures that are required in an enrollment request.</span></span>



| <span data-ttu-id="62ed1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="62ed1-107">Entry</span></span> | <span data-ttu-id="62ed1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="62ed1-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-109">CN</span><span class="sxs-lookup"><span data-stu-id="62ed1-109">CN</span></span>                | <span data-ttu-id="62ed1-110">MS-PKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="62ed1-110">ms-PKI-RA-Signature</span></span>                                                                               |
| <span data-ttu-id="62ed1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="62ed1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="62ed1-112">msPKI-RA-Signature</span><span class="sxs-lookup"><span data-stu-id="62ed1-112">msPKI-RA-Signature</span></span>                                                                                |
| <span data-ttu-id="62ed1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="62ed1-113">Size</span></span>              | <span data-ttu-id="62ed1-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="62ed1-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="62ed1-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="62ed1-115">Update Privilege</span></span>  | <span data-ttu-id="62ed1-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="62ed1-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="62ed1-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="62ed1-117">Update Frequency</span></span>  | <span data-ttu-id="62ed1-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="62ed1-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="62ed1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="62ed1-119">Attribute-Id</span></span>      | <span data-ttu-id="62ed1-120">1.2.840.113556.1.4.1429</span><span class="sxs-lookup"><span data-stu-id="62ed1-120">1.2.840.113556.1.4.1429</span></span>                                                                           |
| <span data-ttu-id="62ed1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="62ed1-121">System-Id-Guid</span></span>    | <span data-ttu-id="62ed1-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span><span class="sxs-lookup"><span data-stu-id="62ed1-122">fe17e04b-937d-4f7e-8e0e-9292c8d5683e</span></span>                                                              |
| <span data-ttu-id="62ed1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ed1-123">Syntax</span></span>            | [<span data-ttu-id="62ed1-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="62ed1-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="62ed1-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="62ed1-125">Implementations</span></span>

-   [<span data-ttu-id="62ed1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="62ed1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="62ed1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="62ed1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="62ed1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="62ed1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="62ed1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="62ed1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="62ed1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="62ed1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="62ed1-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62ed1-131">Windows Server 2003</span></span>



| <span data-ttu-id="62ed1-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="62ed1-132">Entry</span></span> | <span data-ttu-id="62ed1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="62ed1-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="62ed1-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62ed1-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="62ed1-136">System-Only</span></span>            | <span data-ttu-id="62ed1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-137">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="62ed1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="62ed1-139">True</span><span class="sxs-lookup"><span data-stu-id="62ed1-139">True</span></span>                                                                    |
| <span data-ttu-id="62ed1-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="62ed1-140">Is Indexed</span></span>             | <span data-ttu-id="62ed1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-141">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="62ed1-142">In Global Catalog</span></span>      | <span data-ttu-id="62ed1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-143">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="62ed1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="62ed1-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="62ed1-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62ed1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62ed1-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62ed1-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-148">Search-Flags</span></span>           | <span data-ttu-id="62ed1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62ed1-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="62ed1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-150">System-Flags</span></span>           | <span data-ttu-id="62ed1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62ed1-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="62ed1-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="62ed1-152">Classes used in</span></span>        | [<span data-ttu-id="62ed1-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="62ed1-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="62ed1-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="62ed1-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="62ed1-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="62ed1-155">Entry</span></span> | <span data-ttu-id="62ed1-156">Valor</span><span class="sxs-lookup"><span data-stu-id="62ed1-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="62ed1-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62ed1-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="62ed1-159">System-Only</span></span>            | <span data-ttu-id="62ed1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-160">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="62ed1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="62ed1-162">True</span><span class="sxs-lookup"><span data-stu-id="62ed1-162">True</span></span>                                                                    |
| <span data-ttu-id="62ed1-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="62ed1-163">Is Indexed</span></span>             | <span data-ttu-id="62ed1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-164">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="62ed1-165">In Global Catalog</span></span>      | <span data-ttu-id="62ed1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-166">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="62ed1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="62ed1-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="62ed1-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62ed1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62ed1-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62ed1-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-171">Search-Flags</span></span>           | <span data-ttu-id="62ed1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62ed1-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="62ed1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-173">System-Flags</span></span>           | <span data-ttu-id="62ed1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62ed1-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="62ed1-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="62ed1-175">Classes used in</span></span>        | [<span data-ttu-id="62ed1-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="62ed1-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="62ed1-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62ed1-177">Windows Server 2008</span></span>



| <span data-ttu-id="62ed1-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="62ed1-178">Entry</span></span> | <span data-ttu-id="62ed1-179">Valor</span><span class="sxs-lookup"><span data-stu-id="62ed1-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="62ed1-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62ed1-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="62ed1-182">System-Only</span></span>            | <span data-ttu-id="62ed1-183">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-183">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="62ed1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="62ed1-185">True</span><span class="sxs-lookup"><span data-stu-id="62ed1-185">True</span></span>                                                                    |
| <span data-ttu-id="62ed1-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="62ed1-186">Is Indexed</span></span>             | <span data-ttu-id="62ed1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-187">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="62ed1-188">In Global Catalog</span></span>      | <span data-ttu-id="62ed1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-189">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="62ed1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="62ed1-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="62ed1-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62ed1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62ed1-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62ed1-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-194">Search-Flags</span></span>           | <span data-ttu-id="62ed1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62ed1-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="62ed1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-196">System-Flags</span></span>           | <span data-ttu-id="62ed1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62ed1-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="62ed1-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="62ed1-198">Classes used in</span></span>        | [<span data-ttu-id="62ed1-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="62ed1-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="62ed1-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62ed1-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="62ed1-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="62ed1-201">Entry</span></span> | <span data-ttu-id="62ed1-202">Valor</span><span class="sxs-lookup"><span data-stu-id="62ed1-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="62ed1-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62ed1-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="62ed1-205">System-Only</span></span>            | <span data-ttu-id="62ed1-206">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-206">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="62ed1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="62ed1-208">True</span><span class="sxs-lookup"><span data-stu-id="62ed1-208">True</span></span>                                                                    |
| <span data-ttu-id="62ed1-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="62ed1-209">Is Indexed</span></span>             | <span data-ttu-id="62ed1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-210">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="62ed1-211">In Global Catalog</span></span>      | <span data-ttu-id="62ed1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-212">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="62ed1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="62ed1-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="62ed1-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62ed1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62ed1-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62ed1-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-217">Search-Flags</span></span>           | <span data-ttu-id="62ed1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62ed1-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="62ed1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-219">System-Flags</span></span>           | <span data-ttu-id="62ed1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62ed1-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="62ed1-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="62ed1-221">Classes used in</span></span>        | [<span data-ttu-id="62ed1-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="62ed1-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="62ed1-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62ed1-223">Windows Server 2012</span></span>



| <span data-ttu-id="62ed1-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="62ed1-224">Entry</span></span> | <span data-ttu-id="62ed1-225">Valor</span><span class="sxs-lookup"><span data-stu-id="62ed1-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="62ed1-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="62ed1-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62ed1-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="62ed1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="62ed1-228">System-Only</span></span>            | <span data-ttu-id="62ed1-229">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-229">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="62ed1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="62ed1-231">True</span><span class="sxs-lookup"><span data-stu-id="62ed1-231">True</span></span>                                                                    |
| <span data-ttu-id="62ed1-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="62ed1-232">Is Indexed</span></span>             | <span data-ttu-id="62ed1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-233">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="62ed1-234">In Global Catalog</span></span>      | <span data-ttu-id="62ed1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="62ed1-235">False</span></span>                                                                   |
| <span data-ttu-id="62ed1-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="62ed1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="62ed1-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="62ed1-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="62ed1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62ed1-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62ed1-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="62ed1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-240">Search-Flags</span></span>           | <span data-ttu-id="62ed1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62ed1-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="62ed1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62ed1-242">System-Flags</span></span>           | <span data-ttu-id="62ed1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62ed1-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="62ed1-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="62ed1-244">Classes used in</span></span>        | [<span data-ttu-id="62ed1-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="62ed1-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





