---
title: Flat-Name atributo
description: Para domínios do Windows NT, o nome simples é o nome NetBIOS. Para links com não-8211; Domínios do Windows NT, o nome simples é o nome de identificação desse domínio ou é nulo.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Esquema de Flat-Name do atributo AD
- Esquema de AD do atributo flatname
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456141"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="72274-106">Flat-Name atributo</span><span class="sxs-lookup"><span data-stu-id="72274-106">Flat-Name attribute</span></span>

<span data-ttu-id="72274-107">Para domínios do Windows NT, o nome simples é o nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="72274-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="72274-108">Para links com domínios não Windows NT, o nome simples é o nome de identificação desse domínio ou é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="72274-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="72274-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-109">Entry</span></span> | <span data-ttu-id="72274-110">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="72274-111">CN</span><span class="sxs-lookup"><span data-stu-id="72274-111">CN</span></span>                | <span data-ttu-id="72274-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="72274-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="72274-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72274-113">Ldap-Display-Name</span></span> | <span data-ttu-id="72274-114">flatname</span><span class="sxs-lookup"><span data-stu-id="72274-114">flatName</span></span>                                    |
| <span data-ttu-id="72274-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="72274-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="72274-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="72274-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="72274-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="72274-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="72274-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72274-118">Attribute-Id</span></span>      | <span data-ttu-id="72274-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="72274-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="72274-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72274-120">System-Id-Guid</span></span>    | <span data-ttu-id="72274-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="72274-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="72274-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="72274-122">Syntax</span></span>            | [<span data-ttu-id="72274-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="72274-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="72274-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="72274-124">Implementations</span></span>

