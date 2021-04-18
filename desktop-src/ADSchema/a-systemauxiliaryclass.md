---
title: Sistema-atributo de classe auxiliar
description: Uma lista de classes auxiliares que não podem ser modificadas pelo usuário.
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- System-auxiliar-esquema de atributo de classe do AD
- Esquema de AD do atributo systemAuxiliaryClass
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756476"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="78efa-105">Sistema-atributo de classe auxiliar</span><span class="sxs-lookup"><span data-stu-id="78efa-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="78efa-106">Uma lista de classes auxiliares que não podem ser modificadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="78efa-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="78efa-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-107">Entry</span></span> | <span data-ttu-id="78efa-108">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="78efa-109">CN</span><span class="sxs-lookup"><span data-stu-id="78efa-109">CN</span></span>                | <span data-ttu-id="78efa-110">Classe auxiliar do sistema</span><span class="sxs-lookup"><span data-stu-id="78efa-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="78efa-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="78efa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="78efa-112">systemAuxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="78efa-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="78efa-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="78efa-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="78efa-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="78efa-114">Update Privilege</span></span>  | <span data-ttu-id="78efa-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="78efa-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="78efa-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="78efa-116">Update Frequency</span></span>  | <span data-ttu-id="78efa-117">Quando a classe é criada ou uma nova classe auxiliar é adicionada a ela.</span><span class="sxs-lookup"><span data-stu-id="78efa-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="78efa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-118">Attribute-Id</span></span>      | <span data-ttu-id="78efa-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="78efa-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="78efa-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78efa-120">System-Id-Guid</span></span>    | <span data-ttu-id="78efa-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="78efa-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="78efa-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="78efa-122">Syntax</span></span>            | [<span data-ttu-id="78efa-123">**Cadeia de caracteres (identificador de objeto)**</span><span class="sxs-lookup"><span data-stu-id="78efa-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="78efa-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="78efa-124">Implementations</span></span>

