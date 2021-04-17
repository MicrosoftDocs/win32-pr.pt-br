---
title: MS-PKI-template-atributo de versão de esquema
description: Controla as atualizações de esquema da classe PKI-Certificate-template.
ms.assetid: 7ad55f1a-cdb9-4eea-bd09-db4f5e6373ba
ms.tgt_platform: multiple
keywords:
- MS-PKI-template-esquema-Version atributo AD Schema
- msPKI-template-esquema-versão do atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-Template-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc3b7952b55b346da29119775bb9c0f8b825c50
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105811221"
---
# <a name="ms-pki-template-schema-version-attribute"></a><span data-ttu-id="79a09-105">MS-PKI-template-atributo de versão de esquema</span><span class="sxs-lookup"><span data-stu-id="79a09-105">ms-PKI-Template-Schema-Version attribute</span></span>

<span data-ttu-id="79a09-106">Controla as atualizações de esquema da classe PKI-Certificate-template.</span><span class="sxs-lookup"><span data-stu-id="79a09-106">Keeps track of schema updates of the PKI-Certificate-Template class.</span></span>



| <span data-ttu-id="79a09-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="79a09-107">Entry</span></span> | <span data-ttu-id="79a09-108">Valor</span><span class="sxs-lookup"><span data-stu-id="79a09-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a09-109">CN</span><span class="sxs-lookup"><span data-stu-id="79a09-109">CN</span></span>                | <span data-ttu-id="79a09-110">MS-PKI-template-versão de esquema</span><span class="sxs-lookup"><span data-stu-id="79a09-110">ms-PKI-Template-Schema-Version</span></span>                                                                    |
| <span data-ttu-id="79a09-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="79a09-111">Ldap-Display-Name</span></span> | <span data-ttu-id="79a09-112">msPKI-modelo-versão de esquema</span><span class="sxs-lookup"><span data-stu-id="79a09-112">msPKI-Template-Schema-Version</span></span>                                                                     |
| <span data-ttu-id="79a09-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="79a09-113">Size</span></span>              | <span data-ttu-id="79a09-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="79a09-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="79a09-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="79a09-115">Update Privilege</span></span>  | <span data-ttu-id="79a09-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="79a09-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="79a09-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="79a09-117">Update Frequency</span></span>  | <span data-ttu-id="79a09-118">Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado.</span><span class="sxs-lookup"><span data-stu-id="79a09-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="79a09-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79a09-119">Attribute-Id</span></span>      | <span data-ttu-id="79a09-120">1.2.840.113556.1.4.1434</span><span class="sxs-lookup"><span data-stu-id="79a09-120">1.2.840.113556.1.4.1434</span></span>                                                                           |
| <span data-ttu-id="79a09-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="79a09-121">System-Id-Guid</span></span>    | <span data-ttu-id="79a09-122">0c15e9f5-491d-4594-918f-32813a091da9</span><span class="sxs-lookup"><span data-stu-id="79a09-122">0c15e9f5-491d-4594-918f-32813a091da9</span></span>                                                              |
| <span data-ttu-id="79a09-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="79a09-123">Syntax</span></span>            | [<span data-ttu-id="79a09-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="79a09-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="79a09-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="79a09-125">Implementations</span></span>

