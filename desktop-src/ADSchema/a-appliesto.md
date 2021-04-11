---
title: Applies-To atributo
description: Contém a lista de classes de objeto às quais o direito estendido se aplica. Na lista, uma classe de objeto é representada pela propriedade schemaIDGUID para seu objeto schemaClass.
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- Esquema de Applies-To do atributo AD
- atributo de AD de atributos AppliesTo
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087165"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="9b805-106">Applies-To atributo</span><span class="sxs-lookup"><span data-stu-id="9b805-106">Applies-To attribute</span></span>

<span data-ttu-id="9b805-107">Contém a lista de classes de objeto às quais o direito estendido se aplica.</span><span class="sxs-lookup"><span data-stu-id="9b805-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="9b805-108">Na lista, uma classe de objeto é representada pela propriedade schemaIDGUID para seu objeto schemaClass.</span><span class="sxs-lookup"><span data-stu-id="9b805-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="9b805-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-109">Entry</span></span> | <span data-ttu-id="9b805-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9b805-111">CN</span><span class="sxs-lookup"><span data-stu-id="9b805-111">CN</span></span>                | <span data-ttu-id="9b805-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="9b805-112">Applies-To</span></span>                                  |
| <span data-ttu-id="9b805-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9b805-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9b805-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="9b805-114">appliesTo</span></span>                                   |
| <span data-ttu-id="9b805-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9b805-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9b805-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9b805-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9b805-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9b805-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9b805-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-118">Attribute-Id</span></span>      | <span data-ttu-id="9b805-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="9b805-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="9b805-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9b805-120">System-Id-Guid</span></span>    | <span data-ttu-id="9b805-121">8297931d-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9b805-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="9b805-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b805-122">Syntax</span></span>            | [<span data-ttu-id="9b805-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9b805-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9b805-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="9b805-124">Implementations</span></span>

-   [<span data-ttu-id="9b805-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9b805-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9b805-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b805-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b805-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9b805-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9b805-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b805-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b805-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b805-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b805-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b805-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b805-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b805-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9b805-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b805-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9b805-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-133">Entry</span></span> | <span data-ttu-id="9b805-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-137">System-Only</span></span>            | <span data-ttu-id="9b805-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-138">False</span></span>                                                           |
| <span data-ttu-id="9b805-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-140">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-140">False</span></span>                                                           |
| <span data-ttu-id="9b805-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-141">Is Indexed</span></span>             | <span data-ttu-id="9b805-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-142">False</span></span>                                                           |
| <span data-ttu-id="9b805-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-143">In Global Catalog</span></span>      | <span data-ttu-id="9b805-144">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-144">False</span></span>                                                           |
| <span data-ttu-id="9b805-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-147">Range-Lower</span></span>            | <span data-ttu-id="9b805-148">36</span><span class="sxs-lookup"><span data-stu-id="9b805-148">36</span></span>                                                              |
| <span data-ttu-id="9b805-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-149">Range-Upper</span></span>            | <span data-ttu-id="9b805-150">36</span><span class="sxs-lookup"><span data-stu-id="9b805-150">36</span></span>                                                              |
| <span data-ttu-id="9b805-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-151">Search-Flags</span></span>           | <span data-ttu-id="9b805-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-153">System-Flags</span></span>           | <span data-ttu-id="9b805-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-155">Classes used in</span></span>        | [<span data-ttu-id="9b805-156">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9b805-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b805-157">Windows Server 2003</span></span>



| <span data-ttu-id="9b805-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-158">Entry</span></span> | <span data-ttu-id="9b805-159">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-162">System-Only</span></span>            | <span data-ttu-id="9b805-163">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-163">False</span></span>                                                           |
| <span data-ttu-id="9b805-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-165">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-165">False</span></span>                                                           |
| <span data-ttu-id="9b805-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-166">Is Indexed</span></span>             | <span data-ttu-id="9b805-167">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-167">False</span></span>                                                           |
| <span data-ttu-id="9b805-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-168">In Global Catalog</span></span>      | <span data-ttu-id="9b805-169">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-169">False</span></span>                                                           |
| <span data-ttu-id="9b805-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-172">Range-Lower</span></span>            | <span data-ttu-id="9b805-173">36</span><span class="sxs-lookup"><span data-stu-id="9b805-173">36</span></span>                                                              |
| <span data-ttu-id="9b805-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-174">Range-Upper</span></span>            | <span data-ttu-id="9b805-175">36</span><span class="sxs-lookup"><span data-stu-id="9b805-175">36</span></span>                                                              |
| <span data-ttu-id="9b805-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-176">Search-Flags</span></span>           | <span data-ttu-id="9b805-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-178">System-Flags</span></span>           | <span data-ttu-id="9b805-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-180">Classes used in</span></span>        | [<span data-ttu-id="9b805-181">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9b805-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="9b805-182">ADAM</span></span>



| <span data-ttu-id="9b805-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-183">Entry</span></span> | <span data-ttu-id="9b805-184">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-187">System-Only</span></span>            | <span data-ttu-id="9b805-188">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-188">False</span></span>                                                           |
| <span data-ttu-id="9b805-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-190">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-190">False</span></span>                                                           |
| <span data-ttu-id="9b805-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-191">Is Indexed</span></span>             | <span data-ttu-id="9b805-192">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-192">False</span></span>                                                           |
| <span data-ttu-id="9b805-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-193">In Global Catalog</span></span>      | <span data-ttu-id="9b805-194">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-194">False</span></span>                                                           |
| <span data-ttu-id="9b805-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-197">Range-Lower</span></span>            | <span data-ttu-id="9b805-198">36</span><span class="sxs-lookup"><span data-stu-id="9b805-198">36</span></span>                                                              |
| <span data-ttu-id="9b805-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-199">Range-Upper</span></span>            | <span data-ttu-id="9b805-200">36</span><span class="sxs-lookup"><span data-stu-id="9b805-200">36</span></span>                                                              |
| <span data-ttu-id="9b805-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-201">Search-Flags</span></span>           | <span data-ttu-id="9b805-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-203">System-Flags</span></span>           | <span data-ttu-id="9b805-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-205">Classes used in</span></span>        | [<span data-ttu-id="9b805-206">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b805-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b805-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b805-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-208">Entry</span></span> | <span data-ttu-id="9b805-209">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-212">System-Only</span></span>            | <span data-ttu-id="9b805-213">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-213">False</span></span>                                                           |
| <span data-ttu-id="9b805-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-215">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-215">False</span></span>                                                           |
| <span data-ttu-id="9b805-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-216">Is Indexed</span></span>             | <span data-ttu-id="9b805-217">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-217">False</span></span>                                                           |
| <span data-ttu-id="9b805-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-218">In Global Catalog</span></span>      | <span data-ttu-id="9b805-219">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-219">False</span></span>                                                           |
| <span data-ttu-id="9b805-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-222">Range-Lower</span></span>            | <span data-ttu-id="9b805-223">36</span><span class="sxs-lookup"><span data-stu-id="9b805-223">36</span></span>                                                              |
| <span data-ttu-id="9b805-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-224">Range-Upper</span></span>            | <span data-ttu-id="9b805-225">36</span><span class="sxs-lookup"><span data-stu-id="9b805-225">36</span></span>                                                              |
| <span data-ttu-id="9b805-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-226">Search-Flags</span></span>           | <span data-ttu-id="9b805-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-228">System-Flags</span></span>           | <span data-ttu-id="9b805-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-230">Classes used in</span></span>        | [<span data-ttu-id="9b805-231">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b805-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b805-232">Windows Server 2008</span></span>



| <span data-ttu-id="9b805-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-233">Entry</span></span> | <span data-ttu-id="9b805-234">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-237">System-Only</span></span>            | <span data-ttu-id="9b805-238">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-238">False</span></span>                                                           |
| <span data-ttu-id="9b805-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-239">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-240">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-240">False</span></span>                                                           |
| <span data-ttu-id="9b805-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-241">Is Indexed</span></span>             | <span data-ttu-id="9b805-242">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-242">False</span></span>                                                           |
| <span data-ttu-id="9b805-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-243">In Global Catalog</span></span>      | <span data-ttu-id="9b805-244">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-244">False</span></span>                                                           |
| <span data-ttu-id="9b805-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-247">Range-Lower</span></span>            | <span data-ttu-id="9b805-248">36</span><span class="sxs-lookup"><span data-stu-id="9b805-248">36</span></span>                                                              |
| <span data-ttu-id="9b805-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-249">Range-Upper</span></span>            | <span data-ttu-id="9b805-250">36</span><span class="sxs-lookup"><span data-stu-id="9b805-250">36</span></span>                                                              |
| <span data-ttu-id="9b805-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-251">Search-Flags</span></span>           | <span data-ttu-id="9b805-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-253">System-Flags</span></span>           | <span data-ttu-id="9b805-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-255">Classes used in</span></span>        | [<span data-ttu-id="9b805-256">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b805-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b805-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b805-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-258">Entry</span></span> | <span data-ttu-id="9b805-259">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-262">System-Only</span></span>            | <span data-ttu-id="9b805-263">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-263">False</span></span>                                                           |
| <span data-ttu-id="9b805-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-264">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-265">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-265">False</span></span>                                                           |
| <span data-ttu-id="9b805-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-266">Is Indexed</span></span>             | <span data-ttu-id="9b805-267">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-267">False</span></span>                                                           |
| <span data-ttu-id="9b805-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-268">In Global Catalog</span></span>      | <span data-ttu-id="9b805-269">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-269">False</span></span>                                                           |
| <span data-ttu-id="9b805-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-272">Range-Lower</span></span>            | <span data-ttu-id="9b805-273">36</span><span class="sxs-lookup"><span data-stu-id="9b805-273">36</span></span>                                                              |
| <span data-ttu-id="9b805-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-274">Range-Upper</span></span>            | <span data-ttu-id="9b805-275">36</span><span class="sxs-lookup"><span data-stu-id="9b805-275">36</span></span>                                                              |
| <span data-ttu-id="9b805-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-276">Search-Flags</span></span>           | <span data-ttu-id="9b805-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-278">System-Flags</span></span>           | <span data-ttu-id="9b805-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-280">Classes used in</span></span>        | [<span data-ttu-id="9b805-281">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b805-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b805-282">Windows Server 2012</span></span>



| <span data-ttu-id="9b805-283">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b805-283">Entry</span></span> | <span data-ttu-id="9b805-284">Valor</span><span class="sxs-lookup"><span data-stu-id="9b805-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9b805-285">ID do link</span><span class="sxs-lookup"><span data-stu-id="9b805-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b805-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9b805-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b805-287">System-Only</span></span>            | <span data-ttu-id="9b805-288">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-288">False</span></span>                                                           |
| <span data-ttu-id="9b805-289">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9b805-289">Is-Single-Valued</span></span>       | <span data-ttu-id="9b805-290">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-290">False</span></span>                                                           |
| <span data-ttu-id="9b805-291">É indexado</span><span class="sxs-lookup"><span data-stu-id="9b805-291">Is Indexed</span></span>             | <span data-ttu-id="9b805-292">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-292">False</span></span>                                                           |
| <span data-ttu-id="9b805-293">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b805-293">In Global Catalog</span></span>      | <span data-ttu-id="9b805-294">Falso</span><span class="sxs-lookup"><span data-stu-id="9b805-294">False</span></span>                                                           |
| <span data-ttu-id="9b805-295">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9b805-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b805-296">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9b805-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9b805-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b805-297">Range-Lower</span></span>            | <span data-ttu-id="9b805-298">36</span><span class="sxs-lookup"><span data-stu-id="9b805-298">36</span></span>                                                              |
| <span data-ttu-id="9b805-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b805-299">Range-Upper</span></span>            | <span data-ttu-id="9b805-300">36</span><span class="sxs-lookup"><span data-stu-id="9b805-300">36</span></span>                                                              |
| <span data-ttu-id="9b805-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-301">Search-Flags</span></span>           | <span data-ttu-id="9b805-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b805-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="9b805-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b805-303">System-Flags</span></span>           | <span data-ttu-id="9b805-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b805-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="9b805-305">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9b805-305">Classes used in</span></span>        | [<span data-ttu-id="9b805-306">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="9b805-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





