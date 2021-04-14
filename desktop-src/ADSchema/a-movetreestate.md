---
title: Atributo de estado de árvore de movimentação
description: Este atributo contém informações de estado para uma árvore de diretório que está sendo movida.
ms.assetid: 13ec6d05-ed17-4a38-b2ae-7ad175f17b52
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de estado de árvore de movimentação
- Esquema de AD do atributo moveTreeState
topic_type:
- apiref
api_name:
- Move-Tree-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3041d54dfcdb97d7c9e1629162908fab1577b60c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456229"
---
# <a name="move-tree-state-attribute"></a><span data-ttu-id="34006-105">Atributo de estado de árvore de movimentação</span><span class="sxs-lookup"><span data-stu-id="34006-105">Move-Tree-State attribute</span></span>

<span data-ttu-id="34006-106">Este atributo contém informações de estado para uma árvore de diretório que está sendo movida.</span><span class="sxs-lookup"><span data-stu-id="34006-106">This attribute contains state information for a directory tree that is being moved.</span></span>



| <span data-ttu-id="34006-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-107">Entry</span></span> | <span data-ttu-id="34006-108">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="34006-109">CN</span><span class="sxs-lookup"><span data-stu-id="34006-109">CN</span></span>                | <span data-ttu-id="34006-110">Estado de árvore de movimentação</span><span class="sxs-lookup"><span data-stu-id="34006-110">Move-Tree-State</span></span>                                       |
| <span data-ttu-id="34006-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="34006-111">Ldap-Display-Name</span></span> | <span data-ttu-id="34006-112">moveTreeState</span><span class="sxs-lookup"><span data-stu-id="34006-112">moveTreeState</span></span>                                         |
| <span data-ttu-id="34006-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="34006-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="34006-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="34006-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="34006-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="34006-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="34006-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="34006-116">Attribute-Id</span></span>      | <span data-ttu-id="34006-117">1.2.840.113556.1.4.1305</span><span class="sxs-lookup"><span data-stu-id="34006-117">1.2.840.113556.1.4.1305</span></span>                               |
| <span data-ttu-id="34006-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="34006-118">System-Id-Guid</span></span>    | <span data-ttu-id="34006-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="34006-119">1f2ac2c8-3b71-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="34006-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="34006-120">Syntax</span></span>            | [<span data-ttu-id="34006-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="34006-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="34006-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="34006-122">Implementations</span></span>

