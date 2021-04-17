---
title: Lockout-Time atributo
description: A data e hora (UTC) em que essa conta foi bloqueada.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Esquema de Lockout-Time do atributo AD
- atributo de AD de atributos locktime
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755255"
---
# <a name="lockout-time-attribute"></a><span data-ttu-id="51dfb-105">Lockout-Time atributo</span><span class="sxs-lookup"><span data-stu-id="51dfb-105">Lockout-Time attribute</span></span>

<span data-ttu-id="51dfb-106">A data e hora (UTC) em que essa conta foi bloqueada. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="51dfb-106">The date and time (UTC) that this account was locked out. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="51dfb-107">Um valor de zero significa que a conta não está bloqueada no momento.</span><span class="sxs-lookup"><span data-stu-id="51dfb-107">A value of zero means that the account is not currently locked out.</span></span>



| <span data-ttu-id="51dfb-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-108">Entry</span></span> | <span data-ttu-id="51dfb-109">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="51dfb-110">CN</span><span class="sxs-lookup"><span data-stu-id="51dfb-110">CN</span></span>                | <span data-ttu-id="51dfb-111">Lockout-Time</span><span class="sxs-lookup"><span data-stu-id="51dfb-111">Lockout-Time</span></span>                                                                     |
| <span data-ttu-id="51dfb-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="51dfb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="51dfb-113">lockoutTime</span><span class="sxs-lookup"><span data-stu-id="51dfb-113">lockoutTime</span></span>                                                                      |
| <span data-ttu-id="51dfb-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="51dfb-114">Size</span></span>              | <span data-ttu-id="51dfb-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="51dfb-115">8 bytes</span></span>                                                                          |
| <span data-ttu-id="51dfb-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="51dfb-116">Update Privilege</span></span>  | <span data-ttu-id="51dfb-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="51dfb-117">Domain administrator</span></span>                                                             |
| <span data-ttu-id="51dfb-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="51dfb-118">Update Frequency</span></span>  | <span data-ttu-id="51dfb-119">Quando o registro do usuário é criado e sempre que o tempo de bloqueio precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="51dfb-119">When the user's record is created and whenever the lockout time needs to change.</span></span> |
| <span data-ttu-id="51dfb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-120">Attribute-Id</span></span>      | <span data-ttu-id="51dfb-121">1.2.840.113556.1.4.662</span><span class="sxs-lookup"><span data-stu-id="51dfb-121">1.2.840.113556.1.4.662</span></span>                                                           |
| <span data-ttu-id="51dfb-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="51dfb-122">System-Id-Guid</span></span>    | <span data-ttu-id="51dfb-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="51dfb-123">28630ebf-41d5-11d1-a9c1-0000f80367c1</span></span>                                             |
| <span data-ttu-id="51dfb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="51dfb-124">Syntax</span></span>            | [<span data-ttu-id="51dfb-125">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="51dfb-125">**Interval**</span></span>](s-interval.md)                                                   |



## <a name="implementations"></a><span data-ttu-id="51dfb-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="51dfb-126">Implementations</span></span>

