---
title: O atributo GPC-User-Extension-Names
description: Usado pelo objeto Política de Grupo para as políticas de usuário.
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- GPC-User-Extension-Names atributo AD Schema
- Esquema de AD do atributo gPCUserExtensionNames
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456115"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="f8043-105">O atributo GPC-User-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="f8043-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="f8043-106">Usado pelo objeto Política de Grupo para as políticas de usuário.</span><span class="sxs-lookup"><span data-stu-id="f8043-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="f8043-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-107">Entry</span></span> | <span data-ttu-id="f8043-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f8043-109">CN</span><span class="sxs-lookup"><span data-stu-id="f8043-109">CN</span></span>                | <span data-ttu-id="f8043-110">GPC-User-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="f8043-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="f8043-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f8043-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f8043-112">gPCUserExtensionNames</span><span class="sxs-lookup"><span data-stu-id="f8043-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="f8043-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f8043-113">Size</span></span>              | <span data-ttu-id="f8043-114">Depende do número de extensões do lado do cliente que têm uma política nesse GPO.</span><span class="sxs-lookup"><span data-stu-id="f8043-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="f8043-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f8043-115">Update Privilege</span></span>  | <span data-ttu-id="f8043-116">Administrador de política ou de domínio.</span><span class="sxs-lookup"><span data-stu-id="f8043-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="f8043-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f8043-117">Update Frequency</span></span>  | <span data-ttu-id="f8043-118">Sempre que um GPO é atualizado por meio de GPE.</span><span class="sxs-lookup"><span data-stu-id="f8043-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="f8043-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-119">Attribute-Id</span></span>      | <span data-ttu-id="f8043-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="f8043-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="f8043-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f8043-121">System-Id-Guid</span></span>    | <span data-ttu-id="f8043-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f8043-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="f8043-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8043-123">Syntax</span></span>            | [<span data-ttu-id="f8043-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f8043-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="f8043-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="f8043-125">Implementations</span></span>

