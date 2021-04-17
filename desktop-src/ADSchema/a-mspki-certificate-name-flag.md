---
title: MS-PKI-Certificate-Name-atributo de sinalizador
description: Contém os sinalizadores relacionados à construção do nome da entidade em um certificado emitido.
ms.assetid: 7aeeff69-86b5-4251-bd64-bd99b7c9ef4a
ms.tgt_platform: multiple
keywords:
- MS-PKI-Certificate-Name-Flag atributo AD Schema
- msPKI-Certificate-Name-Flag atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Name-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a9a5f8d6db36c3e3b86945fa529572df38ff6df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104370006"
---
# <a name="ms-pki-certificate-name-flag-attribute"></a><span data-ttu-id="edd12-105">MS-PKI-Certificate-Name-atributo de sinalizador</span><span class="sxs-lookup"><span data-stu-id="edd12-105">ms-PKI-Certificate-Name-Flag attribute</span></span>

<span data-ttu-id="edd12-106">Contém os sinalizadores relacionados à construção do nome da entidade em um certificado emitido.</span><span class="sxs-lookup"><span data-stu-id="edd12-106">Contains the flags related to constructing the subject name in an issued certificate.</span></span>



| <span data-ttu-id="edd12-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="edd12-107">Entry</span></span> | <span data-ttu-id="edd12-108">Valor</span><span class="sxs-lookup"><span data-stu-id="edd12-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd12-109">CN</span><span class="sxs-lookup"><span data-stu-id="edd12-109">CN</span></span>                | <span data-ttu-id="edd12-110">MS-PKI-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="edd12-110">ms-PKI-Certificate-Name-Flag</span></span>                                                                      |
| <span data-ttu-id="edd12-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="edd12-111">Ldap-Display-Name</span></span> | <span data-ttu-id="edd12-112">msPKI-nome-do-certificado-sinalizador</span><span class="sxs-lookup"><span data-stu-id="edd12-112">msPKI-Certificate-Name-Flag</span></span>                                                                       |
| <span data-ttu-id="edd12-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="edd12-113">Size</span></span>              | <span data-ttu-id="edd12-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="edd12-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="edd12-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="edd12-115">Update Privilege</span></span>  | <span data-ttu-id="edd12-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="edd12-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="edd12-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="edd12-117">Update Frequency</span></span>  | <span data-ttu-id="edd12-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="edd12-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="edd12-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="edd12-119">Attribute-Id</span></span>      | <span data-ttu-id="edd12-120">1.2.840.113556.1.4.1432</span><span class="sxs-lookup"><span data-stu-id="edd12-120">1.2.840.113556.1.4.1432</span></span>                                                                           |
| <span data-ttu-id="edd12-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="edd12-121">System-Id-Guid</span></span>    | <span data-ttu-id="edd12-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span><span class="sxs-lookup"><span data-stu-id="edd12-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span></span>                                                              |
| <span data-ttu-id="edd12-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="edd12-123">Syntax</span></span>            | [<span data-ttu-id="edd12-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="edd12-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="edd12-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="edd12-125">Implementations</span></span>

