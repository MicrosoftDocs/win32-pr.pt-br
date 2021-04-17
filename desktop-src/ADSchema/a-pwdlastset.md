---
title: Nome do atributo pwd-Last-Set
description: A data e a hora em que a senha desta conta foi alterada pela última vez.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- Pwd-esquema de AD do atributo Last-Set
- Esquema de AD do atributo pwdLastSet
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc49fbbf768d2ca873f6f35f61022cc9182830b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105748272"
---
# <a name="pwd-last-set-attribute"></a><span data-ttu-id="972e2-105">Nome do atributo pwd-Last-Set</span><span class="sxs-lookup"><span data-stu-id="972e2-105">Pwd-Last-Set attribute</span></span>

<span data-ttu-id="972e2-106">A data e a hora em que a senha desta conta foi alterada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="972e2-106">The date and time that the password for this account was last changed.</span></span> <span data-ttu-id="972e2-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="972e2-107">This value is stored as a large integer that represents the number of 100 nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="972e2-108">Se esse valor for definido como 0 e o atributo de [**controle de conta de usuário**](a-useraccountcontrol.md) não contiver o sinalizador de **senha da UF não \_ \_ expirar \_** , o usuário deverá definir a senha no próximo logon.</span><span class="sxs-lookup"><span data-stu-id="972e2-108">If this value is set to 0 and the [**User-Account-Control**](a-useraccountcontrol.md) attribute does not contain the **UF\_DONT\_EXPIRE\_PASSWD** flag, then the user must set the password at the next logon.</span></span>



| <span data-ttu-id="972e2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-109">Entry</span></span> | <span data-ttu-id="972e2-110">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="972e2-111">CN</span><span class="sxs-lookup"><span data-stu-id="972e2-111">CN</span></span>                | <span data-ttu-id="972e2-112">Pwd-último-conjunto</span><span class="sxs-lookup"><span data-stu-id="972e2-112">Pwd-Last-Set</span></span>                         |
| <span data-ttu-id="972e2-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="972e2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="972e2-114">pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="972e2-114">pwdLastSet</span></span>                           |
| <span data-ttu-id="972e2-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="972e2-115">Size</span></span>              | <span data-ttu-id="972e2-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="972e2-116">8 bytes</span></span>                              |
| <span data-ttu-id="972e2-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="972e2-117">Update Privilege</span></span>  | <span data-ttu-id="972e2-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="972e2-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="972e2-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="972e2-119">Update Frequency</span></span>  | <span data-ttu-id="972e2-120">Cada vez que a senha é alterada.</span><span class="sxs-lookup"><span data-stu-id="972e2-120">Each time the password is changed.</span></span>   |
| <span data-ttu-id="972e2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-121">Attribute-Id</span></span>      | <span data-ttu-id="972e2-122">1.2.840.113556.1.4.96</span><span class="sxs-lookup"><span data-stu-id="972e2-122">1.2.840.113556.1.4.96</span></span>                |
| <span data-ttu-id="972e2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="972e2-123">System-Id-Guid</span></span>    | <span data-ttu-id="972e2-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="972e2-124">bf967a0a-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="972e2-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="972e2-125">Syntax</span></span>            | [<span data-ttu-id="972e2-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="972e2-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="972e2-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="972e2-127">Implementations</span></span>

