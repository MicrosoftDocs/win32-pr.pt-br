---
title: Help-Data32 atributo
description: Esse atributo foi usado para o formato de arquivo de ajuda do Win32 para o Exchange 4,0. Ele não é usado para nenhuma outra versão do Exchange.
ms.assetid: 33e64ff9-7cb4-43a6-8d7b-1c5e925b783c
ms.tgt_platform: multiple
keywords:
- Esquema de Help-Data32 do atributo AD
- Esquema de AD do atributo helpData32
topic_type:
- apiref
api_name:
- Help-Data32
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32debc8c72c95313b8da6288e0d31f5713a4205a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754841"
---
# <a name="help-data32-attribute"></a><span data-ttu-id="66fc8-106">Help-Data32 atributo</span><span class="sxs-lookup"><span data-stu-id="66fc8-106">Help-Data32 attribute</span></span>

<span data-ttu-id="66fc8-107">Esse atributo foi usado para o formato de arquivo de ajuda do Win32 para o Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="66fc8-107">This attribute was used for the Win32 help file format for Exchange 4.0.</span></span> <span data-ttu-id="66fc8-108">Ele não é usado para nenhuma outra versão do Exchange.</span><span class="sxs-lookup"><span data-stu-id="66fc8-108">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="66fc8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-109">Entry</span></span> | <span data-ttu-id="66fc8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="66fc8-111">CN</span><span class="sxs-lookup"><span data-stu-id="66fc8-111">CN</span></span>                | <span data-ttu-id="66fc8-112">Help-Data32</span><span class="sxs-lookup"><span data-stu-id="66fc8-112">Help-Data32</span></span>                                           |
| <span data-ttu-id="66fc8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="66fc8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="66fc8-114">helpData32</span><span class="sxs-lookup"><span data-stu-id="66fc8-114">helpData32</span></span>                                            |
| <span data-ttu-id="66fc8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="66fc8-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="66fc8-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="66fc8-116">Update Privilege</span></span>  | <span data-ttu-id="66fc8-117">Isso é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="66fc8-117">This is used by the system.</span></span>                           |
| <span data-ttu-id="66fc8-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="66fc8-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="66fc8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-119">Attribute-Id</span></span>      | <span data-ttu-id="66fc8-120">1.2.840.113556.1.2.9</span><span class="sxs-lookup"><span data-stu-id="66fc8-120">1.2.840.113556.1.2.9</span></span>                                  |
| <span data-ttu-id="66fc8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="66fc8-121">System-Id-Guid</span></span>    | <span data-ttu-id="66fc8-122">5fd424a8-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="66fc8-122">5fd424a8-1262-11d0-a060-00aa006c33ed</span></span>                  |
| <span data-ttu-id="66fc8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="66fc8-123">Syntax</span></span>            | [<span data-ttu-id="66fc8-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="66fc8-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="66fc8-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="66fc8-125">Implementations</span></span>

