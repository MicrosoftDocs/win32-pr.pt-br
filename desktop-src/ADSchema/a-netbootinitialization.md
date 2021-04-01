---
title: Netboot-Initialization atributo
description: Caminho de inicialização padrão para inicialização em disco.
ms.assetid: 359f9fff-1630-4c47-9221-1a2cc6249567
ms.tgt_platform: multiple
keywords:
- Esquema de Netboot-Initialization do atributo AD
- Esquema de AD do atributo netbootInitialization
topic_type:
- apiref
api_name:
- Netboot-Initialization
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4232d57b38e87386b340810f5edea47f2e409c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645421"
---
# <a name="netboot-initialization-attribute"></a><span data-ttu-id="c9f6d-105">Netboot-Initialization atributo</span><span class="sxs-lookup"><span data-stu-id="c9f6d-105">Netboot-Initialization attribute</span></span>

<span data-ttu-id="c9f6d-106">Caminho de inicialização padrão para inicialização em disco.</span><span class="sxs-lookup"><span data-stu-id="c9f6d-106">Default boot path for diskless boot.</span></span>



| <span data-ttu-id="c9f6d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-107">Entry</span></span> | <span data-ttu-id="c9f6d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c9f6d-109">CN</span><span class="sxs-lookup"><span data-stu-id="c9f6d-109">CN</span></span>                | <span data-ttu-id="c9f6d-110">Netboot-Initialization</span><span class="sxs-lookup"><span data-stu-id="c9f6d-110">Netboot-Initialization</span></span>                      |
| <span data-ttu-id="c9f6d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c9f6d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c9f6d-112">netbootInitialization</span><span class="sxs-lookup"><span data-stu-id="c9f6d-112">netbootInitialization</span></span>                       |
| <span data-ttu-id="c9f6d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c9f6d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c9f6d-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c9f6d-114">Update Privilege</span></span>  | <span data-ttu-id="c9f6d-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="c9f6d-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="c9f6d-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c9f6d-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c9f6d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-117">Attribute-Id</span></span>      | <span data-ttu-id="c9f6d-118">1.2.840.113556.1.4.358</span><span class="sxs-lookup"><span data-stu-id="c9f6d-118">1.2.840.113556.1.4.358</span></span>                      |
| <span data-ttu-id="c9f6d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c9f6d-119">System-Id-Guid</span></span>    | <span data-ttu-id="c9f6d-120">3e978920-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c9f6d-120">3e978920-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="c9f6d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9f6d-121">Syntax</span></span>            | [<span data-ttu-id="c9f6d-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c9f6d-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="c9f6d-123">Implementations</span></span>

