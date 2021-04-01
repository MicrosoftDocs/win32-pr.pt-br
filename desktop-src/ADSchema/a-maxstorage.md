---
title: Max-Storage atributo
description: A quantidade máxima de espaço em disco que o usuário pode usar. Use o valor especificado no usuário \_ MAXSTORAGE \_ ilimitado para usar todo o espaço em disco disponível.
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- Esquema de Max-Storage do atributo AD
- Esquema de AD do atributo maxStorage
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825233"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="de5ea-106">Max-Storage atributo</span><span class="sxs-lookup"><span data-stu-id="de5ea-106">Max-Storage attribute</span></span>

<span data-ttu-id="de5ea-107">A quantidade máxima de espaço em disco que o usuário pode usar.</span><span class="sxs-lookup"><span data-stu-id="de5ea-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="de5ea-108">Use o valor especificado no usuário \_ MAXSTORAGE \_ ilimitado para usar todo o espaço em disco disponível.</span><span class="sxs-lookup"><span data-stu-id="de5ea-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="de5ea-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-109">Entry</span></span> | <span data-ttu-id="de5ea-110">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="de5ea-111">CN</span><span class="sxs-lookup"><span data-stu-id="de5ea-111">CN</span></span>                | <span data-ttu-id="de5ea-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="de5ea-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="de5ea-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="de5ea-113">Ldap-Display-Name</span></span> | <span data-ttu-id="de5ea-114">maxStorage</span><span class="sxs-lookup"><span data-stu-id="de5ea-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="de5ea-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="de5ea-115">Size</span></span>              | <span data-ttu-id="de5ea-116">8 bytes: usuário \_ MAXSTORAGE \_ ilimitado ((não assinado longo) – 1L)</span><span class="sxs-lookup"><span data-stu-id="de5ea-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="de5ea-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="de5ea-117">Update Privilege</span></span>  | <span data-ttu-id="de5ea-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="de5ea-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="de5ea-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="de5ea-119">Update Frequency</span></span>  | <span data-ttu-id="de5ea-120">Sempre que a cota de disco precisar ser alterada.</span><span class="sxs-lookup"><span data-stu-id="de5ea-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="de5ea-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-121">Attribute-Id</span></span>      | <span data-ttu-id="de5ea-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="de5ea-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="de5ea-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="de5ea-123">System-Id-Guid</span></span>    | <span data-ttu-id="de5ea-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="de5ea-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="de5ea-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="de5ea-125">Syntax</span></span>            | [<span data-ttu-id="de5ea-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="de5ea-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="de5ea-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="de5ea-127">Implementations</span></span>

