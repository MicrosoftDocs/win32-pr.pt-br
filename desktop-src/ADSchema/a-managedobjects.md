---
title: Managed-Objects atributo
description: Contém a lista de objetos que são gerenciados pelo usuário. Os objetos listados são aqueles que têm a propriedade managedBy da propriedade definida para esse usuário. Cada item da lista é uma referência vinculada ao objeto gerenciado.
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- Esquema de Managed-Objects do atributo AD
- Esquema de AD do atributo managedObjects
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755479"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="f1280-107">Managed-Objects atributo</span><span class="sxs-lookup"><span data-stu-id="f1280-107">Managed-Objects attribute</span></span>

<span data-ttu-id="f1280-108">Contém a lista de objetos que são gerenciados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f1280-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="f1280-109">Os objetos listados são aqueles que têm a propriedade managedBy da propriedade definida para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="f1280-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="f1280-110">Cada item da lista é uma referência vinculada ao objeto gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f1280-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="f1280-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-111">Entry</span></span> | <span data-ttu-id="f1280-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1280-113">CN</span><span class="sxs-lookup"><span data-stu-id="f1280-113">CN</span></span>                | <span data-ttu-id="f1280-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="f1280-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="f1280-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f1280-115">Ldap-Display-Name</span></span> | <span data-ttu-id="f1280-116">managedObjects</span><span class="sxs-lookup"><span data-stu-id="f1280-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="f1280-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f1280-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="f1280-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f1280-118">Update Privilege</span></span>  | <span data-ttu-id="f1280-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f1280-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="f1280-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f1280-120">Update Frequency</span></span>  | <span data-ttu-id="f1280-121">Quando o registro dos usuários é criado e sempre que os objetos gerenciados precisam ser alterados.</span><span class="sxs-lookup"><span data-stu-id="f1280-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="f1280-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-122">Attribute-Id</span></span>      | <span data-ttu-id="f1280-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="f1280-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="f1280-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f1280-124">System-Id-Guid</span></span>    | <span data-ttu-id="f1280-125">0296c124-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f1280-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="f1280-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1280-126">Syntax</span></span>            | [<span data-ttu-id="f1280-127">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f1280-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="f1280-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="f1280-128">Implementations</span></span>