-   [<span data-ttu-id="f8043-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f8043-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f8043-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f8043-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f8043-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f8043-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f8043-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f8043-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f8043-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f8043-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f8043-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f8043-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f8043-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8043-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f8043-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-133">Entry</span></span> | <span data-ttu-id="f8043-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f8043-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8043-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8043-137">System-Only</span></span>            | <span data-ttu-id="f8043-138">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-138">False</span></span>                                                               |
| <span data-ttu-id="f8043-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8043-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f8043-140">True</span><span class="sxs-lookup"><span data-stu-id="f8043-140">True</span></span>                                                                |
| <span data-ttu-id="f8043-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8043-141">Is Indexed</span></span>             | <span data-ttu-id="f8043-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-142">False</span></span>                                                               |
| <span data-ttu-id="f8043-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8043-143">In Global Catalog</span></span>      | <span data-ttu-id="f8043-144">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-144">False</span></span>                                                               |
| <span data-ttu-id="f8043-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8043-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8043-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8043-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f8043-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8043-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8043-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-149">Search-Flags</span></span>           | <span data-ttu-id="f8043-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8043-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="f8043-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-151">System-Flags</span></span>           | <span data-ttu-id="f8043-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8043-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="f8043-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8043-153">Classes used in</span></span>        | [<span data-ttu-id="f8043-154">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="f8043-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f8043-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8043-155">Windows Server 2003</span></span>



| <span data-ttu-id="f8043-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-156">Entry</span></span> | <span data-ttu-id="f8043-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f8043-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8043-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8043-160">System-Only</span></span>            | <span data-ttu-id="f8043-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-161">False</span></span>                                                               |
| <span data-ttu-id="f8043-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8043-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f8043-163">True</span><span class="sxs-lookup"><span data-stu-id="f8043-163">True</span></span>                                                                |
| <span data-ttu-id="f8043-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8043-164">Is Indexed</span></span>             | <span data-ttu-id="f8043-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-165">False</span></span>                                                               |
| <span data-ttu-id="f8043-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8043-166">In Global Catalog</span></span>      | <span data-ttu-id="f8043-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-167">False</span></span>                                                               |
| <span data-ttu-id="f8043-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8043-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8043-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8043-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f8043-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8043-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8043-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-172">Search-Flags</span></span>           | <span data-ttu-id="f8043-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8043-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="f8043-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-174">System-Flags</span></span>           | <span data-ttu-id="f8043-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8043-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="f8043-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8043-176">Classes used in</span></span>        | [<span data-ttu-id="f8043-177">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="f8043-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f8043-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f8043-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f8043-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-179">Entry</span></span> | <span data-ttu-id="f8043-180">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f8043-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8043-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8043-183">System-Only</span></span>            | <span data-ttu-id="f8043-184">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-184">False</span></span>                                                               |
| <span data-ttu-id="f8043-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8043-185">Is-Single-Valued</span></span>       | <span data-ttu-id="f8043-186">True</span><span class="sxs-lookup"><span data-stu-id="f8043-186">True</span></span>                                                                |
| <span data-ttu-id="f8043-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8043-187">Is Indexed</span></span>             | <span data-ttu-id="f8043-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-188">False</span></span>                                                               |
| <span data-ttu-id="f8043-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8043-189">In Global Catalog</span></span>      | <span data-ttu-id="f8043-190">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-190">False</span></span>                                                               |
| <span data-ttu-id="f8043-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8043-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8043-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8043-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f8043-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8043-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8043-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-195">Search-Flags</span></span>           | <span data-ttu-id="f8043-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8043-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="f8043-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-197">System-Flags</span></span>           | <span data-ttu-id="f8043-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8043-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="f8043-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8043-199">Classes used in</span></span>        | [<span data-ttu-id="f8043-200">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="f8043-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f8043-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8043-201">Windows Server 2008</span></span>



| <span data-ttu-id="f8043-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-202">Entry</span></span> | <span data-ttu-id="f8043-203">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f8043-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8043-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8043-206">System-Only</span></span>            | <span data-ttu-id="f8043-207">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-207">False</span></span>                                                               |
| <span data-ttu-id="f8043-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8043-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f8043-209">True</span><span class="sxs-lookup"><span data-stu-id="f8043-209">True</span></span>                                                                |
| <span data-ttu-id="f8043-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8043-210">Is Indexed</span></span>             | <span data-ttu-id="f8043-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-211">False</span></span>                                                               |
| <span data-ttu-id="f8043-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8043-212">In Global Catalog</span></span>      | <span data-ttu-id="f8043-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-213">False</span></span>                                                               |
| <span data-ttu-id="f8043-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8043-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8043-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8043-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f8043-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8043-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8043-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-218">Search-Flags</span></span>           | <span data-ttu-id="f8043-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8043-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="f8043-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-220">System-Flags</span></span>           | <span data-ttu-id="f8043-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8043-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="f8043-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8043-222">Classes used in</span></span>        | [<span data-ttu-id="f8043-223">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="f8043-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f8043-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8043-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f8043-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-225">Entry</span></span> | <span data-ttu-id="f8043-226">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f8043-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8043-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8043-229">System-Only</span></span>            | <span data-ttu-id="f8043-230">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-230">False</span></span>                                                               |
| <span data-ttu-id="f8043-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8043-231">Is-Single-Valued</span></span>       | <span data-ttu-id="f8043-232">True</span><span class="sxs-lookup"><span data-stu-id="f8043-232">True</span></span>                                                                |
| <span data-ttu-id="f8043-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8043-233">Is Indexed</span></span>             | <span data-ttu-id="f8043-234">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-234">False</span></span>                                                               |
| <span data-ttu-id="f8043-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8043-235">In Global Catalog</span></span>      | <span data-ttu-id="f8043-236">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-236">False</span></span>                                                               |
| <span data-ttu-id="f8043-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8043-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8043-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8043-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f8043-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8043-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8043-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-241">Search-Flags</span></span>           | <span data-ttu-id="f8043-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8043-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="f8043-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-243">System-Flags</span></span>           | <span data-ttu-id="f8043-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8043-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="f8043-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8043-245">Classes used in</span></span>        | [<span data-ttu-id="f8043-246">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="f8043-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f8043-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8043-247">Windows Server 2012</span></span>



| <span data-ttu-id="f8043-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8043-248">Entry</span></span> | <span data-ttu-id="f8043-249">Valor</span><span class="sxs-lookup"><span data-stu-id="f8043-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f8043-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8043-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8043-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="f8043-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8043-252">System-Only</span></span>            | <span data-ttu-id="f8043-253">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-253">False</span></span>                                                               |
| <span data-ttu-id="f8043-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8043-254">Is-Single-Valued</span></span>       | <span data-ttu-id="f8043-255">True</span><span class="sxs-lookup"><span data-stu-id="f8043-255">True</span></span>                                                                |
| <span data-ttu-id="f8043-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8043-256">Is Indexed</span></span>             | <span data-ttu-id="f8043-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-257">False</span></span>                                                               |
| <span data-ttu-id="f8043-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8043-258">In Global Catalog</span></span>      | <span data-ttu-id="f8043-259">Falso</span><span class="sxs-lookup"><span data-stu-id="f8043-259">False</span></span>                                                               |
| <span data-ttu-id="f8043-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8043-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8043-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8043-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="f8043-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8043-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8043-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="f8043-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-264">Search-Flags</span></span>           | <span data-ttu-id="f8043-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8043-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="f8043-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8043-266">System-Flags</span></span>           | <span data-ttu-id="f8043-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8043-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="f8043-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8043-268">Classes used in</span></span>        | [<span data-ttu-id="f8043-269">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="f8043-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