-   [<span data-ttu-id="34006-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="34006-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="34006-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="34006-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="34006-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="34006-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="34006-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="34006-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="34006-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="34006-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="34006-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="34006-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="34006-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="34006-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="34006-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34006-130">Windows 2000 Server</span></span>



| <span data-ttu-id="34006-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-131">Entry</span></span> | <span data-ttu-id="34006-132">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-135">System-Only</span></span>            | <span data-ttu-id="34006-136">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-136">False</span></span>                                               |
| <span data-ttu-id="34006-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-137">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-138">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-138">False</span></span>                                               |
| <span data-ttu-id="34006-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-139">Is Indexed</span></span>             | <span data-ttu-id="34006-140">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-140">False</span></span>                                               |
| <span data-ttu-id="34006-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-141">In Global Catalog</span></span>      | <span data-ttu-id="34006-142">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-142">False</span></span>                                               |
| <span data-ttu-id="34006-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-147">Search-Flags</span></span>           | <span data-ttu-id="34006-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-148">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-149">System-Flags</span></span>           | <span data-ttu-id="34006-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-150">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-151">Classes used in</span></span>        | [<span data-ttu-id="34006-152">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-152">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="34006-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34006-153">Windows Server 2003</span></span>



| <span data-ttu-id="34006-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-154">Entry</span></span> | <span data-ttu-id="34006-155">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-158">System-Only</span></span>            | <span data-ttu-id="34006-159">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-159">False</span></span>                                               |
| <span data-ttu-id="34006-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-160">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-161">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-161">False</span></span>                                               |
| <span data-ttu-id="34006-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-162">Is Indexed</span></span>             | <span data-ttu-id="34006-163">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-163">False</span></span>                                               |
| <span data-ttu-id="34006-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-164">In Global Catalog</span></span>      | <span data-ttu-id="34006-165">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-165">False</span></span>                                               |
| <span data-ttu-id="34006-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-170">Search-Flags</span></span>           | <span data-ttu-id="34006-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-171">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-172">System-Flags</span></span>           | <span data-ttu-id="34006-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-173">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-174">Classes used in</span></span>        | [<span data-ttu-id="34006-175">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-175">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="adam"></a><span data-ttu-id="34006-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="34006-176">ADAM</span></span>



| <span data-ttu-id="34006-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-177">Entry</span></span> | <span data-ttu-id="34006-178">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-181">System-Only</span></span>            | <span data-ttu-id="34006-182">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-182">False</span></span>                                               |
| <span data-ttu-id="34006-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-183">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-184">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-184">False</span></span>                                               |
| <span data-ttu-id="34006-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-185">Is Indexed</span></span>             | <span data-ttu-id="34006-186">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-186">False</span></span>                                               |
| <span data-ttu-id="34006-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-187">In Global Catalog</span></span>      | <span data-ttu-id="34006-188">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-188">False</span></span>                                               |
| <span data-ttu-id="34006-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-193">Search-Flags</span></span>           | <span data-ttu-id="34006-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-194">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-195">System-Flags</span></span>           | <span data-ttu-id="34006-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-196">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-197">Classes used in</span></span>        | [<span data-ttu-id="34006-198">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-198">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="34006-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="34006-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="34006-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-200">Entry</span></span> | <span data-ttu-id="34006-201">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-204">System-Only</span></span>            | <span data-ttu-id="34006-205">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-205">False</span></span>                                               |
| <span data-ttu-id="34006-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-206">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-207">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-207">False</span></span>                                               |
| <span data-ttu-id="34006-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-208">Is Indexed</span></span>             | <span data-ttu-id="34006-209">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-209">False</span></span>                                               |
| <span data-ttu-id="34006-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-210">In Global Catalog</span></span>      | <span data-ttu-id="34006-211">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-211">False</span></span>                                               |
| <span data-ttu-id="34006-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-216">Search-Flags</span></span>           | <span data-ttu-id="34006-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-217">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-218">System-Flags</span></span>           | <span data-ttu-id="34006-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-219">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-220">Classes used in</span></span>        | [<span data-ttu-id="34006-221">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-221">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="34006-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34006-222">Windows Server 2008</span></span>



| <span data-ttu-id="34006-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-223">Entry</span></span> | <span data-ttu-id="34006-224">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-227">System-Only</span></span>            | <span data-ttu-id="34006-228">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-228">False</span></span>                                               |
| <span data-ttu-id="34006-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-229">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-230">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-230">False</span></span>                                               |
| <span data-ttu-id="34006-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-231">Is Indexed</span></span>             | <span data-ttu-id="34006-232">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-232">False</span></span>                                               |
| <span data-ttu-id="34006-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-233">In Global Catalog</span></span>      | <span data-ttu-id="34006-234">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-234">False</span></span>                                               |
| <span data-ttu-id="34006-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-239">Search-Flags</span></span>           | <span data-ttu-id="34006-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-240">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-241">System-Flags</span></span>           | <span data-ttu-id="34006-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-242">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-243">Classes used in</span></span>        | [<span data-ttu-id="34006-244">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-244">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="34006-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34006-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="34006-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-246">Entry</span></span> | <span data-ttu-id="34006-247">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-250">System-Only</span></span>            | <span data-ttu-id="34006-251">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-251">False</span></span>                                               |
| <span data-ttu-id="34006-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-252">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-253">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-253">False</span></span>                                               |
| <span data-ttu-id="34006-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-254">Is Indexed</span></span>             | <span data-ttu-id="34006-255">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-255">False</span></span>                                               |
| <span data-ttu-id="34006-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-256">In Global Catalog</span></span>      | <span data-ttu-id="34006-257">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-257">False</span></span>                                               |
| <span data-ttu-id="34006-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-262">Search-Flags</span></span>           | <span data-ttu-id="34006-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-263">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-264">System-Flags</span></span>           | <span data-ttu-id="34006-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-265">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-266">Classes used in</span></span>        | [<span data-ttu-id="34006-267">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-267">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="34006-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34006-268">Windows Server 2012</span></span>



| <span data-ttu-id="34006-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="34006-269">Entry</span></span> | <span data-ttu-id="34006-270">Valor</span><span class="sxs-lookup"><span data-stu-id="34006-270">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="34006-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="34006-271">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="34006-272">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="34006-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="34006-273">System-Only</span></span>            | <span data-ttu-id="34006-274">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-274">False</span></span>                                               |
| <span data-ttu-id="34006-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="34006-275">Is-Single-Valued</span></span>       | <span data-ttu-id="34006-276">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-276">False</span></span>                                               |
| <span data-ttu-id="34006-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="34006-277">Is Indexed</span></span>             | <span data-ttu-id="34006-278">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-278">False</span></span>                                               |
| <span data-ttu-id="34006-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="34006-279">In Global Catalog</span></span>      | <span data-ttu-id="34006-280">Falso</span><span class="sxs-lookup"><span data-stu-id="34006-280">False</span></span>                                               |
| <span data-ttu-id="34006-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="34006-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="34006-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="34006-282">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="34006-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="34006-283">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="34006-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="34006-284">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="34006-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-285">Search-Flags</span></span>           | <span data-ttu-id="34006-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="34006-286">0x00000000</span></span>                                          |
| <span data-ttu-id="34006-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="34006-287">System-Flags</span></span>           | <span data-ttu-id="34006-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="34006-288">0x00000010</span></span>                                          |
| <span data-ttu-id="34006-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="34006-289">Classes used in</span></span>        | [<span data-ttu-id="34006-290">**Perdido e encontrado**</span><span class="sxs-lookup"><span data-stu-id="34006-290">**Lost-And-Found**</span></span>](c-lostandfound.md)<br/> |



 

 





