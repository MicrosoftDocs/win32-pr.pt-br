---
title: Atributo Transport-DLL-Name
description: O nome da DLL que gerenciará um transporte.
ms.assetid: a6b078ec-8738-4c57-9d94-05a96dbc645b
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de Transport-DLL-Name
- Esquema de AD do atributo transportDLLName
topic_type:
- apiref
api_name:
- Transport-DLL-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c118a2f7553c86de4b3c36b2904a3b7d75518a2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754872"
---
# <a name="transport-dll-name-attribute"></a><span data-ttu-id="4e798-105">Atributo Transport-DLL-Name</span><span class="sxs-lookup"><span data-stu-id="4e798-105">Transport-DLL-Name attribute</span></span>

<span data-ttu-id="4e798-106">O nome da DLL que gerenciará um transporte.</span><span class="sxs-lookup"><span data-stu-id="4e798-106">The name of the DLL that will manage a transport.</span></span>



| <span data-ttu-id="4e798-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-107">Entry</span></span> | <span data-ttu-id="4e798-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4e798-109">CN</span><span class="sxs-lookup"><span data-stu-id="4e798-109">CN</span></span>                | <span data-ttu-id="4e798-110">Transport-DLL-Name</span><span class="sxs-lookup"><span data-stu-id="4e798-110">Transport-DLL-Name</span></span>                          |
| <span data-ttu-id="4e798-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4e798-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4e798-112">transportDLLName</span><span class="sxs-lookup"><span data-stu-id="4e798-112">transportDLLName</span></span>                            |
| <span data-ttu-id="4e798-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4e798-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="4e798-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4e798-114">Update Privilege</span></span>  | <span data-ttu-id="4e798-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4e798-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="4e798-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4e798-116">Update Frequency</span></span>  | <span data-ttu-id="4e798-117">Ao conectar sites.</span><span class="sxs-lookup"><span data-stu-id="4e798-117">When connecting sites.</span></span>                      |
| <span data-ttu-id="4e798-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-118">Attribute-Id</span></span>      | <span data-ttu-id="4e798-119">1.2.840.113556.1.4.789</span><span class="sxs-lookup"><span data-stu-id="4e798-119">1.2.840.113556.1.4.789</span></span>                      |
| <span data-ttu-id="4e798-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4e798-120">System-Id-Guid</span></span>    | <span data-ttu-id="4e798-121">26d97372-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4e798-121">26d97372-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="4e798-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e798-122">Syntax</span></span>            | [<span data-ttu-id="4e798-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4e798-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4e798-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="4e798-124">Implementations</span></span>

