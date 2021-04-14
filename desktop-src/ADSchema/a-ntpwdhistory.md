---
title: Atributo NT-pwd-History
description: O histórico de senha do usuário no formato One-Way do Windows NT (OWF). O Windows 2000 usa o Windows NT OWF.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo NT-pwd-History
- Esquema de AD do atributo ntPwdHistory
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500052"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="17a8b-106">Atributo NT-pwd-History</span><span class="sxs-lookup"><span data-stu-id="17a8b-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="17a8b-107">O histórico de senha do usuário no formato One-Way do Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="17a8b-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="17a8b-108">O Windows 2000 usa o Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="17a8b-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="17a8b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-109">Entry</span></span> | <span data-ttu-id="17a8b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="17a8b-111">CN</span><span class="sxs-lookup"><span data-stu-id="17a8b-111">CN</span></span>                | <span data-ttu-id="17a8b-112">NT-pwd-History</span><span class="sxs-lookup"><span data-stu-id="17a8b-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="17a8b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="17a8b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="17a8b-114">ntPwdHistory</span><span class="sxs-lookup"><span data-stu-id="17a8b-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="17a8b-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="17a8b-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="17a8b-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="17a8b-116">Update Privilege</span></span>  | <span data-ttu-id="17a8b-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="17a8b-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="17a8b-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="17a8b-118">Update Frequency</span></span>  | <span data-ttu-id="17a8b-119">Cada vez que o usuário altera as senhas.</span><span class="sxs-lookup"><span data-stu-id="17a8b-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="17a8b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-120">Attribute-Id</span></span>      | <span data-ttu-id="17a8b-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="17a8b-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="17a8b-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="17a8b-122">System-Id-Guid</span></span>    | <span data-ttu-id="17a8b-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="17a8b-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="17a8b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a8b-124">Syntax</span></span>            | [<span data-ttu-id="17a8b-125">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="17a8b-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="17a8b-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="17a8b-126">Implementations</span></span>

