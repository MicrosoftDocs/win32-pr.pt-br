---
title: Atributo netboot-GUID
description: Inicialização em disco de um GUID na placa do computador. Corresponde ao endereço MAC da placa de rede do computador.
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- Esquema netboot-GUID de atributo do AD
- Esquema de AD do atributo netbootGUID
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825315"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="9cdcc-106">Atributo netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="9cdcc-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="9cdcc-107">Inicialização em disco: o GUID da placa do computador.</span><span class="sxs-lookup"><span data-stu-id="9cdcc-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="9cdcc-108">Corresponde ao endereço MAC da placa de rede do computador.</span><span class="sxs-lookup"><span data-stu-id="9cdcc-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="9cdcc-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-109">Entry</span></span> | <span data-ttu-id="9cdcc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9cdcc-111">CN</span><span class="sxs-lookup"><span data-stu-id="9cdcc-111">CN</span></span>                | <span data-ttu-id="9cdcc-112">Netboot – GUID</span><span class="sxs-lookup"><span data-stu-id="9cdcc-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="9cdcc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9cdcc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9cdcc-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="9cdcc-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="9cdcc-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9cdcc-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9cdcc-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9cdcc-116">Update Privilege</span></span>  | <span data-ttu-id="9cdcc-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="9cdcc-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="9cdcc-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9cdcc-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="9cdcc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-119">Attribute-Id</span></span>      | <span data-ttu-id="9cdcc-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="9cdcc-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="9cdcc-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9cdcc-121">System-Id-Guid</span></span>    | <span data-ttu-id="9cdcc-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9cdcc-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="9cdcc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cdcc-123">Syntax</span></span>            | [<span data-ttu-id="9cdcc-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9cdcc-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="9cdcc-125">Implementations</span></span>

