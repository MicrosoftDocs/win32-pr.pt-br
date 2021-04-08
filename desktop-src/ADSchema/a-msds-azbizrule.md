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
# <a name="ms-ds-az-biz-rule-attribute"></a><span data-ttu-id="f0388-105">ms-DS-AZ-biz-atributo Rule</span><span class="sxs-lookup"><span data-stu-id="f0388-105">ms-DS-Az-Biz-Rule attribute</span></span>

<span data-ttu-id="f0388-106">Texto do script que implementa a regra de negócio.</span><span class="sxs-lookup"><span data-stu-id="f0388-106">Text of the script implementing the business rule.</span></span>



| <span data-ttu-id="f0388-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0388-107">Entry</span></span> | <span data-ttu-id="f0388-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f0388-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f0388-109">CN</span><span class="sxs-lookup"><span data-stu-id="f0388-109">CN</span></span>                | <span data-ttu-id="f0388-110">ms-DS-AZ-biz-Rule</span><span class="sxs-lookup"><span data-stu-id="f0388-110">ms-DS-Az-Biz-Rule</span></span>                           |
| <span data-ttu-id="f0388-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f0388-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f0388-112">msDS-AzBizRule</span><span class="sxs-lookup"><span data-stu-id="f0388-112">msDS-AzBizRule</span></span>                              |
| <span data-ttu-id="f0388-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f0388-113">Size</span></span>              | <span data-ttu-id="f0388-114">128 caracteres</span><span class="sxs-lookup"><span data-stu-id="f0388-114">128 characters</span></span>                              |
| <span data-ttu-id="f0388-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f0388-115">Update Privilege</span></span>  | <span data-ttu-id="f0388-116">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="f0388-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="f0388-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f0388-117">Update Frequency</span></span>  | <span data-ttu-id="f0388-118">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="f0388-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="f0388-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0388-119">Attribute-Id</span></span>      | <span data-ttu-id="f0388-120">1.2.840.113556.1.4.1801</span><span class="sxs-lookup"><span data-stu-id="f0388-120">1.2.840.113556.1.4.1801</span></span>                     |
| <span data-ttu-id="f0388-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f0388-121">System-Id-Guid</span></span>    | <span data-ttu-id="f0388-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span><span class="sxs-lookup"><span data-stu-id="f0388-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span></span>        |
| <span data-ttu-id="f0388-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0388-123">Syntax</span></span>            | [<span data-ttu-id="f0388-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f0388-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f0388-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="f0388-125">Implementations</span></span>

-   [<span data-ttu-id="f0388-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0388-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0388-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0388-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0388-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0388-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0388-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0388-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0388-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0388-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f0388-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0388-131">Windows Server 2003</span></span>



| <span data-ttu-id="f0388-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0388-132">Entry</span></span> | <span data-ttu-id="f0388-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f0388-133">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="f0388-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0388-134">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="f0388-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0388-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="f0388-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0388-136">System-Only</span></span>            | <span data-ttu-id="f0388-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-137">False</span></span>                                             |
| <span data-ttu-id="f0388-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0388-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f0388-139">True</span><span class="sxs-lookup"><span data-stu-id="f0388-139">True</span></span>                                              |
| <span data-ttu-id="f0388-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0388-140">Is Indexed</span></span>             | <span data-ttu-id="f0388-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-141">False</span></span>                                             |
| <span data-ttu-id="f0388-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0388-142">In Global Catalog</span></span>      | <span data-ttu-id="f0388-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-143">False</span></span>                                             |
| <span data-ttu-id="f0388-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0388-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0388-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0388-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="f0388-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0388-146">Range-Lower</span></span>            | <span data-ttu-id="f0388-147">0</span><span class="sxs-lookup"><span data-stu-id="f0388-147">0</span></span>                                                 |
| <span data-ttu-id="f0388-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0388-148">Range-Upper</span></span>            | <span data-ttu-id="f0388-149">65536</span><span class="sxs-lookup"><span data-stu-id="f0388-149">65536</span></span>                                             |
| <span data-ttu-id="f0388-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-150">Search-Flags</span></span>           | <span data-ttu-id="f0388-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0388-151">0x00000000</span></span>                                        |
| <span data-ttu-id="f0388-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-152">System-Flags</span></span>           | <span data-ttu-id="f0388-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0388-153">0x00000010</span></span>                                        |
| <span data-ttu-id="f0388-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0388-154">Classes used in</span></span>        | [<span data-ttu-id="f0388-155">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="f0388-155">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0388-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0388-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0388-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0388-157">Entry</span></span> | <span data-ttu-id="f0388-158">Valor</span><span class="sxs-lookup"><span data-stu-id="f0388-158">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="f0388-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0388-159">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="f0388-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0388-160">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="f0388-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0388-161">System-Only</span></span>            | <span data-ttu-id="f0388-162">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-162">False</span></span>                                             |
| <span data-ttu-id="f0388-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0388-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f0388-164">True</span><span class="sxs-lookup"><span data-stu-id="f0388-164">True</span></span>                                              |
| <span data-ttu-id="f0388-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0388-165">Is Indexed</span></span>             | <span data-ttu-id="f0388-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-166">False</span></span>                                             |
| <span data-ttu-id="f0388-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0388-167">In Global Catalog</span></span>      | <span data-ttu-id="f0388-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-168">False</span></span>                                             |
| <span data-ttu-id="f0388-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0388-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0388-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0388-170">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="f0388-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0388-171">Range-Lower</span></span>            | <span data-ttu-id="f0388-172">0</span><span class="sxs-lookup"><span data-stu-id="f0388-172">0</span></span>                                                 |
| <span data-ttu-id="f0388-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0388-173">Range-Upper</span></span>            | <span data-ttu-id="f0388-174">65536</span><span class="sxs-lookup"><span data-stu-id="f0388-174">65536</span></span>                                             |
| <span data-ttu-id="f0388-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-175">Search-Flags</span></span>           | <span data-ttu-id="f0388-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0388-176">0x00000000</span></span>                                        |
| <span data-ttu-id="f0388-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-177">System-Flags</span></span>           | <span data-ttu-id="f0388-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0388-178">0x00000010</span></span>                                        |
| <span data-ttu-id="f0388-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0388-179">Classes used in</span></span>        | [<span data-ttu-id="f0388-180">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="f0388-180">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0388-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0388-181">Windows Server 2008</span></span>



| <span data-ttu-id="f0388-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0388-182">Entry</span></span> | <span data-ttu-id="f0388-183">Valor</span><span class="sxs-lookup"><span data-stu-id="f0388-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0388-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0388-184">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="f0388-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0388-185">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="f0388-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0388-186">System-Only</span></span>            | <span data-ttu-id="f0388-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-187">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0388-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f0388-189">True</span><span class="sxs-lookup"><span data-stu-id="f0388-189">True</span></span>                                                                                  |
| <span data-ttu-id="f0388-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0388-190">Is Indexed</span></span>             | <span data-ttu-id="f0388-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-191">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0388-192">In Global Catalog</span></span>      | <span data-ttu-id="f0388-193">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-193">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0388-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0388-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0388-195">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="f0388-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0388-196">Range-Lower</span></span>            | <span data-ttu-id="f0388-197">0</span><span class="sxs-lookup"><span data-stu-id="f0388-197">0</span></span>                                                                                     |
| <span data-ttu-id="f0388-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0388-198">Range-Upper</span></span>            | <span data-ttu-id="f0388-199">65536</span><span class="sxs-lookup"><span data-stu-id="f0388-199">65536</span></span>                                                                                 |
| <span data-ttu-id="f0388-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-200">Search-Flags</span></span>           | <span data-ttu-id="f0388-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0388-201">0x00000000</span></span>                                                                            |
| <span data-ttu-id="f0388-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-202">System-Flags</span></span>           | <span data-ttu-id="f0388-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0388-203">0x00000010</span></span>                                                                            |
| <span data-ttu-id="f0388-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0388-204">Classes used in</span></span>        | [<span data-ttu-id="f0388-205">**Group**</span><span class="sxs-lookup"><span data-stu-id="f0388-205">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f0388-206">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="f0388-206">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0388-207">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0388-207">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0388-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0388-208">Entry</span></span> | <span data-ttu-id="f0388-209">Valor</span><span class="sxs-lookup"><span data-stu-id="f0388-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0388-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0388-210">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="f0388-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0388-211">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="f0388-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0388-212">System-Only</span></span>            | <span data-ttu-id="f0388-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-213">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0388-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f0388-215">True</span><span class="sxs-lookup"><span data-stu-id="f0388-215">True</span></span>                                                                                  |
| <span data-ttu-id="f0388-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0388-216">Is Indexed</span></span>             | <span data-ttu-id="f0388-217">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-217">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0388-218">In Global Catalog</span></span>      | <span data-ttu-id="f0388-219">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-219">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0388-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0388-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0388-221">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="f0388-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0388-222">Range-Lower</span></span>            | <span data-ttu-id="f0388-223">0</span><span class="sxs-lookup"><span data-stu-id="f0388-223">0</span></span>                                                                                     |
| <span data-ttu-id="f0388-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0388-224">Range-Upper</span></span>            | <span data-ttu-id="f0388-225">65536</span><span class="sxs-lookup"><span data-stu-id="f0388-225">65536</span></span>                                                                                 |
| <span data-ttu-id="f0388-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-226">Search-Flags</span></span>           | <span data-ttu-id="f0388-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0388-227">0x00000000</span></span>                                                                            |
| <span data-ttu-id="f0388-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-228">System-Flags</span></span>           | <span data-ttu-id="f0388-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0388-229">0x00000010</span></span>                                                                            |
| <span data-ttu-id="f0388-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0388-230">Classes used in</span></span>        | [<span data-ttu-id="f0388-231">**Group**</span><span class="sxs-lookup"><span data-stu-id="f0388-231">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f0388-232">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="f0388-232">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0388-233">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0388-233">Windows Server 2012</span></span>



| <span data-ttu-id="f0388-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0388-234">Entry</span></span> | <span data-ttu-id="f0388-235">Valor</span><span class="sxs-lookup"><span data-stu-id="f0388-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0388-236">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0388-236">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="f0388-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0388-237">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="f0388-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0388-238">System-Only</span></span>            | <span data-ttu-id="f0388-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-239">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-240">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0388-240">Is-Single-Valued</span></span>       | <span data-ttu-id="f0388-241">True</span><span class="sxs-lookup"><span data-stu-id="f0388-241">True</span></span>                                                                                  |
| <span data-ttu-id="f0388-242">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0388-242">Is Indexed</span></span>             | <span data-ttu-id="f0388-243">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-243">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-244">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0388-244">In Global Catalog</span></span>      | <span data-ttu-id="f0388-245">Falso</span><span class="sxs-lookup"><span data-stu-id="f0388-245">False</span></span>                                                                                 |
| <span data-ttu-id="f0388-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0388-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0388-247">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0388-247">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="f0388-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0388-248">Range-Lower</span></span>            | <span data-ttu-id="f0388-249">0</span><span class="sxs-lookup"><span data-stu-id="f0388-249">0</span></span>                                                                                     |
| <span data-ttu-id="f0388-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0388-250">Range-Upper</span></span>            | <span data-ttu-id="f0388-251">65536</span><span class="sxs-lookup"><span data-stu-id="f0388-251">65536</span></span>                                                                                 |
| <span data-ttu-id="f0388-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-252">Search-Flags</span></span>           | <span data-ttu-id="f0388-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0388-253">0x00000000</span></span>                                                                            |
| <span data-ttu-id="f0388-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0388-254">System-Flags</span></span>           | <span data-ttu-id="f0388-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0388-255">0x00000010</span></span>                                                                            |
| <span data-ttu-id="f0388-256">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0388-256">Classes used in</span></span>        | [<span data-ttu-id="f0388-257">**Group**</span><span class="sxs-lookup"><span data-stu-id="f0388-257">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="f0388-258">**ms-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="f0388-258">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



 

 





