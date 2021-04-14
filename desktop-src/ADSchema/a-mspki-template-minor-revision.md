---
title: MS-PKI-template-atributo de revisão secundária
description: Controla a alteração de atributos na classe. No entanto, isso não disparará o registro automático.
ms.assetid: ff08b621-9a77-48a9-847d-f390ffb41326
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-PKI-template-Minor-Revision
- Esquema de AD do atributo msPKI-template-Minor-Revision
topic_type:
- apiref
api_name:
- ms-PKI-Template-Minor-Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c44e80fa634067ea8b0336cbc63cbf33c09ab2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456269"
---
# <a name="ms-pki-template-minor-revision-attribute"></a><span data-ttu-id="8b4c9-106">MS-PKI-template-atributo de revisão secundária</span><span class="sxs-lookup"><span data-stu-id="8b4c9-106">ms-PKI-Template-Minor-Revision attribute</span></span>

<span data-ttu-id="8b4c9-107">Controla a alteração de atributos na classe.</span><span class="sxs-lookup"><span data-stu-id="8b4c9-107">Keeps track of attributes in the class changing.</span></span> <span data-ttu-id="8b4c9-108">No entanto, isso não disparará o registro automático.</span><span class="sxs-lookup"><span data-stu-id="8b4c9-108">However, this will not trigger auto-enrollment.</span></span>