-   [<span data-ttu-id="51dfb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51dfb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51dfb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51dfb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51dfb-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="51dfb-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="51dfb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51dfb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51dfb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51dfb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51dfb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51dfb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51dfb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51dfb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51dfb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51dfb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="51dfb-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-135">Entry</span></span> | <span data-ttu-id="51dfb-136">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51dfb-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-139">System-Only</span></span>            | <span data-ttu-id="51dfb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-140">False</span></span>                             |
| <span data-ttu-id="51dfb-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-142">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-142">True</span></span>                              |
| <span data-ttu-id="51dfb-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-143">Is Indexed</span></span>             | <span data-ttu-id="51dfb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-144">False</span></span>                             |
| <span data-ttu-id="51dfb-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-145">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-146">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-146">False</span></span>                             |
| <span data-ttu-id="51dfb-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51dfb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51dfb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51dfb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-151">Search-Flags</span></span>           | <span data-ttu-id="51dfb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-152">0x00000000</span></span>                        |
| <span data-ttu-id="51dfb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-153">System-Flags</span></span>           | <span data-ttu-id="51dfb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-154">0x00000010</span></span>                        |
| <span data-ttu-id="51dfb-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-155">Classes used in</span></span>        | [<span data-ttu-id="51dfb-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="51dfb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51dfb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51dfb-157">Windows Server 2003</span></span>



| <span data-ttu-id="51dfb-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-158">Entry</span></span> | <span data-ttu-id="51dfb-159">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51dfb-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-162">System-Only</span></span>            | <span data-ttu-id="51dfb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-163">False</span></span>                             |
| <span data-ttu-id="51dfb-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-165">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-165">True</span></span>                              |
| <span data-ttu-id="51dfb-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-166">Is Indexed</span></span>             | <span data-ttu-id="51dfb-167">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-167">False</span></span>                             |
| <span data-ttu-id="51dfb-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-168">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-169">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-169">False</span></span>                             |
| <span data-ttu-id="51dfb-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51dfb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51dfb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51dfb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-174">Search-Flags</span></span>           | <span data-ttu-id="51dfb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-175">0x00000000</span></span>                        |
| <span data-ttu-id="51dfb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-176">System-Flags</span></span>           | <span data-ttu-id="51dfb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-177">0x00000010</span></span>                        |
| <span data-ttu-id="51dfb-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-178">Classes used in</span></span>        | [<span data-ttu-id="51dfb-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="51dfb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="51dfb-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="51dfb-180">ADAM</span></span>



| <span data-ttu-id="51dfb-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-181">Entry</span></span> | <span data-ttu-id="51dfb-182">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="51dfb-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="51dfb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="51dfb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-185">System-Only</span></span>            | <span data-ttu-id="51dfb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-186">False</span></span>                                                             |
| <span data-ttu-id="51dfb-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-188">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-188">True</span></span>                                                              |
| <span data-ttu-id="51dfb-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-189">Is Indexed</span></span>             | <span data-ttu-id="51dfb-190">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-190">False</span></span>                                                             |
| <span data-ttu-id="51dfb-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-191">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-192">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-192">False</span></span>                                                             |
| <span data-ttu-id="51dfb-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="51dfb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="51dfb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="51dfb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-197">Search-Flags</span></span>           | <span data-ttu-id="51dfb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="51dfb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-199">System-Flags</span></span>           | <span data-ttu-id="51dfb-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="51dfb-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-201">Classes used in</span></span>        | [<span data-ttu-id="51dfb-202">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="51dfb-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51dfb-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51dfb-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51dfb-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-204">Entry</span></span> | <span data-ttu-id="51dfb-205">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51dfb-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-208">System-Only</span></span>            | <span data-ttu-id="51dfb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-209">False</span></span>                             |
| <span data-ttu-id="51dfb-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-211">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-211">True</span></span>                              |
| <span data-ttu-id="51dfb-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-212">Is Indexed</span></span>             | <span data-ttu-id="51dfb-213">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-213">False</span></span>                             |
| <span data-ttu-id="51dfb-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-214">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-215">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-215">False</span></span>                             |
| <span data-ttu-id="51dfb-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51dfb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51dfb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51dfb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-220">Search-Flags</span></span>           | <span data-ttu-id="51dfb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-221">0x00000000</span></span>                        |
| <span data-ttu-id="51dfb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-222">System-Flags</span></span>           | <span data-ttu-id="51dfb-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-223">0x00000010</span></span>                        |
| <span data-ttu-id="51dfb-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-224">Classes used in</span></span>        | [<span data-ttu-id="51dfb-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="51dfb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51dfb-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51dfb-226">Windows Server 2008</span></span>



| <span data-ttu-id="51dfb-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-227">Entry</span></span> | <span data-ttu-id="51dfb-228">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51dfb-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-231">System-Only</span></span>            | <span data-ttu-id="51dfb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-232">False</span></span>                             |
| <span data-ttu-id="51dfb-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-234">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-234">True</span></span>                              |
| <span data-ttu-id="51dfb-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-235">Is Indexed</span></span>             | <span data-ttu-id="51dfb-236">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-236">False</span></span>                             |
| <span data-ttu-id="51dfb-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-237">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-238">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-238">False</span></span>                             |
| <span data-ttu-id="51dfb-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51dfb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51dfb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51dfb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-243">Search-Flags</span></span>           | <span data-ttu-id="51dfb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-244">0x00000000</span></span>                        |
| <span data-ttu-id="51dfb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-245">System-Flags</span></span>           | <span data-ttu-id="51dfb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-246">0x00000010</span></span>                        |
| <span data-ttu-id="51dfb-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-247">Classes used in</span></span>        | [<span data-ttu-id="51dfb-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="51dfb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51dfb-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51dfb-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51dfb-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-250">Entry</span></span> | <span data-ttu-id="51dfb-251">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51dfb-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-254">System-Only</span></span>            | <span data-ttu-id="51dfb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-255">False</span></span>                             |
| <span data-ttu-id="51dfb-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-257">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-257">True</span></span>                              |
| <span data-ttu-id="51dfb-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-258">Is Indexed</span></span>             | <span data-ttu-id="51dfb-259">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-259">False</span></span>                             |
| <span data-ttu-id="51dfb-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-260">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-261">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-261">False</span></span>                             |
| <span data-ttu-id="51dfb-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51dfb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51dfb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51dfb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-266">Search-Flags</span></span>           | <span data-ttu-id="51dfb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-267">0x00000000</span></span>                        |
| <span data-ttu-id="51dfb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-268">System-Flags</span></span>           | <span data-ttu-id="51dfb-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-269">0x00000010</span></span>                        |
| <span data-ttu-id="51dfb-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-270">Classes used in</span></span>        | [<span data-ttu-id="51dfb-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="51dfb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51dfb-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51dfb-272">Windows Server 2012</span></span>



| <span data-ttu-id="51dfb-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="51dfb-273">Entry</span></span> | <span data-ttu-id="51dfb-274">Valor</span><span class="sxs-lookup"><span data-stu-id="51dfb-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51dfb-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="51dfb-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51dfb-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51dfb-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="51dfb-277">System-Only</span></span>            | <span data-ttu-id="51dfb-278">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-278">False</span></span>                             |
| <span data-ttu-id="51dfb-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="51dfb-279">Is-Single-Valued</span></span>       | <span data-ttu-id="51dfb-280">True</span><span class="sxs-lookup"><span data-stu-id="51dfb-280">True</span></span>                              |
| <span data-ttu-id="51dfb-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="51dfb-281">Is Indexed</span></span>             | <span data-ttu-id="51dfb-282">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-282">False</span></span>                             |
| <span data-ttu-id="51dfb-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="51dfb-283">In Global Catalog</span></span>      | <span data-ttu-id="51dfb-284">Falso</span><span class="sxs-lookup"><span data-stu-id="51dfb-284">False</span></span>                             |
| <span data-ttu-id="51dfb-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="51dfb-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="51dfb-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="51dfb-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51dfb-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51dfb-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51dfb-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51dfb-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51dfb-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-289">Search-Flags</span></span>           | <span data-ttu-id="51dfb-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51dfb-290">0x00000000</span></span>                        |
| <span data-ttu-id="51dfb-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51dfb-291">System-Flags</span></span>           | <span data-ttu-id="51dfb-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51dfb-292">0x00000010</span></span>                        |
| <span data-ttu-id="51dfb-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="51dfb-293">Classes used in</span></span>        | [<span data-ttu-id="51dfb-294">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="51dfb-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="51dfb-295">Comentários</span><span class="sxs-lookup"><span data-stu-id="51dfb-295">Remarks</span></span>

<span data-ttu-id="51dfb-296">A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="51dfb-296">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="51dfb-297">Esse valor de atributo só é redefinido quando a conta é registrada em log com êxito.</span><span class="sxs-lookup"><span data-stu-id="51dfb-297">This attribute value is only reset when the account is logged onto successfully.</span></span> <span data-ttu-id="51dfb-298">Isso significa que esse valor pode ser diferente de zero, mas a conta não está bloqueada. Para determinar com precisão se a conta está bloqueada, você deve adicionar a [**duração do bloqueio**](a-lockoutduration.md) a esse tempo e comparar o resultado com a hora atual, a contabilização de fusos horários locais e do horário de verão.</span><span class="sxs-lookup"><span data-stu-id="51dfb-298">This means that this value may be non zero, yet the account is not locked out. To accurately determine if the account is locked out, you must add the [**Lockout-Duration**](a-lockoutduration.md) to this time and compare the result to the current time, accounting for local time zones and daylight savings time.</span></span>

## <a name="see-also"></a><span data-ttu-id="51dfb-299">Confira também</span><span class="sxs-lookup"><span data-stu-id="51dfb-299">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51dfb-300">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="51dfb-300">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="51dfb-301">**Duração do bloqueio**</span><span class="sxs-lookup"><span data-stu-id="51dfb-301">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

