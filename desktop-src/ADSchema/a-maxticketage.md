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
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="ded5b-105">Atributo Max-ticket-age</span><span class="sxs-lookup"><span data-stu-id="ded5b-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="ded5b-106">Esse atributo determina a quantidade máxima de tempo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para a finalidade da autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ded5b-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="ded5b-107">Quando o TGT de um usuário expira, um novo deve ser solicitado ou o existente deve ser renovado.</span><span class="sxs-lookup"><span data-stu-id="ded5b-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="ded5b-108">Por padrão, essa configuração é definida como 10 horas no objeto de Política de Grupo de domínio padrão (GPO).</span><span class="sxs-lookup"><span data-stu-id="ded5b-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="ded5b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-109">Entry</span></span> | <span data-ttu-id="ded5b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ded5b-111">CN</span><span class="sxs-lookup"><span data-stu-id="ded5b-111">CN</span></span>                | <span data-ttu-id="ded5b-112">Duração máxima de tíquetes</span><span class="sxs-lookup"><span data-stu-id="ded5b-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="ded5b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ded5b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ded5b-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="ded5b-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="ded5b-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ded5b-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="ded5b-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ded5b-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ded5b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ded5b-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ded5b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-118">Attribute-Id</span></span>      | <span data-ttu-id="ded5b-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="ded5b-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="ded5b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ded5b-120">System-Id-Guid</span></span>    | <span data-ttu-id="ded5b-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ded5b-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ded5b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded5b-122">Syntax</span></span>            | [<span data-ttu-id="ded5b-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="ded5b-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ded5b-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="ded5b-124">Implementations</span></span>