-   [<span data-ttu-id="78efa-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78efa-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78efa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78efa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78efa-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="78efa-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="78efa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78efa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78efa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78efa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78efa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78efa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78efa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78efa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78efa-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78efa-132">Windows 2000 Server</span></span>



| <span data-ttu-id="78efa-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-133">Entry</span></span> | <span data-ttu-id="78efa-134">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-137">System-Only</span></span>            | <span data-ttu-id="78efa-138">True</span><span class="sxs-lookup"><span data-stu-id="78efa-138">True</span></span>                                             |
| <span data-ttu-id="78efa-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-139">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-140">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-140">False</span></span>                                            |
| <span data-ttu-id="78efa-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-141">Is Indexed</span></span>             | <span data-ttu-id="78efa-142">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-142">False</span></span>                                            |
| <span data-ttu-id="78efa-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-143">In Global Catalog</span></span>      | <span data-ttu-id="78efa-144">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-144">False</span></span>                                            |
| <span data-ttu-id="78efa-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-149">Search-Flags</span></span>           | <span data-ttu-id="78efa-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-150">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-151">System-Flags</span></span>           | <span data-ttu-id="78efa-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-152">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-153">Classes used in</span></span>        | [<span data-ttu-id="78efa-154">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78efa-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78efa-155">Windows Server 2003</span></span>



| <span data-ttu-id="78efa-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-156">Entry</span></span> | <span data-ttu-id="78efa-157">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-160">System-Only</span></span>            | <span data-ttu-id="78efa-161">True</span><span class="sxs-lookup"><span data-stu-id="78efa-161">True</span></span>                                             |
| <span data-ttu-id="78efa-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-162">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-163">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-163">False</span></span>                                            |
| <span data-ttu-id="78efa-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-164">Is Indexed</span></span>             | <span data-ttu-id="78efa-165">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-165">False</span></span>                                            |
| <span data-ttu-id="78efa-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-166">In Global Catalog</span></span>      | <span data-ttu-id="78efa-167">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-167">False</span></span>                                            |
| <span data-ttu-id="78efa-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-172">Search-Flags</span></span>           | <span data-ttu-id="78efa-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-173">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-174">System-Flags</span></span>           | <span data-ttu-id="78efa-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-175">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-176">Classes used in</span></span>        | [<span data-ttu-id="78efa-177">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="78efa-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="78efa-178">ADAM</span></span>



| <span data-ttu-id="78efa-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-179">Entry</span></span> | <span data-ttu-id="78efa-180">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-183">System-Only</span></span>            | <span data-ttu-id="78efa-184">True</span><span class="sxs-lookup"><span data-stu-id="78efa-184">True</span></span>                                             |
| <span data-ttu-id="78efa-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-185">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-186">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-186">False</span></span>                                            |
| <span data-ttu-id="78efa-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-187">Is Indexed</span></span>             | <span data-ttu-id="78efa-188">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-188">False</span></span>                                            |
| <span data-ttu-id="78efa-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-189">In Global Catalog</span></span>      | <span data-ttu-id="78efa-190">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-190">False</span></span>                                            |
| <span data-ttu-id="78efa-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-195">Search-Flags</span></span>           | <span data-ttu-id="78efa-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-196">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-197">System-Flags</span></span>           | <span data-ttu-id="78efa-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-198">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-199">Classes used in</span></span>        | [<span data-ttu-id="78efa-200">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78efa-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78efa-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78efa-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-202">Entry</span></span> | <span data-ttu-id="78efa-203">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-206">System-Only</span></span>            | <span data-ttu-id="78efa-207">True</span><span class="sxs-lookup"><span data-stu-id="78efa-207">True</span></span>                                             |
| <span data-ttu-id="78efa-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-208">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-209">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-209">False</span></span>                                            |
| <span data-ttu-id="78efa-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-210">Is Indexed</span></span>             | <span data-ttu-id="78efa-211">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-211">False</span></span>                                            |
| <span data-ttu-id="78efa-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-212">In Global Catalog</span></span>      | <span data-ttu-id="78efa-213">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-213">False</span></span>                                            |
| <span data-ttu-id="78efa-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-218">Search-Flags</span></span>           | <span data-ttu-id="78efa-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-219">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-220">System-Flags</span></span>           | <span data-ttu-id="78efa-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-221">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-222">Classes used in</span></span>        | [<span data-ttu-id="78efa-223">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78efa-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78efa-224">Windows Server 2008</span></span>



| <span data-ttu-id="78efa-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-225">Entry</span></span> | <span data-ttu-id="78efa-226">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-229">System-Only</span></span>            | <span data-ttu-id="78efa-230">True</span><span class="sxs-lookup"><span data-stu-id="78efa-230">True</span></span>                                             |
| <span data-ttu-id="78efa-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-231">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-232">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-232">False</span></span>                                            |
| <span data-ttu-id="78efa-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-233">Is Indexed</span></span>             | <span data-ttu-id="78efa-234">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-234">False</span></span>                                            |
| <span data-ttu-id="78efa-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-235">In Global Catalog</span></span>      | <span data-ttu-id="78efa-236">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-236">False</span></span>                                            |
| <span data-ttu-id="78efa-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-241">Search-Flags</span></span>           | <span data-ttu-id="78efa-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-242">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-243">System-Flags</span></span>           | <span data-ttu-id="78efa-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-244">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-245">Classes used in</span></span>        | [<span data-ttu-id="78efa-246">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78efa-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78efa-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78efa-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-248">Entry</span></span> | <span data-ttu-id="78efa-249">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-252">System-Only</span></span>            | <span data-ttu-id="78efa-253">True</span><span class="sxs-lookup"><span data-stu-id="78efa-253">True</span></span>                                             |
| <span data-ttu-id="78efa-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-254">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-255">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-255">False</span></span>                                            |
| <span data-ttu-id="78efa-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-256">Is Indexed</span></span>             | <span data-ttu-id="78efa-257">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-257">False</span></span>                                            |
| <span data-ttu-id="78efa-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-258">In Global Catalog</span></span>      | <span data-ttu-id="78efa-259">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-259">False</span></span>                                            |
| <span data-ttu-id="78efa-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-264">Search-Flags</span></span>           | <span data-ttu-id="78efa-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-265">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-266">System-Flags</span></span>           | <span data-ttu-id="78efa-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-267">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-268">Classes used in</span></span>        | [<span data-ttu-id="78efa-269">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78efa-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78efa-270">Windows Server 2012</span></span>



| <span data-ttu-id="78efa-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="78efa-271">Entry</span></span> | <span data-ttu-id="78efa-272">Valor</span><span class="sxs-lookup"><span data-stu-id="78efa-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="78efa-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="78efa-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78efa-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="78efa-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="78efa-275">System-Only</span></span>            | <span data-ttu-id="78efa-276">True</span><span class="sxs-lookup"><span data-stu-id="78efa-276">True</span></span>                                             |
| <span data-ttu-id="78efa-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78efa-277">Is-Single-Valued</span></span>       | <span data-ttu-id="78efa-278">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-278">False</span></span>                                            |
| <span data-ttu-id="78efa-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="78efa-279">Is Indexed</span></span>             | <span data-ttu-id="78efa-280">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-280">False</span></span>                                            |
| <span data-ttu-id="78efa-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78efa-281">In Global Catalog</span></span>      | <span data-ttu-id="78efa-282">Falso</span><span class="sxs-lookup"><span data-stu-id="78efa-282">False</span></span>                                            |
| <span data-ttu-id="78efa-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78efa-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="78efa-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78efa-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="78efa-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78efa-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="78efa-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78efa-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="78efa-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-287">Search-Flags</span></span>           | <span data-ttu-id="78efa-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78efa-288">0x00000000</span></span>                                       |
| <span data-ttu-id="78efa-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78efa-289">System-Flags</span></span>           | <span data-ttu-id="78efa-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78efa-290">0x00000010</span></span>                                       |
| <span data-ttu-id="78efa-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78efa-291">Classes used in</span></span>        | [<span data-ttu-id="78efa-292">**Esquema de classe**</span><span class="sxs-lookup"><span data-stu-id="78efa-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 





