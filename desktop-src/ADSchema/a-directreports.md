---
title: Atributo de relatórios
description: Contém a lista de usuários que se reportam diretamente ao usuário. Os usuários listados como relatórios são aqueles que têm a propriedade Gerenciador de propriedades definida para esse usuário. Cada item na lista é uma referência vinculada ao objeto que representa o usuário.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de relatórios
- Esquema de AD do atributo directReports
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754444"
---
# <a name="reports-attribute"></a><span data-ttu-id="a4e0e-107">Atributo de relatórios</span><span class="sxs-lookup"><span data-stu-id="a4e0e-107">Reports attribute</span></span>

<span data-ttu-id="a4e0e-108">Contém a lista de usuários que se reportam diretamente ao usuário.</span><span class="sxs-lookup"><span data-stu-id="a4e0e-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="a4e0e-109">Os usuários listados como relatórios são aqueles que têm a propriedade Gerenciador de propriedades definida para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="a4e0e-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="a4e0e-110">Cada item na lista é uma referência vinculada ao objeto que representa o usuário.</span><span class="sxs-lookup"><span data-stu-id="a4e0e-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="a4e0e-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-111">Entry</span></span> | <span data-ttu-id="a4e0e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="a4e0e-113">CN</span><span class="sxs-lookup"><span data-stu-id="a4e0e-113">CN</span></span>                | <span data-ttu-id="a4e0e-114">Relatórios</span><span class="sxs-lookup"><span data-stu-id="a4e0e-114">Reports</span></span>                                         |
| <span data-ttu-id="a4e0e-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a4e0e-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a4e0e-116">directReports</span><span class="sxs-lookup"><span data-stu-id="a4e0e-116">directReports</span></span>                                   |
| <span data-ttu-id="a4e0e-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a4e0e-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="a4e0e-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a4e0e-118">Update Privilege</span></span>  | <span data-ttu-id="a4e0e-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a4e0e-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="a4e0e-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a4e0e-120">Update Frequency</span></span>  | <span data-ttu-id="a4e0e-121">Sempre que os subordinados diretos de um usuário forem alterados.</span><span class="sxs-lookup"><span data-stu-id="a4e0e-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="a4e0e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-122">Attribute-Id</span></span>      | <span data-ttu-id="a4e0e-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="a4e0e-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="a4e0e-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a4e0e-124">System-Id-Guid</span></span>    | <span data-ttu-id="a4e0e-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a4e0e-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="a4e0e-126">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4e0e-126">Syntax</span></span>            | [<span data-ttu-id="a4e0e-127">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="a4e0e-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="a4e0e-128">Implementations</span></span>

