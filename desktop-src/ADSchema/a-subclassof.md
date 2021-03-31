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
# <a name="sub-class-of-attribute"></a><span data-ttu-id="ee0c3-105">Atributo de subclasse</span><span class="sxs-lookup"><span data-stu-id="ee0c3-105">Sub-Class-Of attribute</span></span>

<span data-ttu-id="ee0c3-106">A classe pai de uma classe.</span><span class="sxs-lookup"><span data-stu-id="ee0c3-106">The parent class of a class.</span></span>



| <span data-ttu-id="ee0c3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-107">Entry</span></span> | <span data-ttu-id="ee0c3-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ee0c3-109">CN</span><span class="sxs-lookup"><span data-stu-id="ee0c3-109">CN</span></span>                | <span data-ttu-id="ee0c3-110">Subclasse de</span><span class="sxs-lookup"><span data-stu-id="ee0c3-110">Sub-Class-Of</span></span>                                                    |
| <span data-ttu-id="ee0c3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ee0c3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ee0c3-112">subClassOf</span><span class="sxs-lookup"><span data-stu-id="ee0c3-112">subClassOf</span></span>                                                      |
| <span data-ttu-id="ee0c3-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ee0c3-113">Size</span></span>              | \-                                                              |
| <span data-ttu-id="ee0c3-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ee0c3-114">Update Privilege</span></span>  | <span data-ttu-id="ee0c3-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="ee0c3-115">Schema administrator</span></span>                                            |
| <span data-ttu-id="ee0c3-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ee0c3-116">Update Frequency</span></span>  | \-                                                              |
| <span data-ttu-id="ee0c3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-117">Attribute-Id</span></span>      | <span data-ttu-id="ee0c3-118">1.2.840.113556.1.2.21</span><span class="sxs-lookup"><span data-stu-id="ee0c3-118">1.2.840.113556.1.2.21</span></span>                                           |
| <span data-ttu-id="ee0c3-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ee0c3-119">System-Id-Guid</span></span>    | <span data-ttu-id="ee0c3-120">bf967a3b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ee0c3-120">bf967a3b-0de6-11d0-a285-00aa003049e2</span></span>                            |
| <span data-ttu-id="ee0c3-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee0c3-121">Syntax</span></span>            | [<span data-ttu-id="ee0c3-122">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-122">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="ee0c3-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="ee0c3-123">Implementations</span></span>

-   [<span data-ttu-id="ee0c3-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ee0c3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee0c3-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ee0c3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee0c3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee0c3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee0c3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ee0c3-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee0c3-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ee0c3-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-132">Entry</span></span> | <span data-ttu-id="ee0c3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-136">System-Only</span></span>            | <span data-ttu-id="ee0c3-137">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-137">True</span></span>                                             |
| <span data-ttu-id="ee0c3-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-139">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-139">True</span></span>                                             |
| <span data-ttu-id="ee0c3-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-140">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-141">False</span></span>                                            |
| <span data-ttu-id="ee0c3-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-142">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-143">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-143">False</span></span>                                            |
| <span data-ttu-id="ee0c3-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-148">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-149">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-150">System-Flags</span></span>           | <span data-ttu-id="ee0c3-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-151">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-152">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-153">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-153">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ee0c3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee0c3-154">Windows Server 2003</span></span>



| <span data-ttu-id="ee0c3-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-155">Entry</span></span> | <span data-ttu-id="ee0c3-156">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-159">System-Only</span></span>            | <span data-ttu-id="ee0c3-160">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-160">True</span></span>                                             |
| <span data-ttu-id="ee0c3-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-162">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-162">True</span></span>                                             |
| <span data-ttu-id="ee0c3-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-163">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-164">False</span></span>                                            |
| <span data-ttu-id="ee0c3-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-165">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-166">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-166">False</span></span>                                            |
| <span data-ttu-id="ee0c3-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-171">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-172">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-173">System-Flags</span></span>           | <span data-ttu-id="ee0c3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-174">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-175">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-176">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-176">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ee0c3-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="ee0c3-177">ADAM</span></span>



| <span data-ttu-id="ee0c3-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-178">Entry</span></span> | <span data-ttu-id="ee0c3-179">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-182">System-Only</span></span>            | <span data-ttu-id="ee0c3-183">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-183">True</span></span>                                             |
| <span data-ttu-id="ee0c3-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-185">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-185">True</span></span>                                             |
| <span data-ttu-id="ee0c3-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-186">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-187">False</span></span>                                            |
| <span data-ttu-id="ee0c3-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-188">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-189">False</span></span>                                            |
| <span data-ttu-id="ee0c3-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-194">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-195">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-196">System-Flags</span></span>           | <span data-ttu-id="ee0c3-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-197">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-198">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-199">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-199">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee0c3-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee0c3-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee0c3-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-201">Entry</span></span> | <span data-ttu-id="ee0c3-202">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-205">System-Only</span></span>            | <span data-ttu-id="ee0c3-206">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-206">True</span></span>                                             |
| <span data-ttu-id="ee0c3-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-208">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-208">True</span></span>                                             |
| <span data-ttu-id="ee0c3-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-209">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-210">False</span></span>                                            |
| <span data-ttu-id="ee0c3-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-211">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-212">False</span></span>                                            |
| <span data-ttu-id="ee0c3-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-217">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-218">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-219">System-Flags</span></span>           | <span data-ttu-id="ee0c3-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-220">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-221">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-222">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-222">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee0c3-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-223">Windows Server 2008</span></span>



| <span data-ttu-id="ee0c3-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-224">Entry</span></span> | <span data-ttu-id="ee0c3-225">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-228">System-Only</span></span>            | <span data-ttu-id="ee0c3-229">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-229">True</span></span>                                             |
| <span data-ttu-id="ee0c3-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-231">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-231">True</span></span>                                             |
| <span data-ttu-id="ee0c3-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-232">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-233">False</span></span>                                            |
| <span data-ttu-id="ee0c3-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-234">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-235">False</span></span>                                            |
| <span data-ttu-id="ee0c3-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-240">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-241">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-242">System-Flags</span></span>           | <span data-ttu-id="ee0c3-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-243">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-244">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-245">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-245">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee0c3-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee0c3-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee0c3-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-247">Entry</span></span> | <span data-ttu-id="ee0c3-248">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-251">System-Only</span></span>            | <span data-ttu-id="ee0c3-252">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-252">True</span></span>                                             |
| <span data-ttu-id="ee0c3-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-254">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-254">True</span></span>                                             |
| <span data-ttu-id="ee0c3-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-255">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-256">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-256">False</span></span>                                            |
| <span data-ttu-id="ee0c3-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-257">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-258">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-258">False</span></span>                                            |
| <span data-ttu-id="ee0c3-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-263">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-264">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-265">System-Flags</span></span>           | <span data-ttu-id="ee0c3-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-266">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-267">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-268">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-268">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee0c3-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee0c3-269">Windows Server 2012</span></span>



| <span data-ttu-id="ee0c3-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee0c3-270">Entry</span></span> | <span data-ttu-id="ee0c3-271">Valor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ee0c3-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee0c3-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee0c3-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ee0c3-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee0c3-274">System-Only</span></span>            | <span data-ttu-id="ee0c3-275">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-275">True</span></span>                                             |
| <span data-ttu-id="ee0c3-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee0c3-276">Is-Single-Valued</span></span>       | <span data-ttu-id="ee0c3-277">True</span><span class="sxs-lookup"><span data-stu-id="ee0c3-277">True</span></span>                                             |
| <span data-ttu-id="ee0c3-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee0c3-278">Is Indexed</span></span>             | <span data-ttu-id="ee0c3-279">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-279">False</span></span>                                            |
| <span data-ttu-id="ee0c3-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee0c3-280">In Global Catalog</span></span>      | <span data-ttu-id="ee0c3-281">Falso</span><span class="sxs-lookup"><span data-stu-id="ee0c3-281">False</span></span>                                            |
| <span data-ttu-id="ee0c3-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee0c3-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee0c3-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee0c3-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ee0c3-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee0c3-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee0c3-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ee0c3-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-286">Search-Flags</span></span>           | <span data-ttu-id="ee0c3-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ee0c3-287">0x00000008</span></span>                                       |
| <span data-ttu-id="ee0c3-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee0c3-288">System-Flags</span></span>           | <span data-ttu-id="ee0c3-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee0c3-289">0x00000010</span></span>                                       |
| <span data-ttu-id="ee0c3-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee0c3-290">Classes used in</span></span>        | [<span data-ttu-id="ee0c3-291">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="ee0c3-291">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





