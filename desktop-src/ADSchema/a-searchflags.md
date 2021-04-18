---
title: Search-Flags atributo
description: Contém um conjunto de sinalizadores que especificam informações de pesquisa e indexação para um atributo.
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- Esquema de Search-Flags do atributo AD
- Esquema de AD do atributo searchFlags
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f615464aa0aed69dd9590f668e37ec8c789c88
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105771708"
---
# <a name="search-flags-attribute"></a><span data-ttu-id="71d23-105">Search-Flags atributo</span><span class="sxs-lookup"><span data-stu-id="71d23-105">Search-Flags attribute</span></span>

<span data-ttu-id="71d23-106">Contém um conjunto de sinalizadores que especificam informações de pesquisa e indexação para um atributo.</span><span class="sxs-lookup"><span data-stu-id="71d23-106">Contains a set of flags that specify search and indexing information for an attribute.</span></span> <span data-ttu-id="71d23-107">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="71d23-107">See Remarks.</span></span>



| <span data-ttu-id="71d23-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-108">Entry</span></span> | <span data-ttu-id="71d23-109">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="71d23-110">CN</span><span class="sxs-lookup"><span data-stu-id="71d23-110">CN</span></span>                | <span data-ttu-id="71d23-111">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-111">Search-Flags</span></span>                         |
| <span data-ttu-id="71d23-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="71d23-112">Ldap-Display-Name</span></span> | <span data-ttu-id="71d23-113">searchFlags</span><span class="sxs-lookup"><span data-stu-id="71d23-113">searchFlags</span></span>                          |
| <span data-ttu-id="71d23-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="71d23-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="71d23-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="71d23-115">Update Privilege</span></span>  | <span data-ttu-id="71d23-116">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="71d23-116">Schema administrator</span></span>                 |
| <span data-ttu-id="71d23-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="71d23-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="71d23-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-118">Attribute-Id</span></span>      | <span data-ttu-id="71d23-119">1.2.840.113556.1.2.334</span><span class="sxs-lookup"><span data-stu-id="71d23-119">1.2.840.113556.1.2.334</span></span>               |
| <span data-ttu-id="71d23-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="71d23-120">System-Id-Guid</span></span>    | <span data-ttu-id="71d23-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="71d23-121">bf967a2d-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="71d23-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="71d23-122">Syntax</span></span>            | [<span data-ttu-id="71d23-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="71d23-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="71d23-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="71d23-124">Implementations</span></span>

