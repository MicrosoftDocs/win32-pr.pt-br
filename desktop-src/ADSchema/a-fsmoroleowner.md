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
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="bef62-105">Atributo FSMO-role-Owner</span><span class="sxs-lookup"><span data-stu-id="bef62-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="bef62-106">Operação de Single-Master flexível: o nome distinto do DC em que o esquema pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="bef62-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="bef62-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-107">Entry</span></span> | <span data-ttu-id="bef62-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="bef62-109">CN</span><span class="sxs-lookup"><span data-stu-id="bef62-109">CN</span></span>                | <span data-ttu-id="bef62-110">FSMO-função-proprietário</span><span class="sxs-lookup"><span data-stu-id="bef62-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="bef62-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bef62-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bef62-112">fSMORoleOwner</span><span class="sxs-lookup"><span data-stu-id="bef62-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="bef62-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bef62-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="bef62-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bef62-114">Update Privilege</span></span>  | <span data-ttu-id="bef62-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="bef62-115">Schema administrator</span></span>                    |
| <span data-ttu-id="bef62-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bef62-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="bef62-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-117">Attribute-Id</span></span>      | <span data-ttu-id="bef62-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="bef62-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="bef62-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bef62-119">System-Id-Guid</span></span>    | <span data-ttu-id="bef62-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bef62-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="bef62-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="bef62-121">Syntax</span></span>            | [<span data-ttu-id="bef62-122">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="bef62-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="bef62-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="bef62-123">Implementations</span></span>

