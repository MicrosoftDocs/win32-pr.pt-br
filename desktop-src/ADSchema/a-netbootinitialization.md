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
# <a name="netboot-initialization-attribute"></a><span data-ttu-id="5c4e1-105">Netboot-Initialization atributo</span><span class="sxs-lookup"><span data-stu-id="5c4e1-105">Netboot-Initialization attribute</span></span>

<span data-ttu-id="5c4e1-106">Caminho de inicialização padrão para inicialização em disco.</span><span class="sxs-lookup"><span data-stu-id="5c4e1-106">Default boot path for diskless boot.</span></span>



| <span data-ttu-id="5c4e1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-107">Entry</span></span> | <span data-ttu-id="5c4e1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5c4e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="5c4e1-109">CN</span></span>                | <span data-ttu-id="5c4e1-110">Netboot-Initialization</span><span class="sxs-lookup"><span data-stu-id="5c4e1-110">Netboot-Initialization</span></span>                      |
| <span data-ttu-id="5c4e1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5c4e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5c4e1-112">netbootInitialization</span><span class="sxs-lookup"><span data-stu-id="5c4e1-112">netbootInitialization</span></span>                       |
| <span data-ttu-id="5c4e1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5c4e1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5c4e1-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5c4e1-114">Update Privilege</span></span>  | <span data-ttu-id="5c4e1-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5c4e1-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="5c4e1-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5c4e1-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5c4e1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-117">Attribute-Id</span></span>      | <span data-ttu-id="5c4e1-118">1.2.840.113556.1.4.358</span><span class="sxs-lookup"><span data-stu-id="5c4e1-118">1.2.840.113556.1.4.358</span></span>                      |
| <span data-ttu-id="5c4e1-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5c4e1-119">System-Id-Guid</span></span>    | <span data-ttu-id="5c4e1-120">3e978920-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="5c4e1-120">3e978920-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="5c4e1-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c4e1-121">Syntax</span></span>            | [<span data-ttu-id="5c4e1-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5c4e1-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="5c4e1-123">Implementations</span></span>

-   [<span data-ttu-id="5c4e1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c4e1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c4e1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c4e1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c4e1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c4e1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c4e1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c4e1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="5c4e1-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-131">Entry</span></span> | <span data-ttu-id="5c4e1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4e1-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c4e1-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4e1-135">System-Only</span></span>            | <span data-ttu-id="5c4e1-136">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-136">False</span></span>                                     |
| <span data-ttu-id="5c4e1-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c4e1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4e1-138">True</span><span class="sxs-lookup"><span data-stu-id="5c4e1-138">True</span></span>                                      |
| <span data-ttu-id="5c4e1-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c4e1-139">Is Indexed</span></span>             | <span data-ttu-id="5c4e1-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-140">False</span></span>                                     |
| <span data-ttu-id="5c4e1-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c4e1-141">In Global Catalog</span></span>      | <span data-ttu-id="5c4e1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-142">False</span></span>                                     |
| <span data-ttu-id="5c4e1-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4e1-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c4e1-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4e1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4e1-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4e1-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-147">Search-Flags</span></span>           | <span data-ttu-id="5c4e1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4e1-148">0x00000000</span></span>                                |
| <span data-ttu-id="5c4e1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-149">System-Flags</span></span>           | <span data-ttu-id="5c4e1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4e1-150">0x00000010</span></span>                                |
| <span data-ttu-id="5c4e1-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c4e1-151">Classes used in</span></span>        | [<span data-ttu-id="5c4e1-152">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c4e1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c4e1-153">Windows Server 2003</span></span>



| <span data-ttu-id="5c4e1-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-154">Entry</span></span> | <span data-ttu-id="5c4e1-155">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4e1-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c4e1-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4e1-158">System-Only</span></span>            | <span data-ttu-id="5c4e1-159">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-159">False</span></span>                                     |
| <span data-ttu-id="5c4e1-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c4e1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4e1-161">True</span><span class="sxs-lookup"><span data-stu-id="5c4e1-161">True</span></span>                                      |
| <span data-ttu-id="5c4e1-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c4e1-162">Is Indexed</span></span>             | <span data-ttu-id="5c4e1-163">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-163">False</span></span>                                     |
| <span data-ttu-id="5c4e1-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c4e1-164">In Global Catalog</span></span>      | <span data-ttu-id="5c4e1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-165">False</span></span>                                     |
| <span data-ttu-id="5c4e1-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4e1-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c4e1-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4e1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4e1-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4e1-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-170">Search-Flags</span></span>           | <span data-ttu-id="5c4e1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4e1-171">0x00000000</span></span>                                |
| <span data-ttu-id="5c4e1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-172">System-Flags</span></span>           | <span data-ttu-id="5c4e1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4e1-173">0x00000010</span></span>                                |
| <span data-ttu-id="5c4e1-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c4e1-174">Classes used in</span></span>        | [<span data-ttu-id="5c4e1-175">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c4e1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c4e1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c4e1-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-177">Entry</span></span> | <span data-ttu-id="5c4e1-178">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4e1-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c4e1-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4e1-181">System-Only</span></span>            | <span data-ttu-id="5c4e1-182">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-182">False</span></span>                                     |
| <span data-ttu-id="5c4e1-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c4e1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4e1-184">True</span><span class="sxs-lookup"><span data-stu-id="5c4e1-184">True</span></span>                                      |
| <span data-ttu-id="5c4e1-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c4e1-185">Is Indexed</span></span>             | <span data-ttu-id="5c4e1-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-186">False</span></span>                                     |
| <span data-ttu-id="5c4e1-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c4e1-187">In Global Catalog</span></span>      | <span data-ttu-id="5c4e1-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-188">False</span></span>                                     |
| <span data-ttu-id="5c4e1-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4e1-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c4e1-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4e1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4e1-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4e1-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-193">Search-Flags</span></span>           | <span data-ttu-id="5c4e1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4e1-194">0x00000000</span></span>                                |
| <span data-ttu-id="5c4e1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-195">System-Flags</span></span>           | <span data-ttu-id="5c4e1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4e1-196">0x00000010</span></span>                                |
| <span data-ttu-id="5c4e1-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c4e1-197">Classes used in</span></span>        | [<span data-ttu-id="5c4e1-198">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c4e1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c4e1-199">Windows Server 2008</span></span>



| <span data-ttu-id="5c4e1-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-200">Entry</span></span> | <span data-ttu-id="5c4e1-201">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4e1-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c4e1-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4e1-204">System-Only</span></span>            | <span data-ttu-id="5c4e1-205">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-205">False</span></span>                                     |
| <span data-ttu-id="5c4e1-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c4e1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4e1-207">True</span><span class="sxs-lookup"><span data-stu-id="5c4e1-207">True</span></span>                                      |
| <span data-ttu-id="5c4e1-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c4e1-208">Is Indexed</span></span>             | <span data-ttu-id="5c4e1-209">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-209">False</span></span>                                     |
| <span data-ttu-id="5c4e1-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c4e1-210">In Global Catalog</span></span>      | <span data-ttu-id="5c4e1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-211">False</span></span>                                     |
| <span data-ttu-id="5c4e1-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4e1-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c4e1-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4e1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4e1-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4e1-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-216">Search-Flags</span></span>           | <span data-ttu-id="5c4e1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4e1-217">0x00000000</span></span>                                |
| <span data-ttu-id="5c4e1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-218">System-Flags</span></span>           | <span data-ttu-id="5c4e1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4e1-219">0x00000010</span></span>                                |
| <span data-ttu-id="5c4e1-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c4e1-220">Classes used in</span></span>        | [<span data-ttu-id="5c4e1-221">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c4e1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c4e1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c4e1-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-223">Entry</span></span> | <span data-ttu-id="5c4e1-224">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4e1-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c4e1-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4e1-227">System-Only</span></span>            | <span data-ttu-id="5c4e1-228">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-228">False</span></span>                                     |
| <span data-ttu-id="5c4e1-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c4e1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4e1-230">True</span><span class="sxs-lookup"><span data-stu-id="5c4e1-230">True</span></span>                                      |
| <span data-ttu-id="5c4e1-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c4e1-231">Is Indexed</span></span>             | <span data-ttu-id="5c4e1-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-232">False</span></span>                                     |
| <span data-ttu-id="5c4e1-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c4e1-233">In Global Catalog</span></span>      | <span data-ttu-id="5c4e1-234">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-234">False</span></span>                                     |
| <span data-ttu-id="5c4e1-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4e1-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c4e1-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4e1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4e1-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4e1-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-239">Search-Flags</span></span>           | <span data-ttu-id="5c4e1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4e1-240">0x00000000</span></span>                                |
| <span data-ttu-id="5c4e1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-241">System-Flags</span></span>           | <span data-ttu-id="5c4e1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4e1-242">0x00000010</span></span>                                |
| <span data-ttu-id="5c4e1-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c4e1-243">Classes used in</span></span>        | [<span data-ttu-id="5c4e1-244">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c4e1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c4e1-245">Windows Server 2012</span></span>



| <span data-ttu-id="5c4e1-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c4e1-246">Entry</span></span> | <span data-ttu-id="5c4e1-247">Valor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5c4e1-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c4e1-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c4e1-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5c4e1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c4e1-250">System-Only</span></span>            | <span data-ttu-id="5c4e1-251">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-251">False</span></span>                                     |
| <span data-ttu-id="5c4e1-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c4e1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="5c4e1-253">True</span><span class="sxs-lookup"><span data-stu-id="5c4e1-253">True</span></span>                                      |
| <span data-ttu-id="5c4e1-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c4e1-254">Is Indexed</span></span>             | <span data-ttu-id="5c4e1-255">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-255">False</span></span>                                     |
| <span data-ttu-id="5c4e1-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c4e1-256">In Global Catalog</span></span>      | <span data-ttu-id="5c4e1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="5c4e1-257">False</span></span>                                     |
| <span data-ttu-id="5c4e1-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c4e1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c4e1-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c4e1-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5c4e1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c4e1-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c4e1-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5c4e1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-262">Search-Flags</span></span>           | <span data-ttu-id="5c4e1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c4e1-263">0x00000000</span></span>                                |
| <span data-ttu-id="5c4e1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c4e1-264">System-Flags</span></span>           | <span data-ttu-id="5c4e1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c4e1-265">0x00000010</span></span>                                |
| <span data-ttu-id="5c4e1-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c4e1-266">Classes used in</span></span>        | [<span data-ttu-id="5c4e1-267">**Computador**</span><span class="sxs-lookup"><span data-stu-id="5c4e1-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





