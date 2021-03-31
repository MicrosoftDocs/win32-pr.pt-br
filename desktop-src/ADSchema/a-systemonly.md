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
# <a name="system-only-attribute"></a><span data-ttu-id="3c30f-106">System-Only atributo</span><span class="sxs-lookup"><span data-stu-id="3c30f-106">System-Only attribute</span></span>

<span data-ttu-id="3c30f-107">Um valor booliano que especifica se apenas Active Directory pode modificar a classe.</span><span class="sxs-lookup"><span data-stu-id="3c30f-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="3c30f-108">Classes somente de sistema só podem ser criadas ou excluídas pelo agente do sistema de diretório.</span><span class="sxs-lookup"><span data-stu-id="3c30f-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="3c30f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-109">Entry</span></span> | <span data-ttu-id="3c30f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="3c30f-111">CN</span><span class="sxs-lookup"><span data-stu-id="3c30f-111">CN</span></span>                | <span data-ttu-id="3c30f-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-112">System-Only</span></span>                          |
| <span data-ttu-id="3c30f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3c30f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3c30f-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="3c30f-114">systemOnly</span></span>                           |
| <span data-ttu-id="3c30f-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3c30f-115">Size</span></span>              | <span data-ttu-id="3c30f-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="3c30f-116">4 bytes</span></span>                              |
| <span data-ttu-id="3c30f-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3c30f-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="3c30f-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3c30f-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="3c30f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-119">Attribute-Id</span></span>      | <span data-ttu-id="3c30f-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="3c30f-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="3c30f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3c30f-121">System-Id-Guid</span></span>    | <span data-ttu-id="3c30f-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3c30f-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="3c30f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c30f-123">Syntax</span></span>            | [<span data-ttu-id="3c30f-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3c30f-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="3c30f-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="3c30f-125">Implementations</span></span>

-   [<span data-ttu-id="3c30f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3c30f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3c30f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3c30f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3c30f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3c30f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3c30f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3c30f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3c30f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3c30f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3c30f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3c30f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3c30f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3c30f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3c30f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c30f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="3c30f-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-134">Entry</span></span> | <span data-ttu-id="3c30f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-138">System-Only</span></span>            | <span data-ttu-id="3c30f-139">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-139">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-141">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-141">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-142">Is Indexed</span></span>             | <span data-ttu-id="3c30f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-143">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-144">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-145">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-150">Search-Flags</span></span>           | <span data-ttu-id="3c30f-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-152">System-Flags</span></span>           | <span data-ttu-id="3c30f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-154">Classes used in</span></span>        | [<span data-ttu-id="3c30f-155">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-156">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3c30f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c30f-157">Windows Server 2003</span></span>



| <span data-ttu-id="3c30f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-158">Entry</span></span> | <span data-ttu-id="3c30f-159">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-162">System-Only</span></span>            | <span data-ttu-id="3c30f-163">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-163">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-165">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-165">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-166">Is Indexed</span></span>             | <span data-ttu-id="3c30f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-167">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-168">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-169">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-174">Search-Flags</span></span>           | <span data-ttu-id="3c30f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-176">System-Flags</span></span>           | <span data-ttu-id="3c30f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-178">Classes used in</span></span>        | [<span data-ttu-id="3c30f-179">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-180">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3c30f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="3c30f-181">ADAM</span></span>



| <span data-ttu-id="3c30f-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-182">Entry</span></span> | <span data-ttu-id="3c30f-183">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-186">System-Only</span></span>            | <span data-ttu-id="3c30f-187">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-187">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-189">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-189">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-190">Is Indexed</span></span>             | <span data-ttu-id="3c30f-191">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-191">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-192">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-193">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-193">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-198">Search-Flags</span></span>           | <span data-ttu-id="3c30f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-200">System-Flags</span></span>           | <span data-ttu-id="3c30f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-202">Classes used in</span></span>        | [<span data-ttu-id="3c30f-203">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-204">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3c30f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3c30f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3c30f-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-206">Entry</span></span> | <span data-ttu-id="3c30f-207">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-210">System-Only</span></span>            | <span data-ttu-id="3c30f-211">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-211">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-212">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-213">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-213">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-214">Is Indexed</span></span>             | <span data-ttu-id="3c30f-215">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-215">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-216">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-217">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-217">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-222">Search-Flags</span></span>           | <span data-ttu-id="3c30f-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-224">System-Flags</span></span>           | <span data-ttu-id="3c30f-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-226">Classes used in</span></span>        | [<span data-ttu-id="3c30f-227">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-228">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3c30f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c30f-229">Windows Server 2008</span></span>



| <span data-ttu-id="3c30f-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-230">Entry</span></span> | <span data-ttu-id="3c30f-231">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-234">System-Only</span></span>            | <span data-ttu-id="3c30f-235">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-235">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-237">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-237">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-238">Is Indexed</span></span>             | <span data-ttu-id="3c30f-239">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-239">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-240">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-241">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-241">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-246">Search-Flags</span></span>           | <span data-ttu-id="3c30f-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-248">System-Flags</span></span>           | <span data-ttu-id="3c30f-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-250">Classes used in</span></span>        | [<span data-ttu-id="3c30f-251">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-252">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3c30f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c30f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3c30f-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-254">Entry</span></span> | <span data-ttu-id="3c30f-255">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-258">System-Only</span></span>            | <span data-ttu-id="3c30f-259">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-259">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-260">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-261">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-261">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-262">Is Indexed</span></span>             | <span data-ttu-id="3c30f-263">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-263">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-264">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-265">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-265">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-270">Search-Flags</span></span>           | <span data-ttu-id="3c30f-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-272">System-Flags</span></span>           | <span data-ttu-id="3c30f-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-274">Classes used in</span></span>        | [<span data-ttu-id="3c30f-275">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-276">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3c30f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c30f-277">Windows Server 2012</span></span>



| <span data-ttu-id="3c30f-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="3c30f-278">Entry</span></span> | <span data-ttu-id="3c30f-279">Valor</span><span class="sxs-lookup"><span data-stu-id="3c30f-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c30f-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="3c30f-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3c30f-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="3c30f-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="3c30f-282">System-Only</span></span>            | <span data-ttu-id="3c30f-283">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-283">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-284">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3c30f-284">Is-Single-Valued</span></span>       | <span data-ttu-id="3c30f-285">True</span><span class="sxs-lookup"><span data-stu-id="3c30f-285">True</span></span>                                                                                                      |
| <span data-ttu-id="3c30f-286">É indexado</span><span class="sxs-lookup"><span data-stu-id="3c30f-286">Is Indexed</span></span>             | <span data-ttu-id="3c30f-287">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-287">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-288">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3c30f-288">In Global Catalog</span></span>      | <span data-ttu-id="3c30f-289">Falso</span><span class="sxs-lookup"><span data-stu-id="3c30f-289">False</span></span>                                                                                                     |
| <span data-ttu-id="3c30f-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3c30f-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="3c30f-291">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3c30f-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="3c30f-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3c30f-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3c30f-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="3c30f-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-294">Search-Flags</span></span>           | <span data-ttu-id="3c30f-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3c30f-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="3c30f-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3c30f-296">System-Flags</span></span>           | <span data-ttu-id="3c30f-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c30f-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="3c30f-298">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3c30f-298">Classes used in</span></span>        | [<span data-ttu-id="3c30f-299">**Atributo-esquema**</span><span class="sxs-lookup"><span data-stu-id="3c30f-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="3c30f-300">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="3c30f-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





