---
title: Rights-Guid atributo
description: O GUID usado para representar um direito estendido dentro de uma entrada de controle de acesso.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Esquema de Rights-Guid do atributo AD
- Esquema de AD do atributo rightsGuid
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086996"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="bdde5-105">Rights-Guid atributo</span><span class="sxs-lookup"><span data-stu-id="bdde5-105">Rights-Guid attribute</span></span>

<span data-ttu-id="bdde5-106">O GUID usado para representar um direito estendido dentro de uma entrada de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="bdde5-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="bdde5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-107">Entry</span></span> | <span data-ttu-id="bdde5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bdde5-109">CN</span><span class="sxs-lookup"><span data-stu-id="bdde5-109">CN</span></span>                | <span data-ttu-id="bdde5-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="bdde5-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="bdde5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bdde5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bdde5-112">rightsGuid</span><span class="sxs-lookup"><span data-stu-id="bdde5-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="bdde5-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bdde5-113">Size</span></span>              | <span data-ttu-id="bdde5-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="bdde5-114">16 bytes</span></span>                                    |
| <span data-ttu-id="bdde5-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bdde5-115">Update Privilege</span></span>  | <span data-ttu-id="bdde5-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="bdde5-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="bdde5-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bdde5-117">Update Frequency</span></span>  | <span data-ttu-id="bdde5-118">Quando um novo direito estendido é criado.</span><span class="sxs-lookup"><span data-stu-id="bdde5-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="bdde5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-119">Attribute-Id</span></span>      | <span data-ttu-id="bdde5-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="bdde5-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="bdde5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bdde5-121">System-Id-Guid</span></span>    | <span data-ttu-id="bdde5-122">8297931c-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bdde5-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="bdde5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdde5-123">Syntax</span></span>            | [<span data-ttu-id="bdde5-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bdde5-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bdde5-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="bdde5-125">Implementations</span></span>