-   [<span data-ttu-id="bef62-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bef62-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bef62-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bef62-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bef62-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bef62-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bef62-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bef62-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bef62-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bef62-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bef62-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bef62-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bef62-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bef62-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bef62-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bef62-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bef62-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-132">Entry</span></span> | <span data-ttu-id="bef62-133">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-136">System-Only</span></span>            | <span data-ttu-id="bef62-137">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-137">False</span></span>                           |
| <span data-ttu-id="bef62-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-139">True</span><span class="sxs-lookup"><span data-stu-id="bef62-139">True</span></span>                            |
| <span data-ttu-id="bef62-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-140">Is Indexed</span></span>             | <span data-ttu-id="bef62-141">True</span><span class="sxs-lookup"><span data-stu-id="bef62-141">True</span></span>                            |
| <span data-ttu-id="bef62-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-142">In Global Catalog</span></span>      | <span data-ttu-id="bef62-143">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-143">False</span></span>                           |
| <span data-ttu-id="bef62-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-148">Search-Flags</span></span>           | <span data-ttu-id="bef62-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-149">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-150">System-Flags</span></span>           | <span data-ttu-id="bef62-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-151">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-152">Classes used in</span></span>        | [<span data-ttu-id="bef62-153">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bef62-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bef62-154">Windows Server 2003</span></span>



| <span data-ttu-id="bef62-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-155">Entry</span></span> | <span data-ttu-id="bef62-156">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-159">System-Only</span></span>            | <span data-ttu-id="bef62-160">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-160">False</span></span>                           |
| <span data-ttu-id="bef62-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-161">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-162">True</span><span class="sxs-lookup"><span data-stu-id="bef62-162">True</span></span>                            |
| <span data-ttu-id="bef62-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-163">Is Indexed</span></span>             | <span data-ttu-id="bef62-164">True</span><span class="sxs-lookup"><span data-stu-id="bef62-164">True</span></span>                            |
| <span data-ttu-id="bef62-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-165">In Global Catalog</span></span>      | <span data-ttu-id="bef62-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-166">False</span></span>                           |
| <span data-ttu-id="bef62-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-171">Search-Flags</span></span>           | <span data-ttu-id="bef62-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-172">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-173">System-Flags</span></span>           | <span data-ttu-id="bef62-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-174">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-175">Classes used in</span></span>        | [<span data-ttu-id="bef62-176">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bef62-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="bef62-177">ADAM</span></span>



| <span data-ttu-id="bef62-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-178">Entry</span></span> | <span data-ttu-id="bef62-179">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-182">System-Only</span></span>            | <span data-ttu-id="bef62-183">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-183">False</span></span>                           |
| <span data-ttu-id="bef62-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-184">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-185">True</span><span class="sxs-lookup"><span data-stu-id="bef62-185">True</span></span>                            |
| <span data-ttu-id="bef62-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-186">Is Indexed</span></span>             | <span data-ttu-id="bef62-187">True</span><span class="sxs-lookup"><span data-stu-id="bef62-187">True</span></span>                            |
| <span data-ttu-id="bef62-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-188">In Global Catalog</span></span>      | <span data-ttu-id="bef62-189">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-189">False</span></span>                           |
| <span data-ttu-id="bef62-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-194">Search-Flags</span></span>           | <span data-ttu-id="bef62-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-195">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-196">System-Flags</span></span>           | <span data-ttu-id="bef62-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-197">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-198">Classes used in</span></span>        | [<span data-ttu-id="bef62-199">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bef62-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bef62-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bef62-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-201">Entry</span></span> | <span data-ttu-id="bef62-202">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-205">System-Only</span></span>            | <span data-ttu-id="bef62-206">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-206">False</span></span>                           |
| <span data-ttu-id="bef62-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-207">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-208">True</span><span class="sxs-lookup"><span data-stu-id="bef62-208">True</span></span>                            |
| <span data-ttu-id="bef62-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-209">Is Indexed</span></span>             | <span data-ttu-id="bef62-210">True</span><span class="sxs-lookup"><span data-stu-id="bef62-210">True</span></span>                            |
| <span data-ttu-id="bef62-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-211">In Global Catalog</span></span>      | <span data-ttu-id="bef62-212">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-212">False</span></span>                           |
| <span data-ttu-id="bef62-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-217">Search-Flags</span></span>           | <span data-ttu-id="bef62-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-218">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-219">System-Flags</span></span>           | <span data-ttu-id="bef62-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-220">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-221">Classes used in</span></span>        | [<span data-ttu-id="bef62-222">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bef62-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bef62-223">Windows Server 2008</span></span>



| <span data-ttu-id="bef62-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-224">Entry</span></span> | <span data-ttu-id="bef62-225">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-228">System-Only</span></span>            | <span data-ttu-id="bef62-229">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-229">False</span></span>                           |
| <span data-ttu-id="bef62-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-230">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-231">True</span><span class="sxs-lookup"><span data-stu-id="bef62-231">True</span></span>                            |
| <span data-ttu-id="bef62-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-232">Is Indexed</span></span>             | <span data-ttu-id="bef62-233">True</span><span class="sxs-lookup"><span data-stu-id="bef62-233">True</span></span>                            |
| <span data-ttu-id="bef62-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-234">In Global Catalog</span></span>      | <span data-ttu-id="bef62-235">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-235">False</span></span>                           |
| <span data-ttu-id="bef62-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-240">Search-Flags</span></span>           | <span data-ttu-id="bef62-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-241">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-242">System-Flags</span></span>           | <span data-ttu-id="bef62-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-243">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-244">Classes used in</span></span>        | [<span data-ttu-id="bef62-245">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bef62-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bef62-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bef62-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-247">Entry</span></span> | <span data-ttu-id="bef62-248">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-251">System-Only</span></span>            | <span data-ttu-id="bef62-252">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-252">False</span></span>                           |
| <span data-ttu-id="bef62-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-253">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-254">True</span><span class="sxs-lookup"><span data-stu-id="bef62-254">True</span></span>                            |
| <span data-ttu-id="bef62-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-255">Is Indexed</span></span>             | <span data-ttu-id="bef62-256">True</span><span class="sxs-lookup"><span data-stu-id="bef62-256">True</span></span>                            |
| <span data-ttu-id="bef62-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-257">In Global Catalog</span></span>      | <span data-ttu-id="bef62-258">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-258">False</span></span>                           |
| <span data-ttu-id="bef62-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-263">Search-Flags</span></span>           | <span data-ttu-id="bef62-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-264">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-265">System-Flags</span></span>           | <span data-ttu-id="bef62-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-266">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-267">Classes used in</span></span>        | [<span data-ttu-id="bef62-268">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bef62-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bef62-269">Windows Server 2012</span></span>



| <span data-ttu-id="bef62-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="bef62-270">Entry</span></span> | <span data-ttu-id="bef62-271">Valor</span><span class="sxs-lookup"><span data-stu-id="bef62-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bef62-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="bef62-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bef62-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bef62-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="bef62-274">System-Only</span></span>            | <span data-ttu-id="bef62-275">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-275">False</span></span>                           |
| <span data-ttu-id="bef62-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bef62-276">Is-Single-Valued</span></span>       | <span data-ttu-id="bef62-277">True</span><span class="sxs-lookup"><span data-stu-id="bef62-277">True</span></span>                            |
| <span data-ttu-id="bef62-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="bef62-278">Is Indexed</span></span>             | <span data-ttu-id="bef62-279">True</span><span class="sxs-lookup"><span data-stu-id="bef62-279">True</span></span>                            |
| <span data-ttu-id="bef62-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bef62-280">In Global Catalog</span></span>      | <span data-ttu-id="bef62-281">Falso</span><span class="sxs-lookup"><span data-stu-id="bef62-281">False</span></span>                           |
| <span data-ttu-id="bef62-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bef62-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="bef62-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bef62-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bef62-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bef62-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bef62-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bef62-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bef62-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-286">Search-Flags</span></span>           | <span data-ttu-id="bef62-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bef62-287">0x00000001</span></span>                      |
| <span data-ttu-id="bef62-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bef62-288">System-Flags</span></span>           | <span data-ttu-id="bef62-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bef62-289">0x00000010</span></span>                      |
| <span data-ttu-id="bef62-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bef62-290">Classes used in</span></span>        | [<span data-ttu-id="bef62-291">**Início**</span><span class="sxs-lookup"><span data-stu-id="bef62-291">**Top**</span></span>](c-top.md)<br/> |



 

 





