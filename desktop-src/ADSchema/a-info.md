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
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="07a14-106">Atributo de comentário (esquema do AD)</span><span class="sxs-lookup"><span data-stu-id="07a14-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="07a14-107">Os comentários do usuário.</span><span class="sxs-lookup"><span data-stu-id="07a14-107">The user's comments.</span></span> <span data-ttu-id="07a14-108">Essa cadeia de caracteres pode ser uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="07a14-108">This string can be a null string.</span></span>



| <span data-ttu-id="07a14-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-109">Entry</span></span> | <span data-ttu-id="07a14-110">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="07a14-111">CN</span><span class="sxs-lookup"><span data-stu-id="07a14-111">CN</span></span>                | <span data-ttu-id="07a14-112">Comentário</span><span class="sxs-lookup"><span data-stu-id="07a14-112">Comment</span></span>                                                                  |
| <span data-ttu-id="07a14-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="07a14-113">Ldap-Display-Name</span></span> | <span data-ttu-id="07a14-114">informações</span><span class="sxs-lookup"><span data-stu-id="07a14-114">info</span></span>                                                                     |
| <span data-ttu-id="07a14-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="07a14-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="07a14-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="07a14-116">Update Privilege</span></span>  | <span data-ttu-id="07a14-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="07a14-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="07a14-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="07a14-118">Update Frequency</span></span>  | <span data-ttu-id="07a14-119">Sempre que o usuário ou administrador precisar adicionar comentários na conta.</span><span class="sxs-lookup"><span data-stu-id="07a14-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="07a14-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-120">Attribute-Id</span></span>      | <span data-ttu-id="07a14-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="07a14-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="07a14-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="07a14-122">System-Id-Guid</span></span>    | <span data-ttu-id="07a14-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="07a14-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="07a14-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07a14-124">Syntax</span></span>            | [<span data-ttu-id="07a14-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="07a14-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="07a14-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="07a14-126">Implementations</span></span>

-   [<span data-ttu-id="07a14-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="07a14-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="07a14-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="07a14-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="07a14-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="07a14-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="07a14-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="07a14-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="07a14-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="07a14-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="07a14-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="07a14-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="07a14-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="07a14-133">Windows 2000 Server</span></span>



| <span data-ttu-id="07a14-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-134">Entry</span></span> | <span data-ttu-id="07a14-135">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="07a14-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="07a14-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="07a14-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-137">MAPI-Id</span></span>                | <span data-ttu-id="07a14-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="07a14-138">0x3004</span></span>                                               |
| <span data-ttu-id="07a14-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a14-139">System-Only</span></span>            | <span data-ttu-id="07a14-140">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-140">False</span></span>                                                |
| <span data-ttu-id="07a14-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="07a14-141">Is-Single-Valued</span></span>       | <span data-ttu-id="07a14-142">True</span><span class="sxs-lookup"><span data-stu-id="07a14-142">True</span></span>                                                 |
| <span data-ttu-id="07a14-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="07a14-143">Is Indexed</span></span>             | <span data-ttu-id="07a14-144">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-144">False</span></span>                                                |
| <span data-ttu-id="07a14-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="07a14-145">In Global Catalog</span></span>      | <span data-ttu-id="07a14-146">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-146">False</span></span>                                                |
| <span data-ttu-id="07a14-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="07a14-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a14-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="07a14-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="07a14-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a14-149">Range-Lower</span></span>            | <span data-ttu-id="07a14-150">1</span><span class="sxs-lookup"><span data-stu-id="07a14-150">1</span></span>                                                    |
| <span data-ttu-id="07a14-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a14-151">Range-Upper</span></span>            | <span data-ttu-id="07a14-152">1024</span><span class="sxs-lookup"><span data-stu-id="07a14-152">1024</span></span>                                                 |
| <span data-ttu-id="07a14-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-153">Search-Flags</span></span>           | <span data-ttu-id="07a14-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a14-154">0x00000000</span></span>                                           |
| <span data-ttu-id="07a14-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-155">System-Flags</span></span>           | <span data-ttu-id="07a14-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a14-156">0x00000010</span></span>                                           |
| <span data-ttu-id="07a14-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="07a14-157">Classes used in</span></span>        | [<span data-ttu-id="07a14-158">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="07a14-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="07a14-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07a14-159">Windows Server 2003</span></span>



| <span data-ttu-id="07a14-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-160">Entry</span></span> | <span data-ttu-id="07a14-161">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="07a14-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="07a14-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="07a14-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-163">MAPI-Id</span></span>                | <span data-ttu-id="07a14-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="07a14-164">0x3004</span></span>                                               |
| <span data-ttu-id="07a14-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a14-165">System-Only</span></span>            | <span data-ttu-id="07a14-166">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-166">False</span></span>                                                |
| <span data-ttu-id="07a14-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="07a14-167">Is-Single-Valued</span></span>       | <span data-ttu-id="07a14-168">True</span><span class="sxs-lookup"><span data-stu-id="07a14-168">True</span></span>                                                 |
| <span data-ttu-id="07a14-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="07a14-169">Is Indexed</span></span>             | <span data-ttu-id="07a14-170">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-170">False</span></span>                                                |
| <span data-ttu-id="07a14-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="07a14-171">In Global Catalog</span></span>      | <span data-ttu-id="07a14-172">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-172">False</span></span>                                                |
| <span data-ttu-id="07a14-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="07a14-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a14-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="07a14-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="07a14-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a14-175">Range-Lower</span></span>            | <span data-ttu-id="07a14-176">1</span><span class="sxs-lookup"><span data-stu-id="07a14-176">1</span></span>                                                    |
| <span data-ttu-id="07a14-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a14-177">Range-Upper</span></span>            | <span data-ttu-id="07a14-178">1024</span><span class="sxs-lookup"><span data-stu-id="07a14-178">1024</span></span>                                                 |
| <span data-ttu-id="07a14-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-179">Search-Flags</span></span>           | <span data-ttu-id="07a14-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a14-180">0x00000000</span></span>                                           |
| <span data-ttu-id="07a14-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-181">System-Flags</span></span>           | <span data-ttu-id="07a14-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a14-182">0x00000010</span></span>                                           |
| <span data-ttu-id="07a14-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="07a14-183">Classes used in</span></span>        | [<span data-ttu-id="07a14-184">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="07a14-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="07a14-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="07a14-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="07a14-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-186">Entry</span></span> | <span data-ttu-id="07a14-187">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="07a14-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="07a14-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="07a14-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-189">MAPI-Id</span></span>                | <span data-ttu-id="07a14-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="07a14-190">0x3004</span></span>                                               |
| <span data-ttu-id="07a14-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a14-191">System-Only</span></span>            | <span data-ttu-id="07a14-192">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-192">False</span></span>                                                |
| <span data-ttu-id="07a14-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="07a14-193">Is-Single-Valued</span></span>       | <span data-ttu-id="07a14-194">True</span><span class="sxs-lookup"><span data-stu-id="07a14-194">True</span></span>                                                 |
| <span data-ttu-id="07a14-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="07a14-195">Is Indexed</span></span>             | <span data-ttu-id="07a14-196">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-196">False</span></span>                                                |
| <span data-ttu-id="07a14-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="07a14-197">In Global Catalog</span></span>      | <span data-ttu-id="07a14-198">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-198">False</span></span>                                                |
| <span data-ttu-id="07a14-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="07a14-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a14-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="07a14-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="07a14-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a14-201">Range-Lower</span></span>            | <span data-ttu-id="07a14-202">1</span><span class="sxs-lookup"><span data-stu-id="07a14-202">1</span></span>                                                    |
| <span data-ttu-id="07a14-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a14-203">Range-Upper</span></span>            | <span data-ttu-id="07a14-204">1024</span><span class="sxs-lookup"><span data-stu-id="07a14-204">1024</span></span>                                                 |
| <span data-ttu-id="07a14-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-205">Search-Flags</span></span>           | <span data-ttu-id="07a14-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a14-206">0x00000000</span></span>                                           |
| <span data-ttu-id="07a14-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-207">System-Flags</span></span>           | <span data-ttu-id="07a14-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a14-208">0x00000010</span></span>                                           |
| <span data-ttu-id="07a14-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="07a14-209">Classes used in</span></span>        | [<span data-ttu-id="07a14-210">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="07a14-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="07a14-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a14-211">Windows Server 2008</span></span>



| <span data-ttu-id="07a14-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-212">Entry</span></span> | <span data-ttu-id="07a14-213">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="07a14-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="07a14-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="07a14-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-215">MAPI-Id</span></span>                | <span data-ttu-id="07a14-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="07a14-216">0x3004</span></span>                                               |
| <span data-ttu-id="07a14-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a14-217">System-Only</span></span>            | <span data-ttu-id="07a14-218">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-218">False</span></span>                                                |
| <span data-ttu-id="07a14-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="07a14-219">Is-Single-Valued</span></span>       | <span data-ttu-id="07a14-220">True</span><span class="sxs-lookup"><span data-stu-id="07a14-220">True</span></span>                                                 |
| <span data-ttu-id="07a14-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="07a14-221">Is Indexed</span></span>             | <span data-ttu-id="07a14-222">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-222">False</span></span>                                                |
| <span data-ttu-id="07a14-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="07a14-223">In Global Catalog</span></span>      | <span data-ttu-id="07a14-224">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-224">False</span></span>                                                |
| <span data-ttu-id="07a14-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="07a14-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a14-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="07a14-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="07a14-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a14-227">Range-Lower</span></span>            | <span data-ttu-id="07a14-228">1</span><span class="sxs-lookup"><span data-stu-id="07a14-228">1</span></span>                                                    |
| <span data-ttu-id="07a14-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a14-229">Range-Upper</span></span>            | <span data-ttu-id="07a14-230">1024</span><span class="sxs-lookup"><span data-stu-id="07a14-230">1024</span></span>                                                 |
| <span data-ttu-id="07a14-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-231">Search-Flags</span></span>           | <span data-ttu-id="07a14-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a14-232">0x00000000</span></span>                                           |
| <span data-ttu-id="07a14-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-233">System-Flags</span></span>           | <span data-ttu-id="07a14-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a14-234">0x00000010</span></span>                                           |
| <span data-ttu-id="07a14-235">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="07a14-235">Classes used in</span></span>        | [<span data-ttu-id="07a14-236">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="07a14-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="07a14-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07a14-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="07a14-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-238">Entry</span></span> | <span data-ttu-id="07a14-239">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="07a14-240">ID do link</span><span class="sxs-lookup"><span data-stu-id="07a14-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="07a14-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-241">MAPI-Id</span></span>                | <span data-ttu-id="07a14-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="07a14-242">0x3004</span></span>                                               |
| <span data-ttu-id="07a14-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a14-243">System-Only</span></span>            | <span data-ttu-id="07a14-244">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-244">False</span></span>                                                |
| <span data-ttu-id="07a14-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="07a14-245">Is-Single-Valued</span></span>       | <span data-ttu-id="07a14-246">True</span><span class="sxs-lookup"><span data-stu-id="07a14-246">True</span></span>                                                 |
| <span data-ttu-id="07a14-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="07a14-247">Is Indexed</span></span>             | <span data-ttu-id="07a14-248">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-248">False</span></span>                                                |
| <span data-ttu-id="07a14-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="07a14-249">In Global Catalog</span></span>      | <span data-ttu-id="07a14-250">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-250">False</span></span>                                                |
| <span data-ttu-id="07a14-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="07a14-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a14-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="07a14-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="07a14-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a14-253">Range-Lower</span></span>            | <span data-ttu-id="07a14-254">1</span><span class="sxs-lookup"><span data-stu-id="07a14-254">1</span></span>                                                    |
| <span data-ttu-id="07a14-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a14-255">Range-Upper</span></span>            | <span data-ttu-id="07a14-256">1024</span><span class="sxs-lookup"><span data-stu-id="07a14-256">1024</span></span>                                                 |
| <span data-ttu-id="07a14-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-257">Search-Flags</span></span>           | <span data-ttu-id="07a14-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a14-258">0x00000000</span></span>                                           |
| <span data-ttu-id="07a14-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-259">System-Flags</span></span>           | <span data-ttu-id="07a14-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a14-260">0x00000010</span></span>                                           |
| <span data-ttu-id="07a14-261">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="07a14-261">Classes used in</span></span>        | [<span data-ttu-id="07a14-262">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="07a14-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="07a14-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07a14-263">Windows Server 2012</span></span>



| <span data-ttu-id="07a14-264">Entrada</span><span class="sxs-lookup"><span data-stu-id="07a14-264">Entry</span></span> | <span data-ttu-id="07a14-265">Valor</span><span class="sxs-lookup"><span data-stu-id="07a14-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="07a14-266">ID do link</span><span class="sxs-lookup"><span data-stu-id="07a14-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="07a14-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07a14-267">MAPI-Id</span></span>                | <span data-ttu-id="07a14-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="07a14-268">0x3004</span></span>                                               |
| <span data-ttu-id="07a14-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="07a14-269">System-Only</span></span>            | <span data-ttu-id="07a14-270">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-270">False</span></span>                                                |
| <span data-ttu-id="07a14-271">É de valor único</span><span class="sxs-lookup"><span data-stu-id="07a14-271">Is-Single-Valued</span></span>       | <span data-ttu-id="07a14-272">True</span><span class="sxs-lookup"><span data-stu-id="07a14-272">True</span></span>                                                 |
| <span data-ttu-id="07a14-273">É indexado</span><span class="sxs-lookup"><span data-stu-id="07a14-273">Is Indexed</span></span>             | <span data-ttu-id="07a14-274">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-274">False</span></span>                                                |
| <span data-ttu-id="07a14-275">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="07a14-275">In Global Catalog</span></span>      | <span data-ttu-id="07a14-276">Falso</span><span class="sxs-lookup"><span data-stu-id="07a14-276">False</span></span>                                                |
| <span data-ttu-id="07a14-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="07a14-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="07a14-278">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="07a14-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="07a14-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07a14-279">Range-Lower</span></span>            | <span data-ttu-id="07a14-280">1</span><span class="sxs-lookup"><span data-stu-id="07a14-280">1</span></span>                                                    |
| <span data-ttu-id="07a14-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07a14-281">Range-Upper</span></span>            | <span data-ttu-id="07a14-282">1024</span><span class="sxs-lookup"><span data-stu-id="07a14-282">1024</span></span>                                                 |
| <span data-ttu-id="07a14-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-283">Search-Flags</span></span>           | <span data-ttu-id="07a14-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07a14-284">0x00000000</span></span>                                           |
| <span data-ttu-id="07a14-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07a14-285">System-Flags</span></span>           | <span data-ttu-id="07a14-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="07a14-286">0x00000010</span></span>                                           |
| <span data-ttu-id="07a14-287">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="07a14-287">Classes used in</span></span>        | [<span data-ttu-id="07a14-288">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="07a14-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





