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
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="6901a-106">Modificar-atributo de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="6901a-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="6901a-107">Um atributo computado que representa a data em que esse objeto foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="6901a-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="6901a-108">Esse valor não é replicado.</span><span class="sxs-lookup"><span data-stu-id="6901a-108">This value is not replicated.</span></span>



| <span data-ttu-id="6901a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-109">Entry</span></span> | <span data-ttu-id="6901a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="6901a-111">CN</span><span class="sxs-lookup"><span data-stu-id="6901a-111">CN</span></span>                | <span data-ttu-id="6901a-112">Modificar-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="6901a-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="6901a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6901a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6901a-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="6901a-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="6901a-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6901a-115">Size</span></span>              | <span data-ttu-id="6901a-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="6901a-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="6901a-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6901a-117">Update Privilege</span></span>  | <span data-ttu-id="6901a-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6901a-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="6901a-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6901a-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="6901a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-120">Attribute-Id</span></span>      | <span data-ttu-id="6901a-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="6901a-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="6901a-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6901a-122">System-Id-Guid</span></span>    | <span data-ttu-id="6901a-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6901a-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="6901a-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6901a-124">Syntax</span></span>            | [<span data-ttu-id="6901a-125">**Cadeia de caracteres (em tempo geral)**</span><span class="sxs-lookup"><span data-stu-id="6901a-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="6901a-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="6901a-126">Implementations</span></span>

