---
title: Atributo Max-Renew-age
description: Esse atributo determina o período de tempo, em dias, durante o qual o tíquete de concessão de tíquete (TGT) de um usuário pode ser renovado para fins de autenticação Kerberos. A configuração padrão é 7 dias no objeto de Política de Grupo de domínio padrão (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- Esquema de anúncio de atributo Max-Renew-age
- Esquema de AD do atributo maxRenewAge
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756487"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="294d1-106">Atributo Max-Renew-age</span><span class="sxs-lookup"><span data-stu-id="294d1-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="294d1-107">Esse atributo determina o período de tempo, em dias, durante o qual o tíquete de concessão de tíquete (TGT) de um usuário pode ser renovado para fins de autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="294d1-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="294d1-108">A configuração padrão é 7 dias no objeto de Política de Grupo de domínio padrão (GPO).</span><span class="sxs-lookup"><span data-stu-id="294d1-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="294d1-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-109">Entry</span></span> | <span data-ttu-id="294d1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="294d1-111">CN</span><span class="sxs-lookup"><span data-stu-id="294d1-111">CN</span></span>                | <span data-ttu-id="294d1-112">Max-Renew-age</span><span class="sxs-lookup"><span data-stu-id="294d1-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="294d1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="294d1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="294d1-114">maxRenewAge</span><span class="sxs-lookup"><span data-stu-id="294d1-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="294d1-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="294d1-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="294d1-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="294d1-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="294d1-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="294d1-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="294d1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-118">Attribute-Id</span></span>      | <span data-ttu-id="294d1-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="294d1-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="294d1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="294d1-120">System-Id-Guid</span></span>    | <span data-ttu-id="294d1-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="294d1-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="294d1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="294d1-122">Syntax</span></span>            | [<span data-ttu-id="294d1-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="294d1-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="294d1-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="294d1-124">Implementations</span></span>

-   [<span data-ttu-id="294d1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="294d1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="294d1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="294d1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="294d1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="294d1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="294d1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="294d1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="294d1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="294d1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="294d1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="294d1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="294d1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="294d1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="294d1-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-132">Entry</span></span> | <span data-ttu-id="294d1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="294d1-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="294d1-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="294d1-136">System-Only</span></span>            | <span data-ttu-id="294d1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-137">False</span></span>                                              |
| <span data-ttu-id="294d1-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="294d1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="294d1-139">True</span><span class="sxs-lookup"><span data-stu-id="294d1-139">True</span></span>                                               |
| <span data-ttu-id="294d1-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="294d1-140">Is Indexed</span></span>             | <span data-ttu-id="294d1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-141">False</span></span>                                              |
| <span data-ttu-id="294d1-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="294d1-142">In Global Catalog</span></span>      | <span data-ttu-id="294d1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-143">False</span></span>                                              |
| <span data-ttu-id="294d1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="294d1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="294d1-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="294d1-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="294d1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294d1-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294d1-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-148">Search-Flags</span></span>           | <span data-ttu-id="294d1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294d1-149">0x00000000</span></span>                                         |
| <span data-ttu-id="294d1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-150">System-Flags</span></span>           | <span data-ttu-id="294d1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294d1-151">0x00000010</span></span>                                         |
| <span data-ttu-id="294d1-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="294d1-152">Classes used in</span></span>        | [<span data-ttu-id="294d1-153">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="294d1-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="294d1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="294d1-154">Windows Server 2003</span></span>



| <span data-ttu-id="294d1-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-155">Entry</span></span> | <span data-ttu-id="294d1-156">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="294d1-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="294d1-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="294d1-159">System-Only</span></span>            | <span data-ttu-id="294d1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-160">False</span></span>                                              |
| <span data-ttu-id="294d1-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="294d1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="294d1-162">True</span><span class="sxs-lookup"><span data-stu-id="294d1-162">True</span></span>                                               |
| <span data-ttu-id="294d1-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="294d1-163">Is Indexed</span></span>             | <span data-ttu-id="294d1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-164">False</span></span>                                              |
| <span data-ttu-id="294d1-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="294d1-165">In Global Catalog</span></span>      | <span data-ttu-id="294d1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-166">False</span></span>                                              |
| <span data-ttu-id="294d1-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="294d1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="294d1-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="294d1-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="294d1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294d1-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294d1-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-171">Search-Flags</span></span>           | <span data-ttu-id="294d1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294d1-172">0x00000000</span></span>                                         |
| <span data-ttu-id="294d1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-173">System-Flags</span></span>           | <span data-ttu-id="294d1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294d1-174">0x00000010</span></span>                                         |
| <span data-ttu-id="294d1-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="294d1-175">Classes used in</span></span>        | [<span data-ttu-id="294d1-176">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="294d1-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="294d1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="294d1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="294d1-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-178">Entry</span></span> | <span data-ttu-id="294d1-179">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="294d1-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="294d1-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="294d1-182">System-Only</span></span>            | <span data-ttu-id="294d1-183">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-183">False</span></span>                                              |
| <span data-ttu-id="294d1-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="294d1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="294d1-185">True</span><span class="sxs-lookup"><span data-stu-id="294d1-185">True</span></span>                                               |
| <span data-ttu-id="294d1-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="294d1-186">Is Indexed</span></span>             | <span data-ttu-id="294d1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-187">False</span></span>                                              |
| <span data-ttu-id="294d1-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="294d1-188">In Global Catalog</span></span>      | <span data-ttu-id="294d1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-189">False</span></span>                                              |
| <span data-ttu-id="294d1-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="294d1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="294d1-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="294d1-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="294d1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294d1-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294d1-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-194">Search-Flags</span></span>           | <span data-ttu-id="294d1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294d1-195">0x00000000</span></span>                                         |
| <span data-ttu-id="294d1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-196">System-Flags</span></span>           | <span data-ttu-id="294d1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294d1-197">0x00000010</span></span>                                         |
| <span data-ttu-id="294d1-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="294d1-198">Classes used in</span></span>        | [<span data-ttu-id="294d1-199">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="294d1-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="294d1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="294d1-200">Windows Server 2008</span></span>



| <span data-ttu-id="294d1-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-201">Entry</span></span> | <span data-ttu-id="294d1-202">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="294d1-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="294d1-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="294d1-205">System-Only</span></span>            | <span data-ttu-id="294d1-206">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-206">False</span></span>                                              |
| <span data-ttu-id="294d1-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="294d1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="294d1-208">True</span><span class="sxs-lookup"><span data-stu-id="294d1-208">True</span></span>                                               |
| <span data-ttu-id="294d1-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="294d1-209">Is Indexed</span></span>             | <span data-ttu-id="294d1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-210">False</span></span>                                              |
| <span data-ttu-id="294d1-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="294d1-211">In Global Catalog</span></span>      | <span data-ttu-id="294d1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-212">False</span></span>                                              |
| <span data-ttu-id="294d1-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="294d1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="294d1-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="294d1-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="294d1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294d1-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294d1-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-217">Search-Flags</span></span>           | <span data-ttu-id="294d1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294d1-218">0x00000000</span></span>                                         |
| <span data-ttu-id="294d1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-219">System-Flags</span></span>           | <span data-ttu-id="294d1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294d1-220">0x00000010</span></span>                                         |
| <span data-ttu-id="294d1-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="294d1-221">Classes used in</span></span>        | [<span data-ttu-id="294d1-222">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="294d1-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="294d1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="294d1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="294d1-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-224">Entry</span></span> | <span data-ttu-id="294d1-225">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="294d1-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="294d1-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="294d1-228">System-Only</span></span>            | <span data-ttu-id="294d1-229">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-229">False</span></span>                                              |
| <span data-ttu-id="294d1-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="294d1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="294d1-231">True</span><span class="sxs-lookup"><span data-stu-id="294d1-231">True</span></span>                                               |
| <span data-ttu-id="294d1-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="294d1-232">Is Indexed</span></span>             | <span data-ttu-id="294d1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-233">False</span></span>                                              |
| <span data-ttu-id="294d1-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="294d1-234">In Global Catalog</span></span>      | <span data-ttu-id="294d1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-235">False</span></span>                                              |
| <span data-ttu-id="294d1-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="294d1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="294d1-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="294d1-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="294d1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294d1-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294d1-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-240">Search-Flags</span></span>           | <span data-ttu-id="294d1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294d1-241">0x00000000</span></span>                                         |
| <span data-ttu-id="294d1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-242">System-Flags</span></span>           | <span data-ttu-id="294d1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294d1-243">0x00000010</span></span>                                         |
| <span data-ttu-id="294d1-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="294d1-244">Classes used in</span></span>        | [<span data-ttu-id="294d1-245">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="294d1-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="294d1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="294d1-246">Windows Server 2012</span></span>



| <span data-ttu-id="294d1-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="294d1-247">Entry</span></span> | <span data-ttu-id="294d1-248">Valor</span><span class="sxs-lookup"><span data-stu-id="294d1-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="294d1-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="294d1-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294d1-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="294d1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="294d1-251">System-Only</span></span>            | <span data-ttu-id="294d1-252">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-252">False</span></span>                                              |
| <span data-ttu-id="294d1-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="294d1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="294d1-254">True</span><span class="sxs-lookup"><span data-stu-id="294d1-254">True</span></span>                                               |
| <span data-ttu-id="294d1-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="294d1-255">Is Indexed</span></span>             | <span data-ttu-id="294d1-256">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-256">False</span></span>                                              |
| <span data-ttu-id="294d1-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="294d1-257">In Global Catalog</span></span>      | <span data-ttu-id="294d1-258">Falso</span><span class="sxs-lookup"><span data-stu-id="294d1-258">False</span></span>                                              |
| <span data-ttu-id="294d1-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="294d1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="294d1-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="294d1-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="294d1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294d1-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294d1-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="294d1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-263">Search-Flags</span></span>           | <span data-ttu-id="294d1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294d1-264">0x00000000</span></span>                                         |
| <span data-ttu-id="294d1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294d1-265">System-Flags</span></span>           | <span data-ttu-id="294d1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294d1-266">0x00000010</span></span>                                         |
| <span data-ttu-id="294d1-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="294d1-267">Classes used in</span></span>        | [<span data-ttu-id="294d1-268">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="294d1-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





