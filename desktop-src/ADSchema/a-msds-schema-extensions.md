---
title: atributo ms-DS-Schema-Extensions
description: Um BLOB binário usado para armazenar informações sobre extensões de objetos de esquema.
ms.assetid: a2ffc4c6-ec33-4265-9a1e-c07597d2af50
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-Schema-Extensions
- atributo msDs-Schema-Extensions do AD Schema
topic_type:
- apiref
api_name:
- ms-ds-Schema-Extensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f524e28f2d45d03f7851fc46d32e986968f81bfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456281"
---
# <a name="ms-ds-schema-extensions-attribute"></a><span data-ttu-id="a2429-105">atributo ms-DS-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="a2429-105">ms-ds-Schema-Extensions attribute</span></span>

<span data-ttu-id="a2429-106">Um BLOB binário usado para armazenar informações sobre extensões de objetos de esquema.</span><span class="sxs-lookup"><span data-stu-id="a2429-106">A binary BLOB used to store information about extensions to schema objects.</span></span>



| <span data-ttu-id="a2429-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-107">Entry</span></span> | <span data-ttu-id="a2429-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a2429-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2429-109">CN</span></span>                | <span data-ttu-id="a2429-110">ms-DS-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="a2429-110">ms-ds-Schema-Extensions</span></span>                               |
| <span data-ttu-id="a2429-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a2429-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2429-112">msDs-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="a2429-112">msDs-Schema-Extensions</span></span>                                |
| <span data-ttu-id="a2429-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a2429-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a2429-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a2429-114">Update Privilege</span></span>  | <span data-ttu-id="a2429-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a2429-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="a2429-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a2429-116">Update Frequency</span></span>  | <span data-ttu-id="a2429-117">Quando o esquema é estendido.</span><span class="sxs-lookup"><span data-stu-id="a2429-117">When the schema is extended.</span></span>                          |
| <span data-ttu-id="a2429-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-118">Attribute-Id</span></span>      | <span data-ttu-id="a2429-119">1.2.840.113556.1.4.1440</span><span class="sxs-lookup"><span data-stu-id="a2429-119">1.2.840.113556.1.4.1440</span></span>                               |
| <span data-ttu-id="a2429-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a2429-120">System-Id-Guid</span></span>    | <span data-ttu-id="a2429-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span><span class="sxs-lookup"><span data-stu-id="a2429-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span></span>                  |
| <span data-ttu-id="a2429-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2429-122">Syntax</span></span>            | [<span data-ttu-id="a2429-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a2429-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a2429-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="a2429-124">Implementations</span></span>

-   [<span data-ttu-id="a2429-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2429-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2429-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a2429-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a2429-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2429-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2429-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2429-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2429-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2429-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2429-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2429-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a2429-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2429-131">Windows Server 2003</span></span>



| <span data-ttu-id="a2429-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-132">Entry</span></span> | <span data-ttu-id="a2429-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2429-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="a2429-134">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-135">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2429-136">System-Only</span></span>            | <span data-ttu-id="a2429-137">True</span><span class="sxs-lookup"><span data-stu-id="a2429-137">True</span></span>                                                                                                                                      |
| <span data-ttu-id="a2429-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a2429-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a2429-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-139">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="a2429-140">Is Indexed</span></span>             | <span data-ttu-id="a2429-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-141">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2429-142">In Global Catalog</span></span>      | <span data-ttu-id="a2429-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-143">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2429-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2429-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a2429-145">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="a2429-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2429-146">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2429-147">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-148">Search-Flags</span></span>           | <span data-ttu-id="a2429-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2429-149">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-150">System-Flags</span></span>           | <span data-ttu-id="a2429-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2429-151">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a2429-152">Classes used in</span></span>        | [<span data-ttu-id="a2429-153">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a2429-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a2429-154">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a2429-154">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="a2429-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="a2429-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a2429-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="a2429-156">ADAM</span></span>



| <span data-ttu-id="a2429-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-157">Entry</span></span> | <span data-ttu-id="a2429-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2429-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="a2429-159">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-160">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2429-161">System-Only</span></span>            | <span data-ttu-id="a2429-162">True</span><span class="sxs-lookup"><span data-stu-id="a2429-162">True</span></span>                                                                                                                                      |
| <span data-ttu-id="a2429-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a2429-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a2429-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-164">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="a2429-165">Is Indexed</span></span>             | <span data-ttu-id="a2429-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-166">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2429-167">In Global Catalog</span></span>      | <span data-ttu-id="a2429-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-168">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2429-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2429-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a2429-170">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="a2429-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2429-171">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2429-172">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-173">Search-Flags</span></span>           | <span data-ttu-id="a2429-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2429-174">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-175">System-Flags</span></span>           | <span data-ttu-id="a2429-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2429-176">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a2429-177">Classes used in</span></span>        | [<span data-ttu-id="a2429-178">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a2429-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a2429-179">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a2429-179">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="a2429-180">**DMD**</span><span class="sxs-lookup"><span data-stu-id="a2429-180">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2429-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2429-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2429-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-182">Entry</span></span> | <span data-ttu-id="a2429-183">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2429-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="a2429-184">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-185">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2429-186">System-Only</span></span>            | <span data-ttu-id="a2429-187">True</span><span class="sxs-lookup"><span data-stu-id="a2429-187">True</span></span>                                                                                                                                      |
| <span data-ttu-id="a2429-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a2429-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a2429-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-189">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="a2429-190">Is Indexed</span></span>             | <span data-ttu-id="a2429-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-191">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2429-192">In Global Catalog</span></span>      | <span data-ttu-id="a2429-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-193">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2429-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2429-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a2429-195">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="a2429-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2429-196">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2429-197">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-198">Search-Flags</span></span>           | <span data-ttu-id="a2429-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2429-199">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-200">System-Flags</span></span>           | <span data-ttu-id="a2429-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2429-201">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a2429-202">Classes used in</span></span>        | [<span data-ttu-id="a2429-203">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a2429-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a2429-204">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a2429-204">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="a2429-205">**DMD**</span><span class="sxs-lookup"><span data-stu-id="a2429-205">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2429-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2429-206">Windows Server 2008</span></span>



| <span data-ttu-id="a2429-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-207">Entry</span></span> | <span data-ttu-id="a2429-208">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2429-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="a2429-209">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-210">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2429-211">System-Only</span></span>            | <span data-ttu-id="a2429-212">True</span><span class="sxs-lookup"><span data-stu-id="a2429-212">True</span></span>                                                                                                                                      |
| <span data-ttu-id="a2429-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a2429-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a2429-214">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-214">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="a2429-215">Is Indexed</span></span>             | <span data-ttu-id="a2429-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-216">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2429-217">In Global Catalog</span></span>      | <span data-ttu-id="a2429-218">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-218">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2429-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2429-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a2429-220">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="a2429-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2429-221">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2429-222">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-223">Search-Flags</span></span>           | <span data-ttu-id="a2429-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2429-224">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-225">System-Flags</span></span>           | <span data-ttu-id="a2429-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2429-226">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a2429-227">Classes used in</span></span>        | [<span data-ttu-id="a2429-228">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a2429-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a2429-229">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a2429-229">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="a2429-230">**DMD**</span><span class="sxs-lookup"><span data-stu-id="a2429-230">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2429-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2429-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2429-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-232">Entry</span></span> | <span data-ttu-id="a2429-233">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2429-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="a2429-234">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-235">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2429-236">System-Only</span></span>            | <span data-ttu-id="a2429-237">True</span><span class="sxs-lookup"><span data-stu-id="a2429-237">True</span></span>                                                                                                                                      |
| <span data-ttu-id="a2429-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a2429-238">Is-Single-Valued</span></span>       | <span data-ttu-id="a2429-239">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-239">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="a2429-240">Is Indexed</span></span>             | <span data-ttu-id="a2429-241">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-241">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2429-242">In Global Catalog</span></span>      | <span data-ttu-id="a2429-243">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-243">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2429-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2429-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a2429-245">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="a2429-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2429-246">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2429-247">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-248">Search-Flags</span></span>           | <span data-ttu-id="a2429-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2429-249">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-250">System-Flags</span></span>           | <span data-ttu-id="a2429-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2429-251">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a2429-252">Classes used in</span></span>        | [<span data-ttu-id="a2429-253">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a2429-253">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a2429-254">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a2429-254">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="a2429-255">**DMD**</span><span class="sxs-lookup"><span data-stu-id="a2429-255">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2429-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2429-256">Windows Server 2012</span></span>



| <span data-ttu-id="a2429-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2429-257">Entry</span></span> | <span data-ttu-id="a2429-258">Valor</span><span class="sxs-lookup"><span data-stu-id="a2429-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2429-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="a2429-259">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2429-260">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="a2429-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2429-261">System-Only</span></span>            | <span data-ttu-id="a2429-262">True</span><span class="sxs-lookup"><span data-stu-id="a2429-262">True</span></span>                                                                                                                                      |
| <span data-ttu-id="a2429-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a2429-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a2429-264">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-264">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="a2429-265">Is Indexed</span></span>             | <span data-ttu-id="a2429-266">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-266">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2429-267">In Global Catalog</span></span>      | <span data-ttu-id="a2429-268">Falso</span><span class="sxs-lookup"><span data-stu-id="a2429-268">False</span></span>                                                                                                                                     |
| <span data-ttu-id="a2429-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2429-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2429-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a2429-270">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="a2429-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2429-271">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2429-272">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="a2429-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-273">Search-Flags</span></span>           | <span data-ttu-id="a2429-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2429-274">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2429-275">System-Flags</span></span>           | <span data-ttu-id="a2429-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2429-276">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="a2429-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a2429-277">Classes used in</span></span>        | [<span data-ttu-id="a2429-278">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a2429-278">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a2429-279">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a2429-279">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="a2429-280">**DMD**</span><span class="sxs-lookup"><span data-stu-id="a2429-280">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





