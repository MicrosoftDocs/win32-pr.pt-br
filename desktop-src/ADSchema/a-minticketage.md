---
title: Atributo min-ticket-age
description: Esse atributo determina o período de tempo mínimo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo min-ticket-age
- Esquema de AD do atributo minTicketAge
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086729"
---
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="78663-105">Atributo min-ticket-age</span><span class="sxs-lookup"><span data-stu-id="78663-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="78663-106">Esse atributo determina o período de tempo mínimo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.</span><span class="sxs-lookup"><span data-stu-id="78663-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="78663-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-107">Entry</span></span> | <span data-ttu-id="78663-108">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="78663-109">CN</span><span class="sxs-lookup"><span data-stu-id="78663-109">CN</span></span>                | <span data-ttu-id="78663-110">Duração mínima de tíquetes</span><span class="sxs-lookup"><span data-stu-id="78663-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="78663-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="78663-111">Ldap-Display-Name</span></span> | <span data-ttu-id="78663-112">minTicketAge</span><span class="sxs-lookup"><span data-stu-id="78663-112">minTicketAge</span></span>                         |
| <span data-ttu-id="78663-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="78663-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="78663-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="78663-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="78663-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="78663-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="78663-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78663-116">Attribute-Id</span></span>      | <span data-ttu-id="78663-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="78663-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="78663-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78663-118">System-Id-Guid</span></span>    | <span data-ttu-id="78663-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="78663-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="78663-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="78663-120">Syntax</span></span>            | [<span data-ttu-id="78663-121">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="78663-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="78663-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="78663-122">Implementations</span></span>

