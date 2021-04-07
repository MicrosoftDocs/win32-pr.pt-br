---
title: UPN-Suffixes atributo
description: A lista de sufixos de nome de entidade de usuário para um domínio.
ms.assetid: ad861d2d-b643-468c-a346-36ad6a828359
ms.tgt_platform: multiple
keywords:
- Esquema de UPN-Suffixes do atributo AD
- Esquema de AD do atributo uPNSuffixes
topic_type:
- apiref
api_name:
- UPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4aa5fb9398478e4b91fb8f36b8cf96a244935fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825257"
---
# <a name="upn-suffixes-attribute"></a><span data-ttu-id="332c1-105">UPN-Suffixes atributo</span><span class="sxs-lookup"><span data-stu-id="332c1-105">UPN-Suffixes attribute</span></span>

<span data-ttu-id="332c1-106">A lista de sufixos de nome de entidade de usuário para um domínio.</span><span class="sxs-lookup"><span data-stu-id="332c1-106">The list of User-Principal-Name suffixes for a domain.</span></span>



| <span data-ttu-id="332c1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-107">Entry</span></span> | <span data-ttu-id="332c1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="332c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="332c1-109">CN</span></span>                | <span data-ttu-id="332c1-110">UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="332c1-110">UPN-Suffixes</span></span>                                |
| <span data-ttu-id="332c1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="332c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="332c1-112">uPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="332c1-112">uPNSuffixes</span></span>                                 |
| <span data-ttu-id="332c1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="332c1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="332c1-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="332c1-114">Update Privilege</span></span>  | <span data-ttu-id="332c1-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="332c1-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="332c1-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="332c1-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="332c1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-117">Attribute-Id</span></span>      | <span data-ttu-id="332c1-118">1.2.840.113556.1.4.890</span><span class="sxs-lookup"><span data-stu-id="332c1-118">1.2.840.113556.1.4.890</span></span>                      |
| <span data-ttu-id="332c1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="332c1-119">System-Id-Guid</span></span>    | <span data-ttu-id="332c1-120">032160bf-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="332c1-120">032160bf-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="332c1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="332c1-121">Syntax</span></span>            | [<span data-ttu-id="332c1-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="332c1-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="332c1-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="332c1-123">Implementations</span></span>

-   [<span data-ttu-id="332c1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="332c1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="332c1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="332c1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="332c1-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="332c1-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="332c1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="332c1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="332c1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="332c1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="332c1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="332c1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="332c1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="332c1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="332c1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="332c1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="332c1-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-132">Entry</span></span> | <span data-ttu-id="332c1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-133">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-134">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-135">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-136">System-Only</span></span>            | <span data-ttu-id="332c1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-137">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-139">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-140">Is Indexed</span></span>             | <span data-ttu-id="332c1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-141">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-142">In Global Catalog</span></span>      | <span data-ttu-id="332c1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-143">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-145">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-146">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-147">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-148">Search-Flags</span></span>           | <span data-ttu-id="332c1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-149">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-150">System-Flags</span></span>           | <span data-ttu-id="332c1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-151">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-152">Classes used in</span></span>        | [<span data-ttu-id="332c1-153">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-153">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-154">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-154">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="332c1-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="332c1-155">Windows Server 2003</span></span>



| <span data-ttu-id="332c1-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-156">Entry</span></span> | <span data-ttu-id="332c1-157">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-158">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-159">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-160">System-Only</span></span>            | <span data-ttu-id="332c1-161">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-161">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-163">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-163">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-164">Is Indexed</span></span>             | <span data-ttu-id="332c1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-165">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-166">In Global Catalog</span></span>      | <span data-ttu-id="332c1-167">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-167">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-169">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-170">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-171">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-172">Search-Flags</span></span>           | <span data-ttu-id="332c1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-173">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-174">System-Flags</span></span>           | <span data-ttu-id="332c1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-175">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-176">Classes used in</span></span>        | [<span data-ttu-id="332c1-177">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-178">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-178">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="332c1-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="332c1-179">ADAM</span></span>



| <span data-ttu-id="332c1-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-180">Entry</span></span> | <span data-ttu-id="332c1-181">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-181">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-182">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-183">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-184">System-Only</span></span>            | <span data-ttu-id="332c1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-185">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-187">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-188">Is Indexed</span></span>             | <span data-ttu-id="332c1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-189">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-190">In Global Catalog</span></span>      | <span data-ttu-id="332c1-191">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-191">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-193">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-194">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-195">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-196">Search-Flags</span></span>           | <span data-ttu-id="332c1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-197">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-198">System-Flags</span></span>           | <span data-ttu-id="332c1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-199">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-200">Classes used in</span></span>        | [<span data-ttu-id="332c1-201">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-202">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-202">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="332c1-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="332c1-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="332c1-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-204">Entry</span></span> | <span data-ttu-id="332c1-205">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-205">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-206">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-207">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-208">System-Only</span></span>            | <span data-ttu-id="332c1-209">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-209">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-211">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-212">Is Indexed</span></span>             | <span data-ttu-id="332c1-213">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-213">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-214">In Global Catalog</span></span>      | <span data-ttu-id="332c1-215">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-215">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-217">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-218">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-219">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-220">Search-Flags</span></span>           | <span data-ttu-id="332c1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-221">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-222">System-Flags</span></span>           | <span data-ttu-id="332c1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-223">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-224">Classes used in</span></span>        | [<span data-ttu-id="332c1-225">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-225">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-226">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-226">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="332c1-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="332c1-227">Windows Server 2008</span></span>



| <span data-ttu-id="332c1-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-228">Entry</span></span> | <span data-ttu-id="332c1-229">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-229">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-230">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-231">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-232">System-Only</span></span>            | <span data-ttu-id="332c1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-233">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-234">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-235">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-236">Is Indexed</span></span>             | <span data-ttu-id="332c1-237">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-237">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-238">In Global Catalog</span></span>      | <span data-ttu-id="332c1-239">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-239">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-241">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-242">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-243">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-244">Search-Flags</span></span>           | <span data-ttu-id="332c1-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-245">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-246">System-Flags</span></span>           | <span data-ttu-id="332c1-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-247">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-248">Classes used in</span></span>        | [<span data-ttu-id="332c1-249">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-249">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-250">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-250">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="332c1-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="332c1-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="332c1-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-252">Entry</span></span> | <span data-ttu-id="332c1-253">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-253">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-254">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-255">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-256">System-Only</span></span>            | <span data-ttu-id="332c1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-257">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-258">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-259">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-259">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-260">Is Indexed</span></span>             | <span data-ttu-id="332c1-261">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-261">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-262">In Global Catalog</span></span>      | <span data-ttu-id="332c1-263">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-263">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-265">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-266">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-267">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-268">Search-Flags</span></span>           | <span data-ttu-id="332c1-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-269">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-270">System-Flags</span></span>           | <span data-ttu-id="332c1-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-271">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-272">Classes used in</span></span>        | [<span data-ttu-id="332c1-273">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-273">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-274">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-274">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="332c1-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="332c1-275">Windows Server 2012</span></span>



| <span data-ttu-id="332c1-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="332c1-276">Entry</span></span> | <span data-ttu-id="332c1-277">Valor</span><span class="sxs-lookup"><span data-stu-id="332c1-277">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c1-278">ID do link</span><span class="sxs-lookup"><span data-stu-id="332c1-278">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="332c1-279">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="332c1-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="332c1-280">System-Only</span></span>            | <span data-ttu-id="332c1-281">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-281">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-282">É de valor único</span><span class="sxs-lookup"><span data-stu-id="332c1-282">Is-Single-Valued</span></span>       | <span data-ttu-id="332c1-283">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-283">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-284">É indexado</span><span class="sxs-lookup"><span data-stu-id="332c1-284">Is Indexed</span></span>             | <span data-ttu-id="332c1-285">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-285">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-286">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="332c1-286">In Global Catalog</span></span>      | <span data-ttu-id="332c1-287">Falso</span><span class="sxs-lookup"><span data-stu-id="332c1-287">False</span></span>                                                                                                                        |
| <span data-ttu-id="332c1-288">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="332c1-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="332c1-289">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="332c1-289">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="332c1-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="332c1-290">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="332c1-291">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="332c1-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-292">Search-Flags</span></span>           | <span data-ttu-id="332c1-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="332c1-293">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="332c1-294">System-Flags</span></span>           | <span data-ttu-id="332c1-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="332c1-295">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="332c1-296">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="332c1-296">Classes used in</span></span>        | [<span data-ttu-id="332c1-297">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="332c1-297">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="332c1-298">**Unidade organizacional**</span><span class="sxs-lookup"><span data-stu-id="332c1-298">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





