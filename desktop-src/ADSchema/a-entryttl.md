---
title: Atributo de entrada-TTL
description: Esse atributo operacional é mantido pelo servidor e parece estar presente em todas as entradas dinâmicas.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo entry-TTL
- Esquema de AD do atributo entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456121"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="b89e4-105">Atributo de entrada-TTL</span><span class="sxs-lookup"><span data-stu-id="b89e4-105">Entry-TTL attribute</span></span>

<span data-ttu-id="b89e4-106">Esse atributo operacional é mantido pelo servidor e parece estar presente em todas as entradas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="b89e4-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="b89e4-107">O atributo não está presente quando a entrada não contém a classe de objeto DynamicObject.</span><span class="sxs-lookup"><span data-stu-id="b89e4-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="b89e4-108">O valor desse atributo é o tempo, em segundos, que a entrada continuará existindo antes de desaparecer do diretório.</span><span class="sxs-lookup"><span data-stu-id="b89e4-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="b89e4-109">Na ausência de operações intermediárias de "atualização", os valores retornados pela leitura do atributo em duas pesquisas sucessivas têm a garantia de não aumentar.</span><span class="sxs-lookup"><span data-stu-id="b89e4-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="b89e4-110">O menor valor permitido é 0, indicando que a entrada pode desaparecer sem aviso.</span><span class="sxs-lookup"><span data-stu-id="b89e4-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="b89e4-111">O atributo está marcado como não-usuário-modificação porque só pode ser alterado usando a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="b89e4-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="b89e4-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-112">Entry</span></span> | <span data-ttu-id="b89e4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b89e4-114">CN</span><span class="sxs-lookup"><span data-stu-id="b89e4-114">CN</span></span>                | <span data-ttu-id="b89e4-115">TTL da entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="b89e4-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b89e4-116">Ldap-Display-Name</span></span> | <span data-ttu-id="b89e4-117">entryTTL</span><span class="sxs-lookup"><span data-stu-id="b89e4-117">entryTTL</span></span>                                    |
| <span data-ttu-id="b89e4-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b89e4-118">Size</span></span>              | <span data-ttu-id="b89e4-119">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="b89e4-119">4 bytes.</span></span> <span data-ttu-id="b89e4-120">Máximo = 1 ano, padrão = 1 dia.</span><span class="sxs-lookup"><span data-stu-id="b89e4-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="b89e4-121">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b89e4-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b89e4-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b89e4-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b89e4-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-123">Attribute-Id</span></span>      | <span data-ttu-id="b89e4-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="b89e4-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="b89e4-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b89e4-125">System-Id-Guid</span></span>    | <span data-ttu-id="b89e4-126">d213decc-d81a-4384-AAC2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="b89e4-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="b89e4-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="b89e4-127">Syntax</span></span>            | [<span data-ttu-id="b89e4-128">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="b89e4-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="b89e4-129">Implementações</span><span class="sxs-lookup"><span data-stu-id="b89e4-129">Implementations</span></span>

-   [<span data-ttu-id="b89e4-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b89e4-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b89e4-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b89e4-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b89e4-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b89e4-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b89e4-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b89e4-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b89e4-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b89e4-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b89e4-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b89e4-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b89e4-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b89e4-136">Windows Server 2003</span></span>



| <span data-ttu-id="b89e4-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-137">Entry</span></span> | <span data-ttu-id="b89e4-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b89e4-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="b89e4-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="b89e4-141">System-Only</span></span>            | <span data-ttu-id="b89e4-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-142">False</span></span>                                                |
| <span data-ttu-id="b89e4-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b89e4-143">Is-Single-Valued</span></span>       | <span data-ttu-id="b89e4-144">True</span><span class="sxs-lookup"><span data-stu-id="b89e4-144">True</span></span>                                                 |
| <span data-ttu-id="b89e4-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="b89e4-145">Is Indexed</span></span>             | <span data-ttu-id="b89e4-146">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-146">False</span></span>                                                |
| <span data-ttu-id="b89e4-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b89e4-147">In Global Catalog</span></span>      | <span data-ttu-id="b89e4-148">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-148">False</span></span>                                                |
| <span data-ttu-id="b89e4-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b89e4-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="b89e4-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b89e4-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b89e4-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b89e4-151">Range-Lower</span></span>            | <span data-ttu-id="b89e4-152">0</span><span class="sxs-lookup"><span data-stu-id="b89e4-152">0</span></span>                                                    |
| <span data-ttu-id="b89e4-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b89e4-153">Range-Upper</span></span>            | <span data-ttu-id="b89e4-154">31557600</span><span class="sxs-lookup"><span data-stu-id="b89e4-154">31557600</span></span>                                             |
| <span data-ttu-id="b89e4-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-155">Search-Flags</span></span>           | <span data-ttu-id="b89e4-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b89e4-156">0x00000000</span></span>                                           |
| <span data-ttu-id="b89e4-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-157">System-Flags</span></span>           | <span data-ttu-id="b89e4-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b89e4-158">0x00000014</span></span>                                           |
| <span data-ttu-id="b89e4-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b89e4-159">Classes used in</span></span>        | [<span data-ttu-id="b89e4-160">**Objeto dinâmico**</span><span class="sxs-lookup"><span data-stu-id="b89e4-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b89e4-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="b89e4-161">ADAM</span></span>



| <span data-ttu-id="b89e4-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-162">Entry</span></span> | <span data-ttu-id="b89e4-163">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b89e4-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="b89e4-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="b89e4-166">System-Only</span></span>            | <span data-ttu-id="b89e4-167">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-167">False</span></span>                                                |
| <span data-ttu-id="b89e4-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b89e4-168">Is-Single-Valued</span></span>       | <span data-ttu-id="b89e4-169">True</span><span class="sxs-lookup"><span data-stu-id="b89e4-169">True</span></span>                                                 |
| <span data-ttu-id="b89e4-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="b89e4-170">Is Indexed</span></span>             | <span data-ttu-id="b89e4-171">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-171">False</span></span>                                                |
| <span data-ttu-id="b89e4-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b89e4-172">In Global Catalog</span></span>      | <span data-ttu-id="b89e4-173">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-173">False</span></span>                                                |
| <span data-ttu-id="b89e4-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b89e4-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="b89e4-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b89e4-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b89e4-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b89e4-176">Range-Lower</span></span>            | <span data-ttu-id="b89e4-177">0</span><span class="sxs-lookup"><span data-stu-id="b89e4-177">0</span></span>                                                    |
| <span data-ttu-id="b89e4-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b89e4-178">Range-Upper</span></span>            | <span data-ttu-id="b89e4-179">31557600</span><span class="sxs-lookup"><span data-stu-id="b89e4-179">31557600</span></span>                                             |
| <span data-ttu-id="b89e4-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-180">Search-Flags</span></span>           | <span data-ttu-id="b89e4-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b89e4-181">0x00000000</span></span>                                           |
| <span data-ttu-id="b89e4-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-182">System-Flags</span></span>           | <span data-ttu-id="b89e4-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b89e4-183">0x00000014</span></span>                                           |
| <span data-ttu-id="b89e4-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b89e4-184">Classes used in</span></span>        | [<span data-ttu-id="b89e4-185">**Objeto dinâmico**</span><span class="sxs-lookup"><span data-stu-id="b89e4-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b89e4-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b89e4-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b89e4-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-187">Entry</span></span> | <span data-ttu-id="b89e4-188">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b89e4-189">ID do link</span><span class="sxs-lookup"><span data-stu-id="b89e4-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="b89e4-191">System-Only</span></span>            | <span data-ttu-id="b89e4-192">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-192">False</span></span>                                                |
| <span data-ttu-id="b89e4-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b89e4-193">Is-Single-Valued</span></span>       | <span data-ttu-id="b89e4-194">True</span><span class="sxs-lookup"><span data-stu-id="b89e4-194">True</span></span>                                                 |
| <span data-ttu-id="b89e4-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="b89e4-195">Is Indexed</span></span>             | <span data-ttu-id="b89e4-196">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-196">False</span></span>                                                |
| <span data-ttu-id="b89e4-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b89e4-197">In Global Catalog</span></span>      | <span data-ttu-id="b89e4-198">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-198">False</span></span>                                                |
| <span data-ttu-id="b89e4-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b89e4-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="b89e4-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b89e4-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b89e4-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b89e4-201">Range-Lower</span></span>            | <span data-ttu-id="b89e4-202">0</span><span class="sxs-lookup"><span data-stu-id="b89e4-202">0</span></span>                                                    |
| <span data-ttu-id="b89e4-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b89e4-203">Range-Upper</span></span>            | <span data-ttu-id="b89e4-204">31557600</span><span class="sxs-lookup"><span data-stu-id="b89e4-204">31557600</span></span>                                             |
| <span data-ttu-id="b89e4-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-205">Search-Flags</span></span>           | <span data-ttu-id="b89e4-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b89e4-206">0x00000000</span></span>                                           |
| <span data-ttu-id="b89e4-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-207">System-Flags</span></span>           | <span data-ttu-id="b89e4-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b89e4-208">0x00000014</span></span>                                           |
| <span data-ttu-id="b89e4-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b89e4-209">Classes used in</span></span>        | [<span data-ttu-id="b89e4-210">**Objeto dinâmico**</span><span class="sxs-lookup"><span data-stu-id="b89e4-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b89e4-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b89e4-211">Windows Server 2008</span></span>



| <span data-ttu-id="b89e4-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-212">Entry</span></span> | <span data-ttu-id="b89e4-213">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b89e4-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="b89e4-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="b89e4-216">System-Only</span></span>            | <span data-ttu-id="b89e4-217">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-217">False</span></span>                                                |
| <span data-ttu-id="b89e4-218">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b89e4-218">Is-Single-Valued</span></span>       | <span data-ttu-id="b89e4-219">True</span><span class="sxs-lookup"><span data-stu-id="b89e4-219">True</span></span>                                                 |
| <span data-ttu-id="b89e4-220">É indexado</span><span class="sxs-lookup"><span data-stu-id="b89e4-220">Is Indexed</span></span>             | <span data-ttu-id="b89e4-221">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-221">False</span></span>                                                |
| <span data-ttu-id="b89e4-222">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b89e4-222">In Global Catalog</span></span>      | <span data-ttu-id="b89e4-223">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-223">False</span></span>                                                |
| <span data-ttu-id="b89e4-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b89e4-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="b89e4-225">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b89e4-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b89e4-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b89e4-226">Range-Lower</span></span>            | <span data-ttu-id="b89e4-227">0</span><span class="sxs-lookup"><span data-stu-id="b89e4-227">0</span></span>                                                    |
| <span data-ttu-id="b89e4-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b89e4-228">Range-Upper</span></span>            | <span data-ttu-id="b89e4-229">31557600</span><span class="sxs-lookup"><span data-stu-id="b89e4-229">31557600</span></span>                                             |
| <span data-ttu-id="b89e4-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-230">Search-Flags</span></span>           | <span data-ttu-id="b89e4-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b89e4-231">0x00000000</span></span>                                           |
| <span data-ttu-id="b89e4-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-232">System-Flags</span></span>           | <span data-ttu-id="b89e4-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b89e4-233">0x00000014</span></span>                                           |
| <span data-ttu-id="b89e4-234">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b89e4-234">Classes used in</span></span>        | [<span data-ttu-id="b89e4-235">**Objeto dinâmico**</span><span class="sxs-lookup"><span data-stu-id="b89e4-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b89e4-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b89e4-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b89e4-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-237">Entry</span></span> | <span data-ttu-id="b89e4-238">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b89e4-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="b89e4-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="b89e4-241">System-Only</span></span>            | <span data-ttu-id="b89e4-242">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-242">False</span></span>                                                |
| <span data-ttu-id="b89e4-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b89e4-243">Is-Single-Valued</span></span>       | <span data-ttu-id="b89e4-244">True</span><span class="sxs-lookup"><span data-stu-id="b89e4-244">True</span></span>                                                 |
| <span data-ttu-id="b89e4-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="b89e4-245">Is Indexed</span></span>             | <span data-ttu-id="b89e4-246">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-246">False</span></span>                                                |
| <span data-ttu-id="b89e4-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b89e4-247">In Global Catalog</span></span>      | <span data-ttu-id="b89e4-248">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-248">False</span></span>                                                |
| <span data-ttu-id="b89e4-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b89e4-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="b89e4-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b89e4-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b89e4-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b89e4-251">Range-Lower</span></span>            | <span data-ttu-id="b89e4-252">0</span><span class="sxs-lookup"><span data-stu-id="b89e4-252">0</span></span>                                                    |
| <span data-ttu-id="b89e4-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b89e4-253">Range-Upper</span></span>            | <span data-ttu-id="b89e4-254">31557600</span><span class="sxs-lookup"><span data-stu-id="b89e4-254">31557600</span></span>                                             |
| <span data-ttu-id="b89e4-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-255">Search-Flags</span></span>           | <span data-ttu-id="b89e4-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b89e4-256">0x00000000</span></span>                                           |
| <span data-ttu-id="b89e4-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-257">System-Flags</span></span>           | <span data-ttu-id="b89e4-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b89e4-258">0x00000014</span></span>                                           |
| <span data-ttu-id="b89e4-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b89e4-259">Classes used in</span></span>        | [<span data-ttu-id="b89e4-260">**Objeto dinâmico**</span><span class="sxs-lookup"><span data-stu-id="b89e4-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b89e4-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b89e4-261">Windows Server 2012</span></span>



| <span data-ttu-id="b89e4-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="b89e4-262">Entry</span></span> | <span data-ttu-id="b89e4-263">Valor</span><span class="sxs-lookup"><span data-stu-id="b89e4-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b89e4-264">ID do link</span><span class="sxs-lookup"><span data-stu-id="b89e4-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b89e4-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b89e4-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="b89e4-266">System-Only</span></span>            | <span data-ttu-id="b89e4-267">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-267">False</span></span>                                                |
| <span data-ttu-id="b89e4-268">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b89e4-268">Is-Single-Valued</span></span>       | <span data-ttu-id="b89e4-269">True</span><span class="sxs-lookup"><span data-stu-id="b89e4-269">True</span></span>                                                 |
| <span data-ttu-id="b89e4-270">É indexado</span><span class="sxs-lookup"><span data-stu-id="b89e4-270">Is Indexed</span></span>             | <span data-ttu-id="b89e4-271">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-271">False</span></span>                                                |
| <span data-ttu-id="b89e4-272">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b89e4-272">In Global Catalog</span></span>      | <span data-ttu-id="b89e4-273">Falso</span><span class="sxs-lookup"><span data-stu-id="b89e4-273">False</span></span>                                                |
| <span data-ttu-id="b89e4-274">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b89e4-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="b89e4-275">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b89e4-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b89e4-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b89e4-276">Range-Lower</span></span>            | <span data-ttu-id="b89e4-277">0</span><span class="sxs-lookup"><span data-stu-id="b89e4-277">0</span></span>                                                    |
| <span data-ttu-id="b89e4-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b89e4-278">Range-Upper</span></span>            | <span data-ttu-id="b89e4-279">31557600</span><span class="sxs-lookup"><span data-stu-id="b89e4-279">31557600</span></span>                                             |
| <span data-ttu-id="b89e4-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-280">Search-Flags</span></span>           | <span data-ttu-id="b89e4-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b89e4-281">0x00000000</span></span>                                           |
| <span data-ttu-id="b89e4-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b89e4-282">System-Flags</span></span>           | <span data-ttu-id="b89e4-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b89e4-283">0x00000014</span></span>                                           |
| <span data-ttu-id="b89e4-284">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b89e4-284">Classes used in</span></span>        | [<span data-ttu-id="b89e4-285">**Objeto dinâmico**</span><span class="sxs-lookup"><span data-stu-id="b89e4-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