-   [<span data-ttu-id="4e798-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4e798-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4e798-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4e798-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4e798-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4e798-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4e798-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4e798-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4e798-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4e798-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4e798-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4e798-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4e798-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4e798-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4e798-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4e798-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4e798-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-133">Entry</span></span> | <span data-ttu-id="4e798-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-137">System-Only</span></span>            | <span data-ttu-id="4e798-138">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-138">False</span></span>                                                           |
| <span data-ttu-id="4e798-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-140">True</span><span class="sxs-lookup"><span data-stu-id="4e798-140">True</span></span>                                                            |
| <span data-ttu-id="4e798-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-141">Is Indexed</span></span>             | <span data-ttu-id="4e798-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-142">False</span></span>                                                           |
| <span data-ttu-id="4e798-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-143">In Global Catalog</span></span>      | <span data-ttu-id="4e798-144">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-144">False</span></span>                                                           |
| <span data-ttu-id="4e798-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-147">Range-Lower</span></span>            | <span data-ttu-id="4e798-148">0</span><span class="sxs-lookup"><span data-stu-id="4e798-148">0</span></span>                                                               |
| <span data-ttu-id="4e798-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-149">Range-Upper</span></span>            | <span data-ttu-id="4e798-150">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-150">1024</span></span>                                                            |
| <span data-ttu-id="4e798-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-151">Search-Flags</span></span>           | <span data-ttu-id="4e798-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-153">System-Flags</span></span>           | <span data-ttu-id="4e798-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-155">Classes used in</span></span>        | [<span data-ttu-id="4e798-156">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4e798-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e798-157">Windows Server 2003</span></span>



| <span data-ttu-id="4e798-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-158">Entry</span></span> | <span data-ttu-id="4e798-159">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-162">System-Only</span></span>            | <span data-ttu-id="4e798-163">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-163">False</span></span>                                                           |
| <span data-ttu-id="4e798-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-165">True</span><span class="sxs-lookup"><span data-stu-id="4e798-165">True</span></span>                                                            |
| <span data-ttu-id="4e798-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-166">Is Indexed</span></span>             | <span data-ttu-id="4e798-167">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-167">False</span></span>                                                           |
| <span data-ttu-id="4e798-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-168">In Global Catalog</span></span>      | <span data-ttu-id="4e798-169">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-169">False</span></span>                                                           |
| <span data-ttu-id="4e798-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-172">Range-Lower</span></span>            | <span data-ttu-id="4e798-173">0</span><span class="sxs-lookup"><span data-stu-id="4e798-173">0</span></span>                                                               |
| <span data-ttu-id="4e798-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-174">Range-Upper</span></span>            | <span data-ttu-id="4e798-175">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-175">1024</span></span>                                                            |
| <span data-ttu-id="4e798-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-176">Search-Flags</span></span>           | <span data-ttu-id="4e798-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-178">System-Flags</span></span>           | <span data-ttu-id="4e798-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-180">Classes used in</span></span>        | [<span data-ttu-id="4e798-181">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-181">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4e798-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="4e798-182">ADAM</span></span>



| <span data-ttu-id="4e798-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-183">Entry</span></span> | <span data-ttu-id="4e798-184">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-187">System-Only</span></span>            | <span data-ttu-id="4e798-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-188">False</span></span>                                                           |
| <span data-ttu-id="4e798-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-190">True</span><span class="sxs-lookup"><span data-stu-id="4e798-190">True</span></span>                                                            |
| <span data-ttu-id="4e798-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-191">Is Indexed</span></span>             | <span data-ttu-id="4e798-192">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-192">False</span></span>                                                           |
| <span data-ttu-id="4e798-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-193">In Global Catalog</span></span>      | <span data-ttu-id="4e798-194">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-194">False</span></span>                                                           |
| <span data-ttu-id="4e798-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-197">Range-Lower</span></span>            | <span data-ttu-id="4e798-198">0</span><span class="sxs-lookup"><span data-stu-id="4e798-198">0</span></span>                                                               |
| <span data-ttu-id="4e798-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-199">Range-Upper</span></span>            | <span data-ttu-id="4e798-200">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-200">1024</span></span>                                                            |
| <span data-ttu-id="4e798-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-201">Search-Flags</span></span>           | <span data-ttu-id="4e798-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-203">System-Flags</span></span>           | <span data-ttu-id="4e798-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-205">Classes used in</span></span>        | [<span data-ttu-id="4e798-206">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-206">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4e798-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4e798-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4e798-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-208">Entry</span></span> | <span data-ttu-id="4e798-209">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-212">System-Only</span></span>            | <span data-ttu-id="4e798-213">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-213">False</span></span>                                                           |
| <span data-ttu-id="4e798-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-214">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-215">True</span><span class="sxs-lookup"><span data-stu-id="4e798-215">True</span></span>                                                            |
| <span data-ttu-id="4e798-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-216">Is Indexed</span></span>             | <span data-ttu-id="4e798-217">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-217">False</span></span>                                                           |
| <span data-ttu-id="4e798-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-218">In Global Catalog</span></span>      | <span data-ttu-id="4e798-219">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-219">False</span></span>                                                           |
| <span data-ttu-id="4e798-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-222">Range-Lower</span></span>            | <span data-ttu-id="4e798-223">0</span><span class="sxs-lookup"><span data-stu-id="4e798-223">0</span></span>                                                               |
| <span data-ttu-id="4e798-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-224">Range-Upper</span></span>            | <span data-ttu-id="4e798-225">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-225">1024</span></span>                                                            |
| <span data-ttu-id="4e798-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-226">Search-Flags</span></span>           | <span data-ttu-id="4e798-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-228">System-Flags</span></span>           | <span data-ttu-id="4e798-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-230">Classes used in</span></span>        | [<span data-ttu-id="4e798-231">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-231">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4e798-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e798-232">Windows Server 2008</span></span>



| <span data-ttu-id="4e798-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-233">Entry</span></span> | <span data-ttu-id="4e798-234">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-237">System-Only</span></span>            | <span data-ttu-id="4e798-238">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-238">False</span></span>                                                           |
| <span data-ttu-id="4e798-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-239">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-240">True</span><span class="sxs-lookup"><span data-stu-id="4e798-240">True</span></span>                                                            |
| <span data-ttu-id="4e798-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-241">Is Indexed</span></span>             | <span data-ttu-id="4e798-242">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-242">False</span></span>                                                           |
| <span data-ttu-id="4e798-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-243">In Global Catalog</span></span>      | <span data-ttu-id="4e798-244">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-244">False</span></span>                                                           |
| <span data-ttu-id="4e798-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-247">Range-Lower</span></span>            | <span data-ttu-id="4e798-248">0</span><span class="sxs-lookup"><span data-stu-id="4e798-248">0</span></span>                                                               |
| <span data-ttu-id="4e798-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-249">Range-Upper</span></span>            | <span data-ttu-id="4e798-250">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-250">1024</span></span>                                                            |
| <span data-ttu-id="4e798-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-251">Search-Flags</span></span>           | <span data-ttu-id="4e798-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-253">System-Flags</span></span>           | <span data-ttu-id="4e798-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-255">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-255">Classes used in</span></span>        | [<span data-ttu-id="4e798-256">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-256">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4e798-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4e798-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4e798-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-258">Entry</span></span> | <span data-ttu-id="4e798-259">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-260">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-262">System-Only</span></span>            | <span data-ttu-id="4e798-263">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-263">False</span></span>                                                           |
| <span data-ttu-id="4e798-264">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-264">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-265">True</span><span class="sxs-lookup"><span data-stu-id="4e798-265">True</span></span>                                                            |
| <span data-ttu-id="4e798-266">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-266">Is Indexed</span></span>             | <span data-ttu-id="4e798-267">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-267">False</span></span>                                                           |
| <span data-ttu-id="4e798-268">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-268">In Global Catalog</span></span>      | <span data-ttu-id="4e798-269">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-269">False</span></span>                                                           |
| <span data-ttu-id="4e798-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-271">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-272">Range-Lower</span></span>            | <span data-ttu-id="4e798-273">0</span><span class="sxs-lookup"><span data-stu-id="4e798-273">0</span></span>                                                               |
| <span data-ttu-id="4e798-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-274">Range-Upper</span></span>            | <span data-ttu-id="4e798-275">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-275">1024</span></span>                                                            |
| <span data-ttu-id="4e798-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-276">Search-Flags</span></span>           | <span data-ttu-id="4e798-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-278">System-Flags</span></span>           | <span data-ttu-id="4e798-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-280">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-280">Classes used in</span></span>        | [<span data-ttu-id="4e798-281">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-281">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4e798-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4e798-282">Windows Server 2012</span></span>



| <span data-ttu-id="4e798-283">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e798-283">Entry</span></span> | <span data-ttu-id="4e798-284">Valor</span><span class="sxs-lookup"><span data-stu-id="4e798-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4e798-285">ID do link</span><span class="sxs-lookup"><span data-stu-id="4e798-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e798-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="4e798-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e798-287">System-Only</span></span>            | <span data-ttu-id="4e798-288">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-288">False</span></span>                                                           |
| <span data-ttu-id="4e798-289">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4e798-289">Is-Single-Valued</span></span>       | <span data-ttu-id="4e798-290">True</span><span class="sxs-lookup"><span data-stu-id="4e798-290">True</span></span>                                                            |
| <span data-ttu-id="4e798-291">É indexado</span><span class="sxs-lookup"><span data-stu-id="4e798-291">Is Indexed</span></span>             | <span data-ttu-id="4e798-292">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-292">False</span></span>                                                           |
| <span data-ttu-id="4e798-293">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4e798-293">In Global Catalog</span></span>      | <span data-ttu-id="4e798-294">Falso</span><span class="sxs-lookup"><span data-stu-id="4e798-294">False</span></span>                                                           |
| <span data-ttu-id="4e798-295">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4e798-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e798-296">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4e798-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="4e798-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e798-297">Range-Lower</span></span>            | <span data-ttu-id="4e798-298">0</span><span class="sxs-lookup"><span data-stu-id="4e798-298">0</span></span>                                                               |
| <span data-ttu-id="4e798-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e798-299">Range-Upper</span></span>            | <span data-ttu-id="4e798-300">1024</span><span class="sxs-lookup"><span data-stu-id="4e798-300">1024</span></span>                                                            |
| <span data-ttu-id="4e798-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-301">Search-Flags</span></span>           | <span data-ttu-id="4e798-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e798-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="4e798-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e798-303">System-Flags</span></span>           | <span data-ttu-id="4e798-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e798-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="4e798-305">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4e798-305">Classes used in</span></span>        | [<span data-ttu-id="4e798-306">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="4e798-306">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



 

 





