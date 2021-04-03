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
# <a name="min-ticket-age-attribute"></a><span data-ttu-id="e5c2b-105">Atributo min-ticket-age</span><span class="sxs-lookup"><span data-stu-id="e5c2b-105">Min-Ticket-Age attribute</span></span>

<span data-ttu-id="e5c2b-106">Esse atributo determina o período de tempo mínimo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.</span><span class="sxs-lookup"><span data-stu-id="e5c2b-106">This attribute determines the minimum time period, in hours, that a user's ticket-granting ticket (TGT) can be used for Kerberos authentication before a request can be made to renew the ticket.</span></span>



| <span data-ttu-id="e5c2b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-107">Entry</span></span> | <span data-ttu-id="e5c2b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e5c2b-109">CN</span><span class="sxs-lookup"><span data-stu-id="e5c2b-109">CN</span></span>                | <span data-ttu-id="e5c2b-110">Duração mínima de tíquetes</span><span class="sxs-lookup"><span data-stu-id="e5c2b-110">Min-Ticket-Age</span></span>                       |
| <span data-ttu-id="e5c2b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e5c2b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e5c2b-112">minTicketAge</span><span class="sxs-lookup"><span data-stu-id="e5c2b-112">minTicketAge</span></span>                         |
| <span data-ttu-id="e5c2b-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e5c2b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="e5c2b-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e5c2b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e5c2b-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e5c2b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e5c2b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-116">Attribute-Id</span></span>      | <span data-ttu-id="e5c2b-117">1.2.840.113556.1.4.80</span><span class="sxs-lookup"><span data-stu-id="e5c2b-117">1.2.840.113556.1.4.80</span></span>                |
| <span data-ttu-id="e5c2b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e5c2b-118">System-Id-Guid</span></span>    | <span data-ttu-id="e5c2b-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e5c2b-119">bf9679c4-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e5c2b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5c2b-120">Syntax</span></span>            | [<span data-ttu-id="e5c2b-121">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-121">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e5c2b-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="e5c2b-122">Implementations</span></span>

