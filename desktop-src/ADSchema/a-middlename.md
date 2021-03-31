---
title: Other-Name atributo
description: Nomes adicionais para um usuário. Por exemplo, nome do meio, patronymic, matronymic ou outros.
ms.assetid: 539de593-e879-4b4a-bf75-c022f53e80de
ms.tgt_platform: multiple
keywords:
- Esquema de Other-Name do atributo AD
- Esquema de AD do atributo MiddleName
topic_type:
- apiref
api_name:
- Other-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e62a9555d77d95d5e30ebacaec5950a19c318b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086954"
---
# <a name="other-name-attribute"></a><span data-ttu-id="bf44a-106">Other-Name atributo</span><span class="sxs-lookup"><span data-stu-id="bf44a-106">Other-Name attribute</span></span>

<span data-ttu-id="bf44a-107">Nomes adicionais para um usuário.</span><span class="sxs-lookup"><span data-stu-id="bf44a-107">Additional names for a user.</span></span> <span data-ttu-id="bf44a-108">Por exemplo, nome do meio, patronymic, matronymic ou outros.</span><span class="sxs-lookup"><span data-stu-id="bf44a-108">For example, middle name, patronymic, matronymic, or others.</span></span>



| <span data-ttu-id="bf44a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-109">Entry</span></span> | <span data-ttu-id="bf44a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bf44a-111">CN</span><span class="sxs-lookup"><span data-stu-id="bf44a-111">CN</span></span>                | <span data-ttu-id="bf44a-112">Other-Name</span><span class="sxs-lookup"><span data-stu-id="bf44a-112">Other-Name</span></span>                                  |
| <span data-ttu-id="bf44a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bf44a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bf44a-114">middleName</span><span class="sxs-lookup"><span data-stu-id="bf44a-114">middleName</span></span>                                  |
| <span data-ttu-id="bf44a-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bf44a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="bf44a-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bf44a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="bf44a-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bf44a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bf44a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-118">Attribute-Id</span></span>      | <span data-ttu-id="bf44a-119">2.16.840.1.113730.3.1.34</span><span class="sxs-lookup"><span data-stu-id="bf44a-119">2.16.840.1.113730.3.1.34</span></span>                    |
| <span data-ttu-id="bf44a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bf44a-120">System-Id-Guid</span></span>    | <span data-ttu-id="bf44a-121">bf9679f2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bf44a-121">bf9679f2-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="bf44a-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf44a-122">Syntax</span></span>            | [<span data-ttu-id="bf44a-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bf44a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bf44a-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="bf44a-124">Implementations</span></span>

