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
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="ea0b8-106">Atributo de endereço de email SMTP</span><span class="sxs-lookup"><span data-stu-id="ea0b8-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="ea0b8-107">Atributo de endereço de email genérico.</span><span class="sxs-lookup"><span data-stu-id="ea0b8-107">Generic mail address attribute.</span></span> <span data-ttu-id="ea0b8-108">Usado na caixa como um atributo opcional de objetos de servidor, onde é consumido pela replicação DS baseada em email (se os computadores estiverem tão configurados).</span><span class="sxs-lookup"><span data-stu-id="ea0b8-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="ea0b8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-109">Entry</span></span> | <span data-ttu-id="ea0b8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ea0b8-111">CN</span><span class="sxs-lookup"><span data-stu-id="ea0b8-111">CN</span></span>                | <span data-ttu-id="ea0b8-112">Endereço de email SMTP</span><span class="sxs-lookup"><span data-stu-id="ea0b8-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="ea0b8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ea0b8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ea0b8-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="ea0b8-114">mailAddress</span></span>                                 |
| <span data-ttu-id="ea0b8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ea0b8-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ea0b8-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ea0b8-116">Update Privilege</span></span>  | <span data-ttu-id="ea0b8-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="ea0b8-117">Domain administrator</span></span>                        |
| <span data-ttu-id="ea0b8-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ea0b8-118">Update Frequency</span></span>  | <span data-ttu-id="ea0b8-119">Quase nunca</span><span class="sxs-lookup"><span data-stu-id="ea0b8-119">Almost never</span></span>                                |
| <span data-ttu-id="ea0b8-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-120">Attribute-Id</span></span>      | <span data-ttu-id="ea0b8-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="ea0b8-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="ea0b8-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ea0b8-122">System-Id-Guid</span></span>    | <span data-ttu-id="ea0b8-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ea0b8-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="ea0b8-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0b8-124">Syntax</span></span>            | [<span data-ttu-id="ea0b8-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ea0b8-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="ea0b8-126">Implementations</span></span>

