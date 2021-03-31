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
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="a7b35-106">Atributo de endereço de email SMTP</span><span class="sxs-lookup"><span data-stu-id="a7b35-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="a7b35-107">Atributo de endereço de email genérico.</span><span class="sxs-lookup"><span data-stu-id="a7b35-107">Generic mail address attribute.</span></span> <span data-ttu-id="a7b35-108">Usado na caixa como um atributo opcional de objetos de servidor, onde é consumido pela replicação DS baseada em email (se os computadores estiverem tão configurados).</span><span class="sxs-lookup"><span data-stu-id="a7b35-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="a7b35-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-109">Entry</span></span> | <span data-ttu-id="a7b35-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a7b35-111">CN</span><span class="sxs-lookup"><span data-stu-id="a7b35-111">CN</span></span>                | <span data-ttu-id="a7b35-112">Endereço de email SMTP</span><span class="sxs-lookup"><span data-stu-id="a7b35-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="a7b35-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a7b35-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a7b35-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="a7b35-114">mailAddress</span></span>                                 |
| <span data-ttu-id="a7b35-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a7b35-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a7b35-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a7b35-116">Update Privilege</span></span>  | <span data-ttu-id="a7b35-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="a7b35-117">Domain administrator</span></span>                        |
| <span data-ttu-id="a7b35-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a7b35-118">Update Frequency</span></span>  | <span data-ttu-id="a7b35-119">Quase nunca</span><span class="sxs-lookup"><span data-stu-id="a7b35-119">Almost never</span></span>                                |
| <span data-ttu-id="a7b35-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-120">Attribute-Id</span></span>      | <span data-ttu-id="a7b35-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="a7b35-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="a7b35-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a7b35-122">System-Id-Guid</span></span>    | <span data-ttu-id="a7b35-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a7b35-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="a7b35-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7b35-124">Syntax</span></span>            | [<span data-ttu-id="a7b35-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a7b35-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a7b35-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="a7b35-126">Implementations</span></span>