-   [<span data-ttu-id="bf44a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bf44a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bf44a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf44a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf44a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf44a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf44a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf44a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf44a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf44a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf44a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf44a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bf44a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf44a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bf44a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-132">Entry</span></span> | <span data-ttu-id="bf44a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bf44a-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf44a-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf44a-136">System-Only</span></span>            | <span data-ttu-id="bf44a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-137">False</span></span>                                                              |
| <span data-ttu-id="bf44a-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf44a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bf44a-139">True</span><span class="sxs-lookup"><span data-stu-id="bf44a-139">True</span></span>                                                               |
| <span data-ttu-id="bf44a-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf44a-140">Is Indexed</span></span>             | <span data-ttu-id="bf44a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-141">False</span></span>                                                              |
| <span data-ttu-id="bf44a-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf44a-142">In Global Catalog</span></span>      | <span data-ttu-id="bf44a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-143">False</span></span>                                                              |
| <span data-ttu-id="bf44a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf44a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf44a-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf44a-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bf44a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf44a-146">Range-Lower</span></span>            | <span data-ttu-id="bf44a-147">0</span><span class="sxs-lookup"><span data-stu-id="bf44a-147">0</span></span>                                                                  |
| <span data-ttu-id="bf44a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf44a-148">Range-Upper</span></span>            | <span data-ttu-id="bf44a-149">64</span><span class="sxs-lookup"><span data-stu-id="bf44a-149">64</span></span>                                                                 |
| <span data-ttu-id="bf44a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-150">Search-Flags</span></span>           | <span data-ttu-id="bf44a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf44a-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="bf44a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-152">System-Flags</span></span>           | <span data-ttu-id="bf44a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf44a-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="bf44a-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf44a-154">Classes used in</span></span>        | [<span data-ttu-id="bf44a-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bf44a-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bf44a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf44a-156">Windows Server 2003</span></span>



| <span data-ttu-id="bf44a-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-157">Entry</span></span> | <span data-ttu-id="bf44a-158">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bf44a-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf44a-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf44a-161">System-Only</span></span>            | <span data-ttu-id="bf44a-162">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-162">False</span></span>                                                              |
| <span data-ttu-id="bf44a-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf44a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bf44a-164">True</span><span class="sxs-lookup"><span data-stu-id="bf44a-164">True</span></span>                                                               |
| <span data-ttu-id="bf44a-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf44a-165">Is Indexed</span></span>             | <span data-ttu-id="bf44a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-166">False</span></span>                                                              |
| <span data-ttu-id="bf44a-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf44a-167">In Global Catalog</span></span>      | <span data-ttu-id="bf44a-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-168">False</span></span>                                                              |
| <span data-ttu-id="bf44a-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf44a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf44a-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf44a-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bf44a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf44a-171">Range-Lower</span></span>            | <span data-ttu-id="bf44a-172">0</span><span class="sxs-lookup"><span data-stu-id="bf44a-172">0</span></span>                                                                  |
| <span data-ttu-id="bf44a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf44a-173">Range-Upper</span></span>            | <span data-ttu-id="bf44a-174">64</span><span class="sxs-lookup"><span data-stu-id="bf44a-174">64</span></span>                                                                 |
| <span data-ttu-id="bf44a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-175">Search-Flags</span></span>           | <span data-ttu-id="bf44a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf44a-176">0x00000000</span></span>                                                         |
| <span data-ttu-id="bf44a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-177">System-Flags</span></span>           | <span data-ttu-id="bf44a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf44a-178">0x00000010</span></span>                                                         |
| <span data-ttu-id="bf44a-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf44a-179">Classes used in</span></span>        | [<span data-ttu-id="bf44a-180">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bf44a-180">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf44a-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf44a-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf44a-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-182">Entry</span></span> | <span data-ttu-id="bf44a-183">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-183">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bf44a-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf44a-184">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-185">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf44a-186">System-Only</span></span>            | <span data-ttu-id="bf44a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-187">False</span></span>                                                              |
| <span data-ttu-id="bf44a-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf44a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bf44a-189">True</span><span class="sxs-lookup"><span data-stu-id="bf44a-189">True</span></span>                                                               |
| <span data-ttu-id="bf44a-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf44a-190">Is Indexed</span></span>             | <span data-ttu-id="bf44a-191">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-191">False</span></span>                                                              |
| <span data-ttu-id="bf44a-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf44a-192">In Global Catalog</span></span>      | <span data-ttu-id="bf44a-193">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-193">False</span></span>                                                              |
| <span data-ttu-id="bf44a-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf44a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf44a-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf44a-195">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bf44a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf44a-196">Range-Lower</span></span>            | <span data-ttu-id="bf44a-197">0</span><span class="sxs-lookup"><span data-stu-id="bf44a-197">0</span></span>                                                                  |
| <span data-ttu-id="bf44a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf44a-198">Range-Upper</span></span>            | <span data-ttu-id="bf44a-199">64</span><span class="sxs-lookup"><span data-stu-id="bf44a-199">64</span></span>                                                                 |
| <span data-ttu-id="bf44a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-200">Search-Flags</span></span>           | <span data-ttu-id="bf44a-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf44a-201">0x00000000</span></span>                                                         |
| <span data-ttu-id="bf44a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-202">System-Flags</span></span>           | <span data-ttu-id="bf44a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf44a-203">0x00000010</span></span>                                                         |
| <span data-ttu-id="bf44a-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf44a-204">Classes used in</span></span>        | [<span data-ttu-id="bf44a-205">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bf44a-205">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf44a-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf44a-206">Windows Server 2008</span></span>



| <span data-ttu-id="bf44a-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-207">Entry</span></span> | <span data-ttu-id="bf44a-208">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-208">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bf44a-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf44a-209">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-210">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf44a-211">System-Only</span></span>            | <span data-ttu-id="bf44a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-212">False</span></span>                                                              |
| <span data-ttu-id="bf44a-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf44a-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bf44a-214">True</span><span class="sxs-lookup"><span data-stu-id="bf44a-214">True</span></span>                                                               |
| <span data-ttu-id="bf44a-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf44a-215">Is Indexed</span></span>             | <span data-ttu-id="bf44a-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-216">False</span></span>                                                              |
| <span data-ttu-id="bf44a-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf44a-217">In Global Catalog</span></span>      | <span data-ttu-id="bf44a-218">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-218">False</span></span>                                                              |
| <span data-ttu-id="bf44a-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf44a-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf44a-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf44a-220">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bf44a-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf44a-221">Range-Lower</span></span>            | <span data-ttu-id="bf44a-222">0</span><span class="sxs-lookup"><span data-stu-id="bf44a-222">0</span></span>                                                                  |
| <span data-ttu-id="bf44a-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf44a-223">Range-Upper</span></span>            | <span data-ttu-id="bf44a-224">64</span><span class="sxs-lookup"><span data-stu-id="bf44a-224">64</span></span>                                                                 |
| <span data-ttu-id="bf44a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-225">Search-Flags</span></span>           | <span data-ttu-id="bf44a-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf44a-226">0x00000000</span></span>                                                         |
| <span data-ttu-id="bf44a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-227">System-Flags</span></span>           | <span data-ttu-id="bf44a-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf44a-228">0x00000010</span></span>                                                         |
| <span data-ttu-id="bf44a-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf44a-229">Classes used in</span></span>        | [<span data-ttu-id="bf44a-230">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bf44a-230">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf44a-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf44a-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf44a-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-232">Entry</span></span> | <span data-ttu-id="bf44a-233">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bf44a-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf44a-234">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-235">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf44a-236">System-Only</span></span>            | <span data-ttu-id="bf44a-237">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-237">False</span></span>                                                              |
| <span data-ttu-id="bf44a-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf44a-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bf44a-239">True</span><span class="sxs-lookup"><span data-stu-id="bf44a-239">True</span></span>                                                               |
| <span data-ttu-id="bf44a-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf44a-240">Is Indexed</span></span>             | <span data-ttu-id="bf44a-241">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-241">False</span></span>                                                              |
| <span data-ttu-id="bf44a-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf44a-242">In Global Catalog</span></span>      | <span data-ttu-id="bf44a-243">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-243">False</span></span>                                                              |
| <span data-ttu-id="bf44a-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf44a-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf44a-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf44a-245">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bf44a-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf44a-246">Range-Lower</span></span>            | <span data-ttu-id="bf44a-247">0</span><span class="sxs-lookup"><span data-stu-id="bf44a-247">0</span></span>                                                                  |
| <span data-ttu-id="bf44a-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf44a-248">Range-Upper</span></span>            | <span data-ttu-id="bf44a-249">64</span><span class="sxs-lookup"><span data-stu-id="bf44a-249">64</span></span>                                                                 |
| <span data-ttu-id="bf44a-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-250">Search-Flags</span></span>           | <span data-ttu-id="bf44a-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf44a-251">0x00000000</span></span>                                                         |
| <span data-ttu-id="bf44a-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-252">System-Flags</span></span>           | <span data-ttu-id="bf44a-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf44a-253">0x00000010</span></span>                                                         |
| <span data-ttu-id="bf44a-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf44a-254">Classes used in</span></span>        | [<span data-ttu-id="bf44a-255">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bf44a-255">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf44a-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf44a-256">Windows Server 2012</span></span>



| <span data-ttu-id="bf44a-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf44a-257">Entry</span></span> | <span data-ttu-id="bf44a-258">Valor</span><span class="sxs-lookup"><span data-stu-id="bf44a-258">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bf44a-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf44a-259">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf44a-260">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bf44a-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf44a-261">System-Only</span></span>            | <span data-ttu-id="bf44a-262">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-262">False</span></span>                                                              |
| <span data-ttu-id="bf44a-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf44a-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bf44a-264">True</span><span class="sxs-lookup"><span data-stu-id="bf44a-264">True</span></span>                                                               |
| <span data-ttu-id="bf44a-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf44a-265">Is Indexed</span></span>             | <span data-ttu-id="bf44a-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-266">False</span></span>                                                              |
| <span data-ttu-id="bf44a-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf44a-267">In Global Catalog</span></span>      | <span data-ttu-id="bf44a-268">Falso</span><span class="sxs-lookup"><span data-stu-id="bf44a-268">False</span></span>                                                              |
| <span data-ttu-id="bf44a-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf44a-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf44a-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf44a-270">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bf44a-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf44a-271">Range-Lower</span></span>            | <span data-ttu-id="bf44a-272">0</span><span class="sxs-lookup"><span data-stu-id="bf44a-272">0</span></span>                                                                  |
| <span data-ttu-id="bf44a-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf44a-273">Range-Upper</span></span>            | <span data-ttu-id="bf44a-274">64</span><span class="sxs-lookup"><span data-stu-id="bf44a-274">64</span></span>                                                                 |
| <span data-ttu-id="bf44a-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-275">Search-Flags</span></span>           | <span data-ttu-id="bf44a-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf44a-276">0x00000000</span></span>                                                         |
| <span data-ttu-id="bf44a-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf44a-277">System-Flags</span></span>           | <span data-ttu-id="bf44a-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf44a-278">0x00000010</span></span>                                                         |
| <span data-ttu-id="bf44a-279">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf44a-279">Classes used in</span></span>        | [<span data-ttu-id="bf44a-280">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bf44a-280">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