-   [<span data-ttu-id="ded5b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ded5b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ded5b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ded5b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ded5b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ded5b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ded5b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ded5b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ded5b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ded5b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ded5b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ded5b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ded5b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ded5b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ded5b-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-132">Entry</span></span> | <span data-ttu-id="ded5b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ded5b-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="ded5b-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded5b-136">System-Only</span></span>            | <span data-ttu-id="ded5b-137">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-137">False</span></span>                                              |
| <span data-ttu-id="ded5b-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ded5b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ded5b-139">True</span><span class="sxs-lookup"><span data-stu-id="ded5b-139">True</span></span>                                               |
| <span data-ttu-id="ded5b-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="ded5b-140">Is Indexed</span></span>             | <span data-ttu-id="ded5b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-141">False</span></span>                                              |
| <span data-ttu-id="ded5b-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ded5b-142">In Global Catalog</span></span>      | <span data-ttu-id="ded5b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-143">False</span></span>                                              |
| <span data-ttu-id="ded5b-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded5b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded5b-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ded5b-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ded5b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded5b-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded5b-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-148">Search-Flags</span></span>           | <span data-ttu-id="ded5b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded5b-149">0x00000000</span></span>                                         |
| <span data-ttu-id="ded5b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-150">System-Flags</span></span>           | <span data-ttu-id="ded5b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded5b-151">0x00000010</span></span>                                         |
| <span data-ttu-id="ded5b-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ded5b-152">Classes used in</span></span>        | [<span data-ttu-id="ded5b-153">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ded5b-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ded5b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ded5b-154">Windows Server 2003</span></span>



| <span data-ttu-id="ded5b-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-155">Entry</span></span> | <span data-ttu-id="ded5b-156">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ded5b-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="ded5b-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded5b-159">System-Only</span></span>            | <span data-ttu-id="ded5b-160">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-160">False</span></span>                                              |
| <span data-ttu-id="ded5b-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ded5b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ded5b-162">True</span><span class="sxs-lookup"><span data-stu-id="ded5b-162">True</span></span>                                               |
| <span data-ttu-id="ded5b-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="ded5b-163">Is Indexed</span></span>             | <span data-ttu-id="ded5b-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-164">False</span></span>                                              |
| <span data-ttu-id="ded5b-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ded5b-165">In Global Catalog</span></span>      | <span data-ttu-id="ded5b-166">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-166">False</span></span>                                              |
| <span data-ttu-id="ded5b-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded5b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded5b-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ded5b-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ded5b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded5b-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded5b-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-171">Search-Flags</span></span>           | <span data-ttu-id="ded5b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded5b-172">0x00000000</span></span>                                         |
| <span data-ttu-id="ded5b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-173">System-Flags</span></span>           | <span data-ttu-id="ded5b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded5b-174">0x00000010</span></span>                                         |
| <span data-ttu-id="ded5b-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ded5b-175">Classes used in</span></span>        | [<span data-ttu-id="ded5b-176">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ded5b-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ded5b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ded5b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ded5b-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-178">Entry</span></span> | <span data-ttu-id="ded5b-179">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ded5b-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="ded5b-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded5b-182">System-Only</span></span>            | <span data-ttu-id="ded5b-183">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-183">False</span></span>                                              |
| <span data-ttu-id="ded5b-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ded5b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ded5b-185">True</span><span class="sxs-lookup"><span data-stu-id="ded5b-185">True</span></span>                                               |
| <span data-ttu-id="ded5b-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="ded5b-186">Is Indexed</span></span>             | <span data-ttu-id="ded5b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-187">False</span></span>                                              |
| <span data-ttu-id="ded5b-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ded5b-188">In Global Catalog</span></span>      | <span data-ttu-id="ded5b-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-189">False</span></span>                                              |
| <span data-ttu-id="ded5b-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded5b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded5b-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ded5b-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ded5b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded5b-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded5b-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-194">Search-Flags</span></span>           | <span data-ttu-id="ded5b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded5b-195">0x00000000</span></span>                                         |
| <span data-ttu-id="ded5b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-196">System-Flags</span></span>           | <span data-ttu-id="ded5b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded5b-197">0x00000010</span></span>                                         |
| <span data-ttu-id="ded5b-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ded5b-198">Classes used in</span></span>        | [<span data-ttu-id="ded5b-199">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ded5b-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ded5b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ded5b-200">Windows Server 2008</span></span>



| <span data-ttu-id="ded5b-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-201">Entry</span></span> | <span data-ttu-id="ded5b-202">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ded5b-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="ded5b-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded5b-205">System-Only</span></span>            | <span data-ttu-id="ded5b-206">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-206">False</span></span>                                              |
| <span data-ttu-id="ded5b-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ded5b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ded5b-208">True</span><span class="sxs-lookup"><span data-stu-id="ded5b-208">True</span></span>                                               |
| <span data-ttu-id="ded5b-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="ded5b-209">Is Indexed</span></span>             | <span data-ttu-id="ded5b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-210">False</span></span>                                              |
| <span data-ttu-id="ded5b-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ded5b-211">In Global Catalog</span></span>      | <span data-ttu-id="ded5b-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-212">False</span></span>                                              |
| <span data-ttu-id="ded5b-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded5b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded5b-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ded5b-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ded5b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded5b-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded5b-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-217">Search-Flags</span></span>           | <span data-ttu-id="ded5b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded5b-218">0x00000000</span></span>                                         |
| <span data-ttu-id="ded5b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-219">System-Flags</span></span>           | <span data-ttu-id="ded5b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded5b-220">0x00000010</span></span>                                         |
| <span data-ttu-id="ded5b-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ded5b-221">Classes used in</span></span>        | [<span data-ttu-id="ded5b-222">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ded5b-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ded5b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ded5b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ded5b-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-224">Entry</span></span> | <span data-ttu-id="ded5b-225">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ded5b-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="ded5b-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded5b-228">System-Only</span></span>            | <span data-ttu-id="ded5b-229">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-229">False</span></span>                                              |
| <span data-ttu-id="ded5b-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ded5b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ded5b-231">True</span><span class="sxs-lookup"><span data-stu-id="ded5b-231">True</span></span>                                               |
| <span data-ttu-id="ded5b-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="ded5b-232">Is Indexed</span></span>             | <span data-ttu-id="ded5b-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-233">False</span></span>                                              |
| <span data-ttu-id="ded5b-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ded5b-234">In Global Catalog</span></span>      | <span data-ttu-id="ded5b-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-235">False</span></span>                                              |
| <span data-ttu-id="ded5b-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded5b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded5b-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ded5b-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ded5b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded5b-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded5b-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-240">Search-Flags</span></span>           | <span data-ttu-id="ded5b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded5b-241">0x00000000</span></span>                                         |
| <span data-ttu-id="ded5b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-242">System-Flags</span></span>           | <span data-ttu-id="ded5b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded5b-243">0x00000010</span></span>                                         |
| <span data-ttu-id="ded5b-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ded5b-244">Classes used in</span></span>        | [<span data-ttu-id="ded5b-245">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ded5b-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ded5b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ded5b-246">Windows Server 2012</span></span>



| <span data-ttu-id="ded5b-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="ded5b-247">Entry</span></span> | <span data-ttu-id="ded5b-248">Valor</span><span class="sxs-lookup"><span data-stu-id="ded5b-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="ded5b-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="ded5b-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded5b-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="ded5b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded5b-251">System-Only</span></span>            | <span data-ttu-id="ded5b-252">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-252">False</span></span>                                              |
| <span data-ttu-id="ded5b-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ded5b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ded5b-254">True</span><span class="sxs-lookup"><span data-stu-id="ded5b-254">True</span></span>                                               |
| <span data-ttu-id="ded5b-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="ded5b-255">Is Indexed</span></span>             | <span data-ttu-id="ded5b-256">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-256">False</span></span>                                              |
| <span data-ttu-id="ded5b-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ded5b-257">In Global Catalog</span></span>      | <span data-ttu-id="ded5b-258">Falso</span><span class="sxs-lookup"><span data-stu-id="ded5b-258">False</span></span>                                              |
| <span data-ttu-id="ded5b-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded5b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded5b-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ded5b-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="ded5b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded5b-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded5b-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="ded5b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-263">Search-Flags</span></span>           | <span data-ttu-id="ded5b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded5b-264">0x00000000</span></span>                                         |
| <span data-ttu-id="ded5b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded5b-265">System-Flags</span></span>           | <span data-ttu-id="ded5b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded5b-266">0x00000010</span></span>                                         |
| <span data-ttu-id="ded5b-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ded5b-267">Classes used in</span></span>        | [<span data-ttu-id="ded5b-268">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="ded5b-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





