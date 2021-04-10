---
title: Atributo de endereço de email SMTP
description: Atributo de endereço de email genérico. Usado na caixa como um atributo opcional de objetos de servidor, onde é consumido pela replicação DS baseada em email (se os computadores estiverem tão configurados).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo de email SMTP
- Esquema de AD do atributo mailAddress
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086738"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="8a812-106">Atributo de endereço de email SMTP</span><span class="sxs-lookup"><span data-stu-id="8a812-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="8a812-107">Atributo de endereço de email genérico.</span><span class="sxs-lookup"><span data-stu-id="8a812-107">Generic mail address attribute.</span></span> <span data-ttu-id="8a812-108">Usado na caixa como um atributo opcional de objetos de servidor, onde é consumido pela replicação DS baseada em email (se os computadores estiverem tão configurados).</span><span class="sxs-lookup"><span data-stu-id="8a812-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="8a812-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-109">Entry</span></span> | <span data-ttu-id="8a812-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8a812-111">CN</span><span class="sxs-lookup"><span data-stu-id="8a812-111">CN</span></span>                | <span data-ttu-id="8a812-112">Endereço de email SMTP</span><span class="sxs-lookup"><span data-stu-id="8a812-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="8a812-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8a812-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8a812-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="8a812-114">mailAddress</span></span>                                 |
| <span data-ttu-id="8a812-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8a812-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="8a812-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8a812-116">Update Privilege</span></span>  | <span data-ttu-id="8a812-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="8a812-117">Domain administrator</span></span>                        |
| <span data-ttu-id="8a812-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8a812-118">Update Frequency</span></span>  | <span data-ttu-id="8a812-119">Quase nunca</span><span class="sxs-lookup"><span data-stu-id="8a812-119">Almost never</span></span>                                |
| <span data-ttu-id="8a812-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-120">Attribute-Id</span></span>      | <span data-ttu-id="8a812-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="8a812-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="8a812-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8a812-122">System-Id-Guid</span></span>    | <span data-ttu-id="8a812-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8a812-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="8a812-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a812-124">Syntax</span></span>            | [<span data-ttu-id="8a812-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8a812-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8a812-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="8a812-126">Implementations</span></span>