| <span data-ttu-id="8b4c9-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b4c9-109">Entry</span></span> | <span data-ttu-id="8b4c9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4c9-111">CN</span><span class="sxs-lookup"><span data-stu-id="8b4c9-111">CN</span></span>                | <span data-ttu-id="8b4c9-112">MS-PKI-template – Minor-Revision</span><span class="sxs-lookup"><span data-stu-id="8b4c9-112">ms-PKI-Template-Minor-Revision</span></span>                                                                    |
| <span data-ttu-id="8b4c9-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8b4c9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8b4c9-114">msPKI-modelo-menor revisão</span><span class="sxs-lookup"><span data-stu-id="8b4c9-114">msPKI-Template-Minor-Revision</span></span>                                                                     |
| <span data-ttu-id="8b4c9-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8b4c9-115">Size</span></span>              | <span data-ttu-id="8b4c9-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="8b4c9-116">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="8b4c9-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8b4c9-117">Update Privilege</span></span>  | <span data-ttu-id="8b4c9-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="8b4c9-118">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="8b4c9-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8b4c9-119">Update Frequency</span></span>  | <span data-ttu-id="8b4c9-120">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="8b4c9-120">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="8b4c9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b4c9-121">Attribute-Id</span></span>      | <span data-ttu-id="8b4c9-122">1.2.840.113556.1.4.1435</span><span class="sxs-lookup"><span data-stu-id="8b4c9-122">1.2.840.113556.1.4.1435</span></span>                                                                           |
| <span data-ttu-id="8b4c9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8b4c9-123">System-Id-Guid</span></span>    | <span data-ttu-id="8b4c9-124">13f5236c-1884-46b1-b5d0-484e38990d58</span><span class="sxs-lookup"><span data-stu-id="8b4c9-124">13f5236c-1884-46b1-b5d0-484e38990d58</span></span>                                                              |
| <span data-ttu-id="8b4c9-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b4c9-125">Syntax</span></span>            | [<span data-ttu-id="8b4c9-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-126">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="8b4c9-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="8b4c9-127">Implementations</span></span>

-   [<span data-ttu-id="8b4c9-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b4c9-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b4c9-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b4c9-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b4c9-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8b4c9-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b4c9-133">Windows Server 2003</span></span>



| <span data-ttu-id="8b4c9-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b4c9-134">Entry</span></span> | <span data-ttu-id="8b4c9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-135">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8b4c9-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="8b4c9-136">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b4c9-137">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b4c9-138">System-Only</span></span>            | <span data-ttu-id="8b4c9-139">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-139">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8b4c9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="8b4c9-141">True</span><span class="sxs-lookup"><span data-stu-id="8b4c9-141">True</span></span>                                                                    |
| <span data-ttu-id="8b4c9-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="8b4c9-142">Is Indexed</span></span>             | <span data-ttu-id="8b4c9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-143">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b4c9-144">In Global Catalog</span></span>      | <span data-ttu-id="8b4c9-145">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-145">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b4c9-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8b4c9-147">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8b4c9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b4c9-148">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b4c9-149">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-150">Search-Flags</span></span>           | <span data-ttu-id="8b4c9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b4c9-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="8b4c9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-152">System-Flags</span></span>           | <span data-ttu-id="8b4c9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b4c9-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="8b4c9-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8b4c9-154">Classes used in</span></span>        | [<span data-ttu-id="8b4c9-155">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-155">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b4c9-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b4c9-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b4c9-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b4c9-157">Entry</span></span> | <span data-ttu-id="8b4c9-158">Valor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8b4c9-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="8b4c9-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b4c9-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b4c9-161">System-Only</span></span>            | <span data-ttu-id="8b4c9-162">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-162">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8b4c9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8b4c9-164">True</span><span class="sxs-lookup"><span data-stu-id="8b4c9-164">True</span></span>                                                                    |
| <span data-ttu-id="8b4c9-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="8b4c9-165">Is Indexed</span></span>             | <span data-ttu-id="8b4c9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-166">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b4c9-167">In Global Catalog</span></span>      | <span data-ttu-id="8b4c9-168">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-168">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b4c9-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8b4c9-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8b4c9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b4c9-171">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b4c9-172">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-173">Search-Flags</span></span>           | <span data-ttu-id="8b4c9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b4c9-174">0x00000000</span></span>                                                              |
| <span data-ttu-id="8b4c9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-175">System-Flags</span></span>           | <span data-ttu-id="8b4c9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b4c9-176">0x00000010</span></span>                                                              |
| <span data-ttu-id="8b4c9-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8b4c9-177">Classes used in</span></span>        | [<span data-ttu-id="8b4c9-178">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-178">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b4c9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b4c9-179">Windows Server 2008</span></span>



| <span data-ttu-id="8b4c9-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b4c9-180">Entry</span></span> | <span data-ttu-id="8b4c9-181">Valor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8b4c9-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="8b4c9-182">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b4c9-183">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b4c9-184">System-Only</span></span>            | <span data-ttu-id="8b4c9-185">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-185">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8b4c9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8b4c9-187">True</span><span class="sxs-lookup"><span data-stu-id="8b4c9-187">True</span></span>                                                                    |
| <span data-ttu-id="8b4c9-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="8b4c9-188">Is Indexed</span></span>             | <span data-ttu-id="8b4c9-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-189">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b4c9-190">In Global Catalog</span></span>      | <span data-ttu-id="8b4c9-191">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-191">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b4c9-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8b4c9-193">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8b4c9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b4c9-194">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b4c9-195">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-196">Search-Flags</span></span>           | <span data-ttu-id="8b4c9-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b4c9-197">0x00000000</span></span>                                                              |
| <span data-ttu-id="8b4c9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-198">System-Flags</span></span>           | <span data-ttu-id="8b4c9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b4c9-199">0x00000010</span></span>                                                              |
| <span data-ttu-id="8b4c9-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8b4c9-200">Classes used in</span></span>        | [<span data-ttu-id="8b4c9-201">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-201">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b4c9-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b4c9-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b4c9-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b4c9-203">Entry</span></span> | <span data-ttu-id="8b4c9-204">Valor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8b4c9-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="8b4c9-205">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b4c9-206">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b4c9-207">System-Only</span></span>            | <span data-ttu-id="8b4c9-208">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-208">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8b4c9-209">Is-Single-Valued</span></span>       | <span data-ttu-id="8b4c9-210">True</span><span class="sxs-lookup"><span data-stu-id="8b4c9-210">True</span></span>                                                                    |
| <span data-ttu-id="8b4c9-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="8b4c9-211">Is Indexed</span></span>             | <span data-ttu-id="8b4c9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-212">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b4c9-213">In Global Catalog</span></span>      | <span data-ttu-id="8b4c9-214">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-214">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b4c9-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8b4c9-216">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8b4c9-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b4c9-217">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b4c9-218">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-219">Search-Flags</span></span>           | <span data-ttu-id="8b4c9-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b4c9-220">0x00000000</span></span>                                                              |
| <span data-ttu-id="8b4c9-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-221">System-Flags</span></span>           | <span data-ttu-id="8b4c9-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b4c9-222">0x00000010</span></span>                                                              |
| <span data-ttu-id="8b4c9-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8b4c9-223">Classes used in</span></span>        | [<span data-ttu-id="8b4c9-224">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-224">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b4c9-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b4c9-225">Windows Server 2012</span></span>



| <span data-ttu-id="8b4c9-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="8b4c9-226">Entry</span></span> | <span data-ttu-id="8b4c9-227">Valor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8b4c9-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="8b4c9-228">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b4c9-229">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8b4c9-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b4c9-230">System-Only</span></span>            | <span data-ttu-id="8b4c9-231">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-231">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8b4c9-232">Is-Single-Valued</span></span>       | <span data-ttu-id="8b4c9-233">True</span><span class="sxs-lookup"><span data-stu-id="8b4c9-233">True</span></span>                                                                    |
| <span data-ttu-id="8b4c9-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="8b4c9-234">Is Indexed</span></span>             | <span data-ttu-id="8b4c9-235">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-235">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8b4c9-236">In Global Catalog</span></span>      | <span data-ttu-id="8b4c9-237">Falso</span><span class="sxs-lookup"><span data-stu-id="8b4c9-237">False</span></span>                                                                   |
| <span data-ttu-id="8b4c9-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b4c9-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b4c9-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8b4c9-239">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8b4c9-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b4c9-240">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b4c9-241">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8b4c9-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-242">Search-Flags</span></span>           | <span data-ttu-id="8b4c9-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b4c9-243">0x00000000</span></span>                                                              |
| <span data-ttu-id="8b4c9-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b4c9-244">System-Flags</span></span>           | <span data-ttu-id="8b4c9-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b4c9-245">0x00000010</span></span>                                                              |
| <span data-ttu-id="8b4c9-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8b4c9-246">Classes used in</span></span>        | [<span data-ttu-id="8b4c9-247">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="8b4c9-247">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





