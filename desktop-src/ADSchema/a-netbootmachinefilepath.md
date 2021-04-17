---
title: Atributo netboot-Machine-File-Path
description: Esse atributo especifica o servidor que responde ao cliente. A partir do sistema operacional Windows Server 2003, ele pode indicar o Startrom.com que o cliente obtém.
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- Netboot – Machine-arquivo-Path atributo AD Schema
- Esquema de AD do atributo netbootMachineFilePath
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749103"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="b034a-106">Atributo netboot-Machine-File-Path</span><span class="sxs-lookup"><span data-stu-id="b034a-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="b034a-107">Esse atributo especifica o servidor que responde ao cliente.</span><span class="sxs-lookup"><span data-stu-id="b034a-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="b034a-108">A partir do sistema operacional Windows Server 2003, ele pode indicar o Startrom.com que o cliente obtém.</span><span class="sxs-lookup"><span data-stu-id="b034a-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="b034a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-109">Entry</span></span> | <span data-ttu-id="b034a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b034a-111">CN</span><span class="sxs-lookup"><span data-stu-id="b034a-111">CN</span></span>                | <span data-ttu-id="b034a-112">Netboot-máquina-arquivo-caminho</span><span class="sxs-lookup"><span data-stu-id="b034a-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="b034a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b034a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b034a-114">netbootMachineFilePath</span><span class="sxs-lookup"><span data-stu-id="b034a-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="b034a-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b034a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b034a-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b034a-116">Update Privilege</span></span>  | <span data-ttu-id="b034a-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b034a-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="b034a-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b034a-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b034a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-119">Attribute-Id</span></span>      | <span data-ttu-id="b034a-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="b034a-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="b034a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b034a-121">System-Id-Guid</span></span>    | <span data-ttu-id="b034a-122">3e978923-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b034a-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="b034a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b034a-123">Syntax</span></span>            | [<span data-ttu-id="b034a-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b034a-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b034a-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="b034a-125">Implementations</span></span>