-   [<span data-ttu-id="78663-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78663-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78663-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78663-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78663-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78663-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78663-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78663-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78663-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78663-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78663-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78663-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78663-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78663-129">Windows 2000 Server</span></span>



| <span data-ttu-id="78663-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-130">Entry</span></span> | <span data-ttu-id="78663-131">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="78663-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="78663-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78663-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="78663-134">System-Only</span></span>            | <span data-ttu-id="78663-135">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-135">False</span></span>                                              |
| <span data-ttu-id="78663-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78663-136">Is-Single-Valued</span></span>       | <span data-ttu-id="78663-137">True</span><span class="sxs-lookup"><span data-stu-id="78663-137">True</span></span>                                               |
| <span data-ttu-id="78663-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="78663-138">Is Indexed</span></span>             | <span data-ttu-id="78663-139">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-139">False</span></span>                                              |
| <span data-ttu-id="78663-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78663-140">In Global Catalog</span></span>      | <span data-ttu-id="78663-141">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-141">False</span></span>                                              |
| <span data-ttu-id="78663-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78663-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="78663-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78663-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="78663-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78663-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="78663-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78663-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="78663-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-146">Search-Flags</span></span>           | <span data-ttu-id="78663-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78663-147">0x00000000</span></span>                                         |
| <span data-ttu-id="78663-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-148">System-Flags</span></span>           | <span data-ttu-id="78663-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78663-149">0x00000010</span></span>                                         |
| <span data-ttu-id="78663-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78663-150">Classes used in</span></span>        | [<span data-ttu-id="78663-151">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="78663-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78663-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78663-152">Windows Server 2003</span></span>



| <span data-ttu-id="78663-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-153">Entry</span></span> | <span data-ttu-id="78663-154">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="78663-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="78663-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78663-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="78663-157">System-Only</span></span>            | <span data-ttu-id="78663-158">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-158">False</span></span>                                              |
| <span data-ttu-id="78663-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78663-159">Is-Single-Valued</span></span>       | <span data-ttu-id="78663-160">True</span><span class="sxs-lookup"><span data-stu-id="78663-160">True</span></span>                                               |
| <span data-ttu-id="78663-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="78663-161">Is Indexed</span></span>             | <span data-ttu-id="78663-162">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-162">False</span></span>                                              |
| <span data-ttu-id="78663-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78663-163">In Global Catalog</span></span>      | <span data-ttu-id="78663-164">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-164">False</span></span>                                              |
| <span data-ttu-id="78663-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78663-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="78663-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78663-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="78663-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78663-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="78663-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78663-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="78663-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-169">Search-Flags</span></span>           | <span data-ttu-id="78663-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78663-170">0x00000000</span></span>                                         |
| <span data-ttu-id="78663-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-171">System-Flags</span></span>           | <span data-ttu-id="78663-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78663-172">0x00000010</span></span>                                         |
| <span data-ttu-id="78663-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78663-173">Classes used in</span></span>        | [<span data-ttu-id="78663-174">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="78663-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78663-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78663-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78663-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-176">Entry</span></span> | <span data-ttu-id="78663-177">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="78663-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="78663-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78663-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="78663-180">System-Only</span></span>            | <span data-ttu-id="78663-181">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-181">False</span></span>                                              |
| <span data-ttu-id="78663-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78663-182">Is-Single-Valued</span></span>       | <span data-ttu-id="78663-183">True</span><span class="sxs-lookup"><span data-stu-id="78663-183">True</span></span>                                               |
| <span data-ttu-id="78663-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="78663-184">Is Indexed</span></span>             | <span data-ttu-id="78663-185">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-185">False</span></span>                                              |
| <span data-ttu-id="78663-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78663-186">In Global Catalog</span></span>      | <span data-ttu-id="78663-187">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-187">False</span></span>                                              |
| <span data-ttu-id="78663-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78663-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="78663-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78663-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="78663-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78663-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="78663-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78663-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="78663-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-192">Search-Flags</span></span>           | <span data-ttu-id="78663-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78663-193">0x00000000</span></span>                                         |
| <span data-ttu-id="78663-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-194">System-Flags</span></span>           | <span data-ttu-id="78663-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78663-195">0x00000010</span></span>                                         |
| <span data-ttu-id="78663-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78663-196">Classes used in</span></span>        | [<span data-ttu-id="78663-197">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="78663-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78663-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78663-198">Windows Server 2008</span></span>



| <span data-ttu-id="78663-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-199">Entry</span></span> | <span data-ttu-id="78663-200">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="78663-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="78663-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78663-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="78663-203">System-Only</span></span>            | <span data-ttu-id="78663-204">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-204">False</span></span>                                              |
| <span data-ttu-id="78663-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78663-205">Is-Single-Valued</span></span>       | <span data-ttu-id="78663-206">True</span><span class="sxs-lookup"><span data-stu-id="78663-206">True</span></span>                                               |
| <span data-ttu-id="78663-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="78663-207">Is Indexed</span></span>             | <span data-ttu-id="78663-208">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-208">False</span></span>                                              |
| <span data-ttu-id="78663-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78663-209">In Global Catalog</span></span>      | <span data-ttu-id="78663-210">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-210">False</span></span>                                              |
| <span data-ttu-id="78663-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78663-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="78663-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78663-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="78663-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78663-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="78663-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78663-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="78663-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-215">Search-Flags</span></span>           | <span data-ttu-id="78663-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78663-216">0x00000000</span></span>                                         |
| <span data-ttu-id="78663-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-217">System-Flags</span></span>           | <span data-ttu-id="78663-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78663-218">0x00000010</span></span>                                         |
| <span data-ttu-id="78663-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78663-219">Classes used in</span></span>        | [<span data-ttu-id="78663-220">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="78663-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78663-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78663-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78663-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-222">Entry</span></span> | <span data-ttu-id="78663-223">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="78663-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="78663-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78663-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="78663-226">System-Only</span></span>            | <span data-ttu-id="78663-227">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-227">False</span></span>                                              |
| <span data-ttu-id="78663-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78663-228">Is-Single-Valued</span></span>       | <span data-ttu-id="78663-229">True</span><span class="sxs-lookup"><span data-stu-id="78663-229">True</span></span>                                               |
| <span data-ttu-id="78663-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="78663-230">Is Indexed</span></span>             | <span data-ttu-id="78663-231">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-231">False</span></span>                                              |
| <span data-ttu-id="78663-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78663-232">In Global Catalog</span></span>      | <span data-ttu-id="78663-233">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-233">False</span></span>                                              |
| <span data-ttu-id="78663-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78663-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="78663-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78663-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="78663-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78663-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="78663-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78663-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="78663-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-238">Search-Flags</span></span>           | <span data-ttu-id="78663-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78663-239">0x00000000</span></span>                                         |
| <span data-ttu-id="78663-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-240">System-Flags</span></span>           | <span data-ttu-id="78663-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78663-241">0x00000010</span></span>                                         |
| <span data-ttu-id="78663-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78663-242">Classes used in</span></span>        | [<span data-ttu-id="78663-243">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="78663-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78663-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78663-244">Windows Server 2012</span></span>



| <span data-ttu-id="78663-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="78663-245">Entry</span></span> | <span data-ttu-id="78663-246">Valor</span><span class="sxs-lookup"><span data-stu-id="78663-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="78663-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="78663-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78663-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="78663-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="78663-249">System-Only</span></span>            | <span data-ttu-id="78663-250">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-250">False</span></span>                                              |
| <span data-ttu-id="78663-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78663-251">Is-Single-Valued</span></span>       | <span data-ttu-id="78663-252">True</span><span class="sxs-lookup"><span data-stu-id="78663-252">True</span></span>                                               |
| <span data-ttu-id="78663-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="78663-253">Is Indexed</span></span>             | <span data-ttu-id="78663-254">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-254">False</span></span>                                              |
| <span data-ttu-id="78663-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78663-255">In Global Catalog</span></span>      | <span data-ttu-id="78663-256">Falso</span><span class="sxs-lookup"><span data-stu-id="78663-256">False</span></span>                                              |
| <span data-ttu-id="78663-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78663-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="78663-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78663-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="78663-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78663-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="78663-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78663-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="78663-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-261">Search-Flags</span></span>           | <span data-ttu-id="78663-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78663-262">0x00000000</span></span>                                         |
| <span data-ttu-id="78663-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78663-263">System-Flags</span></span>           | <span data-ttu-id="78663-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78663-264">0x00000010</span></span>                                         |
| <span data-ttu-id="78663-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78663-265">Classes used in</span></span>        | [<span data-ttu-id="78663-266">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="78663-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