-   [<span data-ttu-id="66fc8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="66fc8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="66fc8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="66fc8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="66fc8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="66fc8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="66fc8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="66fc8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="66fc8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="66fc8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="66fc8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66fc8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="66fc8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66fc8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="66fc8-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-133">Entry</span></span> | <span data-ttu-id="66fc8-134">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="66fc8-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="66fc8-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="66fc8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-136">MAPI-Id</span></span>                | <span data-ttu-id="66fc8-137">0x8010</span><span class="sxs-lookup"><span data-stu-id="66fc8-137">0x8010</span></span>                                                   |
| <span data-ttu-id="66fc8-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="66fc8-138">System-Only</span></span>            | <span data-ttu-id="66fc8-139">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-139">False</span></span>                                                    |
| <span data-ttu-id="66fc8-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="66fc8-140">Is-Single-Valued</span></span>       | <span data-ttu-id="66fc8-141">True</span><span class="sxs-lookup"><span data-stu-id="66fc8-141">True</span></span>                                                     |
| <span data-ttu-id="66fc8-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="66fc8-142">Is Indexed</span></span>             | <span data-ttu-id="66fc8-143">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-143">False</span></span>                                                    |
| <span data-ttu-id="66fc8-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="66fc8-144">In Global Catalog</span></span>      | <span data-ttu-id="66fc8-145">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-145">False</span></span>                                                    |
| <span data-ttu-id="66fc8-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="66fc8-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="66fc8-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="66fc8-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="66fc8-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66fc8-148">Range-Lower</span></span>            | <span data-ttu-id="66fc8-149">1</span><span class="sxs-lookup"><span data-stu-id="66fc8-149">1</span></span>                                                        |
| <span data-ttu-id="66fc8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66fc8-150">Range-Upper</span></span>            | <span data-ttu-id="66fc8-151">32768</span><span class="sxs-lookup"><span data-stu-id="66fc8-151">32768</span></span>                                                    |
| <span data-ttu-id="66fc8-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-152">Search-Flags</span></span>           | <span data-ttu-id="66fc8-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66fc8-153">0x00000000</span></span>                                               |
| <span data-ttu-id="66fc8-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-154">System-Flags</span></span>           | <span data-ttu-id="66fc8-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66fc8-155">0x00000010</span></span>                                               |
| <span data-ttu-id="66fc8-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="66fc8-156">Classes used in</span></span>        | [<span data-ttu-id="66fc8-157">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="66fc8-157">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="66fc8-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66fc8-158">Windows Server 2003</span></span>



| <span data-ttu-id="66fc8-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-159">Entry</span></span> | <span data-ttu-id="66fc8-160">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-160">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="66fc8-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="66fc8-161">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="66fc8-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-162">MAPI-Id</span></span>                | <span data-ttu-id="66fc8-163">0x8010</span><span class="sxs-lookup"><span data-stu-id="66fc8-163">0x8010</span></span>                                                   |
| <span data-ttu-id="66fc8-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="66fc8-164">System-Only</span></span>            | <span data-ttu-id="66fc8-165">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-165">False</span></span>                                                    |
| <span data-ttu-id="66fc8-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="66fc8-166">Is-Single-Valued</span></span>       | <span data-ttu-id="66fc8-167">True</span><span class="sxs-lookup"><span data-stu-id="66fc8-167">True</span></span>                                                     |
| <span data-ttu-id="66fc8-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="66fc8-168">Is Indexed</span></span>             | <span data-ttu-id="66fc8-169">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-169">False</span></span>                                                    |
| <span data-ttu-id="66fc8-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="66fc8-170">In Global Catalog</span></span>      | <span data-ttu-id="66fc8-171">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-171">False</span></span>                                                    |
| <span data-ttu-id="66fc8-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="66fc8-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="66fc8-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="66fc8-173">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="66fc8-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66fc8-174">Range-Lower</span></span>            | <span data-ttu-id="66fc8-175">1</span><span class="sxs-lookup"><span data-stu-id="66fc8-175">1</span></span>                                                        |
| <span data-ttu-id="66fc8-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66fc8-176">Range-Upper</span></span>            | <span data-ttu-id="66fc8-177">32768</span><span class="sxs-lookup"><span data-stu-id="66fc8-177">32768</span></span>                                                    |
| <span data-ttu-id="66fc8-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-178">Search-Flags</span></span>           | <span data-ttu-id="66fc8-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66fc8-179">0x00000000</span></span>                                               |
| <span data-ttu-id="66fc8-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-180">System-Flags</span></span>           | <span data-ttu-id="66fc8-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66fc8-181">0x00000010</span></span>                                               |
| <span data-ttu-id="66fc8-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="66fc8-182">Classes used in</span></span>        | [<span data-ttu-id="66fc8-183">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="66fc8-183">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="66fc8-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="66fc8-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="66fc8-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-185">Entry</span></span> | <span data-ttu-id="66fc8-186">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-186">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="66fc8-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="66fc8-187">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="66fc8-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-188">MAPI-Id</span></span>                | <span data-ttu-id="66fc8-189">0x8010</span><span class="sxs-lookup"><span data-stu-id="66fc8-189">0x8010</span></span>                                                   |
| <span data-ttu-id="66fc8-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="66fc8-190">System-Only</span></span>            | <span data-ttu-id="66fc8-191">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-191">False</span></span>                                                    |
| <span data-ttu-id="66fc8-192">É de valor único</span><span class="sxs-lookup"><span data-stu-id="66fc8-192">Is-Single-Valued</span></span>       | <span data-ttu-id="66fc8-193">True</span><span class="sxs-lookup"><span data-stu-id="66fc8-193">True</span></span>                                                     |
| <span data-ttu-id="66fc8-194">É indexado</span><span class="sxs-lookup"><span data-stu-id="66fc8-194">Is Indexed</span></span>             | <span data-ttu-id="66fc8-195">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-195">False</span></span>                                                    |
| <span data-ttu-id="66fc8-196">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="66fc8-196">In Global Catalog</span></span>      | <span data-ttu-id="66fc8-197">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-197">False</span></span>                                                    |
| <span data-ttu-id="66fc8-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="66fc8-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="66fc8-199">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="66fc8-199">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="66fc8-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66fc8-200">Range-Lower</span></span>            | <span data-ttu-id="66fc8-201">1</span><span class="sxs-lookup"><span data-stu-id="66fc8-201">1</span></span>                                                        |
| <span data-ttu-id="66fc8-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66fc8-202">Range-Upper</span></span>            | <span data-ttu-id="66fc8-203">32768</span><span class="sxs-lookup"><span data-stu-id="66fc8-203">32768</span></span>                                                    |
| <span data-ttu-id="66fc8-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-204">Search-Flags</span></span>           | <span data-ttu-id="66fc8-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66fc8-205">0x00000000</span></span>                                               |
| <span data-ttu-id="66fc8-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-206">System-Flags</span></span>           | <span data-ttu-id="66fc8-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66fc8-207">0x00000010</span></span>                                               |
| <span data-ttu-id="66fc8-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="66fc8-208">Classes used in</span></span>        | [<span data-ttu-id="66fc8-209">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="66fc8-209">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="66fc8-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66fc8-210">Windows Server 2008</span></span>



| <span data-ttu-id="66fc8-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-211">Entry</span></span> | <span data-ttu-id="66fc8-212">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-212">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="66fc8-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="66fc8-213">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="66fc8-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-214">MAPI-Id</span></span>                | <span data-ttu-id="66fc8-215">0x8010</span><span class="sxs-lookup"><span data-stu-id="66fc8-215">0x8010</span></span>                                                   |
| <span data-ttu-id="66fc8-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="66fc8-216">System-Only</span></span>            | <span data-ttu-id="66fc8-217">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-217">False</span></span>                                                    |
| <span data-ttu-id="66fc8-218">É de valor único</span><span class="sxs-lookup"><span data-stu-id="66fc8-218">Is-Single-Valued</span></span>       | <span data-ttu-id="66fc8-219">True</span><span class="sxs-lookup"><span data-stu-id="66fc8-219">True</span></span>                                                     |
| <span data-ttu-id="66fc8-220">É indexado</span><span class="sxs-lookup"><span data-stu-id="66fc8-220">Is Indexed</span></span>             | <span data-ttu-id="66fc8-221">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-221">False</span></span>                                                    |
| <span data-ttu-id="66fc8-222">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="66fc8-222">In Global Catalog</span></span>      | <span data-ttu-id="66fc8-223">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-223">False</span></span>                                                    |
| <span data-ttu-id="66fc8-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="66fc8-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="66fc8-225">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="66fc8-225">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="66fc8-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66fc8-226">Range-Lower</span></span>            | <span data-ttu-id="66fc8-227">1</span><span class="sxs-lookup"><span data-stu-id="66fc8-227">1</span></span>                                                        |
| <span data-ttu-id="66fc8-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66fc8-228">Range-Upper</span></span>            | <span data-ttu-id="66fc8-229">32768</span><span class="sxs-lookup"><span data-stu-id="66fc8-229">32768</span></span>                                                    |
| <span data-ttu-id="66fc8-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-230">Search-Flags</span></span>           | <span data-ttu-id="66fc8-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66fc8-231">0x00000000</span></span>                                               |
| <span data-ttu-id="66fc8-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-232">System-Flags</span></span>           | <span data-ttu-id="66fc8-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66fc8-233">0x00000010</span></span>                                               |
| <span data-ttu-id="66fc8-234">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="66fc8-234">Classes used in</span></span>        | [<span data-ttu-id="66fc8-235">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="66fc8-235">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="66fc8-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66fc8-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="66fc8-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-237">Entry</span></span> | <span data-ttu-id="66fc8-238">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-238">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="66fc8-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="66fc8-239">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="66fc8-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-240">MAPI-Id</span></span>                | <span data-ttu-id="66fc8-241">0x8010</span><span class="sxs-lookup"><span data-stu-id="66fc8-241">0x8010</span></span>                                                   |
| <span data-ttu-id="66fc8-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="66fc8-242">System-Only</span></span>            | <span data-ttu-id="66fc8-243">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-243">False</span></span>                                                    |
| <span data-ttu-id="66fc8-244">É de valor único</span><span class="sxs-lookup"><span data-stu-id="66fc8-244">Is-Single-Valued</span></span>       | <span data-ttu-id="66fc8-245">True</span><span class="sxs-lookup"><span data-stu-id="66fc8-245">True</span></span>                                                     |
| <span data-ttu-id="66fc8-246">É indexado</span><span class="sxs-lookup"><span data-stu-id="66fc8-246">Is Indexed</span></span>             | <span data-ttu-id="66fc8-247">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-247">False</span></span>                                                    |
| <span data-ttu-id="66fc8-248">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="66fc8-248">In Global Catalog</span></span>      | <span data-ttu-id="66fc8-249">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-249">False</span></span>                                                    |
| <span data-ttu-id="66fc8-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="66fc8-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="66fc8-251">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="66fc8-251">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="66fc8-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66fc8-252">Range-Lower</span></span>            | <span data-ttu-id="66fc8-253">1</span><span class="sxs-lookup"><span data-stu-id="66fc8-253">1</span></span>                                                        |
| <span data-ttu-id="66fc8-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66fc8-254">Range-Upper</span></span>            | <span data-ttu-id="66fc8-255">32768</span><span class="sxs-lookup"><span data-stu-id="66fc8-255">32768</span></span>                                                    |
| <span data-ttu-id="66fc8-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-256">Search-Flags</span></span>           | <span data-ttu-id="66fc8-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66fc8-257">0x00000000</span></span>                                               |
| <span data-ttu-id="66fc8-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-258">System-Flags</span></span>           | <span data-ttu-id="66fc8-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66fc8-259">0x00000010</span></span>                                               |
| <span data-ttu-id="66fc8-260">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="66fc8-260">Classes used in</span></span>        | [<span data-ttu-id="66fc8-261">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="66fc8-261">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="66fc8-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66fc8-262">Windows Server 2012</span></span>



| <span data-ttu-id="66fc8-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="66fc8-263">Entry</span></span> | <span data-ttu-id="66fc8-264">Valor</span><span class="sxs-lookup"><span data-stu-id="66fc8-264">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="66fc8-265">ID do link</span><span class="sxs-lookup"><span data-stu-id="66fc8-265">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="66fc8-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66fc8-266">MAPI-Id</span></span>                | <span data-ttu-id="66fc8-267">0x8010</span><span class="sxs-lookup"><span data-stu-id="66fc8-267">0x8010</span></span>                                                   |
| <span data-ttu-id="66fc8-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="66fc8-268">System-Only</span></span>            | <span data-ttu-id="66fc8-269">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-269">False</span></span>                                                    |
| <span data-ttu-id="66fc8-270">É de valor único</span><span class="sxs-lookup"><span data-stu-id="66fc8-270">Is-Single-Valued</span></span>       | <span data-ttu-id="66fc8-271">True</span><span class="sxs-lookup"><span data-stu-id="66fc8-271">True</span></span>                                                     |
| <span data-ttu-id="66fc8-272">É indexado</span><span class="sxs-lookup"><span data-stu-id="66fc8-272">Is Indexed</span></span>             | <span data-ttu-id="66fc8-273">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-273">False</span></span>                                                    |
| <span data-ttu-id="66fc8-274">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="66fc8-274">In Global Catalog</span></span>      | <span data-ttu-id="66fc8-275">Falso</span><span class="sxs-lookup"><span data-stu-id="66fc8-275">False</span></span>                                                    |
| <span data-ttu-id="66fc8-276">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="66fc8-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="66fc8-277">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="66fc8-277">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="66fc8-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66fc8-278">Range-Lower</span></span>            | <span data-ttu-id="66fc8-279">1</span><span class="sxs-lookup"><span data-stu-id="66fc8-279">1</span></span>                                                        |
| <span data-ttu-id="66fc8-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66fc8-280">Range-Upper</span></span>            | <span data-ttu-id="66fc8-281">32768</span><span class="sxs-lookup"><span data-stu-id="66fc8-281">32768</span></span>                                                    |
| <span data-ttu-id="66fc8-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-282">Search-Flags</span></span>           | <span data-ttu-id="66fc8-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66fc8-283">0x00000000</span></span>                                               |
| <span data-ttu-id="66fc8-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66fc8-284">System-Flags</span></span>           | <span data-ttu-id="66fc8-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66fc8-285">0x00000010</span></span>                                               |
| <span data-ttu-id="66fc8-286">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="66fc8-286">Classes used in</span></span>        | [<span data-ttu-id="66fc8-287">**Display-template**</span><span class="sxs-lookup"><span data-stu-id="66fc8-287">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