-   [<span data-ttu-id="72274-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="72274-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="72274-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72274-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72274-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72274-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72274-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72274-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72274-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72274-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72274-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72274-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="72274-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72274-131">Windows 2000 Server</span></span>



| <span data-ttu-id="72274-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-132">Entry</span></span> | <span data-ttu-id="72274-133">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72274-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="72274-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72274-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="72274-136">System-Only</span></span>            | <span data-ttu-id="72274-137">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-137">False</span></span>                                                |
| <span data-ttu-id="72274-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72274-138">Is-Single-Valued</span></span>       | <span data-ttu-id="72274-139">True</span><span class="sxs-lookup"><span data-stu-id="72274-139">True</span></span>                                                 |
| <span data-ttu-id="72274-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="72274-140">Is Indexed</span></span>             | <span data-ttu-id="72274-141">True</span><span class="sxs-lookup"><span data-stu-id="72274-141">True</span></span>                                                 |
| <span data-ttu-id="72274-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72274-142">In Global Catalog</span></span>      | <span data-ttu-id="72274-143">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-143">False</span></span>                                                |
| <span data-ttu-id="72274-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72274-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="72274-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72274-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="72274-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72274-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="72274-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72274-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="72274-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-148">Search-Flags</span></span>           | <span data-ttu-id="72274-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72274-149">0x00000001</span></span>                                           |
| <span data-ttu-id="72274-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-150">System-Flags</span></span>           | <span data-ttu-id="72274-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72274-151">0x00000010</span></span>                                           |
| <span data-ttu-id="72274-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72274-152">Classes used in</span></span>        | [<span data-ttu-id="72274-153">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="72274-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="72274-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72274-154">Windows Server 2003</span></span>



| <span data-ttu-id="72274-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-155">Entry</span></span> | <span data-ttu-id="72274-156">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72274-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="72274-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72274-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="72274-159">System-Only</span></span>            | <span data-ttu-id="72274-160">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-160">False</span></span>                                                |
| <span data-ttu-id="72274-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72274-161">Is-Single-Valued</span></span>       | <span data-ttu-id="72274-162">True</span><span class="sxs-lookup"><span data-stu-id="72274-162">True</span></span>                                                 |
| <span data-ttu-id="72274-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="72274-163">Is Indexed</span></span>             | <span data-ttu-id="72274-164">True</span><span class="sxs-lookup"><span data-stu-id="72274-164">True</span></span>                                                 |
| <span data-ttu-id="72274-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72274-165">In Global Catalog</span></span>      | <span data-ttu-id="72274-166">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-166">False</span></span>                                                |
| <span data-ttu-id="72274-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72274-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="72274-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72274-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="72274-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72274-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="72274-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72274-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="72274-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-171">Search-Flags</span></span>           | <span data-ttu-id="72274-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72274-172">0x00000001</span></span>                                           |
| <span data-ttu-id="72274-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-173">System-Flags</span></span>           | <span data-ttu-id="72274-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72274-174">0x00000010</span></span>                                           |
| <span data-ttu-id="72274-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72274-175">Classes used in</span></span>        | [<span data-ttu-id="72274-176">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="72274-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72274-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72274-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72274-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-178">Entry</span></span> | <span data-ttu-id="72274-179">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72274-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="72274-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72274-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="72274-182">System-Only</span></span>            | <span data-ttu-id="72274-183">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-183">False</span></span>                                                |
| <span data-ttu-id="72274-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72274-184">Is-Single-Valued</span></span>       | <span data-ttu-id="72274-185">True</span><span class="sxs-lookup"><span data-stu-id="72274-185">True</span></span>                                                 |
| <span data-ttu-id="72274-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="72274-186">Is Indexed</span></span>             | <span data-ttu-id="72274-187">True</span><span class="sxs-lookup"><span data-stu-id="72274-187">True</span></span>                                                 |
| <span data-ttu-id="72274-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72274-188">In Global Catalog</span></span>      | <span data-ttu-id="72274-189">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-189">False</span></span>                                                |
| <span data-ttu-id="72274-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72274-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="72274-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72274-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="72274-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72274-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="72274-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72274-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="72274-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-194">Search-Flags</span></span>           | <span data-ttu-id="72274-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72274-195">0x00000001</span></span>                                           |
| <span data-ttu-id="72274-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-196">System-Flags</span></span>           | <span data-ttu-id="72274-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72274-197">0x00000010</span></span>                                           |
| <span data-ttu-id="72274-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72274-198">Classes used in</span></span>        | [<span data-ttu-id="72274-199">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="72274-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72274-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72274-200">Windows Server 2008</span></span>



| <span data-ttu-id="72274-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-201">Entry</span></span> | <span data-ttu-id="72274-202">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72274-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="72274-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72274-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="72274-205">System-Only</span></span>            | <span data-ttu-id="72274-206">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-206">False</span></span>                                                |
| <span data-ttu-id="72274-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72274-207">Is-Single-Valued</span></span>       | <span data-ttu-id="72274-208">True</span><span class="sxs-lookup"><span data-stu-id="72274-208">True</span></span>                                                 |
| <span data-ttu-id="72274-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="72274-209">Is Indexed</span></span>             | <span data-ttu-id="72274-210">True</span><span class="sxs-lookup"><span data-stu-id="72274-210">True</span></span>                                                 |
| <span data-ttu-id="72274-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72274-211">In Global Catalog</span></span>      | <span data-ttu-id="72274-212">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-212">False</span></span>                                                |
| <span data-ttu-id="72274-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72274-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="72274-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72274-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="72274-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72274-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="72274-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72274-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="72274-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-217">Search-Flags</span></span>           | <span data-ttu-id="72274-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72274-218">0x00000001</span></span>                                           |
| <span data-ttu-id="72274-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-219">System-Flags</span></span>           | <span data-ttu-id="72274-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72274-220">0x00000010</span></span>                                           |
| <span data-ttu-id="72274-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72274-221">Classes used in</span></span>        | [<span data-ttu-id="72274-222">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="72274-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72274-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72274-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72274-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-224">Entry</span></span> | <span data-ttu-id="72274-225">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72274-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="72274-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72274-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="72274-228">System-Only</span></span>            | <span data-ttu-id="72274-229">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-229">False</span></span>                                                |
| <span data-ttu-id="72274-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72274-230">Is-Single-Valued</span></span>       | <span data-ttu-id="72274-231">True</span><span class="sxs-lookup"><span data-stu-id="72274-231">True</span></span>                                                 |
| <span data-ttu-id="72274-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="72274-232">Is Indexed</span></span>             | <span data-ttu-id="72274-233">True</span><span class="sxs-lookup"><span data-stu-id="72274-233">True</span></span>                                                 |
| <span data-ttu-id="72274-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72274-234">In Global Catalog</span></span>      | <span data-ttu-id="72274-235">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-235">False</span></span>                                                |
| <span data-ttu-id="72274-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72274-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="72274-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72274-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="72274-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72274-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="72274-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72274-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="72274-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-240">Search-Flags</span></span>           | <span data-ttu-id="72274-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72274-241">0x00000001</span></span>                                           |
| <span data-ttu-id="72274-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-242">System-Flags</span></span>           | <span data-ttu-id="72274-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72274-243">0x00000010</span></span>                                           |
| <span data-ttu-id="72274-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72274-244">Classes used in</span></span>        | [<span data-ttu-id="72274-245">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="72274-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72274-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72274-246">Windows Server 2012</span></span>



| <span data-ttu-id="72274-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="72274-247">Entry</span></span> | <span data-ttu-id="72274-248">Valor</span><span class="sxs-lookup"><span data-stu-id="72274-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="72274-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="72274-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72274-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="72274-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="72274-251">System-Only</span></span>            | <span data-ttu-id="72274-252">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-252">False</span></span>                                                |
| <span data-ttu-id="72274-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72274-253">Is-Single-Valued</span></span>       | <span data-ttu-id="72274-254">True</span><span class="sxs-lookup"><span data-stu-id="72274-254">True</span></span>                                                 |
| <span data-ttu-id="72274-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="72274-255">Is Indexed</span></span>             | <span data-ttu-id="72274-256">True</span><span class="sxs-lookup"><span data-stu-id="72274-256">True</span></span>                                                 |
| <span data-ttu-id="72274-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72274-257">In Global Catalog</span></span>      | <span data-ttu-id="72274-258">Falso</span><span class="sxs-lookup"><span data-stu-id="72274-258">False</span></span>                                                |
| <span data-ttu-id="72274-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72274-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="72274-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72274-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="72274-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72274-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="72274-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72274-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="72274-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-263">Search-Flags</span></span>           | <span data-ttu-id="72274-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72274-264">0x00000001</span></span>                                           |
| <span data-ttu-id="72274-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72274-265">System-Flags</span></span>           | <span data-ttu-id="72274-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72274-266">0x00000010</span></span>                                           |
| <span data-ttu-id="72274-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72274-267">Classes used in</span></span>        | [<span data-ttu-id="72274-268">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="72274-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