-   [<span data-ttu-id="f1280-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1280-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1280-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1280-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1280-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f1280-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f1280-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1280-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1280-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1280-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1280-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1280-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1280-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1280-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1280-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1280-136">Windows 2000 Server</span></span>



| <span data-ttu-id="f1280-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-137">Entry</span></span> | <span data-ttu-id="f1280-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-139">Link-Id</span></span>                | <span data-ttu-id="f1280-140">73</span><span class="sxs-lookup"><span data-stu-id="f1280-140">73</span></span>                              |
| <span data-ttu-id="f1280-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-141">MAPI-Id</span></span>                | <span data-ttu-id="f1280-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-142">0x8024</span></span>                          |
| <span data-ttu-id="f1280-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-143">System-Only</span></span>            | <span data-ttu-id="f1280-144">True</span><span class="sxs-lookup"><span data-stu-id="f1280-144">True</span></span>                            |
| <span data-ttu-id="f1280-145">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-145">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-146">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-146">False</span></span>                           |
| <span data-ttu-id="f1280-147">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-147">Is Indexed</span></span>             | <span data-ttu-id="f1280-148">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-148">False</span></span>                           |
| <span data-ttu-id="f1280-149">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-149">In Global Catalog</span></span>      | <span data-ttu-id="f1280-150">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-150">False</span></span>                           |
| <span data-ttu-id="f1280-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-152">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-155">Search-Flags</span></span>           | <span data-ttu-id="f1280-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-156">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-157">System-Flags</span></span>           | <span data-ttu-id="f1280-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-158">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-159">Classes used in</span></span>        | [<span data-ttu-id="f1280-160">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1280-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1280-161">Windows Server 2003</span></span>



| <span data-ttu-id="f1280-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-162">Entry</span></span> | <span data-ttu-id="f1280-163">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-164">Link-Id</span></span>                | <span data-ttu-id="f1280-165">73</span><span class="sxs-lookup"><span data-stu-id="f1280-165">73</span></span>                              |
| <span data-ttu-id="f1280-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-166">MAPI-Id</span></span>                | <span data-ttu-id="f1280-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-167">0x8024</span></span>                          |
| <span data-ttu-id="f1280-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-168">System-Only</span></span>            | <span data-ttu-id="f1280-169">True</span><span class="sxs-lookup"><span data-stu-id="f1280-169">True</span></span>                            |
| <span data-ttu-id="f1280-170">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-170">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-171">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-171">False</span></span>                           |
| <span data-ttu-id="f1280-172">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-172">Is Indexed</span></span>             | <span data-ttu-id="f1280-173">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-173">False</span></span>                           |
| <span data-ttu-id="f1280-174">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-174">In Global Catalog</span></span>      | <span data-ttu-id="f1280-175">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-175">False</span></span>                           |
| <span data-ttu-id="f1280-176">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-177">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-180">Search-Flags</span></span>           | <span data-ttu-id="f1280-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-181">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-182">System-Flags</span></span>           | <span data-ttu-id="f1280-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-183">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-184">Classes used in</span></span>        | [<span data-ttu-id="f1280-185">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f1280-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="f1280-186">ADAM</span></span>



| <span data-ttu-id="f1280-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-187">Entry</span></span> | <span data-ttu-id="f1280-188">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-189">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-189">Link-Id</span></span>                | <span data-ttu-id="f1280-190">73</span><span class="sxs-lookup"><span data-stu-id="f1280-190">73</span></span>                              |
| <span data-ttu-id="f1280-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-191">MAPI-Id</span></span>                | <span data-ttu-id="f1280-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-192">0x8024</span></span>                          |
| <span data-ttu-id="f1280-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-193">System-Only</span></span>            | <span data-ttu-id="f1280-194">True</span><span class="sxs-lookup"><span data-stu-id="f1280-194">True</span></span>                            |
| <span data-ttu-id="f1280-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-195">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-196">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-196">False</span></span>                           |
| <span data-ttu-id="f1280-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-197">Is Indexed</span></span>             | <span data-ttu-id="f1280-198">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-198">False</span></span>                           |
| <span data-ttu-id="f1280-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-199">In Global Catalog</span></span>      | <span data-ttu-id="f1280-200">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-200">False</span></span>                           |
| <span data-ttu-id="f1280-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-205">Search-Flags</span></span>           | <span data-ttu-id="f1280-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-206">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-207">System-Flags</span></span>           | <span data-ttu-id="f1280-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-208">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-209">Classes used in</span></span>        | [<span data-ttu-id="f1280-210">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1280-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1280-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1280-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-212">Entry</span></span> | <span data-ttu-id="f1280-213">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-214">Link-Id</span></span>                | <span data-ttu-id="f1280-215">73</span><span class="sxs-lookup"><span data-stu-id="f1280-215">73</span></span>                              |
| <span data-ttu-id="f1280-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-216">MAPI-Id</span></span>                | <span data-ttu-id="f1280-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-217">0x8024</span></span>                          |
| <span data-ttu-id="f1280-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-218">System-Only</span></span>            | <span data-ttu-id="f1280-219">True</span><span class="sxs-lookup"><span data-stu-id="f1280-219">True</span></span>                            |
| <span data-ttu-id="f1280-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-220">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-221">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-221">False</span></span>                           |
| <span data-ttu-id="f1280-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-222">Is Indexed</span></span>             | <span data-ttu-id="f1280-223">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-223">False</span></span>                           |
| <span data-ttu-id="f1280-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-224">In Global Catalog</span></span>      | <span data-ttu-id="f1280-225">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-225">False</span></span>                           |
| <span data-ttu-id="f1280-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-230">Search-Flags</span></span>           | <span data-ttu-id="f1280-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-231">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-232">System-Flags</span></span>           | <span data-ttu-id="f1280-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-233">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-234">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-234">Classes used in</span></span>        | [<span data-ttu-id="f1280-235">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1280-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1280-236">Windows Server 2008</span></span>



| <span data-ttu-id="f1280-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-237">Entry</span></span> | <span data-ttu-id="f1280-238">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-239">Link-Id</span></span>                | <span data-ttu-id="f1280-240">73</span><span class="sxs-lookup"><span data-stu-id="f1280-240">73</span></span>                              |
| <span data-ttu-id="f1280-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-241">MAPI-Id</span></span>                | <span data-ttu-id="f1280-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-242">0x8024</span></span>                          |
| <span data-ttu-id="f1280-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-243">System-Only</span></span>            | <span data-ttu-id="f1280-244">True</span><span class="sxs-lookup"><span data-stu-id="f1280-244">True</span></span>                            |
| <span data-ttu-id="f1280-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-245">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-246">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-246">False</span></span>                           |
| <span data-ttu-id="f1280-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-247">Is Indexed</span></span>             | <span data-ttu-id="f1280-248">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-248">False</span></span>                           |
| <span data-ttu-id="f1280-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-249">In Global Catalog</span></span>      | <span data-ttu-id="f1280-250">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-250">False</span></span>                           |
| <span data-ttu-id="f1280-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-255">Search-Flags</span></span>           | <span data-ttu-id="f1280-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-256">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-257">System-Flags</span></span>           | <span data-ttu-id="f1280-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-258">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-259">Classes used in</span></span>        | [<span data-ttu-id="f1280-260">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1280-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1280-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1280-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-262">Entry</span></span> | <span data-ttu-id="f1280-263">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-264">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-264">Link-Id</span></span>                | <span data-ttu-id="f1280-265">73</span><span class="sxs-lookup"><span data-stu-id="f1280-265">73</span></span>                              |
| <span data-ttu-id="f1280-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-266">MAPI-Id</span></span>                | <span data-ttu-id="f1280-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-267">0x8024</span></span>                          |
| <span data-ttu-id="f1280-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-268">System-Only</span></span>            | <span data-ttu-id="f1280-269">True</span><span class="sxs-lookup"><span data-stu-id="f1280-269">True</span></span>                            |
| <span data-ttu-id="f1280-270">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-270">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-271">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-271">False</span></span>                           |
| <span data-ttu-id="f1280-272">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-272">Is Indexed</span></span>             | <span data-ttu-id="f1280-273">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-273">False</span></span>                           |
| <span data-ttu-id="f1280-274">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-274">In Global Catalog</span></span>      | <span data-ttu-id="f1280-275">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-275">False</span></span>                           |
| <span data-ttu-id="f1280-276">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-277">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-280">Search-Flags</span></span>           | <span data-ttu-id="f1280-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-281">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-282">System-Flags</span></span>           | <span data-ttu-id="f1280-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-283">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-284">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-284">Classes used in</span></span>        | [<span data-ttu-id="f1280-285">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1280-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1280-286">Windows Server 2012</span></span>



| <span data-ttu-id="f1280-287">Entrada</span><span class="sxs-lookup"><span data-stu-id="f1280-287">Entry</span></span> | <span data-ttu-id="f1280-288">Valor</span><span class="sxs-lookup"><span data-stu-id="f1280-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1280-289">ID do link</span><span class="sxs-lookup"><span data-stu-id="f1280-289">Link-Id</span></span>                | <span data-ttu-id="f1280-290">73</span><span class="sxs-lookup"><span data-stu-id="f1280-290">73</span></span>                              |
| <span data-ttu-id="f1280-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1280-291">MAPI-Id</span></span>                | <span data-ttu-id="f1280-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="f1280-292">0x8024</span></span>                          |
| <span data-ttu-id="f1280-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1280-293">System-Only</span></span>            | <span data-ttu-id="f1280-294">True</span><span class="sxs-lookup"><span data-stu-id="f1280-294">True</span></span>                            |
| <span data-ttu-id="f1280-295">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f1280-295">Is-Single-Valued</span></span>       | <span data-ttu-id="f1280-296">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-296">False</span></span>                           |
| <span data-ttu-id="f1280-297">É indexado</span><span class="sxs-lookup"><span data-stu-id="f1280-297">Is Indexed</span></span>             | <span data-ttu-id="f1280-298">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-298">False</span></span>                           |
| <span data-ttu-id="f1280-299">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f1280-299">In Global Catalog</span></span>      | <span data-ttu-id="f1280-300">Falso</span><span class="sxs-lookup"><span data-stu-id="f1280-300">False</span></span>                           |
| <span data-ttu-id="f1280-301">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f1280-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1280-302">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f1280-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1280-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1280-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f1280-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1280-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f1280-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-305">Search-Flags</span></span>           | <span data-ttu-id="f1280-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f1280-306">0x00000000</span></span>                      |
| <span data-ttu-id="f1280-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1280-307">System-Flags</span></span>           | <span data-ttu-id="f1280-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f1280-308">0x00000010</span></span>                      |
| <span data-ttu-id="f1280-309">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f1280-309">Classes used in</span></span>        | [<span data-ttu-id="f1280-310">**Início**</span><span class="sxs-lookup"><span data-stu-id="f1280-310">**Top**</span></span>](c-top.md)<br/> |



 

 





