---
title: Is-Defunct atributo
description: Se for TRUE, a classe ou o atributo não poderá mais ser usado. As versões antigas desse objeto podem existir, mas novas não podem ser criadas.
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- Esquema de Is-Defunct do atributo AD
- Esquema de AD de atributo isfunct
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749378"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="ceb0e-106">Is-Defunct atributo</span><span class="sxs-lookup"><span data-stu-id="ceb0e-106">Is-Defunct attribute</span></span>

<span data-ttu-id="ceb0e-107">Se **for true**, a classe ou o atributo não poderá mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="ceb0e-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="ceb0e-108">As versões antigas desse objeto podem existir, mas novas não podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="ceb0e-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="ceb0e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-109">Entry</span></span> | <span data-ttu-id="ceb0e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ceb0e-111">CN</span><span class="sxs-lookup"><span data-stu-id="ceb0e-111">CN</span></span>                | <span data-ttu-id="ceb0e-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="ceb0e-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="ceb0e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ceb0e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ceb0e-114">isDefunct</span><span class="sxs-lookup"><span data-stu-id="ceb0e-114">isDefunct</span></span>                            |
| <span data-ttu-id="ceb0e-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ceb0e-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="ceb0e-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ceb0e-116">Update Privilege</span></span>  | <span data-ttu-id="ceb0e-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="ceb0e-117">Schema administrator</span></span>                 |
| <span data-ttu-id="ceb0e-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ceb0e-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ceb0e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-119">Attribute-Id</span></span>      | <span data-ttu-id="ceb0e-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="ceb0e-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="ceb0e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ceb0e-121">System-Id-Guid</span></span>    | <span data-ttu-id="ceb0e-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ceb0e-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="ceb0e-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ceb0e-123">Syntax</span></span>            | [<span data-ttu-id="ceb0e-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="ceb0e-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="ceb0e-125">Implementations</span></span>

-   [<span data-ttu-id="ceb0e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ceb0e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ceb0e-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ceb0e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ceb0e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ceb0e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ceb0e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ceb0e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ceb0e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="ceb0e-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-134">Entry</span></span> | <span data-ttu-id="ceb0e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-138">System-Only</span></span>            | <span data-ttu-id="ceb0e-139">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-139">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-141">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-141">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-142">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-143">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-144">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-145">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-145">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-150">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-152">System-Flags</span></span>           | <span data-ttu-id="ceb0e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-154">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-155">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-156">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ceb0e-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ceb0e-157">Windows Server 2003</span></span>



| <span data-ttu-id="ceb0e-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-158">Entry</span></span> | <span data-ttu-id="ceb0e-159">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-162">System-Only</span></span>            | <span data-ttu-id="ceb0e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-163">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-165">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-165">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-166">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-167">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-168">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-169">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-169">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-174">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-176">System-Flags</span></span>           | <span data-ttu-id="ceb0e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-178">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-179">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-180">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ceb0e-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="ceb0e-181">ADAM</span></span>



| <span data-ttu-id="ceb0e-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-182">Entry</span></span> | <span data-ttu-id="ceb0e-183">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-186">System-Only</span></span>            | <span data-ttu-id="ceb0e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-187">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-189">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-189">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-190">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-191">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-191">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-192">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-193">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-193">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-198">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-200">System-Flags</span></span>           | <span data-ttu-id="ceb0e-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-202">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-203">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-204">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ceb0e-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ceb0e-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ceb0e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-206">Entry</span></span> | <span data-ttu-id="ceb0e-207">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-210">System-Only</span></span>            | <span data-ttu-id="ceb0e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-211">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-213">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-213">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-214">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-215">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-215">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-216">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-217">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-217">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-222">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-224">System-Flags</span></span>           | <span data-ttu-id="ceb0e-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-226">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-227">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-228">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ceb0e-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceb0e-229">Windows Server 2008</span></span>



| <span data-ttu-id="ceb0e-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-230">Entry</span></span> | <span data-ttu-id="ceb0e-231">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-234">System-Only</span></span>            | <span data-ttu-id="ceb0e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-235">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-236">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-237">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-237">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-238">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-239">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-239">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-240">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-241">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-241">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-246">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-248">System-Flags</span></span>           | <span data-ttu-id="ceb0e-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-250">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-251">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-252">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ceb0e-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ceb0e-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ceb0e-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-254">Entry</span></span> | <span data-ttu-id="ceb0e-255">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-258">System-Only</span></span>            | <span data-ttu-id="ceb0e-259">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-259">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-260">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-261">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-261">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-262">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-263">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-263">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-264">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-265">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-265">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-270">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-272">System-Flags</span></span>           | <span data-ttu-id="ceb0e-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-274">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-275">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-276">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ceb0e-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ceb0e-277">Windows Server 2012</span></span>



| <span data-ttu-id="ceb0e-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="ceb0e-278">Entry</span></span> | <span data-ttu-id="ceb0e-279">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0e-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="ceb0e-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ceb0e-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="ceb0e-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="ceb0e-282">System-Only</span></span>            | <span data-ttu-id="ceb0e-283">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-283">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-284">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ceb0e-284">Is-Single-Valued</span></span>       | <span data-ttu-id="ceb0e-285">True</span><span class="sxs-lookup"><span data-stu-id="ceb0e-285">True</span></span>                                                                                                      |
| <span data-ttu-id="ceb0e-286">É indexado</span><span class="sxs-lookup"><span data-stu-id="ceb0e-286">Is Indexed</span></span>             | <span data-ttu-id="ceb0e-287">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-287">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-288">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ceb0e-288">In Global Catalog</span></span>      | <span data-ttu-id="ceb0e-289">Falso</span><span class="sxs-lookup"><span data-stu-id="ceb0e-289">False</span></span>                                                                                                     |
| <span data-ttu-id="ceb0e-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ceb0e-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="ceb0e-291">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ceb0e-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="ceb0e-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ceb0e-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ceb0e-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="ceb0e-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-294">Search-Flags</span></span>           | <span data-ttu-id="ceb0e-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ceb0e-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ceb0e-296">System-Flags</span></span>           | <span data-ttu-id="ceb0e-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ceb0e-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="ceb0e-298">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ceb0e-298">Classes used in</span></span>        | [<span data-ttu-id="ceb0e-299">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="ceb0e-300">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ceb0e-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





