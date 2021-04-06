---
title: Atributo MS-DS-Creator-SID
description: A ID de segurança do criador do objeto que contém este atributo.
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-DS-Creator-SID
- Esquema de AD do atributo mS-DS-CreatorSID
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919351"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="e4bdb-105">Atributo MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="e4bdb-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="e4bdb-106">A ID de segurança do criador do objeto que contém este atributo.</span><span class="sxs-lookup"><span data-stu-id="e4bdb-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="e4bdb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-107">Entry</span></span> | <span data-ttu-id="e4bdb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e4bdb-109">CN</span><span class="sxs-lookup"><span data-stu-id="e4bdb-109">CN</span></span>                | <span data-ttu-id="e4bdb-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="e4bdb-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="e4bdb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e4bdb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e4bdb-112">mS-DS-CreatorSID</span><span class="sxs-lookup"><span data-stu-id="e4bdb-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="e4bdb-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e4bdb-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="e4bdb-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e4bdb-114">Update Privilege</span></span>  | <span data-ttu-id="e4bdb-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e4bdb-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="e4bdb-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e4bdb-116">Update Frequency</span></span>  | <span data-ttu-id="e4bdb-117">Sempre que um novo objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="e4bdb-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="e4bdb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-118">Attribute-Id</span></span>      | <span data-ttu-id="e4bdb-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="e4bdb-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="e4bdb-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e4bdb-120">System-Id-Guid</span></span>    | <span data-ttu-id="e4bdb-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e4bdb-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="e4bdb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4bdb-122">Syntax</span></span>            | [<span data-ttu-id="e4bdb-123">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="e4bdb-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="e4bdb-124">Implementations</span></span>

-   [<span data-ttu-id="e4bdb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e4bdb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e4bdb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e4bdb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e4bdb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e4bdb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e4bdb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4bdb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e4bdb-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-132">Entry</span></span> | <span data-ttu-id="e4bdb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e4bdb-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="e4bdb-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4bdb-136">System-Only</span></span>            | <span data-ttu-id="e4bdb-137">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-137">True</span></span>                              |
| <span data-ttu-id="e4bdb-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e4bdb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e4bdb-139">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-139">True</span></span>                              |
| <span data-ttu-id="e4bdb-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="e4bdb-140">Is Indexed</span></span>             | <span data-ttu-id="e4bdb-141">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-141">True</span></span>                              |
| <span data-ttu-id="e4bdb-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e4bdb-142">In Global Catalog</span></span>      | <span data-ttu-id="e4bdb-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e4bdb-143">False</span></span>                             |
| <span data-ttu-id="e4bdb-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4bdb-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e4bdb-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e4bdb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4bdb-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4bdb-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-148">Search-Flags</span></span>           | <span data-ttu-id="e4bdb-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4bdb-149">0x00000001</span></span>                        |
| <span data-ttu-id="e4bdb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-150">System-Flags</span></span>           | <span data-ttu-id="e4bdb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4bdb-151">0x00000010</span></span>                        |
| <span data-ttu-id="e4bdb-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e4bdb-152">Classes used in</span></span>        | [<span data-ttu-id="e4bdb-153">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e4bdb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4bdb-154">Windows Server 2003</span></span>



| <span data-ttu-id="e4bdb-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-155">Entry</span></span> | <span data-ttu-id="e4bdb-156">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e4bdb-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="e4bdb-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4bdb-159">System-Only</span></span>            | <span data-ttu-id="e4bdb-160">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-160">True</span></span>                              |
| <span data-ttu-id="e4bdb-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e4bdb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e4bdb-162">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-162">True</span></span>                              |
| <span data-ttu-id="e4bdb-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="e4bdb-163">Is Indexed</span></span>             | <span data-ttu-id="e4bdb-164">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-164">True</span></span>                              |
| <span data-ttu-id="e4bdb-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e4bdb-165">In Global Catalog</span></span>      | <span data-ttu-id="e4bdb-166">Falso</span><span class="sxs-lookup"><span data-stu-id="e4bdb-166">False</span></span>                             |
| <span data-ttu-id="e4bdb-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4bdb-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e4bdb-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e4bdb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4bdb-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4bdb-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-171">Search-Flags</span></span>           | <span data-ttu-id="e4bdb-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4bdb-172">0x00000001</span></span>                        |
| <span data-ttu-id="e4bdb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-173">System-Flags</span></span>           | <span data-ttu-id="e4bdb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4bdb-174">0x00000010</span></span>                        |
| <span data-ttu-id="e4bdb-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e4bdb-175">Classes used in</span></span>        | [<span data-ttu-id="e4bdb-176">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e4bdb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e4bdb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e4bdb-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-178">Entry</span></span> | <span data-ttu-id="e4bdb-179">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e4bdb-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="e4bdb-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4bdb-182">System-Only</span></span>            | <span data-ttu-id="e4bdb-183">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-183">True</span></span>                              |
| <span data-ttu-id="e4bdb-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e4bdb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e4bdb-185">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-185">True</span></span>                              |
| <span data-ttu-id="e4bdb-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="e4bdb-186">Is Indexed</span></span>             | <span data-ttu-id="e4bdb-187">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-187">True</span></span>                              |
| <span data-ttu-id="e4bdb-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e4bdb-188">In Global Catalog</span></span>      | <span data-ttu-id="e4bdb-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e4bdb-189">False</span></span>                             |
| <span data-ttu-id="e4bdb-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4bdb-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e4bdb-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e4bdb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4bdb-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4bdb-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-194">Search-Flags</span></span>           | <span data-ttu-id="e4bdb-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4bdb-195">0x00000001</span></span>                        |
| <span data-ttu-id="e4bdb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-196">System-Flags</span></span>           | <span data-ttu-id="e4bdb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4bdb-197">0x00000010</span></span>                        |
| <span data-ttu-id="e4bdb-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e4bdb-198">Classes used in</span></span>        | [<span data-ttu-id="e4bdb-199">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e4bdb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4bdb-200">Windows Server 2008</span></span>



| <span data-ttu-id="e4bdb-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-201">Entry</span></span> | <span data-ttu-id="e4bdb-202">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e4bdb-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="e4bdb-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4bdb-205">System-Only</span></span>            | <span data-ttu-id="e4bdb-206">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-206">True</span></span>                              |
| <span data-ttu-id="e4bdb-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e4bdb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e4bdb-208">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-208">True</span></span>                              |
| <span data-ttu-id="e4bdb-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="e4bdb-209">Is Indexed</span></span>             | <span data-ttu-id="e4bdb-210">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-210">True</span></span>                              |
| <span data-ttu-id="e4bdb-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e4bdb-211">In Global Catalog</span></span>      | <span data-ttu-id="e4bdb-212">Falso</span><span class="sxs-lookup"><span data-stu-id="e4bdb-212">False</span></span>                             |
| <span data-ttu-id="e4bdb-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4bdb-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e4bdb-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e4bdb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4bdb-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4bdb-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-217">Search-Flags</span></span>           | <span data-ttu-id="e4bdb-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4bdb-218">0x00000001</span></span>                        |
| <span data-ttu-id="e4bdb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-219">System-Flags</span></span>           | <span data-ttu-id="e4bdb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4bdb-220">0x00000010</span></span>                        |
| <span data-ttu-id="e4bdb-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e4bdb-221">Classes used in</span></span>        | [<span data-ttu-id="e4bdb-222">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e4bdb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4bdb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e4bdb-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-224">Entry</span></span> | <span data-ttu-id="e4bdb-225">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e4bdb-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="e4bdb-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4bdb-228">System-Only</span></span>            | <span data-ttu-id="e4bdb-229">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-229">True</span></span>                              |
| <span data-ttu-id="e4bdb-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e4bdb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e4bdb-231">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-231">True</span></span>                              |
| <span data-ttu-id="e4bdb-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="e4bdb-232">Is Indexed</span></span>             | <span data-ttu-id="e4bdb-233">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-233">True</span></span>                              |
| <span data-ttu-id="e4bdb-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e4bdb-234">In Global Catalog</span></span>      | <span data-ttu-id="e4bdb-235">Falso</span><span class="sxs-lookup"><span data-stu-id="e4bdb-235">False</span></span>                             |
| <span data-ttu-id="e4bdb-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4bdb-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e4bdb-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e4bdb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4bdb-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4bdb-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-240">Search-Flags</span></span>           | <span data-ttu-id="e4bdb-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4bdb-241">0x00000001</span></span>                        |
| <span data-ttu-id="e4bdb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-242">System-Flags</span></span>           | <span data-ttu-id="e4bdb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4bdb-243">0x00000010</span></span>                        |
| <span data-ttu-id="e4bdb-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e4bdb-244">Classes used in</span></span>        | [<span data-ttu-id="e4bdb-245">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e4bdb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4bdb-246">Windows Server 2012</span></span>



| <span data-ttu-id="e4bdb-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4bdb-247">Entry</span></span> | <span data-ttu-id="e4bdb-248">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e4bdb-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="e4bdb-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4bdb-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e4bdb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4bdb-251">System-Only</span></span>            | <span data-ttu-id="e4bdb-252">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-252">True</span></span>                              |
| <span data-ttu-id="e4bdb-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e4bdb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e4bdb-254">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-254">True</span></span>                              |
| <span data-ttu-id="e4bdb-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="e4bdb-255">Is Indexed</span></span>             | <span data-ttu-id="e4bdb-256">True</span><span class="sxs-lookup"><span data-stu-id="e4bdb-256">True</span></span>                              |
| <span data-ttu-id="e4bdb-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e4bdb-257">In Global Catalog</span></span>      | <span data-ttu-id="e4bdb-258">Falso</span><span class="sxs-lookup"><span data-stu-id="e4bdb-258">False</span></span>                             |
| <span data-ttu-id="e4bdb-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e4bdb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4bdb-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e4bdb-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e4bdb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4bdb-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4bdb-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e4bdb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-263">Search-Flags</span></span>           | <span data-ttu-id="e4bdb-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4bdb-264">0x00000001</span></span>                        |
| <span data-ttu-id="e4bdb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4bdb-265">System-Flags</span></span>           | <span data-ttu-id="e4bdb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4bdb-266">0x00000010</span></span>                        |
| <span data-ttu-id="e4bdb-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e4bdb-267">Classes used in</span></span>        | [<span data-ttu-id="e4bdb-268">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e4bdb-268">**User**</span></span>](c-user.md)<br/> |



 

 





