---
title: Server-State atributo
description: Indica se o servidor está habilitado ou desabilitado.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Esquema de Server-State do atributo AD
- Esquema de AD do atributo ServerState
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105750962"
---
# <a name="server-state-attribute"></a><span data-ttu-id="189b3-105">Server-State atributo</span><span class="sxs-lookup"><span data-stu-id="189b3-105">Server-State attribute</span></span>

<span data-ttu-id="189b3-106">Indica se o servidor está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="189b3-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="189b3-107">Um valor de 1 indica que o servidor está habilitado.</span><span class="sxs-lookup"><span data-stu-id="189b3-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="189b3-108">Um valor de 2 indica que o servidor está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="189b3-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="189b3-109">Todos os outros valores são inválidos.</span><span class="sxs-lookup"><span data-stu-id="189b3-109">All other values are invalid.</span></span>



| <span data-ttu-id="189b3-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-110">Entry</span></span> | <span data-ttu-id="189b3-111">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="189b3-112">CN</span><span class="sxs-lookup"><span data-stu-id="189b3-112">CN</span></span>                | <span data-ttu-id="189b3-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="189b3-113">Server-State</span></span>                         |
| <span data-ttu-id="189b3-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="189b3-114">Ldap-Display-Name</span></span> | <span data-ttu-id="189b3-115">serverState</span><span class="sxs-lookup"><span data-stu-id="189b3-115">serverState</span></span>                          |
| <span data-ttu-id="189b3-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="189b3-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="189b3-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="189b3-117">Update Privilege</span></span>  | <span data-ttu-id="189b3-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="189b3-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="189b3-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="189b3-119">Update Frequency</span></span>  | <span data-ttu-id="189b3-120">Quando a política para um usuário é alterada.</span><span class="sxs-lookup"><span data-stu-id="189b3-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="189b3-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-121">Attribute-Id</span></span>      | <span data-ttu-id="189b3-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="189b3-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="189b3-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="189b3-123">System-Id-Guid</span></span>    | <span data-ttu-id="189b3-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="189b3-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="189b3-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="189b3-125">Syntax</span></span>            | [<span data-ttu-id="189b3-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="189b3-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="189b3-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="189b3-127">Implementations</span></span>