-   [<span data-ttu-id="e5c2b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e5c2b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e5c2b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e5c2b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e5c2b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e5c2b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e5c2b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5c2b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e5c2b-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-130">Entry</span></span> | <span data-ttu-id="e5c2b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e5c2b-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="e5c2b-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5c2b-134">System-Only</span></span>            | <span data-ttu-id="e5c2b-135">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-135">False</span></span>                                              |
| <span data-ttu-id="e5c2b-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e5c2b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e5c2b-137">True</span><span class="sxs-lookup"><span data-stu-id="e5c2b-137">True</span></span>                                               |
| <span data-ttu-id="e5c2b-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="e5c2b-138">Is Indexed</span></span>             | <span data-ttu-id="e5c2b-139">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-139">False</span></span>                                              |
| <span data-ttu-id="e5c2b-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5c2b-140">In Global Catalog</span></span>      | <span data-ttu-id="e5c2b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-141">False</span></span>                                              |
| <span data-ttu-id="e5c2b-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5c2b-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e5c2b-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e5c2b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5c2b-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5c2b-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-146">Search-Flags</span></span>           | <span data-ttu-id="e5c2b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5c2b-147">0x00000000</span></span>                                         |
| <span data-ttu-id="e5c2b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-148">System-Flags</span></span>           | <span data-ttu-id="e5c2b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5c2b-149">0x00000010</span></span>                                         |
| <span data-ttu-id="e5c2b-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e5c2b-150">Classes used in</span></span>        | [<span data-ttu-id="e5c2b-151">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e5c2b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5c2b-152">Windows Server 2003</span></span>



| <span data-ttu-id="e5c2b-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-153">Entry</span></span> | <span data-ttu-id="e5c2b-154">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e5c2b-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="e5c2b-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5c2b-157">System-Only</span></span>            | <span data-ttu-id="e5c2b-158">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-158">False</span></span>                                              |
| <span data-ttu-id="e5c2b-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e5c2b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="e5c2b-160">True</span><span class="sxs-lookup"><span data-stu-id="e5c2b-160">True</span></span>                                               |
| <span data-ttu-id="e5c2b-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="e5c2b-161">Is Indexed</span></span>             | <span data-ttu-id="e5c2b-162">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-162">False</span></span>                                              |
| <span data-ttu-id="e5c2b-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5c2b-163">In Global Catalog</span></span>      | <span data-ttu-id="e5c2b-164">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-164">False</span></span>                                              |
| <span data-ttu-id="e5c2b-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5c2b-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e5c2b-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e5c2b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5c2b-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5c2b-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-169">Search-Flags</span></span>           | <span data-ttu-id="e5c2b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5c2b-170">0x00000000</span></span>                                         |
| <span data-ttu-id="e5c2b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-171">System-Flags</span></span>           | <span data-ttu-id="e5c2b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5c2b-172">0x00000010</span></span>                                         |
| <span data-ttu-id="e5c2b-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e5c2b-173">Classes used in</span></span>        | [<span data-ttu-id="e5c2b-174">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e5c2b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e5c2b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e5c2b-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-176">Entry</span></span> | <span data-ttu-id="e5c2b-177">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e5c2b-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="e5c2b-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5c2b-180">System-Only</span></span>            | <span data-ttu-id="e5c2b-181">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-181">False</span></span>                                              |
| <span data-ttu-id="e5c2b-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e5c2b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="e5c2b-183">True</span><span class="sxs-lookup"><span data-stu-id="e5c2b-183">True</span></span>                                               |
| <span data-ttu-id="e5c2b-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="e5c2b-184">Is Indexed</span></span>             | <span data-ttu-id="e5c2b-185">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-185">False</span></span>                                              |
| <span data-ttu-id="e5c2b-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5c2b-186">In Global Catalog</span></span>      | <span data-ttu-id="e5c2b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-187">False</span></span>                                              |
| <span data-ttu-id="e5c2b-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5c2b-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e5c2b-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e5c2b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5c2b-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5c2b-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-192">Search-Flags</span></span>           | <span data-ttu-id="e5c2b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5c2b-193">0x00000000</span></span>                                         |
| <span data-ttu-id="e5c2b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-194">System-Flags</span></span>           | <span data-ttu-id="e5c2b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5c2b-195">0x00000010</span></span>                                         |
| <span data-ttu-id="e5c2b-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e5c2b-196">Classes used in</span></span>        | [<span data-ttu-id="e5c2b-197">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e5c2b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5c2b-198">Windows Server 2008</span></span>



| <span data-ttu-id="e5c2b-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-199">Entry</span></span> | <span data-ttu-id="e5c2b-200">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e5c2b-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="e5c2b-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5c2b-203">System-Only</span></span>            | <span data-ttu-id="e5c2b-204">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-204">False</span></span>                                              |
| <span data-ttu-id="e5c2b-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e5c2b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="e5c2b-206">True</span><span class="sxs-lookup"><span data-stu-id="e5c2b-206">True</span></span>                                               |
| <span data-ttu-id="e5c2b-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="e5c2b-207">Is Indexed</span></span>             | <span data-ttu-id="e5c2b-208">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-208">False</span></span>                                              |
| <span data-ttu-id="e5c2b-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5c2b-209">In Global Catalog</span></span>      | <span data-ttu-id="e5c2b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-210">False</span></span>                                              |
| <span data-ttu-id="e5c2b-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5c2b-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e5c2b-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e5c2b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5c2b-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5c2b-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-215">Search-Flags</span></span>           | <span data-ttu-id="e5c2b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5c2b-216">0x00000000</span></span>                                         |
| <span data-ttu-id="e5c2b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-217">System-Flags</span></span>           | <span data-ttu-id="e5c2b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5c2b-218">0x00000010</span></span>                                         |
| <span data-ttu-id="e5c2b-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e5c2b-219">Classes used in</span></span>        | [<span data-ttu-id="e5c2b-220">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e5c2b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5c2b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e5c2b-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-222">Entry</span></span> | <span data-ttu-id="e5c2b-223">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e5c2b-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="e5c2b-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5c2b-226">System-Only</span></span>            | <span data-ttu-id="e5c2b-227">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-227">False</span></span>                                              |
| <span data-ttu-id="e5c2b-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e5c2b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="e5c2b-229">True</span><span class="sxs-lookup"><span data-stu-id="e5c2b-229">True</span></span>                                               |
| <span data-ttu-id="e5c2b-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="e5c2b-230">Is Indexed</span></span>             | <span data-ttu-id="e5c2b-231">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-231">False</span></span>                                              |
| <span data-ttu-id="e5c2b-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5c2b-232">In Global Catalog</span></span>      | <span data-ttu-id="e5c2b-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-233">False</span></span>                                              |
| <span data-ttu-id="e5c2b-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5c2b-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e5c2b-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e5c2b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5c2b-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5c2b-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-238">Search-Flags</span></span>           | <span data-ttu-id="e5c2b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5c2b-239">0x00000000</span></span>                                         |
| <span data-ttu-id="e5c2b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-240">System-Flags</span></span>           | <span data-ttu-id="e5c2b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5c2b-241">0x00000010</span></span>                                         |
| <span data-ttu-id="e5c2b-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e5c2b-242">Classes used in</span></span>        | [<span data-ttu-id="e5c2b-243">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e5c2b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5c2b-244">Windows Server 2012</span></span>



| <span data-ttu-id="e5c2b-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5c2b-245">Entry</span></span> | <span data-ttu-id="e5c2b-246">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="e5c2b-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="e5c2b-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5c2b-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="e5c2b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5c2b-249">System-Only</span></span>            | <span data-ttu-id="e5c2b-250">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-250">False</span></span>                                              |
| <span data-ttu-id="e5c2b-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e5c2b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="e5c2b-252">True</span><span class="sxs-lookup"><span data-stu-id="e5c2b-252">True</span></span>                                               |
| <span data-ttu-id="e5c2b-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="e5c2b-253">Is Indexed</span></span>             | <span data-ttu-id="e5c2b-254">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-254">False</span></span>                                              |
| <span data-ttu-id="e5c2b-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5c2b-255">In Global Catalog</span></span>      | <span data-ttu-id="e5c2b-256">Falso</span><span class="sxs-lookup"><span data-stu-id="e5c2b-256">False</span></span>                                              |
| <span data-ttu-id="e5c2b-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e5c2b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5c2b-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e5c2b-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="e5c2b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5c2b-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5c2b-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="e5c2b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-261">Search-Flags</span></span>           | <span data-ttu-id="e5c2b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5c2b-262">0x00000000</span></span>                                         |
| <span data-ttu-id="e5c2b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5c2b-263">System-Flags</span></span>           | <span data-ttu-id="e5c2b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5c2b-264">0x00000010</span></span>                                         |
| <span data-ttu-id="e5c2b-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e5c2b-265">Classes used in</span></span>        | [<span data-ttu-id="e5c2b-266">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="e5c2b-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





