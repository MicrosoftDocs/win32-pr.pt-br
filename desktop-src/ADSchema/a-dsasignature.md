---
title: DSA-Signature atributo
description: A DSA-Signature de um objeto é a ID de invocação do último diretório para modificar o objeto.
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- Esquema de DSA-Signature do atributo AD
- Esquema de AD do atributo dSASignature
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754415"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="92f17-105">DSA-Signature atributo</span><span class="sxs-lookup"><span data-stu-id="92f17-105">DSA-Signature attribute</span></span>

<span data-ttu-id="92f17-106">A DSA-Signature de um objeto é a ID de invocação do último diretório para modificar o objeto.</span><span class="sxs-lookup"><span data-stu-id="92f17-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="92f17-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-107">Entry</span></span> | <span data-ttu-id="92f17-108">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="92f17-109">CN</span><span class="sxs-lookup"><span data-stu-id="92f17-109">CN</span></span>                | <span data-ttu-id="92f17-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="92f17-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="92f17-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="92f17-111">Ldap-Display-Name</span></span> | <span data-ttu-id="92f17-112">dSASignature</span><span class="sxs-lookup"><span data-stu-id="92f17-112">dSASignature</span></span>                                          |
| <span data-ttu-id="92f17-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="92f17-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="92f17-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="92f17-114">Update Privilege</span></span>  | <span data-ttu-id="92f17-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="92f17-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="92f17-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="92f17-116">Update Frequency</span></span>  | <span data-ttu-id="92f17-117">Sempre que um objeto é modificado.</span><span class="sxs-lookup"><span data-stu-id="92f17-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="92f17-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-118">Attribute-Id</span></span>      | <span data-ttu-id="92f17-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="92f17-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="92f17-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="92f17-120">System-Id-Guid</span></span>    | <span data-ttu-id="92f17-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="92f17-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="92f17-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="92f17-122">Syntax</span></span>            | [<span data-ttu-id="92f17-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="92f17-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="92f17-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="92f17-124">Implementations</span></span>