-   [<span data-ttu-id="b034a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b034a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b034a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b034a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b034a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b034a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b034a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b034a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b034a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b034a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b034a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b034a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b034a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b034a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b034a-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-133">Entry</span></span> | <span data-ttu-id="b034a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b034a-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="b034a-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b034a-137">System-Only</span></span>            | <span data-ttu-id="b034a-138">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-138">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b034a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b034a-140">True</span><span class="sxs-lookup"><span data-stu-id="b034a-140">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="b034a-141">Is Indexed</span></span>             | <span data-ttu-id="b034a-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-142">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b034a-143">In Global Catalog</span></span>      | <span data-ttu-id="b034a-144">True</span><span class="sxs-lookup"><span data-stu-id="b034a-144">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b034a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b034a-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b034a-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="b034a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b034a-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b034a-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-149">Search-Flags</span></span>           | <span data-ttu-id="b034a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b034a-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="b034a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-151">System-Flags</span></span>           | <span data-ttu-id="b034a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b034a-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="b034a-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b034a-153">Classes used in</span></span>        | [<span data-ttu-id="b034a-154">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b034a-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b034a-155">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b034a-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b034a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b034a-156">Windows Server 2003</span></span>



| <span data-ttu-id="b034a-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-157">Entry</span></span> | <span data-ttu-id="b034a-158">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b034a-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="b034a-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b034a-161">System-Only</span></span>            | <span data-ttu-id="b034a-162">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-162">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b034a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b034a-164">True</span><span class="sxs-lookup"><span data-stu-id="b034a-164">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="b034a-165">Is Indexed</span></span>             | <span data-ttu-id="b034a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-166">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b034a-167">In Global Catalog</span></span>      | <span data-ttu-id="b034a-168">True</span><span class="sxs-lookup"><span data-stu-id="b034a-168">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b034a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b034a-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b034a-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="b034a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b034a-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b034a-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-173">Search-Flags</span></span>           | <span data-ttu-id="b034a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b034a-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="b034a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-175">System-Flags</span></span>           | <span data-ttu-id="b034a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b034a-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="b034a-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b034a-177">Classes used in</span></span>        | [<span data-ttu-id="b034a-178">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b034a-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b034a-179">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b034a-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b034a-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b034a-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b034a-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-181">Entry</span></span> | <span data-ttu-id="b034a-182">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b034a-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="b034a-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b034a-185">System-Only</span></span>            | <span data-ttu-id="b034a-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-186">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b034a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b034a-188">True</span><span class="sxs-lookup"><span data-stu-id="b034a-188">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="b034a-189">Is Indexed</span></span>             | <span data-ttu-id="b034a-190">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-190">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b034a-191">In Global Catalog</span></span>      | <span data-ttu-id="b034a-192">True</span><span class="sxs-lookup"><span data-stu-id="b034a-192">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b034a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b034a-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b034a-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="b034a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b034a-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b034a-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-197">Search-Flags</span></span>           | <span data-ttu-id="b034a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b034a-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="b034a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-199">System-Flags</span></span>           | <span data-ttu-id="b034a-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b034a-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="b034a-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b034a-201">Classes used in</span></span>        | [<span data-ttu-id="b034a-202">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b034a-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b034a-203">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b034a-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b034a-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b034a-204">Windows Server 2008</span></span>



| <span data-ttu-id="b034a-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-205">Entry</span></span> | <span data-ttu-id="b034a-206">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b034a-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="b034a-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b034a-209">System-Only</span></span>            | <span data-ttu-id="b034a-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-210">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b034a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b034a-212">True</span><span class="sxs-lookup"><span data-stu-id="b034a-212">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="b034a-213">Is Indexed</span></span>             | <span data-ttu-id="b034a-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-214">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b034a-215">In Global Catalog</span></span>      | <span data-ttu-id="b034a-216">True</span><span class="sxs-lookup"><span data-stu-id="b034a-216">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b034a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b034a-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b034a-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="b034a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b034a-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b034a-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-221">Search-Flags</span></span>           | <span data-ttu-id="b034a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b034a-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="b034a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-223">System-Flags</span></span>           | <span data-ttu-id="b034a-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b034a-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="b034a-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b034a-225">Classes used in</span></span>        | [<span data-ttu-id="b034a-226">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b034a-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b034a-227">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b034a-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b034a-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b034a-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b034a-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-229">Entry</span></span> | <span data-ttu-id="b034a-230">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b034a-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="b034a-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="b034a-233">System-Only</span></span>            | <span data-ttu-id="b034a-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-234">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b034a-235">Is-Single-Valued</span></span>       | <span data-ttu-id="b034a-236">True</span><span class="sxs-lookup"><span data-stu-id="b034a-236">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="b034a-237">Is Indexed</span></span>             | <span data-ttu-id="b034a-238">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-238">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b034a-239">In Global Catalog</span></span>      | <span data-ttu-id="b034a-240">True</span><span class="sxs-lookup"><span data-stu-id="b034a-240">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b034a-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="b034a-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b034a-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="b034a-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b034a-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b034a-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-245">Search-Flags</span></span>           | <span data-ttu-id="b034a-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b034a-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="b034a-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-247">System-Flags</span></span>           | <span data-ttu-id="b034a-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b034a-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="b034a-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b034a-249">Classes used in</span></span>        | [<span data-ttu-id="b034a-250">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b034a-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b034a-251">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b034a-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b034a-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b034a-252">Windows Server 2012</span></span>



| <span data-ttu-id="b034a-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="b034a-253">Entry</span></span> | <span data-ttu-id="b034a-254">Valor</span><span class="sxs-lookup"><span data-stu-id="b034a-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b034a-255">ID do link</span><span class="sxs-lookup"><span data-stu-id="b034a-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b034a-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="b034a-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="b034a-257">System-Only</span></span>            | <span data-ttu-id="b034a-258">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-258">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b034a-259">Is-Single-Valued</span></span>       | <span data-ttu-id="b034a-260">True</span><span class="sxs-lookup"><span data-stu-id="b034a-260">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="b034a-261">Is Indexed</span></span>             | <span data-ttu-id="b034a-262">Falso</span><span class="sxs-lookup"><span data-stu-id="b034a-262">False</span></span>                                                                                                |
| <span data-ttu-id="b034a-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b034a-263">In Global Catalog</span></span>      | <span data-ttu-id="b034a-264">True</span><span class="sxs-lookup"><span data-stu-id="b034a-264">True</span></span>                                                                                                 |
| <span data-ttu-id="b034a-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b034a-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="b034a-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b034a-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="b034a-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b034a-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b034a-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="b034a-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-269">Search-Flags</span></span>           | <span data-ttu-id="b034a-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b034a-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="b034a-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b034a-271">System-Flags</span></span>           | <span data-ttu-id="b034a-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b034a-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="b034a-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b034a-273">Classes used in</span></span>        | [<span data-ttu-id="b034a-274">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b034a-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b034a-275">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="b034a-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





