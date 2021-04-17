---
title: Atributo estrutural-objeto-Class
description: Esse atributo construído armazena uma lista de classes contidas em uma hierarquia de classes, incluindo classes abstratas. Esta lista contém classes auxiliares vinculadas dinamicamente.
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo estrutural-Object-Class
- Esquema de AD do atributo structuralObjectClass
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755469"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="0f1a1-106">Atributo estrutural-objeto-Class</span><span class="sxs-lookup"><span data-stu-id="0f1a1-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="0f1a1-107">Esse atributo construído armazena uma lista de classes contidas em uma hierarquia de classes, incluindo classes abstratas.</span><span class="sxs-lookup"><span data-stu-id="0f1a1-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="0f1a1-108">Esta lista contém classes auxiliares vinculadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="0f1a1-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="0f1a1-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-109">Entry</span></span> | <span data-ttu-id="0f1a1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0f1a1-111">CN</span><span class="sxs-lookup"><span data-stu-id="0f1a1-111">CN</span></span>                | <span data-ttu-id="0f1a1-112">Classe de objeto estrutural</span><span class="sxs-lookup"><span data-stu-id="0f1a1-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="0f1a1-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0f1a1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0f1a1-114">structuralObjectClass</span><span class="sxs-lookup"><span data-stu-id="0f1a1-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="0f1a1-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0f1a1-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="0f1a1-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0f1a1-116">Update Privilege</span></span>  | <span data-ttu-id="0f1a1-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0f1a1-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="0f1a1-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0f1a1-118">Update Frequency</span></span>  | <span data-ttu-id="0f1a1-119">Na criação da classe.</span><span class="sxs-lookup"><span data-stu-id="0f1a1-119">At class creation.</span></span>                                              |
| <span data-ttu-id="0f1a1-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-120">Attribute-Id</span></span>      | <span data-ttu-id="0f1a1-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="0f1a1-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="0f1a1-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0f1a1-122">System-Id-Guid</span></span>    | <span data-ttu-id="0f1a1-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="0f1a1-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="0f1a1-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f1a1-124">Syntax</span></span>            | [<span data-ttu-id="0f1a1-125">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="0f1a1-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="0f1a1-126">Implementations</span></span>

-   [<span data-ttu-id="0f1a1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0f1a1-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0f1a1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0f1a1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0f1a1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0f1a1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0f1a1-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f1a1-133">Windows Server 2003</span></span>



| <span data-ttu-id="0f1a1-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-134">Entry</span></span> | <span data-ttu-id="0f1a1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0f1a1-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f1a1-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f1a1-138">System-Only</span></span>            | <span data-ttu-id="0f1a1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-139">False</span></span>                           |
| <span data-ttu-id="0f1a1-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f1a1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="0f1a1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-141">False</span></span>                           |
| <span data-ttu-id="0f1a1-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f1a1-142">Is Indexed</span></span>             | <span data-ttu-id="0f1a1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-143">False</span></span>                           |
| <span data-ttu-id="0f1a1-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f1a1-144">In Global Catalog</span></span>      | <span data-ttu-id="0f1a1-145">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-145">False</span></span>                           |
| <span data-ttu-id="0f1a1-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f1a1-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f1a1-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0f1a1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f1a1-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f1a1-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-150">Search-Flags</span></span>           | <span data-ttu-id="0f1a1-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f1a1-151">0x00000000</span></span>                      |
| <span data-ttu-id="0f1a1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-152">System-Flags</span></span>           | <span data-ttu-id="0f1a1-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="0f1a1-153">0x00000014</span></span>                      |
| <span data-ttu-id="0f1a1-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f1a1-154">Classes used in</span></span>        | [<span data-ttu-id="0f1a1-155">**Início**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0f1a1-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="0f1a1-156">ADAM</span></span>



| <span data-ttu-id="0f1a1-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-157">Entry</span></span> | <span data-ttu-id="0f1a1-158">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0f1a1-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f1a1-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f1a1-161">System-Only</span></span>            | <span data-ttu-id="0f1a1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-162">False</span></span>                           |
| <span data-ttu-id="0f1a1-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f1a1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0f1a1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-164">False</span></span>                           |
| <span data-ttu-id="0f1a1-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f1a1-165">Is Indexed</span></span>             | <span data-ttu-id="0f1a1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-166">False</span></span>                           |
| <span data-ttu-id="0f1a1-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f1a1-167">In Global Catalog</span></span>      | <span data-ttu-id="0f1a1-168">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-168">False</span></span>                           |
| <span data-ttu-id="0f1a1-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f1a1-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f1a1-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0f1a1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f1a1-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f1a1-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-173">Search-Flags</span></span>           | <span data-ttu-id="0f1a1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f1a1-174">0x00000000</span></span>                      |
| <span data-ttu-id="0f1a1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-175">System-Flags</span></span>           | <span data-ttu-id="0f1a1-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="0f1a1-176">0x00000014</span></span>                      |
| <span data-ttu-id="0f1a1-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f1a1-177">Classes used in</span></span>        | [<span data-ttu-id="0f1a1-178">**Início**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0f1a1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0f1a1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0f1a1-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-180">Entry</span></span> | <span data-ttu-id="0f1a1-181">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0f1a1-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f1a1-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f1a1-184">System-Only</span></span>            | <span data-ttu-id="0f1a1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-185">False</span></span>                           |
| <span data-ttu-id="0f1a1-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f1a1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0f1a1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-187">False</span></span>                           |
| <span data-ttu-id="0f1a1-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f1a1-188">Is Indexed</span></span>             | <span data-ttu-id="0f1a1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-189">False</span></span>                           |
| <span data-ttu-id="0f1a1-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f1a1-190">In Global Catalog</span></span>      | <span data-ttu-id="0f1a1-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-191">False</span></span>                           |
| <span data-ttu-id="0f1a1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f1a1-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f1a1-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0f1a1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f1a1-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f1a1-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-196">Search-Flags</span></span>           | <span data-ttu-id="0f1a1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f1a1-197">0x00000000</span></span>                      |
| <span data-ttu-id="0f1a1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-198">System-Flags</span></span>           | <span data-ttu-id="0f1a1-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="0f1a1-199">0x00000014</span></span>                      |
| <span data-ttu-id="0f1a1-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f1a1-200">Classes used in</span></span>        | [<span data-ttu-id="0f1a1-201">**Início**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0f1a1-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f1a1-202">Windows Server 2008</span></span>



| <span data-ttu-id="0f1a1-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-203">Entry</span></span> | <span data-ttu-id="0f1a1-204">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0f1a1-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f1a1-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f1a1-207">System-Only</span></span>            | <span data-ttu-id="0f1a1-208">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-208">False</span></span>                           |
| <span data-ttu-id="0f1a1-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f1a1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="0f1a1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-210">False</span></span>                           |
| <span data-ttu-id="0f1a1-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f1a1-211">Is Indexed</span></span>             | <span data-ttu-id="0f1a1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-212">False</span></span>                           |
| <span data-ttu-id="0f1a1-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f1a1-213">In Global Catalog</span></span>      | <span data-ttu-id="0f1a1-214">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-214">False</span></span>                           |
| <span data-ttu-id="0f1a1-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f1a1-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f1a1-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0f1a1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f1a1-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f1a1-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-219">Search-Flags</span></span>           | <span data-ttu-id="0f1a1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f1a1-220">0x00000000</span></span>                      |
| <span data-ttu-id="0f1a1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-221">System-Flags</span></span>           | <span data-ttu-id="0f1a1-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="0f1a1-222">0x00000014</span></span>                      |
| <span data-ttu-id="0f1a1-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f1a1-223">Classes used in</span></span>        | [<span data-ttu-id="0f1a1-224">**Início**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0f1a1-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f1a1-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0f1a1-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-226">Entry</span></span> | <span data-ttu-id="0f1a1-227">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0f1a1-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f1a1-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f1a1-230">System-Only</span></span>            | <span data-ttu-id="0f1a1-231">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-231">False</span></span>                           |
| <span data-ttu-id="0f1a1-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f1a1-232">Is-Single-Valued</span></span>       | <span data-ttu-id="0f1a1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-233">False</span></span>                           |
| <span data-ttu-id="0f1a1-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f1a1-234">Is Indexed</span></span>             | <span data-ttu-id="0f1a1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-235">False</span></span>                           |
| <span data-ttu-id="0f1a1-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f1a1-236">In Global Catalog</span></span>      | <span data-ttu-id="0f1a1-237">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-237">False</span></span>                           |
| <span data-ttu-id="0f1a1-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f1a1-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f1a1-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0f1a1-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f1a1-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f1a1-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-242">Search-Flags</span></span>           | <span data-ttu-id="0f1a1-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f1a1-243">0x00000000</span></span>                      |
| <span data-ttu-id="0f1a1-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-244">System-Flags</span></span>           | <span data-ttu-id="0f1a1-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="0f1a1-245">0x00000014</span></span>                      |
| <span data-ttu-id="0f1a1-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f1a1-246">Classes used in</span></span>        | [<span data-ttu-id="0f1a1-247">**Início**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0f1a1-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f1a1-248">Windows Server 2012</span></span>



| <span data-ttu-id="0f1a1-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="0f1a1-249">Entry</span></span> | <span data-ttu-id="0f1a1-250">Valor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0f1a1-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="0f1a1-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0f1a1-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0f1a1-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="0f1a1-253">System-Only</span></span>            | <span data-ttu-id="0f1a1-254">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-254">False</span></span>                           |
| <span data-ttu-id="0f1a1-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0f1a1-255">Is-Single-Valued</span></span>       | <span data-ttu-id="0f1a1-256">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-256">False</span></span>                           |
| <span data-ttu-id="0f1a1-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="0f1a1-257">Is Indexed</span></span>             | <span data-ttu-id="0f1a1-258">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-258">False</span></span>                           |
| <span data-ttu-id="0f1a1-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0f1a1-259">In Global Catalog</span></span>      | <span data-ttu-id="0f1a1-260">Falso</span><span class="sxs-lookup"><span data-stu-id="0f1a1-260">False</span></span>                           |
| <span data-ttu-id="0f1a1-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0f1a1-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="0f1a1-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0f1a1-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0f1a1-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0f1a1-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0f1a1-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0f1a1-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-265">Search-Flags</span></span>           | <span data-ttu-id="0f1a1-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f1a1-266">0x00000000</span></span>                      |
| <span data-ttu-id="0f1a1-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0f1a1-267">System-Flags</span></span>           | <span data-ttu-id="0f1a1-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="0f1a1-268">0x00000014</span></span>                      |
| <span data-ttu-id="0f1a1-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0f1a1-269">Classes used in</span></span>        | [<span data-ttu-id="0f1a1-270">**Início**</span><span class="sxs-lookup"><span data-stu-id="0f1a1-270">**Top**</span></span>](c-top.md)<br/> |



 

 