-   [<span data-ttu-id="ea0b8-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ea0b8-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ea0b8-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ea0b8-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ea0b8-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ea0b8-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ea0b8-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ea0b8-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea0b8-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ea0b8-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-135">Entry</span></span> | <span data-ttu-id="ea0b8-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-139">System-Only</span></span>            | <span data-ttu-id="ea0b8-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-140">False</span></span>                                 |
| <span data-ttu-id="ea0b8-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-142">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-142">True</span></span>                                  |
| <span data-ttu-id="ea0b8-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-143">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-144">False</span></span>                                 |
| <span data-ttu-id="ea0b8-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-145">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-146">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-146">False</span></span>                                 |
| <span data-ttu-id="ea0b8-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-151">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-152">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-153">System-Flags</span></span>           | <span data-ttu-id="ea0b8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-154">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-155">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-156">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ea0b8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea0b8-157">Windows Server 2003</span></span>



| <span data-ttu-id="ea0b8-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-158">Entry</span></span> | <span data-ttu-id="ea0b8-159">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-162">System-Only</span></span>            | <span data-ttu-id="ea0b8-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-163">False</span></span>                                 |
| <span data-ttu-id="ea0b8-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-165">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-165">True</span></span>                                  |
| <span data-ttu-id="ea0b8-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-166">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-167">False</span></span>                                 |
| <span data-ttu-id="ea0b8-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-168">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-169">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-169">False</span></span>                                 |
| <span data-ttu-id="ea0b8-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-174">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-175">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-176">System-Flags</span></span>           | <span data-ttu-id="ea0b8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-177">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-178">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-179">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ea0b8-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="ea0b8-180">ADAM</span></span>



| <span data-ttu-id="ea0b8-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-181">Entry</span></span> | <span data-ttu-id="ea0b8-182">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-185">System-Only</span></span>            | <span data-ttu-id="ea0b8-186">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-186">False</span></span>                                 |
| <span data-ttu-id="ea0b8-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-188">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-188">True</span></span>                                  |
| <span data-ttu-id="ea0b8-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-189">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-190">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-190">False</span></span>                                 |
| <span data-ttu-id="ea0b8-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-191">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-192">False</span></span>                                 |
| <span data-ttu-id="ea0b8-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-197">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-198">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-199">System-Flags</span></span>           | <span data-ttu-id="ea0b8-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-200">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-201">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-202">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ea0b8-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ea0b8-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ea0b8-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-204">Entry</span></span> | <span data-ttu-id="ea0b8-205">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-208">System-Only</span></span>            | <span data-ttu-id="ea0b8-209">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-209">False</span></span>                                 |
| <span data-ttu-id="ea0b8-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-211">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-211">True</span></span>                                  |
| <span data-ttu-id="ea0b8-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-212">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-213">False</span></span>                                 |
| <span data-ttu-id="ea0b8-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-214">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-215">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-215">False</span></span>                                 |
| <span data-ttu-id="ea0b8-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-220">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-221">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-222">System-Flags</span></span>           | <span data-ttu-id="ea0b8-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-223">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-224">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-225">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ea0b8-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea0b8-226">Windows Server 2008</span></span>



| <span data-ttu-id="ea0b8-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-227">Entry</span></span> | <span data-ttu-id="ea0b8-228">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-231">System-Only</span></span>            | <span data-ttu-id="ea0b8-232">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-232">False</span></span>                                 |
| <span data-ttu-id="ea0b8-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-233">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-234">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-234">True</span></span>                                  |
| <span data-ttu-id="ea0b8-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-235">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-236">False</span></span>                                 |
| <span data-ttu-id="ea0b8-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-237">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-238">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-238">False</span></span>                                 |
| <span data-ttu-id="ea0b8-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-243">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-244">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-245">System-Flags</span></span>           | <span data-ttu-id="ea0b8-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-246">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-247">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-248">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ea0b8-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ea0b8-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ea0b8-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-250">Entry</span></span> | <span data-ttu-id="ea0b8-251">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-254">System-Only</span></span>            | <span data-ttu-id="ea0b8-255">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-255">False</span></span>                                 |
| <span data-ttu-id="ea0b8-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-256">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-257">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-257">True</span></span>                                  |
| <span data-ttu-id="ea0b8-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-258">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-259">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-259">False</span></span>                                 |
| <span data-ttu-id="ea0b8-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-260">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-261">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-261">False</span></span>                                 |
| <span data-ttu-id="ea0b8-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-266">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-267">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-268">System-Flags</span></span>           | <span data-ttu-id="ea0b8-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-269">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-270">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-271">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ea0b8-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea0b8-272">Windows Server 2012</span></span>



| <span data-ttu-id="ea0b8-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="ea0b8-273">Entry</span></span> | <span data-ttu-id="ea0b8-274">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="ea0b8-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="ea0b8-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ea0b8-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="ea0b8-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="ea0b8-277">System-Only</span></span>            | <span data-ttu-id="ea0b8-278">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-278">False</span></span>                                 |
| <span data-ttu-id="ea0b8-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ea0b8-279">Is-Single-Valued</span></span>       | <span data-ttu-id="ea0b8-280">True</span><span class="sxs-lookup"><span data-stu-id="ea0b8-280">True</span></span>                                  |
| <span data-ttu-id="ea0b8-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="ea0b8-281">Is Indexed</span></span>             | <span data-ttu-id="ea0b8-282">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-282">False</span></span>                                 |
| <span data-ttu-id="ea0b8-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ea0b8-283">In Global Catalog</span></span>      | <span data-ttu-id="ea0b8-284">Falso</span><span class="sxs-lookup"><span data-stu-id="ea0b8-284">False</span></span>                                 |
| <span data-ttu-id="ea0b8-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ea0b8-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="ea0b8-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ea0b8-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="ea0b8-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ea0b8-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ea0b8-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="ea0b8-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-289">Search-Flags</span></span>           | <span data-ttu-id="ea0b8-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea0b8-290">0x00000000</span></span>                            |
| <span data-ttu-id="ea0b8-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ea0b8-291">System-Flags</span></span>           | <span data-ttu-id="ea0b8-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea0b8-292">0x00000010</span></span>                            |
| <span data-ttu-id="ea0b8-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ea0b8-293">Classes used in</span></span>        | [<span data-ttu-id="ea0b8-294">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="ea0b8-294">**Server**</span></span>](c-server.md)<br/> |



 

 





