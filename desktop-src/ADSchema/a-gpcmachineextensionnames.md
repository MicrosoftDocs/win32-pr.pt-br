---
title: O atributo GPC-Machine-Extension-Names
description: Usado pelo objeto Política de Grupo para as políticas do computador.
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- GPC-Machine-Extension-Names atributo AD Schema
- Esquema de AD do atributo gPCMachineExtensionNames
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919534"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="fd8bf-105">O atributo GPC-Machine-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="fd8bf-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="fd8bf-106">Usado pelo objeto Política de Grupo para as políticas do computador.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="fd8bf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-107">Entry</span></span> | <span data-ttu-id="fd8bf-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-109">CN</span><span class="sxs-lookup"><span data-stu-id="fd8bf-109">CN</span></span>                | <span data-ttu-id="fd8bf-110">GPC-Machine-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="fd8bf-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="fd8bf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fd8bf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fd8bf-112">gPCMachineExtensionNames</span><span class="sxs-lookup"><span data-stu-id="fd8bf-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="fd8bf-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="fd8bf-113">Size</span></span>              | <span data-ttu-id="fd8bf-114">Depende do número de extensões do lado do cliente que têm uma política nesse GPO.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="fd8bf-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="fd8bf-115">Update Privilege</span></span>  | <span data-ttu-id="fd8bf-116">Administrador de política ou de domínio.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="fd8bf-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="fd8bf-117">Update Frequency</span></span>  | <span data-ttu-id="fd8bf-118">Sempre que um GPO é atualizado por meio de GPE.</span><span class="sxs-lookup"><span data-stu-id="fd8bf-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="fd8bf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-119">Attribute-Id</span></span>      | <span data-ttu-id="fd8bf-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="fd8bf-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="fd8bf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fd8bf-121">System-Id-Guid</span></span>    | <span data-ttu-id="fd8bf-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="fd8bf-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="fd8bf-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd8bf-123">Syntax</span></span>            | [<span data-ttu-id="fd8bf-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="fd8bf-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="fd8bf-125">Implementations</span></span>

-   [<span data-ttu-id="fd8bf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fd8bf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fd8bf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fd8bf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fd8bf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fd8bf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fd8bf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd8bf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fd8bf-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-133">Entry</span></span> | <span data-ttu-id="fd8bf-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="fd8bf-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd8bf-137">System-Only</span></span>            | <span data-ttu-id="fd8bf-138">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-138">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fd8bf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fd8bf-140">True</span><span class="sxs-lookup"><span data-stu-id="fd8bf-140">True</span></span>                                                                |
| <span data-ttu-id="fd8bf-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="fd8bf-141">Is Indexed</span></span>             | <span data-ttu-id="fd8bf-142">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-142">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fd8bf-143">In Global Catalog</span></span>      | <span data-ttu-id="fd8bf-144">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-144">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd8bf-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fd8bf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd8bf-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd8bf-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-149">Search-Flags</span></span>           | <span data-ttu-id="fd8bf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd8bf-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="fd8bf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-151">System-Flags</span></span>           | <span data-ttu-id="fd8bf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd8bf-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="fd8bf-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fd8bf-153">Classes used in</span></span>        | [<span data-ttu-id="fd8bf-154">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fd8bf-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd8bf-155">Windows Server 2003</span></span>



| <span data-ttu-id="fd8bf-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-156">Entry</span></span> | <span data-ttu-id="fd8bf-157">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="fd8bf-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd8bf-160">System-Only</span></span>            | <span data-ttu-id="fd8bf-161">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-161">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fd8bf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fd8bf-163">True</span><span class="sxs-lookup"><span data-stu-id="fd8bf-163">True</span></span>                                                                |
| <span data-ttu-id="fd8bf-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="fd8bf-164">Is Indexed</span></span>             | <span data-ttu-id="fd8bf-165">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-165">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fd8bf-166">In Global Catalog</span></span>      | <span data-ttu-id="fd8bf-167">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-167">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd8bf-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fd8bf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd8bf-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd8bf-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-172">Search-Flags</span></span>           | <span data-ttu-id="fd8bf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd8bf-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="fd8bf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-174">System-Flags</span></span>           | <span data-ttu-id="fd8bf-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd8bf-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="fd8bf-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fd8bf-176">Classes used in</span></span>        | [<span data-ttu-id="fd8bf-177">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fd8bf-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fd8bf-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fd8bf-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-179">Entry</span></span> | <span data-ttu-id="fd8bf-180">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="fd8bf-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd8bf-183">System-Only</span></span>            | <span data-ttu-id="fd8bf-184">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-184">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fd8bf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fd8bf-186">True</span><span class="sxs-lookup"><span data-stu-id="fd8bf-186">True</span></span>                                                                |
| <span data-ttu-id="fd8bf-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="fd8bf-187">Is Indexed</span></span>             | <span data-ttu-id="fd8bf-188">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-188">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fd8bf-189">In Global Catalog</span></span>      | <span data-ttu-id="fd8bf-190">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-190">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd8bf-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fd8bf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd8bf-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd8bf-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-195">Search-Flags</span></span>           | <span data-ttu-id="fd8bf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd8bf-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="fd8bf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-197">System-Flags</span></span>           | <span data-ttu-id="fd8bf-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd8bf-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="fd8bf-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fd8bf-199">Classes used in</span></span>        | [<span data-ttu-id="fd8bf-200">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fd8bf-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd8bf-201">Windows Server 2008</span></span>



| <span data-ttu-id="fd8bf-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-202">Entry</span></span> | <span data-ttu-id="fd8bf-203">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="fd8bf-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd8bf-206">System-Only</span></span>            | <span data-ttu-id="fd8bf-207">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-207">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fd8bf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fd8bf-209">True</span><span class="sxs-lookup"><span data-stu-id="fd8bf-209">True</span></span>                                                                |
| <span data-ttu-id="fd8bf-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="fd8bf-210">Is Indexed</span></span>             | <span data-ttu-id="fd8bf-211">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-211">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fd8bf-212">In Global Catalog</span></span>      | <span data-ttu-id="fd8bf-213">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-213">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd8bf-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fd8bf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd8bf-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd8bf-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-218">Search-Flags</span></span>           | <span data-ttu-id="fd8bf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd8bf-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="fd8bf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-220">System-Flags</span></span>           | <span data-ttu-id="fd8bf-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd8bf-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="fd8bf-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fd8bf-222">Classes used in</span></span>        | [<span data-ttu-id="fd8bf-223">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fd8bf-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd8bf-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fd8bf-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-225">Entry</span></span> | <span data-ttu-id="fd8bf-226">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="fd8bf-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd8bf-229">System-Only</span></span>            | <span data-ttu-id="fd8bf-230">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-230">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fd8bf-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fd8bf-232">True</span><span class="sxs-lookup"><span data-stu-id="fd8bf-232">True</span></span>                                                                |
| <span data-ttu-id="fd8bf-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="fd8bf-233">Is Indexed</span></span>             | <span data-ttu-id="fd8bf-234">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-234">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fd8bf-235">In Global Catalog</span></span>      | <span data-ttu-id="fd8bf-236">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-236">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd8bf-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fd8bf-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd8bf-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd8bf-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-241">Search-Flags</span></span>           | <span data-ttu-id="fd8bf-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd8bf-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="fd8bf-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-243">System-Flags</span></span>           | <span data-ttu-id="fd8bf-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd8bf-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="fd8bf-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fd8bf-245">Classes used in</span></span>        | [<span data-ttu-id="fd8bf-246">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fd8bf-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd8bf-247">Windows Server 2012</span></span>



| <span data-ttu-id="fd8bf-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd8bf-248">Entry</span></span> | <span data-ttu-id="fd8bf-249">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fd8bf-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="fd8bf-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fd8bf-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="fd8bf-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="fd8bf-252">System-Only</span></span>            | <span data-ttu-id="fd8bf-253">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-253">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fd8bf-254">Is-Single-Valued</span></span>       | <span data-ttu-id="fd8bf-255">True</span><span class="sxs-lookup"><span data-stu-id="fd8bf-255">True</span></span>                                                                |
| <span data-ttu-id="fd8bf-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="fd8bf-256">Is Indexed</span></span>             | <span data-ttu-id="fd8bf-257">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-257">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fd8bf-258">In Global Catalog</span></span>      | <span data-ttu-id="fd8bf-259">Falso</span><span class="sxs-lookup"><span data-stu-id="fd8bf-259">False</span></span>                                                               |
| <span data-ttu-id="fd8bf-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fd8bf-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="fd8bf-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fd8bf-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="fd8bf-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fd8bf-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fd8bf-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="fd8bf-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-264">Search-Flags</span></span>           | <span data-ttu-id="fd8bf-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd8bf-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="fd8bf-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fd8bf-266">System-Flags</span></span>           | <span data-ttu-id="fd8bf-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fd8bf-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="fd8bf-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fd8bf-268">Classes used in</span></span>        | [<span data-ttu-id="fd8bf-269">**Grupo-política-contêiner**</span><span class="sxs-lookup"><span data-stu-id="fd8bf-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





