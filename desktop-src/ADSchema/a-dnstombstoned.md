---
title: DNS-Tombstoned atributo
description: True se este objeto tiver sido marcado para exclusão. Esse atributo existe para tornar a pesquisa de registros marcados para exclusão mais fácil e rápida. Os objetos marcados para exclusão são objetos que foram excluídos, mas que ainda não foram removidos do diretório.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Esquema de DNS-Tombstoned do atributo AD
- Esquema de AD do atributo dNSTombstoned
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825004"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="4f37b-107">DNS-Tombstoned atributo</span><span class="sxs-lookup"><span data-stu-id="4f37b-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="4f37b-108">True se este objeto tiver sido marcado para exclusão.</span><span class="sxs-lookup"><span data-stu-id="4f37b-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="4f37b-109">Esse atributo existe para tornar a pesquisa de registros marcados para exclusão mais fácil e rápida.</span><span class="sxs-lookup"><span data-stu-id="4f37b-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="4f37b-110">Os objetos marcados para exclusão são objetos que foram excluídos, mas que ainda não foram removidos do diretório.</span><span class="sxs-lookup"><span data-stu-id="4f37b-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="4f37b-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-111">Entry</span></span> | <span data-ttu-id="4f37b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4f37b-113">CN</span><span class="sxs-lookup"><span data-stu-id="4f37b-113">CN</span></span>                | <span data-ttu-id="4f37b-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="4f37b-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="4f37b-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4f37b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4f37b-116">dNSTombstoned</span><span class="sxs-lookup"><span data-stu-id="4f37b-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="4f37b-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4f37b-117">Size</span></span>              | <span data-ttu-id="4f37b-118">4 bytes</span><span class="sxs-lookup"><span data-stu-id="4f37b-118">4 bytes</span></span>                              |
| <span data-ttu-id="4f37b-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4f37b-119">Update Privilege</span></span>  | <span data-ttu-id="4f37b-120">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4f37b-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="4f37b-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4f37b-121">Update Frequency</span></span>  | <span data-ttu-id="4f37b-122">Sempre que um objeto é excluído.</span><span class="sxs-lookup"><span data-stu-id="4f37b-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="4f37b-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-123">Attribute-Id</span></span>      | <span data-ttu-id="4f37b-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="4f37b-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="4f37b-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4f37b-125">System-Id-Guid</span></span>    | <span data-ttu-id="4f37b-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="4f37b-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="4f37b-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f37b-127">Syntax</span></span>            | [<span data-ttu-id="4f37b-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f37b-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="4f37b-129">Implementações</span><span class="sxs-lookup"><span data-stu-id="4f37b-129">Implementations</span></span>

