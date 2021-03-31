---
title: ms-DS-AZ-biz-atributo Rule
description: Texto do script que implementa a regra de negócio.
ms.assetid: 884513ae-9600-49b0-a371-6f77b84b54f9
ms.tgt_platform: multiple
keywords:
- ms-DS-AZ-biz-atributo Rule esquema do AD
- atributo msDS-AzBizRule do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Az-Biz-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571ab48c9742ffb93015c433685c01cb3a9666d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087094"
---
# <a name="ms-ds-az-biz-rule-attribute"></a><span data-ttu-id="90304-105">ms-DS-AZ-biz-atributo Rule</span><span class="sxs-lookup"><span data-stu-id="90304-105">ms-DS-Az-Biz-Rule attribute</span></span>

<span data-ttu-id="90304-106">Texto do script que implementa a regra de negócio.</span><span class="sxs-lookup"><span data-stu-id="90304-106">Text of the script implementing the business rule.</span></span>



| <span data-ttu-id="90304-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="90304-107">Entry</span></span> | <span data-ttu-id="90304-108">Valor</span><span class="sxs-lookup"><span data-stu-id="90304-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="90304-109">CN</span><span class="sxs-lookup"><span data-stu-id="90304-109">CN</span></span>                | <span data-ttu-id="90304-110">ms-DS-AZ-biz-Rule</span><span class="sxs-lookup"><span data-stu-id="90304-110">ms-DS-Az-Biz-Rule</span></span>                           |
| <span data-ttu-id="90304-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="90304-111">Ldap-Display-Name</span></span> | <span data-ttu-id="90304-112">msDS-AzBizRule</span><span class="sxs-lookup"><span data-stu-id="90304-112">msDS-AzBizRule</span></span>                              |
| <span data-ttu-id="90304-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="90304-113">Size</span></span>              | <span data-ttu-id="90304-114">128 caracteres</span><span class="sxs-lookup"><span data-stu-id="90304-114">128 characters</span></span>                              |
| <span data-ttu-id="90304-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="90304-115">Update Privilege</span></span>  | <span data-ttu-id="90304-116">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="90304-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="90304-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="90304-117">Update Frequency</span></span>  | <span data-ttu-id="90304-118">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="90304-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="90304-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90304-119">Attribute-Id</span></span>      | <span data-ttu-id="90304-120">1.2.840.113556.1.4.1801</span><span class="sxs-lookup"><span data-stu-id="90304-120">1.2.840.113556.1.4.1801</span></span>                     |
| <span data-ttu-id="90304-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="90304-121">System-Id-Guid</span></span>    | <span data-ttu-id="90304-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span><span class="sxs-lookup"><span data-stu-id="90304-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span></span>        |
| <span data-ttu-id="90304-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90304-123">Syntax</span></span>            | [<span data-ttu-id="90304-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="90304-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="90304-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="90304-125">Implementations</span></span>

-   [<span data-ttu-id="90304-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90304-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90304-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90304-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90304-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90304-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90304-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90304-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90304-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90304-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="90304-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90304-131">Windows Server 2003</span></span>



| <span data-ttu-id="90304-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="90304-132">Entry</span></span> | <span data-ttu-id="90304-133">Valor</span><span class="sxs-lookup"><span data-stu-id="90304-133">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="90304-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="90304-134">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="90304-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90304-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="90304-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="90304-136">System-Only</span></span>            | <span data-ttu-id="90304-137">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-137">False</span></span>                                             |
| <span data-ttu-id="90304-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90304-138">Is-Single-Valued</span></span>       | <span data-ttu-id="90304-139">True</span><span class="sxs-lookup"><span data-stu-id="90304-139">True</span></span>                                              |
| <span data-ttu-id="90304-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="90304-140">Is Indexed</span></span>             | <span data-ttu-id="90304-141">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-141">False</span></span>                                             |
| <span data-ttu-id="90304-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90304-142">In Global Catalog</span></span>      | <span data-ttu-id="90304-143">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-143">False</span></span>                                             |
| <span data-ttu-id="90304-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90304-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="90304-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90304-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="90304-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90304-146">Range-Lower</span></span>            | <span data-ttu-id="90304-147">0</span><span class="sxs-lookup"><span data-stu-id="90304-147">0</span></span>                                                 |
| <span data-ttu-id="90304-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90304-148">Range-Upper</span></span>            | <span data-ttu-id="90304-149">65536</span><span class="sxs-lookup"><span data-stu-id="90304-149">65536</span></span>                                             |
| <span data-ttu-id="90304-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-150">Search-Flags</span></span>           | <span data-ttu-id="90304-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90304-151">0x00000000</span></span>                                        |
| <span data-ttu-id="90304-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-152">System-Flags</span></span>           | <span data-ttu-id="90304-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90304-153">0x00000010</span></span>                                        |
| <span data-ttu-id="90304-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90304-154">Classes used in</span></span>        | [<span data-ttu-id="90304-155">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="90304-155">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90304-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90304-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90304-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="90304-157">Entry</span></span> | <span data-ttu-id="90304-158">Valor</span><span class="sxs-lookup"><span data-stu-id="90304-158">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="90304-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="90304-159">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="90304-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90304-160">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="90304-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="90304-161">System-Only</span></span>            | <span data-ttu-id="90304-162">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-162">False</span></span>                                             |
| <span data-ttu-id="90304-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90304-163">Is-Single-Valued</span></span>       | <span data-ttu-id="90304-164">True</span><span class="sxs-lookup"><span data-stu-id="90304-164">True</span></span>                                              |
| <span data-ttu-id="90304-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="90304-165">Is Indexed</span></span>             | <span data-ttu-id="90304-166">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-166">False</span></span>                                             |
| <span data-ttu-id="90304-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90304-167">In Global Catalog</span></span>      | <span data-ttu-id="90304-168">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-168">False</span></span>                                             |
| <span data-ttu-id="90304-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90304-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="90304-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90304-170">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="90304-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90304-171">Range-Lower</span></span>            | <span data-ttu-id="90304-172">0</span><span class="sxs-lookup"><span data-stu-id="90304-172">0</span></span>                                                 |
| <span data-ttu-id="90304-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90304-173">Range-Upper</span></span>            | <span data-ttu-id="90304-174">65536</span><span class="sxs-lookup"><span data-stu-id="90304-174">65536</span></span>                                             |
| <span data-ttu-id="90304-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-175">Search-Flags</span></span>           | <span data-ttu-id="90304-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90304-176">0x00000000</span></span>                                        |
| <span data-ttu-id="90304-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-177">System-Flags</span></span>           | <span data-ttu-id="90304-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90304-178">0x00000010</span></span>                                        |
| <span data-ttu-id="90304-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90304-179">Classes used in</span></span>        | [<span data-ttu-id="90304-180">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="90304-180">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90304-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90304-181">Windows Server 2008</span></span>



| <span data-ttu-id="90304-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="90304-182">Entry</span></span> | <span data-ttu-id="90304-183">Valor</span><span class="sxs-lookup"><span data-stu-id="90304-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90304-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="90304-184">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="90304-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90304-185">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="90304-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="90304-186">System-Only</span></span>            | <span data-ttu-id="90304-187">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-187">False</span></span>                                                                                 |
| <span data-ttu-id="90304-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90304-188">Is-Single-Valued</span></span>       | <span data-ttu-id="90304-189">True</span><span class="sxs-lookup"><span data-stu-id="90304-189">True</span></span>                                                                                  |
| <span data-ttu-id="90304-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="90304-190">Is Indexed</span></span>             | <span data-ttu-id="90304-191">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-191">False</span></span>                                                                                 |
| <span data-ttu-id="90304-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90304-192">In Global Catalog</span></span>      | <span data-ttu-id="90304-193">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-193">False</span></span>                                                                                 |
| <span data-ttu-id="90304-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90304-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="90304-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90304-195">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="90304-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90304-196">Range-Lower</span></span>            | <span data-ttu-id="90304-197">0</span><span class="sxs-lookup"><span data-stu-id="90304-197">0</span></span>                                                                                     |
| <span data-ttu-id="90304-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90304-198">Range-Upper</span></span>            | <span data-ttu-id="90304-199">65536</span><span class="sxs-lookup"><span data-stu-id="90304-199">65536</span></span>                                                                                 |
| <span data-ttu-id="90304-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-200">Search-Flags</span></span>           | <span data-ttu-id="90304-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90304-201">0x00000000</span></span>                                                                            |
| <span data-ttu-id="90304-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-202">System-Flags</span></span>           | <span data-ttu-id="90304-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90304-203">0x00000010</span></span>                                                                            |
| <span data-ttu-id="90304-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90304-204">Classes used in</span></span>        | [<span data-ttu-id="90304-205">**Group**</span><span class="sxs-lookup"><span data-stu-id="90304-205">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="90304-206">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="90304-206">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90304-207">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90304-207">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90304-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="90304-208">Entry</span></span> | <span data-ttu-id="90304-209">Valor</span><span class="sxs-lookup"><span data-stu-id="90304-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90304-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="90304-210">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="90304-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90304-211">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="90304-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="90304-212">System-Only</span></span>            | <span data-ttu-id="90304-213">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-213">False</span></span>                                                                                 |
| <span data-ttu-id="90304-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90304-214">Is-Single-Valued</span></span>       | <span data-ttu-id="90304-215">True</span><span class="sxs-lookup"><span data-stu-id="90304-215">True</span></span>                                                                                  |
| <span data-ttu-id="90304-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="90304-216">Is Indexed</span></span>             | <span data-ttu-id="90304-217">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-217">False</span></span>                                                                                 |
| <span data-ttu-id="90304-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90304-218">In Global Catalog</span></span>      | <span data-ttu-id="90304-219">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-219">False</span></span>                                                                                 |
| <span data-ttu-id="90304-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90304-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="90304-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90304-221">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="90304-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90304-222">Range-Lower</span></span>            | <span data-ttu-id="90304-223">0</span><span class="sxs-lookup"><span data-stu-id="90304-223">0</span></span>                                                                                     |
| <span data-ttu-id="90304-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90304-224">Range-Upper</span></span>            | <span data-ttu-id="90304-225">65536</span><span class="sxs-lookup"><span data-stu-id="90304-225">65536</span></span>                                                                                 |
| <span data-ttu-id="90304-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-226">Search-Flags</span></span>           | <span data-ttu-id="90304-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90304-227">0x00000000</span></span>                                                                            |
| <span data-ttu-id="90304-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-228">System-Flags</span></span>           | <span data-ttu-id="90304-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90304-229">0x00000010</span></span>                                                                            |
| <span data-ttu-id="90304-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90304-230">Classes used in</span></span>        | [<span data-ttu-id="90304-231">**Group**</span><span class="sxs-lookup"><span data-stu-id="90304-231">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="90304-232">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="90304-232">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90304-233">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90304-233">Windows Server 2012</span></span>



| <span data-ttu-id="90304-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="90304-234">Entry</span></span> | <span data-ttu-id="90304-235">Valor</span><span class="sxs-lookup"><span data-stu-id="90304-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90304-236">ID do link</span><span class="sxs-lookup"><span data-stu-id="90304-236">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="90304-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90304-237">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="90304-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="90304-238">System-Only</span></span>            | <span data-ttu-id="90304-239">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-239">False</span></span>                                                                                 |
| <span data-ttu-id="90304-240">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90304-240">Is-Single-Valued</span></span>       | <span data-ttu-id="90304-241">True</span><span class="sxs-lookup"><span data-stu-id="90304-241">True</span></span>                                                                                  |
| <span data-ttu-id="90304-242">É indexado</span><span class="sxs-lookup"><span data-stu-id="90304-242">Is Indexed</span></span>             | <span data-ttu-id="90304-243">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-243">False</span></span>                                                                                 |
| <span data-ttu-id="90304-244">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90304-244">In Global Catalog</span></span>      | <span data-ttu-id="90304-245">Falso</span><span class="sxs-lookup"><span data-stu-id="90304-245">False</span></span>                                                                                 |
| <span data-ttu-id="90304-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90304-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="90304-247">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90304-247">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="90304-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90304-248">Range-Lower</span></span>            | <span data-ttu-id="90304-249">0</span><span class="sxs-lookup"><span data-stu-id="90304-249">0</span></span>                                                                                     |
| <span data-ttu-id="90304-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90304-250">Range-Upper</span></span>            | <span data-ttu-id="90304-251">65536</span><span class="sxs-lookup"><span data-stu-id="90304-251">65536</span></span>                                                                                 |
| <span data-ttu-id="90304-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-252">Search-Flags</span></span>           | <span data-ttu-id="90304-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90304-253">0x00000000</span></span>                                                                            |
| <span data-ttu-id="90304-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90304-254">System-Flags</span></span>           | <span data-ttu-id="90304-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90304-255">0x00000010</span></span>                                                                            |
| <span data-ttu-id="90304-256">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90304-256">Classes used in</span></span>        | [<span data-ttu-id="90304-257">**Group**</span><span class="sxs-lookup"><span data-stu-id="90304-257">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="90304-258">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="90304-258">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



 

 