-   [<span data-ttu-id="a4e0e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a4e0e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4e0e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4e0e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4e0e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4e0e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a4e0e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4e0e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a4e0e-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-136">Entry</span></span> | <span data-ttu-id="a4e0e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a4e0e-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4e0e-138">Link-Id</span></span>                | <span data-ttu-id="a4e0e-139">43</span><span class="sxs-lookup"><span data-stu-id="a4e0e-139">43</span></span>                              |
| <span data-ttu-id="a4e0e-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-140">MAPI-Id</span></span>                | <span data-ttu-id="a4e0e-141">0x800E</span><span class="sxs-lookup"><span data-stu-id="a4e0e-141">0x800E</span></span>                          |
| <span data-ttu-id="a4e0e-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4e0e-142">System-Only</span></span>            | <span data-ttu-id="a4e0e-143">True</span><span class="sxs-lookup"><span data-stu-id="a4e0e-143">True</span></span>                            |
| <span data-ttu-id="a4e0e-144">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4e0e-144">Is-Single-Valued</span></span>       | <span data-ttu-id="a4e0e-145">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-145">False</span></span>                           |
| <span data-ttu-id="a4e0e-146">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4e0e-146">Is Indexed</span></span>             | <span data-ttu-id="a4e0e-147">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-147">False</span></span>                           |
| <span data-ttu-id="a4e0e-148">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4e0e-148">In Global Catalog</span></span>      | <span data-ttu-id="a4e0e-149">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-149">False</span></span>                           |
| <span data-ttu-id="a4e0e-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4e0e-151">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4e0e-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a4e0e-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4e0e-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4e0e-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-154">Search-Flags</span></span>           | <span data-ttu-id="a4e0e-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4e0e-155">0x00000000</span></span>                      |
| <span data-ttu-id="a4e0e-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-156">System-Flags</span></span>           | <span data-ttu-id="a4e0e-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4e0e-157">0x00000010</span></span>                      |
| <span data-ttu-id="a4e0e-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4e0e-158">Classes used in</span></span>        | [<span data-ttu-id="a4e0e-159">**Início**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a4e0e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4e0e-160">Windows Server 2003</span></span>



| <span data-ttu-id="a4e0e-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-161">Entry</span></span> | <span data-ttu-id="a4e0e-162">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a4e0e-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4e0e-163">Link-Id</span></span>                | <span data-ttu-id="a4e0e-164">43</span><span class="sxs-lookup"><span data-stu-id="a4e0e-164">43</span></span>                              |
| <span data-ttu-id="a4e0e-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-165">MAPI-Id</span></span>                | <span data-ttu-id="a4e0e-166">0x800E</span><span class="sxs-lookup"><span data-stu-id="a4e0e-166">0x800E</span></span>                          |
| <span data-ttu-id="a4e0e-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4e0e-167">System-Only</span></span>            | <span data-ttu-id="a4e0e-168">True</span><span class="sxs-lookup"><span data-stu-id="a4e0e-168">True</span></span>                            |
| <span data-ttu-id="a4e0e-169">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4e0e-169">Is-Single-Valued</span></span>       | <span data-ttu-id="a4e0e-170">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-170">False</span></span>                           |
| <span data-ttu-id="a4e0e-171">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4e0e-171">Is Indexed</span></span>             | <span data-ttu-id="a4e0e-172">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-172">False</span></span>                           |
| <span data-ttu-id="a4e0e-173">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4e0e-173">In Global Catalog</span></span>      | <span data-ttu-id="a4e0e-174">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-174">False</span></span>                           |
| <span data-ttu-id="a4e0e-175">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4e0e-176">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4e0e-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a4e0e-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4e0e-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4e0e-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-179">Search-Flags</span></span>           | <span data-ttu-id="a4e0e-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4e0e-180">0x00000000</span></span>                      |
| <span data-ttu-id="a4e0e-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-181">System-Flags</span></span>           | <span data-ttu-id="a4e0e-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4e0e-182">0x00000010</span></span>                      |
| <span data-ttu-id="a4e0e-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4e0e-183">Classes used in</span></span>        | [<span data-ttu-id="a4e0e-184">**Início**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4e0e-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4e0e-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4e0e-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-186">Entry</span></span> | <span data-ttu-id="a4e0e-187">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a4e0e-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4e0e-188">Link-Id</span></span>                | <span data-ttu-id="a4e0e-189">43</span><span class="sxs-lookup"><span data-stu-id="a4e0e-189">43</span></span>                              |
| <span data-ttu-id="a4e0e-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-190">MAPI-Id</span></span>                | <span data-ttu-id="a4e0e-191">0x800E</span><span class="sxs-lookup"><span data-stu-id="a4e0e-191">0x800E</span></span>                          |
| <span data-ttu-id="a4e0e-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4e0e-192">System-Only</span></span>            | <span data-ttu-id="a4e0e-193">True</span><span class="sxs-lookup"><span data-stu-id="a4e0e-193">True</span></span>                            |
| <span data-ttu-id="a4e0e-194">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4e0e-194">Is-Single-Valued</span></span>       | <span data-ttu-id="a4e0e-195">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-195">False</span></span>                           |
| <span data-ttu-id="a4e0e-196">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4e0e-196">Is Indexed</span></span>             | <span data-ttu-id="a4e0e-197">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-197">False</span></span>                           |
| <span data-ttu-id="a4e0e-198">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4e0e-198">In Global Catalog</span></span>      | <span data-ttu-id="a4e0e-199">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-199">False</span></span>                           |
| <span data-ttu-id="a4e0e-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4e0e-201">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4e0e-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a4e0e-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4e0e-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4e0e-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-204">Search-Flags</span></span>           | <span data-ttu-id="a4e0e-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4e0e-205">0x00000000</span></span>                      |
| <span data-ttu-id="a4e0e-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-206">System-Flags</span></span>           | <span data-ttu-id="a4e0e-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4e0e-207">0x00000010</span></span>                      |
| <span data-ttu-id="a4e0e-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4e0e-208">Classes used in</span></span>        | [<span data-ttu-id="a4e0e-209">**Início**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a4e0e-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4e0e-210">Windows Server 2008</span></span>



| <span data-ttu-id="a4e0e-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-211">Entry</span></span> | <span data-ttu-id="a4e0e-212">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a4e0e-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4e0e-213">Link-Id</span></span>                | <span data-ttu-id="a4e0e-214">43</span><span class="sxs-lookup"><span data-stu-id="a4e0e-214">43</span></span>                              |
| <span data-ttu-id="a4e0e-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-215">MAPI-Id</span></span>                | <span data-ttu-id="a4e0e-216">0x800E</span><span class="sxs-lookup"><span data-stu-id="a4e0e-216">0x800E</span></span>                          |
| <span data-ttu-id="a4e0e-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4e0e-217">System-Only</span></span>            | <span data-ttu-id="a4e0e-218">True</span><span class="sxs-lookup"><span data-stu-id="a4e0e-218">True</span></span>                            |
| <span data-ttu-id="a4e0e-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4e0e-219">Is-Single-Valued</span></span>       | <span data-ttu-id="a4e0e-220">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-220">False</span></span>                           |
| <span data-ttu-id="a4e0e-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4e0e-221">Is Indexed</span></span>             | <span data-ttu-id="a4e0e-222">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-222">False</span></span>                           |
| <span data-ttu-id="a4e0e-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4e0e-223">In Global Catalog</span></span>      | <span data-ttu-id="a4e0e-224">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-224">False</span></span>                           |
| <span data-ttu-id="a4e0e-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4e0e-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4e0e-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a4e0e-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4e0e-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4e0e-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-229">Search-Flags</span></span>           | <span data-ttu-id="a4e0e-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4e0e-230">0x00000000</span></span>                      |
| <span data-ttu-id="a4e0e-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-231">System-Flags</span></span>           | <span data-ttu-id="a4e0e-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4e0e-232">0x00000010</span></span>                      |
| <span data-ttu-id="a4e0e-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4e0e-233">Classes used in</span></span>        | [<span data-ttu-id="a4e0e-234">**Início**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4e0e-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4e0e-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4e0e-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-236">Entry</span></span> | <span data-ttu-id="a4e0e-237">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a4e0e-238">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4e0e-238">Link-Id</span></span>                | <span data-ttu-id="a4e0e-239">43</span><span class="sxs-lookup"><span data-stu-id="a4e0e-239">43</span></span>                              |
| <span data-ttu-id="a4e0e-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-240">MAPI-Id</span></span>                | <span data-ttu-id="a4e0e-241">0x800E</span><span class="sxs-lookup"><span data-stu-id="a4e0e-241">0x800E</span></span>                          |
| <span data-ttu-id="a4e0e-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4e0e-242">System-Only</span></span>            | <span data-ttu-id="a4e0e-243">True</span><span class="sxs-lookup"><span data-stu-id="a4e0e-243">True</span></span>                            |
| <span data-ttu-id="a4e0e-244">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4e0e-244">Is-Single-Valued</span></span>       | <span data-ttu-id="a4e0e-245">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-245">False</span></span>                           |
| <span data-ttu-id="a4e0e-246">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4e0e-246">Is Indexed</span></span>             | <span data-ttu-id="a4e0e-247">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-247">False</span></span>                           |
| <span data-ttu-id="a4e0e-248">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4e0e-248">In Global Catalog</span></span>      | <span data-ttu-id="a4e0e-249">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-249">False</span></span>                           |
| <span data-ttu-id="a4e0e-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4e0e-251">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4e0e-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a4e0e-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4e0e-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4e0e-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-254">Search-Flags</span></span>           | <span data-ttu-id="a4e0e-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4e0e-255">0x00000000</span></span>                      |
| <span data-ttu-id="a4e0e-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-256">System-Flags</span></span>           | <span data-ttu-id="a4e0e-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4e0e-257">0x00000010</span></span>                      |
| <span data-ttu-id="a4e0e-258">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4e0e-258">Classes used in</span></span>        | [<span data-ttu-id="a4e0e-259">**Início**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a4e0e-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4e0e-260">Windows Server 2012</span></span>



| <span data-ttu-id="a4e0e-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4e0e-261">Entry</span></span> | <span data-ttu-id="a4e0e-262">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a4e0e-263">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4e0e-263">Link-Id</span></span>                | <span data-ttu-id="a4e0e-264">43</span><span class="sxs-lookup"><span data-stu-id="a4e0e-264">43</span></span>                              |
| <span data-ttu-id="a4e0e-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4e0e-265">MAPI-Id</span></span>                | <span data-ttu-id="a4e0e-266">0x800E</span><span class="sxs-lookup"><span data-stu-id="a4e0e-266">0x800E</span></span>                          |
| <span data-ttu-id="a4e0e-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4e0e-267">System-Only</span></span>            | <span data-ttu-id="a4e0e-268">True</span><span class="sxs-lookup"><span data-stu-id="a4e0e-268">True</span></span>                            |
| <span data-ttu-id="a4e0e-269">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4e0e-269">Is-Single-Valued</span></span>       | <span data-ttu-id="a4e0e-270">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-270">False</span></span>                           |
| <span data-ttu-id="a4e0e-271">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4e0e-271">Is Indexed</span></span>             | <span data-ttu-id="a4e0e-272">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-272">False</span></span>                           |
| <span data-ttu-id="a4e0e-273">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4e0e-273">In Global Catalog</span></span>      | <span data-ttu-id="a4e0e-274">Falso</span><span class="sxs-lookup"><span data-stu-id="a4e0e-274">False</span></span>                           |
| <span data-ttu-id="a4e0e-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4e0e-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4e0e-276">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4e0e-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a4e0e-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4e0e-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4e0e-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a4e0e-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-279">Search-Flags</span></span>           | <span data-ttu-id="a4e0e-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4e0e-280">0x00000000</span></span>                      |
| <span data-ttu-id="a4e0e-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4e0e-281">System-Flags</span></span>           | <span data-ttu-id="a4e0e-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4e0e-282">0x00000010</span></span>                      |
| <span data-ttu-id="a4e0e-283">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4e0e-283">Classes used in</span></span>        | [<span data-ttu-id="a4e0e-284">**Início**</span><span class="sxs-lookup"><span data-stu-id="a4e0e-284">**Top**</span></span>](c-top.md)<br/> |



 

 