-   [<span data-ttu-id="de5ea-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="de5ea-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="de5ea-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="de5ea-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="de5ea-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="de5ea-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="de5ea-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de5ea-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de5ea-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de5ea-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de5ea-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de5ea-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="de5ea-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de5ea-134">Windows 2000 Server</span></span>



| <span data-ttu-id="de5ea-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-135">Entry</span></span> | <span data-ttu-id="de5ea-136">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de5ea-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="de5ea-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="de5ea-139">System-Only</span></span>            | <span data-ttu-id="de5ea-140">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-140">False</span></span>                             |
| <span data-ttu-id="de5ea-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="de5ea-141">Is-Single-Valued</span></span>       | <span data-ttu-id="de5ea-142">True</span><span class="sxs-lookup"><span data-stu-id="de5ea-142">True</span></span>                              |
| <span data-ttu-id="de5ea-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="de5ea-143">Is Indexed</span></span>             | <span data-ttu-id="de5ea-144">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-144">False</span></span>                             |
| <span data-ttu-id="de5ea-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="de5ea-145">In Global Catalog</span></span>      | <span data-ttu-id="de5ea-146">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-146">False</span></span>                             |
| <span data-ttu-id="de5ea-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="de5ea-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="de5ea-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="de5ea-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de5ea-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de5ea-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de5ea-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de5ea-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de5ea-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-151">Search-Flags</span></span>           | <span data-ttu-id="de5ea-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-152">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-153">System-Flags</span></span>           | <span data-ttu-id="de5ea-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-154">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="de5ea-155">Classes used in</span></span>        | [<span data-ttu-id="de5ea-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="de5ea-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="de5ea-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de5ea-157">Windows Server 2003</span></span>



| <span data-ttu-id="de5ea-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-158">Entry</span></span> | <span data-ttu-id="de5ea-159">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de5ea-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="de5ea-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="de5ea-162">System-Only</span></span>            | <span data-ttu-id="de5ea-163">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-163">False</span></span>                             |
| <span data-ttu-id="de5ea-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="de5ea-164">Is-Single-Valued</span></span>       | <span data-ttu-id="de5ea-165">True</span><span class="sxs-lookup"><span data-stu-id="de5ea-165">True</span></span>                              |
| <span data-ttu-id="de5ea-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="de5ea-166">Is Indexed</span></span>             | <span data-ttu-id="de5ea-167">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-167">False</span></span>                             |
| <span data-ttu-id="de5ea-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="de5ea-168">In Global Catalog</span></span>      | <span data-ttu-id="de5ea-169">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-169">False</span></span>                             |
| <span data-ttu-id="de5ea-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="de5ea-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="de5ea-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="de5ea-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de5ea-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de5ea-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de5ea-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de5ea-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de5ea-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-174">Search-Flags</span></span>           | <span data-ttu-id="de5ea-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-175">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-176">System-Flags</span></span>           | <span data-ttu-id="de5ea-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-177">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="de5ea-178">Classes used in</span></span>        | [<span data-ttu-id="de5ea-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="de5ea-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="de5ea-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="de5ea-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="de5ea-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-181">Entry</span></span> | <span data-ttu-id="de5ea-182">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de5ea-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="de5ea-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="de5ea-185">System-Only</span></span>            | <span data-ttu-id="de5ea-186">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-186">False</span></span>                             |
| <span data-ttu-id="de5ea-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="de5ea-187">Is-Single-Valued</span></span>       | <span data-ttu-id="de5ea-188">True</span><span class="sxs-lookup"><span data-stu-id="de5ea-188">True</span></span>                              |
| <span data-ttu-id="de5ea-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="de5ea-189">Is Indexed</span></span>             | <span data-ttu-id="de5ea-190">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-190">False</span></span>                             |
| <span data-ttu-id="de5ea-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="de5ea-191">In Global Catalog</span></span>      | <span data-ttu-id="de5ea-192">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-192">False</span></span>                             |
| <span data-ttu-id="de5ea-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="de5ea-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="de5ea-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="de5ea-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de5ea-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de5ea-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de5ea-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de5ea-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de5ea-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-197">Search-Flags</span></span>           | <span data-ttu-id="de5ea-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-198">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-199">System-Flags</span></span>           | <span data-ttu-id="de5ea-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-200">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="de5ea-201">Classes used in</span></span>        | [<span data-ttu-id="de5ea-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="de5ea-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="de5ea-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de5ea-203">Windows Server 2008</span></span>



| <span data-ttu-id="de5ea-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-204">Entry</span></span> | <span data-ttu-id="de5ea-205">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de5ea-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="de5ea-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="de5ea-208">System-Only</span></span>            | <span data-ttu-id="de5ea-209">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-209">False</span></span>                             |
| <span data-ttu-id="de5ea-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="de5ea-210">Is-Single-Valued</span></span>       | <span data-ttu-id="de5ea-211">True</span><span class="sxs-lookup"><span data-stu-id="de5ea-211">True</span></span>                              |
| <span data-ttu-id="de5ea-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="de5ea-212">Is Indexed</span></span>             | <span data-ttu-id="de5ea-213">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-213">False</span></span>                             |
| <span data-ttu-id="de5ea-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="de5ea-214">In Global Catalog</span></span>      | <span data-ttu-id="de5ea-215">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-215">False</span></span>                             |
| <span data-ttu-id="de5ea-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="de5ea-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="de5ea-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="de5ea-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de5ea-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de5ea-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de5ea-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de5ea-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de5ea-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-220">Search-Flags</span></span>           | <span data-ttu-id="de5ea-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-221">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-222">System-Flags</span></span>           | <span data-ttu-id="de5ea-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-223">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="de5ea-224">Classes used in</span></span>        | [<span data-ttu-id="de5ea-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="de5ea-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de5ea-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de5ea-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de5ea-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-227">Entry</span></span> | <span data-ttu-id="de5ea-228">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de5ea-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="de5ea-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="de5ea-231">System-Only</span></span>            | <span data-ttu-id="de5ea-232">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-232">False</span></span>                             |
| <span data-ttu-id="de5ea-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="de5ea-233">Is-Single-Valued</span></span>       | <span data-ttu-id="de5ea-234">True</span><span class="sxs-lookup"><span data-stu-id="de5ea-234">True</span></span>                              |
| <span data-ttu-id="de5ea-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="de5ea-235">Is Indexed</span></span>             | <span data-ttu-id="de5ea-236">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-236">False</span></span>                             |
| <span data-ttu-id="de5ea-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="de5ea-237">In Global Catalog</span></span>      | <span data-ttu-id="de5ea-238">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-238">False</span></span>                             |
| <span data-ttu-id="de5ea-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="de5ea-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="de5ea-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="de5ea-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de5ea-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de5ea-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de5ea-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de5ea-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de5ea-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-243">Search-Flags</span></span>           | <span data-ttu-id="de5ea-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-244">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-245">System-Flags</span></span>           | <span data-ttu-id="de5ea-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-246">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="de5ea-247">Classes used in</span></span>        | [<span data-ttu-id="de5ea-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="de5ea-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de5ea-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de5ea-249">Windows Server 2012</span></span>



| <span data-ttu-id="de5ea-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="de5ea-250">Entry</span></span> | <span data-ttu-id="de5ea-251">Valor</span><span class="sxs-lookup"><span data-stu-id="de5ea-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="de5ea-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="de5ea-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de5ea-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="de5ea-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="de5ea-254">System-Only</span></span>            | <span data-ttu-id="de5ea-255">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-255">False</span></span>                             |
| <span data-ttu-id="de5ea-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="de5ea-256">Is-Single-Valued</span></span>       | <span data-ttu-id="de5ea-257">True</span><span class="sxs-lookup"><span data-stu-id="de5ea-257">True</span></span>                              |
| <span data-ttu-id="de5ea-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="de5ea-258">Is Indexed</span></span>             | <span data-ttu-id="de5ea-259">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-259">False</span></span>                             |
| <span data-ttu-id="de5ea-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="de5ea-260">In Global Catalog</span></span>      | <span data-ttu-id="de5ea-261">Falso</span><span class="sxs-lookup"><span data-stu-id="de5ea-261">False</span></span>                             |
| <span data-ttu-id="de5ea-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="de5ea-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="de5ea-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="de5ea-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="de5ea-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de5ea-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="de5ea-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de5ea-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="de5ea-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-266">Search-Flags</span></span>           | <span data-ttu-id="de5ea-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-267">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de5ea-268">System-Flags</span></span>           | <span data-ttu-id="de5ea-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="de5ea-269">0x00000010</span></span>                        |
| <span data-ttu-id="de5ea-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="de5ea-270">Classes used in</span></span>        | [<span data-ttu-id="de5ea-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="de5ea-271">**User**</span></span>](c-user.md)<br/> |



 

 





