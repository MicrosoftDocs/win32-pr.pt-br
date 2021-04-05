---
title: Atributo FSMO-role-Owner
description: Operação de Single-Master flexível o nome distinto do controlador de domínio em que o esquema pode ser modificado.
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- FSMO-role-Owner atributo AD Schema
- Esquema de AD do atributo fSMORoleOwner
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825250"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="9a637-105">Atributo FSMO-role-Owner</span><span class="sxs-lookup"><span data-stu-id="9a637-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="9a637-106">Operação de Single-Master flexível: o nome distinto do DC em que o esquema pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="9a637-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="9a637-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-107">Entry</span></span> | <span data-ttu-id="9a637-108">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9a637-109">CN</span><span class="sxs-lookup"><span data-stu-id="9a637-109">CN</span></span>                | <span data-ttu-id="9a637-110">FSMO-função-proprietário</span><span class="sxs-lookup"><span data-stu-id="9a637-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="9a637-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a637-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9a637-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="9a637-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="9a637-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9a637-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="9a637-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9a637-114">Update Privilege</span></span>  | <span data-ttu-id="9a637-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="9a637-115">Schema administrator</span></span>                    |
| <span data-ttu-id="9a637-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9a637-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="9a637-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-117">Attribute-Id</span></span>      | <span data-ttu-id="9a637-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="9a637-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="9a637-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a637-119">System-Id-Guid</span></span>    | <span data-ttu-id="9a637-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9a637-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="9a637-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a637-121">Syntax</span></span>            | [<span data-ttu-id="9a637-122">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9a637-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9a637-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="9a637-123">Implementations</span></span>

-   [<span data-ttu-id="9a637-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9a637-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9a637-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a637-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a637-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9a637-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9a637-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a637-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a637-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a637-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a637-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a637-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a637-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a637-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9a637-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a637-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9a637-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-132">Entry</span></span> | <span data-ttu-id="9a637-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-136">System-Only</span></span>            | <span data-ttu-id="9a637-137">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-137">False</span></span>                           |
| <span data-ttu-id="9a637-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-139">True</span><span class="sxs-lookup"><span data-stu-id="9a637-139">True</span></span>                            |
| <span data-ttu-id="9a637-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-140">Is Indexed</span></span>             | <span data-ttu-id="9a637-141">True</span><span class="sxs-lookup"><span data-stu-id="9a637-141">True</span></span>                            |
| <span data-ttu-id="9a637-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-142">In Global Catalog</span></span>      | <span data-ttu-id="9a637-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-143">False</span></span>                           |
| <span data-ttu-id="9a637-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-148">Search-Flags</span></span>           | <span data-ttu-id="9a637-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-149">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-150">System-Flags</span></span>           | <span data-ttu-id="9a637-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-151">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-152">Classes used in</span></span>        | [<span data-ttu-id="9a637-153">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9a637-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a637-154">Windows Server 2003</span></span>



| <span data-ttu-id="9a637-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-155">Entry</span></span> | <span data-ttu-id="9a637-156">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-159">System-Only</span></span>            | <span data-ttu-id="9a637-160">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-160">False</span></span>                           |
| <span data-ttu-id="9a637-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-162">True</span><span class="sxs-lookup"><span data-stu-id="9a637-162">True</span></span>                            |
| <span data-ttu-id="9a637-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-163">Is Indexed</span></span>             | <span data-ttu-id="9a637-164">True</span><span class="sxs-lookup"><span data-stu-id="9a637-164">True</span></span>                            |
| <span data-ttu-id="9a637-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-165">In Global Catalog</span></span>      | <span data-ttu-id="9a637-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-166">False</span></span>                           |
| <span data-ttu-id="9a637-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-171">Search-Flags</span></span>           | <span data-ttu-id="9a637-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-172">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-173">System-Flags</span></span>           | <span data-ttu-id="9a637-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-174">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-175">Classes used in</span></span>        | [<span data-ttu-id="9a637-176">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9a637-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="9a637-177">ADAM</span></span>



| <span data-ttu-id="9a637-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-178">Entry</span></span> | <span data-ttu-id="9a637-179">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-182">System-Only</span></span>            | <span data-ttu-id="9a637-183">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-183">False</span></span>                           |
| <span data-ttu-id="9a637-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-185">True</span><span class="sxs-lookup"><span data-stu-id="9a637-185">True</span></span>                            |
| <span data-ttu-id="9a637-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-186">Is Indexed</span></span>             | <span data-ttu-id="9a637-187">True</span><span class="sxs-lookup"><span data-stu-id="9a637-187">True</span></span>                            |
| <span data-ttu-id="9a637-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-188">In Global Catalog</span></span>      | <span data-ttu-id="9a637-189">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-189">False</span></span>                           |
| <span data-ttu-id="9a637-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-194">Search-Flags</span></span>           | <span data-ttu-id="9a637-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-195">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-196">System-Flags</span></span>           | <span data-ttu-id="9a637-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-197">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-198">Classes used in</span></span>        | [<span data-ttu-id="9a637-199">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a637-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a637-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a637-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-201">Entry</span></span> | <span data-ttu-id="9a637-202">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-205">System-Only</span></span>            | <span data-ttu-id="9a637-206">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-206">False</span></span>                           |
| <span data-ttu-id="9a637-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-208">True</span><span class="sxs-lookup"><span data-stu-id="9a637-208">True</span></span>                            |
| <span data-ttu-id="9a637-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-209">Is Indexed</span></span>             | <span data-ttu-id="9a637-210">True</span><span class="sxs-lookup"><span data-stu-id="9a637-210">True</span></span>                            |
| <span data-ttu-id="9a637-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-211">In Global Catalog</span></span>      | <span data-ttu-id="9a637-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-212">False</span></span>                           |
| <span data-ttu-id="9a637-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-217">Search-Flags</span></span>           | <span data-ttu-id="9a637-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-218">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-219">System-Flags</span></span>           | <span data-ttu-id="9a637-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-220">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-221">Classes used in</span></span>        | [<span data-ttu-id="9a637-222">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a637-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a637-223">Windows Server 2008</span></span>



| <span data-ttu-id="9a637-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-224">Entry</span></span> | <span data-ttu-id="9a637-225">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-228">System-Only</span></span>            | <span data-ttu-id="9a637-229">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-229">False</span></span>                           |
| <span data-ttu-id="9a637-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-231">True</span><span class="sxs-lookup"><span data-stu-id="9a637-231">True</span></span>                            |
| <span data-ttu-id="9a637-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-232">Is Indexed</span></span>             | <span data-ttu-id="9a637-233">True</span><span class="sxs-lookup"><span data-stu-id="9a637-233">True</span></span>                            |
| <span data-ttu-id="9a637-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-234">In Global Catalog</span></span>      | <span data-ttu-id="9a637-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-235">False</span></span>                           |
| <span data-ttu-id="9a637-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-240">Search-Flags</span></span>           | <span data-ttu-id="9a637-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-241">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-242">System-Flags</span></span>           | <span data-ttu-id="9a637-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-243">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-244">Classes used in</span></span>        | [<span data-ttu-id="9a637-245">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a637-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a637-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a637-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-247">Entry</span></span> | <span data-ttu-id="9a637-248">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-251">System-Only</span></span>            | <span data-ttu-id="9a637-252">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-252">False</span></span>                           |
| <span data-ttu-id="9a637-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-254">True</span><span class="sxs-lookup"><span data-stu-id="9a637-254">True</span></span>                            |
| <span data-ttu-id="9a637-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-255">Is Indexed</span></span>             | <span data-ttu-id="9a637-256">True</span><span class="sxs-lookup"><span data-stu-id="9a637-256">True</span></span>                            |
| <span data-ttu-id="9a637-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-257">In Global Catalog</span></span>      | <span data-ttu-id="9a637-258">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-258">False</span></span>                           |
| <span data-ttu-id="9a637-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-263">Search-Flags</span></span>           | <span data-ttu-id="9a637-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-264">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-265">System-Flags</span></span>           | <span data-ttu-id="9a637-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-266">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-267">Classes used in</span></span>        | [<span data-ttu-id="9a637-268">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a637-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a637-269">Windows Server 2012</span></span>



| <span data-ttu-id="9a637-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="9a637-270">Entry</span></span> | <span data-ttu-id="9a637-271">Valor</span><span class="sxs-lookup"><span data-stu-id="9a637-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9a637-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="9a637-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a637-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="9a637-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a637-274">System-Only</span></span>            | <span data-ttu-id="9a637-275">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-275">False</span></span>                           |
| <span data-ttu-id="9a637-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9a637-276">Is-Single-Valued</span></span>       | <span data-ttu-id="9a637-277">True</span><span class="sxs-lookup"><span data-stu-id="9a637-277">True</span></span>                            |
| <span data-ttu-id="9a637-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="9a637-278">Is Indexed</span></span>             | <span data-ttu-id="9a637-279">True</span><span class="sxs-lookup"><span data-stu-id="9a637-279">True</span></span>                            |
| <span data-ttu-id="9a637-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9a637-280">In Global Catalog</span></span>      | <span data-ttu-id="9a637-281">Falso</span><span class="sxs-lookup"><span data-stu-id="9a637-281">False</span></span>                           |
| <span data-ttu-id="9a637-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a637-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a637-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9a637-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9a637-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a637-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9a637-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a637-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9a637-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-286">Search-Flags</span></span>           | <span data-ttu-id="9a637-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a637-287">0x00000001</span></span>                      |
| <span data-ttu-id="9a637-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a637-288">System-Flags</span></span>           | <span data-ttu-id="9a637-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a637-289">0x00000010</span></span>                      |
| <span data-ttu-id="9a637-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9a637-290">Classes used in</span></span>        | [<span data-ttu-id="9a637-291">**Início**</span><span class="sxs-lookup"><span data-stu-id="9a637-291">**Top**</span></span>](c-top.md)<br/> |



 

 





