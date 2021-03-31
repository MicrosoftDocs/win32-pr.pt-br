---
title: Unicode-Pwd atributo
description: A senha do usuário no formato One-Way do Windows NT (OWF). O Windows 2000 usa o Windows NT OWF. Essa propriedade é usada somente pelo sistema operacional. Observe que você não pode derivar a senha de limpeza do formulário OWF da senha.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Esquema de Unicode-Pwd do atributo AD
- Esquema de AD do atributo unicodePwd
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086980"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="0c698-108">Unicode-Pwd atributo</span><span class="sxs-lookup"><span data-stu-id="0c698-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="0c698-109">A senha do usuário no formato One-Way do Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="0c698-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="0c698-110">O Windows 2000 usa o Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="0c698-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="0c698-111">Essa propriedade é usada somente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0c698-111">This property is used only by the operating system.</span></span> <span data-ttu-id="0c698-112">Observe que você não pode derivar a senha de limpeza do formulário OWF da senha.</span><span class="sxs-lookup"><span data-stu-id="0c698-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="0c698-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-113">Entry</span></span> | <span data-ttu-id="0c698-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0c698-115">CN</span><span class="sxs-lookup"><span data-stu-id="0c698-115">CN</span></span>                | <span data-ttu-id="0c698-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="0c698-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="0c698-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c698-117">Ldap-Display-Name</span></span> | <span data-ttu-id="0c698-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="0c698-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="0c698-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0c698-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="0c698-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0c698-120">Update Privilege</span></span>  | <span data-ttu-id="0c698-121">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="0c698-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="0c698-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0c698-122">Update Frequency</span></span>  | <span data-ttu-id="0c698-123">Quando o registro do usuário é criado e sempre que a senha precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="0c698-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="0c698-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-124">Attribute-Id</span></span>      | <span data-ttu-id="0c698-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="0c698-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="0c698-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c698-126">System-Id-Guid</span></span>    | <span data-ttu-id="0c698-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="0c698-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="0c698-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c698-128">Syntax</span></span>            | [<span data-ttu-id="0c698-129">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="0c698-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="0c698-130">Implementações</span><span class="sxs-lookup"><span data-stu-id="0c698-130">Implementations</span></span>

