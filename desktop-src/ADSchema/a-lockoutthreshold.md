---
title: Lockout-Threshold atributo
description: O número de tentativas de logon inválidas permitidas antes que a conta seja bloqueada.
ms.assetid: c4dcbbb6-0680-45f3-9b0b-f9c4bbf2b349
ms.tgt_platform: multiple
keywords:
- Esquema de Lockout-Threshold do atributo AD
- Esquema de AD do atributo lockoutThreshold
topic_type:
- apiref
api_name:
- Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345977055597c48d70e30a20ce9bfbc9f07f3929
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824986"
---
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="3f170-105">Lockout-Threshold atributo</span><span class="sxs-lookup"><span data-stu-id="3f170-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="3f170-106">O número de tentativas de logon inválidas permitidas antes que a conta seja bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3f170-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="3f170-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-107">Entry</span></span> | <span data-ttu-id="3f170-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3f170-109">CN</span><span class="sxs-lookup"><span data-stu-id="3f170-109">CN</span></span>                | <span data-ttu-id="3f170-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="3f170-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="3f170-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3f170-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3f170-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="3f170-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="3f170-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3f170-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="3f170-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3f170-114">Update Privilege</span></span>  | <span data-ttu-id="3f170-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="3f170-115">Domain administrator</span></span>                 |
| <span data-ttu-id="3f170-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3f170-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3f170-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-117">Attribute-Id</span></span>      | <span data-ttu-id="3f170-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="3f170-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="3f170-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3f170-119">System-Id-Guid</span></span>    | <span data-ttu-id="3f170-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3f170-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3f170-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f170-121">Syntax</span></span>            | [<span data-ttu-id="3f170-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="3f170-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="3f170-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="3f170-123">Implementations</span></span>

-   [<span data-ttu-id="3f170-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3f170-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3f170-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3f170-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3f170-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3f170-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3f170-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f170-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f170-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f170-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f170-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f170-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3f170-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f170-130">Windows 2000 Server</span></span>



| <span data-ttu-id="3f170-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-131">Entry</span></span> | <span data-ttu-id="3f170-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f170-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f170-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f170-135">System-Only</span></span>            | <span data-ttu-id="3f170-136">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f170-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3f170-138">True</span><span class="sxs-lookup"><span data-stu-id="3f170-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="3f170-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f170-139">Is Indexed</span></span>             | <span data-ttu-id="3f170-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f170-141">In Global Catalog</span></span>      | <span data-ttu-id="3f170-142">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f170-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f170-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f170-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="3f170-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f170-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f170-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-147">Search-Flags</span></span>           | <span data-ttu-id="3f170-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f170-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-149">System-Flags</span></span>           | <span data-ttu-id="3f170-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f170-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f170-151">Classes used in</span></span>        | [<span data-ttu-id="3f170-152">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="3f170-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="3f170-154">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="3f170-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3f170-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f170-155">Windows Server 2003</span></span>



| <span data-ttu-id="3f170-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-156">Entry</span></span> | <span data-ttu-id="3f170-157">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f170-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f170-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f170-160">System-Only</span></span>            | <span data-ttu-id="3f170-161">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f170-162">Is-Single-Valued</span></span>       | <span data-ttu-id="3f170-163">True</span><span class="sxs-lookup"><span data-stu-id="3f170-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="3f170-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f170-164">Is Indexed</span></span>             | <span data-ttu-id="3f170-165">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f170-166">In Global Catalog</span></span>      | <span data-ttu-id="3f170-167">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f170-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f170-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f170-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="3f170-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f170-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f170-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-172">Search-Flags</span></span>           | <span data-ttu-id="3f170-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f170-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-174">System-Flags</span></span>           | <span data-ttu-id="3f170-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f170-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f170-176">Classes used in</span></span>        | [<span data-ttu-id="3f170-177">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="3f170-178">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="3f170-179">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="3f170-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3f170-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3f170-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3f170-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-181">Entry</span></span> | <span data-ttu-id="3f170-182">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f170-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f170-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f170-185">System-Only</span></span>            | <span data-ttu-id="3f170-186">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f170-187">Is-Single-Valued</span></span>       | <span data-ttu-id="3f170-188">True</span><span class="sxs-lookup"><span data-stu-id="3f170-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="3f170-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f170-189">Is Indexed</span></span>             | <span data-ttu-id="3f170-190">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f170-191">In Global Catalog</span></span>      | <span data-ttu-id="3f170-192">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f170-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f170-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f170-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="3f170-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f170-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f170-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-197">Search-Flags</span></span>           | <span data-ttu-id="3f170-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f170-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-199">System-Flags</span></span>           | <span data-ttu-id="3f170-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f170-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f170-201">Classes used in</span></span>        | [<span data-ttu-id="3f170-202">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="3f170-203">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="3f170-204">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="3f170-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3f170-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f170-205">Windows Server 2008</span></span>



| <span data-ttu-id="3f170-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-206">Entry</span></span> | <span data-ttu-id="3f170-207">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f170-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f170-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f170-210">System-Only</span></span>            | <span data-ttu-id="3f170-211">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f170-212">Is-Single-Valued</span></span>       | <span data-ttu-id="3f170-213">True</span><span class="sxs-lookup"><span data-stu-id="3f170-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="3f170-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f170-214">Is Indexed</span></span>             | <span data-ttu-id="3f170-215">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f170-216">In Global Catalog</span></span>      | <span data-ttu-id="3f170-217">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f170-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f170-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f170-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="3f170-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f170-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f170-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-222">Search-Flags</span></span>           | <span data-ttu-id="3f170-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f170-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-224">System-Flags</span></span>           | <span data-ttu-id="3f170-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f170-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f170-226">Classes used in</span></span>        | [<span data-ttu-id="3f170-227">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="3f170-228">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="3f170-229">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="3f170-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f170-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f170-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f170-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-231">Entry</span></span> | <span data-ttu-id="3f170-232">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f170-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f170-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f170-235">System-Only</span></span>            | <span data-ttu-id="3f170-236">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f170-237">Is-Single-Valued</span></span>       | <span data-ttu-id="3f170-238">True</span><span class="sxs-lookup"><span data-stu-id="3f170-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="3f170-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f170-239">Is Indexed</span></span>             | <span data-ttu-id="3f170-240">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f170-241">In Global Catalog</span></span>      | <span data-ttu-id="3f170-242">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f170-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f170-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f170-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="3f170-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f170-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f170-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-247">Search-Flags</span></span>           | <span data-ttu-id="3f170-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f170-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-249">System-Flags</span></span>           | <span data-ttu-id="3f170-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f170-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f170-251">Classes used in</span></span>        | [<span data-ttu-id="3f170-252">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="3f170-253">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="3f170-254">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="3f170-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3f170-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f170-255">Windows Server 2012</span></span>



| <span data-ttu-id="3f170-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f170-256">Entry</span></span> | <span data-ttu-id="3f170-257">Valor</span><span class="sxs-lookup"><span data-stu-id="3f170-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f170-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f170-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f170-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f170-260">System-Only</span></span>            | <span data-ttu-id="3f170-261">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f170-262">Is-Single-Valued</span></span>       | <span data-ttu-id="3f170-263">True</span><span class="sxs-lookup"><span data-stu-id="3f170-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="3f170-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f170-264">Is Indexed</span></span>             | <span data-ttu-id="3f170-265">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f170-266">In Global Catalog</span></span>      | <span data-ttu-id="3f170-267">Falso</span><span class="sxs-lookup"><span data-stu-id="3f170-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="3f170-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f170-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f170-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f170-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="3f170-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f170-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f170-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="3f170-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-272">Search-Flags</span></span>           | <span data-ttu-id="3f170-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f170-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f170-274">System-Flags</span></span>           | <span data-ttu-id="3f170-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3f170-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="3f170-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f170-276">Classes used in</span></span>        | [<span data-ttu-id="3f170-277">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="3f170-278">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="3f170-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="3f170-279">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="3f170-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="3f170-280">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f170-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f170-281">**Duração do bloqueio**</span><span class="sxs-lookup"><span data-stu-id="3f170-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