-   [<span data-ttu-id="17a8b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="17a8b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="17a8b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17a8b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17a8b-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="17a8b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="17a8b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17a8b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17a8b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17a8b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17a8b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17a8b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17a8b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17a8b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="17a8b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17a8b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="17a8b-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-135">Entry</span></span> | <span data-ttu-id="17a8b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17a8b-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-139">System-Only</span></span>            | <span data-ttu-id="17a8b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-140">False</span></span>                             |
| <span data-ttu-id="17a8b-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-142">False</span></span>                             |
| <span data-ttu-id="17a8b-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-143">Is Indexed</span></span>             | <span data-ttu-id="17a8b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-144">False</span></span>                             |
| <span data-ttu-id="17a8b-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-145">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-146">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-146">False</span></span>                             |
| <span data-ttu-id="17a8b-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17a8b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17a8b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17a8b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-151">Search-Flags</span></span>           | <span data-ttu-id="17a8b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-152">0x00000000</span></span>                        |
| <span data-ttu-id="17a8b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-153">System-Flags</span></span>           | <span data-ttu-id="17a8b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-154">0x00000010</span></span>                        |
| <span data-ttu-id="17a8b-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-155">Classes used in</span></span>        | [<span data-ttu-id="17a8b-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="17a8b-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="17a8b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17a8b-157">Windows Server 2003</span></span>



| <span data-ttu-id="17a8b-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-158">Entry</span></span> | <span data-ttu-id="17a8b-159">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17a8b-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-162">System-Only</span></span>            | <span data-ttu-id="17a8b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-163">False</span></span>                             |
| <span data-ttu-id="17a8b-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-165">False</span></span>                             |
| <span data-ttu-id="17a8b-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-166">Is Indexed</span></span>             | <span data-ttu-id="17a8b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-167">False</span></span>                             |
| <span data-ttu-id="17a8b-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-168">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-169">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-169">False</span></span>                             |
| <span data-ttu-id="17a8b-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17a8b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17a8b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17a8b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-174">Search-Flags</span></span>           | <span data-ttu-id="17a8b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-175">0x00000000</span></span>                        |
| <span data-ttu-id="17a8b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-176">System-Flags</span></span>           | <span data-ttu-id="17a8b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-177">0x00000010</span></span>                        |
| <span data-ttu-id="17a8b-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-178">Classes used in</span></span>        | [<span data-ttu-id="17a8b-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="17a8b-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="17a8b-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="17a8b-180">ADAM</span></span>



| <span data-ttu-id="17a8b-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-181">Entry</span></span> | <span data-ttu-id="17a8b-182">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="17a8b-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="17a8b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="17a8b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-185">System-Only</span></span>            | <span data-ttu-id="17a8b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-186">False</span></span>                                                             |
| <span data-ttu-id="17a8b-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-188">False</span></span>                                                             |
| <span data-ttu-id="17a8b-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-189">Is Indexed</span></span>             | <span data-ttu-id="17a8b-190">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-190">False</span></span>                                                             |
| <span data-ttu-id="17a8b-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-191">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-192">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-192">False</span></span>                                                             |
| <span data-ttu-id="17a8b-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="17a8b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="17a8b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="17a8b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-197">Search-Flags</span></span>           | <span data-ttu-id="17a8b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="17a8b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-199">System-Flags</span></span>           | <span data-ttu-id="17a8b-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="17a8b-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-201">Classes used in</span></span>        | [<span data-ttu-id="17a8b-202">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="17a8b-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17a8b-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17a8b-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17a8b-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-204">Entry</span></span> | <span data-ttu-id="17a8b-205">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17a8b-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-208">System-Only</span></span>            | <span data-ttu-id="17a8b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-209">False</span></span>                             |
| <span data-ttu-id="17a8b-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-210">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-211">False</span></span>                             |
| <span data-ttu-id="17a8b-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-212">Is Indexed</span></span>             | <span data-ttu-id="17a8b-213">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-213">False</span></span>                             |
| <span data-ttu-id="17a8b-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-214">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-215">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-215">False</span></span>                             |
| <span data-ttu-id="17a8b-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17a8b-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17a8b-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17a8b-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-220">Search-Flags</span></span>           | <span data-ttu-id="17a8b-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-221">0x00000000</span></span>                        |
| <span data-ttu-id="17a8b-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-222">System-Flags</span></span>           | <span data-ttu-id="17a8b-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-223">0x00000010</span></span>                        |
| <span data-ttu-id="17a8b-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-224">Classes used in</span></span>        | [<span data-ttu-id="17a8b-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="17a8b-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17a8b-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17a8b-226">Windows Server 2008</span></span>



| <span data-ttu-id="17a8b-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-227">Entry</span></span> | <span data-ttu-id="17a8b-228">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17a8b-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-231">System-Only</span></span>            | <span data-ttu-id="17a8b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-232">False</span></span>                             |
| <span data-ttu-id="17a8b-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-233">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-234">False</span></span>                             |
| <span data-ttu-id="17a8b-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-235">Is Indexed</span></span>             | <span data-ttu-id="17a8b-236">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-236">False</span></span>                             |
| <span data-ttu-id="17a8b-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-237">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-238">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-238">False</span></span>                             |
| <span data-ttu-id="17a8b-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17a8b-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17a8b-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17a8b-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-243">Search-Flags</span></span>           | <span data-ttu-id="17a8b-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-244">0x00000000</span></span>                        |
| <span data-ttu-id="17a8b-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-245">System-Flags</span></span>           | <span data-ttu-id="17a8b-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-246">0x00000010</span></span>                        |
| <span data-ttu-id="17a8b-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-247">Classes used in</span></span>        | [<span data-ttu-id="17a8b-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="17a8b-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17a8b-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17a8b-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17a8b-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-250">Entry</span></span> | <span data-ttu-id="17a8b-251">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17a8b-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-254">System-Only</span></span>            | <span data-ttu-id="17a8b-255">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-255">False</span></span>                             |
| <span data-ttu-id="17a8b-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-256">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-257">False</span></span>                             |
| <span data-ttu-id="17a8b-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-258">Is Indexed</span></span>             | <span data-ttu-id="17a8b-259">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-259">False</span></span>                             |
| <span data-ttu-id="17a8b-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-260">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-261">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-261">False</span></span>                             |
| <span data-ttu-id="17a8b-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17a8b-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17a8b-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17a8b-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-266">Search-Flags</span></span>           | <span data-ttu-id="17a8b-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-267">0x00000000</span></span>                        |
| <span data-ttu-id="17a8b-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-268">System-Flags</span></span>           | <span data-ttu-id="17a8b-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-269">0x00000010</span></span>                        |
| <span data-ttu-id="17a8b-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-270">Classes used in</span></span>        | [<span data-ttu-id="17a8b-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="17a8b-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17a8b-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17a8b-272">Windows Server 2012</span></span>



| <span data-ttu-id="17a8b-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="17a8b-273">Entry</span></span> | <span data-ttu-id="17a8b-274">Valor</span><span class="sxs-lookup"><span data-stu-id="17a8b-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="17a8b-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="17a8b-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17a8b-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="17a8b-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="17a8b-277">System-Only</span></span>            | <span data-ttu-id="17a8b-278">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-278">False</span></span>                             |
| <span data-ttu-id="17a8b-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="17a8b-279">Is-Single-Valued</span></span>       | <span data-ttu-id="17a8b-280">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-280">False</span></span>                             |
| <span data-ttu-id="17a8b-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="17a8b-281">Is Indexed</span></span>             | <span data-ttu-id="17a8b-282">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-282">False</span></span>                             |
| <span data-ttu-id="17a8b-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="17a8b-283">In Global Catalog</span></span>      | <span data-ttu-id="17a8b-284">Falso</span><span class="sxs-lookup"><span data-stu-id="17a8b-284">False</span></span>                             |
| <span data-ttu-id="17a8b-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="17a8b-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="17a8b-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="17a8b-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="17a8b-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17a8b-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="17a8b-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17a8b-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="17a8b-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-289">Search-Flags</span></span>           | <span data-ttu-id="17a8b-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17a8b-290">0x00000000</span></span>                        |
| <span data-ttu-id="17a8b-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17a8b-291">System-Flags</span></span>           | <span data-ttu-id="17a8b-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17a8b-292">0x00000010</span></span>                        |
| <span data-ttu-id="17a8b-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="17a8b-293">Classes used in</span></span>        | [<span data-ttu-id="17a8b-294">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="17a8b-294">**User**</span></span>](c-user.md)<br/> |



 

 