-   [<span data-ttu-id="edd12-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="edd12-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="edd12-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="edd12-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="edd12-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="edd12-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="edd12-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="edd12-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="edd12-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="edd12-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="edd12-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="edd12-131">Windows Server 2003</span></span>



| <span data-ttu-id="edd12-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="edd12-132">Entry</span></span> | <span data-ttu-id="edd12-133">Valor</span><span class="sxs-lookup"><span data-stu-id="edd12-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edd12-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="edd12-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edd12-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="edd12-136">System-Only</span></span>            | <span data-ttu-id="edd12-137">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-137">False</span></span>                                                                   |
| <span data-ttu-id="edd12-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="edd12-138">Is-Single-Valued</span></span>       | <span data-ttu-id="edd12-139">True</span><span class="sxs-lookup"><span data-stu-id="edd12-139">True</span></span>                                                                    |
| <span data-ttu-id="edd12-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="edd12-140">Is Indexed</span></span>             | <span data-ttu-id="edd12-141">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-141">False</span></span>                                                                   |
| <span data-ttu-id="edd12-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="edd12-142">In Global Catalog</span></span>      | <span data-ttu-id="edd12-143">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-143">False</span></span>                                                                   |
| <span data-ttu-id="edd12-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edd12-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="edd12-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="edd12-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edd12-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edd12-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edd12-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-148">Search-Flags</span></span>           | <span data-ttu-id="edd12-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edd12-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="edd12-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-150">System-Flags</span></span>           | <span data-ttu-id="edd12-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edd12-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="edd12-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="edd12-152">Classes used in</span></span>        | [<span data-ttu-id="edd12-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="edd12-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="edd12-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="edd12-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="edd12-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="edd12-155">Entry</span></span> | <span data-ttu-id="edd12-156">Valor</span><span class="sxs-lookup"><span data-stu-id="edd12-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edd12-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="edd12-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edd12-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="edd12-159">System-Only</span></span>            | <span data-ttu-id="edd12-160">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-160">False</span></span>                                                                   |
| <span data-ttu-id="edd12-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="edd12-161">Is-Single-Valued</span></span>       | <span data-ttu-id="edd12-162">True</span><span class="sxs-lookup"><span data-stu-id="edd12-162">True</span></span>                                                                    |
| <span data-ttu-id="edd12-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="edd12-163">Is Indexed</span></span>             | <span data-ttu-id="edd12-164">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-164">False</span></span>                                                                   |
| <span data-ttu-id="edd12-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="edd12-165">In Global Catalog</span></span>      | <span data-ttu-id="edd12-166">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-166">False</span></span>                                                                   |
| <span data-ttu-id="edd12-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edd12-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="edd12-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="edd12-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edd12-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edd12-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edd12-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-171">Search-Flags</span></span>           | <span data-ttu-id="edd12-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edd12-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="edd12-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-173">System-Flags</span></span>           | <span data-ttu-id="edd12-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edd12-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="edd12-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="edd12-175">Classes used in</span></span>        | [<span data-ttu-id="edd12-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="edd12-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="edd12-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edd12-177">Windows Server 2008</span></span>



| <span data-ttu-id="edd12-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="edd12-178">Entry</span></span> | <span data-ttu-id="edd12-179">Valor</span><span class="sxs-lookup"><span data-stu-id="edd12-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edd12-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="edd12-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edd12-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="edd12-182">System-Only</span></span>            | <span data-ttu-id="edd12-183">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-183">False</span></span>                                                                   |
| <span data-ttu-id="edd12-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="edd12-184">Is-Single-Valued</span></span>       | <span data-ttu-id="edd12-185">True</span><span class="sxs-lookup"><span data-stu-id="edd12-185">True</span></span>                                                                    |
| <span data-ttu-id="edd12-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="edd12-186">Is Indexed</span></span>             | <span data-ttu-id="edd12-187">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-187">False</span></span>                                                                   |
| <span data-ttu-id="edd12-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="edd12-188">In Global Catalog</span></span>      | <span data-ttu-id="edd12-189">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-189">False</span></span>                                                                   |
| <span data-ttu-id="edd12-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edd12-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="edd12-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="edd12-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edd12-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edd12-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edd12-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-194">Search-Flags</span></span>           | <span data-ttu-id="edd12-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edd12-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="edd12-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-196">System-Flags</span></span>           | <span data-ttu-id="edd12-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edd12-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="edd12-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="edd12-198">Classes used in</span></span>        | [<span data-ttu-id="edd12-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="edd12-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="edd12-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="edd12-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="edd12-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="edd12-201">Entry</span></span> | <span data-ttu-id="edd12-202">Valor</span><span class="sxs-lookup"><span data-stu-id="edd12-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edd12-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="edd12-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edd12-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="edd12-205">System-Only</span></span>            | <span data-ttu-id="edd12-206">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-206">False</span></span>                                                                   |
| <span data-ttu-id="edd12-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="edd12-207">Is-Single-Valued</span></span>       | <span data-ttu-id="edd12-208">True</span><span class="sxs-lookup"><span data-stu-id="edd12-208">True</span></span>                                                                    |
| <span data-ttu-id="edd12-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="edd12-209">Is Indexed</span></span>             | <span data-ttu-id="edd12-210">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-210">False</span></span>                                                                   |
| <span data-ttu-id="edd12-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="edd12-211">In Global Catalog</span></span>      | <span data-ttu-id="edd12-212">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-212">False</span></span>                                                                   |
| <span data-ttu-id="edd12-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edd12-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="edd12-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="edd12-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edd12-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edd12-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edd12-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-217">Search-Flags</span></span>           | <span data-ttu-id="edd12-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edd12-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="edd12-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-219">System-Flags</span></span>           | <span data-ttu-id="edd12-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edd12-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="edd12-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="edd12-221">Classes used in</span></span>        | [<span data-ttu-id="edd12-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="edd12-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="edd12-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edd12-223">Windows Server 2012</span></span>



| <span data-ttu-id="edd12-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="edd12-224">Entry</span></span> | <span data-ttu-id="edd12-225">Valor</span><span class="sxs-lookup"><span data-stu-id="edd12-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="edd12-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="edd12-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="edd12-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="edd12-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="edd12-228">System-Only</span></span>            | <span data-ttu-id="edd12-229">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-229">False</span></span>                                                                   |
| <span data-ttu-id="edd12-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="edd12-230">Is-Single-Valued</span></span>       | <span data-ttu-id="edd12-231">True</span><span class="sxs-lookup"><span data-stu-id="edd12-231">True</span></span>                                                                    |
| <span data-ttu-id="edd12-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="edd12-232">Is Indexed</span></span>             | <span data-ttu-id="edd12-233">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-233">False</span></span>                                                                   |
| <span data-ttu-id="edd12-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="edd12-234">In Global Catalog</span></span>      | <span data-ttu-id="edd12-235">Falso</span><span class="sxs-lookup"><span data-stu-id="edd12-235">False</span></span>                                                                   |
| <span data-ttu-id="edd12-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="edd12-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="edd12-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="edd12-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="edd12-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="edd12-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="edd12-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="edd12-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-240">Search-Flags</span></span>           | <span data-ttu-id="edd12-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="edd12-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="edd12-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="edd12-242">System-Flags</span></span>           | <span data-ttu-id="edd12-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="edd12-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="edd12-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="edd12-244">Classes used in</span></span>        | [<span data-ttu-id="edd12-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="edd12-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





