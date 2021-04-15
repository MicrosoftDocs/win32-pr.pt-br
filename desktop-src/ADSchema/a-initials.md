---
title: Atributo inicials
description: Contém as iniciais de partes do nome completo do usuário. Isso pode ser usado como a inicial do meio no catálogo de endereços do Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Esquema do atributo do AD de iniciais
- Esquema do atributo do AD de iniciais
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753658"
---
# <a name="initials-attribute"></a><span data-ttu-id="03ad8-106">Atributo inicials</span><span class="sxs-lookup"><span data-stu-id="03ad8-106">Initials attribute</span></span>

<span data-ttu-id="03ad8-107">Contém as iniciais de partes do nome completo do usuário.</span><span class="sxs-lookup"><span data-stu-id="03ad8-107">Contains the initials for parts of the user's full name.</span></span> <span data-ttu-id="03ad8-108">Isso pode ser usado como a inicial do meio no catálogo de endereços do Windows.</span><span class="sxs-lookup"><span data-stu-id="03ad8-108">This may be used as the middle initial in the Windows Address Book.</span></span>



| <span data-ttu-id="03ad8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-109">Entry</span></span> | <span data-ttu-id="03ad8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="03ad8-111">CN</span><span class="sxs-lookup"><span data-stu-id="03ad8-111">CN</span></span>                | <span data-ttu-id="03ad8-112">Iniciais</span><span class="sxs-lookup"><span data-stu-id="03ad8-112">Initials</span></span>                                    |
| <span data-ttu-id="03ad8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="03ad8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="03ad8-114">Initials</span><span class="sxs-lookup"><span data-stu-id="03ad8-114">initials</span></span>                                    |
| <span data-ttu-id="03ad8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="03ad8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="03ad8-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="03ad8-116">Update Privilege</span></span>  | <span data-ttu-id="03ad8-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="03ad8-117">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="03ad8-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="03ad8-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="03ad8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-119">Attribute-Id</span></span>      | <span data-ttu-id="03ad8-120">2.5.4.43</span><span class="sxs-lookup"><span data-stu-id="03ad8-120">2.5.4.43</span></span>                                    |
| <span data-ttu-id="03ad8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="03ad8-121">System-Id-Guid</span></span>    | <span data-ttu-id="03ad8-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="03ad8-122">f0f8ff90-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="03ad8-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03ad8-123">Syntax</span></span>            | [<span data-ttu-id="03ad8-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="03ad8-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="03ad8-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="03ad8-125">Implementations</span></span>

-   [<span data-ttu-id="03ad8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="03ad8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="03ad8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="03ad8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="03ad8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="03ad8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="03ad8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="03ad8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="03ad8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="03ad8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="03ad8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="03ad8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="03ad8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03ad8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="03ad8-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-133">Entry</span></span> | <span data-ttu-id="03ad8-134">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="03ad8-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="03ad8-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="03ad8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-136">MAPI-Id</span></span>                | <span data-ttu-id="03ad8-137">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="03ad8-137">0x3A0A</span></span>                                                             |
| <span data-ttu-id="03ad8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="03ad8-138">System-Only</span></span>            | <span data-ttu-id="03ad8-139">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-139">False</span></span>                                                              |
| <span data-ttu-id="03ad8-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="03ad8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="03ad8-141">True</span><span class="sxs-lookup"><span data-stu-id="03ad8-141">True</span></span>                                                               |
| <span data-ttu-id="03ad8-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="03ad8-142">Is Indexed</span></span>             | <span data-ttu-id="03ad8-143">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-143">False</span></span>                                                              |
| <span data-ttu-id="03ad8-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="03ad8-144">In Global Catalog</span></span>      | <span data-ttu-id="03ad8-145">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-145">False</span></span>                                                              |
| <span data-ttu-id="03ad8-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03ad8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="03ad8-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="03ad8-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="03ad8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03ad8-148">Range-Lower</span></span>            | <span data-ttu-id="03ad8-149">1</span><span class="sxs-lookup"><span data-stu-id="03ad8-149">1</span></span>                                                                  |
| <span data-ttu-id="03ad8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03ad8-150">Range-Upper</span></span>            | <span data-ttu-id="03ad8-151">6</span><span class="sxs-lookup"><span data-stu-id="03ad8-151">6</span></span>                                                                  |
| <span data-ttu-id="03ad8-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-152">Search-Flags</span></span>           | <span data-ttu-id="03ad8-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03ad8-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="03ad8-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-154">System-Flags</span></span>           | <span data-ttu-id="03ad8-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03ad8-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="03ad8-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="03ad8-156">Classes used in</span></span>        | [<span data-ttu-id="03ad8-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="03ad8-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="03ad8-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03ad8-158">Windows Server 2003</span></span>



| <span data-ttu-id="03ad8-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-159">Entry</span></span> | <span data-ttu-id="03ad8-160">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad8-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="03ad8-161">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="03ad8-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-162">MAPI-Id</span></span>                | <span data-ttu-id="03ad8-163">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="03ad8-163">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="03ad8-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="03ad8-164">System-Only</span></span>            | <span data-ttu-id="03ad8-165">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-165">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="03ad8-166">Is-Single-Valued</span></span>       | <span data-ttu-id="03ad8-167">True</span><span class="sxs-lookup"><span data-stu-id="03ad8-167">True</span></span>                                                                                                                   |
| <span data-ttu-id="03ad8-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="03ad8-168">Is Indexed</span></span>             | <span data-ttu-id="03ad8-169">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-169">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="03ad8-170">In Global Catalog</span></span>      | <span data-ttu-id="03ad8-171">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-171">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03ad8-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="03ad8-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="03ad8-173">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="03ad8-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03ad8-174">Range-Lower</span></span>            | <span data-ttu-id="03ad8-175">1</span><span class="sxs-lookup"><span data-stu-id="03ad8-175">1</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03ad8-176">Range-Upper</span></span>            | <span data-ttu-id="03ad8-177">6</span><span class="sxs-lookup"><span data-stu-id="03ad8-177">6</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-178">Search-Flags</span></span>           | <span data-ttu-id="03ad8-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03ad8-179">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-180">System-Flags</span></span>           | <span data-ttu-id="03ad8-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03ad8-181">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="03ad8-182">Classes used in</span></span>        | [<span data-ttu-id="03ad8-183">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="03ad8-183">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="03ad8-184">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="03ad8-184">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="03ad8-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="03ad8-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="03ad8-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-186">Entry</span></span> | <span data-ttu-id="03ad8-187">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-187">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad8-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="03ad8-188">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="03ad8-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-189">MAPI-Id</span></span>                | <span data-ttu-id="03ad8-190">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="03ad8-190">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="03ad8-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="03ad8-191">System-Only</span></span>            | <span data-ttu-id="03ad8-192">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="03ad8-193">Is-Single-Valued</span></span>       | <span data-ttu-id="03ad8-194">True</span><span class="sxs-lookup"><span data-stu-id="03ad8-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="03ad8-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="03ad8-195">Is Indexed</span></span>             | <span data-ttu-id="03ad8-196">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="03ad8-197">In Global Catalog</span></span>      | <span data-ttu-id="03ad8-198">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-198">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03ad8-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="03ad8-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="03ad8-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="03ad8-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03ad8-201">Range-Lower</span></span>            | <span data-ttu-id="03ad8-202">1</span><span class="sxs-lookup"><span data-stu-id="03ad8-202">1</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03ad8-203">Range-Upper</span></span>            | <span data-ttu-id="03ad8-204">6</span><span class="sxs-lookup"><span data-stu-id="03ad8-204">6</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-205">Search-Flags</span></span>           | <span data-ttu-id="03ad8-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03ad8-206">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-207">System-Flags</span></span>           | <span data-ttu-id="03ad8-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03ad8-208">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="03ad8-209">Classes used in</span></span>        | [<span data-ttu-id="03ad8-210">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="03ad8-210">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="03ad8-211">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="03ad8-211">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="03ad8-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03ad8-212">Windows Server 2008</span></span>



| <span data-ttu-id="03ad8-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-213">Entry</span></span> | <span data-ttu-id="03ad8-214">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-214">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad8-215">ID do link</span><span class="sxs-lookup"><span data-stu-id="03ad8-215">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="03ad8-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-216">MAPI-Id</span></span>                | <span data-ttu-id="03ad8-217">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="03ad8-217">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="03ad8-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="03ad8-218">System-Only</span></span>            | <span data-ttu-id="03ad8-219">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-219">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="03ad8-220">Is-Single-Valued</span></span>       | <span data-ttu-id="03ad8-221">True</span><span class="sxs-lookup"><span data-stu-id="03ad8-221">True</span></span>                                                                                                                   |
| <span data-ttu-id="03ad8-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="03ad8-222">Is Indexed</span></span>             | <span data-ttu-id="03ad8-223">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-223">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="03ad8-224">In Global Catalog</span></span>      | <span data-ttu-id="03ad8-225">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-225">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03ad8-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="03ad8-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="03ad8-227">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="03ad8-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03ad8-228">Range-Lower</span></span>            | <span data-ttu-id="03ad8-229">1</span><span class="sxs-lookup"><span data-stu-id="03ad8-229">1</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03ad8-230">Range-Upper</span></span>            | <span data-ttu-id="03ad8-231">6</span><span class="sxs-lookup"><span data-stu-id="03ad8-231">6</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-232">Search-Flags</span></span>           | <span data-ttu-id="03ad8-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03ad8-233">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-234">System-Flags</span></span>           | <span data-ttu-id="03ad8-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03ad8-235">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="03ad8-236">Classes used in</span></span>        | [<span data-ttu-id="03ad8-237">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="03ad8-237">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="03ad8-238">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="03ad8-238">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="03ad8-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03ad8-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="03ad8-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-240">Entry</span></span> | <span data-ttu-id="03ad8-241">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-241">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad8-242">ID do link</span><span class="sxs-lookup"><span data-stu-id="03ad8-242">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="03ad8-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-243">MAPI-Id</span></span>                | <span data-ttu-id="03ad8-244">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="03ad8-244">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="03ad8-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="03ad8-245">System-Only</span></span>            | <span data-ttu-id="03ad8-246">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-246">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-247">É de valor único</span><span class="sxs-lookup"><span data-stu-id="03ad8-247">Is-Single-Valued</span></span>       | <span data-ttu-id="03ad8-248">True</span><span class="sxs-lookup"><span data-stu-id="03ad8-248">True</span></span>                                                                                                                   |
| <span data-ttu-id="03ad8-249">É indexado</span><span class="sxs-lookup"><span data-stu-id="03ad8-249">Is Indexed</span></span>             | <span data-ttu-id="03ad8-250">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-250">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-251">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="03ad8-251">In Global Catalog</span></span>      | <span data-ttu-id="03ad8-252">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-252">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03ad8-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="03ad8-254">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="03ad8-254">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="03ad8-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03ad8-255">Range-Lower</span></span>            | <span data-ttu-id="03ad8-256">1</span><span class="sxs-lookup"><span data-stu-id="03ad8-256">1</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03ad8-257">Range-Upper</span></span>            | <span data-ttu-id="03ad8-258">6</span><span class="sxs-lookup"><span data-stu-id="03ad8-258">6</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-259">Search-Flags</span></span>           | <span data-ttu-id="03ad8-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03ad8-260">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-261">System-Flags</span></span>           | <span data-ttu-id="03ad8-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03ad8-262">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="03ad8-263">Classes used in</span></span>        | [<span data-ttu-id="03ad8-264">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="03ad8-264">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="03ad8-265">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="03ad8-265">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="03ad8-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03ad8-266">Windows Server 2012</span></span>



| <span data-ttu-id="03ad8-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="03ad8-267">Entry</span></span> | <span data-ttu-id="03ad8-268">Valor</span><span class="sxs-lookup"><span data-stu-id="03ad8-268">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad8-269">ID do link</span><span class="sxs-lookup"><span data-stu-id="03ad8-269">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="03ad8-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="03ad8-270">MAPI-Id</span></span>                | <span data-ttu-id="03ad8-271">0x3A0A</span><span class="sxs-lookup"><span data-stu-id="03ad8-271">0x3A0A</span></span>                                                                                                                 |
| <span data-ttu-id="03ad8-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="03ad8-272">System-Only</span></span>            | <span data-ttu-id="03ad8-273">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-273">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-274">É de valor único</span><span class="sxs-lookup"><span data-stu-id="03ad8-274">Is-Single-Valued</span></span>       | <span data-ttu-id="03ad8-275">True</span><span class="sxs-lookup"><span data-stu-id="03ad8-275">True</span></span>                                                                                                                   |
| <span data-ttu-id="03ad8-276">É indexado</span><span class="sxs-lookup"><span data-stu-id="03ad8-276">Is Indexed</span></span>             | <span data-ttu-id="03ad8-277">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-277">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-278">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="03ad8-278">In Global Catalog</span></span>      | <span data-ttu-id="03ad8-279">Falso</span><span class="sxs-lookup"><span data-stu-id="03ad8-279">False</span></span>                                                                                                                  |
| <span data-ttu-id="03ad8-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="03ad8-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="03ad8-281">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="03ad8-281">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="03ad8-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="03ad8-282">Range-Lower</span></span>            | <span data-ttu-id="03ad8-283">1</span><span class="sxs-lookup"><span data-stu-id="03ad8-283">1</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="03ad8-284">Range-Upper</span></span>            | <span data-ttu-id="03ad8-285">6</span><span class="sxs-lookup"><span data-stu-id="03ad8-285">6</span></span>                                                                                                                      |
| <span data-ttu-id="03ad8-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-286">Search-Flags</span></span>           | <span data-ttu-id="03ad8-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03ad8-287">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="03ad8-288">System-Flags</span></span>           | <span data-ttu-id="03ad8-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="03ad8-289">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="03ad8-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="03ad8-290">Classes used in</span></span>        | [<span data-ttu-id="03ad8-291">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="03ad8-291">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="03ad8-292">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="03ad8-292">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





