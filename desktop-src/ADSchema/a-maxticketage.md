---
title: Atributo Max-ticket-age
description: Esse atributo determina a quantidade máxima de tempo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para a finalidade da autenticação Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo Max-ticket-age
- Esquema de AD do atributo maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645361"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="32066-105">Atributo Max-ticket-age</span><span class="sxs-lookup"><span data-stu-id="32066-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="32066-106">Esse atributo determina a quantidade máxima de tempo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para a finalidade da autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="32066-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="32066-107">Quando o TGT de um usuário expira, um novo deve ser solicitado ou o existente deve ser renovado.</span><span class="sxs-lookup"><span data-stu-id="32066-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="32066-108">Por padrão, essa configuração é definida como 10 horas no objeto de Política de Grupo de domínio padrão (GPO).</span><span class="sxs-lookup"><span data-stu-id="32066-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="32066-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-109">Entry</span></span> | <span data-ttu-id="32066-110">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="32066-111">CN</span><span class="sxs-lookup"><span data-stu-id="32066-111">CN</span></span>                | <span data-ttu-id="32066-112">Duração máxima de tíquetes</span><span class="sxs-lookup"><span data-stu-id="32066-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="32066-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="32066-113">Ldap-Display-Name</span></span> | <span data-ttu-id="32066-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="32066-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="32066-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="32066-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="32066-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="32066-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="32066-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="32066-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="32066-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32066-118">Attribute-Id</span></span>      | <span data-ttu-id="32066-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="32066-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="32066-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="32066-120">System-Id-Guid</span></span>    | <span data-ttu-id="32066-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="32066-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="32066-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32066-122">Syntax</span></span>            | [<span data-ttu-id="32066-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="32066-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="32066-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="32066-124">Implementations</span></span>

-   [<span data-ttu-id="32066-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="32066-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="32066-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="32066-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="32066-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="32066-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="32066-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32066-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32066-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32066-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32066-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32066-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="32066-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32066-131">Windows 2000 Server</span></span>



| <span data-ttu-id="32066-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-132">Entry</span></span> | <span data-ttu-id="32066-133">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="32066-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="32066-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32066-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="32066-136">System-Only</span></span>            | <span data-ttu-id="32066-137">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-137">False</span></span>                                              |
| <span data-ttu-id="32066-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32066-138">Is-Single-Valued</span></span>       | <span data-ttu-id="32066-139">True</span><span class="sxs-lookup"><span data-stu-id="32066-139">True</span></span>                                               |
| <span data-ttu-id="32066-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="32066-140">Is Indexed</span></span>             | <span data-ttu-id="32066-141">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-141">False</span></span>                                              |
| <span data-ttu-id="32066-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32066-142">In Global Catalog</span></span>      | <span data-ttu-id="32066-143">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-143">False</span></span>                                              |
| <span data-ttu-id="32066-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32066-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="32066-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32066-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="32066-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32066-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="32066-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32066-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="32066-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-148">Search-Flags</span></span>           | <span data-ttu-id="32066-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32066-149">0x00000000</span></span>                                         |
| <span data-ttu-id="32066-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-150">System-Flags</span></span>           | <span data-ttu-id="32066-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32066-151">0x00000010</span></span>                                         |
| <span data-ttu-id="32066-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32066-152">Classes used in</span></span>        | [<span data-ttu-id="32066-153">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="32066-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="32066-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32066-154">Windows Server 2003</span></span>



| <span data-ttu-id="32066-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-155">Entry</span></span> | <span data-ttu-id="32066-156">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="32066-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="32066-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32066-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="32066-159">System-Only</span></span>            | <span data-ttu-id="32066-160">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-160">False</span></span>                                              |
| <span data-ttu-id="32066-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32066-161">Is-Single-Valued</span></span>       | <span data-ttu-id="32066-162">True</span><span class="sxs-lookup"><span data-stu-id="32066-162">True</span></span>                                               |
| <span data-ttu-id="32066-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="32066-163">Is Indexed</span></span>             | <span data-ttu-id="32066-164">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-164">False</span></span>                                              |
| <span data-ttu-id="32066-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32066-165">In Global Catalog</span></span>      | <span data-ttu-id="32066-166">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-166">False</span></span>                                              |
| <span data-ttu-id="32066-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32066-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="32066-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32066-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="32066-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32066-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="32066-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32066-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="32066-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-171">Search-Flags</span></span>           | <span data-ttu-id="32066-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32066-172">0x00000000</span></span>                                         |
| <span data-ttu-id="32066-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-173">System-Flags</span></span>           | <span data-ttu-id="32066-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32066-174">0x00000010</span></span>                                         |
| <span data-ttu-id="32066-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32066-175">Classes used in</span></span>        | [<span data-ttu-id="32066-176">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="32066-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="32066-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="32066-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="32066-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-178">Entry</span></span> | <span data-ttu-id="32066-179">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="32066-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="32066-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32066-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="32066-182">System-Only</span></span>            | <span data-ttu-id="32066-183">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-183">False</span></span>                                              |
| <span data-ttu-id="32066-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32066-184">Is-Single-Valued</span></span>       | <span data-ttu-id="32066-185">True</span><span class="sxs-lookup"><span data-stu-id="32066-185">True</span></span>                                               |
| <span data-ttu-id="32066-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="32066-186">Is Indexed</span></span>             | <span data-ttu-id="32066-187">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-187">False</span></span>                                              |
| <span data-ttu-id="32066-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32066-188">In Global Catalog</span></span>      | <span data-ttu-id="32066-189">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-189">False</span></span>                                              |
| <span data-ttu-id="32066-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32066-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="32066-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32066-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="32066-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32066-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="32066-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32066-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="32066-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-194">Search-Flags</span></span>           | <span data-ttu-id="32066-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32066-195">0x00000000</span></span>                                         |
| <span data-ttu-id="32066-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-196">System-Flags</span></span>           | <span data-ttu-id="32066-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32066-197">0x00000010</span></span>                                         |
| <span data-ttu-id="32066-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32066-198">Classes used in</span></span>        | [<span data-ttu-id="32066-199">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="32066-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="32066-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32066-200">Windows Server 2008</span></span>



| <span data-ttu-id="32066-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-201">Entry</span></span> | <span data-ttu-id="32066-202">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="32066-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="32066-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32066-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="32066-205">System-Only</span></span>            | <span data-ttu-id="32066-206">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-206">False</span></span>                                              |
| <span data-ttu-id="32066-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32066-207">Is-Single-Valued</span></span>       | <span data-ttu-id="32066-208">True</span><span class="sxs-lookup"><span data-stu-id="32066-208">True</span></span>                                               |
| <span data-ttu-id="32066-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="32066-209">Is Indexed</span></span>             | <span data-ttu-id="32066-210">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-210">False</span></span>                                              |
| <span data-ttu-id="32066-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32066-211">In Global Catalog</span></span>      | <span data-ttu-id="32066-212">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-212">False</span></span>                                              |
| <span data-ttu-id="32066-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32066-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="32066-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32066-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="32066-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32066-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="32066-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32066-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="32066-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-217">Search-Flags</span></span>           | <span data-ttu-id="32066-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32066-218">0x00000000</span></span>                                         |
| <span data-ttu-id="32066-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-219">System-Flags</span></span>           | <span data-ttu-id="32066-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32066-220">0x00000010</span></span>                                         |
| <span data-ttu-id="32066-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32066-221">Classes used in</span></span>        | [<span data-ttu-id="32066-222">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="32066-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32066-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32066-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32066-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-224">Entry</span></span> | <span data-ttu-id="32066-225">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="32066-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="32066-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32066-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="32066-228">System-Only</span></span>            | <span data-ttu-id="32066-229">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-229">False</span></span>                                              |
| <span data-ttu-id="32066-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32066-230">Is-Single-Valued</span></span>       | <span data-ttu-id="32066-231">True</span><span class="sxs-lookup"><span data-stu-id="32066-231">True</span></span>                                               |
| <span data-ttu-id="32066-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="32066-232">Is Indexed</span></span>             | <span data-ttu-id="32066-233">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-233">False</span></span>                                              |
| <span data-ttu-id="32066-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32066-234">In Global Catalog</span></span>      | <span data-ttu-id="32066-235">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-235">False</span></span>                                              |
| <span data-ttu-id="32066-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32066-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="32066-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32066-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="32066-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32066-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="32066-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32066-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="32066-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-240">Search-Flags</span></span>           | <span data-ttu-id="32066-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32066-241">0x00000000</span></span>                                         |
| <span data-ttu-id="32066-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-242">System-Flags</span></span>           | <span data-ttu-id="32066-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32066-243">0x00000010</span></span>                                         |
| <span data-ttu-id="32066-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32066-244">Classes used in</span></span>        | [<span data-ttu-id="32066-245">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="32066-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32066-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32066-246">Windows Server 2012</span></span>



| <span data-ttu-id="32066-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="32066-247">Entry</span></span> | <span data-ttu-id="32066-248">Valor</span><span class="sxs-lookup"><span data-stu-id="32066-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="32066-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="32066-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32066-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="32066-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="32066-251">System-Only</span></span>            | <span data-ttu-id="32066-252">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-252">False</span></span>                                              |
| <span data-ttu-id="32066-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="32066-253">Is-Single-Valued</span></span>       | <span data-ttu-id="32066-254">True</span><span class="sxs-lookup"><span data-stu-id="32066-254">True</span></span>                                               |
| <span data-ttu-id="32066-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="32066-255">Is Indexed</span></span>             | <span data-ttu-id="32066-256">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-256">False</span></span>                                              |
| <span data-ttu-id="32066-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="32066-257">In Global Catalog</span></span>      | <span data-ttu-id="32066-258">Falso</span><span class="sxs-lookup"><span data-stu-id="32066-258">False</span></span>                                              |
| <span data-ttu-id="32066-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="32066-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="32066-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="32066-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="32066-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32066-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="32066-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32066-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="32066-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-263">Search-Flags</span></span>           | <span data-ttu-id="32066-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32066-264">0x00000000</span></span>                                         |
| <span data-ttu-id="32066-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32066-265">System-Flags</span></span>           | <span data-ttu-id="32066-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32066-266">0x00000010</span></span>                                         |
| <span data-ttu-id="32066-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="32066-267">Classes used in</span></span>        | [<span data-ttu-id="32066-268">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="32066-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





