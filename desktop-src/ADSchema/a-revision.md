---
title: Atributo de revisão
description: O nível de revisão para um descritor de segurança ou outra alteração. Usado somente nos objetos Sam-Server e DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de revisão
- Esquema de AD do atributo de revisão
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499954"
---
# <a name="revision-attribute"></a><span data-ttu-id="7d194-106">Atributo de revisão</span><span class="sxs-lookup"><span data-stu-id="7d194-106">Revision attribute</span></span>

<span data-ttu-id="7d194-107">O nível de revisão para um descritor de segurança ou outra alteração.</span><span class="sxs-lookup"><span data-stu-id="7d194-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="7d194-108">Usado somente nos objetos Sam-Server e DS-UI-Settings.</span><span class="sxs-lookup"><span data-stu-id="7d194-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="7d194-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-109">Entry</span></span> | <span data-ttu-id="7d194-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7d194-111">CN</span><span class="sxs-lookup"><span data-stu-id="7d194-111">CN</span></span>                | <span data-ttu-id="7d194-112">Revisão</span><span class="sxs-lookup"><span data-stu-id="7d194-112">Revision</span></span>                             |
| <span data-ttu-id="7d194-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7d194-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7d194-114">revisão</span><span class="sxs-lookup"><span data-stu-id="7d194-114">revision</span></span>                             |
| <span data-ttu-id="7d194-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7d194-115">Size</span></span>              | <span data-ttu-id="7d194-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="7d194-116">4 bytes</span></span>                              |
| <span data-ttu-id="7d194-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7d194-117">Update Privilege</span></span>  | <span data-ttu-id="7d194-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7d194-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="7d194-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7d194-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7d194-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-120">Attribute-Id</span></span>      | <span data-ttu-id="7d194-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="7d194-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="7d194-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7d194-122">System-Id-Guid</span></span>    | <span data-ttu-id="7d194-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7d194-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7d194-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d194-124">Syntax</span></span>            | [<span data-ttu-id="7d194-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="7d194-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7d194-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="7d194-126">Implementations</span></span>

