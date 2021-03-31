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
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="63c4d-105">MS-PKI-atributo de tamanho mínimo de chave</span><span class="sxs-lookup"><span data-stu-id="63c4d-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="63c4d-106">Indica o tamanho mínimo da chave privada.</span><span class="sxs-lookup"><span data-stu-id="63c4d-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="63c4d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c4d-107">Entry</span></span> | <span data-ttu-id="63c4d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="63c4d-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c4d-109">CN</span><span class="sxs-lookup"><span data-stu-id="63c4d-109">CN</span></span>                | <span data-ttu-id="63c4d-110">MS-PKI-tamanho mínimo-chave</span><span class="sxs-lookup"><span data-stu-id="63c4d-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="63c4d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="63c4d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="63c4d-112">msPKI-tamanho mínimo da chave</span><span class="sxs-lookup"><span data-stu-id="63c4d-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="63c4d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="63c4d-113">Size</span></span>              | <span data-ttu-id="63c4d-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="63c4d-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="63c4d-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="63c4d-115">Update Privilege</span></span>  | <span data-ttu-id="63c4d-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="63c4d-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="63c4d-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="63c4d-117">Update Frequency</span></span>  | <span data-ttu-id="63c4d-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="63c4d-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="63c4d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63c4d-119">Attribute-Id</span></span>      | <span data-ttu-id="63c4d-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="63c4d-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="63c4d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="63c4d-121">System-Id-Guid</span></span>    | <span data-ttu-id="63c4d-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="63c4d-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="63c4d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="63c4d-123">Syntax</span></span>            | [<span data-ttu-id="63c4d-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="63c4d-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="63c4d-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="63c4d-125">Implementations</span></span>

-   [<span data-ttu-id="63c4d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63c4d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63c4d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63c4d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63c4d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63c4d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63c4d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63c4d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63c4d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63c4d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="63c4d-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63c4d-131">Windows Server 2003</span></span>



| <span data-ttu-id="63c4d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c4d-132">Entry</span></span> | <span data-ttu-id="63c4d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="63c4d-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="63c4d-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="63c4d-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63c4d-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="63c4d-136">System-Only</span></span>            | <span data-ttu-id="63c4d-137">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-137">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63c4d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="63c4d-139">True</span><span class="sxs-lookup"><span data-stu-id="63c4d-139">True</span></span>                                                                    |
| <span data-ttu-id="63c4d-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="63c4d-140">Is Indexed</span></span>             | <span data-ttu-id="63c4d-141">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-141">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63c4d-142">In Global Catalog</span></span>      | <span data-ttu-id="63c4d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-143">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63c4d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="63c4d-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63c4d-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="63c4d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63c4d-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63c4d-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-148">Search-Flags</span></span>           | <span data-ttu-id="63c4d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63c4d-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="63c4d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-150">System-Flags</span></span>           | <span data-ttu-id="63c4d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63c4d-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="63c4d-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63c4d-152">Classes used in</span></span>        | [<span data-ttu-id="63c4d-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="63c4d-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63c4d-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63c4d-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63c4d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c4d-155">Entry</span></span> | <span data-ttu-id="63c4d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="63c4d-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="63c4d-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="63c4d-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63c4d-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="63c4d-159">System-Only</span></span>            | <span data-ttu-id="63c4d-160">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-160">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63c4d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="63c4d-162">True</span><span class="sxs-lookup"><span data-stu-id="63c4d-162">True</span></span>                                                                    |
| <span data-ttu-id="63c4d-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="63c4d-163">Is Indexed</span></span>             | <span data-ttu-id="63c4d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-164">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63c4d-165">In Global Catalog</span></span>      | <span data-ttu-id="63c4d-166">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-166">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63c4d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="63c4d-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63c4d-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="63c4d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63c4d-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63c4d-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-171">Search-Flags</span></span>           | <span data-ttu-id="63c4d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63c4d-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="63c4d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-173">System-Flags</span></span>           | <span data-ttu-id="63c4d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63c4d-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="63c4d-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63c4d-175">Classes used in</span></span>        | [<span data-ttu-id="63c4d-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="63c4d-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63c4d-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63c4d-177">Windows Server 2008</span></span>



| <span data-ttu-id="63c4d-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c4d-178">Entry</span></span> | <span data-ttu-id="63c4d-179">Valor</span><span class="sxs-lookup"><span data-stu-id="63c4d-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="63c4d-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="63c4d-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63c4d-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="63c4d-182">System-Only</span></span>            | <span data-ttu-id="63c4d-183">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-183">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63c4d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="63c4d-185">True</span><span class="sxs-lookup"><span data-stu-id="63c4d-185">True</span></span>                                                                    |
| <span data-ttu-id="63c4d-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="63c4d-186">Is Indexed</span></span>             | <span data-ttu-id="63c4d-187">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-187">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63c4d-188">In Global Catalog</span></span>      | <span data-ttu-id="63c4d-189">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-189">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63c4d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="63c4d-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63c4d-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="63c4d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63c4d-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63c4d-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-194">Search-Flags</span></span>           | <span data-ttu-id="63c4d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63c4d-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="63c4d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-196">System-Flags</span></span>           | <span data-ttu-id="63c4d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63c4d-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="63c4d-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63c4d-198">Classes used in</span></span>        | [<span data-ttu-id="63c4d-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="63c4d-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63c4d-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63c4d-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63c4d-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c4d-201">Entry</span></span> | <span data-ttu-id="63c4d-202">Valor</span><span class="sxs-lookup"><span data-stu-id="63c4d-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="63c4d-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="63c4d-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63c4d-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="63c4d-205">System-Only</span></span>            | <span data-ttu-id="63c4d-206">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-206">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63c4d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="63c4d-208">True</span><span class="sxs-lookup"><span data-stu-id="63c4d-208">True</span></span>                                                                    |
| <span data-ttu-id="63c4d-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="63c4d-209">Is Indexed</span></span>             | <span data-ttu-id="63c4d-210">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-210">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63c4d-211">In Global Catalog</span></span>      | <span data-ttu-id="63c4d-212">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-212">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63c4d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="63c4d-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63c4d-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="63c4d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63c4d-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63c4d-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-217">Search-Flags</span></span>           | <span data-ttu-id="63c4d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63c4d-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="63c4d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-219">System-Flags</span></span>           | <span data-ttu-id="63c4d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63c4d-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="63c4d-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63c4d-221">Classes used in</span></span>        | [<span data-ttu-id="63c4d-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="63c4d-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63c4d-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63c4d-223">Windows Server 2012</span></span>



| <span data-ttu-id="63c4d-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="63c4d-224">Entry</span></span> | <span data-ttu-id="63c4d-225">Valor</span><span class="sxs-lookup"><span data-stu-id="63c4d-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="63c4d-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="63c4d-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63c4d-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="63c4d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="63c4d-228">System-Only</span></span>            | <span data-ttu-id="63c4d-229">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-229">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="63c4d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="63c4d-231">True</span><span class="sxs-lookup"><span data-stu-id="63c4d-231">True</span></span>                                                                    |
| <span data-ttu-id="63c4d-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="63c4d-232">Is Indexed</span></span>             | <span data-ttu-id="63c4d-233">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-233">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="63c4d-234">In Global Catalog</span></span>      | <span data-ttu-id="63c4d-235">Falso</span><span class="sxs-lookup"><span data-stu-id="63c4d-235">False</span></span>                                                                   |
| <span data-ttu-id="63c4d-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="63c4d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="63c4d-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="63c4d-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="63c4d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63c4d-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63c4d-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="63c4d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-240">Search-Flags</span></span>           | <span data-ttu-id="63c4d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63c4d-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="63c4d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63c4d-242">System-Flags</span></span>           | <span data-ttu-id="63c4d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63c4d-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="63c4d-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="63c4d-244">Classes used in</span></span>        | [<span data-ttu-id="63c4d-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="63c4d-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