-   [<span data-ttu-id="bdde5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bdde5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bdde5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bdde5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bdde5-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bdde5-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bdde5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bdde5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bdde5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bdde5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bdde5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bdde5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bdde5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bdde5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bdde5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bdde5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="bdde5-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-134">Entry</span></span> | <span data-ttu-id="bdde5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-138">System-Only</span></span>            | <span data-ttu-id="bdde5-139">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-139">False</span></span>                                                           |
| <span data-ttu-id="bdde5-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-141">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-141">True</span></span>                                                            |
| <span data-ttu-id="bdde5-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-142">Is Indexed</span></span>             | <span data-ttu-id="bdde5-143">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-143">False</span></span>                                                           |
| <span data-ttu-id="bdde5-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-144">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-145">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-145">False</span></span>                                                           |
| <span data-ttu-id="bdde5-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-148">Range-Lower</span></span>            | <span data-ttu-id="bdde5-149">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-149">36</span></span>                                                              |
| <span data-ttu-id="bdde5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-150">Range-Upper</span></span>            | <span data-ttu-id="bdde5-151">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-151">36</span></span>                                                              |
| <span data-ttu-id="bdde5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-152">Search-Flags</span></span>           | <span data-ttu-id="bdde5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-154">System-Flags</span></span>           | <span data-ttu-id="bdde5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-156">Classes used in</span></span>        | [<span data-ttu-id="bdde5-157">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bdde5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdde5-158">Windows Server 2003</span></span>



| <span data-ttu-id="bdde5-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-159">Entry</span></span> | <span data-ttu-id="bdde5-160">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-163">System-Only</span></span>            | <span data-ttu-id="bdde5-164">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-164">False</span></span>                                                           |
| <span data-ttu-id="bdde5-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-166">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-166">True</span></span>                                                            |
| <span data-ttu-id="bdde5-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-167">Is Indexed</span></span>             | <span data-ttu-id="bdde5-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-168">False</span></span>                                                           |
| <span data-ttu-id="bdde5-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-169">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-170">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-170">False</span></span>                                                           |
| <span data-ttu-id="bdde5-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-173">Range-Lower</span></span>            | <span data-ttu-id="bdde5-174">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-174">36</span></span>                                                              |
| <span data-ttu-id="bdde5-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-175">Range-Upper</span></span>            | <span data-ttu-id="bdde5-176">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-176">36</span></span>                                                              |
| <span data-ttu-id="bdde5-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-177">Search-Flags</span></span>           | <span data-ttu-id="bdde5-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-179">System-Flags</span></span>           | <span data-ttu-id="bdde5-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-181">Classes used in</span></span>        | [<span data-ttu-id="bdde5-182">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bdde5-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="bdde5-183">ADAM</span></span>



| <span data-ttu-id="bdde5-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-184">Entry</span></span> | <span data-ttu-id="bdde5-185">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-188">System-Only</span></span>            | <span data-ttu-id="bdde5-189">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-189">False</span></span>                                                           |
| <span data-ttu-id="bdde5-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-190">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-191">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-191">True</span></span>                                                            |
| <span data-ttu-id="bdde5-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-192">Is Indexed</span></span>             | <span data-ttu-id="bdde5-193">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-193">False</span></span>                                                           |
| <span data-ttu-id="bdde5-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-194">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-195">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-195">False</span></span>                                                           |
| <span data-ttu-id="bdde5-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-198">Range-Lower</span></span>            | <span data-ttu-id="bdde5-199">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-199">36</span></span>                                                              |
| <span data-ttu-id="bdde5-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-200">Range-Upper</span></span>            | <span data-ttu-id="bdde5-201">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-201">36</span></span>                                                              |
| <span data-ttu-id="bdde5-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-202">Search-Flags</span></span>           | <span data-ttu-id="bdde5-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-204">System-Flags</span></span>           | <span data-ttu-id="bdde5-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-206">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-206">Classes used in</span></span>        | [<span data-ttu-id="bdde5-207">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bdde5-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bdde5-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bdde5-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-209">Entry</span></span> | <span data-ttu-id="bdde5-210">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-211">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-213">System-Only</span></span>            | <span data-ttu-id="bdde5-214">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-214">False</span></span>                                                           |
| <span data-ttu-id="bdde5-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-215">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-216">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-216">True</span></span>                                                            |
| <span data-ttu-id="bdde5-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-217">Is Indexed</span></span>             | <span data-ttu-id="bdde5-218">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-218">False</span></span>                                                           |
| <span data-ttu-id="bdde5-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-219">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-220">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-220">False</span></span>                                                           |
| <span data-ttu-id="bdde5-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-223">Range-Lower</span></span>            | <span data-ttu-id="bdde5-224">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-224">36</span></span>                                                              |
| <span data-ttu-id="bdde5-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-225">Range-Upper</span></span>            | <span data-ttu-id="bdde5-226">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-226">36</span></span>                                                              |
| <span data-ttu-id="bdde5-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-227">Search-Flags</span></span>           | <span data-ttu-id="bdde5-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-229">System-Flags</span></span>           | <span data-ttu-id="bdde5-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-231">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-231">Classes used in</span></span>        | [<span data-ttu-id="bdde5-232">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bdde5-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdde5-233">Windows Server 2008</span></span>



| <span data-ttu-id="bdde5-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-234">Entry</span></span> | <span data-ttu-id="bdde5-235">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-236">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-238">System-Only</span></span>            | <span data-ttu-id="bdde5-239">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-239">False</span></span>                                                           |
| <span data-ttu-id="bdde5-240">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-240">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-241">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-241">True</span></span>                                                            |
| <span data-ttu-id="bdde5-242">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-242">Is Indexed</span></span>             | <span data-ttu-id="bdde5-243">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-243">False</span></span>                                                           |
| <span data-ttu-id="bdde5-244">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-244">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-245">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-245">False</span></span>                                                           |
| <span data-ttu-id="bdde5-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-247">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-248">Range-Lower</span></span>            | <span data-ttu-id="bdde5-249">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-249">36</span></span>                                                              |
| <span data-ttu-id="bdde5-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-250">Range-Upper</span></span>            | <span data-ttu-id="bdde5-251">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-251">36</span></span>                                                              |
| <span data-ttu-id="bdde5-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-252">Search-Flags</span></span>           | <span data-ttu-id="bdde5-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-254">System-Flags</span></span>           | <span data-ttu-id="bdde5-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-256">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-256">Classes used in</span></span>        | [<span data-ttu-id="bdde5-257">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bdde5-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdde5-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bdde5-259">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-259">Entry</span></span> | <span data-ttu-id="bdde5-260">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-261">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-263">System-Only</span></span>            | <span data-ttu-id="bdde5-264">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-264">False</span></span>                                                           |
| <span data-ttu-id="bdde5-265">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-265">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-266">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-266">True</span></span>                                                            |
| <span data-ttu-id="bdde5-267">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-267">Is Indexed</span></span>             | <span data-ttu-id="bdde5-268">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-268">False</span></span>                                                           |
| <span data-ttu-id="bdde5-269">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-269">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-270">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-270">False</span></span>                                                           |
| <span data-ttu-id="bdde5-271">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-272">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-273">Range-Lower</span></span>            | <span data-ttu-id="bdde5-274">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-274">36</span></span>                                                              |
| <span data-ttu-id="bdde5-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-275">Range-Upper</span></span>            | <span data-ttu-id="bdde5-276">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-276">36</span></span>                                                              |
| <span data-ttu-id="bdde5-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-277">Search-Flags</span></span>           | <span data-ttu-id="bdde5-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-279">System-Flags</span></span>           | <span data-ttu-id="bdde5-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-281">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-281">Classes used in</span></span>        | [<span data-ttu-id="bdde5-282">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bdde5-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bdde5-283">Windows Server 2012</span></span>



| <span data-ttu-id="bdde5-284">Entrada</span><span class="sxs-lookup"><span data-stu-id="bdde5-284">Entry</span></span> | <span data-ttu-id="bdde5-285">Valor</span><span class="sxs-lookup"><span data-stu-id="bdde5-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="bdde5-286">ID do link</span><span class="sxs-lookup"><span data-stu-id="bdde5-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdde5-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="bdde5-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdde5-288">System-Only</span></span>            | <span data-ttu-id="bdde5-289">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-289">False</span></span>                                                           |
| <span data-ttu-id="bdde5-290">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bdde5-290">Is-Single-Valued</span></span>       | <span data-ttu-id="bdde5-291">True</span><span class="sxs-lookup"><span data-stu-id="bdde5-291">True</span></span>                                                            |
| <span data-ttu-id="bdde5-292">É indexado</span><span class="sxs-lookup"><span data-stu-id="bdde5-292">Is Indexed</span></span>             | <span data-ttu-id="bdde5-293">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-293">False</span></span>                                                           |
| <span data-ttu-id="bdde5-294">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bdde5-294">In Global Catalog</span></span>      | <span data-ttu-id="bdde5-295">Falso</span><span class="sxs-lookup"><span data-stu-id="bdde5-295">False</span></span>                                                           |
| <span data-ttu-id="bdde5-296">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bdde5-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdde5-297">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bdde5-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="bdde5-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdde5-298">Range-Lower</span></span>            | <span data-ttu-id="bdde5-299">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-299">36</span></span>                                                              |
| <span data-ttu-id="bdde5-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdde5-300">Range-Upper</span></span>            | <span data-ttu-id="bdde5-301">36</span><span class="sxs-lookup"><span data-stu-id="bdde5-301">36</span></span>                                                              |
| <span data-ttu-id="bdde5-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-302">Search-Flags</span></span>           | <span data-ttu-id="bdde5-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdde5-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="bdde5-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdde5-304">System-Flags</span></span>           | <span data-ttu-id="bdde5-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdde5-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="bdde5-306">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bdde5-306">Classes used in</span></span>        | [<span data-ttu-id="bdde5-307">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="bdde5-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