-   [<span data-ttu-id="6901a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6901a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6901a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6901a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6901a-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6901a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6901a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6901a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6901a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6901a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6901a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6901a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6901a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6901a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6901a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6901a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6901a-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-135">Entry</span></span> | <span data-ttu-id="6901a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-139">System-Only</span></span>            | <span data-ttu-id="6901a-140">True</span><span class="sxs-lookup"><span data-stu-id="6901a-140">True</span></span>                                                                        |
| <span data-ttu-id="6901a-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-142">True</span><span class="sxs-lookup"><span data-stu-id="6901a-142">True</span></span>                                                                        |
| <span data-ttu-id="6901a-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-143">Is Indexed</span></span>             | <span data-ttu-id="6901a-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-144">False</span></span>                                                                       |
| <span data-ttu-id="6901a-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-145">In Global Catalog</span></span>      | <span data-ttu-id="6901a-146">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-146">False</span></span>                                                                       |
| <span data-ttu-id="6901a-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-151">Search-Flags</span></span>           | <span data-ttu-id="6901a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-153">System-Flags</span></span>           | <span data-ttu-id="6901a-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-155">Classes used in</span></span>        | [<span data-ttu-id="6901a-156">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6901a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6901a-158">Windows Server 2003</span></span>



| <span data-ttu-id="6901a-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-159">Entry</span></span> | <span data-ttu-id="6901a-160">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-163">System-Only</span></span>            | <span data-ttu-id="6901a-164">True</span><span class="sxs-lookup"><span data-stu-id="6901a-164">True</span></span>                                                                        |
| <span data-ttu-id="6901a-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-166">True</span><span class="sxs-lookup"><span data-stu-id="6901a-166">True</span></span>                                                                        |
| <span data-ttu-id="6901a-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-167">Is Indexed</span></span>             | <span data-ttu-id="6901a-168">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-168">False</span></span>                                                                       |
| <span data-ttu-id="6901a-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-169">In Global Catalog</span></span>      | <span data-ttu-id="6901a-170">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-170">False</span></span>                                                                       |
| <span data-ttu-id="6901a-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-175">Search-Flags</span></span>           | <span data-ttu-id="6901a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-177">System-Flags</span></span>           | <span data-ttu-id="6901a-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-179">Classes used in</span></span>        | [<span data-ttu-id="6901a-180">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6901a-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="6901a-182">ADAM</span></span>



| <span data-ttu-id="6901a-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-183">Entry</span></span> | <span data-ttu-id="6901a-184">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-187">System-Only</span></span>            | <span data-ttu-id="6901a-188">True</span><span class="sxs-lookup"><span data-stu-id="6901a-188">True</span></span>                                                                        |
| <span data-ttu-id="6901a-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-190">True</span><span class="sxs-lookup"><span data-stu-id="6901a-190">True</span></span>                                                                        |
| <span data-ttu-id="6901a-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-191">Is Indexed</span></span>             | <span data-ttu-id="6901a-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-192">False</span></span>                                                                       |
| <span data-ttu-id="6901a-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-193">In Global Catalog</span></span>      | <span data-ttu-id="6901a-194">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-194">False</span></span>                                                                       |
| <span data-ttu-id="6901a-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-199">Search-Flags</span></span>           | <span data-ttu-id="6901a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-201">System-Flags</span></span>           | <span data-ttu-id="6901a-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-203">Classes used in</span></span>        | [<span data-ttu-id="6901a-204">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-205">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6901a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6901a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6901a-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-207">Entry</span></span> | <span data-ttu-id="6901a-208">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-211">System-Only</span></span>            | <span data-ttu-id="6901a-212">True</span><span class="sxs-lookup"><span data-stu-id="6901a-212">True</span></span>                                                                        |
| <span data-ttu-id="6901a-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-214">True</span><span class="sxs-lookup"><span data-stu-id="6901a-214">True</span></span>                                                                        |
| <span data-ttu-id="6901a-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-215">Is Indexed</span></span>             | <span data-ttu-id="6901a-216">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-216">False</span></span>                                                                       |
| <span data-ttu-id="6901a-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-217">In Global Catalog</span></span>      | <span data-ttu-id="6901a-218">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-218">False</span></span>                                                                       |
| <span data-ttu-id="6901a-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-223">Search-Flags</span></span>           | <span data-ttu-id="6901a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-225">System-Flags</span></span>           | <span data-ttu-id="6901a-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-227">Classes used in</span></span>        | [<span data-ttu-id="6901a-228">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-229">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6901a-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6901a-230">Windows Server 2008</span></span>



| <span data-ttu-id="6901a-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-231">Entry</span></span> | <span data-ttu-id="6901a-232">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-235">System-Only</span></span>            | <span data-ttu-id="6901a-236">True</span><span class="sxs-lookup"><span data-stu-id="6901a-236">True</span></span>                                                                        |
| <span data-ttu-id="6901a-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-237">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-238">True</span><span class="sxs-lookup"><span data-stu-id="6901a-238">True</span></span>                                                                        |
| <span data-ttu-id="6901a-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-239">Is Indexed</span></span>             | <span data-ttu-id="6901a-240">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-240">False</span></span>                                                                       |
| <span data-ttu-id="6901a-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-241">In Global Catalog</span></span>      | <span data-ttu-id="6901a-242">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-242">False</span></span>                                                                       |
| <span data-ttu-id="6901a-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-247">Search-Flags</span></span>           | <span data-ttu-id="6901a-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-249">System-Flags</span></span>           | <span data-ttu-id="6901a-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-251">Classes used in</span></span>        | [<span data-ttu-id="6901a-252">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-253">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6901a-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6901a-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6901a-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-255">Entry</span></span> | <span data-ttu-id="6901a-256">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-259">System-Only</span></span>            | <span data-ttu-id="6901a-260">True</span><span class="sxs-lookup"><span data-stu-id="6901a-260">True</span></span>                                                                        |
| <span data-ttu-id="6901a-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-261">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-262">True</span><span class="sxs-lookup"><span data-stu-id="6901a-262">True</span></span>                                                                        |
| <span data-ttu-id="6901a-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-263">Is Indexed</span></span>             | <span data-ttu-id="6901a-264">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-264">False</span></span>                                                                       |
| <span data-ttu-id="6901a-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-265">In Global Catalog</span></span>      | <span data-ttu-id="6901a-266">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-266">False</span></span>                                                                       |
| <span data-ttu-id="6901a-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-271">Search-Flags</span></span>           | <span data-ttu-id="6901a-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-273">System-Flags</span></span>           | <span data-ttu-id="6901a-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-275">Classes used in</span></span>        | [<span data-ttu-id="6901a-276">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-277">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6901a-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6901a-278">Windows Server 2012</span></span>



| <span data-ttu-id="6901a-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="6901a-279">Entry</span></span> | <span data-ttu-id="6901a-280">Valor</span><span class="sxs-lookup"><span data-stu-id="6901a-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6901a-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="6901a-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6901a-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="6901a-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="6901a-283">System-Only</span></span>            | <span data-ttu-id="6901a-284">True</span><span class="sxs-lookup"><span data-stu-id="6901a-284">True</span></span>                                                                        |
| <span data-ttu-id="6901a-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6901a-285">Is-Single-Valued</span></span>       | <span data-ttu-id="6901a-286">True</span><span class="sxs-lookup"><span data-stu-id="6901a-286">True</span></span>                                                                        |
| <span data-ttu-id="6901a-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="6901a-287">Is Indexed</span></span>             | <span data-ttu-id="6901a-288">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-288">False</span></span>                                                                       |
| <span data-ttu-id="6901a-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6901a-289">In Global Catalog</span></span>      | <span data-ttu-id="6901a-290">Falso</span><span class="sxs-lookup"><span data-stu-id="6901a-290">False</span></span>                                                                       |
| <span data-ttu-id="6901a-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6901a-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="6901a-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6901a-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="6901a-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6901a-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6901a-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="6901a-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-295">Search-Flags</span></span>           | <span data-ttu-id="6901a-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6901a-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="6901a-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6901a-297">System-Flags</span></span>           | <span data-ttu-id="6901a-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6901a-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="6901a-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6901a-299">Classes used in</span></span>        | [<span data-ttu-id="6901a-300">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="6901a-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="6901a-301">**Início**</span><span class="sxs-lookup"><span data-stu-id="6901a-301">**Top**</span></span>](c-top.md)<br/> |



 

 





