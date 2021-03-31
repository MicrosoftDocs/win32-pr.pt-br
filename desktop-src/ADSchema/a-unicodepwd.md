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
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="d3e46-108">Unicode-Pwd atributo</span><span class="sxs-lookup"><span data-stu-id="d3e46-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="d3e46-109">A senha do usuário no formato One-Way do Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="d3e46-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="d3e46-110">O Windows 2000 usa o Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="d3e46-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="d3e46-111">Essa propriedade é usada somente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d3e46-111">This property is used only by the operating system.</span></span> <span data-ttu-id="d3e46-112">Observe que você não pode derivar a senha de limpeza do formulário OWF da senha.</span><span class="sxs-lookup"><span data-stu-id="d3e46-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="d3e46-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-113">Entry</span></span> | <span data-ttu-id="d3e46-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d3e46-115">CN</span><span class="sxs-lookup"><span data-stu-id="d3e46-115">CN</span></span>                | <span data-ttu-id="d3e46-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="d3e46-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="d3e46-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d3e46-117">Ldap-Display-Name</span></span> | <span data-ttu-id="d3e46-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="d3e46-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="d3e46-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d3e46-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="d3e46-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d3e46-120">Update Privilege</span></span>  | <span data-ttu-id="d3e46-121">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="d3e46-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="d3e46-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d3e46-122">Update Frequency</span></span>  | <span data-ttu-id="d3e46-123">Quando o registro do usuário é criado e sempre que a senha precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="d3e46-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="d3e46-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-124">Attribute-Id</span></span>      | <span data-ttu-id="d3e46-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="d3e46-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="d3e46-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d3e46-126">System-Id-Guid</span></span>    | <span data-ttu-id="d3e46-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d3e46-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="d3e46-128">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3e46-128">Syntax</span></span>            | [<span data-ttu-id="d3e46-129">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="d3e46-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="d3e46-130">Implementações</span><span class="sxs-lookup"><span data-stu-id="d3e46-130">Implementations</span></span>

-   [<span data-ttu-id="d3e46-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d3e46-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d3e46-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d3e46-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d3e46-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d3e46-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d3e46-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d3e46-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d3e46-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d3e46-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d3e46-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d3e46-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d3e46-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d3e46-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d3e46-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3e46-138">Windows 2000 Server</span></span>



| <span data-ttu-id="d3e46-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-139">Entry</span></span> | <span data-ttu-id="d3e46-140">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3e46-141">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-143">System-Only</span></span>            | <span data-ttu-id="d3e46-144">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-144">False</span></span>                             |
| <span data-ttu-id="d3e46-145">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-145">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-146">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-146">True</span></span>                              |
| <span data-ttu-id="d3e46-147">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-147">Is Indexed</span></span>             | <span data-ttu-id="d3e46-148">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-148">False</span></span>                             |
| <span data-ttu-id="d3e46-149">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-149">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-150">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-150">False</span></span>                             |
| <span data-ttu-id="d3e46-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-152">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3e46-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3e46-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3e46-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-155">Search-Flags</span></span>           | <span data-ttu-id="d3e46-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-156">0x00000000</span></span>                        |
| <span data-ttu-id="d3e46-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-157">System-Flags</span></span>           | <span data-ttu-id="d3e46-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-158">0x00000010</span></span>                        |
| <span data-ttu-id="d3e46-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-159">Classes used in</span></span>        | [<span data-ttu-id="d3e46-160">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d3e46-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d3e46-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3e46-161">Windows Server 2003</span></span>



| <span data-ttu-id="d3e46-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-162">Entry</span></span> | <span data-ttu-id="d3e46-163">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3e46-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-166">System-Only</span></span>            | <span data-ttu-id="d3e46-167">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-167">False</span></span>                             |
| <span data-ttu-id="d3e46-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-168">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-169">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-169">True</span></span>                              |
| <span data-ttu-id="d3e46-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-170">Is Indexed</span></span>             | <span data-ttu-id="d3e46-171">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-171">False</span></span>                             |
| <span data-ttu-id="d3e46-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-172">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-173">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-173">False</span></span>                             |
| <span data-ttu-id="d3e46-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3e46-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3e46-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3e46-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-178">Search-Flags</span></span>           | <span data-ttu-id="d3e46-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-179">0x00000000</span></span>                        |
| <span data-ttu-id="d3e46-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-180">System-Flags</span></span>           | <span data-ttu-id="d3e46-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-181">0x00000010</span></span>                        |
| <span data-ttu-id="d3e46-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-182">Classes used in</span></span>        | [<span data-ttu-id="d3e46-183">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d3e46-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d3e46-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="d3e46-184">ADAM</span></span>



| <span data-ttu-id="d3e46-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-185">Entry</span></span> | <span data-ttu-id="d3e46-186">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="d3e46-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="d3e46-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="d3e46-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-189">System-Only</span></span>            | <span data-ttu-id="d3e46-190">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-190">False</span></span>                                                             |
| <span data-ttu-id="d3e46-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-191">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-192">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-192">True</span></span>                                                              |
| <span data-ttu-id="d3e46-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-193">Is Indexed</span></span>             | <span data-ttu-id="d3e46-194">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-194">False</span></span>                                                             |
| <span data-ttu-id="d3e46-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-195">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-196">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-196">False</span></span>                                                             |
| <span data-ttu-id="d3e46-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="d3e46-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="d3e46-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="d3e46-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-201">Search-Flags</span></span>           | <span data-ttu-id="d3e46-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="d3e46-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-203">System-Flags</span></span>           | <span data-ttu-id="d3e46-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="d3e46-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-205">Classes used in</span></span>        | [<span data-ttu-id="d3e46-206">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="d3e46-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d3e46-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d3e46-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d3e46-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-208">Entry</span></span> | <span data-ttu-id="d3e46-209">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3e46-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-212">System-Only</span></span>            | <span data-ttu-id="d3e46-213">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-213">False</span></span>                             |
| <span data-ttu-id="d3e46-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-214">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-215">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-215">True</span></span>                              |
| <span data-ttu-id="d3e46-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-216">Is Indexed</span></span>             | <span data-ttu-id="d3e46-217">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-217">False</span></span>                             |
| <span data-ttu-id="d3e46-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-218">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-219">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-219">False</span></span>                             |
| <span data-ttu-id="d3e46-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3e46-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3e46-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3e46-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-224">Search-Flags</span></span>           | <span data-ttu-id="d3e46-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-225">0x00000000</span></span>                        |
| <span data-ttu-id="d3e46-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-226">System-Flags</span></span>           | <span data-ttu-id="d3e46-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-227">0x00000010</span></span>                        |
| <span data-ttu-id="d3e46-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-228">Classes used in</span></span>        | [<span data-ttu-id="d3e46-229">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d3e46-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d3e46-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3e46-230">Windows Server 2008</span></span>



| <span data-ttu-id="d3e46-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-231">Entry</span></span> | <span data-ttu-id="d3e46-232">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3e46-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-235">System-Only</span></span>            | <span data-ttu-id="d3e46-236">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-236">False</span></span>                             |
| <span data-ttu-id="d3e46-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-237">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-238">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-238">True</span></span>                              |
| <span data-ttu-id="d3e46-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-239">Is Indexed</span></span>             | <span data-ttu-id="d3e46-240">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-240">False</span></span>                             |
| <span data-ttu-id="d3e46-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-241">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-242">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-242">False</span></span>                             |
| <span data-ttu-id="d3e46-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3e46-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3e46-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3e46-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-247">Search-Flags</span></span>           | <span data-ttu-id="d3e46-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-248">0x00000000</span></span>                        |
| <span data-ttu-id="d3e46-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-249">System-Flags</span></span>           | <span data-ttu-id="d3e46-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-250">0x00000010</span></span>                        |
| <span data-ttu-id="d3e46-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-251">Classes used in</span></span>        | [<span data-ttu-id="d3e46-252">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d3e46-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d3e46-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3e46-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d3e46-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-254">Entry</span></span> | <span data-ttu-id="d3e46-255">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3e46-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-258">System-Only</span></span>            | <span data-ttu-id="d3e46-259">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-259">False</span></span>                             |
| <span data-ttu-id="d3e46-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-260">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-261">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-261">True</span></span>                              |
| <span data-ttu-id="d3e46-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-262">Is Indexed</span></span>             | <span data-ttu-id="d3e46-263">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-263">False</span></span>                             |
| <span data-ttu-id="d3e46-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-264">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-265">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-265">False</span></span>                             |
| <span data-ttu-id="d3e46-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3e46-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3e46-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3e46-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-270">Search-Flags</span></span>           | <span data-ttu-id="d3e46-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-271">0x00000000</span></span>                        |
| <span data-ttu-id="d3e46-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-272">System-Flags</span></span>           | <span data-ttu-id="d3e46-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-273">0x00000010</span></span>                        |
| <span data-ttu-id="d3e46-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-274">Classes used in</span></span>        | [<span data-ttu-id="d3e46-275">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d3e46-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d3e46-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3e46-276">Windows Server 2012</span></span>



| <span data-ttu-id="d3e46-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3e46-277">Entry</span></span> | <span data-ttu-id="d3e46-278">Valor</span><span class="sxs-lookup"><span data-stu-id="d3e46-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d3e46-279">ID do link</span><span class="sxs-lookup"><span data-stu-id="d3e46-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d3e46-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d3e46-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="d3e46-281">System-Only</span></span>            | <span data-ttu-id="d3e46-282">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-282">False</span></span>                             |
| <span data-ttu-id="d3e46-283">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d3e46-283">Is-Single-Valued</span></span>       | <span data-ttu-id="d3e46-284">True</span><span class="sxs-lookup"><span data-stu-id="d3e46-284">True</span></span>                              |
| <span data-ttu-id="d3e46-285">É indexado</span><span class="sxs-lookup"><span data-stu-id="d3e46-285">Is Indexed</span></span>             | <span data-ttu-id="d3e46-286">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-286">False</span></span>                             |
| <span data-ttu-id="d3e46-287">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d3e46-287">In Global Catalog</span></span>      | <span data-ttu-id="d3e46-288">Falso</span><span class="sxs-lookup"><span data-stu-id="d3e46-288">False</span></span>                             |
| <span data-ttu-id="d3e46-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d3e46-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="d3e46-290">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d3e46-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d3e46-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d3e46-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d3e46-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d3e46-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d3e46-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-293">Search-Flags</span></span>           | <span data-ttu-id="d3e46-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d3e46-294">0x00000000</span></span>                        |
| <span data-ttu-id="d3e46-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d3e46-295">System-Flags</span></span>           | <span data-ttu-id="d3e46-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d3e46-296">0x00000010</span></span>                        |
| <span data-ttu-id="d3e46-297">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d3e46-297">Classes used in</span></span>        | [<span data-ttu-id="d3e46-298">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d3e46-298">**User**</span></span>](c-user.md)<br/> |



 

 





