---
title: Modificar-atributo de carimbo de data/hora
description: Um atributo computado que representa a data em que esse objeto foi alterado pela última vez. Esse valor não é replicado.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- Modificar-esquema de atributos do atributo de carimbo de data/hora
- Esquema de AD do atributo modifyTimeStamp
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645359"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="a923b-106">Modificar-atributo de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="a923b-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="a923b-107">Um atributo computado que representa a data em que esse objeto foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="a923b-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="a923b-108">Esse valor não é replicado.</span><span class="sxs-lookup"><span data-stu-id="a923b-108">This value is not replicated.</span></span>



| <span data-ttu-id="a923b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-109">Entry</span></span> | <span data-ttu-id="a923b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="a923b-111">CN</span><span class="sxs-lookup"><span data-stu-id="a923b-111">CN</span></span>                | <span data-ttu-id="a923b-112">Modificar-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="a923b-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="a923b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a923b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a923b-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="a923b-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="a923b-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a923b-115">Size</span></span>              | <span data-ttu-id="a923b-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="a923b-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="a923b-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a923b-117">Update Privilege</span></span>  | <span data-ttu-id="a923b-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a923b-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="a923b-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a923b-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="a923b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-120">Attribute-Id</span></span>      | <span data-ttu-id="a923b-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="a923b-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="a923b-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a923b-122">System-Id-Guid</span></span>    | <span data-ttu-id="a923b-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="a923b-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="a923b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="a923b-124">Syntax</span></span>            | [<span data-ttu-id="a923b-125">**Cadeia de caracteres (em tempo geral)**</span><span class="sxs-lookup"><span data-stu-id="a923b-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="a923b-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="a923b-126">Implementations</span></span>

