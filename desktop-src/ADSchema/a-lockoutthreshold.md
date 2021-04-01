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
# <a name="lockout-threshold-attribute"></a><span data-ttu-id="42a7d-105">Lockout-Threshold atributo</span><span class="sxs-lookup"><span data-stu-id="42a7d-105">Lockout-Threshold attribute</span></span>

<span data-ttu-id="42a7d-106">O número de tentativas de logon inválidas permitidas antes que a conta seja bloqueada.</span><span class="sxs-lookup"><span data-stu-id="42a7d-106">The number of invalid logon attempts that are permitted before the account is locked out.</span></span>



| <span data-ttu-id="42a7d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-107">Entry</span></span> | <span data-ttu-id="42a7d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="42a7d-109">CN</span><span class="sxs-lookup"><span data-stu-id="42a7d-109">CN</span></span>                | <span data-ttu-id="42a7d-110">Lockout-Threshold</span><span class="sxs-lookup"><span data-stu-id="42a7d-110">Lockout-Threshold</span></span>                    |
| <span data-ttu-id="42a7d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="42a7d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="42a7d-112">lockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="42a7d-112">lockoutThreshold</span></span>                     |
| <span data-ttu-id="42a7d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="42a7d-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="42a7d-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="42a7d-114">Update Privilege</span></span>  | <span data-ttu-id="42a7d-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="42a7d-115">Domain administrator</span></span>                 |
| <span data-ttu-id="42a7d-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="42a7d-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="42a7d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-117">Attribute-Id</span></span>      | <span data-ttu-id="42a7d-118">1.2.840.113556.1.4.73</span><span class="sxs-lookup"><span data-stu-id="42a7d-118">1.2.840.113556.1.4.73</span></span>                |
| <span data-ttu-id="42a7d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="42a7d-119">System-Id-Guid</span></span>    | <span data-ttu-id="42a7d-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="42a7d-120">bf9679a6-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="42a7d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a7d-121">Syntax</span></span>            | [<span data-ttu-id="42a7d-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="42a7d-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="42a7d-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="42a7d-123">Implementations</span></span>

-   [<span data-ttu-id="42a7d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42a7d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42a7d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42a7d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42a7d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42a7d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42a7d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42a7d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42a7d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42a7d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42a7d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42a7d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42a7d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42a7d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="42a7d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-131">Entry</span></span> | <span data-ttu-id="42a7d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7d-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="42a7d-133">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-134">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a7d-135">System-Only</span></span>            | <span data-ttu-id="42a7d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-136">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42a7d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="42a7d-138">True</span><span class="sxs-lookup"><span data-stu-id="42a7d-138">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="42a7d-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="42a7d-139">Is Indexed</span></span>             | <span data-ttu-id="42a7d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-140">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42a7d-141">In Global Catalog</span></span>      | <span data-ttu-id="42a7d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-142">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42a7d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a7d-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42a7d-144">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="42a7d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a7d-145">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a7d-146">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-147">Search-Flags</span></span>           | <span data-ttu-id="42a7d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42a7d-148">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-149">System-Flags</span></span>           | <span data-ttu-id="42a7d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a7d-150">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42a7d-151">Classes used in</span></span>        | [<span data-ttu-id="42a7d-152">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="42a7d-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="42a7d-154">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="42a7d-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42a7d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42a7d-155">Windows Server 2003</span></span>



| <span data-ttu-id="42a7d-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-156">Entry</span></span> | <span data-ttu-id="42a7d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7d-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="42a7d-158">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-159">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a7d-160">System-Only</span></span>            | <span data-ttu-id="42a7d-161">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-161">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42a7d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="42a7d-163">True</span><span class="sxs-lookup"><span data-stu-id="42a7d-163">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="42a7d-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="42a7d-164">Is Indexed</span></span>             | <span data-ttu-id="42a7d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-165">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42a7d-166">In Global Catalog</span></span>      | <span data-ttu-id="42a7d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-167">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42a7d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a7d-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42a7d-169">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="42a7d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a7d-170">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a7d-171">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-172">Search-Flags</span></span>           | <span data-ttu-id="42a7d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42a7d-173">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-174">System-Flags</span></span>           | <span data-ttu-id="42a7d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a7d-175">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42a7d-176">Classes used in</span></span>        | [<span data-ttu-id="42a7d-177">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="42a7d-178">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="42a7d-179">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="42a7d-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42a7d-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42a7d-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42a7d-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-181">Entry</span></span> | <span data-ttu-id="42a7d-182">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7d-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="42a7d-183">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-184">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a7d-185">System-Only</span></span>            | <span data-ttu-id="42a7d-186">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-186">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42a7d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="42a7d-188">True</span><span class="sxs-lookup"><span data-stu-id="42a7d-188">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="42a7d-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="42a7d-189">Is Indexed</span></span>             | <span data-ttu-id="42a7d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-190">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42a7d-191">In Global Catalog</span></span>      | <span data-ttu-id="42a7d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-192">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42a7d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a7d-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42a7d-194">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="42a7d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a7d-195">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a7d-196">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-197">Search-Flags</span></span>           | <span data-ttu-id="42a7d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42a7d-198">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-199">System-Flags</span></span>           | <span data-ttu-id="42a7d-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a7d-200">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42a7d-201">Classes used in</span></span>        | [<span data-ttu-id="42a7d-202">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="42a7d-203">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="42a7d-204">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="42a7d-204">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42a7d-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42a7d-205">Windows Server 2008</span></span>



| <span data-ttu-id="42a7d-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-206">Entry</span></span> | <span data-ttu-id="42a7d-207">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-207">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7d-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="42a7d-208">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-209">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a7d-210">System-Only</span></span>            | <span data-ttu-id="42a7d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-211">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42a7d-212">Is-Single-Valued</span></span>       | <span data-ttu-id="42a7d-213">True</span><span class="sxs-lookup"><span data-stu-id="42a7d-213">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="42a7d-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="42a7d-214">Is Indexed</span></span>             | <span data-ttu-id="42a7d-215">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-215">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42a7d-216">In Global Catalog</span></span>      | <span data-ttu-id="42a7d-217">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-217">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42a7d-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a7d-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42a7d-219">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="42a7d-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a7d-220">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a7d-221">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-222">Search-Flags</span></span>           | <span data-ttu-id="42a7d-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42a7d-223">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-224">System-Flags</span></span>           | <span data-ttu-id="42a7d-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a7d-225">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42a7d-226">Classes used in</span></span>        | [<span data-ttu-id="42a7d-227">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="42a7d-228">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="42a7d-229">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="42a7d-229">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42a7d-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42a7d-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42a7d-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-231">Entry</span></span> | <span data-ttu-id="42a7d-232">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-232">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7d-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="42a7d-233">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-234">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a7d-235">System-Only</span></span>            | <span data-ttu-id="42a7d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-236">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42a7d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="42a7d-238">True</span><span class="sxs-lookup"><span data-stu-id="42a7d-238">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="42a7d-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="42a7d-239">Is Indexed</span></span>             | <span data-ttu-id="42a7d-240">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-240">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42a7d-241">In Global Catalog</span></span>      | <span data-ttu-id="42a7d-242">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-242">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42a7d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a7d-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42a7d-244">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="42a7d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a7d-245">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a7d-246">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-247">Search-Flags</span></span>           | <span data-ttu-id="42a7d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42a7d-248">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-249">System-Flags</span></span>           | <span data-ttu-id="42a7d-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a7d-250">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42a7d-251">Classes used in</span></span>        | [<span data-ttu-id="42a7d-252">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="42a7d-253">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="42a7d-254">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="42a7d-254">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42a7d-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42a7d-255">Windows Server 2012</span></span>



| <span data-ttu-id="42a7d-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="42a7d-256">Entry</span></span> | <span data-ttu-id="42a7d-257">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7d-257">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7d-258">ID do link</span><span class="sxs-lookup"><span data-stu-id="42a7d-258">Link-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42a7d-259">MAPI-Id</span></span>                | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="42a7d-260">System-Only</span></span>            | <span data-ttu-id="42a7d-261">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-261">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="42a7d-262">Is-Single-Valued</span></span>       | <span data-ttu-id="42a7d-263">True</span><span class="sxs-lookup"><span data-stu-id="42a7d-263">True</span></span>                                                                                                                                                  |
| <span data-ttu-id="42a7d-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="42a7d-264">Is Indexed</span></span>             | <span data-ttu-id="42a7d-265">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-265">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="42a7d-266">In Global Catalog</span></span>      | <span data-ttu-id="42a7d-267">Falso</span><span class="sxs-lookup"><span data-stu-id="42a7d-267">False</span></span>                                                                                                                                                 |
| <span data-ttu-id="42a7d-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42a7d-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="42a7d-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="42a7d-269">O:BAG:BAD:S:</span></span>                                                                                                                                          |
| <span data-ttu-id="42a7d-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42a7d-270">Range-Lower</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42a7d-271">Range-Upper</span></span>            | \-                                                                                                                                                    |
| <span data-ttu-id="42a7d-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-272">Search-Flags</span></span>           | <span data-ttu-id="42a7d-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42a7d-273">0x00000000</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42a7d-274">System-Flags</span></span>           | <span data-ttu-id="42a7d-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42a7d-275">0x00000010</span></span>                                                                                                                                            |
| <span data-ttu-id="42a7d-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="42a7d-276">Classes used in</span></span>        | [<span data-ttu-id="42a7d-277">**Política de domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="42a7d-278">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="42a7d-279">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="42a7d-279">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="42a7d-280">Confira também</span><span class="sxs-lookup"><span data-stu-id="42a7d-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a7d-281">**Duração do bloqueio**</span><span class="sxs-lookup"><span data-stu-id="42a7d-281">**Lockout-Duration**</span></span>](a-lockoutduration.md)
</dt> </dl>

 

 





