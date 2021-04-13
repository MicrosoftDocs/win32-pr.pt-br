---
title: System-Flags atributo
description: Um valor inteiro que contém sinalizadores que definem propriedades adicionais da classe.
ms.assetid: ce24322c-fb01-462a-aefe-cb422851f782
ms.tgt_platform: multiple
keywords:
- Esquema de System-Flags do atributo AD
- Esquema de atributos de atributo systemFlags
topic_type:
- apiref
api_name:
- System-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34bf4286cbdadc84bf340eea3f6cbec741c7920
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456249"
---
# <a name="system-flags-attribute"></a><span data-ttu-id="8a30c-105">System-Flags atributo</span><span class="sxs-lookup"><span data-stu-id="8a30c-105">System-Flags attribute</span></span>

<span data-ttu-id="8a30c-106">Um valor inteiro que contém sinalizadores que definem propriedades adicionais da classe.</span><span class="sxs-lookup"><span data-stu-id="8a30c-106">An integer value that contains flags that define additional properties of the class.</span></span> <span data-ttu-id="8a30c-107">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="8a30c-107">See Remarks.</span></span>



| <span data-ttu-id="8a30c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-108">Entry</span></span> | <span data-ttu-id="8a30c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="8a30c-110">CN</span><span class="sxs-lookup"><span data-stu-id="8a30c-110">CN</span></span>                | <span data-ttu-id="8a30c-111">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-111">System-Flags</span></span>                                   |
| <span data-ttu-id="8a30c-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8a30c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8a30c-113">systemFlags</span><span class="sxs-lookup"><span data-stu-id="8a30c-113">systemFlags</span></span>                                    |
| <span data-ttu-id="8a30c-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8a30c-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="8a30c-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8a30c-115">Update Privilege</span></span>  | <span data-ttu-id="8a30c-116">Esse valor é definido pelo administrador do esquema.</span><span class="sxs-lookup"><span data-stu-id="8a30c-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="8a30c-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8a30c-117">Update Frequency</span></span>  | <span data-ttu-id="8a30c-118">Sempre que o estado do objeto for alterado.</span><span class="sxs-lookup"><span data-stu-id="8a30c-118">Whenever the state of the object changes.</span></span>      |
| <span data-ttu-id="8a30c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-119">Attribute-Id</span></span>      | <span data-ttu-id="8a30c-120">1.2.840.113556.1.4.375</span><span class="sxs-lookup"><span data-stu-id="8a30c-120">1.2.840.113556.1.4.375</span></span>                         |
| <span data-ttu-id="8a30c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8a30c-121">System-Id-Guid</span></span>    | <span data-ttu-id="8a30c-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="8a30c-122">e0fa1e62-9b45-11d0-afdd-00c04fd930c9</span></span>           |
| <span data-ttu-id="8a30c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a30c-123">Syntax</span></span>            | [<span data-ttu-id="8a30c-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="8a30c-124">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="8a30c-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="8a30c-125">Implementations</span></span>

-   [<span data-ttu-id="8a30c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a30c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a30c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a30c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a30c-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8a30c-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8a30c-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a30c-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a30c-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a30c-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a30c-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a30c-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a30c-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a30c-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a30c-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a30c-133">Windows 2000 Server</span></span>



| <span data-ttu-id="8a30c-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-134">Entry</span></span> | <span data-ttu-id="8a30c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-138">System-Only</span></span>            | <span data-ttu-id="8a30c-139">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-139">True</span></span>                            |
| <span data-ttu-id="8a30c-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-141">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-141">True</span></span>                            |
| <span data-ttu-id="8a30c-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-142">Is Indexed</span></span>             | <span data-ttu-id="8a30c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-143">False</span></span>                           |
| <span data-ttu-id="8a30c-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-144">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-145">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-145">False</span></span>                           |
| <span data-ttu-id="8a30c-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-150">Search-Flags</span></span>           | <span data-ttu-id="8a30c-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-151">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-152">System-Flags</span></span>           | <span data-ttu-id="8a30c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-153">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-154">Classes used in</span></span>        | [<span data-ttu-id="8a30c-155">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a30c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a30c-156">Windows Server 2003</span></span>



| <span data-ttu-id="8a30c-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-157">Entry</span></span> | <span data-ttu-id="8a30c-158">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-161">System-Only</span></span>            | <span data-ttu-id="8a30c-162">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-162">True</span></span>                            |
| <span data-ttu-id="8a30c-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-164">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-164">True</span></span>                            |
| <span data-ttu-id="8a30c-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-165">Is Indexed</span></span>             | <span data-ttu-id="8a30c-166">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-166">False</span></span>                           |
| <span data-ttu-id="8a30c-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-167">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-168">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-168">False</span></span>                           |
| <span data-ttu-id="8a30c-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-173">Search-Flags</span></span>           | <span data-ttu-id="8a30c-174">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-174">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-175">System-Flags</span></span>           | <span data-ttu-id="8a30c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-176">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-177">Classes used in</span></span>        | [<span data-ttu-id="8a30c-178">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8a30c-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="8a30c-179">ADAM</span></span>



| <span data-ttu-id="8a30c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-180">Entry</span></span> | <span data-ttu-id="8a30c-181">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-184">System-Only</span></span>            | <span data-ttu-id="8a30c-185">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-185">True</span></span>                            |
| <span data-ttu-id="8a30c-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-187">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-187">True</span></span>                            |
| <span data-ttu-id="8a30c-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-188">Is Indexed</span></span>             | <span data-ttu-id="8a30c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-189">False</span></span>                           |
| <span data-ttu-id="8a30c-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-190">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-191">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-191">False</span></span>                           |
| <span data-ttu-id="8a30c-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-196">Search-Flags</span></span>           | <span data-ttu-id="8a30c-197">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-197">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-198">System-Flags</span></span>           | <span data-ttu-id="8a30c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-199">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-200">Classes used in</span></span>        | [<span data-ttu-id="8a30c-201">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a30c-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a30c-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a30c-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-203">Entry</span></span> | <span data-ttu-id="8a30c-204">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-207">System-Only</span></span>            | <span data-ttu-id="8a30c-208">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-208">True</span></span>                            |
| <span data-ttu-id="8a30c-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-209">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-210">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-210">True</span></span>                            |
| <span data-ttu-id="8a30c-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-211">Is Indexed</span></span>             | <span data-ttu-id="8a30c-212">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-212">False</span></span>                           |
| <span data-ttu-id="8a30c-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-213">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-214">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-214">False</span></span>                           |
| <span data-ttu-id="8a30c-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-219">Search-Flags</span></span>           | <span data-ttu-id="8a30c-220">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-220">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-221">System-Flags</span></span>           | <span data-ttu-id="8a30c-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-222">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-223">Classes used in</span></span>        | [<span data-ttu-id="8a30c-224">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a30c-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a30c-225">Windows Server 2008</span></span>



| <span data-ttu-id="8a30c-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-226">Entry</span></span> | <span data-ttu-id="8a30c-227">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-230">System-Only</span></span>            | <span data-ttu-id="8a30c-231">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-231">True</span></span>                            |
| <span data-ttu-id="8a30c-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-232">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-233">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-233">True</span></span>                            |
| <span data-ttu-id="8a30c-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-234">Is Indexed</span></span>             | <span data-ttu-id="8a30c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-235">False</span></span>                           |
| <span data-ttu-id="8a30c-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-236">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-237">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-237">False</span></span>                           |
| <span data-ttu-id="8a30c-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-242">Search-Flags</span></span>           | <span data-ttu-id="8a30c-243">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-243">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-244">System-Flags</span></span>           | <span data-ttu-id="8a30c-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-245">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-246">Classes used in</span></span>        | [<span data-ttu-id="8a30c-247">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a30c-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a30c-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a30c-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-249">Entry</span></span> | <span data-ttu-id="8a30c-250">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-253">System-Only</span></span>            | <span data-ttu-id="8a30c-254">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-254">True</span></span>                            |
| <span data-ttu-id="8a30c-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-255">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-256">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-256">True</span></span>                            |
| <span data-ttu-id="8a30c-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-257">Is Indexed</span></span>             | <span data-ttu-id="8a30c-258">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-258">False</span></span>                           |
| <span data-ttu-id="8a30c-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-259">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-260">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-260">False</span></span>                           |
| <span data-ttu-id="8a30c-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-265">Search-Flags</span></span>           | <span data-ttu-id="8a30c-266">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-266">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-267">System-Flags</span></span>           | <span data-ttu-id="8a30c-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-268">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-269">Classes used in</span></span>        | [<span data-ttu-id="8a30c-270">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a30c-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a30c-271">Windows Server 2012</span></span>



| <span data-ttu-id="8a30c-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a30c-272">Entry</span></span> | <span data-ttu-id="8a30c-273">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a30c-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a30c-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a30c-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8a30c-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a30c-276">System-Only</span></span>            | <span data-ttu-id="8a30c-277">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-277">True</span></span>                            |
| <span data-ttu-id="8a30c-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a30c-278">Is-Single-Valued</span></span>       | <span data-ttu-id="8a30c-279">True</span><span class="sxs-lookup"><span data-stu-id="8a30c-279">True</span></span>                            |
| <span data-ttu-id="8a30c-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a30c-280">Is Indexed</span></span>             | <span data-ttu-id="8a30c-281">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-281">False</span></span>                           |
| <span data-ttu-id="8a30c-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a30c-282">In Global Catalog</span></span>      | <span data-ttu-id="8a30c-283">Falso</span><span class="sxs-lookup"><span data-stu-id="8a30c-283">False</span></span>                           |
| <span data-ttu-id="8a30c-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a30c-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a30c-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a30c-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a30c-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a30c-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8a30c-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a30c-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8a30c-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-288">Search-Flags</span></span>           | <span data-ttu-id="8a30c-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8a30c-289">0x00000008</span></span>                      |
| <span data-ttu-id="8a30c-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a30c-290">System-Flags</span></span>           | <span data-ttu-id="8a30c-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a30c-291">0x00000010</span></span>                      |
| <span data-ttu-id="8a30c-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a30c-292">Classes used in</span></span>        | [<span data-ttu-id="8a30c-293">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a30c-293">**Top**</span></span>](c-top.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8a30c-294">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a30c-294">Remarks</span></span>

<span data-ttu-id="8a30c-295">Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a30c-295">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="8a30c-296">Valor</span><span class="sxs-lookup"><span data-stu-id="8a30c-296">Value</span></span>                   | <span data-ttu-id="8a30c-297">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a30c-297">Description</span></span>                                                                                                                                                                                                                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a30c-298">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8a30c-298">1 (0x00000001)</span></span>          | <span data-ttu-id="8a30c-299">Quando aplicado a um atributo, o atributo não será replicado. Quando aplicado a um objeto de [**referência cruzada**](c-crossref.md) , o contexto de nomenclatura está em NTDS.</span><span class="sxs-lookup"><span data-stu-id="8a30c-299">When applied to an attribute, the attribute will not be replicated.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is in NTDS.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="8a30c-300">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="8a30c-300">2 (0x00000002)</span></span>          | <span data-ttu-id="8a30c-301">Quando aplicado a um atributo, o atributo será replicado para o catálogo global. Quando aplicado a um objeto de [**referência cruzada**](c-crossref.md) , o contexto de nomenclatura é um domínio.</span><span class="sxs-lookup"><span data-stu-id="8a30c-301">When applied to an attribute, the attribute will be replicated to the global catalog.When applied to a [**Cross-Ref**](c-crossref.md) object, the naming context is a domain.</span></span><br/>                                                                                                       |
| <span data-ttu-id="8a30c-302">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="8a30c-302">4 (0x00000004)</span></span>          | <span data-ttu-id="8a30c-303">Quando aplicado a um atributo, o atributo é construído.</span><span class="sxs-lookup"><span data-stu-id="8a30c-303">When applied to an attribute, the attribute is constructed.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="8a30c-304">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="8a30c-304">16 (0x00000010)</span></span>         | <span data-ttu-id="8a30c-305">Quando definido, indica que o objeto é um objeto da categoria 1.</span><span class="sxs-lookup"><span data-stu-id="8a30c-305">When set, indicates the object is a category 1 object.</span></span> <span data-ttu-id="8a30c-306">Um objeto Category 1 é uma classe ou um atributo que é incluído no esquema base incluído no sistema.</span><span class="sxs-lookup"><span data-stu-id="8a30c-306">A category 1 object is a class or attribute that is included in the base schema included with the system.</span></span>                                                                                                                                |
| <span data-ttu-id="8a30c-307">33554432 (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-307">33554432 (0x02000000)</span></span>   | <span data-ttu-id="8a30c-308">O objeto não é movido para o contêiner objetos excluídos quando ele é excluído.</span><span class="sxs-lookup"><span data-stu-id="8a30c-308">The object is not moved to the Deleted Objects container when it is deleted.</span></span> <span data-ttu-id="8a30c-309">Ele será excluído imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a30c-309">It will be deleted immediately.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="8a30c-310">67108864 (0x04000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-310">67108864 (0x04000000)</span></span>   | <span data-ttu-id="8a30c-311">O objeto não pode ser movido.</span><span class="sxs-lookup"><span data-stu-id="8a30c-311">The object cannot be moved.</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8a30c-312">134217728 (0x08000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-312">134217728 (0x08000000)</span></span>  | <span data-ttu-id="8a30c-313">O objeto não pode ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="8a30c-313">The object cannot be renamed.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8a30c-314">268435456 (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-314">268435456 (0x10000000)</span></span>  | <span data-ttu-id="8a30c-315">Para objetos na partição de configuração, se esse sinalizador for definido, o objeto poderá ser movido com restrições; caso contrário, o objeto não poderá ser movido.</span><span class="sxs-lookup"><span data-stu-id="8a30c-315">For objects in the configuration partition, if this flag is set, the object can be moved with restrictions; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="8a30c-316">Por padrão, esse sinalizador não é definido em novos objetos criados na partição de configuração.</span><span class="sxs-lookup"><span data-stu-id="8a30c-316">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="8a30c-317">Esse sinalizador só pode ser definido durante a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a30c-317">This flag can only be set during object creation.</span></span> |
| <span data-ttu-id="8a30c-318">536870912 (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-318">536870912 (0x20000000)</span></span>  | <span data-ttu-id="8a30c-319">Para objetos na partição de configuração, se esse sinalizador for definido, o objeto poderá ser movido; caso contrário, o objeto não poderá ser movido.</span><span class="sxs-lookup"><span data-stu-id="8a30c-319">For objects in the configuration partition, if this flag is set, the object can be moved; otherwise, the object cannot be moved.</span></span> <span data-ttu-id="8a30c-320">Por padrão, esse sinalizador não é definido em novos objetos criados na partição de configuração.</span><span class="sxs-lookup"><span data-stu-id="8a30c-320">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="8a30c-321">Esse sinalizador só pode ser definido durante a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a30c-321">This flag can only be set during object creation.</span></span>                   |
| <span data-ttu-id="8a30c-322">1073741824 (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-322">1073741824 (0x40000000)</span></span> | <span data-ttu-id="8a30c-323">Para objetos na partição de configuração, se esse sinalizador for definido, o objeto poderá ser renomeado; caso contrário, o objeto não poderá ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="8a30c-323">For objects in the configuration partition, if this flag is set, the object can be renamed; otherwise, the object cannot be renamed.</span></span> <span data-ttu-id="8a30c-324">Por padrão, esse sinalizador não é definido em novos objetos criados na partição de configuração.</span><span class="sxs-lookup"><span data-stu-id="8a30c-324">By default, this flag is not set on new objects created under the configuration partition.</span></span> <span data-ttu-id="8a30c-325">Esse sinalizador só pode ser definido durante a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a30c-325">This flag can only be set during object creation.</span></span>               |
| <span data-ttu-id="8a30c-326">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="8a30c-326">2147483648 (0x80000000)</span></span> | <span data-ttu-id="8a30c-327">O objeto não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8a30c-327">The object cannot be deleted.</span></span>                                                                                                                                                                                                                                                                   |



 

 

 





