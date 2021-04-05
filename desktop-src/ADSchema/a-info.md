---
title: Atributo de comentário
description: Os comentários do usuário. Essa cadeia de caracteres pode ser uma cadeia de caracteres nula.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Atributo de comentário do esquema do AD
- atributo de informações esquema do AD
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645327"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="cebb5-106">Atributo de comentário (esquema do AD)</span><span class="sxs-lookup"><span data-stu-id="cebb5-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="cebb5-107">Os comentários do usuário.</span><span class="sxs-lookup"><span data-stu-id="cebb5-107">The user's comments.</span></span> <span data-ttu-id="cebb5-108">Essa cadeia de caracteres pode ser uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="cebb5-108">This string can be a null string.</span></span>



| <span data-ttu-id="cebb5-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-109">Entry</span></span> | <span data-ttu-id="cebb5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="cebb5-111">CN</span><span class="sxs-lookup"><span data-stu-id="cebb5-111">CN</span></span>                | <span data-ttu-id="cebb5-112">Comentário</span><span class="sxs-lookup"><span data-stu-id="cebb5-112">Comment</span></span>                                                                  |
| <span data-ttu-id="cebb5-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cebb5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cebb5-114">informações</span><span class="sxs-lookup"><span data-stu-id="cebb5-114">info</span></span>                                                                     |
| <span data-ttu-id="cebb5-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cebb5-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="cebb5-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="cebb5-116">Update Privilege</span></span>  | <span data-ttu-id="cebb5-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="cebb5-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="cebb5-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="cebb5-118">Update Frequency</span></span>  | <span data-ttu-id="cebb5-119">Sempre que o usuário ou administrador precisar adicionar comentários na conta.</span><span class="sxs-lookup"><span data-stu-id="cebb5-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="cebb5-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-120">Attribute-Id</span></span>      | <span data-ttu-id="cebb5-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="cebb5-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="cebb5-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cebb5-122">System-Id-Guid</span></span>    | <span data-ttu-id="cebb5-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cebb5-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="cebb5-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="cebb5-124">Syntax</span></span>            | [<span data-ttu-id="cebb5-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cebb5-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="cebb5-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="cebb5-126">Implementations</span></span>

-   [<span data-ttu-id="cebb5-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cebb5-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cebb5-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cebb5-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cebb5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cebb5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cebb5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cebb5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cebb5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cebb5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cebb5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cebb5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cebb5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cebb5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="cebb5-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-134">Entry</span></span> | <span data-ttu-id="cebb5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cebb5-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="cebb5-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cebb5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-137">MAPI-Id</span></span>                | <span data-ttu-id="cebb5-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="cebb5-138">0x3004</span></span>                                               |
| <span data-ttu-id="cebb5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="cebb5-139">System-Only</span></span>            | <span data-ttu-id="cebb5-140">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-140">False</span></span>                                                |
| <span data-ttu-id="cebb5-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cebb5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="cebb5-142">True</span><span class="sxs-lookup"><span data-stu-id="cebb5-142">True</span></span>                                                 |
| <span data-ttu-id="cebb5-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="cebb5-143">Is Indexed</span></span>             | <span data-ttu-id="cebb5-144">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-144">False</span></span>                                                |
| <span data-ttu-id="cebb5-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cebb5-145">In Global Catalog</span></span>      | <span data-ttu-id="cebb5-146">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-146">False</span></span>                                                |
| <span data-ttu-id="cebb5-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cebb5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="cebb5-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cebb5-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cebb5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cebb5-149">Range-Lower</span></span>            | <span data-ttu-id="cebb5-150">1</span><span class="sxs-lookup"><span data-stu-id="cebb5-150">1</span></span>                                                    |
| <span data-ttu-id="cebb5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cebb5-151">Range-Upper</span></span>            | <span data-ttu-id="cebb5-152">1024</span><span class="sxs-lookup"><span data-stu-id="cebb5-152">1024</span></span>                                                 |
| <span data-ttu-id="cebb5-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-153">Search-Flags</span></span>           | <span data-ttu-id="cebb5-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cebb5-154">0x00000000</span></span>                                           |
| <span data-ttu-id="cebb5-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-155">System-Flags</span></span>           | <span data-ttu-id="cebb5-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cebb5-156">0x00000010</span></span>                                           |
| <span data-ttu-id="cebb5-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cebb5-157">Classes used in</span></span>        | [<span data-ttu-id="cebb5-158">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="cebb5-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cebb5-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cebb5-159">Windows Server 2003</span></span>



| <span data-ttu-id="cebb5-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-160">Entry</span></span> | <span data-ttu-id="cebb5-161">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cebb5-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="cebb5-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cebb5-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-163">MAPI-Id</span></span>                | <span data-ttu-id="cebb5-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="cebb5-164">0x3004</span></span>                                               |
| <span data-ttu-id="cebb5-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="cebb5-165">System-Only</span></span>            | <span data-ttu-id="cebb5-166">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-166">False</span></span>                                                |
| <span data-ttu-id="cebb5-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cebb5-167">Is-Single-Valued</span></span>       | <span data-ttu-id="cebb5-168">True</span><span class="sxs-lookup"><span data-stu-id="cebb5-168">True</span></span>                                                 |
| <span data-ttu-id="cebb5-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="cebb5-169">Is Indexed</span></span>             | <span data-ttu-id="cebb5-170">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-170">False</span></span>                                                |
| <span data-ttu-id="cebb5-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cebb5-171">In Global Catalog</span></span>      | <span data-ttu-id="cebb5-172">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-172">False</span></span>                                                |
| <span data-ttu-id="cebb5-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cebb5-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="cebb5-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cebb5-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cebb5-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cebb5-175">Range-Lower</span></span>            | <span data-ttu-id="cebb5-176">1</span><span class="sxs-lookup"><span data-stu-id="cebb5-176">1</span></span>                                                    |
| <span data-ttu-id="cebb5-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cebb5-177">Range-Upper</span></span>            | <span data-ttu-id="cebb5-178">1024</span><span class="sxs-lookup"><span data-stu-id="cebb5-178">1024</span></span>                                                 |
| <span data-ttu-id="cebb5-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-179">Search-Flags</span></span>           | <span data-ttu-id="cebb5-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cebb5-180">0x00000000</span></span>                                           |
| <span data-ttu-id="cebb5-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-181">System-Flags</span></span>           | <span data-ttu-id="cebb5-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cebb5-182">0x00000010</span></span>                                           |
| <span data-ttu-id="cebb5-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cebb5-183">Classes used in</span></span>        | [<span data-ttu-id="cebb5-184">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="cebb5-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cebb5-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cebb5-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cebb5-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-186">Entry</span></span> | <span data-ttu-id="cebb5-187">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cebb5-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="cebb5-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cebb5-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-189">MAPI-Id</span></span>                | <span data-ttu-id="cebb5-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="cebb5-190">0x3004</span></span>                                               |
| <span data-ttu-id="cebb5-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="cebb5-191">System-Only</span></span>            | <span data-ttu-id="cebb5-192">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-192">False</span></span>                                                |
| <span data-ttu-id="cebb5-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cebb5-193">Is-Single-Valued</span></span>       | <span data-ttu-id="cebb5-194">True</span><span class="sxs-lookup"><span data-stu-id="cebb5-194">True</span></span>                                                 |
| <span data-ttu-id="cebb5-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="cebb5-195">Is Indexed</span></span>             | <span data-ttu-id="cebb5-196">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-196">False</span></span>                                                |
| <span data-ttu-id="cebb5-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cebb5-197">In Global Catalog</span></span>      | <span data-ttu-id="cebb5-198">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-198">False</span></span>                                                |
| <span data-ttu-id="cebb5-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cebb5-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="cebb5-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cebb5-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cebb5-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cebb5-201">Range-Lower</span></span>            | <span data-ttu-id="cebb5-202">1</span><span class="sxs-lookup"><span data-stu-id="cebb5-202">1</span></span>                                                    |
| <span data-ttu-id="cebb5-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cebb5-203">Range-Upper</span></span>            | <span data-ttu-id="cebb5-204">1024</span><span class="sxs-lookup"><span data-stu-id="cebb5-204">1024</span></span>                                                 |
| <span data-ttu-id="cebb5-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-205">Search-Flags</span></span>           | <span data-ttu-id="cebb5-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cebb5-206">0x00000000</span></span>                                           |
| <span data-ttu-id="cebb5-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-207">System-Flags</span></span>           | <span data-ttu-id="cebb5-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cebb5-208">0x00000010</span></span>                                           |
| <span data-ttu-id="cebb5-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cebb5-209">Classes used in</span></span>        | [<span data-ttu-id="cebb5-210">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="cebb5-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cebb5-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cebb5-211">Windows Server 2008</span></span>



| <span data-ttu-id="cebb5-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-212">Entry</span></span> | <span data-ttu-id="cebb5-213">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cebb5-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="cebb5-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cebb5-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-215">MAPI-Id</span></span>                | <span data-ttu-id="cebb5-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="cebb5-216">0x3004</span></span>                                               |
| <span data-ttu-id="cebb5-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="cebb5-217">System-Only</span></span>            | <span data-ttu-id="cebb5-218">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-218">False</span></span>                                                |
| <span data-ttu-id="cebb5-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cebb5-219">Is-Single-Valued</span></span>       | <span data-ttu-id="cebb5-220">True</span><span class="sxs-lookup"><span data-stu-id="cebb5-220">True</span></span>                                                 |
| <span data-ttu-id="cebb5-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="cebb5-221">Is Indexed</span></span>             | <span data-ttu-id="cebb5-222">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-222">False</span></span>                                                |
| <span data-ttu-id="cebb5-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cebb5-223">In Global Catalog</span></span>      | <span data-ttu-id="cebb5-224">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-224">False</span></span>                                                |
| <span data-ttu-id="cebb5-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cebb5-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="cebb5-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cebb5-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cebb5-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cebb5-227">Range-Lower</span></span>            | <span data-ttu-id="cebb5-228">1</span><span class="sxs-lookup"><span data-stu-id="cebb5-228">1</span></span>                                                    |
| <span data-ttu-id="cebb5-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cebb5-229">Range-Upper</span></span>            | <span data-ttu-id="cebb5-230">1024</span><span class="sxs-lookup"><span data-stu-id="cebb5-230">1024</span></span>                                                 |
| <span data-ttu-id="cebb5-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-231">Search-Flags</span></span>           | <span data-ttu-id="cebb5-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cebb5-232">0x00000000</span></span>                                           |
| <span data-ttu-id="cebb5-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-233">System-Flags</span></span>           | <span data-ttu-id="cebb5-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cebb5-234">0x00000010</span></span>                                           |
| <span data-ttu-id="cebb5-235">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cebb5-235">Classes used in</span></span>        | [<span data-ttu-id="cebb5-236">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="cebb5-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cebb5-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cebb5-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cebb5-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-238">Entry</span></span> | <span data-ttu-id="cebb5-239">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cebb5-240">ID do link</span><span class="sxs-lookup"><span data-stu-id="cebb5-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cebb5-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-241">MAPI-Id</span></span>                | <span data-ttu-id="cebb5-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="cebb5-242">0x3004</span></span>                                               |
| <span data-ttu-id="cebb5-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="cebb5-243">System-Only</span></span>            | <span data-ttu-id="cebb5-244">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-244">False</span></span>                                                |
| <span data-ttu-id="cebb5-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cebb5-245">Is-Single-Valued</span></span>       | <span data-ttu-id="cebb5-246">True</span><span class="sxs-lookup"><span data-stu-id="cebb5-246">True</span></span>                                                 |
| <span data-ttu-id="cebb5-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="cebb5-247">Is Indexed</span></span>             | <span data-ttu-id="cebb5-248">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-248">False</span></span>                                                |
| <span data-ttu-id="cebb5-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cebb5-249">In Global Catalog</span></span>      | <span data-ttu-id="cebb5-250">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-250">False</span></span>                                                |
| <span data-ttu-id="cebb5-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cebb5-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="cebb5-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cebb5-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cebb5-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cebb5-253">Range-Lower</span></span>            | <span data-ttu-id="cebb5-254">1</span><span class="sxs-lookup"><span data-stu-id="cebb5-254">1</span></span>                                                    |
| <span data-ttu-id="cebb5-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cebb5-255">Range-Upper</span></span>            | <span data-ttu-id="cebb5-256">1024</span><span class="sxs-lookup"><span data-stu-id="cebb5-256">1024</span></span>                                                 |
| <span data-ttu-id="cebb5-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-257">Search-Flags</span></span>           | <span data-ttu-id="cebb5-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cebb5-258">0x00000000</span></span>                                           |
| <span data-ttu-id="cebb5-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-259">System-Flags</span></span>           | <span data-ttu-id="cebb5-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cebb5-260">0x00000010</span></span>                                           |
| <span data-ttu-id="cebb5-261">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cebb5-261">Classes used in</span></span>        | [<span data-ttu-id="cebb5-262">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="cebb5-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cebb5-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cebb5-263">Windows Server 2012</span></span>



| <span data-ttu-id="cebb5-264">Entrada</span><span class="sxs-lookup"><span data-stu-id="cebb5-264">Entry</span></span> | <span data-ttu-id="cebb5-265">Valor</span><span class="sxs-lookup"><span data-stu-id="cebb5-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="cebb5-266">ID do link</span><span class="sxs-lookup"><span data-stu-id="cebb5-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="cebb5-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cebb5-267">MAPI-Id</span></span>                | <span data-ttu-id="cebb5-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="cebb5-268">0x3004</span></span>                                               |
| <span data-ttu-id="cebb5-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="cebb5-269">System-Only</span></span>            | <span data-ttu-id="cebb5-270">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-270">False</span></span>                                                |
| <span data-ttu-id="cebb5-271">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cebb5-271">Is-Single-Valued</span></span>       | <span data-ttu-id="cebb5-272">True</span><span class="sxs-lookup"><span data-stu-id="cebb5-272">True</span></span>                                                 |
| <span data-ttu-id="cebb5-273">É indexado</span><span class="sxs-lookup"><span data-stu-id="cebb5-273">Is Indexed</span></span>             | <span data-ttu-id="cebb5-274">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-274">False</span></span>                                                |
| <span data-ttu-id="cebb5-275">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cebb5-275">In Global Catalog</span></span>      | <span data-ttu-id="cebb5-276">Falso</span><span class="sxs-lookup"><span data-stu-id="cebb5-276">False</span></span>                                                |
| <span data-ttu-id="cebb5-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cebb5-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="cebb5-278">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cebb5-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="cebb5-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cebb5-279">Range-Lower</span></span>            | <span data-ttu-id="cebb5-280">1</span><span class="sxs-lookup"><span data-stu-id="cebb5-280">1</span></span>                                                    |
| <span data-ttu-id="cebb5-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cebb5-281">Range-Upper</span></span>            | <span data-ttu-id="cebb5-282">1024</span><span class="sxs-lookup"><span data-stu-id="cebb5-282">1024</span></span>                                                 |
| <span data-ttu-id="cebb5-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-283">Search-Flags</span></span>           | <span data-ttu-id="cebb5-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cebb5-284">0x00000000</span></span>                                           |
| <span data-ttu-id="cebb5-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cebb5-285">System-Flags</span></span>           | <span data-ttu-id="cebb5-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cebb5-286">0x00000010</span></span>                                           |
| <span data-ttu-id="cebb5-287">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cebb5-287">Classes used in</span></span>        | [<span data-ttu-id="cebb5-288">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="cebb5-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





