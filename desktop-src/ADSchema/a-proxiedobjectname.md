---
title: Atributo de nome de objeto com proxy
description: Esse atributo é usado internamente pelo Active Directory para ajudar a acompanhar as movimentações entre domínios.
ms.assetid: 661ea322-f78c-44dc-8d64-4f28ead1a7aa
ms.tgt_platform: multiple
keywords:
- Atributo do AD-Object-Name-Schema
- Esquema de AD do atributo proxiedObjectName
topic_type:
- apiref
api_name:
- Proxied-Object-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ffafbbea411c950954102a788226c29589029e1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756477"
---
# <a name="proxied-object-name-attribute"></a><span data-ttu-id="ee93d-105">Atributo de nome de objeto com proxy</span><span class="sxs-lookup"><span data-stu-id="ee93d-105">Proxied-Object-Name attribute</span></span>

<span data-ttu-id="ee93d-106">Esse atributo é usado internamente pelo Active Directory para ajudar a acompanhar as movimentações entre domínios.</span><span class="sxs-lookup"><span data-stu-id="ee93d-106">This attribute is used internally by Active Directory to help track interdomain moves.</span></span>



| <span data-ttu-id="ee93d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-107">Entry</span></span> | <span data-ttu-id="ee93d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="ee93d-109">CN</span><span class="sxs-lookup"><span data-stu-id="ee93d-109">CN</span></span>                | <span data-ttu-id="ee93d-110">Nome-do-objeto-proxy</span><span class="sxs-lookup"><span data-stu-id="ee93d-110">Proxied-Object-Name</span></span>                             |
| <span data-ttu-id="ee93d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ee93d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ee93d-112">proxiedObjectName</span><span class="sxs-lookup"><span data-stu-id="ee93d-112">proxiedObjectName</span></span>                               |
| <span data-ttu-id="ee93d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ee93d-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="ee93d-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ee93d-114">Update Privilege</span></span>  | <span data-ttu-id="ee93d-115">Isso é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="ee93d-115">This is used by the system.</span></span>                     |
| <span data-ttu-id="ee93d-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ee93d-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="ee93d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-117">Attribute-Id</span></span>      | <span data-ttu-id="ee93d-118">1.2.840.113556.1.4.1249</span><span class="sxs-lookup"><span data-stu-id="ee93d-118">1.2.840.113556.1.4.1249</span></span>                         |
| <span data-ttu-id="ee93d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ee93d-119">System-Id-Guid</span></span>    | <span data-ttu-id="ee93d-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ee93d-120">e1aea402-cd5b-11d0-afff-0000f80367c1</span></span>            |
| <span data-ttu-id="ee93d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee93d-121">Syntax</span></span>            | [<span data-ttu-id="ee93d-122">**Objeto (DN-binário)**</span><span class="sxs-lookup"><span data-stu-id="ee93d-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="ee93d-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="ee93d-123">Implementations</span></span>

-   [<span data-ttu-id="ee93d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ee93d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ee93d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee93d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee93d-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ee93d-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ee93d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee93d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee93d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee93d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee93d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee93d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee93d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee93d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ee93d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee93d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ee93d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-132">Entry</span></span> | <span data-ttu-id="ee93d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-136">System-Only</span></span>            | <span data-ttu-id="ee93d-137">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-137">True</span></span>                            |
| <span data-ttu-id="ee93d-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-139">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-139">True</span></span>                            |
| <span data-ttu-id="ee93d-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-140">Is Indexed</span></span>             | <span data-ttu-id="ee93d-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-141">False</span></span>                           |
| <span data-ttu-id="ee93d-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-142">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-143">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-143">True</span></span>                            |
| <span data-ttu-id="ee93d-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-148">Search-Flags</span></span>           | <span data-ttu-id="ee93d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-149">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-150">System-Flags</span></span>           | <span data-ttu-id="ee93d-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-151">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-152">Classes used in</span></span>        | [<span data-ttu-id="ee93d-153">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ee93d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee93d-154">Windows Server 2003</span></span>



| <span data-ttu-id="ee93d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-155">Entry</span></span> | <span data-ttu-id="ee93d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-159">System-Only</span></span>            | <span data-ttu-id="ee93d-160">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-160">True</span></span>                            |
| <span data-ttu-id="ee93d-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-162">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-162">True</span></span>                            |
| <span data-ttu-id="ee93d-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-163">Is Indexed</span></span>             | <span data-ttu-id="ee93d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-164">False</span></span>                           |
| <span data-ttu-id="ee93d-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-165">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-166">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-166">True</span></span>                            |
| <span data-ttu-id="ee93d-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-171">Search-Flags</span></span>           | <span data-ttu-id="ee93d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-172">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-173">System-Flags</span></span>           | <span data-ttu-id="ee93d-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-174">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-175">Classes used in</span></span>        | [<span data-ttu-id="ee93d-176">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ee93d-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="ee93d-177">ADAM</span></span>



| <span data-ttu-id="ee93d-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-178">Entry</span></span> | <span data-ttu-id="ee93d-179">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-182">System-Only</span></span>            | <span data-ttu-id="ee93d-183">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-183">True</span></span>                            |
| <span data-ttu-id="ee93d-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-185">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-185">True</span></span>                            |
| <span data-ttu-id="ee93d-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-186">Is Indexed</span></span>             | <span data-ttu-id="ee93d-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-187">False</span></span>                           |
| <span data-ttu-id="ee93d-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-188">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-189">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-189">True</span></span>                            |
| <span data-ttu-id="ee93d-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-194">Search-Flags</span></span>           | <span data-ttu-id="ee93d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-195">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-196">System-Flags</span></span>           | <span data-ttu-id="ee93d-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-197">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-198">Classes used in</span></span>        | [<span data-ttu-id="ee93d-199">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee93d-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee93d-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee93d-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-201">Entry</span></span> | <span data-ttu-id="ee93d-202">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-205">System-Only</span></span>            | <span data-ttu-id="ee93d-206">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-206">True</span></span>                            |
| <span data-ttu-id="ee93d-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-208">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-208">True</span></span>                            |
| <span data-ttu-id="ee93d-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-209">Is Indexed</span></span>             | <span data-ttu-id="ee93d-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-210">False</span></span>                           |
| <span data-ttu-id="ee93d-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-211">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-212">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-212">True</span></span>                            |
| <span data-ttu-id="ee93d-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-217">Search-Flags</span></span>           | <span data-ttu-id="ee93d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-218">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-219">System-Flags</span></span>           | <span data-ttu-id="ee93d-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-220">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-221">Classes used in</span></span>        | [<span data-ttu-id="ee93d-222">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee93d-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee93d-223">Windows Server 2008</span></span>



| <span data-ttu-id="ee93d-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-224">Entry</span></span> | <span data-ttu-id="ee93d-225">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-228">System-Only</span></span>            | <span data-ttu-id="ee93d-229">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-229">True</span></span>                            |
| <span data-ttu-id="ee93d-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-231">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-231">True</span></span>                            |
| <span data-ttu-id="ee93d-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-232">Is Indexed</span></span>             | <span data-ttu-id="ee93d-233">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-233">False</span></span>                           |
| <span data-ttu-id="ee93d-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-234">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-235">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-235">True</span></span>                            |
| <span data-ttu-id="ee93d-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-240">Search-Flags</span></span>           | <span data-ttu-id="ee93d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-241">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-242">System-Flags</span></span>           | <span data-ttu-id="ee93d-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-243">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-244">Classes used in</span></span>        | [<span data-ttu-id="ee93d-245">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee93d-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee93d-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee93d-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-247">Entry</span></span> | <span data-ttu-id="ee93d-248">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-251">System-Only</span></span>            | <span data-ttu-id="ee93d-252">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-252">True</span></span>                            |
| <span data-ttu-id="ee93d-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-254">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-254">True</span></span>                            |
| <span data-ttu-id="ee93d-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-255">Is Indexed</span></span>             | <span data-ttu-id="ee93d-256">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-256">False</span></span>                           |
| <span data-ttu-id="ee93d-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-257">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-258">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-258">True</span></span>                            |
| <span data-ttu-id="ee93d-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-263">Search-Flags</span></span>           | <span data-ttu-id="ee93d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-264">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-265">System-Flags</span></span>           | <span data-ttu-id="ee93d-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-266">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-267">Classes used in</span></span>        | [<span data-ttu-id="ee93d-268">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee93d-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee93d-269">Windows Server 2012</span></span>



| <span data-ttu-id="ee93d-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="ee93d-270">Entry</span></span> | <span data-ttu-id="ee93d-271">Valor</span><span class="sxs-lookup"><span data-stu-id="ee93d-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ee93d-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="ee93d-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee93d-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ee93d-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee93d-274">System-Only</span></span>            | <span data-ttu-id="ee93d-275">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-275">True</span></span>                            |
| <span data-ttu-id="ee93d-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ee93d-276">Is-Single-Valued</span></span>       | <span data-ttu-id="ee93d-277">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-277">True</span></span>                            |
| <span data-ttu-id="ee93d-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="ee93d-278">Is Indexed</span></span>             | <span data-ttu-id="ee93d-279">Falso</span><span class="sxs-lookup"><span data-stu-id="ee93d-279">False</span></span>                           |
| <span data-ttu-id="ee93d-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ee93d-280">In Global Catalog</span></span>      | <span data-ttu-id="ee93d-281">True</span><span class="sxs-lookup"><span data-stu-id="ee93d-281">True</span></span>                            |
| <span data-ttu-id="ee93d-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ee93d-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee93d-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ee93d-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ee93d-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee93d-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ee93d-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee93d-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ee93d-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-286">Search-Flags</span></span>           | <span data-ttu-id="ee93d-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee93d-287">0x00000000</span></span>                      |
| <span data-ttu-id="ee93d-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee93d-288">System-Flags</span></span>           | <span data-ttu-id="ee93d-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="ee93d-289">0x00000012</span></span>                      |
| <span data-ttu-id="ee93d-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ee93d-290">Classes used in</span></span>        | [<span data-ttu-id="ee93d-291">**Início**</span><span class="sxs-lookup"><span data-stu-id="ee93d-291">**Top**</span></span>](c-top.md)<br/> |



 

 





