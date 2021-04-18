---
title: Último atributo pai conhecido
description: O DN (nome distinto) do último pai conhecido de um objeto órfão.
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- Último esquema de atributo de domínio pai conhecido
- Esquema de AD do atributo lastKnownParent
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756087"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="1fb6e-105">Último atributo pai conhecido</span><span class="sxs-lookup"><span data-stu-id="1fb6e-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="1fb6e-106">O DN (nome distinto) do último pai conhecido de um objeto órfão.</span><span class="sxs-lookup"><span data-stu-id="1fb6e-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="1fb6e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-107">Entry</span></span> | <span data-ttu-id="1fb6e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="1fb6e-109">CN</span><span class="sxs-lookup"><span data-stu-id="1fb6e-109">CN</span></span>                | <span data-ttu-id="1fb6e-110">Último-pai conhecido</span><span class="sxs-lookup"><span data-stu-id="1fb6e-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="1fb6e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1fb6e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1fb6e-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="1fb6e-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="1fb6e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1fb6e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="1fb6e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1fb6e-114">Update Privilege</span></span>  | <span data-ttu-id="1fb6e-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1fb6e-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="1fb6e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1fb6e-116">Update Frequency</span></span>  | <span data-ttu-id="1fb6e-117">Sempre que um objeto estiver órfão.</span><span class="sxs-lookup"><span data-stu-id="1fb6e-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="1fb6e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-118">Attribute-Id</span></span>      | <span data-ttu-id="1fb6e-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="1fb6e-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="1fb6e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1fb6e-120">System-Id-Guid</span></span>    | <span data-ttu-id="1fb6e-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1fb6e-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="1fb6e-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fb6e-122">Syntax</span></span>            | [<span data-ttu-id="1fb6e-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="1fb6e-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="1fb6e-124">Implementations</span></span>

