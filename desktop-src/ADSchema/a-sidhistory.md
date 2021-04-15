---
title: SID-History atributo
description: Contém os SIDs anteriores usados para o objeto se o objeto foi movido de outro domínio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Esquema de SID-History do atributo AD
- Esquema do AD do atributo sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456174"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="a4170-105">SID-History atributo</span><span class="sxs-lookup"><span data-stu-id="a4170-105">SID-History attribute</span></span>

<span data-ttu-id="a4170-106">Contém os SIDs anteriores usados para o objeto se o objeto foi movido de outro domínio.</span><span class="sxs-lookup"><span data-stu-id="a4170-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="a4170-107">Sempre que um objeto é movido de um domínio para outro, um novo SID é criado e esse novo SID torna-se o objectSid.</span><span class="sxs-lookup"><span data-stu-id="a4170-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="a4170-108">O SID anterior é adicionado à propriedade sIDHistory.</span><span class="sxs-lookup"><span data-stu-id="a4170-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="a4170-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-109">Entry</span></span> | <span data-ttu-id="a4170-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="a4170-111">CN</span><span class="sxs-lookup"><span data-stu-id="a4170-111">CN</span></span>                | <span data-ttu-id="a4170-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="a4170-112">SID-History</span></span>                                    |
| <span data-ttu-id="a4170-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a4170-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a4170-114">sIDHistory</span><span class="sxs-lookup"><span data-stu-id="a4170-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="a4170-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a4170-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="a4170-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a4170-116">Update Privilege</span></span>  | <span data-ttu-id="a4170-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a4170-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="a4170-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a4170-118">Update Frequency</span></span>  | <span data-ttu-id="a4170-119">Cada vez que o objeto é movido para um novo domínio.</span><span class="sxs-lookup"><span data-stu-id="a4170-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="a4170-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-120">Attribute-Id</span></span>      | <span data-ttu-id="a4170-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="a4170-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="a4170-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a4170-122">System-Id-Guid</span></span>    | <span data-ttu-id="a4170-123">17eb4278-d167-11d0-b002-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a4170-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="a4170-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4170-124">Syntax</span></span>            | [<span data-ttu-id="a4170-125">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="a4170-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="a4170-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="a4170-126">Implementations</span></span>

-   [<span data-ttu-id="a4170-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a4170-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a4170-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4170-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4170-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4170-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4170-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4170-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4170-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4170-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4170-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4170-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a4170-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4170-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a4170-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-134">Entry</span></span> | <span data-ttu-id="a4170-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a4170-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4170-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4170-138">System-Only</span></span>            | <span data-ttu-id="a4170-139">True</span><span class="sxs-lookup"><span data-stu-id="a4170-139">True</span></span>                                                         |
| <span data-ttu-id="a4170-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4170-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a4170-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-141">False</span></span>                                                        |
| <span data-ttu-id="a4170-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4170-142">Is Indexed</span></span>             | <span data-ttu-id="a4170-143">True</span><span class="sxs-lookup"><span data-stu-id="a4170-143">True</span></span>                                                         |
| <span data-ttu-id="a4170-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4170-144">In Global Catalog</span></span>      | <span data-ttu-id="a4170-145">True</span><span class="sxs-lookup"><span data-stu-id="a4170-145">True</span></span>                                                         |
| <span data-ttu-id="a4170-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4170-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4170-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4170-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a4170-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4170-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4170-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-150">Search-Flags</span></span>           | <span data-ttu-id="a4170-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4170-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="a4170-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-152">System-Flags</span></span>           | <span data-ttu-id="a4170-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a4170-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="a4170-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4170-154">Classes used in</span></span>        | [<span data-ttu-id="a4170-155">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="a4170-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a4170-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4170-156">Windows Server 2003</span></span>



| <span data-ttu-id="a4170-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-157">Entry</span></span> | <span data-ttu-id="a4170-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a4170-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4170-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4170-161">System-Only</span></span>            | <span data-ttu-id="a4170-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-162">False</span></span>                                                        |
| <span data-ttu-id="a4170-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4170-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a4170-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-164">False</span></span>                                                        |
| <span data-ttu-id="a4170-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4170-165">Is Indexed</span></span>             | <span data-ttu-id="a4170-166">True</span><span class="sxs-lookup"><span data-stu-id="a4170-166">True</span></span>                                                         |
| <span data-ttu-id="a4170-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4170-167">In Global Catalog</span></span>      | <span data-ttu-id="a4170-168">True</span><span class="sxs-lookup"><span data-stu-id="a4170-168">True</span></span>                                                         |
| <span data-ttu-id="a4170-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4170-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4170-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4170-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a4170-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4170-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4170-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-173">Search-Flags</span></span>           | <span data-ttu-id="a4170-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4170-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="a4170-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-175">System-Flags</span></span>           | <span data-ttu-id="a4170-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a4170-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="a4170-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4170-177">Classes used in</span></span>        | [<span data-ttu-id="a4170-178">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="a4170-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4170-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4170-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4170-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-180">Entry</span></span> | <span data-ttu-id="a4170-181">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a4170-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4170-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4170-184">System-Only</span></span>            | <span data-ttu-id="a4170-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-185">False</span></span>                                                        |
| <span data-ttu-id="a4170-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4170-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a4170-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-187">False</span></span>                                                        |
| <span data-ttu-id="a4170-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4170-188">Is Indexed</span></span>             | <span data-ttu-id="a4170-189">True</span><span class="sxs-lookup"><span data-stu-id="a4170-189">True</span></span>                                                         |
| <span data-ttu-id="a4170-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4170-190">In Global Catalog</span></span>      | <span data-ttu-id="a4170-191">True</span><span class="sxs-lookup"><span data-stu-id="a4170-191">True</span></span>                                                         |
| <span data-ttu-id="a4170-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4170-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4170-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4170-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a4170-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4170-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4170-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-196">Search-Flags</span></span>           | <span data-ttu-id="a4170-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4170-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="a4170-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-198">System-Flags</span></span>           | <span data-ttu-id="a4170-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a4170-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="a4170-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4170-200">Classes used in</span></span>        | [<span data-ttu-id="a4170-201">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="a4170-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a4170-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4170-202">Windows Server 2008</span></span>



| <span data-ttu-id="a4170-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-203">Entry</span></span> | <span data-ttu-id="a4170-204">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a4170-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4170-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4170-207">System-Only</span></span>            | <span data-ttu-id="a4170-208">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-208">False</span></span>                                                        |
| <span data-ttu-id="a4170-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4170-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a4170-210">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-210">False</span></span>                                                        |
| <span data-ttu-id="a4170-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4170-211">Is Indexed</span></span>             | <span data-ttu-id="a4170-212">True</span><span class="sxs-lookup"><span data-stu-id="a4170-212">True</span></span>                                                         |
| <span data-ttu-id="a4170-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4170-213">In Global Catalog</span></span>      | <span data-ttu-id="a4170-214">True</span><span class="sxs-lookup"><span data-stu-id="a4170-214">True</span></span>                                                         |
| <span data-ttu-id="a4170-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4170-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4170-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4170-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a4170-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4170-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4170-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-219">Search-Flags</span></span>           | <span data-ttu-id="a4170-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4170-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="a4170-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-221">System-Flags</span></span>           | <span data-ttu-id="a4170-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a4170-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="a4170-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4170-223">Classes used in</span></span>        | [<span data-ttu-id="a4170-224">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="a4170-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4170-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4170-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4170-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-226">Entry</span></span> | <span data-ttu-id="a4170-227">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a4170-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4170-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4170-230">System-Only</span></span>            | <span data-ttu-id="a4170-231">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-231">False</span></span>                                                        |
| <span data-ttu-id="a4170-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4170-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a4170-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-233">False</span></span>                                                        |
| <span data-ttu-id="a4170-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4170-234">Is Indexed</span></span>             | <span data-ttu-id="a4170-235">True</span><span class="sxs-lookup"><span data-stu-id="a4170-235">True</span></span>                                                         |
| <span data-ttu-id="a4170-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4170-236">In Global Catalog</span></span>      | <span data-ttu-id="a4170-237">True</span><span class="sxs-lookup"><span data-stu-id="a4170-237">True</span></span>                                                         |
| <span data-ttu-id="a4170-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4170-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4170-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4170-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a4170-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4170-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4170-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-242">Search-Flags</span></span>           | <span data-ttu-id="a4170-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4170-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="a4170-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-244">System-Flags</span></span>           | <span data-ttu-id="a4170-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a4170-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="a4170-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4170-246">Classes used in</span></span>        | [<span data-ttu-id="a4170-247">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="a4170-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a4170-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4170-248">Windows Server 2012</span></span>



| <span data-ttu-id="a4170-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4170-249">Entry</span></span> | <span data-ttu-id="a4170-250">Valor</span><span class="sxs-lookup"><span data-stu-id="a4170-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a4170-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="a4170-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4170-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="a4170-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4170-253">System-Only</span></span>            | <span data-ttu-id="a4170-254">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-254">False</span></span>                                                        |
| <span data-ttu-id="a4170-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a4170-255">Is-Single-Valued</span></span>       | <span data-ttu-id="a4170-256">Falso</span><span class="sxs-lookup"><span data-stu-id="a4170-256">False</span></span>                                                        |
| <span data-ttu-id="a4170-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="a4170-257">Is Indexed</span></span>             | <span data-ttu-id="a4170-258">True</span><span class="sxs-lookup"><span data-stu-id="a4170-258">True</span></span>                                                         |
| <span data-ttu-id="a4170-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4170-259">In Global Catalog</span></span>      | <span data-ttu-id="a4170-260">True</span><span class="sxs-lookup"><span data-stu-id="a4170-260">True</span></span>                                                         |
| <span data-ttu-id="a4170-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a4170-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4170-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a4170-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="a4170-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4170-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4170-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="a4170-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-265">Search-Flags</span></span>           | <span data-ttu-id="a4170-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a4170-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="a4170-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4170-267">System-Flags</span></span>           | <span data-ttu-id="a4170-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a4170-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="a4170-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a4170-269">Classes used in</span></span>        | [<span data-ttu-id="a4170-270">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="a4170-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





