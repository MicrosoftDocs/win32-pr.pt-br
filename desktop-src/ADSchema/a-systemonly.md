---
title: System-Only atributo
description: Um valor booliano que especifica se apenas Active Directory pode modificar a classe. Classes somente de sistema só podem ser criadas ou excluídas pelo agente do sistema de diretório.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Esquema de System-Only do atributo AD
- Esquema de AD do atributo systemOnly
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825079"
---
# <a name="system-only-attribute"></a><span data-ttu-id="a72ec-106">System-Only atributo</span><span class="sxs-lookup"><span data-stu-id="a72ec-106">System-Only attribute</span></span>

<span data-ttu-id="a72ec-107">Um valor booliano que especifica se apenas Active Directory pode modificar a classe.</span><span class="sxs-lookup"><span data-stu-id="a72ec-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="a72ec-108">Classes somente de sistema só podem ser criadas ou excluídas pelo agente do sistema de diretório.</span><span class="sxs-lookup"><span data-stu-id="a72ec-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="a72ec-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-109">Entry</span></span> | <span data-ttu-id="a72ec-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a72ec-111">CN</span><span class="sxs-lookup"><span data-stu-id="a72ec-111">CN</span></span>                | <span data-ttu-id="a72ec-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-112">System-Only</span></span>                          |
| <span data-ttu-id="a72ec-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a72ec-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a72ec-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="a72ec-114">systemOnly</span></span>                           |
| <span data-ttu-id="a72ec-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a72ec-115">Size</span></span>              | <span data-ttu-id="a72ec-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="a72ec-116">4 bytes</span></span>                              |
| <span data-ttu-id="a72ec-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a72ec-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a72ec-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a72ec-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a72ec-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-119">Attribute-Id</span></span>      | <span data-ttu-id="a72ec-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="a72ec-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="a72ec-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a72ec-121">System-Id-Guid</span></span>    | <span data-ttu-id="a72ec-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a72ec-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a72ec-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a72ec-123">Syntax</span></span>            | [<span data-ttu-id="a72ec-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a72ec-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="a72ec-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="a72ec-125">Implementations</span></span>

-   [<span data-ttu-id="a72ec-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a72ec-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a72ec-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a72ec-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a72ec-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a72ec-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a72ec-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a72ec-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a72ec-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a72ec-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a72ec-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a72ec-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a72ec-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a72ec-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a72ec-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a72ec-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a72ec-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-134">Entry</span></span> | <span data-ttu-id="a72ec-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-138">System-Only</span></span>            | <span data-ttu-id="a72ec-139">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-139">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-141">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-141">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-142">Is Indexed</span></span>             | <span data-ttu-id="a72ec-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-143">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-144">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-145">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-145">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-150">Search-Flags</span></span>           | <span data-ttu-id="a72ec-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-152">System-Flags</span></span>           | <span data-ttu-id="a72ec-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-154">Classes used in</span></span>        | [<span data-ttu-id="a72ec-155">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-156">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a72ec-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a72ec-157">Windows Server 2003</span></span>



| <span data-ttu-id="a72ec-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-158">Entry</span></span> | <span data-ttu-id="a72ec-159">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-162">System-Only</span></span>            | <span data-ttu-id="a72ec-163">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-163">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-165">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-165">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-166">Is Indexed</span></span>             | <span data-ttu-id="a72ec-167">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-167">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-168">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-169">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-169">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-174">Search-Flags</span></span>           | <span data-ttu-id="a72ec-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-176">System-Flags</span></span>           | <span data-ttu-id="a72ec-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-178">Classes used in</span></span>        | [<span data-ttu-id="a72ec-179">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-180">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a72ec-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="a72ec-181">ADAM</span></span>



| <span data-ttu-id="a72ec-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-182">Entry</span></span> | <span data-ttu-id="a72ec-183">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-186">System-Only</span></span>            | <span data-ttu-id="a72ec-187">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-187">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-189">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-189">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-190">Is Indexed</span></span>             | <span data-ttu-id="a72ec-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-191">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-192">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-193">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-198">Search-Flags</span></span>           | <span data-ttu-id="a72ec-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-200">System-Flags</span></span>           | <span data-ttu-id="a72ec-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-202">Classes used in</span></span>        | [<span data-ttu-id="a72ec-203">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-204">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a72ec-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a72ec-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a72ec-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-206">Entry</span></span> | <span data-ttu-id="a72ec-207">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-210">System-Only</span></span>            | <span data-ttu-id="a72ec-211">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-211">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-212">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-213">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-213">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-214">Is Indexed</span></span>             | <span data-ttu-id="a72ec-215">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-215">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-216">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-217">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-217">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-222">Search-Flags</span></span>           | <span data-ttu-id="a72ec-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-224">System-Flags</span></span>           | <span data-ttu-id="a72ec-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-226">Classes used in</span></span>        | [<span data-ttu-id="a72ec-227">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-228">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a72ec-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a72ec-229">Windows Server 2008</span></span>



| <span data-ttu-id="a72ec-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-230">Entry</span></span> | <span data-ttu-id="a72ec-231">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-234">System-Only</span></span>            | <span data-ttu-id="a72ec-235">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-235">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-236">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-237">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-237">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-238">Is Indexed</span></span>             | <span data-ttu-id="a72ec-239">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-239">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-240">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-241">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-241">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-246">Search-Flags</span></span>           | <span data-ttu-id="a72ec-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-248">System-Flags</span></span>           | <span data-ttu-id="a72ec-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-250">Classes used in</span></span>        | [<span data-ttu-id="a72ec-251">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-252">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a72ec-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a72ec-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a72ec-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-254">Entry</span></span> | <span data-ttu-id="a72ec-255">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-258">System-Only</span></span>            | <span data-ttu-id="a72ec-259">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-259">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-260">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-261">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-261">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-262">Is Indexed</span></span>             | <span data-ttu-id="a72ec-263">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-263">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-264">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-265">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-265">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-270">Search-Flags</span></span>           | <span data-ttu-id="a72ec-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-272">System-Flags</span></span>           | <span data-ttu-id="a72ec-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-274">Classes used in</span></span>        | [<span data-ttu-id="a72ec-275">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-276">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a72ec-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a72ec-277">Windows Server 2012</span></span>



| <span data-ttu-id="a72ec-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="a72ec-278">Entry</span></span> | <span data-ttu-id="a72ec-279">Valor</span><span class="sxs-lookup"><span data-stu-id="a72ec-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72ec-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="a72ec-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a72ec-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="a72ec-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="a72ec-282">System-Only</span></span>            | <span data-ttu-id="a72ec-283">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-283">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-284">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a72ec-284">Is-Single-Valued</span></span>       | <span data-ttu-id="a72ec-285">True</span><span class="sxs-lookup"><span data-stu-id="a72ec-285">True</span></span>                                                                                                      |
| <span data-ttu-id="a72ec-286">É indexado</span><span class="sxs-lookup"><span data-stu-id="a72ec-286">Is Indexed</span></span>             | <span data-ttu-id="a72ec-287">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-287">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-288">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a72ec-288">In Global Catalog</span></span>      | <span data-ttu-id="a72ec-289">Falso</span><span class="sxs-lookup"><span data-stu-id="a72ec-289">False</span></span>                                                                                                     |
| <span data-ttu-id="a72ec-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a72ec-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="a72ec-291">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a72ec-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="a72ec-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a72ec-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a72ec-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="a72ec-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-294">Search-Flags</span></span>           | <span data-ttu-id="a72ec-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a72ec-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="a72ec-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a72ec-296">System-Flags</span></span>           | <span data-ttu-id="a72ec-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a72ec-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="a72ec-298">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a72ec-298">Classes used in</span></span>        | [<span data-ttu-id="a72ec-299">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="a72ec-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="a72ec-300">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="a72ec-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