-   [<span data-ttu-id="1fb6e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1fb6e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1fb6e-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1fb6e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1fb6e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1fb6e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1fb6e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1fb6e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1fb6e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1fb6e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-133">Entry</span></span> | <span data-ttu-id="1fb6e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-137">System-Only</span></span>            | <span data-ttu-id="1fb6e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-138">False</span></span>                           |
| <span data-ttu-id="1fb6e-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-140">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-140">True</span></span>                            |
| <span data-ttu-id="1fb6e-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-141">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-142">False</span></span>                           |
| <span data-ttu-id="1fb6e-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-143">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-144">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-144">False</span></span>                           |
| <span data-ttu-id="1fb6e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-149">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-150">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-151">System-Flags</span></span>           | <span data-ttu-id="1fb6e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-152">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-153">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-154">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1fb6e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1fb6e-155">Windows Server 2003</span></span>



| <span data-ttu-id="1fb6e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-156">Entry</span></span> | <span data-ttu-id="1fb6e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-160">System-Only</span></span>            | <span data-ttu-id="1fb6e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-161">False</span></span>                           |
| <span data-ttu-id="1fb6e-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-163">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-163">True</span></span>                            |
| <span data-ttu-id="1fb6e-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-164">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-165">False</span></span>                           |
| <span data-ttu-id="1fb6e-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-166">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-167">False</span></span>                           |
| <span data-ttu-id="1fb6e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-172">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-173">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-174">System-Flags</span></span>           | <span data-ttu-id="1fb6e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-175">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-176">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-177">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1fb6e-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="1fb6e-178">ADAM</span></span>



| <span data-ttu-id="1fb6e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-179">Entry</span></span> | <span data-ttu-id="1fb6e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-183">System-Only</span></span>            | <span data-ttu-id="1fb6e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-184">False</span></span>                           |
| <span data-ttu-id="1fb6e-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-186">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-186">True</span></span>                            |
| <span data-ttu-id="1fb6e-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-187">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-188">False</span></span>                           |
| <span data-ttu-id="1fb6e-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-189">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-190">False</span></span>                           |
| <span data-ttu-id="1fb6e-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-195">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-196">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-197">System-Flags</span></span>           | <span data-ttu-id="1fb6e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-198">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-199">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-200">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1fb6e-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1fb6e-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1fb6e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-202">Entry</span></span> | <span data-ttu-id="1fb6e-203">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-206">System-Only</span></span>            | <span data-ttu-id="1fb6e-207">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-207">False</span></span>                           |
| <span data-ttu-id="1fb6e-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-209">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-209">True</span></span>                            |
| <span data-ttu-id="1fb6e-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-210">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-211">False</span></span>                           |
| <span data-ttu-id="1fb6e-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-212">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-213">False</span></span>                           |
| <span data-ttu-id="1fb6e-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-218">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-219">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-220">System-Flags</span></span>           | <span data-ttu-id="1fb6e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-221">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-222">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-223">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1fb6e-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fb6e-224">Windows Server 2008</span></span>



| <span data-ttu-id="1fb6e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-225">Entry</span></span> | <span data-ttu-id="1fb6e-226">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-229">System-Only</span></span>            | <span data-ttu-id="1fb6e-230">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-230">False</span></span>                           |
| <span data-ttu-id="1fb6e-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-232">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-232">True</span></span>                            |
| <span data-ttu-id="1fb6e-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-233">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-234">False</span></span>                           |
| <span data-ttu-id="1fb6e-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-235">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-236">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-236">False</span></span>                           |
| <span data-ttu-id="1fb6e-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-241">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-242">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-243">System-Flags</span></span>           | <span data-ttu-id="1fb6e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-244">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-245">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-246">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1fb6e-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fb6e-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1fb6e-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-248">Entry</span></span> | <span data-ttu-id="1fb6e-249">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-252">System-Only</span></span>            | <span data-ttu-id="1fb6e-253">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-253">False</span></span>                           |
| <span data-ttu-id="1fb6e-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-255">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-255">True</span></span>                            |
| <span data-ttu-id="1fb6e-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-256">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-257">False</span></span>                           |
| <span data-ttu-id="1fb6e-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-258">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-259">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-259">False</span></span>                           |
| <span data-ttu-id="1fb6e-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-264">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-265">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-266">System-Flags</span></span>           | <span data-ttu-id="1fb6e-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-267">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-268">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-269">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1fb6e-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fb6e-270">Windows Server 2012</span></span>



| <span data-ttu-id="1fb6e-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="1fb6e-271">Entry</span></span> | <span data-ttu-id="1fb6e-272">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1fb6e-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="1fb6e-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1fb6e-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1fb6e-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="1fb6e-275">System-Only</span></span>            | <span data-ttu-id="1fb6e-276">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-276">False</span></span>                           |
| <span data-ttu-id="1fb6e-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1fb6e-277">Is-Single-Valued</span></span>       | <span data-ttu-id="1fb6e-278">True</span><span class="sxs-lookup"><span data-stu-id="1fb6e-278">True</span></span>                            |
| <span data-ttu-id="1fb6e-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="1fb6e-279">Is Indexed</span></span>             | <span data-ttu-id="1fb6e-280">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-280">False</span></span>                           |
| <span data-ttu-id="1fb6e-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1fb6e-281">In Global Catalog</span></span>      | <span data-ttu-id="1fb6e-282">Falso</span><span class="sxs-lookup"><span data-stu-id="1fb6e-282">False</span></span>                           |
| <span data-ttu-id="1fb6e-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1fb6e-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="1fb6e-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1fb6e-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1fb6e-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1fb6e-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1fb6e-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1fb6e-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-287">Search-Flags</span></span>           | <span data-ttu-id="1fb6e-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1fb6e-288">0x00000000</span></span>                      |
| <span data-ttu-id="1fb6e-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1fb6e-289">System-Flags</span></span>           | <span data-ttu-id="1fb6e-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1fb6e-290">0x00000010</span></span>                      |
| <span data-ttu-id="1fb6e-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1fb6e-291">Classes used in</span></span>        | [<span data-ttu-id="1fb6e-292">**Início**</span><span class="sxs-lookup"><span data-stu-id="1fb6e-292">**Top**</span></span>](c-top.md)<br/> |



 

 