-   [<span data-ttu-id="0c698-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c698-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c698-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c698-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c698-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0c698-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0c698-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c698-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c698-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c698-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c698-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c698-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c698-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c698-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c698-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c698-138">Windows 2000 Server</span></span>



| <span data-ttu-id="0c698-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-139">Entry</span></span> | <span data-ttu-id="0c698-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c698-141">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-143">System-Only</span></span>            | <span data-ttu-id="0c698-144">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-144">False</span></span>                             |
| <span data-ttu-id="0c698-145">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-145">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-146">True</span><span class="sxs-lookup"><span data-stu-id="0c698-146">True</span></span>                              |
| <span data-ttu-id="0c698-147">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-147">Is Indexed</span></span>             | <span data-ttu-id="0c698-148">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-148">False</span></span>                             |
| <span data-ttu-id="0c698-149">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-149">In Global Catalog</span></span>      | <span data-ttu-id="0c698-150">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-150">False</span></span>                             |
| <span data-ttu-id="0c698-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-152">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c698-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c698-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c698-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-155">Search-Flags</span></span>           | <span data-ttu-id="0c698-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-156">0x00000000</span></span>                        |
| <span data-ttu-id="0c698-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-157">System-Flags</span></span>           | <span data-ttu-id="0c698-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-158">0x00000010</span></span>                        |
| <span data-ttu-id="0c698-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-159">Classes used in</span></span>        | [<span data-ttu-id="0c698-160">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="0c698-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c698-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c698-161">Windows Server 2003</span></span>



| <span data-ttu-id="0c698-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-162">Entry</span></span> | <span data-ttu-id="0c698-163">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c698-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-166">System-Only</span></span>            | <span data-ttu-id="0c698-167">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-167">False</span></span>                             |
| <span data-ttu-id="0c698-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-168">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-169">True</span><span class="sxs-lookup"><span data-stu-id="0c698-169">True</span></span>                              |
| <span data-ttu-id="0c698-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-170">Is Indexed</span></span>             | <span data-ttu-id="0c698-171">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-171">False</span></span>                             |
| <span data-ttu-id="0c698-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-172">In Global Catalog</span></span>      | <span data-ttu-id="0c698-173">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-173">False</span></span>                             |
| <span data-ttu-id="0c698-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c698-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c698-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c698-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-178">Search-Flags</span></span>           | <span data-ttu-id="0c698-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-179">0x00000000</span></span>                        |
| <span data-ttu-id="0c698-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-180">System-Flags</span></span>           | <span data-ttu-id="0c698-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-181">0x00000010</span></span>                        |
| <span data-ttu-id="0c698-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-182">Classes used in</span></span>        | [<span data-ttu-id="0c698-183">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="0c698-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0c698-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="0c698-184">ADAM</span></span>



| <span data-ttu-id="0c698-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-185">Entry</span></span> | <span data-ttu-id="0c698-186">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="0c698-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="0c698-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="0c698-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-189">System-Only</span></span>            | <span data-ttu-id="0c698-190">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-190">False</span></span>                                                             |
| <span data-ttu-id="0c698-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-191">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-192">True</span><span class="sxs-lookup"><span data-stu-id="0c698-192">True</span></span>                                                              |
| <span data-ttu-id="0c698-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-193">Is Indexed</span></span>             | <span data-ttu-id="0c698-194">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-194">False</span></span>                                                             |
| <span data-ttu-id="0c698-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-195">In Global Catalog</span></span>      | <span data-ttu-id="0c698-196">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-196">False</span></span>                                                             |
| <span data-ttu-id="0c698-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="0c698-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="0c698-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="0c698-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-201">Search-Flags</span></span>           | <span data-ttu-id="0c698-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="0c698-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-203">System-Flags</span></span>           | <span data-ttu-id="0c698-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="0c698-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-205">Classes used in</span></span>        | [<span data-ttu-id="0c698-206">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="0c698-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c698-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c698-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c698-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-208">Entry</span></span> | <span data-ttu-id="0c698-209">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c698-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-212">System-Only</span></span>            | <span data-ttu-id="0c698-213">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-213">False</span></span>                             |
| <span data-ttu-id="0c698-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-214">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-215">True</span><span class="sxs-lookup"><span data-stu-id="0c698-215">True</span></span>                              |
| <span data-ttu-id="0c698-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-216">Is Indexed</span></span>             | <span data-ttu-id="0c698-217">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-217">False</span></span>                             |
| <span data-ttu-id="0c698-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-218">In Global Catalog</span></span>      | <span data-ttu-id="0c698-219">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-219">False</span></span>                             |
| <span data-ttu-id="0c698-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c698-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c698-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c698-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-224">Search-Flags</span></span>           | <span data-ttu-id="0c698-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-225">0x00000000</span></span>                        |
| <span data-ttu-id="0c698-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-226">System-Flags</span></span>           | <span data-ttu-id="0c698-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-227">0x00000010</span></span>                        |
| <span data-ttu-id="0c698-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-228">Classes used in</span></span>        | [<span data-ttu-id="0c698-229">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="0c698-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c698-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c698-230">Windows Server 2008</span></span>



| <span data-ttu-id="0c698-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-231">Entry</span></span> | <span data-ttu-id="0c698-232">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c698-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-235">System-Only</span></span>            | <span data-ttu-id="0c698-236">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-236">False</span></span>                             |
| <span data-ttu-id="0c698-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-237">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-238">True</span><span class="sxs-lookup"><span data-stu-id="0c698-238">True</span></span>                              |
| <span data-ttu-id="0c698-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-239">Is Indexed</span></span>             | <span data-ttu-id="0c698-240">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-240">False</span></span>                             |
| <span data-ttu-id="0c698-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-241">In Global Catalog</span></span>      | <span data-ttu-id="0c698-242">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-242">False</span></span>                             |
| <span data-ttu-id="0c698-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c698-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c698-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c698-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-247">Search-Flags</span></span>           | <span data-ttu-id="0c698-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-248">0x00000000</span></span>                        |
| <span data-ttu-id="0c698-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-249">System-Flags</span></span>           | <span data-ttu-id="0c698-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-250">0x00000010</span></span>                        |
| <span data-ttu-id="0c698-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-251">Classes used in</span></span>        | [<span data-ttu-id="0c698-252">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="0c698-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c698-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c698-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c698-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-254">Entry</span></span> | <span data-ttu-id="0c698-255">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c698-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-258">System-Only</span></span>            | <span data-ttu-id="0c698-259">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-259">False</span></span>                             |
| <span data-ttu-id="0c698-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-260">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-261">True</span><span class="sxs-lookup"><span data-stu-id="0c698-261">True</span></span>                              |
| <span data-ttu-id="0c698-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-262">Is Indexed</span></span>             | <span data-ttu-id="0c698-263">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-263">False</span></span>                             |
| <span data-ttu-id="0c698-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-264">In Global Catalog</span></span>      | <span data-ttu-id="0c698-265">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-265">False</span></span>                             |
| <span data-ttu-id="0c698-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c698-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c698-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c698-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-270">Search-Flags</span></span>           | <span data-ttu-id="0c698-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-271">0x00000000</span></span>                        |
| <span data-ttu-id="0c698-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-272">System-Flags</span></span>           | <span data-ttu-id="0c698-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-273">0x00000010</span></span>                        |
| <span data-ttu-id="0c698-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-274">Classes used in</span></span>        | [<span data-ttu-id="0c698-275">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="0c698-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c698-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c698-276">Windows Server 2012</span></span>



| <span data-ttu-id="0c698-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c698-277">Entry</span></span> | <span data-ttu-id="0c698-278">Valor</span><span class="sxs-lookup"><span data-stu-id="0c698-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="0c698-279">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c698-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c698-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="0c698-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c698-281">System-Only</span></span>            | <span data-ttu-id="0c698-282">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-282">False</span></span>                             |
| <span data-ttu-id="0c698-283">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c698-283">Is-Single-Valued</span></span>       | <span data-ttu-id="0c698-284">True</span><span class="sxs-lookup"><span data-stu-id="0c698-284">True</span></span>                              |
| <span data-ttu-id="0c698-285">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c698-285">Is Indexed</span></span>             | <span data-ttu-id="0c698-286">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-286">False</span></span>                             |
| <span data-ttu-id="0c698-287">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c698-287">In Global Catalog</span></span>      | <span data-ttu-id="0c698-288">Falso</span><span class="sxs-lookup"><span data-stu-id="0c698-288">False</span></span>                             |
| <span data-ttu-id="0c698-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c698-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c698-290">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c698-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="0c698-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c698-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="0c698-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c698-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="0c698-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-293">Search-Flags</span></span>           | <span data-ttu-id="0c698-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c698-294">0x00000000</span></span>                        |
| <span data-ttu-id="0c698-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c698-295">System-Flags</span></span>           | <span data-ttu-id="0c698-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c698-296">0x00000010</span></span>                        |
| <span data-ttu-id="0c698-297">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c698-297">Classes used in</span></span>        | [<span data-ttu-id="0c698-298">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="0c698-298">**User**</span></span>](c-user.md)<br/> |



 

 