-   [<span data-ttu-id="92f17-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92f17-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92f17-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92f17-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92f17-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="92f17-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="92f17-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92f17-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92f17-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92f17-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92f17-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92f17-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92f17-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92f17-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92f17-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92f17-132">Windows 2000 Server</span></span>



| <span data-ttu-id="92f17-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-133">Entry</span></span> | <span data-ttu-id="92f17-134">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-136">MAPI-Id</span></span>                | <span data-ttu-id="92f17-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-137">0x8077</span></span>                          |
| <span data-ttu-id="92f17-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-138">System-Only</span></span>            | <span data-ttu-id="92f17-139">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-139">False</span></span>                           |
| <span data-ttu-id="92f17-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-140">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-141">True</span><span class="sxs-lookup"><span data-stu-id="92f17-141">True</span></span>                            |
| <span data-ttu-id="92f17-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-142">Is Indexed</span></span>             | <span data-ttu-id="92f17-143">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-143">False</span></span>                           |
| <span data-ttu-id="92f17-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-144">In Global Catalog</span></span>      | <span data-ttu-id="92f17-145">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-145">False</span></span>                           |
| <span data-ttu-id="92f17-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-150">Search-Flags</span></span>           | <span data-ttu-id="92f17-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-151">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-152">System-Flags</span></span>           | <span data-ttu-id="92f17-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-153">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-154">Classes used in</span></span>        | [<span data-ttu-id="92f17-155">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92f17-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92f17-156">Windows Server 2003</span></span>



| <span data-ttu-id="92f17-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-157">Entry</span></span> | <span data-ttu-id="92f17-158">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-160">MAPI-Id</span></span>                | <span data-ttu-id="92f17-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-161">0x8077</span></span>                          |
| <span data-ttu-id="92f17-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-162">System-Only</span></span>            | <span data-ttu-id="92f17-163">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-163">False</span></span>                           |
| <span data-ttu-id="92f17-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-164">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-165">True</span><span class="sxs-lookup"><span data-stu-id="92f17-165">True</span></span>                            |
| <span data-ttu-id="92f17-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-166">Is Indexed</span></span>             | <span data-ttu-id="92f17-167">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-167">False</span></span>                           |
| <span data-ttu-id="92f17-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-168">In Global Catalog</span></span>      | <span data-ttu-id="92f17-169">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-169">False</span></span>                           |
| <span data-ttu-id="92f17-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-174">Search-Flags</span></span>           | <span data-ttu-id="92f17-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-175">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-176">System-Flags</span></span>           | <span data-ttu-id="92f17-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-177">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-178">Classes used in</span></span>        | [<span data-ttu-id="92f17-179">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="92f17-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="92f17-180">ADAM</span></span>



| <span data-ttu-id="92f17-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-181">Entry</span></span> | <span data-ttu-id="92f17-182">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-184">MAPI-Id</span></span>                | <span data-ttu-id="92f17-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-185">0x8077</span></span>                          |
| <span data-ttu-id="92f17-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-186">System-Only</span></span>            | <span data-ttu-id="92f17-187">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-187">False</span></span>                           |
| <span data-ttu-id="92f17-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-188">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-189">True</span><span class="sxs-lookup"><span data-stu-id="92f17-189">True</span></span>                            |
| <span data-ttu-id="92f17-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-190">Is Indexed</span></span>             | <span data-ttu-id="92f17-191">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-191">False</span></span>                           |
| <span data-ttu-id="92f17-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-192">In Global Catalog</span></span>      | <span data-ttu-id="92f17-193">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-193">False</span></span>                           |
| <span data-ttu-id="92f17-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-198">Search-Flags</span></span>           | <span data-ttu-id="92f17-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-199">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-200">System-Flags</span></span>           | <span data-ttu-id="92f17-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-201">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-202">Classes used in</span></span>        | [<span data-ttu-id="92f17-203">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92f17-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92f17-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92f17-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-205">Entry</span></span> | <span data-ttu-id="92f17-206">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-208">MAPI-Id</span></span>                | <span data-ttu-id="92f17-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-209">0x8077</span></span>                          |
| <span data-ttu-id="92f17-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-210">System-Only</span></span>            | <span data-ttu-id="92f17-211">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-211">False</span></span>                           |
| <span data-ttu-id="92f17-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-212">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-213">True</span><span class="sxs-lookup"><span data-stu-id="92f17-213">True</span></span>                            |
| <span data-ttu-id="92f17-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-214">Is Indexed</span></span>             | <span data-ttu-id="92f17-215">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-215">False</span></span>                           |
| <span data-ttu-id="92f17-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-216">In Global Catalog</span></span>      | <span data-ttu-id="92f17-217">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-217">False</span></span>                           |
| <span data-ttu-id="92f17-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-222">Search-Flags</span></span>           | <span data-ttu-id="92f17-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-223">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-224">System-Flags</span></span>           | <span data-ttu-id="92f17-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-225">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-226">Classes used in</span></span>        | [<span data-ttu-id="92f17-227">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92f17-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92f17-228">Windows Server 2008</span></span>



| <span data-ttu-id="92f17-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-229">Entry</span></span> | <span data-ttu-id="92f17-230">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-232">MAPI-Id</span></span>                | <span data-ttu-id="92f17-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-233">0x8077</span></span>                          |
| <span data-ttu-id="92f17-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-234">System-Only</span></span>            | <span data-ttu-id="92f17-235">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-235">False</span></span>                           |
| <span data-ttu-id="92f17-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-236">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-237">True</span><span class="sxs-lookup"><span data-stu-id="92f17-237">True</span></span>                            |
| <span data-ttu-id="92f17-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-238">Is Indexed</span></span>             | <span data-ttu-id="92f17-239">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-239">False</span></span>                           |
| <span data-ttu-id="92f17-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-240">In Global Catalog</span></span>      | <span data-ttu-id="92f17-241">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-241">False</span></span>                           |
| <span data-ttu-id="92f17-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-246">Search-Flags</span></span>           | <span data-ttu-id="92f17-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-247">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-248">System-Flags</span></span>           | <span data-ttu-id="92f17-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-249">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-250">Classes used in</span></span>        | [<span data-ttu-id="92f17-251">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92f17-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92f17-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92f17-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-253">Entry</span></span> | <span data-ttu-id="92f17-254">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-256">MAPI-Id</span></span>                | <span data-ttu-id="92f17-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-257">0x8077</span></span>                          |
| <span data-ttu-id="92f17-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-258">System-Only</span></span>            | <span data-ttu-id="92f17-259">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-259">False</span></span>                           |
| <span data-ttu-id="92f17-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-260">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-261">True</span><span class="sxs-lookup"><span data-stu-id="92f17-261">True</span></span>                            |
| <span data-ttu-id="92f17-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-262">Is Indexed</span></span>             | <span data-ttu-id="92f17-263">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-263">False</span></span>                           |
| <span data-ttu-id="92f17-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-264">In Global Catalog</span></span>      | <span data-ttu-id="92f17-265">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-265">False</span></span>                           |
| <span data-ttu-id="92f17-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-270">Search-Flags</span></span>           | <span data-ttu-id="92f17-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-271">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-272">System-Flags</span></span>           | <span data-ttu-id="92f17-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-273">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-274">Classes used in</span></span>        | [<span data-ttu-id="92f17-275">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92f17-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92f17-276">Windows Server 2012</span></span>



| <span data-ttu-id="92f17-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f17-277">Entry</span></span> | <span data-ttu-id="92f17-278">Valor</span><span class="sxs-lookup"><span data-stu-id="92f17-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="92f17-279">ID do link</span><span class="sxs-lookup"><span data-stu-id="92f17-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="92f17-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92f17-280">MAPI-Id</span></span>                | <span data-ttu-id="92f17-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="92f17-281">0x8077</span></span>                          |
| <span data-ttu-id="92f17-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="92f17-282">System-Only</span></span>            | <span data-ttu-id="92f17-283">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-283">False</span></span>                           |
| <span data-ttu-id="92f17-284">É de valor único</span><span class="sxs-lookup"><span data-stu-id="92f17-284">Is-Single-Valued</span></span>       | <span data-ttu-id="92f17-285">True</span><span class="sxs-lookup"><span data-stu-id="92f17-285">True</span></span>                            |
| <span data-ttu-id="92f17-286">É indexado</span><span class="sxs-lookup"><span data-stu-id="92f17-286">Is Indexed</span></span>             | <span data-ttu-id="92f17-287">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-287">False</span></span>                           |
| <span data-ttu-id="92f17-288">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="92f17-288">In Global Catalog</span></span>      | <span data-ttu-id="92f17-289">Falso</span><span class="sxs-lookup"><span data-stu-id="92f17-289">False</span></span>                           |
| <span data-ttu-id="92f17-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="92f17-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="92f17-291">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="92f17-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="92f17-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92f17-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="92f17-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92f17-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="92f17-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-294">Search-Flags</span></span>           | <span data-ttu-id="92f17-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92f17-295">0x00000000</span></span>                      |
| <span data-ttu-id="92f17-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92f17-296">System-Flags</span></span>           | <span data-ttu-id="92f17-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92f17-297">0x00000010</span></span>                      |
| <span data-ttu-id="92f17-298">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="92f17-298">Classes used in</span></span>        | [<span data-ttu-id="92f17-299">**Início**</span><span class="sxs-lookup"><span data-stu-id="92f17-299">**Top**</span></span>](c-top.md)<br/> |



 

 





