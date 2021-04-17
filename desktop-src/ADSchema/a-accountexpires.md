---
title: Account-Expires atributo
description: A data em que a conta expira.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Esquema de Account-Expires do atributo AD
- Esquema de AD do atributo accountExpires
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754852"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="d8e10-105">Account-Expires atributo</span><span class="sxs-lookup"><span data-stu-id="d8e10-105">Account-Expires attribute</span></span>

<span data-ttu-id="d8e10-106">A data em que a conta expira.</span><span class="sxs-lookup"><span data-stu-id="d8e10-106">The date when the account expires.</span></span> <span data-ttu-id="d8e10-107">Esse valor representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="d8e10-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="d8e10-108">Um valor de 0 ou 0x7FFFFFFFFFFFFFFF (9223372036854775807) indica que a conta nunca expira.</span><span class="sxs-lookup"><span data-stu-id="d8e10-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="d8e10-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-109">Entry</span></span> | <span data-ttu-id="d8e10-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d8e10-111">CN</span><span class="sxs-lookup"><span data-stu-id="d8e10-111">CN</span></span>                | <span data-ttu-id="d8e10-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="d8e10-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="d8e10-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d8e10-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d8e10-114">accountExpires</span><span class="sxs-lookup"><span data-stu-id="d8e10-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="d8e10-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d8e10-115">Size</span></span>              | <span data-ttu-id="d8e10-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="d8e10-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="d8e10-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d8e10-117">Update Privilege</span></span>  | <span data-ttu-id="d8e10-118">O administrador de domínio define esse atributo.</span><span class="sxs-lookup"><span data-stu-id="d8e10-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="d8e10-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d8e10-119">Update Frequency</span></span>  | <span data-ttu-id="d8e10-120">Sempre que a data de expiração anterior expirar e precisar ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d8e10-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="d8e10-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-121">Attribute-Id</span></span>      | <span data-ttu-id="d8e10-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="d8e10-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="d8e10-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d8e10-123">System-Id-Guid</span></span>    | <span data-ttu-id="d8e10-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d8e10-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="d8e10-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8e10-125">Syntax</span></span>            | [<span data-ttu-id="d8e10-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="d8e10-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="d8e10-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="d8e10-127">Implementations</span></span>