-   [<span data-ttu-id="79a09-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79a09-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79a09-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79a09-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79a09-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79a09-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79a09-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79a09-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79a09-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79a09-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="79a09-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79a09-131">Windows Server 2003</span></span>



| <span data-ttu-id="79a09-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="79a09-132">Entry</span></span> | <span data-ttu-id="79a09-133">Valor</span><span class="sxs-lookup"><span data-stu-id="79a09-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="79a09-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="79a09-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79a09-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="79a09-136">System-Only</span></span>            | <span data-ttu-id="79a09-137">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-137">False</span></span>                                                                   |
| <span data-ttu-id="79a09-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79a09-138">Is-Single-Valued</span></span>       | <span data-ttu-id="79a09-139">True</span><span class="sxs-lookup"><span data-stu-id="79a09-139">True</span></span>                                                                    |
| <span data-ttu-id="79a09-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="79a09-140">Is Indexed</span></span>             | <span data-ttu-id="79a09-141">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-141">False</span></span>                                                                   |
| <span data-ttu-id="79a09-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79a09-142">In Global Catalog</span></span>      | <span data-ttu-id="79a09-143">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-143">False</span></span>                                                                   |
| <span data-ttu-id="79a09-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79a09-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="79a09-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79a09-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="79a09-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79a09-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79a09-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-148">Search-Flags</span></span>           | <span data-ttu-id="79a09-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79a09-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="79a09-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-150">System-Flags</span></span>           | <span data-ttu-id="79a09-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79a09-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="79a09-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79a09-152">Classes used in</span></span>        | [<span data-ttu-id="79a09-153">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="79a09-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79a09-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79a09-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79a09-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="79a09-155">Entry</span></span> | <span data-ttu-id="79a09-156">Valor</span><span class="sxs-lookup"><span data-stu-id="79a09-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="79a09-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="79a09-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79a09-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="79a09-159">System-Only</span></span>            | <span data-ttu-id="79a09-160">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-160">False</span></span>                                                                   |
| <span data-ttu-id="79a09-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79a09-161">Is-Single-Valued</span></span>       | <span data-ttu-id="79a09-162">True</span><span class="sxs-lookup"><span data-stu-id="79a09-162">True</span></span>                                                                    |
| <span data-ttu-id="79a09-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="79a09-163">Is Indexed</span></span>             | <span data-ttu-id="79a09-164">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-164">False</span></span>                                                                   |
| <span data-ttu-id="79a09-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79a09-165">In Global Catalog</span></span>      | <span data-ttu-id="79a09-166">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-166">False</span></span>                                                                   |
| <span data-ttu-id="79a09-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79a09-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="79a09-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79a09-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="79a09-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79a09-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79a09-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-171">Search-Flags</span></span>           | <span data-ttu-id="79a09-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79a09-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="79a09-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-173">System-Flags</span></span>           | <span data-ttu-id="79a09-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79a09-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="79a09-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79a09-175">Classes used in</span></span>        | [<span data-ttu-id="79a09-176">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="79a09-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79a09-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79a09-177">Windows Server 2008</span></span>



| <span data-ttu-id="79a09-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="79a09-178">Entry</span></span> | <span data-ttu-id="79a09-179">Valor</span><span class="sxs-lookup"><span data-stu-id="79a09-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="79a09-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="79a09-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79a09-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="79a09-182">System-Only</span></span>            | <span data-ttu-id="79a09-183">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-183">False</span></span>                                                                   |
| <span data-ttu-id="79a09-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79a09-184">Is-Single-Valued</span></span>       | <span data-ttu-id="79a09-185">True</span><span class="sxs-lookup"><span data-stu-id="79a09-185">True</span></span>                                                                    |
| <span data-ttu-id="79a09-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="79a09-186">Is Indexed</span></span>             | <span data-ttu-id="79a09-187">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-187">False</span></span>                                                                   |
| <span data-ttu-id="79a09-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79a09-188">In Global Catalog</span></span>      | <span data-ttu-id="79a09-189">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-189">False</span></span>                                                                   |
| <span data-ttu-id="79a09-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79a09-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="79a09-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79a09-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="79a09-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79a09-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79a09-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-194">Search-Flags</span></span>           | <span data-ttu-id="79a09-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79a09-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="79a09-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-196">System-Flags</span></span>           | <span data-ttu-id="79a09-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79a09-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="79a09-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79a09-198">Classes used in</span></span>        | [<span data-ttu-id="79a09-199">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="79a09-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79a09-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79a09-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79a09-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="79a09-201">Entry</span></span> | <span data-ttu-id="79a09-202">Valor</span><span class="sxs-lookup"><span data-stu-id="79a09-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="79a09-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="79a09-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79a09-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="79a09-205">System-Only</span></span>            | <span data-ttu-id="79a09-206">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-206">False</span></span>                                                                   |
| <span data-ttu-id="79a09-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79a09-207">Is-Single-Valued</span></span>       | <span data-ttu-id="79a09-208">True</span><span class="sxs-lookup"><span data-stu-id="79a09-208">True</span></span>                                                                    |
| <span data-ttu-id="79a09-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="79a09-209">Is Indexed</span></span>             | <span data-ttu-id="79a09-210">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-210">False</span></span>                                                                   |
| <span data-ttu-id="79a09-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79a09-211">In Global Catalog</span></span>      | <span data-ttu-id="79a09-212">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-212">False</span></span>                                                                   |
| <span data-ttu-id="79a09-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79a09-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="79a09-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79a09-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="79a09-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79a09-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79a09-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-217">Search-Flags</span></span>           | <span data-ttu-id="79a09-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79a09-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="79a09-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-219">System-Flags</span></span>           | <span data-ttu-id="79a09-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79a09-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="79a09-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79a09-221">Classes used in</span></span>        | [<span data-ttu-id="79a09-222">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="79a09-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79a09-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79a09-223">Windows Server 2012</span></span>



| <span data-ttu-id="79a09-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="79a09-224">Entry</span></span> | <span data-ttu-id="79a09-225">Valor</span><span class="sxs-lookup"><span data-stu-id="79a09-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="79a09-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="79a09-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79a09-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="79a09-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="79a09-228">System-Only</span></span>            | <span data-ttu-id="79a09-229">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-229">False</span></span>                                                                   |
| <span data-ttu-id="79a09-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79a09-230">Is-Single-Valued</span></span>       | <span data-ttu-id="79a09-231">True</span><span class="sxs-lookup"><span data-stu-id="79a09-231">True</span></span>                                                                    |
| <span data-ttu-id="79a09-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="79a09-232">Is Indexed</span></span>             | <span data-ttu-id="79a09-233">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-233">False</span></span>                                                                   |
| <span data-ttu-id="79a09-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79a09-234">In Global Catalog</span></span>      | <span data-ttu-id="79a09-235">Falso</span><span class="sxs-lookup"><span data-stu-id="79a09-235">False</span></span>                                                                   |
| <span data-ttu-id="79a09-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79a09-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="79a09-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79a09-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="79a09-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79a09-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79a09-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="79a09-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-240">Search-Flags</span></span>           | <span data-ttu-id="79a09-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79a09-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="79a09-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79a09-242">System-Flags</span></span>           | <span data-ttu-id="79a09-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79a09-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="79a09-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79a09-244">Classes used in</span></span>        | [<span data-ttu-id="79a09-245">**PKI-certificado-modelo**</span><span class="sxs-lookup"><span data-stu-id="79a09-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





