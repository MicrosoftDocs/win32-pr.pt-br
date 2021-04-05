---
title: Atributo de subclasse
description: A classe pai de uma classe.
ms.assetid: ff2afb13-5d72-4b8b-9e66-c16fb0ae5e88
ms.tgt_platform: multiple
keywords:
- Subclasse-do atributo AD Schema
- Esquema de AD do atributo listas SubClassOf
topic_type:
- apiref
api_name:
- Sub-Class-Of
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90c1e431e8c1e501731070359d379436973ef67
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086832"
---
# <a name="sub-class-of-attribute"></a><span data-ttu-id="b66d2-105">Atributo de subclasse</span><span class="sxs-lookup"><span data-stu-id="b66d2-105">Sub-Class-Of attribute</span></span>

<span data-ttu-id="b66d2-106">A classe pai de uma classe.</span><span class="sxs-lookup"><span data-stu-id="b66d2-106">The parent class of a class.</span></span>



| <span data-ttu-id="b66d2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-107">Entry</span></span> | <span data-ttu-id="b66d2-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b66d2-109">CN</span><span class="sxs-lookup"><span data-stu-id="b66d2-109">CN</span></span>                | <span data-ttu-id="b66d2-110">Subclasse de</span><span class="sxs-lookup"><span data-stu-id="b66d2-110">Sub-Class-Of</span></span>                                                    |
| <span data-ttu-id="b66d2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b66d2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b66d2-112">subClassOf</span><span class="sxs-lookup"><span data-stu-id="b66d2-112">subClassOf</span></span>                                                      |
| <span data-ttu-id="b66d2-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b66d2-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="b66d2-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b66d2-114">Update Privilege</span></span>  | <span data-ttu-id="b66d2-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="b66d2-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="b66d2-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b66d2-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="b66d2-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-117">Attribute-Id</span></span>      | <span data-ttu-id="b66d2-118">1.2.840.113556.1.2.21</span><span class="sxs-lookup"><span data-stu-id="b66d2-118">1.2.840.113556.1.2.21</span></span>                                           |
| <span data-ttu-id="b66d2-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b66d2-119">System-Id-Guid</span></span>    | <span data-ttu-id="b66d2-120">bf967a3b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b66d2-120">bf967a3b-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="b66d2-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="b66d2-121">Syntax</span></span>            | [<span data-ttu-id="b66d2-122">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="b66d2-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="b66d2-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="b66d2-123">Implementations</span></span>

-   [<span data-ttu-id="b66d2-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b66d2-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b66d2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b66d2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b66d2-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b66d2-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b66d2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b66d2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b66d2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b66d2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b66d2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b66d2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b66d2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b66d2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b66d2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b66d2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b66d2-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-132">Entry</span></span> | <span data-ttu-id="b66d2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-136">System-Only</span></span>            | <span data-ttu-id="b66d2-137">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-137">True</span></span>                                             |
| <span data-ttu-id="b66d2-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-139">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-139">True</span></span>                                             |
| <span data-ttu-id="b66d2-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-140">Is Indexed</span></span>             | <span data-ttu-id="b66d2-141">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-141">False</span></span>                                            |
| <span data-ttu-id="b66d2-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-142">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-143">False</span></span>                                            |
| <span data-ttu-id="b66d2-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-148">Search-Flags</span></span>           | <span data-ttu-id="b66d2-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-149">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-150">System-Flags</span></span>           | <span data-ttu-id="b66d2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-151">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-152">Classes used in</span></span>        | [<span data-ttu-id="b66d2-153">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b66d2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b66d2-154">Windows Server 2003</span></span>



| <span data-ttu-id="b66d2-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-155">Entry</span></span> | <span data-ttu-id="b66d2-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-159">System-Only</span></span>            | <span data-ttu-id="b66d2-160">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-160">True</span></span>                                             |
| <span data-ttu-id="b66d2-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-162">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-162">True</span></span>                                             |
| <span data-ttu-id="b66d2-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-163">Is Indexed</span></span>             | <span data-ttu-id="b66d2-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-164">False</span></span>                                            |
| <span data-ttu-id="b66d2-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-165">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-166">False</span></span>                                            |
| <span data-ttu-id="b66d2-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-171">Search-Flags</span></span>           | <span data-ttu-id="b66d2-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-172">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-173">System-Flags</span></span>           | <span data-ttu-id="b66d2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-174">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-175">Classes used in</span></span>        | [<span data-ttu-id="b66d2-176">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b66d2-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="b66d2-177">ADAM</span></span>



| <span data-ttu-id="b66d2-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-178">Entry</span></span> | <span data-ttu-id="b66d2-179">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-182">System-Only</span></span>            | <span data-ttu-id="b66d2-183">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-183">True</span></span>                                             |
| <span data-ttu-id="b66d2-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-185">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-185">True</span></span>                                             |
| <span data-ttu-id="b66d2-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-186">Is Indexed</span></span>             | <span data-ttu-id="b66d2-187">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-187">False</span></span>                                            |
| <span data-ttu-id="b66d2-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-188">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-189">False</span></span>                                            |
| <span data-ttu-id="b66d2-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-194">Search-Flags</span></span>           | <span data-ttu-id="b66d2-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-195">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-196">System-Flags</span></span>           | <span data-ttu-id="b66d2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-197">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-198">Classes used in</span></span>        | [<span data-ttu-id="b66d2-199">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b66d2-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b66d2-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b66d2-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-201">Entry</span></span> | <span data-ttu-id="b66d2-202">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-205">System-Only</span></span>            | <span data-ttu-id="b66d2-206">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-206">True</span></span>                                             |
| <span data-ttu-id="b66d2-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-208">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-208">True</span></span>                                             |
| <span data-ttu-id="b66d2-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-209">Is Indexed</span></span>             | <span data-ttu-id="b66d2-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-210">False</span></span>                                            |
| <span data-ttu-id="b66d2-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-211">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-212">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-212">False</span></span>                                            |
| <span data-ttu-id="b66d2-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-217">Search-Flags</span></span>           | <span data-ttu-id="b66d2-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-218">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-219">System-Flags</span></span>           | <span data-ttu-id="b66d2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-220">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-221">Classes used in</span></span>        | [<span data-ttu-id="b66d2-222">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b66d2-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b66d2-223">Windows Server 2008</span></span>



| <span data-ttu-id="b66d2-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-224">Entry</span></span> | <span data-ttu-id="b66d2-225">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-228">System-Only</span></span>            | <span data-ttu-id="b66d2-229">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-229">True</span></span>                                             |
| <span data-ttu-id="b66d2-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-231">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-231">True</span></span>                                             |
| <span data-ttu-id="b66d2-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-232">Is Indexed</span></span>             | <span data-ttu-id="b66d2-233">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-233">False</span></span>                                            |
| <span data-ttu-id="b66d2-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-234">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-235">False</span></span>                                            |
| <span data-ttu-id="b66d2-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-240">Search-Flags</span></span>           | <span data-ttu-id="b66d2-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-241">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-242">System-Flags</span></span>           | <span data-ttu-id="b66d2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-243">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-244">Classes used in</span></span>        | [<span data-ttu-id="b66d2-245">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b66d2-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b66d2-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b66d2-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-247">Entry</span></span> | <span data-ttu-id="b66d2-248">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-251">System-Only</span></span>            | <span data-ttu-id="b66d2-252">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-252">True</span></span>                                             |
| <span data-ttu-id="b66d2-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-254">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-254">True</span></span>                                             |
| <span data-ttu-id="b66d2-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-255">Is Indexed</span></span>             | <span data-ttu-id="b66d2-256">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-256">False</span></span>                                            |
| <span data-ttu-id="b66d2-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-257">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-258">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-258">False</span></span>                                            |
| <span data-ttu-id="b66d2-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-263">Search-Flags</span></span>           | <span data-ttu-id="b66d2-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-264">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-265">System-Flags</span></span>           | <span data-ttu-id="b66d2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-266">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-267">Classes used in</span></span>        | [<span data-ttu-id="b66d2-268">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b66d2-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b66d2-269">Windows Server 2012</span></span>



| <span data-ttu-id="b66d2-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="b66d2-270">Entry</span></span> | <span data-ttu-id="b66d2-271">Valor</span><span class="sxs-lookup"><span data-stu-id="b66d2-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="b66d2-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="b66d2-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b66d2-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="b66d2-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="b66d2-274">System-Only</span></span>            | <span data-ttu-id="b66d2-275">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-275">True</span></span>                                             |
| <span data-ttu-id="b66d2-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b66d2-276">Is-Single-Valued</span></span>       | <span data-ttu-id="b66d2-277">True</span><span class="sxs-lookup"><span data-stu-id="b66d2-277">True</span></span>                                             |
| <span data-ttu-id="b66d2-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="b66d2-278">Is Indexed</span></span>             | <span data-ttu-id="b66d2-279">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-279">False</span></span>                                            |
| <span data-ttu-id="b66d2-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b66d2-280">In Global Catalog</span></span>      | <span data-ttu-id="b66d2-281">Falso</span><span class="sxs-lookup"><span data-stu-id="b66d2-281">False</span></span>                                            |
| <span data-ttu-id="b66d2-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b66d2-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="b66d2-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b66d2-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="b66d2-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b66d2-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b66d2-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="b66d2-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-286">Search-Flags</span></span>           | <span data-ttu-id="b66d2-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b66d2-287">0x00000008</span></span>                                       |
| <span data-ttu-id="b66d2-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b66d2-288">System-Flags</span></span>           | <span data-ttu-id="b66d2-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b66d2-289">0x00000010</span></span>                                       |
| <span data-ttu-id="b66d2-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b66d2-290">Classes used in</span></span>        | [<span data-ttu-id="b66d2-291">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="b66d2-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