-   [<span data-ttu-id="9cdcc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9cdcc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9cdcc-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9cdcc-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9cdcc-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9cdcc-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9cdcc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9cdcc-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9cdcc-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-133">Entry</span></span> | <span data-ttu-id="9cdcc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9cdcc-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="9cdcc-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cdcc-137">System-Only</span></span>            | <span data-ttu-id="9cdcc-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9cdcc-138">False</span></span>                                     |
| <span data-ttu-id="9cdcc-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9cdcc-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9cdcc-140">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-140">True</span></span>                                      |
| <span data-ttu-id="9cdcc-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="9cdcc-141">Is Indexed</span></span>             | <span data-ttu-id="9cdcc-142">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-142">True</span></span>                                      |
| <span data-ttu-id="9cdcc-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9cdcc-143">In Global Catalog</span></span>      | <span data-ttu-id="9cdcc-144">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-144">True</span></span>                                      |
| <span data-ttu-id="9cdcc-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cdcc-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9cdcc-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9cdcc-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cdcc-147">Range-Lower</span></span>            | <span data-ttu-id="9cdcc-148">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-148">16</span></span>                                        |
| <span data-ttu-id="9cdcc-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cdcc-149">Range-Upper</span></span>            | <span data-ttu-id="9cdcc-150">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-150">16</span></span>                                        |
| <span data-ttu-id="9cdcc-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-151">Search-Flags</span></span>           | <span data-ttu-id="9cdcc-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cdcc-152">0x00000001</span></span>                                |
| <span data-ttu-id="9cdcc-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-153">System-Flags</span></span>           | <span data-ttu-id="9cdcc-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cdcc-154">0x00000010</span></span>                                |
| <span data-ttu-id="9cdcc-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9cdcc-155">Classes used in</span></span>        | [<span data-ttu-id="9cdcc-156">**Computador**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9cdcc-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9cdcc-157">Windows Server 2003</span></span>



| <span data-ttu-id="9cdcc-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-158">Entry</span></span> | <span data-ttu-id="9cdcc-159">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9cdcc-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="9cdcc-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cdcc-162">System-Only</span></span>            | <span data-ttu-id="9cdcc-163">Falso</span><span class="sxs-lookup"><span data-stu-id="9cdcc-163">False</span></span>                                     |
| <span data-ttu-id="9cdcc-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9cdcc-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9cdcc-165">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-165">True</span></span>                                      |
| <span data-ttu-id="9cdcc-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="9cdcc-166">Is Indexed</span></span>             | <span data-ttu-id="9cdcc-167">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-167">True</span></span>                                      |
| <span data-ttu-id="9cdcc-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9cdcc-168">In Global Catalog</span></span>      | <span data-ttu-id="9cdcc-169">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-169">True</span></span>                                      |
| <span data-ttu-id="9cdcc-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cdcc-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9cdcc-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9cdcc-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cdcc-172">Range-Lower</span></span>            | <span data-ttu-id="9cdcc-173">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-173">16</span></span>                                        |
| <span data-ttu-id="9cdcc-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cdcc-174">Range-Upper</span></span>            | <span data-ttu-id="9cdcc-175">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-175">16</span></span>                                        |
| <span data-ttu-id="9cdcc-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-176">Search-Flags</span></span>           | <span data-ttu-id="9cdcc-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cdcc-177">0x00000001</span></span>                                |
| <span data-ttu-id="9cdcc-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-178">System-Flags</span></span>           | <span data-ttu-id="9cdcc-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cdcc-179">0x00000010</span></span>                                |
| <span data-ttu-id="9cdcc-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9cdcc-180">Classes used in</span></span>        | [<span data-ttu-id="9cdcc-181">**Computador**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9cdcc-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9cdcc-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9cdcc-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-183">Entry</span></span> | <span data-ttu-id="9cdcc-184">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9cdcc-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="9cdcc-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cdcc-187">System-Only</span></span>            | <span data-ttu-id="9cdcc-188">Falso</span><span class="sxs-lookup"><span data-stu-id="9cdcc-188">False</span></span>                                     |
| <span data-ttu-id="9cdcc-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9cdcc-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9cdcc-190">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-190">True</span></span>                                      |
| <span data-ttu-id="9cdcc-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="9cdcc-191">Is Indexed</span></span>             | <span data-ttu-id="9cdcc-192">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-192">True</span></span>                                      |
| <span data-ttu-id="9cdcc-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9cdcc-193">In Global Catalog</span></span>      | <span data-ttu-id="9cdcc-194">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-194">True</span></span>                                      |
| <span data-ttu-id="9cdcc-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cdcc-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9cdcc-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9cdcc-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cdcc-197">Range-Lower</span></span>            | <span data-ttu-id="9cdcc-198">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-198">16</span></span>                                        |
| <span data-ttu-id="9cdcc-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cdcc-199">Range-Upper</span></span>            | <span data-ttu-id="9cdcc-200">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-200">16</span></span>                                        |
| <span data-ttu-id="9cdcc-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-201">Search-Flags</span></span>           | <span data-ttu-id="9cdcc-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cdcc-202">0x00000001</span></span>                                |
| <span data-ttu-id="9cdcc-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-203">System-Flags</span></span>           | <span data-ttu-id="9cdcc-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cdcc-204">0x00000010</span></span>                                |
| <span data-ttu-id="9cdcc-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9cdcc-205">Classes used in</span></span>        | [<span data-ttu-id="9cdcc-206">**Computador**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9cdcc-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cdcc-207">Windows Server 2008</span></span>



| <span data-ttu-id="9cdcc-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-208">Entry</span></span> | <span data-ttu-id="9cdcc-209">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9cdcc-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="9cdcc-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cdcc-212">System-Only</span></span>            | <span data-ttu-id="9cdcc-213">Falso</span><span class="sxs-lookup"><span data-stu-id="9cdcc-213">False</span></span>                                     |
| <span data-ttu-id="9cdcc-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9cdcc-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9cdcc-215">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-215">True</span></span>                                      |
| <span data-ttu-id="9cdcc-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="9cdcc-216">Is Indexed</span></span>             | <span data-ttu-id="9cdcc-217">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-217">True</span></span>                                      |
| <span data-ttu-id="9cdcc-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9cdcc-218">In Global Catalog</span></span>      | <span data-ttu-id="9cdcc-219">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-219">True</span></span>                                      |
| <span data-ttu-id="9cdcc-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cdcc-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9cdcc-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9cdcc-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cdcc-222">Range-Lower</span></span>            | <span data-ttu-id="9cdcc-223">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-223">16</span></span>                                        |
| <span data-ttu-id="9cdcc-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cdcc-224">Range-Upper</span></span>            | <span data-ttu-id="9cdcc-225">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-225">16</span></span>                                        |
| <span data-ttu-id="9cdcc-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-226">Search-Flags</span></span>           | <span data-ttu-id="9cdcc-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cdcc-227">0x00000001</span></span>                                |
| <span data-ttu-id="9cdcc-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-228">System-Flags</span></span>           | <span data-ttu-id="9cdcc-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cdcc-229">0x00000010</span></span>                                |
| <span data-ttu-id="9cdcc-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9cdcc-230">Classes used in</span></span>        | [<span data-ttu-id="9cdcc-231">**Computador**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9cdcc-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9cdcc-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9cdcc-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-233">Entry</span></span> | <span data-ttu-id="9cdcc-234">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9cdcc-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="9cdcc-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cdcc-237">System-Only</span></span>            | <span data-ttu-id="9cdcc-238">Falso</span><span class="sxs-lookup"><span data-stu-id="9cdcc-238">False</span></span>                                     |
| <span data-ttu-id="9cdcc-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9cdcc-239">Is-Single-Valued</span></span>       | <span data-ttu-id="9cdcc-240">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-240">True</span></span>                                      |
| <span data-ttu-id="9cdcc-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="9cdcc-241">Is Indexed</span></span>             | <span data-ttu-id="9cdcc-242">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-242">True</span></span>                                      |
| <span data-ttu-id="9cdcc-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9cdcc-243">In Global Catalog</span></span>      | <span data-ttu-id="9cdcc-244">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-244">True</span></span>                                      |
| <span data-ttu-id="9cdcc-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cdcc-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9cdcc-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9cdcc-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cdcc-247">Range-Lower</span></span>            | <span data-ttu-id="9cdcc-248">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-248">16</span></span>                                        |
| <span data-ttu-id="9cdcc-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cdcc-249">Range-Upper</span></span>            | <span data-ttu-id="9cdcc-250">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-250">16</span></span>                                        |
| <span data-ttu-id="9cdcc-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-251">Search-Flags</span></span>           | <span data-ttu-id="9cdcc-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cdcc-252">0x00000001</span></span>                                |
| <span data-ttu-id="9cdcc-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-253">System-Flags</span></span>           | <span data-ttu-id="9cdcc-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cdcc-254">0x00000010</span></span>                                |
| <span data-ttu-id="9cdcc-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9cdcc-255">Classes used in</span></span>        | [<span data-ttu-id="9cdcc-256">**Computador**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9cdcc-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9cdcc-257">Windows Server 2012</span></span>



| <span data-ttu-id="9cdcc-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="9cdcc-258">Entry</span></span> | <span data-ttu-id="9cdcc-259">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="9cdcc-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="9cdcc-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cdcc-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="9cdcc-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cdcc-262">System-Only</span></span>            | <span data-ttu-id="9cdcc-263">Falso</span><span class="sxs-lookup"><span data-stu-id="9cdcc-263">False</span></span>                                     |
| <span data-ttu-id="9cdcc-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9cdcc-264">Is-Single-Valued</span></span>       | <span data-ttu-id="9cdcc-265">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-265">True</span></span>                                      |
| <span data-ttu-id="9cdcc-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="9cdcc-266">Is Indexed</span></span>             | <span data-ttu-id="9cdcc-267">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-267">True</span></span>                                      |
| <span data-ttu-id="9cdcc-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9cdcc-268">In Global Catalog</span></span>      | <span data-ttu-id="9cdcc-269">True</span><span class="sxs-lookup"><span data-stu-id="9cdcc-269">True</span></span>                                      |
| <span data-ttu-id="9cdcc-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9cdcc-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cdcc-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9cdcc-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="9cdcc-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cdcc-272">Range-Lower</span></span>            | <span data-ttu-id="9cdcc-273">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-273">16</span></span>                                        |
| <span data-ttu-id="9cdcc-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cdcc-274">Range-Upper</span></span>            | <span data-ttu-id="9cdcc-275">16</span><span class="sxs-lookup"><span data-stu-id="9cdcc-275">16</span></span>                                        |
| <span data-ttu-id="9cdcc-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-276">Search-Flags</span></span>           | <span data-ttu-id="9cdcc-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cdcc-277">0x00000001</span></span>                                |
| <span data-ttu-id="9cdcc-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cdcc-278">System-Flags</span></span>           | <span data-ttu-id="9cdcc-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cdcc-279">0x00000010</span></span>                                |
| <span data-ttu-id="9cdcc-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9cdcc-280">Classes used in</span></span>        | [<span data-ttu-id="9cdcc-281">**Computador**</span><span class="sxs-lookup"><span data-stu-id="9cdcc-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





