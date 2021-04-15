---
title: Country-Code atributo
description: Especifica o código de país/região para o idioma de escolha do usuário. Esse valor não é usado pelo Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Esquema de Country-Code do atributo AD
- Esquema de AD do atributo countryCode
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753611"
---
# <a name="country-code-attribute"></a><span data-ttu-id="01217-106">Country-Code atributo</span><span class="sxs-lookup"><span data-stu-id="01217-106">Country-Code attribute</span></span>

<span data-ttu-id="01217-107">Especifica o código de país/região para o idioma de escolha do usuário.</span><span class="sxs-lookup"><span data-stu-id="01217-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="01217-108">Esse valor não é usado pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="01217-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="01217-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-109">Entry</span></span> | <span data-ttu-id="01217-110">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="01217-111">CN</span><span class="sxs-lookup"><span data-stu-id="01217-111">CN</span></span>                | <span data-ttu-id="01217-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="01217-112">Country-Code</span></span>                            |
| <span data-ttu-id="01217-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="01217-113">Ldap-Display-Name</span></span> | <span data-ttu-id="01217-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="01217-114">countryCode</span></span>                             |
| <span data-ttu-id="01217-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="01217-115">Size</span></span>              | <span data-ttu-id="01217-116">2 bytes</span><span class="sxs-lookup"><span data-stu-id="01217-116">2 bytes</span></span>                                 |
| <span data-ttu-id="01217-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="01217-117">Update Privilege</span></span>  | <span data-ttu-id="01217-118">Proprietário da conta ou administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="01217-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="01217-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="01217-119">Update Frequency</span></span>  | <span data-ttu-id="01217-120">Quando o país/região do usuário é alterado.</span><span class="sxs-lookup"><span data-stu-id="01217-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="01217-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01217-121">Attribute-Id</span></span>      | <span data-ttu-id="01217-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="01217-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="01217-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="01217-123">System-Id-Guid</span></span>    | <span data-ttu-id="01217-124">5fd42471-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="01217-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="01217-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="01217-125">Syntax</span></span>            | [<span data-ttu-id="01217-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="01217-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="01217-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="01217-127">Implementations</span></span>

