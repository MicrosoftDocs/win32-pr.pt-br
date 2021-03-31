---
title: atributo ms-DS-AZ-Class-ID
description: Uma ID de classe exigida pela interface do usuário do amAzRoles no objeto AzApplication.
ms.assetid: cbbdc898-82b2-410e-8c9d-ae4f9641ac1a
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-AZ-Class-ID
- atributo msDS-AzClassId do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Az-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77d7ae6376deceaf23a9b7fa3c85ee8cb2b9748
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087092"
---
# <a name="ms-ds-az-class-id-attribute"></a><span data-ttu-id="da93b-105">atributo ms-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="da93b-105">ms-DS-Az-Class-ID attribute</span></span>

<span data-ttu-id="da93b-106">Uma ID de classe exigida pela interface do usuário do amAzRoles no objeto AzApplication.</span><span class="sxs-lookup"><span data-stu-id="da93b-106">A class ID required by the AzRoles UI on the AzApplication object.</span></span>



| <span data-ttu-id="da93b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="da93b-107">Entry</span></span> | <span data-ttu-id="da93b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="da93b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="da93b-109">CN</span><span class="sxs-lookup"><span data-stu-id="da93b-109">CN</span></span>                | <span data-ttu-id="da93b-110">ms-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="da93b-110">ms-DS-Az-Class-ID</span></span>                           |
| <span data-ttu-id="da93b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="da93b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="da93b-112">msDS-AzClassId</span><span class="sxs-lookup"><span data-stu-id="da93b-112">msDS-AzClassId</span></span>                              |
| <span data-ttu-id="da93b-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="da93b-113">Size</span></span>              | <span data-ttu-id="da93b-114">36 caracteres</span><span class="sxs-lookup"><span data-stu-id="da93b-114">36 characters</span></span>                               |
| <span data-ttu-id="da93b-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="da93b-115">Update Privilege</span></span>  | <span data-ttu-id="da93b-116">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="da93b-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="da93b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="da93b-117">Update Frequency</span></span>  | <span data-ttu-id="da93b-118">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="da93b-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="da93b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="da93b-119">Attribute-Id</span></span>      | <span data-ttu-id="da93b-120">1.2.840.113556.1.4.1816</span><span class="sxs-lookup"><span data-stu-id="da93b-120">1.2.840.113556.1.4.1816</span></span>                     |
| <span data-ttu-id="da93b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="da93b-121">System-Id-Guid</span></span>    | <span data-ttu-id="da93b-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span><span class="sxs-lookup"><span data-stu-id="da93b-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span></span>        |
| <span data-ttu-id="da93b-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da93b-123">Syntax</span></span>            | [<span data-ttu-id="da93b-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="da93b-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="da93b-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="da93b-125">Implementations</span></span>

-   [<span data-ttu-id="da93b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="da93b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="da93b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="da93b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="da93b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="da93b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="da93b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="da93b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="da93b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="da93b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="da93b-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da93b-131">Windows Server 2003</span></span>



| <span data-ttu-id="da93b-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="da93b-132">Entry</span></span> | <span data-ttu-id="da93b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="da93b-133">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="da93b-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="da93b-134">Link-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da93b-135">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="da93b-136">System-Only</span></span>            | <span data-ttu-id="da93b-137">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-137">False</span></span>        |
| <span data-ttu-id="da93b-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="da93b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="da93b-139">True</span><span class="sxs-lookup"><span data-stu-id="da93b-139">True</span></span>         |
| <span data-ttu-id="da93b-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="da93b-140">Is Indexed</span></span>             | <span data-ttu-id="da93b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-141">False</span></span>        |
| <span data-ttu-id="da93b-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="da93b-142">In Global Catalog</span></span>      | <span data-ttu-id="da93b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-143">False</span></span>        |
| <span data-ttu-id="da93b-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da93b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="da93b-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="da93b-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="da93b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da93b-146">Range-Lower</span></span>            | <span data-ttu-id="da93b-147">0</span><span class="sxs-lookup"><span data-stu-id="da93b-147">0</span></span>            |
| <span data-ttu-id="da93b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da93b-148">Range-Upper</span></span>            | <span data-ttu-id="da93b-149">40</span><span class="sxs-lookup"><span data-stu-id="da93b-149">40</span></span>           |
| <span data-ttu-id="da93b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-150">Search-Flags</span></span>           | <span data-ttu-id="da93b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da93b-151">0x00000000</span></span>   |
| <span data-ttu-id="da93b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-152">System-Flags</span></span>           | <span data-ttu-id="da93b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da93b-153">0x00000010</span></span>   |
| <span data-ttu-id="da93b-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="da93b-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="da93b-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="da93b-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="da93b-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="da93b-156">Entry</span></span> | <span data-ttu-id="da93b-157">Valor</span><span class="sxs-lookup"><span data-stu-id="da93b-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="da93b-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="da93b-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da93b-159">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="da93b-160">System-Only</span></span>            | <span data-ttu-id="da93b-161">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-161">False</span></span>        |
| <span data-ttu-id="da93b-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="da93b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="da93b-163">True</span><span class="sxs-lookup"><span data-stu-id="da93b-163">True</span></span>         |
| <span data-ttu-id="da93b-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="da93b-164">Is Indexed</span></span>             | <span data-ttu-id="da93b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-165">False</span></span>        |
| <span data-ttu-id="da93b-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="da93b-166">In Global Catalog</span></span>      | <span data-ttu-id="da93b-167">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-167">False</span></span>        |
| <span data-ttu-id="da93b-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da93b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="da93b-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="da93b-169">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="da93b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da93b-170">Range-Lower</span></span>            | <span data-ttu-id="da93b-171">0</span><span class="sxs-lookup"><span data-stu-id="da93b-171">0</span></span>            |
| <span data-ttu-id="da93b-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da93b-172">Range-Upper</span></span>            | <span data-ttu-id="da93b-173">40</span><span class="sxs-lookup"><span data-stu-id="da93b-173">40</span></span>           |
| <span data-ttu-id="da93b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-174">Search-Flags</span></span>           | <span data-ttu-id="da93b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da93b-175">0x00000000</span></span>   |
| <span data-ttu-id="da93b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-176">System-Flags</span></span>           | <span data-ttu-id="da93b-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da93b-177">0x00000010</span></span>   |
| <span data-ttu-id="da93b-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="da93b-178">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="da93b-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da93b-179">Windows Server 2008</span></span>



| <span data-ttu-id="da93b-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="da93b-180">Entry</span></span> | <span data-ttu-id="da93b-181">Valor</span><span class="sxs-lookup"><span data-stu-id="da93b-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="da93b-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="da93b-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da93b-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="da93b-184">System-Only</span></span>            | <span data-ttu-id="da93b-185">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-185">False</span></span>        |
| <span data-ttu-id="da93b-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="da93b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="da93b-187">True</span><span class="sxs-lookup"><span data-stu-id="da93b-187">True</span></span>         |
| <span data-ttu-id="da93b-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="da93b-188">Is Indexed</span></span>             | <span data-ttu-id="da93b-189">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-189">False</span></span>        |
| <span data-ttu-id="da93b-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="da93b-190">In Global Catalog</span></span>      | <span data-ttu-id="da93b-191">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-191">False</span></span>        |
| <span data-ttu-id="da93b-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da93b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="da93b-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="da93b-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="da93b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da93b-194">Range-Lower</span></span>            | <span data-ttu-id="da93b-195">0</span><span class="sxs-lookup"><span data-stu-id="da93b-195">0</span></span>            |
| <span data-ttu-id="da93b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da93b-196">Range-Upper</span></span>            | <span data-ttu-id="da93b-197">40</span><span class="sxs-lookup"><span data-stu-id="da93b-197">40</span></span>           |
| <span data-ttu-id="da93b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-198">Search-Flags</span></span>           | <span data-ttu-id="da93b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da93b-199">0x00000000</span></span>   |
| <span data-ttu-id="da93b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-200">System-Flags</span></span>           | <span data-ttu-id="da93b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da93b-201">0x00000010</span></span>   |
| <span data-ttu-id="da93b-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="da93b-202">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="da93b-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da93b-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="da93b-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="da93b-204">Entry</span></span> | <span data-ttu-id="da93b-205">Valor</span><span class="sxs-lookup"><span data-stu-id="da93b-205">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="da93b-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="da93b-206">Link-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da93b-207">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="da93b-208">System-Only</span></span>            | <span data-ttu-id="da93b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-209">False</span></span>        |
| <span data-ttu-id="da93b-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="da93b-210">Is-Single-Valued</span></span>       | <span data-ttu-id="da93b-211">True</span><span class="sxs-lookup"><span data-stu-id="da93b-211">True</span></span>         |
| <span data-ttu-id="da93b-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="da93b-212">Is Indexed</span></span>             | <span data-ttu-id="da93b-213">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-213">False</span></span>        |
| <span data-ttu-id="da93b-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="da93b-214">In Global Catalog</span></span>      | <span data-ttu-id="da93b-215">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-215">False</span></span>        |
| <span data-ttu-id="da93b-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da93b-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="da93b-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="da93b-217">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="da93b-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da93b-218">Range-Lower</span></span>            | <span data-ttu-id="da93b-219">0</span><span class="sxs-lookup"><span data-stu-id="da93b-219">0</span></span>            |
| <span data-ttu-id="da93b-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da93b-220">Range-Upper</span></span>            | <span data-ttu-id="da93b-221">40</span><span class="sxs-lookup"><span data-stu-id="da93b-221">40</span></span>           |
| <span data-ttu-id="da93b-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-222">Search-Flags</span></span>           | <span data-ttu-id="da93b-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da93b-223">0x00000000</span></span>   |
| <span data-ttu-id="da93b-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-224">System-Flags</span></span>           | <span data-ttu-id="da93b-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da93b-225">0x00000010</span></span>   |
| <span data-ttu-id="da93b-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="da93b-226">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="da93b-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da93b-227">Windows Server 2012</span></span>



| <span data-ttu-id="da93b-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="da93b-228">Entry</span></span> | <span data-ttu-id="da93b-229">Valor</span><span class="sxs-lookup"><span data-stu-id="da93b-229">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="da93b-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="da93b-230">Link-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="da93b-231">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="da93b-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="da93b-232">System-Only</span></span>            | <span data-ttu-id="da93b-233">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-233">False</span></span>        |
| <span data-ttu-id="da93b-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="da93b-234">Is-Single-Valued</span></span>       | <span data-ttu-id="da93b-235">True</span><span class="sxs-lookup"><span data-stu-id="da93b-235">True</span></span>         |
| <span data-ttu-id="da93b-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="da93b-236">Is Indexed</span></span>             | <span data-ttu-id="da93b-237">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-237">False</span></span>        |
| <span data-ttu-id="da93b-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="da93b-238">In Global Catalog</span></span>      | <span data-ttu-id="da93b-239">Falso</span><span class="sxs-lookup"><span data-stu-id="da93b-239">False</span></span>        |
| <span data-ttu-id="da93b-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="da93b-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="da93b-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="da93b-241">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="da93b-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="da93b-242">Range-Lower</span></span>            | <span data-ttu-id="da93b-243">0</span><span class="sxs-lookup"><span data-stu-id="da93b-243">0</span></span>            |
| <span data-ttu-id="da93b-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="da93b-244">Range-Upper</span></span>            | <span data-ttu-id="da93b-245">40</span><span class="sxs-lookup"><span data-stu-id="da93b-245">40</span></span>           |
| <span data-ttu-id="da93b-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-246">Search-Flags</span></span>           | <span data-ttu-id="da93b-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="da93b-247">0x00000000</span></span>   |
| <span data-ttu-id="da93b-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="da93b-248">System-Flags</span></span>           | <span data-ttu-id="da93b-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da93b-249">0x00000010</span></span>   |
| <span data-ttu-id="da93b-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="da93b-250">Classes used in</span></span>        | \-           |



 

 