-   [<span data-ttu-id="8a812-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a812-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a812-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a812-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a812-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8a812-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8a812-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a812-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a812-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a812-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a812-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a812-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a812-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a812-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a812-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a812-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8a812-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-135">Entry</span></span> | <span data-ttu-id="8a812-136">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-139">System-Only</span></span>            | <span data-ttu-id="8a812-140">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-140">False</span></span>                                 |
| <span data-ttu-id="8a812-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-142">True</span><span class="sxs-lookup"><span data-stu-id="8a812-142">True</span></span>                                  |
| <span data-ttu-id="8a812-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-143">Is Indexed</span></span>             | <span data-ttu-id="8a812-144">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-144">False</span></span>                                 |
| <span data-ttu-id="8a812-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-145">In Global Catalog</span></span>      | <span data-ttu-id="8a812-146">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-146">False</span></span>                                 |
| <span data-ttu-id="8a812-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-151">Search-Flags</span></span>           | <span data-ttu-id="8a812-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-152">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-153">System-Flags</span></span>           | <span data-ttu-id="8a812-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-154">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-155">Classes used in</span></span>        | [<span data-ttu-id="8a812-156">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a812-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a812-157">Windows Server 2003</span></span>



| <span data-ttu-id="8a812-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-158">Entry</span></span> | <span data-ttu-id="8a812-159">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-162">System-Only</span></span>            | <span data-ttu-id="8a812-163">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-163">False</span></span>                                 |
| <span data-ttu-id="8a812-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-164">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-165">True</span><span class="sxs-lookup"><span data-stu-id="8a812-165">True</span></span>                                  |
| <span data-ttu-id="8a812-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-166">Is Indexed</span></span>             | <span data-ttu-id="8a812-167">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-167">False</span></span>                                 |
| <span data-ttu-id="8a812-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-168">In Global Catalog</span></span>      | <span data-ttu-id="8a812-169">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-169">False</span></span>                                 |
| <span data-ttu-id="8a812-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-174">Search-Flags</span></span>           | <span data-ttu-id="8a812-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-175">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-176">System-Flags</span></span>           | <span data-ttu-id="8a812-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-177">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-178">Classes used in</span></span>        | [<span data-ttu-id="8a812-179">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8a812-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="8a812-180">ADAM</span></span>



| <span data-ttu-id="8a812-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-181">Entry</span></span> | <span data-ttu-id="8a812-182">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-185">System-Only</span></span>            | <span data-ttu-id="8a812-186">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-186">False</span></span>                                 |
| <span data-ttu-id="8a812-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-188">True</span><span class="sxs-lookup"><span data-stu-id="8a812-188">True</span></span>                                  |
| <span data-ttu-id="8a812-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-189">Is Indexed</span></span>             | <span data-ttu-id="8a812-190">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-190">False</span></span>                                 |
| <span data-ttu-id="8a812-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-191">In Global Catalog</span></span>      | <span data-ttu-id="8a812-192">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-192">False</span></span>                                 |
| <span data-ttu-id="8a812-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-197">Search-Flags</span></span>           | <span data-ttu-id="8a812-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-198">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-199">System-Flags</span></span>           | <span data-ttu-id="8a812-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-200">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-201">Classes used in</span></span>        | [<span data-ttu-id="8a812-202">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a812-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a812-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a812-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-204">Entry</span></span> | <span data-ttu-id="8a812-205">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-208">System-Only</span></span>            | <span data-ttu-id="8a812-209">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-209">False</span></span>                                 |
| <span data-ttu-id="8a812-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-210">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-211">True</span><span class="sxs-lookup"><span data-stu-id="8a812-211">True</span></span>                                  |
| <span data-ttu-id="8a812-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-212">Is Indexed</span></span>             | <span data-ttu-id="8a812-213">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-213">False</span></span>                                 |
| <span data-ttu-id="8a812-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-214">In Global Catalog</span></span>      | <span data-ttu-id="8a812-215">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-215">False</span></span>                                 |
| <span data-ttu-id="8a812-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-220">Search-Flags</span></span>           | <span data-ttu-id="8a812-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-221">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-222">System-Flags</span></span>           | <span data-ttu-id="8a812-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-223">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-224">Classes used in</span></span>        | [<span data-ttu-id="8a812-225">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a812-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a812-226">Windows Server 2008</span></span>



| <span data-ttu-id="8a812-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-227">Entry</span></span> | <span data-ttu-id="8a812-228">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-231">System-Only</span></span>            | <span data-ttu-id="8a812-232">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-232">False</span></span>                                 |
| <span data-ttu-id="8a812-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-233">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-234">True</span><span class="sxs-lookup"><span data-stu-id="8a812-234">True</span></span>                                  |
| <span data-ttu-id="8a812-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-235">Is Indexed</span></span>             | <span data-ttu-id="8a812-236">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-236">False</span></span>                                 |
| <span data-ttu-id="8a812-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-237">In Global Catalog</span></span>      | <span data-ttu-id="8a812-238">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-238">False</span></span>                                 |
| <span data-ttu-id="8a812-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-243">Search-Flags</span></span>           | <span data-ttu-id="8a812-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-244">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-245">System-Flags</span></span>           | <span data-ttu-id="8a812-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-246">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-247">Classes used in</span></span>        | [<span data-ttu-id="8a812-248">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a812-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a812-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a812-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-250">Entry</span></span> | <span data-ttu-id="8a812-251">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-254">System-Only</span></span>            | <span data-ttu-id="8a812-255">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-255">False</span></span>                                 |
| <span data-ttu-id="8a812-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-256">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-257">True</span><span class="sxs-lookup"><span data-stu-id="8a812-257">True</span></span>                                  |
| <span data-ttu-id="8a812-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-258">Is Indexed</span></span>             | <span data-ttu-id="8a812-259">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-259">False</span></span>                                 |
| <span data-ttu-id="8a812-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-260">In Global Catalog</span></span>      | <span data-ttu-id="8a812-261">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-261">False</span></span>                                 |
| <span data-ttu-id="8a812-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-266">Search-Flags</span></span>           | <span data-ttu-id="8a812-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-267">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-268">System-Flags</span></span>           | <span data-ttu-id="8a812-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-269">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-270">Classes used in</span></span>        | [<span data-ttu-id="8a812-271">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a812-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a812-272">Windows Server 2012</span></span>



| <span data-ttu-id="8a812-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a812-273">Entry</span></span> | <span data-ttu-id="8a812-274">Valor</span><span class="sxs-lookup"><span data-stu-id="8a812-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="8a812-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a812-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a812-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="8a812-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a812-277">System-Only</span></span>            | <span data-ttu-id="8a812-278">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-278">False</span></span>                                 |
| <span data-ttu-id="8a812-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a812-279">Is-Single-Valued</span></span>       | <span data-ttu-id="8a812-280">True</span><span class="sxs-lookup"><span data-stu-id="8a812-280">True</span></span>                                  |
| <span data-ttu-id="8a812-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a812-281">Is Indexed</span></span>             | <span data-ttu-id="8a812-282">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-282">False</span></span>                                 |
| <span data-ttu-id="8a812-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a812-283">In Global Catalog</span></span>      | <span data-ttu-id="8a812-284">Falso</span><span class="sxs-lookup"><span data-stu-id="8a812-284">False</span></span>                                 |
| <span data-ttu-id="8a812-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a812-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a812-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a812-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="8a812-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a812-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="8a812-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a812-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="8a812-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-289">Search-Flags</span></span>           | <span data-ttu-id="8a812-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a812-290">0x00000000</span></span>                            |
| <span data-ttu-id="8a812-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a812-291">System-Flags</span></span>           | <span data-ttu-id="8a812-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a812-292">0x00000010</span></span>                            |
| <span data-ttu-id="8a812-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a812-293">Classes used in</span></span>        | [<span data-ttu-id="8a812-294">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="8a812-294">**Server**</span></span>](c-server.md)<br/> |



 

 





