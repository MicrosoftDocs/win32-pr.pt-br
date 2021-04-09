---
title: MS-PKI-atributo de tamanho mínimo de chave
description: Indica o tamanho mínimo da chave privada.
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- MS-PKI-esquema do atributo de tamanho mínimo-de-chave
- msPKI-esquema de AD de atributos de tamanho mínimo-chave
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086903"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="7c03c-105">MS-PKI-atributo de tamanho mínimo de chave</span><span class="sxs-lookup"><span data-stu-id="7c03c-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="7c03c-106">Indica o tamanho mínimo da chave privada.</span><span class="sxs-lookup"><span data-stu-id="7c03c-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="7c03c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c03c-107">Entry</span></span> | <span data-ttu-id="7c03c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03c-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c03c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c03c-109">CN</span></span>                | <span data-ttu-id="7c03c-110">MS-PKI-tamanho mínimo-chave</span><span class="sxs-lookup"><span data-stu-id="7c03c-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="7c03c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7c03c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7c03c-112">msPKI-tamanho mínimo da chave</span><span class="sxs-lookup"><span data-stu-id="7c03c-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="7c03c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7c03c-113">Size</span></span>              | <span data-ttu-id="7c03c-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="7c03c-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="7c03c-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7c03c-115">Update Privilege</span></span>  | <span data-ttu-id="7c03c-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="7c03c-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="7c03c-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7c03c-117">Update Frequency</span></span>  | <span data-ttu-id="7c03c-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="7c03c-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="7c03c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c03c-119">Attribute-Id</span></span>      | <span data-ttu-id="7c03c-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="7c03c-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="7c03c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7c03c-121">System-Id-Guid</span></span>    | <span data-ttu-id="7c03c-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="7c03c-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="7c03c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c03c-123">Syntax</span></span>            | [<span data-ttu-id="7c03c-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="7c03c-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="7c03c-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="7c03c-125">Implementations</span></span>

-   [<span data-ttu-id="7c03c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c03c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c03c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c03c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c03c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c03c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c03c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c03c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c03c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c03c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7c03c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c03c-131">Windows Server 2003</span></span>



| <span data-ttu-id="7c03c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c03c-132">Entry</span></span> | <span data-ttu-id="7c03c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03c-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c03c-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c03c-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c03c-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c03c-136">System-Only</span></span>            | <span data-ttu-id="7c03c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-137">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c03c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7c03c-139">True</span><span class="sxs-lookup"><span data-stu-id="7c03c-139">True</span></span>                                                                    |
| <span data-ttu-id="7c03c-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c03c-140">Is Indexed</span></span>             | <span data-ttu-id="7c03c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-141">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c03c-142">In Global Catalog</span></span>      | <span data-ttu-id="7c03c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-143">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c03c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c03c-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c03c-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c03c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c03c-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c03c-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-148">Search-Flags</span></span>           | <span data-ttu-id="7c03c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c03c-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c03c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-150">System-Flags</span></span>           | <span data-ttu-id="7c03c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c03c-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c03c-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c03c-152">Classes used in</span></span>        | [<span data-ttu-id="7c03c-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7c03c-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c03c-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c03c-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c03c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c03c-155">Entry</span></span> | <span data-ttu-id="7c03c-156">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03c-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c03c-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c03c-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c03c-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c03c-159">System-Only</span></span>            | <span data-ttu-id="7c03c-160">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-160">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c03c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7c03c-162">True</span><span class="sxs-lookup"><span data-stu-id="7c03c-162">True</span></span>                                                                    |
| <span data-ttu-id="7c03c-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c03c-163">Is Indexed</span></span>             | <span data-ttu-id="7c03c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-164">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c03c-165">In Global Catalog</span></span>      | <span data-ttu-id="7c03c-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-166">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c03c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c03c-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c03c-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c03c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c03c-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c03c-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-171">Search-Flags</span></span>           | <span data-ttu-id="7c03c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c03c-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c03c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-173">System-Flags</span></span>           | <span data-ttu-id="7c03c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c03c-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c03c-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c03c-175">Classes used in</span></span>        | [<span data-ttu-id="7c03c-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7c03c-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c03c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c03c-177">Windows Server 2008</span></span>



| <span data-ttu-id="7c03c-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c03c-178">Entry</span></span> | <span data-ttu-id="7c03c-179">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03c-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c03c-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c03c-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c03c-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c03c-182">System-Only</span></span>            | <span data-ttu-id="7c03c-183">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-183">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c03c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7c03c-185">True</span><span class="sxs-lookup"><span data-stu-id="7c03c-185">True</span></span>                                                                    |
| <span data-ttu-id="7c03c-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c03c-186">Is Indexed</span></span>             | <span data-ttu-id="7c03c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-187">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c03c-188">In Global Catalog</span></span>      | <span data-ttu-id="7c03c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-189">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c03c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c03c-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c03c-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c03c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c03c-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c03c-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-194">Search-Flags</span></span>           | <span data-ttu-id="7c03c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c03c-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c03c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-196">System-Flags</span></span>           | <span data-ttu-id="7c03c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c03c-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c03c-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c03c-198">Classes used in</span></span>        | [<span data-ttu-id="7c03c-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7c03c-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c03c-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c03c-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c03c-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c03c-201">Entry</span></span> | <span data-ttu-id="7c03c-202">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03c-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c03c-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c03c-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c03c-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c03c-205">System-Only</span></span>            | <span data-ttu-id="7c03c-206">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-206">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c03c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7c03c-208">True</span><span class="sxs-lookup"><span data-stu-id="7c03c-208">True</span></span>                                                                    |
| <span data-ttu-id="7c03c-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c03c-209">Is Indexed</span></span>             | <span data-ttu-id="7c03c-210">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-210">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c03c-211">In Global Catalog</span></span>      | <span data-ttu-id="7c03c-212">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-212">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c03c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c03c-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c03c-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c03c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c03c-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c03c-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-217">Search-Flags</span></span>           | <span data-ttu-id="7c03c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c03c-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c03c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-219">System-Flags</span></span>           | <span data-ttu-id="7c03c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c03c-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c03c-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c03c-221">Classes used in</span></span>        | [<span data-ttu-id="7c03c-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7c03c-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c03c-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c03c-223">Windows Server 2012</span></span>



| <span data-ttu-id="7c03c-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c03c-224">Entry</span></span> | <span data-ttu-id="7c03c-225">Valor</span><span class="sxs-lookup"><span data-stu-id="7c03c-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c03c-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c03c-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c03c-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="7c03c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c03c-228">System-Only</span></span>            | <span data-ttu-id="7c03c-229">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-229">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c03c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7c03c-231">True</span><span class="sxs-lookup"><span data-stu-id="7c03c-231">True</span></span>                                                                    |
| <span data-ttu-id="7c03c-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c03c-232">Is Indexed</span></span>             | <span data-ttu-id="7c03c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-233">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c03c-234">In Global Catalog</span></span>      | <span data-ttu-id="7c03c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="7c03c-235">False</span></span>                                                                   |
| <span data-ttu-id="7c03c-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c03c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c03c-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c03c-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="7c03c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c03c-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c03c-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="7c03c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-240">Search-Flags</span></span>           | <span data-ttu-id="7c03c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c03c-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="7c03c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c03c-242">System-Flags</span></span>           | <span data-ttu-id="7c03c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c03c-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="7c03c-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c03c-244">Classes used in</span></span>        | [<span data-ttu-id="7c03c-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="7c03c-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