-   [<span data-ttu-id="972e2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="972e2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="972e2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="972e2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="972e2-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="972e2-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="972e2-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="972e2-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="972e2-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="972e2-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="972e2-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="972e2-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="972e2-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="972e2-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="972e2-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="972e2-135">Windows 2000 Server</span></span>



| <span data-ttu-id="972e2-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-136">Entry</span></span> | <span data-ttu-id="972e2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="972e2-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-140">System-Only</span></span>            | <span data-ttu-id="972e2-141">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-141">False</span></span>                             |
| <span data-ttu-id="972e2-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-142">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-143">True</span><span class="sxs-lookup"><span data-stu-id="972e2-143">True</span></span>                              |
| <span data-ttu-id="972e2-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-144">Is Indexed</span></span>             | <span data-ttu-id="972e2-145">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-145">False</span></span>                             |
| <span data-ttu-id="972e2-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-146">In Global Catalog</span></span>      | <span data-ttu-id="972e2-147">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-147">False</span></span>                             |
| <span data-ttu-id="972e2-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="972e2-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="972e2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="972e2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-152">Search-Flags</span></span>           | <span data-ttu-id="972e2-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-153">0x00000000</span></span>                        |
| <span data-ttu-id="972e2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-154">System-Flags</span></span>           | <span data-ttu-id="972e2-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-155">0x00000010</span></span>                        |
| <span data-ttu-id="972e2-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-156">Classes used in</span></span>        | [<span data-ttu-id="972e2-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="972e2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="972e2-158">Windows Server 2003</span></span>



| <span data-ttu-id="972e2-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-159">Entry</span></span> | <span data-ttu-id="972e2-160">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="972e2-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-163">System-Only</span></span>            | <span data-ttu-id="972e2-164">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-164">False</span></span>                             |
| <span data-ttu-id="972e2-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-166">True</span><span class="sxs-lookup"><span data-stu-id="972e2-166">True</span></span>                              |
| <span data-ttu-id="972e2-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-167">Is Indexed</span></span>             | <span data-ttu-id="972e2-168">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-168">False</span></span>                             |
| <span data-ttu-id="972e2-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-169">In Global Catalog</span></span>      | <span data-ttu-id="972e2-170">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-170">False</span></span>                             |
| <span data-ttu-id="972e2-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="972e2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="972e2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="972e2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-175">Search-Flags</span></span>           | <span data-ttu-id="972e2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-176">0x00000000</span></span>                        |
| <span data-ttu-id="972e2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-177">System-Flags</span></span>           | <span data-ttu-id="972e2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-178">0x00000010</span></span>                        |
| <span data-ttu-id="972e2-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-179">Classes used in</span></span>        | [<span data-ttu-id="972e2-180">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="972e2-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="972e2-181">ADAM</span></span>



| <span data-ttu-id="972e2-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-182">Entry</span></span> | <span data-ttu-id="972e2-183">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="972e2-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="972e2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="972e2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-186">System-Only</span></span>            | <span data-ttu-id="972e2-187">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-187">False</span></span>                                                             |
| <span data-ttu-id="972e2-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-189">True</span><span class="sxs-lookup"><span data-stu-id="972e2-189">True</span></span>                                                              |
| <span data-ttu-id="972e2-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-190">Is Indexed</span></span>             | <span data-ttu-id="972e2-191">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-191">False</span></span>                                                             |
| <span data-ttu-id="972e2-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-192">In Global Catalog</span></span>      | <span data-ttu-id="972e2-193">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-193">False</span></span>                                                             |
| <span data-ttu-id="972e2-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="972e2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="972e2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="972e2-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-198">Search-Flags</span></span>           | <span data-ttu-id="972e2-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="972e2-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-200">System-Flags</span></span>           | <span data-ttu-id="972e2-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="972e2-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-202">Classes used in</span></span>        | [<span data-ttu-id="972e2-203">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="972e2-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="972e2-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="972e2-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="972e2-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-205">Entry</span></span> | <span data-ttu-id="972e2-206">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="972e2-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-209">System-Only</span></span>            | <span data-ttu-id="972e2-210">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-210">False</span></span>                             |
| <span data-ttu-id="972e2-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-212">True</span><span class="sxs-lookup"><span data-stu-id="972e2-212">True</span></span>                              |
| <span data-ttu-id="972e2-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-213">Is Indexed</span></span>             | <span data-ttu-id="972e2-214">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-214">False</span></span>                             |
| <span data-ttu-id="972e2-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-215">In Global Catalog</span></span>      | <span data-ttu-id="972e2-216">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-216">False</span></span>                             |
| <span data-ttu-id="972e2-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="972e2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="972e2-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="972e2-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-221">Search-Flags</span></span>           | <span data-ttu-id="972e2-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-222">0x00000000</span></span>                        |
| <span data-ttu-id="972e2-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-223">System-Flags</span></span>           | <span data-ttu-id="972e2-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-224">0x00000010</span></span>                        |
| <span data-ttu-id="972e2-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-225">Classes used in</span></span>        | [<span data-ttu-id="972e2-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="972e2-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="972e2-227">Windows Server 2008</span></span>



| <span data-ttu-id="972e2-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-228">Entry</span></span> | <span data-ttu-id="972e2-229">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="972e2-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-232">System-Only</span></span>            | <span data-ttu-id="972e2-233">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-233">False</span></span>                             |
| <span data-ttu-id="972e2-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-234">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-235">True</span><span class="sxs-lookup"><span data-stu-id="972e2-235">True</span></span>                              |
| <span data-ttu-id="972e2-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-236">Is Indexed</span></span>             | <span data-ttu-id="972e2-237">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-237">False</span></span>                             |
| <span data-ttu-id="972e2-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-238">In Global Catalog</span></span>      | <span data-ttu-id="972e2-239">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-239">False</span></span>                             |
| <span data-ttu-id="972e2-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="972e2-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="972e2-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="972e2-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-244">Search-Flags</span></span>           | <span data-ttu-id="972e2-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-245">0x00000000</span></span>                        |
| <span data-ttu-id="972e2-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-246">System-Flags</span></span>           | <span data-ttu-id="972e2-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-247">0x00000010</span></span>                        |
| <span data-ttu-id="972e2-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-248">Classes used in</span></span>        | [<span data-ttu-id="972e2-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="972e2-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="972e2-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="972e2-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-251">Entry</span></span> | <span data-ttu-id="972e2-252">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="972e2-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-255">System-Only</span></span>            | <span data-ttu-id="972e2-256">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-256">False</span></span>                             |
| <span data-ttu-id="972e2-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-257">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-258">True</span><span class="sxs-lookup"><span data-stu-id="972e2-258">True</span></span>                              |
| <span data-ttu-id="972e2-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-259">Is Indexed</span></span>             | <span data-ttu-id="972e2-260">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-260">False</span></span>                             |
| <span data-ttu-id="972e2-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-261">In Global Catalog</span></span>      | <span data-ttu-id="972e2-262">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-262">False</span></span>                             |
| <span data-ttu-id="972e2-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="972e2-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="972e2-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="972e2-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-267">Search-Flags</span></span>           | <span data-ttu-id="972e2-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-268">0x00000000</span></span>                        |
| <span data-ttu-id="972e2-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-269">System-Flags</span></span>           | <span data-ttu-id="972e2-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-270">0x00000010</span></span>                        |
| <span data-ttu-id="972e2-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-271">Classes used in</span></span>        | [<span data-ttu-id="972e2-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="972e2-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="972e2-273">Windows Server 2012</span></span>



| <span data-ttu-id="972e2-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="972e2-274">Entry</span></span> | <span data-ttu-id="972e2-275">Valor</span><span class="sxs-lookup"><span data-stu-id="972e2-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="972e2-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="972e2-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="972e2-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="972e2-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="972e2-278">System-Only</span></span>            | <span data-ttu-id="972e2-279">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-279">False</span></span>                             |
| <span data-ttu-id="972e2-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="972e2-280">Is-Single-Valued</span></span>       | <span data-ttu-id="972e2-281">True</span><span class="sxs-lookup"><span data-stu-id="972e2-281">True</span></span>                              |
| <span data-ttu-id="972e2-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="972e2-282">Is Indexed</span></span>             | <span data-ttu-id="972e2-283">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-283">False</span></span>                             |
| <span data-ttu-id="972e2-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="972e2-284">In Global Catalog</span></span>      | <span data-ttu-id="972e2-285">Falso</span><span class="sxs-lookup"><span data-stu-id="972e2-285">False</span></span>                             |
| <span data-ttu-id="972e2-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="972e2-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="972e2-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="972e2-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="972e2-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="972e2-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="972e2-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="972e2-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="972e2-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-290">Search-Flags</span></span>           | <span data-ttu-id="972e2-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="972e2-291">0x00000000</span></span>                        |
| <span data-ttu-id="972e2-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="972e2-292">System-Flags</span></span>           | <span data-ttu-id="972e2-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="972e2-293">0x00000010</span></span>                        |
| <span data-ttu-id="972e2-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="972e2-294">Classes used in</span></span>        | [<span data-ttu-id="972e2-295">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="972e2-296">Comentários</span><span class="sxs-lookup"><span data-stu-id="972e2-296">Remarks</span></span>

<span data-ttu-id="972e2-297">A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="972e2-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="972e2-298">Confira também</span><span class="sxs-lookup"><span data-stu-id="972e2-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972e2-299">**Controle de conta de usuário**</span><span class="sxs-lookup"><span data-stu-id="972e2-299">**User-Account-Control**</span></span>](a-useraccountcontrol.md)
</dt> </dl>

 