-   [<span data-ttu-id="a7b35-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a7b35-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a7b35-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7b35-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7b35-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a7b35-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a7b35-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7b35-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7b35-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7b35-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7b35-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7b35-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7b35-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7b35-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a7b35-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7b35-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a7b35-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-135">Entry</span></span> | <span data-ttu-id="a7b35-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-139">System-Only</span></span>            | <span data-ttu-id="a7b35-140">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-140">False</span></span>                                 |
| <span data-ttu-id="a7b35-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-142">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-142">True</span></span>                                  |
| <span data-ttu-id="a7b35-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-143">Is Indexed</span></span>             | <span data-ttu-id="a7b35-144">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-144">False</span></span>                                 |
| <span data-ttu-id="a7b35-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-145">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-146">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-146">False</span></span>                                 |
| <span data-ttu-id="a7b35-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-151">Search-Flags</span></span>           | <span data-ttu-id="a7b35-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-152">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-153">System-Flags</span></span>           | <span data-ttu-id="a7b35-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-154">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-155">Classes used in</span></span>        | [<span data-ttu-id="a7b35-156">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a7b35-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7b35-157">Windows Server 2003</span></span>



| <span data-ttu-id="a7b35-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-158">Entry</span></span> | <span data-ttu-id="a7b35-159">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-162">System-Only</span></span>            | <span data-ttu-id="a7b35-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-163">False</span></span>                                 |
| <span data-ttu-id="a7b35-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-165">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-165">True</span></span>                                  |
| <span data-ttu-id="a7b35-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-166">Is Indexed</span></span>             | <span data-ttu-id="a7b35-167">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-167">False</span></span>                                 |
| <span data-ttu-id="a7b35-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-168">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-169">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-169">False</span></span>                                 |
| <span data-ttu-id="a7b35-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-174">Search-Flags</span></span>           | <span data-ttu-id="a7b35-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-175">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-176">System-Flags</span></span>           | <span data-ttu-id="a7b35-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-177">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-178">Classes used in</span></span>        | [<span data-ttu-id="a7b35-179">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a7b35-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="a7b35-180">ADAM</span></span>



| <span data-ttu-id="a7b35-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-181">Entry</span></span> | <span data-ttu-id="a7b35-182">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-185">System-Only</span></span>            | <span data-ttu-id="a7b35-186">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-186">False</span></span>                                 |
| <span data-ttu-id="a7b35-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-188">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-188">True</span></span>                                  |
| <span data-ttu-id="a7b35-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-189">Is Indexed</span></span>             | <span data-ttu-id="a7b35-190">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-190">False</span></span>                                 |
| <span data-ttu-id="a7b35-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-191">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-192">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-192">False</span></span>                                 |
| <span data-ttu-id="a7b35-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-197">Search-Flags</span></span>           | <span data-ttu-id="a7b35-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-198">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-199">System-Flags</span></span>           | <span data-ttu-id="a7b35-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-200">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-201">Classes used in</span></span>        | [<span data-ttu-id="a7b35-202">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7b35-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7b35-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7b35-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-204">Entry</span></span> | <span data-ttu-id="a7b35-205">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-208">System-Only</span></span>            | <span data-ttu-id="a7b35-209">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-209">False</span></span>                                 |
| <span data-ttu-id="a7b35-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-210">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-211">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-211">True</span></span>                                  |
| <span data-ttu-id="a7b35-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-212">Is Indexed</span></span>             | <span data-ttu-id="a7b35-213">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-213">False</span></span>                                 |
| <span data-ttu-id="a7b35-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-214">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-215">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-215">False</span></span>                                 |
| <span data-ttu-id="a7b35-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-220">Search-Flags</span></span>           | <span data-ttu-id="a7b35-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-221">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-222">System-Flags</span></span>           | <span data-ttu-id="a7b35-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-223">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-224">Classes used in</span></span>        | [<span data-ttu-id="a7b35-225">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7b35-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7b35-226">Windows Server 2008</span></span>



| <span data-ttu-id="a7b35-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-227">Entry</span></span> | <span data-ttu-id="a7b35-228">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-231">System-Only</span></span>            | <span data-ttu-id="a7b35-232">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-232">False</span></span>                                 |
| <span data-ttu-id="a7b35-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-233">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-234">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-234">True</span></span>                                  |
| <span data-ttu-id="a7b35-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-235">Is Indexed</span></span>             | <span data-ttu-id="a7b35-236">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-236">False</span></span>                                 |
| <span data-ttu-id="a7b35-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-237">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-238">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-238">False</span></span>                                 |
| <span data-ttu-id="a7b35-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-243">Search-Flags</span></span>           | <span data-ttu-id="a7b35-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-244">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-245">System-Flags</span></span>           | <span data-ttu-id="a7b35-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-246">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-247">Classes used in</span></span>        | [<span data-ttu-id="a7b35-248">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7b35-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7b35-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7b35-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-250">Entry</span></span> | <span data-ttu-id="a7b35-251">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-254">System-Only</span></span>            | <span data-ttu-id="a7b35-255">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-255">False</span></span>                                 |
| <span data-ttu-id="a7b35-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-256">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-257">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-257">True</span></span>                                  |
| <span data-ttu-id="a7b35-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-258">Is Indexed</span></span>             | <span data-ttu-id="a7b35-259">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-259">False</span></span>                                 |
| <span data-ttu-id="a7b35-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-260">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-261">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-261">False</span></span>                                 |
| <span data-ttu-id="a7b35-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-266">Search-Flags</span></span>           | <span data-ttu-id="a7b35-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-267">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-268">System-Flags</span></span>           | <span data-ttu-id="a7b35-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-269">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-270">Classes used in</span></span>        | [<span data-ttu-id="a7b35-271">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7b35-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7b35-272">Windows Server 2012</span></span>



| <span data-ttu-id="a7b35-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7b35-273">Entry</span></span> | <span data-ttu-id="a7b35-274">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b35-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a7b35-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="a7b35-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7b35-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a7b35-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7b35-277">System-Only</span></span>            | <span data-ttu-id="a7b35-278">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-278">False</span></span>                                 |
| <span data-ttu-id="a7b35-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a7b35-279">Is-Single-Valued</span></span>       | <span data-ttu-id="a7b35-280">True</span><span class="sxs-lookup"><span data-stu-id="a7b35-280">True</span></span>                                  |
| <span data-ttu-id="a7b35-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="a7b35-281">Is Indexed</span></span>             | <span data-ttu-id="a7b35-282">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-282">False</span></span>                                 |
| <span data-ttu-id="a7b35-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7b35-283">In Global Catalog</span></span>      | <span data-ttu-id="a7b35-284">Falso</span><span class="sxs-lookup"><span data-stu-id="a7b35-284">False</span></span>                                 |
| <span data-ttu-id="a7b35-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a7b35-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7b35-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a7b35-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a7b35-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7b35-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7b35-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a7b35-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-289">Search-Flags</span></span>           | <span data-ttu-id="a7b35-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7b35-290">0x00000000</span></span>                            |
| <span data-ttu-id="a7b35-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7b35-291">System-Flags</span></span>           | <span data-ttu-id="a7b35-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7b35-292">0x00000010</span></span>                            |
| <span data-ttu-id="a7b35-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a7b35-293">Classes used in</span></span>        | [<span data-ttu-id="a7b35-294">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="a7b35-294">**Server**</span></span>](c-server.md)<br/> |



 

 