-   [<span data-ttu-id="189b3-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="189b3-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="189b3-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="189b3-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="189b3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="189b3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="189b3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="189b3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="189b3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="189b3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="189b3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="189b3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="189b3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="189b3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="189b3-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-135">Entry</span></span> | <span data-ttu-id="189b3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="189b3-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="189b3-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="189b3-139">System-Only</span></span>            | <span data-ttu-id="189b3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-140">False</span></span>                                                 |
| <span data-ttu-id="189b3-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="189b3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="189b3-142">True</span><span class="sxs-lookup"><span data-stu-id="189b3-142">True</span></span>                                                  |
| <span data-ttu-id="189b3-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="189b3-143">Is Indexed</span></span>             | <span data-ttu-id="189b3-144">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-144">False</span></span>                                                 |
| <span data-ttu-id="189b3-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="189b3-145">In Global Catalog</span></span>      | <span data-ttu-id="189b3-146">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-146">False</span></span>                                                 |
| <span data-ttu-id="189b3-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="189b3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="189b3-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="189b3-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="189b3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="189b3-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="189b3-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-151">Search-Flags</span></span>           | <span data-ttu-id="189b3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="189b3-152">0x00000000</span></span>                                            |
| <span data-ttu-id="189b3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-153">System-Flags</span></span>           | <span data-ttu-id="189b3-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="189b3-154">0x00000011</span></span>                                            |
| <span data-ttu-id="189b3-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="189b3-155">Classes used in</span></span>        | [<span data-ttu-id="189b3-156">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="189b3-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="189b3-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="189b3-157">Windows Server 2003</span></span>



| <span data-ttu-id="189b3-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-158">Entry</span></span> | <span data-ttu-id="189b3-159">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="189b3-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="189b3-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="189b3-162">System-Only</span></span>            | <span data-ttu-id="189b3-163">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-163">False</span></span>                                                 |
| <span data-ttu-id="189b3-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="189b3-164">Is-Single-Valued</span></span>       | <span data-ttu-id="189b3-165">True</span><span class="sxs-lookup"><span data-stu-id="189b3-165">True</span></span>                                                  |
| <span data-ttu-id="189b3-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="189b3-166">Is Indexed</span></span>             | <span data-ttu-id="189b3-167">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-167">False</span></span>                                                 |
| <span data-ttu-id="189b3-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="189b3-168">In Global Catalog</span></span>      | <span data-ttu-id="189b3-169">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-169">False</span></span>                                                 |
| <span data-ttu-id="189b3-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="189b3-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="189b3-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="189b3-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="189b3-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="189b3-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="189b3-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-174">Search-Flags</span></span>           | <span data-ttu-id="189b3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="189b3-175">0x00000000</span></span>                                            |
| <span data-ttu-id="189b3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-176">System-Flags</span></span>           | <span data-ttu-id="189b3-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="189b3-177">0x00000011</span></span>                                            |
| <span data-ttu-id="189b3-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="189b3-178">Classes used in</span></span>        | [<span data-ttu-id="189b3-179">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="189b3-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="189b3-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="189b3-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="189b3-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-181">Entry</span></span> | <span data-ttu-id="189b3-182">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="189b3-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="189b3-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="189b3-185">System-Only</span></span>            | <span data-ttu-id="189b3-186">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-186">False</span></span>                                                 |
| <span data-ttu-id="189b3-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="189b3-187">Is-Single-Valued</span></span>       | <span data-ttu-id="189b3-188">True</span><span class="sxs-lookup"><span data-stu-id="189b3-188">True</span></span>                                                  |
| <span data-ttu-id="189b3-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="189b3-189">Is Indexed</span></span>             | <span data-ttu-id="189b3-190">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-190">False</span></span>                                                 |
| <span data-ttu-id="189b3-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="189b3-191">In Global Catalog</span></span>      | <span data-ttu-id="189b3-192">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-192">False</span></span>                                                 |
| <span data-ttu-id="189b3-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="189b3-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="189b3-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="189b3-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="189b3-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="189b3-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="189b3-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-197">Search-Flags</span></span>           | <span data-ttu-id="189b3-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="189b3-198">0x00000000</span></span>                                            |
| <span data-ttu-id="189b3-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-199">System-Flags</span></span>           | <span data-ttu-id="189b3-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="189b3-200">0x00000011</span></span>                                            |
| <span data-ttu-id="189b3-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="189b3-201">Classes used in</span></span>        | [<span data-ttu-id="189b3-202">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="189b3-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="189b3-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="189b3-203">Windows Server 2008</span></span>



| <span data-ttu-id="189b3-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-204">Entry</span></span> | <span data-ttu-id="189b3-205">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="189b3-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="189b3-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="189b3-208">System-Only</span></span>            | <span data-ttu-id="189b3-209">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-209">False</span></span>                                                 |
| <span data-ttu-id="189b3-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="189b3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="189b3-211">True</span><span class="sxs-lookup"><span data-stu-id="189b3-211">True</span></span>                                                  |
| <span data-ttu-id="189b3-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="189b3-212">Is Indexed</span></span>             | <span data-ttu-id="189b3-213">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-213">False</span></span>                                                 |
| <span data-ttu-id="189b3-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="189b3-214">In Global Catalog</span></span>      | <span data-ttu-id="189b3-215">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-215">False</span></span>                                                 |
| <span data-ttu-id="189b3-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="189b3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="189b3-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="189b3-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="189b3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="189b3-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="189b3-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-220">Search-Flags</span></span>           | <span data-ttu-id="189b3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="189b3-221">0x00000000</span></span>                                            |
| <span data-ttu-id="189b3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-222">System-Flags</span></span>           | <span data-ttu-id="189b3-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="189b3-223">0x00000011</span></span>                                            |
| <span data-ttu-id="189b3-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="189b3-224">Classes used in</span></span>        | [<span data-ttu-id="189b3-225">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="189b3-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="189b3-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="189b3-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="189b3-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-227">Entry</span></span> | <span data-ttu-id="189b3-228">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="189b3-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="189b3-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="189b3-231">System-Only</span></span>            | <span data-ttu-id="189b3-232">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-232">False</span></span>                                                 |
| <span data-ttu-id="189b3-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="189b3-233">Is-Single-Valued</span></span>       | <span data-ttu-id="189b3-234">True</span><span class="sxs-lookup"><span data-stu-id="189b3-234">True</span></span>                                                  |
| <span data-ttu-id="189b3-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="189b3-235">Is Indexed</span></span>             | <span data-ttu-id="189b3-236">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-236">False</span></span>                                                 |
| <span data-ttu-id="189b3-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="189b3-237">In Global Catalog</span></span>      | <span data-ttu-id="189b3-238">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-238">False</span></span>                                                 |
| <span data-ttu-id="189b3-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="189b3-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="189b3-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="189b3-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="189b3-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="189b3-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="189b3-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-243">Search-Flags</span></span>           | <span data-ttu-id="189b3-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="189b3-244">0x00000000</span></span>                                            |
| <span data-ttu-id="189b3-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-245">System-Flags</span></span>           | <span data-ttu-id="189b3-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="189b3-246">0x00000011</span></span>                                            |
| <span data-ttu-id="189b3-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="189b3-247">Classes used in</span></span>        | [<span data-ttu-id="189b3-248">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="189b3-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="189b3-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="189b3-249">Windows Server 2012</span></span>



| <span data-ttu-id="189b3-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="189b3-250">Entry</span></span> | <span data-ttu-id="189b3-251">Valor</span><span class="sxs-lookup"><span data-stu-id="189b3-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="189b3-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="189b3-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="189b3-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="189b3-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="189b3-254">System-Only</span></span>            | <span data-ttu-id="189b3-255">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-255">False</span></span>                                                 |
| <span data-ttu-id="189b3-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="189b3-256">Is-Single-Valued</span></span>       | <span data-ttu-id="189b3-257">True</span><span class="sxs-lookup"><span data-stu-id="189b3-257">True</span></span>                                                  |
| <span data-ttu-id="189b3-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="189b3-258">Is Indexed</span></span>             | <span data-ttu-id="189b3-259">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-259">False</span></span>                                                 |
| <span data-ttu-id="189b3-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="189b3-260">In Global Catalog</span></span>      | <span data-ttu-id="189b3-261">Falso</span><span class="sxs-lookup"><span data-stu-id="189b3-261">False</span></span>                                                 |
| <span data-ttu-id="189b3-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="189b3-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="189b3-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="189b3-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="189b3-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="189b3-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="189b3-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="189b3-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-266">Search-Flags</span></span>           | <span data-ttu-id="189b3-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="189b3-267">0x00000000</span></span>                                            |
| <span data-ttu-id="189b3-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="189b3-268">System-Flags</span></span>           | <span data-ttu-id="189b3-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="189b3-269">0x00000011</span></span>                                            |
| <span data-ttu-id="189b3-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="189b3-270">Classes used in</span></span>        | [<span data-ttu-id="189b3-271">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="189b3-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