-   [<span data-ttu-id="71d23-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="71d23-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="71d23-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="71d23-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="71d23-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="71d23-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="71d23-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="71d23-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="71d23-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="71d23-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="71d23-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="71d23-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="71d23-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="71d23-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="71d23-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71d23-132">Windows 2000 Server</span></span>



| <span data-ttu-id="71d23-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-133">Entry</span></span> | <span data-ttu-id="71d23-134">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-136">MAPI-Id</span></span>                | <span data-ttu-id="71d23-137">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-137">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-138">System-Only</span></span>            | <span data-ttu-id="71d23-139">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-139">False</span></span>                                                    |
| <span data-ttu-id="71d23-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-140">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-141">True</span><span class="sxs-lookup"><span data-stu-id="71d23-141">True</span></span>                                                     |
| <span data-ttu-id="71d23-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-142">Is Indexed</span></span>             | <span data-ttu-id="71d23-143">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-143">False</span></span>                                                    |
| <span data-ttu-id="71d23-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-144">In Global Catalog</span></span>      | <span data-ttu-id="71d23-145">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-145">False</span></span>                                                    |
| <span data-ttu-id="71d23-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-148">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-149">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-150">Search-Flags</span></span>           | <span data-ttu-id="71d23-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-151">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-152">System-Flags</span></span>           | <span data-ttu-id="71d23-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-153">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-154">Classes used in</span></span>        | [<span data-ttu-id="71d23-155">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="71d23-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71d23-156">Windows Server 2003</span></span>



| <span data-ttu-id="71d23-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-157">Entry</span></span> | <span data-ttu-id="71d23-158">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-160">MAPI-Id</span></span>                | <span data-ttu-id="71d23-161">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-161">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-162">System-Only</span></span>            | <span data-ttu-id="71d23-163">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-163">False</span></span>                                                    |
| <span data-ttu-id="71d23-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-164">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-165">True</span><span class="sxs-lookup"><span data-stu-id="71d23-165">True</span></span>                                                     |
| <span data-ttu-id="71d23-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-166">Is Indexed</span></span>             | <span data-ttu-id="71d23-167">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-167">False</span></span>                                                    |
| <span data-ttu-id="71d23-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-168">In Global Catalog</span></span>      | <span data-ttu-id="71d23-169">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-169">False</span></span>                                                    |
| <span data-ttu-id="71d23-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-171">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-172">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-173">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-174">Search-Flags</span></span>           | <span data-ttu-id="71d23-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-175">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-176">System-Flags</span></span>           | <span data-ttu-id="71d23-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-177">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-178">Classes used in</span></span>        | [<span data-ttu-id="71d23-179">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="71d23-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="71d23-180">ADAM</span></span>



| <span data-ttu-id="71d23-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-181">Entry</span></span> | <span data-ttu-id="71d23-182">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-182">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-183">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-184">MAPI-Id</span></span>                | <span data-ttu-id="71d23-185">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-185">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-186">System-Only</span></span>            | <span data-ttu-id="71d23-187">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-187">False</span></span>                                                    |
| <span data-ttu-id="71d23-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-188">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-189">True</span><span class="sxs-lookup"><span data-stu-id="71d23-189">True</span></span>                                                     |
| <span data-ttu-id="71d23-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-190">Is Indexed</span></span>             | <span data-ttu-id="71d23-191">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-191">False</span></span>                                                    |
| <span data-ttu-id="71d23-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-192">In Global Catalog</span></span>      | <span data-ttu-id="71d23-193">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-193">False</span></span>                                                    |
| <span data-ttu-id="71d23-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-196">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-197">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-198">Search-Flags</span></span>           | <span data-ttu-id="71d23-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-199">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-200">System-Flags</span></span>           | <span data-ttu-id="71d23-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-201">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-202">Classes used in</span></span>        | [<span data-ttu-id="71d23-203">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="71d23-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="71d23-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="71d23-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-205">Entry</span></span> | <span data-ttu-id="71d23-206">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-208">MAPI-Id</span></span>                | <span data-ttu-id="71d23-209">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-209">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-210">System-Only</span></span>            | <span data-ttu-id="71d23-211">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-211">False</span></span>                                                    |
| <span data-ttu-id="71d23-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-212">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-213">True</span><span class="sxs-lookup"><span data-stu-id="71d23-213">True</span></span>                                                     |
| <span data-ttu-id="71d23-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-214">Is Indexed</span></span>             | <span data-ttu-id="71d23-215">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-215">False</span></span>                                                    |
| <span data-ttu-id="71d23-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-216">In Global Catalog</span></span>      | <span data-ttu-id="71d23-217">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-217">False</span></span>                                                    |
| <span data-ttu-id="71d23-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-219">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-220">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-221">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-222">Search-Flags</span></span>           | <span data-ttu-id="71d23-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-223">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-224">System-Flags</span></span>           | <span data-ttu-id="71d23-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-225">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-226">Classes used in</span></span>        | [<span data-ttu-id="71d23-227">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="71d23-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71d23-228">Windows Server 2008</span></span>



| <span data-ttu-id="71d23-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-229">Entry</span></span> | <span data-ttu-id="71d23-230">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-230">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-231">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-232">MAPI-Id</span></span>                | <span data-ttu-id="71d23-233">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-233">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-234">System-Only</span></span>            | <span data-ttu-id="71d23-235">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-235">False</span></span>                                                    |
| <span data-ttu-id="71d23-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-236">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-237">True</span><span class="sxs-lookup"><span data-stu-id="71d23-237">True</span></span>                                                     |
| <span data-ttu-id="71d23-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-238">Is Indexed</span></span>             | <span data-ttu-id="71d23-239">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-239">False</span></span>                                                    |
| <span data-ttu-id="71d23-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-240">In Global Catalog</span></span>      | <span data-ttu-id="71d23-241">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-241">False</span></span>                                                    |
| <span data-ttu-id="71d23-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-244">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-245">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-246">Search-Flags</span></span>           | <span data-ttu-id="71d23-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-247">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-248">System-Flags</span></span>           | <span data-ttu-id="71d23-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-249">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-250">Classes used in</span></span>        | [<span data-ttu-id="71d23-251">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="71d23-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71d23-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="71d23-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-253">Entry</span></span> | <span data-ttu-id="71d23-254">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-254">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-255">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-256">MAPI-Id</span></span>                | <span data-ttu-id="71d23-257">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-257">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-258">System-Only</span></span>            | <span data-ttu-id="71d23-259">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-259">False</span></span>                                                    |
| <span data-ttu-id="71d23-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-260">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-261">True</span><span class="sxs-lookup"><span data-stu-id="71d23-261">True</span></span>                                                     |
| <span data-ttu-id="71d23-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-262">Is Indexed</span></span>             | <span data-ttu-id="71d23-263">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-263">False</span></span>                                                    |
| <span data-ttu-id="71d23-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-264">In Global Catalog</span></span>      | <span data-ttu-id="71d23-265">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-265">False</span></span>                                                    |
| <span data-ttu-id="71d23-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-267">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-268">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-269">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-270">Search-Flags</span></span>           | <span data-ttu-id="71d23-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-271">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-272">System-Flags</span></span>           | <span data-ttu-id="71d23-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-273">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-274">Classes used in</span></span>        | [<span data-ttu-id="71d23-275">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="71d23-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71d23-276">Windows Server 2012</span></span>



| <span data-ttu-id="71d23-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="71d23-277">Entry</span></span> | <span data-ttu-id="71d23-278">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-278">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d23-279">ID do link</span><span class="sxs-lookup"><span data-stu-id="71d23-279">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="71d23-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="71d23-280">MAPI-Id</span></span>                | <span data-ttu-id="71d23-281">0x812D</span><span class="sxs-lookup"><span data-stu-id="71d23-281">0x812D</span></span>                                                   |
| <span data-ttu-id="71d23-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="71d23-282">System-Only</span></span>            | <span data-ttu-id="71d23-283">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-283">False</span></span>                                                    |
| <span data-ttu-id="71d23-284">É de valor único</span><span class="sxs-lookup"><span data-stu-id="71d23-284">Is-Single-Valued</span></span>       | <span data-ttu-id="71d23-285">True</span><span class="sxs-lookup"><span data-stu-id="71d23-285">True</span></span>                                                     |
| <span data-ttu-id="71d23-286">É indexado</span><span class="sxs-lookup"><span data-stu-id="71d23-286">Is Indexed</span></span>             | <span data-ttu-id="71d23-287">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-287">False</span></span>                                                    |
| <span data-ttu-id="71d23-288">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="71d23-288">In Global Catalog</span></span>      | <span data-ttu-id="71d23-289">Falso</span><span class="sxs-lookup"><span data-stu-id="71d23-289">False</span></span>                                                    |
| <span data-ttu-id="71d23-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="71d23-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="71d23-291">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="71d23-291">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="71d23-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="71d23-292">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="71d23-293">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="71d23-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-294">Search-Flags</span></span>           | <span data-ttu-id="71d23-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="71d23-295">0x00000000</span></span>                                               |
| <span data-ttu-id="71d23-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="71d23-296">System-Flags</span></span>           | <span data-ttu-id="71d23-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="71d23-297">0x00000010</span></span>                                               |
| <span data-ttu-id="71d23-298">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="71d23-298">Classes used in</span></span>        | [<span data-ttu-id="71d23-299">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="71d23-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="71d23-300">Comentários</span><span class="sxs-lookup"><span data-stu-id="71d23-300">Remarks</span></span>

<span data-ttu-id="71d23-301">Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="71d23-301">This attribute can be zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="71d23-302">Valor</span><span class="sxs-lookup"><span data-stu-id="71d23-302">Value</span></span>            | <span data-ttu-id="71d23-303">Descrição</span><span class="sxs-lookup"><span data-stu-id="71d23-303">Description</span></span>                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d23-304">1 (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="71d23-304">1 (0x00000001)</span></span>   | <span data-ttu-id="71d23-305">Crie um índice para o atributo.</span><span class="sxs-lookup"><span data-stu-id="71d23-305">Create an index for the attribute.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="71d23-306">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="71d23-306">2 (0x00000002)</span></span>   | <span data-ttu-id="71d23-307">Crie um índice para o atributo em cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="71d23-307">Create an index for the attribute in each container.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="71d23-308">4 (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="71d23-308">4 (0x00000004)</span></span>   | <span data-ttu-id="71d23-309">Adicione este atributo ao conjunto de resolução de nome ambíguo (ANR).</span><span class="sxs-lookup"><span data-stu-id="71d23-309">Add this attribute to the Ambiguous Name Resolution (ANR) set.</span></span> <span data-ttu-id="71d23-310">Isso é usado para auxiliar na localização de um objeto quando apenas informações parciais são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="71d23-310">This is used to assist in finding an object when only partial information is given.</span></span> <span data-ttu-id="71d23-311">Por exemplo, se o filtro LDAP for (ANR = JEFF), a pesquisa localizará cada objeto em que o nome, sobrenome, endereço de email ou outro atributo ANR é igual a JEFF.</span><span class="sxs-lookup"><span data-stu-id="71d23-311">For example, if the LDAP filter is (ANR=JEFF), the search will find each object where the first name, last name, email address, or other ANR attribute is equal to JEFF.</span></span> <span data-ttu-id="71d23-312">O bit 0 deve ser definido para que esse índice tenha efeito.</span><span class="sxs-lookup"><span data-stu-id="71d23-312">Bit 0 must be set for this index take affect.</span></span> |
| <span data-ttu-id="71d23-313">8 (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="71d23-313">8 (0x00000008)</span></span>   | <span data-ttu-id="71d23-314">Preserve esse atributo no objeto de marca para exclusão para objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="71d23-314">Preserve this attribute in the tombstone object for deleted objects.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="71d23-315">16 (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="71d23-315">16 (0x00000010)</span></span>  | <span data-ttu-id="71d23-316">Copie o valor desse atributo quando o objeto for copiado.</span><span class="sxs-lookup"><span data-stu-id="71d23-316">Copy the value for this attribute when the object is copied.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="71d23-317">32 (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="71d23-317">32 (0x00000020)</span></span>  | <span data-ttu-id="71d23-318">Crie um índice de tupla para o atributo.</span><span class="sxs-lookup"><span data-stu-id="71d23-318">Create a tuple index for the attribute.</span></span> <span data-ttu-id="71d23-319">Isso melhorará as pesquisas em que o curinga aparece na frente da cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="71d23-319">This will improve searches where the wildcard appears at the front of the search string.</span></span> <span data-ttu-id="71d23-320">Por exemplo, (SN = \* mith).</span><span class="sxs-lookup"><span data-stu-id="71d23-320">For example, (sn=\*mith).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="71d23-321">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="71d23-321">64(0x00000040)</span></span>   | <span data-ttu-id="71d23-322">Com suporte a partir do ADAM.</span><span class="sxs-lookup"><span data-stu-id="71d23-322">Supported beginning with ADAM.</span></span> <span data-ttu-id="71d23-323">Cria um índice para ajudar muito o desempenho de VLV em atributos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="71d23-323">Creates an index to greatly help VLV performance on arbitrary attributes.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="71d23-324">128 (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="71d23-324">128 (0x00000080)</span></span> | <span data-ttu-id="71d23-325">Marque o atributo como confidencial.</span><span class="sxs-lookup"><span data-stu-id="71d23-325">Mark attribute as confidential.</span></span> <span data-ttu-id="71d23-326">Ignorado para atributos de esquema base (systemFlags = 0x10).</span><span class="sxs-lookup"><span data-stu-id="71d23-326">Ignored for base schema attributes (systemFlags=0x10).</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="71d23-327">64 (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="71d23-327">64 (0x00000040)</span></span>  | <span data-ttu-id="71d23-328">Com suporte a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="71d23-328">Supported beginning with Windows Server 2008.</span></span> <span data-ttu-id="71d23-329">Crie um índice para melhorar o desempenho da pesquisa VLV nesse atributo.</span><span class="sxs-lookup"><span data-stu-id="71d23-329">Create an index to improve VLV search performance on this attribute.</span></span>                                                                                                                                                                                                                                                        |



 

 

 





