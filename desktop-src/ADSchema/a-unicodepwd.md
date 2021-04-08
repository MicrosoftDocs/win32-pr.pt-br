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
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="615b0-108">Unicode-Pwd atributo</span><span class="sxs-lookup"><span data-stu-id="615b0-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="615b0-109">A senha do usuário no formato One-Way do Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="615b0-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="615b0-110">O Windows 2000 usa o Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="615b0-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="615b0-111">Essa propriedade é usada somente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="615b0-111">This property is used only by the operating system.</span></span> <span data-ttu-id="615b0-112">Observe que você não pode derivar a senha de limpeza do formulário OWF da senha.</span><span class="sxs-lookup"><span data-stu-id="615b0-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="615b0-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-113">Entry</span></span> | <span data-ttu-id="615b0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="615b0-115">CN</span><span class="sxs-lookup"><span data-stu-id="615b0-115">CN</span></span>                | <span data-ttu-id="615b0-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="615b0-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="615b0-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="615b0-117">Ldap-Display-Name</span></span> | <span data-ttu-id="615b0-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="615b0-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="615b0-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="615b0-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="615b0-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="615b0-120">Update Privilege</span></span>  | <span data-ttu-id="615b0-121">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="615b0-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="615b0-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="615b0-122">Update Frequency</span></span>  | <span data-ttu-id="615b0-123">Quando o registro do usuário é criado e sempre que a senha precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="615b0-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="615b0-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-124">Attribute-Id</span></span>      | <span data-ttu-id="615b0-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="615b0-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="615b0-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="615b0-126">System-Id-Guid</span></span>    | <span data-ttu-id="615b0-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="615b0-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="615b0-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="615b0-128">Syntax</span></span>            | [<span data-ttu-id="615b0-129">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="615b0-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="615b0-130">Implementações</span><span class="sxs-lookup"><span data-stu-id="615b0-130">Implementations</span></span>

-   [<span data-ttu-id="615b0-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="615b0-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="615b0-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="615b0-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="615b0-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="615b0-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="615b0-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="615b0-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="615b0-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="615b0-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="615b0-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="615b0-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="615b0-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="615b0-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="615b0-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="615b0-138">Windows 2000 Server</span></span>



| <span data-ttu-id="615b0-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-139">Entry</span></span> | <span data-ttu-id="615b0-140">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="615b0-141">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-143">System-Only</span></span>            | <span data-ttu-id="615b0-144">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-144">False</span></span>                             |
| <span data-ttu-id="615b0-145">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-145">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-146">True</span><span class="sxs-lookup"><span data-stu-id="615b0-146">True</span></span>                              |
| <span data-ttu-id="615b0-147">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-147">Is Indexed</span></span>             | <span data-ttu-id="615b0-148">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-148">False</span></span>                             |
| <span data-ttu-id="615b0-149">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-149">In Global Catalog</span></span>      | <span data-ttu-id="615b0-150">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-150">False</span></span>                             |
| <span data-ttu-id="615b0-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-152">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="615b0-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="615b0-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="615b0-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-155">Search-Flags</span></span>           | <span data-ttu-id="615b0-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-156">0x00000000</span></span>                        |
| <span data-ttu-id="615b0-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-157">System-Flags</span></span>           | <span data-ttu-id="615b0-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-158">0x00000010</span></span>                        |
| <span data-ttu-id="615b0-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-159">Classes used in</span></span>        | [<span data-ttu-id="615b0-160">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="615b0-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="615b0-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="615b0-161">Windows Server 2003</span></span>



| <span data-ttu-id="615b0-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-162">Entry</span></span> | <span data-ttu-id="615b0-163">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="615b0-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-166">System-Only</span></span>            | <span data-ttu-id="615b0-167">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-167">False</span></span>                             |
| <span data-ttu-id="615b0-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-168">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-169">True</span><span class="sxs-lookup"><span data-stu-id="615b0-169">True</span></span>                              |
| <span data-ttu-id="615b0-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-170">Is Indexed</span></span>             | <span data-ttu-id="615b0-171">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-171">False</span></span>                             |
| <span data-ttu-id="615b0-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-172">In Global Catalog</span></span>      | <span data-ttu-id="615b0-173">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-173">False</span></span>                             |
| <span data-ttu-id="615b0-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="615b0-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="615b0-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="615b0-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-178">Search-Flags</span></span>           | <span data-ttu-id="615b0-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-179">0x00000000</span></span>                        |
| <span data-ttu-id="615b0-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-180">System-Flags</span></span>           | <span data-ttu-id="615b0-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-181">0x00000010</span></span>                        |
| <span data-ttu-id="615b0-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-182">Classes used in</span></span>        | [<span data-ttu-id="615b0-183">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="615b0-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="615b0-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="615b0-184">ADAM</span></span>



| <span data-ttu-id="615b0-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-185">Entry</span></span> | <span data-ttu-id="615b0-186">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="615b0-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="615b0-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="615b0-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-189">System-Only</span></span>            | <span data-ttu-id="615b0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-190">False</span></span>                                                             |
| <span data-ttu-id="615b0-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-191">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-192">True</span><span class="sxs-lookup"><span data-stu-id="615b0-192">True</span></span>                                                              |
| <span data-ttu-id="615b0-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-193">Is Indexed</span></span>             | <span data-ttu-id="615b0-194">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-194">False</span></span>                                                             |
| <span data-ttu-id="615b0-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-195">In Global Catalog</span></span>      | <span data-ttu-id="615b0-196">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-196">False</span></span>                                                             |
| <span data-ttu-id="615b0-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="615b0-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="615b0-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="615b0-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-201">Search-Flags</span></span>           | <span data-ttu-id="615b0-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="615b0-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-203">System-Flags</span></span>           | <span data-ttu-id="615b0-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="615b0-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-205">Classes used in</span></span>        | [<span data-ttu-id="615b0-206">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="615b0-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="615b0-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="615b0-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="615b0-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-208">Entry</span></span> | <span data-ttu-id="615b0-209">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="615b0-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-212">System-Only</span></span>            | <span data-ttu-id="615b0-213">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-213">False</span></span>                             |
| <span data-ttu-id="615b0-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-214">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-215">True</span><span class="sxs-lookup"><span data-stu-id="615b0-215">True</span></span>                              |
| <span data-ttu-id="615b0-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-216">Is Indexed</span></span>             | <span data-ttu-id="615b0-217">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-217">False</span></span>                             |
| <span data-ttu-id="615b0-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-218">In Global Catalog</span></span>      | <span data-ttu-id="615b0-219">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-219">False</span></span>                             |
| <span data-ttu-id="615b0-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="615b0-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="615b0-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="615b0-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-224">Search-Flags</span></span>           | <span data-ttu-id="615b0-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-225">0x00000000</span></span>                        |
| <span data-ttu-id="615b0-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-226">System-Flags</span></span>           | <span data-ttu-id="615b0-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-227">0x00000010</span></span>                        |
| <span data-ttu-id="615b0-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-228">Classes used in</span></span>        | [<span data-ttu-id="615b0-229">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="615b0-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="615b0-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="615b0-230">Windows Server 2008</span></span>



| <span data-ttu-id="615b0-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-231">Entry</span></span> | <span data-ttu-id="615b0-232">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="615b0-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-235">System-Only</span></span>            | <span data-ttu-id="615b0-236">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-236">False</span></span>                             |
| <span data-ttu-id="615b0-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-237">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-238">True</span><span class="sxs-lookup"><span data-stu-id="615b0-238">True</span></span>                              |
| <span data-ttu-id="615b0-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-239">Is Indexed</span></span>             | <span data-ttu-id="615b0-240">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-240">False</span></span>                             |
| <span data-ttu-id="615b0-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-241">In Global Catalog</span></span>      | <span data-ttu-id="615b0-242">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-242">False</span></span>                             |
| <span data-ttu-id="615b0-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="615b0-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="615b0-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="615b0-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-247">Search-Flags</span></span>           | <span data-ttu-id="615b0-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-248">0x00000000</span></span>                        |
| <span data-ttu-id="615b0-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-249">System-Flags</span></span>           | <span data-ttu-id="615b0-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-250">0x00000010</span></span>                        |
| <span data-ttu-id="615b0-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-251">Classes used in</span></span>        | [<span data-ttu-id="615b0-252">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="615b0-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="615b0-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="615b0-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="615b0-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-254">Entry</span></span> | <span data-ttu-id="615b0-255">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="615b0-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-258">System-Only</span></span>            | <span data-ttu-id="615b0-259">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-259">False</span></span>                             |
| <span data-ttu-id="615b0-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-260">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-261">True</span><span class="sxs-lookup"><span data-stu-id="615b0-261">True</span></span>                              |
| <span data-ttu-id="615b0-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-262">Is Indexed</span></span>             | <span data-ttu-id="615b0-263">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-263">False</span></span>                             |
| <span data-ttu-id="615b0-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-264">In Global Catalog</span></span>      | <span data-ttu-id="615b0-265">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-265">False</span></span>                             |
| <span data-ttu-id="615b0-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="615b0-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="615b0-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="615b0-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-270">Search-Flags</span></span>           | <span data-ttu-id="615b0-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-271">0x00000000</span></span>                        |
| <span data-ttu-id="615b0-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-272">System-Flags</span></span>           | <span data-ttu-id="615b0-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-273">0x00000010</span></span>                        |
| <span data-ttu-id="615b0-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-274">Classes used in</span></span>        | [<span data-ttu-id="615b0-275">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="615b0-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="615b0-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="615b0-276">Windows Server 2012</span></span>



| <span data-ttu-id="615b0-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="615b0-277">Entry</span></span> | <span data-ttu-id="615b0-278">Valor</span><span class="sxs-lookup"><span data-stu-id="615b0-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="615b0-279">ID do link</span><span class="sxs-lookup"><span data-stu-id="615b0-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="615b0-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="615b0-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="615b0-281">System-Only</span></span>            | <span data-ttu-id="615b0-282">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-282">False</span></span>                             |
| <span data-ttu-id="615b0-283">É de valor único</span><span class="sxs-lookup"><span data-stu-id="615b0-283">Is-Single-Valued</span></span>       | <span data-ttu-id="615b0-284">True</span><span class="sxs-lookup"><span data-stu-id="615b0-284">True</span></span>                              |
| <span data-ttu-id="615b0-285">É indexado</span><span class="sxs-lookup"><span data-stu-id="615b0-285">Is Indexed</span></span>             | <span data-ttu-id="615b0-286">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-286">False</span></span>                             |
| <span data-ttu-id="615b0-287">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="615b0-287">In Global Catalog</span></span>      | <span data-ttu-id="615b0-288">Falso</span><span class="sxs-lookup"><span data-stu-id="615b0-288">False</span></span>                             |
| <span data-ttu-id="615b0-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="615b0-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="615b0-290">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="615b0-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="615b0-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="615b0-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="615b0-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="615b0-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="615b0-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-293">Search-Flags</span></span>           | <span data-ttu-id="615b0-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="615b0-294">0x00000000</span></span>                        |
| <span data-ttu-id="615b0-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="615b0-295">System-Flags</span></span>           | <span data-ttu-id="615b0-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="615b0-296">0x00000010</span></span>                        |
| <span data-ttu-id="615b0-297">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="615b0-297">Classes used in</span></span>        | [<span data-ttu-id="615b0-298">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="615b0-298">**User**</span></span>](c-user.md)<br/> |



 

 