-   [<span data-ttu-id="a923b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a923b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a923b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a923b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a923b-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a923b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a923b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a923b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a923b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a923b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a923b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a923b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a923b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a923b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a923b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a923b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a923b-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-135">Entry</span></span> | <span data-ttu-id="a923b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-139">System-Only</span></span>            | <span data-ttu-id="a923b-140">True</span><span class="sxs-lookup"><span data-stu-id="a923b-140">True</span></span>                                                                        |
| <span data-ttu-id="a923b-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-142">True</span><span class="sxs-lookup"><span data-stu-id="a923b-142">True</span></span>                                                                        |
| <span data-ttu-id="a923b-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-143">Is Indexed</span></span>             | <span data-ttu-id="a923b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-144">False</span></span>                                                                       |
| <span data-ttu-id="a923b-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-145">In Global Catalog</span></span>      | <span data-ttu-id="a923b-146">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-146">False</span></span>                                                                       |
| <span data-ttu-id="a923b-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-151">Search-Flags</span></span>           | <span data-ttu-id="a923b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-153">System-Flags</span></span>           | <span data-ttu-id="a923b-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-155">Classes used in</span></span>        | [<span data-ttu-id="a923b-156">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a923b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a923b-158">Windows Server 2003</span></span>



| <span data-ttu-id="a923b-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-159">Entry</span></span> | <span data-ttu-id="a923b-160">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-163">System-Only</span></span>            | <span data-ttu-id="a923b-164">True</span><span class="sxs-lookup"><span data-stu-id="a923b-164">True</span></span>                                                                        |
| <span data-ttu-id="a923b-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-166">True</span><span class="sxs-lookup"><span data-stu-id="a923b-166">True</span></span>                                                                        |
| <span data-ttu-id="a923b-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-167">Is Indexed</span></span>             | <span data-ttu-id="a923b-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-168">False</span></span>                                                                       |
| <span data-ttu-id="a923b-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-169">In Global Catalog</span></span>      | <span data-ttu-id="a923b-170">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-170">False</span></span>                                                                       |
| <span data-ttu-id="a923b-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-175">Search-Flags</span></span>           | <span data-ttu-id="a923b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-177">System-Flags</span></span>           | <span data-ttu-id="a923b-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-179">Classes used in</span></span>        | [<span data-ttu-id="a923b-180">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a923b-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="a923b-182">ADAM</span></span>



| <span data-ttu-id="a923b-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-183">Entry</span></span> | <span data-ttu-id="a923b-184">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-187">System-Only</span></span>            | <span data-ttu-id="a923b-188">True</span><span class="sxs-lookup"><span data-stu-id="a923b-188">True</span></span>                                                                        |
| <span data-ttu-id="a923b-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-190">True</span><span class="sxs-lookup"><span data-stu-id="a923b-190">True</span></span>                                                                        |
| <span data-ttu-id="a923b-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-191">Is Indexed</span></span>             | <span data-ttu-id="a923b-192">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-192">False</span></span>                                                                       |
| <span data-ttu-id="a923b-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-193">In Global Catalog</span></span>      | <span data-ttu-id="a923b-194">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-194">False</span></span>                                                                       |
| <span data-ttu-id="a923b-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-199">Search-Flags</span></span>           | <span data-ttu-id="a923b-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-201">System-Flags</span></span>           | <span data-ttu-id="a923b-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-203">Classes used in</span></span>        | [<span data-ttu-id="a923b-204">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-205">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a923b-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a923b-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a923b-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-207">Entry</span></span> | <span data-ttu-id="a923b-208">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-211">System-Only</span></span>            | <span data-ttu-id="a923b-212">True</span><span class="sxs-lookup"><span data-stu-id="a923b-212">True</span></span>                                                                        |
| <span data-ttu-id="a923b-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-214">True</span><span class="sxs-lookup"><span data-stu-id="a923b-214">True</span></span>                                                                        |
| <span data-ttu-id="a923b-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-215">Is Indexed</span></span>             | <span data-ttu-id="a923b-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-216">False</span></span>                                                                       |
| <span data-ttu-id="a923b-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-217">In Global Catalog</span></span>      | <span data-ttu-id="a923b-218">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-218">False</span></span>                                                                       |
| <span data-ttu-id="a923b-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-223">Search-Flags</span></span>           | <span data-ttu-id="a923b-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-225">System-Flags</span></span>           | <span data-ttu-id="a923b-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-227">Classes used in</span></span>        | [<span data-ttu-id="a923b-228">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-229">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a923b-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a923b-230">Windows Server 2008</span></span>



| <span data-ttu-id="a923b-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-231">Entry</span></span> | <span data-ttu-id="a923b-232">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-235">System-Only</span></span>            | <span data-ttu-id="a923b-236">True</span><span class="sxs-lookup"><span data-stu-id="a923b-236">True</span></span>                                                                        |
| <span data-ttu-id="a923b-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-238">True</span><span class="sxs-lookup"><span data-stu-id="a923b-238">True</span></span>                                                                        |
| <span data-ttu-id="a923b-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-239">Is Indexed</span></span>             | <span data-ttu-id="a923b-240">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-240">False</span></span>                                                                       |
| <span data-ttu-id="a923b-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-241">In Global Catalog</span></span>      | <span data-ttu-id="a923b-242">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-242">False</span></span>                                                                       |
| <span data-ttu-id="a923b-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-247">Search-Flags</span></span>           | <span data-ttu-id="a923b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-249">System-Flags</span></span>           | <span data-ttu-id="a923b-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-251">Classes used in</span></span>        | [<span data-ttu-id="a923b-252">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-253">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a923b-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a923b-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a923b-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-255">Entry</span></span> | <span data-ttu-id="a923b-256">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-259">System-Only</span></span>            | <span data-ttu-id="a923b-260">True</span><span class="sxs-lookup"><span data-stu-id="a923b-260">True</span></span>                                                                        |
| <span data-ttu-id="a923b-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-261">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-262">True</span><span class="sxs-lookup"><span data-stu-id="a923b-262">True</span></span>                                                                        |
| <span data-ttu-id="a923b-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-263">Is Indexed</span></span>             | <span data-ttu-id="a923b-264">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-264">False</span></span>                                                                       |
| <span data-ttu-id="a923b-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-265">In Global Catalog</span></span>      | <span data-ttu-id="a923b-266">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-266">False</span></span>                                                                       |
| <span data-ttu-id="a923b-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-271">Search-Flags</span></span>           | <span data-ttu-id="a923b-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-273">System-Flags</span></span>           | <span data-ttu-id="a923b-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-275">Classes used in</span></span>        | [<span data-ttu-id="a923b-276">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-277">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a923b-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a923b-278">Windows Server 2012</span></span>



| <span data-ttu-id="a923b-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="a923b-279">Entry</span></span> | <span data-ttu-id="a923b-280">Valor</span><span class="sxs-lookup"><span data-stu-id="a923b-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a923b-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="a923b-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a923b-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="a923b-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="a923b-283">System-Only</span></span>            | <span data-ttu-id="a923b-284">True</span><span class="sxs-lookup"><span data-stu-id="a923b-284">True</span></span>                                                                        |
| <span data-ttu-id="a923b-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a923b-285">Is-Single-Valued</span></span>       | <span data-ttu-id="a923b-286">True</span><span class="sxs-lookup"><span data-stu-id="a923b-286">True</span></span>                                                                        |
| <span data-ttu-id="a923b-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="a923b-287">Is Indexed</span></span>             | <span data-ttu-id="a923b-288">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-288">False</span></span>                                                                       |
| <span data-ttu-id="a923b-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a923b-289">In Global Catalog</span></span>      | <span data-ttu-id="a923b-290">Falso</span><span class="sxs-lookup"><span data-stu-id="a923b-290">False</span></span>                                                                       |
| <span data-ttu-id="a923b-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a923b-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="a923b-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a923b-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="a923b-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a923b-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a923b-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="a923b-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-295">Search-Flags</span></span>           | <span data-ttu-id="a923b-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a923b-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="a923b-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a923b-297">System-Flags</span></span>           | <span data-ttu-id="a923b-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a923b-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="a923b-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a923b-299">Classes used in</span></span>        | [<span data-ttu-id="a923b-300">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a923b-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="a923b-301">**Início**</span><span class="sxs-lookup"><span data-stu-id="a923b-301">**Top**</span></span>](c-top.md)<br/> |



 

 