-   [<span data-ttu-id="d8e10-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d8e10-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d8e10-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d8e10-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d8e10-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d8e10-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d8e10-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d8e10-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d8e10-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d8e10-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d8e10-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d8e10-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d8e10-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d8e10-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d8e10-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d8e10-135">Windows 2000 Server</span></span>



| <span data-ttu-id="d8e10-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-136">Entry</span></span> | <span data-ttu-id="d8e10-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d8e10-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-140">System-Only</span></span>            | <span data-ttu-id="d8e10-141">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-141">False</span></span>                             |
| <span data-ttu-id="d8e10-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-143">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-143">True</span></span>                              |
| <span data-ttu-id="d8e10-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-144">Is Indexed</span></span>             | <span data-ttu-id="d8e10-145">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-145">False</span></span>                             |
| <span data-ttu-id="d8e10-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-146">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-147">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-147">False</span></span>                             |
| <span data-ttu-id="d8e10-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d8e10-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d8e10-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d8e10-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-152">Search-Flags</span></span>           | <span data-ttu-id="d8e10-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-153">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-154">System-Flags</span></span>           | <span data-ttu-id="d8e10-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-155">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-156">Classes used in</span></span>        | [<span data-ttu-id="d8e10-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d8e10-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d8e10-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8e10-158">Windows Server 2003</span></span>



| <span data-ttu-id="d8e10-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-159">Entry</span></span> | <span data-ttu-id="d8e10-160">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d8e10-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-163">System-Only</span></span>            | <span data-ttu-id="d8e10-164">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-164">False</span></span>                             |
| <span data-ttu-id="d8e10-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-165">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-166">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-166">True</span></span>                              |
| <span data-ttu-id="d8e10-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-167">Is Indexed</span></span>             | <span data-ttu-id="d8e10-168">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-168">False</span></span>                             |
| <span data-ttu-id="d8e10-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-169">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-170">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-170">False</span></span>                             |
| <span data-ttu-id="d8e10-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d8e10-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d8e10-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d8e10-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-175">Search-Flags</span></span>           | <span data-ttu-id="d8e10-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-176">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-177">System-Flags</span></span>           | <span data-ttu-id="d8e10-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-178">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-179">Classes used in</span></span>        | [<span data-ttu-id="d8e10-180">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d8e10-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d8e10-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="d8e10-181">ADAM</span></span>



| <span data-ttu-id="d8e10-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-182">Entry</span></span> | <span data-ttu-id="d8e10-183">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="d8e10-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="d8e10-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="d8e10-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-186">System-Only</span></span>            | <span data-ttu-id="d8e10-187">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-187">False</span></span>                                                             |
| <span data-ttu-id="d8e10-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-189">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-189">True</span></span>                                                              |
| <span data-ttu-id="d8e10-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-190">Is Indexed</span></span>             | <span data-ttu-id="d8e10-191">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-191">False</span></span>                                                             |
| <span data-ttu-id="d8e10-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-192">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-193">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-193">False</span></span>                                                             |
| <span data-ttu-id="d8e10-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="d8e10-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="d8e10-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="d8e10-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-198">Search-Flags</span></span>           | <span data-ttu-id="d8e10-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="d8e10-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-200">System-Flags</span></span>           | <span data-ttu-id="d8e10-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="d8e10-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-202">Classes used in</span></span>        | [<span data-ttu-id="d8e10-203">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="d8e10-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d8e10-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d8e10-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d8e10-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-205">Entry</span></span> | <span data-ttu-id="d8e10-206">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d8e10-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-209">System-Only</span></span>            | <span data-ttu-id="d8e10-210">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-210">False</span></span>                             |
| <span data-ttu-id="d8e10-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-211">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-212">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-212">True</span></span>                              |
| <span data-ttu-id="d8e10-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-213">Is Indexed</span></span>             | <span data-ttu-id="d8e10-214">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-214">False</span></span>                             |
| <span data-ttu-id="d8e10-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-215">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-216">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-216">False</span></span>                             |
| <span data-ttu-id="d8e10-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d8e10-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d8e10-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d8e10-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-221">Search-Flags</span></span>           | <span data-ttu-id="d8e10-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-222">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-223">System-Flags</span></span>           | <span data-ttu-id="d8e10-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-224">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-225">Classes used in</span></span>        | [<span data-ttu-id="d8e10-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d8e10-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d8e10-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8e10-227">Windows Server 2008</span></span>



| <span data-ttu-id="d8e10-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-228">Entry</span></span> | <span data-ttu-id="d8e10-229">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d8e10-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-232">System-Only</span></span>            | <span data-ttu-id="d8e10-233">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-233">False</span></span>                             |
| <span data-ttu-id="d8e10-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-234">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-235">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-235">True</span></span>                              |
| <span data-ttu-id="d8e10-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-236">Is Indexed</span></span>             | <span data-ttu-id="d8e10-237">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-237">False</span></span>                             |
| <span data-ttu-id="d8e10-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-238">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-239">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-239">False</span></span>                             |
| <span data-ttu-id="d8e10-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d8e10-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d8e10-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d8e10-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-244">Search-Flags</span></span>           | <span data-ttu-id="d8e10-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-245">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-246">System-Flags</span></span>           | <span data-ttu-id="d8e10-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-247">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-248">Classes used in</span></span>        | [<span data-ttu-id="d8e10-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d8e10-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d8e10-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d8e10-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d8e10-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-251">Entry</span></span> | <span data-ttu-id="d8e10-252">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d8e10-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-255">System-Only</span></span>            | <span data-ttu-id="d8e10-256">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-256">False</span></span>                             |
| <span data-ttu-id="d8e10-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-257">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-258">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-258">True</span></span>                              |
| <span data-ttu-id="d8e10-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-259">Is Indexed</span></span>             | <span data-ttu-id="d8e10-260">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-260">False</span></span>                             |
| <span data-ttu-id="d8e10-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-261">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-262">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-262">False</span></span>                             |
| <span data-ttu-id="d8e10-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d8e10-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d8e10-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d8e10-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-267">Search-Flags</span></span>           | <span data-ttu-id="d8e10-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-268">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-269">System-Flags</span></span>           | <span data-ttu-id="d8e10-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-270">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-271">Classes used in</span></span>        | [<span data-ttu-id="d8e10-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d8e10-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d8e10-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8e10-273">Windows Server 2012</span></span>



| <span data-ttu-id="d8e10-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="d8e10-274">Entry</span></span> | <span data-ttu-id="d8e10-275">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e10-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d8e10-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="d8e10-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d8e10-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d8e10-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="d8e10-278">System-Only</span></span>            | <span data-ttu-id="d8e10-279">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-279">False</span></span>                             |
| <span data-ttu-id="d8e10-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d8e10-280">Is-Single-Valued</span></span>       | <span data-ttu-id="d8e10-281">True</span><span class="sxs-lookup"><span data-stu-id="d8e10-281">True</span></span>                              |
| <span data-ttu-id="d8e10-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="d8e10-282">Is Indexed</span></span>             | <span data-ttu-id="d8e10-283">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-283">False</span></span>                             |
| <span data-ttu-id="d8e10-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d8e10-284">In Global Catalog</span></span>      | <span data-ttu-id="d8e10-285">Falso</span><span class="sxs-lookup"><span data-stu-id="d8e10-285">False</span></span>                             |
| <span data-ttu-id="d8e10-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d8e10-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="d8e10-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d8e10-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d8e10-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d8e10-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d8e10-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d8e10-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d8e10-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-290">Search-Flags</span></span>           | <span data-ttu-id="d8e10-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-291">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d8e10-292">System-Flags</span></span>           | <span data-ttu-id="d8e10-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d8e10-293">0x00000010</span></span>                        |
| <span data-ttu-id="d8e10-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d8e10-294">Classes used in</span></span>        | [<span data-ttu-id="d8e10-295">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="d8e10-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d8e10-296">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8e10-296">Remarks</span></span>

<span data-ttu-id="d8e10-297">A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="d8e10-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 