-   [<span data-ttu-id="c9f6d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c9f6d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c9f6d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c9f6d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c9f6d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c9f6d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c9f6d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9f6d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c9f6d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-131">Entry</span></span> | <span data-ttu-id="c9f6d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c9f6d-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="c9f6d-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9f6d-135">System-Only</span></span>            | <span data-ttu-id="c9f6d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-136">False</span></span>                                     |
| <span data-ttu-id="c9f6d-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c9f6d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c9f6d-138">True</span><span class="sxs-lookup"><span data-stu-id="c9f6d-138">True</span></span>                                      |
| <span data-ttu-id="c9f6d-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="c9f6d-139">Is Indexed</span></span>             | <span data-ttu-id="c9f6d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-140">False</span></span>                                     |
| <span data-ttu-id="c9f6d-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c9f6d-141">In Global Catalog</span></span>      | <span data-ttu-id="c9f6d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-142">False</span></span>                                     |
| <span data-ttu-id="c9f6d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9f6d-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c9f6d-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c9f6d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9f6d-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9f6d-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-147">Search-Flags</span></span>           | <span data-ttu-id="c9f6d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9f6d-148">0x00000000</span></span>                                |
| <span data-ttu-id="c9f6d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-149">System-Flags</span></span>           | <span data-ttu-id="c9f6d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9f6d-150">0x00000010</span></span>                                |
| <span data-ttu-id="c9f6d-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c9f6d-151">Classes used in</span></span>        | [<span data-ttu-id="c9f6d-152">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c9f6d-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9f6d-153">Windows Server 2003</span></span>



| <span data-ttu-id="c9f6d-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-154">Entry</span></span> | <span data-ttu-id="c9f6d-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c9f6d-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="c9f6d-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9f6d-158">System-Only</span></span>            | <span data-ttu-id="c9f6d-159">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-159">False</span></span>                                     |
| <span data-ttu-id="c9f6d-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c9f6d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c9f6d-161">True</span><span class="sxs-lookup"><span data-stu-id="c9f6d-161">True</span></span>                                      |
| <span data-ttu-id="c9f6d-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="c9f6d-162">Is Indexed</span></span>             | <span data-ttu-id="c9f6d-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-163">False</span></span>                                     |
| <span data-ttu-id="c9f6d-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c9f6d-164">In Global Catalog</span></span>      | <span data-ttu-id="c9f6d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-165">False</span></span>                                     |
| <span data-ttu-id="c9f6d-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9f6d-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c9f6d-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c9f6d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9f6d-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9f6d-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-170">Search-Flags</span></span>           | <span data-ttu-id="c9f6d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9f6d-171">0x00000000</span></span>                                |
| <span data-ttu-id="c9f6d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-172">System-Flags</span></span>           | <span data-ttu-id="c9f6d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9f6d-173">0x00000010</span></span>                                |
| <span data-ttu-id="c9f6d-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c9f6d-174">Classes used in</span></span>        | [<span data-ttu-id="c9f6d-175">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c9f6d-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c9f6d-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c9f6d-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-177">Entry</span></span> | <span data-ttu-id="c9f6d-178">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c9f6d-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="c9f6d-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9f6d-181">System-Only</span></span>            | <span data-ttu-id="c9f6d-182">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-182">False</span></span>                                     |
| <span data-ttu-id="c9f6d-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c9f6d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c9f6d-184">True</span><span class="sxs-lookup"><span data-stu-id="c9f6d-184">True</span></span>                                      |
| <span data-ttu-id="c9f6d-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="c9f6d-185">Is Indexed</span></span>             | <span data-ttu-id="c9f6d-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-186">False</span></span>                                     |
| <span data-ttu-id="c9f6d-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c9f6d-187">In Global Catalog</span></span>      | <span data-ttu-id="c9f6d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-188">False</span></span>                                     |
| <span data-ttu-id="c9f6d-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9f6d-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c9f6d-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c9f6d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9f6d-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9f6d-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-193">Search-Flags</span></span>           | <span data-ttu-id="c9f6d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9f6d-194">0x00000000</span></span>                                |
| <span data-ttu-id="c9f6d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-195">System-Flags</span></span>           | <span data-ttu-id="c9f6d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9f6d-196">0x00000010</span></span>                                |
| <span data-ttu-id="c9f6d-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c9f6d-197">Classes used in</span></span>        | [<span data-ttu-id="c9f6d-198">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c9f6d-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9f6d-199">Windows Server 2008</span></span>



| <span data-ttu-id="c9f6d-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-200">Entry</span></span> | <span data-ttu-id="c9f6d-201">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c9f6d-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="c9f6d-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9f6d-204">System-Only</span></span>            | <span data-ttu-id="c9f6d-205">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-205">False</span></span>                                     |
| <span data-ttu-id="c9f6d-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c9f6d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c9f6d-207">True</span><span class="sxs-lookup"><span data-stu-id="c9f6d-207">True</span></span>                                      |
| <span data-ttu-id="c9f6d-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="c9f6d-208">Is Indexed</span></span>             | <span data-ttu-id="c9f6d-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-209">False</span></span>                                     |
| <span data-ttu-id="c9f6d-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c9f6d-210">In Global Catalog</span></span>      | <span data-ttu-id="c9f6d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-211">False</span></span>                                     |
| <span data-ttu-id="c9f6d-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9f6d-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c9f6d-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c9f6d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9f6d-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9f6d-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-216">Search-Flags</span></span>           | <span data-ttu-id="c9f6d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9f6d-217">0x00000000</span></span>                                |
| <span data-ttu-id="c9f6d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-218">System-Flags</span></span>           | <span data-ttu-id="c9f6d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9f6d-219">0x00000010</span></span>                                |
| <span data-ttu-id="c9f6d-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c9f6d-220">Classes used in</span></span>        | [<span data-ttu-id="c9f6d-221">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c9f6d-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9f6d-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c9f6d-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-223">Entry</span></span> | <span data-ttu-id="c9f6d-224">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c9f6d-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="c9f6d-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9f6d-227">System-Only</span></span>            | <span data-ttu-id="c9f6d-228">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-228">False</span></span>                                     |
| <span data-ttu-id="c9f6d-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c9f6d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c9f6d-230">True</span><span class="sxs-lookup"><span data-stu-id="c9f6d-230">True</span></span>                                      |
| <span data-ttu-id="c9f6d-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="c9f6d-231">Is Indexed</span></span>             | <span data-ttu-id="c9f6d-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-232">False</span></span>                                     |
| <span data-ttu-id="c9f6d-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c9f6d-233">In Global Catalog</span></span>      | <span data-ttu-id="c9f6d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-234">False</span></span>                                     |
| <span data-ttu-id="c9f6d-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9f6d-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c9f6d-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c9f6d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9f6d-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9f6d-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-239">Search-Flags</span></span>           | <span data-ttu-id="c9f6d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9f6d-240">0x00000000</span></span>                                |
| <span data-ttu-id="c9f6d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-241">System-Flags</span></span>           | <span data-ttu-id="c9f6d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9f6d-242">0x00000010</span></span>                                |
| <span data-ttu-id="c9f6d-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c9f6d-243">Classes used in</span></span>        | [<span data-ttu-id="c9f6d-244">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c9f6d-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9f6d-245">Windows Server 2012</span></span>



| <span data-ttu-id="c9f6d-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9f6d-246">Entry</span></span> | <span data-ttu-id="c9f6d-247">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="c9f6d-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="c9f6d-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9f6d-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="c9f6d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9f6d-250">System-Only</span></span>            | <span data-ttu-id="c9f6d-251">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-251">False</span></span>                                     |
| <span data-ttu-id="c9f6d-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c9f6d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c9f6d-253">True</span><span class="sxs-lookup"><span data-stu-id="c9f6d-253">True</span></span>                                      |
| <span data-ttu-id="c9f6d-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="c9f6d-254">Is Indexed</span></span>             | <span data-ttu-id="c9f6d-255">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-255">False</span></span>                                     |
| <span data-ttu-id="c9f6d-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c9f6d-256">In Global Catalog</span></span>      | <span data-ttu-id="c9f6d-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c9f6d-257">False</span></span>                                     |
| <span data-ttu-id="c9f6d-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9f6d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9f6d-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c9f6d-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="c9f6d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9f6d-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9f6d-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="c9f6d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-262">Search-Flags</span></span>           | <span data-ttu-id="c9f6d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c9f6d-263">0x00000000</span></span>                                |
| <span data-ttu-id="c9f6d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9f6d-264">System-Flags</span></span>           | <span data-ttu-id="c9f6d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9f6d-265">0x00000010</span></span>                                |
| <span data-ttu-id="c9f6d-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c9f6d-266">Classes used in</span></span>        | [<span data-ttu-id="c9f6d-267">**Computador**</span><span class="sxs-lookup"><span data-stu-id="c9f6d-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