-   [<span data-ttu-id="01217-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="01217-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="01217-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01217-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01217-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="01217-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="01217-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01217-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01217-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01217-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01217-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01217-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01217-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01217-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="01217-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01217-135">Windows 2000 Server</span></span>



| <span data-ttu-id="01217-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-136">Entry</span></span> | <span data-ttu-id="01217-137">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01217-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-140">System-Only</span></span>            | <span data-ttu-id="01217-141">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-142">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-143">True</span><span class="sxs-lookup"><span data-stu-id="01217-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="01217-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-144">Is Indexed</span></span>             | <span data-ttu-id="01217-145">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-146">In Global Catalog</span></span>      | <span data-ttu-id="01217-147">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="01217-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="01217-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="01217-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-152">Search-Flags</span></span>           | <span data-ttu-id="01217-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-154">System-Flags</span></span>           | <span data-ttu-id="01217-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-156">Classes used in</span></span>        | [<span data-ttu-id="01217-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="01217-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="01217-158">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="01217-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01217-159">Windows Server 2003</span></span>



| <span data-ttu-id="01217-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-160">Entry</span></span> | <span data-ttu-id="01217-161">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01217-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-164">System-Only</span></span>            | <span data-ttu-id="01217-165">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-166">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-167">True</span><span class="sxs-lookup"><span data-stu-id="01217-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="01217-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-168">Is Indexed</span></span>             | <span data-ttu-id="01217-169">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-170">In Global Catalog</span></span>      | <span data-ttu-id="01217-171">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="01217-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-174">Range-Lower</span></span>            | <span data-ttu-id="01217-175">0</span><span class="sxs-lookup"><span data-stu-id="01217-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="01217-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-176">Range-Upper</span></span>            | <span data-ttu-id="01217-177">65535</span><span class="sxs-lookup"><span data-stu-id="01217-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="01217-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-178">Search-Flags</span></span>           | <span data-ttu-id="01217-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-180">System-Flags</span></span>           | <span data-ttu-id="01217-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-182">Classes used in</span></span>        | [<span data-ttu-id="01217-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="01217-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="01217-184">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="01217-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="01217-185">ADAM</span></span>



| <span data-ttu-id="01217-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-186">Entry</span></span> | <span data-ttu-id="01217-187">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01217-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01217-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="01217-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-190">System-Only</span></span>            | <span data-ttu-id="01217-191">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-191">False</span></span>                                                          |
| <span data-ttu-id="01217-192">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-192">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-193">True</span><span class="sxs-lookup"><span data-stu-id="01217-193">True</span></span>                                                           |
| <span data-ttu-id="01217-194">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-194">Is Indexed</span></span>             | <span data-ttu-id="01217-195">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-195">False</span></span>                                                          |
| <span data-ttu-id="01217-196">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-196">In Global Catalog</span></span>      | <span data-ttu-id="01217-197">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-197">False</span></span>                                                          |
| <span data-ttu-id="01217-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-199">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="01217-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-200">Range-Lower</span></span>            | <span data-ttu-id="01217-201">0</span><span class="sxs-lookup"><span data-stu-id="01217-201">0</span></span>                                                              |
| <span data-ttu-id="01217-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-202">Range-Upper</span></span>            | <span data-ttu-id="01217-203">65535</span><span class="sxs-lookup"><span data-stu-id="01217-203">65535</span></span>                                                          |
| <span data-ttu-id="01217-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-204">Search-Flags</span></span>           | <span data-ttu-id="01217-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="01217-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-206">System-Flags</span></span>           | <span data-ttu-id="01217-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="01217-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-208">Classes used in</span></span>        | [<span data-ttu-id="01217-209">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01217-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01217-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01217-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-211">Entry</span></span> | <span data-ttu-id="01217-212">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01217-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-215">System-Only</span></span>            | <span data-ttu-id="01217-216">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-217">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-218">True</span><span class="sxs-lookup"><span data-stu-id="01217-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="01217-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-219">Is Indexed</span></span>             | <span data-ttu-id="01217-220">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-221">In Global Catalog</span></span>      | <span data-ttu-id="01217-222">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="01217-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-225">Range-Lower</span></span>            | <span data-ttu-id="01217-226">0</span><span class="sxs-lookup"><span data-stu-id="01217-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="01217-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-227">Range-Upper</span></span>            | <span data-ttu-id="01217-228">65535</span><span class="sxs-lookup"><span data-stu-id="01217-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="01217-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-229">Search-Flags</span></span>           | <span data-ttu-id="01217-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-231">System-Flags</span></span>           | <span data-ttu-id="01217-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-233">Classes used in</span></span>        | [<span data-ttu-id="01217-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="01217-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="01217-235">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01217-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01217-236">Windows Server 2008</span></span>



| <span data-ttu-id="01217-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-237">Entry</span></span> | <span data-ttu-id="01217-238">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01217-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-241">System-Only</span></span>            | <span data-ttu-id="01217-242">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-243">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-244">True</span><span class="sxs-lookup"><span data-stu-id="01217-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="01217-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-245">Is Indexed</span></span>             | <span data-ttu-id="01217-246">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-247">In Global Catalog</span></span>      | <span data-ttu-id="01217-248">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="01217-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-251">Range-Lower</span></span>            | <span data-ttu-id="01217-252">0</span><span class="sxs-lookup"><span data-stu-id="01217-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="01217-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-253">Range-Upper</span></span>            | <span data-ttu-id="01217-254">65535</span><span class="sxs-lookup"><span data-stu-id="01217-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="01217-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-255">Search-Flags</span></span>           | <span data-ttu-id="01217-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-257">System-Flags</span></span>           | <span data-ttu-id="01217-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-259">Classes used in</span></span>        | [<span data-ttu-id="01217-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="01217-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="01217-261">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01217-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01217-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01217-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-263">Entry</span></span> | <span data-ttu-id="01217-264">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01217-265">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-267">System-Only</span></span>            | <span data-ttu-id="01217-268">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-269">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-269">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-270">True</span><span class="sxs-lookup"><span data-stu-id="01217-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="01217-271">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-271">Is Indexed</span></span>             | <span data-ttu-id="01217-272">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-273">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-273">In Global Catalog</span></span>      | <span data-ttu-id="01217-274">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-276">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="01217-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-277">Range-Lower</span></span>            | <span data-ttu-id="01217-278">0</span><span class="sxs-lookup"><span data-stu-id="01217-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="01217-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-279">Range-Upper</span></span>            | <span data-ttu-id="01217-280">65535</span><span class="sxs-lookup"><span data-stu-id="01217-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="01217-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-281">Search-Flags</span></span>           | <span data-ttu-id="01217-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-283">System-Flags</span></span>           | <span data-ttu-id="01217-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-285">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-285">Classes used in</span></span>        | [<span data-ttu-id="01217-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="01217-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="01217-287">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01217-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01217-288">Windows Server 2012</span></span>



| <span data-ttu-id="01217-289">Entrada</span><span class="sxs-lookup"><span data-stu-id="01217-289">Entry</span></span> | <span data-ttu-id="01217-290">Valor</span><span class="sxs-lookup"><span data-stu-id="01217-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01217-291">ID do link</span><span class="sxs-lookup"><span data-stu-id="01217-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01217-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="01217-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="01217-293">System-Only</span></span>            | <span data-ttu-id="01217-294">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-295">É de valor único</span><span class="sxs-lookup"><span data-stu-id="01217-295">Is-Single-Valued</span></span>       | <span data-ttu-id="01217-296">True</span><span class="sxs-lookup"><span data-stu-id="01217-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="01217-297">É indexado</span><span class="sxs-lookup"><span data-stu-id="01217-297">Is Indexed</span></span>             | <span data-ttu-id="01217-298">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-299">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="01217-299">In Global Catalog</span></span>      | <span data-ttu-id="01217-300">Falso</span><span class="sxs-lookup"><span data-stu-id="01217-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="01217-301">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="01217-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="01217-302">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="01217-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="01217-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01217-303">Range-Lower</span></span>            | <span data-ttu-id="01217-304">0</span><span class="sxs-lookup"><span data-stu-id="01217-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="01217-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01217-305">Range-Upper</span></span>            | <span data-ttu-id="01217-306">65535</span><span class="sxs-lookup"><span data-stu-id="01217-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="01217-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-307">Search-Flags</span></span>           | <span data-ttu-id="01217-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01217-309">System-Flags</span></span>           | <span data-ttu-id="01217-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01217-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="01217-311">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="01217-311">Classes used in</span></span>        | [<span data-ttu-id="01217-312">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="01217-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="01217-313">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="01217-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