-   [<span data-ttu-id="7d194-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7d194-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7d194-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7d194-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7d194-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7d194-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7d194-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7d194-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7d194-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7d194-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7d194-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7d194-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7d194-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7d194-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7d194-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d194-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7d194-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-135">Entry</span></span> | <span data-ttu-id="7d194-136">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-139">System-Only</span></span>            | <span data-ttu-id="7d194-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-140">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-142">True</span><span class="sxs-lookup"><span data-stu-id="7d194-142">True</span></span>                                                                                  |
| <span data-ttu-id="7d194-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-143">Is Indexed</span></span>             | <span data-ttu-id="7d194-144">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-144">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-145">In Global Catalog</span></span>      | <span data-ttu-id="7d194-146">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-146">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="7d194-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-151">Search-Flags</span></span>           | <span data-ttu-id="7d194-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="7d194-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-153">System-Flags</span></span>           | <span data-ttu-id="7d194-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="7d194-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-155">Classes used in</span></span>        | [<span data-ttu-id="7d194-156">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="7d194-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="7d194-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7d194-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d194-158">Windows Server 2003</span></span>



| <span data-ttu-id="7d194-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-159">Entry</span></span> | <span data-ttu-id="7d194-160">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-163">System-Only</span></span>            | <span data-ttu-id="7d194-164">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-164">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-165">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-166">True</span><span class="sxs-lookup"><span data-stu-id="7d194-166">True</span></span>                                                                                  |
| <span data-ttu-id="7d194-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-167">Is Indexed</span></span>             | <span data-ttu-id="7d194-168">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-168">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-169">In Global Catalog</span></span>      | <span data-ttu-id="7d194-170">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-170">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="7d194-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-175">Search-Flags</span></span>           | <span data-ttu-id="7d194-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="7d194-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-177">System-Flags</span></span>           | <span data-ttu-id="7d194-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="7d194-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-179">Classes used in</span></span>        | [<span data-ttu-id="7d194-180">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="7d194-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="7d194-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7d194-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="7d194-182">ADAM</span></span>



| <span data-ttu-id="7d194-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-183">Entry</span></span> | <span data-ttu-id="7d194-184">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7d194-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7d194-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7d194-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-187">System-Only</span></span>            | <span data-ttu-id="7d194-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-188">False</span></span>                           |
| <span data-ttu-id="7d194-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-189">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-190">True</span><span class="sxs-lookup"><span data-stu-id="7d194-190">True</span></span>                            |
| <span data-ttu-id="7d194-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-191">Is Indexed</span></span>             | <span data-ttu-id="7d194-192">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-192">False</span></span>                           |
| <span data-ttu-id="7d194-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-193">In Global Catalog</span></span>      | <span data-ttu-id="7d194-194">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-194">False</span></span>                           |
| <span data-ttu-id="7d194-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7d194-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7d194-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7d194-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-199">Search-Flags</span></span>           | <span data-ttu-id="7d194-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-200">0x00000000</span></span>                      |
| <span data-ttu-id="7d194-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-201">System-Flags</span></span>           | <span data-ttu-id="7d194-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-202">0x00000010</span></span>                      |
| <span data-ttu-id="7d194-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-203">Classes used in</span></span>        | [<span data-ttu-id="7d194-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7d194-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7d194-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7d194-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-206">Entry</span></span> | <span data-ttu-id="7d194-207">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-210">System-Only</span></span>            | <span data-ttu-id="7d194-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-211">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-213">True</span><span class="sxs-lookup"><span data-stu-id="7d194-213">True</span></span>                                                                                  |
| <span data-ttu-id="7d194-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-214">Is Indexed</span></span>             | <span data-ttu-id="7d194-215">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-215">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-216">In Global Catalog</span></span>      | <span data-ttu-id="7d194-217">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-217">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="7d194-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-222">Search-Flags</span></span>           | <span data-ttu-id="7d194-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="7d194-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-224">System-Flags</span></span>           | <span data-ttu-id="7d194-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="7d194-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-226">Classes used in</span></span>        | [<span data-ttu-id="7d194-227">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="7d194-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="7d194-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7d194-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d194-229">Windows Server 2008</span></span>



| <span data-ttu-id="7d194-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-230">Entry</span></span> | <span data-ttu-id="7d194-231">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-234">System-Only</span></span>            | <span data-ttu-id="7d194-235">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-235">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-236">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-237">True</span><span class="sxs-lookup"><span data-stu-id="7d194-237">True</span></span>                                                                                  |
| <span data-ttu-id="7d194-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-238">Is Indexed</span></span>             | <span data-ttu-id="7d194-239">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-239">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-240">In Global Catalog</span></span>      | <span data-ttu-id="7d194-241">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-241">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="7d194-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-246">Search-Flags</span></span>           | <span data-ttu-id="7d194-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="7d194-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-248">System-Flags</span></span>           | <span data-ttu-id="7d194-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="7d194-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-250">Classes used in</span></span>        | [<span data-ttu-id="7d194-251">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="7d194-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="7d194-252">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7d194-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d194-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7d194-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-254">Entry</span></span> | <span data-ttu-id="7d194-255">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-258">System-Only</span></span>            | <span data-ttu-id="7d194-259">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-259">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-260">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-260">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-261">True</span><span class="sxs-lookup"><span data-stu-id="7d194-261">True</span></span>                                                                                  |
| <span data-ttu-id="7d194-262">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-262">Is Indexed</span></span>             | <span data-ttu-id="7d194-263">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-263">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-264">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-264">In Global Catalog</span></span>      | <span data-ttu-id="7d194-265">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-265">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-266">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-267">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="7d194-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-270">Search-Flags</span></span>           | <span data-ttu-id="7d194-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="7d194-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-272">System-Flags</span></span>           | <span data-ttu-id="7d194-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="7d194-274">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-274">Classes used in</span></span>        | [<span data-ttu-id="7d194-275">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="7d194-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="7d194-276">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7d194-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d194-277">Windows Server 2012</span></span>



| <span data-ttu-id="7d194-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d194-278">Entry</span></span> | <span data-ttu-id="7d194-279">Valor</span><span class="sxs-lookup"><span data-stu-id="7d194-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="7d194-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d194-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="7d194-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d194-282">System-Only</span></span>            | <span data-ttu-id="7d194-283">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-283">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-284">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7d194-284">Is-Single-Valued</span></span>       | <span data-ttu-id="7d194-285">True</span><span class="sxs-lookup"><span data-stu-id="7d194-285">True</span></span>                                                                                  |
| <span data-ttu-id="7d194-286">É indexado</span><span class="sxs-lookup"><span data-stu-id="7d194-286">Is Indexed</span></span>             | <span data-ttu-id="7d194-287">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-287">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-288">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7d194-288">In Global Catalog</span></span>      | <span data-ttu-id="7d194-289">Falso</span><span class="sxs-lookup"><span data-stu-id="7d194-289">False</span></span>                                                                                 |
| <span data-ttu-id="7d194-290">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7d194-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d194-291">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7d194-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="7d194-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d194-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d194-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="7d194-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-294">Search-Flags</span></span>           | <span data-ttu-id="7d194-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d194-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="7d194-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d194-296">System-Flags</span></span>           | <span data-ttu-id="7d194-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d194-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="7d194-298">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7d194-298">Classes used in</span></span>        | [<span data-ttu-id="7d194-299">**Sam-domínio-base**</span><span class="sxs-lookup"><span data-stu-id="7d194-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="7d194-300">**Início**</span><span class="sxs-lookup"><span data-stu-id="7d194-300">**Top**</span></span>](c-top.md)<br/> |



 

 