-   [<span data-ttu-id="4f37b-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4f37b-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4f37b-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f37b-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f37b-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f37b-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f37b-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f37b-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f37b-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f37b-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f37b-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f37b-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4f37b-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f37b-136">Windows 2000 Server</span></span>



| <span data-ttu-id="4f37b-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-137">Entry</span></span> | <span data-ttu-id="4f37b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f37b-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f37b-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f37b-141">System-Only</span></span>            | <span data-ttu-id="4f37b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-142">False</span></span>                                    |
| <span data-ttu-id="4f37b-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f37b-143">Is-Single-Valued</span></span>       | <span data-ttu-id="4f37b-144">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-144">True</span></span>                                     |
| <span data-ttu-id="4f37b-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f37b-145">Is Indexed</span></span>             | <span data-ttu-id="4f37b-146">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-146">True</span></span>                                     |
| <span data-ttu-id="4f37b-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f37b-147">In Global Catalog</span></span>      | <span data-ttu-id="4f37b-148">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-148">False</span></span>                                    |
| <span data-ttu-id="4f37b-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f37b-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f37b-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f37b-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f37b-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f37b-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f37b-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-153">Search-Flags</span></span>           | <span data-ttu-id="4f37b-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4f37b-154">0x00000001</span></span>                               |
| <span data-ttu-id="4f37b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-155">System-Flags</span></span>           | <span data-ttu-id="4f37b-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f37b-156">0x00000010</span></span>                               |
| <span data-ttu-id="4f37b-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f37b-157">Classes used in</span></span>        | [<span data-ttu-id="4f37b-158">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="4f37b-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4f37b-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f37b-159">Windows Server 2003</span></span>



| <span data-ttu-id="4f37b-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-160">Entry</span></span> | <span data-ttu-id="4f37b-161">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f37b-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f37b-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f37b-164">System-Only</span></span>            | <span data-ttu-id="4f37b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-165">False</span></span>                                    |
| <span data-ttu-id="4f37b-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f37b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="4f37b-167">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-167">True</span></span>                                     |
| <span data-ttu-id="4f37b-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f37b-168">Is Indexed</span></span>             | <span data-ttu-id="4f37b-169">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-169">True</span></span>                                     |
| <span data-ttu-id="4f37b-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f37b-170">In Global Catalog</span></span>      | <span data-ttu-id="4f37b-171">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-171">False</span></span>                                    |
| <span data-ttu-id="4f37b-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f37b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f37b-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f37b-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f37b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f37b-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f37b-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-176">Search-Flags</span></span>           | <span data-ttu-id="4f37b-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4f37b-177">0x00000001</span></span>                               |
| <span data-ttu-id="4f37b-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-178">System-Flags</span></span>           | <span data-ttu-id="4f37b-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f37b-179">0x00000010</span></span>                               |
| <span data-ttu-id="4f37b-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f37b-180">Classes used in</span></span>        | [<span data-ttu-id="4f37b-181">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="4f37b-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f37b-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f37b-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f37b-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-183">Entry</span></span> | <span data-ttu-id="4f37b-184">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f37b-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f37b-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f37b-187">System-Only</span></span>            | <span data-ttu-id="4f37b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-188">False</span></span>                                    |
| <span data-ttu-id="4f37b-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f37b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4f37b-190">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-190">True</span></span>                                     |
| <span data-ttu-id="4f37b-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f37b-191">Is Indexed</span></span>             | <span data-ttu-id="4f37b-192">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-192">True</span></span>                                     |
| <span data-ttu-id="4f37b-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f37b-193">In Global Catalog</span></span>      | <span data-ttu-id="4f37b-194">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-194">False</span></span>                                    |
| <span data-ttu-id="4f37b-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f37b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f37b-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f37b-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f37b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f37b-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f37b-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-199">Search-Flags</span></span>           | <span data-ttu-id="4f37b-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4f37b-200">0x00000001</span></span>                               |
| <span data-ttu-id="4f37b-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-201">System-Flags</span></span>           | <span data-ttu-id="4f37b-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f37b-202">0x00000010</span></span>                               |
| <span data-ttu-id="4f37b-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f37b-203">Classes used in</span></span>        | [<span data-ttu-id="4f37b-204">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="4f37b-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f37b-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f37b-205">Windows Server 2008</span></span>



| <span data-ttu-id="4f37b-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-206">Entry</span></span> | <span data-ttu-id="4f37b-207">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f37b-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f37b-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f37b-210">System-Only</span></span>            | <span data-ttu-id="4f37b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-211">False</span></span>                                    |
| <span data-ttu-id="4f37b-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f37b-212">Is-Single-Valued</span></span>       | <span data-ttu-id="4f37b-213">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-213">True</span></span>                                     |
| <span data-ttu-id="4f37b-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f37b-214">Is Indexed</span></span>             | <span data-ttu-id="4f37b-215">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-215">True</span></span>                                     |
| <span data-ttu-id="4f37b-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f37b-216">In Global Catalog</span></span>      | <span data-ttu-id="4f37b-217">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-217">False</span></span>                                    |
| <span data-ttu-id="4f37b-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f37b-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f37b-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f37b-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f37b-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f37b-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f37b-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-222">Search-Flags</span></span>           | <span data-ttu-id="4f37b-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4f37b-223">0x00000001</span></span>                               |
| <span data-ttu-id="4f37b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-224">System-Flags</span></span>           | <span data-ttu-id="4f37b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f37b-225">0x00000010</span></span>                               |
| <span data-ttu-id="4f37b-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f37b-226">Classes used in</span></span>        | [<span data-ttu-id="4f37b-227">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="4f37b-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f37b-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f37b-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f37b-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-229">Entry</span></span> | <span data-ttu-id="4f37b-230">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f37b-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f37b-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f37b-233">System-Only</span></span>            | <span data-ttu-id="4f37b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-234">False</span></span>                                    |
| <span data-ttu-id="4f37b-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f37b-235">Is-Single-Valued</span></span>       | <span data-ttu-id="4f37b-236">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-236">True</span></span>                                     |
| <span data-ttu-id="4f37b-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f37b-237">Is Indexed</span></span>             | <span data-ttu-id="4f37b-238">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-238">True</span></span>                                     |
| <span data-ttu-id="4f37b-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f37b-239">In Global Catalog</span></span>      | <span data-ttu-id="4f37b-240">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-240">False</span></span>                                    |
| <span data-ttu-id="4f37b-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f37b-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f37b-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f37b-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f37b-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f37b-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f37b-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-245">Search-Flags</span></span>           | <span data-ttu-id="4f37b-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4f37b-246">0x00000001</span></span>                               |
| <span data-ttu-id="4f37b-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-247">System-Flags</span></span>           | <span data-ttu-id="4f37b-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f37b-248">0x00000010</span></span>                               |
| <span data-ttu-id="4f37b-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f37b-249">Classes used in</span></span>        | [<span data-ttu-id="4f37b-250">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="4f37b-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f37b-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f37b-251">Windows Server 2012</span></span>



| <span data-ttu-id="4f37b-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f37b-252">Entry</span></span> | <span data-ttu-id="4f37b-253">Valor</span><span class="sxs-lookup"><span data-stu-id="4f37b-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="4f37b-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="4f37b-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f37b-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="4f37b-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f37b-256">System-Only</span></span>            | <span data-ttu-id="4f37b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-257">False</span></span>                                    |
| <span data-ttu-id="4f37b-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4f37b-258">Is-Single-Valued</span></span>       | <span data-ttu-id="4f37b-259">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-259">True</span></span>                                     |
| <span data-ttu-id="4f37b-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="4f37b-260">Is Indexed</span></span>             | <span data-ttu-id="4f37b-261">True</span><span class="sxs-lookup"><span data-stu-id="4f37b-261">True</span></span>                                     |
| <span data-ttu-id="4f37b-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4f37b-262">In Global Catalog</span></span>      | <span data-ttu-id="4f37b-263">Falso</span><span class="sxs-lookup"><span data-stu-id="4f37b-263">False</span></span>                                    |
| <span data-ttu-id="4f37b-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4f37b-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f37b-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4f37b-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="4f37b-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f37b-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f37b-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="4f37b-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-268">Search-Flags</span></span>           | <span data-ttu-id="4f37b-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4f37b-269">0x00000001</span></span>                               |
| <span data-ttu-id="4f37b-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f37b-270">System-Flags</span></span>           | <span data-ttu-id="4f37b-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4f37b-271">0x00000010</span></span>                               |
| <span data-ttu-id="4f37b-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4f37b-272">Classes used in</span></span>        | [<span data-ttu-id="4f37b-273">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="4f37b-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





