---
title: USN-Source atributo
description: Valor do atributo USN-Changed do objeto do diretório remoto que replicou a alteração para o servidor local.
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- Esquema de USN-Source do atributo AD
- Esquema de AD do atributo uSNSource
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369968"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="baa58-105">USN-Source atributo</span><span class="sxs-lookup"><span data-stu-id="baa58-105">USN-Source attribute</span></span>

<span data-ttu-id="baa58-106">Valor do atributo [**USN-Changed**](a-usnchanged.md) do objeto do diretório remoto que replicou a alteração para o servidor local.</span><span class="sxs-lookup"><span data-stu-id="baa58-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="baa58-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-107">Entry</span></span> | <span data-ttu-id="baa58-108">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa58-109">CN</span><span class="sxs-lookup"><span data-stu-id="baa58-109">CN</span></span>                | <span data-ttu-id="baa58-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="baa58-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="baa58-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="baa58-111">Ldap-Display-Name</span></span> | <span data-ttu-id="baa58-112">uSNSource</span><span class="sxs-lookup"><span data-stu-id="baa58-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="baa58-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="baa58-113">Size</span></span>              | <span data-ttu-id="baa58-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="baa58-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="baa58-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="baa58-115">Update Privilege</span></span>  | <span data-ttu-id="baa58-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="baa58-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="baa58-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="baa58-117">Update Frequency</span></span>  | <span data-ttu-id="baa58-118">Quando o objeto é alterado em um diretório remoto que replicou a alteração para o diretório local.</span><span class="sxs-lookup"><span data-stu-id="baa58-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="baa58-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-119">Attribute-Id</span></span>      | <span data-ttu-id="baa58-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="baa58-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="baa58-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="baa58-121">System-Id-Guid</span></span>    | <span data-ttu-id="baa58-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="baa58-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="baa58-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="baa58-123">Syntax</span></span>            | [<span data-ttu-id="baa58-124">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="baa58-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="baa58-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="baa58-125">Implementations</span></span>

-   [<span data-ttu-id="baa58-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="baa58-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="baa58-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="baa58-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="baa58-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="baa58-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="baa58-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="baa58-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="baa58-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="baa58-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="baa58-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="baa58-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="baa58-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="baa58-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="baa58-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="baa58-133">Windows 2000 Server</span></span>



| <span data-ttu-id="baa58-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-134">Entry</span></span> | <span data-ttu-id="baa58-135">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-137">MAPI-Id</span></span>                | <span data-ttu-id="baa58-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-138">0x8157</span></span>                          |
| <span data-ttu-id="baa58-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-139">System-Only</span></span>            | <span data-ttu-id="baa58-140">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-140">False</span></span>                           |
| <span data-ttu-id="baa58-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-141">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-142">True</span><span class="sxs-lookup"><span data-stu-id="baa58-142">True</span></span>                            |
| <span data-ttu-id="baa58-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-143">Is Indexed</span></span>             | <span data-ttu-id="baa58-144">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-144">False</span></span>                           |
| <span data-ttu-id="baa58-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-145">In Global Catalog</span></span>      | <span data-ttu-id="baa58-146">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-146">False</span></span>                           |
| <span data-ttu-id="baa58-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-151">Search-Flags</span></span>           | <span data-ttu-id="baa58-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-152">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-153">System-Flags</span></span>           | <span data-ttu-id="baa58-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-154">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-155">Classes used in</span></span>        | [<span data-ttu-id="baa58-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="baa58-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="baa58-157">Windows Server 2003</span></span>



| <span data-ttu-id="baa58-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-158">Entry</span></span> | <span data-ttu-id="baa58-159">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-161">MAPI-Id</span></span>                | <span data-ttu-id="baa58-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-162">0x8157</span></span>                          |
| <span data-ttu-id="baa58-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-163">System-Only</span></span>            | <span data-ttu-id="baa58-164">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-164">False</span></span>                           |
| <span data-ttu-id="baa58-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-165">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-166">True</span><span class="sxs-lookup"><span data-stu-id="baa58-166">True</span></span>                            |
| <span data-ttu-id="baa58-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-167">Is Indexed</span></span>             | <span data-ttu-id="baa58-168">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-168">False</span></span>                           |
| <span data-ttu-id="baa58-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-169">In Global Catalog</span></span>      | <span data-ttu-id="baa58-170">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-170">False</span></span>                           |
| <span data-ttu-id="baa58-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-175">Search-Flags</span></span>           | <span data-ttu-id="baa58-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-176">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-177">System-Flags</span></span>           | <span data-ttu-id="baa58-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-178">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-179">Classes used in</span></span>        | [<span data-ttu-id="baa58-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="baa58-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="baa58-181">ADAM</span></span>



| <span data-ttu-id="baa58-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-182">Entry</span></span> | <span data-ttu-id="baa58-183">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-185">MAPI-Id</span></span>                | <span data-ttu-id="baa58-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-186">0x8157</span></span>                          |
| <span data-ttu-id="baa58-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-187">System-Only</span></span>            | <span data-ttu-id="baa58-188">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-188">False</span></span>                           |
| <span data-ttu-id="baa58-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-189">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-190">True</span><span class="sxs-lookup"><span data-stu-id="baa58-190">True</span></span>                            |
| <span data-ttu-id="baa58-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-191">Is Indexed</span></span>             | <span data-ttu-id="baa58-192">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-192">False</span></span>                           |
| <span data-ttu-id="baa58-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-193">In Global Catalog</span></span>      | <span data-ttu-id="baa58-194">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-194">False</span></span>                           |
| <span data-ttu-id="baa58-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-199">Search-Flags</span></span>           | <span data-ttu-id="baa58-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-200">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-201">System-Flags</span></span>           | <span data-ttu-id="baa58-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-202">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-203">Classes used in</span></span>        | [<span data-ttu-id="baa58-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="baa58-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="baa58-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="baa58-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-206">Entry</span></span> | <span data-ttu-id="baa58-207">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-209">MAPI-Id</span></span>                | <span data-ttu-id="baa58-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-210">0x8157</span></span>                          |
| <span data-ttu-id="baa58-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-211">System-Only</span></span>            | <span data-ttu-id="baa58-212">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-212">False</span></span>                           |
| <span data-ttu-id="baa58-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-213">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-214">True</span><span class="sxs-lookup"><span data-stu-id="baa58-214">True</span></span>                            |
| <span data-ttu-id="baa58-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-215">Is Indexed</span></span>             | <span data-ttu-id="baa58-216">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-216">False</span></span>                           |
| <span data-ttu-id="baa58-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-217">In Global Catalog</span></span>      | <span data-ttu-id="baa58-218">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-218">False</span></span>                           |
| <span data-ttu-id="baa58-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-223">Search-Flags</span></span>           | <span data-ttu-id="baa58-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-224">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-225">System-Flags</span></span>           | <span data-ttu-id="baa58-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-226">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-227">Classes used in</span></span>        | [<span data-ttu-id="baa58-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="baa58-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baa58-229">Windows Server 2008</span></span>



| <span data-ttu-id="baa58-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-230">Entry</span></span> | <span data-ttu-id="baa58-231">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-233">MAPI-Id</span></span>                | <span data-ttu-id="baa58-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-234">0x8157</span></span>                          |
| <span data-ttu-id="baa58-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-235">System-Only</span></span>            | <span data-ttu-id="baa58-236">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-236">False</span></span>                           |
| <span data-ttu-id="baa58-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-237">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-238">True</span><span class="sxs-lookup"><span data-stu-id="baa58-238">True</span></span>                            |
| <span data-ttu-id="baa58-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-239">Is Indexed</span></span>             | <span data-ttu-id="baa58-240">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-240">False</span></span>                           |
| <span data-ttu-id="baa58-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-241">In Global Catalog</span></span>      | <span data-ttu-id="baa58-242">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-242">False</span></span>                           |
| <span data-ttu-id="baa58-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-247">Search-Flags</span></span>           | <span data-ttu-id="baa58-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-248">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-249">System-Flags</span></span>           | <span data-ttu-id="baa58-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-250">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-251">Classes used in</span></span>        | [<span data-ttu-id="baa58-252">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="baa58-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="baa58-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="baa58-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-254">Entry</span></span> | <span data-ttu-id="baa58-255">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-257">MAPI-Id</span></span>                | <span data-ttu-id="baa58-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-258">0x8157</span></span>                          |
| <span data-ttu-id="baa58-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-259">System-Only</span></span>            | <span data-ttu-id="baa58-260">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-260">False</span></span>                           |
| <span data-ttu-id="baa58-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-261">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-262">True</span><span class="sxs-lookup"><span data-stu-id="baa58-262">True</span></span>                            |
| <span data-ttu-id="baa58-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-263">Is Indexed</span></span>             | <span data-ttu-id="baa58-264">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-264">False</span></span>                           |
| <span data-ttu-id="baa58-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-265">In Global Catalog</span></span>      | <span data-ttu-id="baa58-266">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-266">False</span></span>                           |
| <span data-ttu-id="baa58-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-271">Search-Flags</span></span>           | <span data-ttu-id="baa58-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-272">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-273">System-Flags</span></span>           | <span data-ttu-id="baa58-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-274">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-275">Classes used in</span></span>        | [<span data-ttu-id="baa58-276">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="baa58-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="baa58-277">Windows Server 2012</span></span>



| <span data-ttu-id="baa58-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="baa58-278">Entry</span></span> | <span data-ttu-id="baa58-279">Valor</span><span class="sxs-lookup"><span data-stu-id="baa58-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="baa58-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="baa58-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="baa58-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="baa58-281">MAPI-Id</span></span>                | <span data-ttu-id="baa58-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="baa58-282">0x8157</span></span>                          |
| <span data-ttu-id="baa58-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="baa58-283">System-Only</span></span>            | <span data-ttu-id="baa58-284">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-284">False</span></span>                           |
| <span data-ttu-id="baa58-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="baa58-285">Is-Single-Valued</span></span>       | <span data-ttu-id="baa58-286">True</span><span class="sxs-lookup"><span data-stu-id="baa58-286">True</span></span>                            |
| <span data-ttu-id="baa58-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="baa58-287">Is Indexed</span></span>             | <span data-ttu-id="baa58-288">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-288">False</span></span>                           |
| <span data-ttu-id="baa58-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="baa58-289">In Global Catalog</span></span>      | <span data-ttu-id="baa58-290">Falso</span><span class="sxs-lookup"><span data-stu-id="baa58-290">False</span></span>                           |
| <span data-ttu-id="baa58-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="baa58-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="baa58-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="baa58-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="baa58-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="baa58-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="baa58-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="baa58-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="baa58-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-295">Search-Flags</span></span>           | <span data-ttu-id="baa58-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="baa58-296">0x00000000</span></span>                      |
| <span data-ttu-id="baa58-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="baa58-297">System-Flags</span></span>           | <span data-ttu-id="baa58-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="baa58-298">0x00000010</span></span>                      |
| <span data-ttu-id="baa58-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="baa58-299">Classes used in</span></span>        | [<span data-ttu-id="baa58-300">**Início**</span><span class="sxs-lookup"><span data-stu-id="baa58-300">**Top**</span></span>](c-top.md)<br/> |



 

 





