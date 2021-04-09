---
title: DIT-atributo Content-Rules
description: Isso especifica o conteúdo permitido de entradas de uma determinada classe de objeto estrutural usando a identificação de um conjunto opcional de classes de objeto auxiliar e os atributos obrigatórios, opcionais e impedidos.
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- DIT-Content-Rules atributo AD Schema
- Esquema de AD do atributo dITContentRules
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087127"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="0261b-105">DIT-atributo Content-Rules</span><span class="sxs-lookup"><span data-stu-id="0261b-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="0261b-106">Isso especifica o conteúdo permitido de entradas de uma determinada classe de objeto estrutural usando a identificação de um conjunto opcional de classes de objeto auxiliar e os atributos obrigatórios, opcionais e impedidos.</span><span class="sxs-lookup"><span data-stu-id="0261b-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="0261b-107">Atributos coletivos são incluídos em DIT-Content-Rules, conforme definido no RFC 2251.</span><span class="sxs-lookup"><span data-stu-id="0261b-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="0261b-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-108">Entry</span></span> | <span data-ttu-id="0261b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0261b-110">CN</span><span class="sxs-lookup"><span data-stu-id="0261b-110">CN</span></span>                | <span data-ttu-id="0261b-111">DIT-Content-Rules</span><span class="sxs-lookup"><span data-stu-id="0261b-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="0261b-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0261b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0261b-113">dITContentRules</span><span class="sxs-lookup"><span data-stu-id="0261b-113">dITContentRules</span></span>                             |
| <span data-ttu-id="0261b-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0261b-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="0261b-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0261b-115">Update Privilege</span></span>  | <span data-ttu-id="0261b-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="0261b-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="0261b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0261b-117">Update Frequency</span></span>  | <span data-ttu-id="0261b-118">Sempre que uma nova classe é criada.</span><span class="sxs-lookup"><span data-stu-id="0261b-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="0261b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-119">Attribute-Id</span></span>      | <span data-ttu-id="0261b-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="0261b-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="0261b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0261b-121">System-Id-Guid</span></span>    | <span data-ttu-id="0261b-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="0261b-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="0261b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0261b-123">Syntax</span></span>            | [<span data-ttu-id="0261b-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0261b-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0261b-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="0261b-125">Implementations</span></span>

-   [<span data-ttu-id="0261b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0261b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0261b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0261b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0261b-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0261b-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0261b-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0261b-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0261b-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0261b-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0261b-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0261b-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0261b-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0261b-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0261b-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0261b-133">Windows 2000 Server</span></span>



| <span data-ttu-id="0261b-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-134">Entry</span></span> | <span data-ttu-id="0261b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-138">System-Only</span></span>            | <span data-ttu-id="0261b-139">True</span><span class="sxs-lookup"><span data-stu-id="0261b-139">True</span></span>                                        |
| <span data-ttu-id="0261b-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-140">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-141">False</span></span>                                       |
| <span data-ttu-id="0261b-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-142">Is Indexed</span></span>             | <span data-ttu-id="0261b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-143">False</span></span>                                       |
| <span data-ttu-id="0261b-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-144">In Global Catalog</span></span>      | <span data-ttu-id="0261b-145">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-145">False</span></span>                                       |
| <span data-ttu-id="0261b-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-150">Search-Flags</span></span>           | <span data-ttu-id="0261b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-151">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-152">System-Flags</span></span>           | <span data-ttu-id="0261b-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-153">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-154">Classes used in</span></span>        | [<span data-ttu-id="0261b-155">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0261b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0261b-156">Windows Server 2003</span></span>



| <span data-ttu-id="0261b-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-157">Entry</span></span> | <span data-ttu-id="0261b-158">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-161">System-Only</span></span>            | <span data-ttu-id="0261b-162">True</span><span class="sxs-lookup"><span data-stu-id="0261b-162">True</span></span>                                        |
| <span data-ttu-id="0261b-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-164">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-164">False</span></span>                                       |
| <span data-ttu-id="0261b-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-165">Is Indexed</span></span>             | <span data-ttu-id="0261b-166">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-166">False</span></span>                                       |
| <span data-ttu-id="0261b-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-167">In Global Catalog</span></span>      | <span data-ttu-id="0261b-168">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-168">False</span></span>                                       |
| <span data-ttu-id="0261b-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-173">Search-Flags</span></span>           | <span data-ttu-id="0261b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-174">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-175">System-Flags</span></span>           | <span data-ttu-id="0261b-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-176">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-177">Classes used in</span></span>        | [<span data-ttu-id="0261b-178">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0261b-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="0261b-179">ADAM</span></span>



| <span data-ttu-id="0261b-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-180">Entry</span></span> | <span data-ttu-id="0261b-181">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-184">System-Only</span></span>            | <span data-ttu-id="0261b-185">True</span><span class="sxs-lookup"><span data-stu-id="0261b-185">True</span></span>                                        |
| <span data-ttu-id="0261b-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-187">False</span></span>                                       |
| <span data-ttu-id="0261b-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-188">Is Indexed</span></span>             | <span data-ttu-id="0261b-189">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-189">False</span></span>                                       |
| <span data-ttu-id="0261b-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-190">In Global Catalog</span></span>      | <span data-ttu-id="0261b-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-191">False</span></span>                                       |
| <span data-ttu-id="0261b-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-196">Search-Flags</span></span>           | <span data-ttu-id="0261b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-197">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-198">System-Flags</span></span>           | <span data-ttu-id="0261b-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-199">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-200">Classes used in</span></span>        | [<span data-ttu-id="0261b-201">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0261b-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0261b-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0261b-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-203">Entry</span></span> | <span data-ttu-id="0261b-204">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-207">System-Only</span></span>            | <span data-ttu-id="0261b-208">True</span><span class="sxs-lookup"><span data-stu-id="0261b-208">True</span></span>                                        |
| <span data-ttu-id="0261b-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-209">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-210">False</span></span>                                       |
| <span data-ttu-id="0261b-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-211">Is Indexed</span></span>             | <span data-ttu-id="0261b-212">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-212">False</span></span>                                       |
| <span data-ttu-id="0261b-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-213">In Global Catalog</span></span>      | <span data-ttu-id="0261b-214">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-214">False</span></span>                                       |
| <span data-ttu-id="0261b-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-219">Search-Flags</span></span>           | <span data-ttu-id="0261b-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-220">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-221">System-Flags</span></span>           | <span data-ttu-id="0261b-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-222">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-223">Classes used in</span></span>        | [<span data-ttu-id="0261b-224">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0261b-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0261b-225">Windows Server 2008</span></span>



| <span data-ttu-id="0261b-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-226">Entry</span></span> | <span data-ttu-id="0261b-227">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-230">System-Only</span></span>            | <span data-ttu-id="0261b-231">True</span><span class="sxs-lookup"><span data-stu-id="0261b-231">True</span></span>                                        |
| <span data-ttu-id="0261b-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-232">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-233">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-233">False</span></span>                                       |
| <span data-ttu-id="0261b-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-234">Is Indexed</span></span>             | <span data-ttu-id="0261b-235">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-235">False</span></span>                                       |
| <span data-ttu-id="0261b-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-236">In Global Catalog</span></span>      | <span data-ttu-id="0261b-237">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-237">False</span></span>                                       |
| <span data-ttu-id="0261b-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-242">Search-Flags</span></span>           | <span data-ttu-id="0261b-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-243">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-244">System-Flags</span></span>           | <span data-ttu-id="0261b-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-245">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-246">Classes used in</span></span>        | [<span data-ttu-id="0261b-247">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0261b-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0261b-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0261b-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-249">Entry</span></span> | <span data-ttu-id="0261b-250">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-253">System-Only</span></span>            | <span data-ttu-id="0261b-254">True</span><span class="sxs-lookup"><span data-stu-id="0261b-254">True</span></span>                                        |
| <span data-ttu-id="0261b-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-255">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-256">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-256">False</span></span>                                       |
| <span data-ttu-id="0261b-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-257">Is Indexed</span></span>             | <span data-ttu-id="0261b-258">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-258">False</span></span>                                       |
| <span data-ttu-id="0261b-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-259">In Global Catalog</span></span>      | <span data-ttu-id="0261b-260">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-260">False</span></span>                                       |
| <span data-ttu-id="0261b-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-265">Search-Flags</span></span>           | <span data-ttu-id="0261b-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-266">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-267">System-Flags</span></span>           | <span data-ttu-id="0261b-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-268">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-269">Classes used in</span></span>        | [<span data-ttu-id="0261b-270">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0261b-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0261b-271">Windows Server 2012</span></span>



| <span data-ttu-id="0261b-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="0261b-272">Entry</span></span> | <span data-ttu-id="0261b-273">Valor</span><span class="sxs-lookup"><span data-stu-id="0261b-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="0261b-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="0261b-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0261b-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="0261b-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="0261b-276">System-Only</span></span>            | <span data-ttu-id="0261b-277">True</span><span class="sxs-lookup"><span data-stu-id="0261b-277">True</span></span>                                        |
| <span data-ttu-id="0261b-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0261b-278">Is-Single-Valued</span></span>       | <span data-ttu-id="0261b-279">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-279">False</span></span>                                       |
| <span data-ttu-id="0261b-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="0261b-280">Is Indexed</span></span>             | <span data-ttu-id="0261b-281">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-281">False</span></span>                                       |
| <span data-ttu-id="0261b-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0261b-282">In Global Catalog</span></span>      | <span data-ttu-id="0261b-283">Falso</span><span class="sxs-lookup"><span data-stu-id="0261b-283">False</span></span>                                       |
| <span data-ttu-id="0261b-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0261b-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="0261b-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0261b-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="0261b-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0261b-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="0261b-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0261b-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="0261b-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-288">Search-Flags</span></span>           | <span data-ttu-id="0261b-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0261b-289">0x00000000</span></span>                                  |
| <span data-ttu-id="0261b-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0261b-290">System-Flags</span></span>           | <span data-ttu-id="0261b-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="0261b-291">0x08000014</span></span>                                  |
| <span data-ttu-id="0261b-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0261b-292">Classes used in</span></span>        | [<span data-ttu-id="0261b-293">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="0261b-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





