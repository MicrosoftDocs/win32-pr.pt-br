---
title: atributo ms-DS-allowed-to-delegate
description: Este é um atributo em objetos de conta de serviço (computador ou conta de usuário).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- ms-DS – permitido-para-delegar para atributos do AD
- atributo msDS-AllowedToDelegateTo do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755732"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="0546e-105">atributo ms-DS-allowed-to-delegate</span><span class="sxs-lookup"><span data-stu-id="0546e-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="0546e-106">Este é um atributo em objetos de conta de serviço (computador ou conta de usuário).</span><span class="sxs-lookup"><span data-stu-id="0546e-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="0546e-107">Ele contém uma lista de SPNs (nomes de entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="0546e-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="0546e-108">Esse atributo é usado para configurar um serviço para que ele possa obter tíquetes de serviço que podem ser usados para delegação restrita.</span><span class="sxs-lookup"><span data-stu-id="0546e-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="0546e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="0546e-109">Entry</span></span> | <span data-ttu-id="0546e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0546e-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0546e-111">CN</span><span class="sxs-lookup"><span data-stu-id="0546e-111">CN</span></span>                | <span data-ttu-id="0546e-112">ms-DS-permitido-para-delegar para</span><span class="sxs-lookup"><span data-stu-id="0546e-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="0546e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0546e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0546e-114">msDS-AllowedToDelegateTo</span><span class="sxs-lookup"><span data-stu-id="0546e-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="0546e-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0546e-115">Size</span></span>              | <span data-ttu-id="0546e-116">0 a 64K</span><span class="sxs-lookup"><span data-stu-id="0546e-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="0546e-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0546e-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0546e-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0546e-118">Update Frequency</span></span>  | <span data-ttu-id="0546e-119">Raramente</span><span class="sxs-lookup"><span data-stu-id="0546e-119">Infrequently</span></span>                                |
| <span data-ttu-id="0546e-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0546e-120">Attribute-Id</span></span>      | <span data-ttu-id="0546e-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="0546e-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="0546e-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0546e-122">System-Id-Guid</span></span>    | <span data-ttu-id="0546e-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="0546e-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="0546e-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="0546e-124">Syntax</span></span>            | [<span data-ttu-id="0546e-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0546e-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0546e-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="0546e-126">Implementations</span></span>

-   [<span data-ttu-id="0546e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0546e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0546e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0546e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0546e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0546e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0546e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0546e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0546e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0546e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0546e-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0546e-132">Windows Server 2003</span></span>



| <span data-ttu-id="0546e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="0546e-133">Entry</span></span> | <span data-ttu-id="0546e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0546e-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0546e-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="0546e-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546e-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546e-137">System-Only</span></span>            | <span data-ttu-id="0546e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-138">False</span></span>                                                              |
| <span data-ttu-id="0546e-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0546e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0546e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-140">False</span></span>                                                              |
| <span data-ttu-id="0546e-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="0546e-141">Is Indexed</span></span>             | <span data-ttu-id="0546e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-142">False</span></span>                                                              |
| <span data-ttu-id="0546e-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0546e-143">In Global Catalog</span></span>      | <span data-ttu-id="0546e-144">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-144">False</span></span>                                                              |
| <span data-ttu-id="0546e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546e-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0546e-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0546e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546e-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546e-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-149">Search-Flags</span></span>           | <span data-ttu-id="0546e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0546e-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="0546e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-151">System-Flags</span></span>           | <span data-ttu-id="0546e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0546e-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="0546e-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0546e-153">Classes used in</span></span>        | [<span data-ttu-id="0546e-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0546e-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0546e-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0546e-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0546e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="0546e-156">Entry</span></span> | <span data-ttu-id="0546e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0546e-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0546e-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="0546e-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546e-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546e-160">System-Only</span></span>            | <span data-ttu-id="0546e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-161">False</span></span>                                                              |
| <span data-ttu-id="0546e-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0546e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0546e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-163">False</span></span>                                                              |
| <span data-ttu-id="0546e-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="0546e-164">Is Indexed</span></span>             | <span data-ttu-id="0546e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-165">False</span></span>                                                              |
| <span data-ttu-id="0546e-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0546e-166">In Global Catalog</span></span>      | <span data-ttu-id="0546e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-167">False</span></span>                                                              |
| <span data-ttu-id="0546e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546e-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0546e-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0546e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546e-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546e-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-172">Search-Flags</span></span>           | <span data-ttu-id="0546e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0546e-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="0546e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-174">System-Flags</span></span>           | <span data-ttu-id="0546e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0546e-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="0546e-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0546e-176">Classes used in</span></span>        | [<span data-ttu-id="0546e-177">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0546e-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0546e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0546e-178">Windows Server 2008</span></span>



| <span data-ttu-id="0546e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="0546e-179">Entry</span></span> | <span data-ttu-id="0546e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="0546e-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0546e-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="0546e-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546e-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546e-183">System-Only</span></span>            | <span data-ttu-id="0546e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-184">False</span></span>                                                              |
| <span data-ttu-id="0546e-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0546e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="0546e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-186">False</span></span>                                                              |
| <span data-ttu-id="0546e-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="0546e-187">Is Indexed</span></span>             | <span data-ttu-id="0546e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-188">False</span></span>                                                              |
| <span data-ttu-id="0546e-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0546e-189">In Global Catalog</span></span>      | <span data-ttu-id="0546e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-190">False</span></span>                                                              |
| <span data-ttu-id="0546e-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546e-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0546e-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0546e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546e-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546e-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-195">Search-Flags</span></span>           | <span data-ttu-id="0546e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0546e-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="0546e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-197">System-Flags</span></span>           | <span data-ttu-id="0546e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0546e-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="0546e-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0546e-199">Classes used in</span></span>        | [<span data-ttu-id="0546e-200">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0546e-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0546e-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0546e-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0546e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="0546e-202">Entry</span></span> | <span data-ttu-id="0546e-203">Valor</span><span class="sxs-lookup"><span data-stu-id="0546e-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0546e-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="0546e-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546e-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546e-206">System-Only</span></span>            | <span data-ttu-id="0546e-207">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-207">False</span></span>                                                              |
| <span data-ttu-id="0546e-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0546e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="0546e-209">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-209">False</span></span>                                                              |
| <span data-ttu-id="0546e-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="0546e-210">Is Indexed</span></span>             | <span data-ttu-id="0546e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-211">False</span></span>                                                              |
| <span data-ttu-id="0546e-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0546e-212">In Global Catalog</span></span>      | <span data-ttu-id="0546e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-213">False</span></span>                                                              |
| <span data-ttu-id="0546e-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546e-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0546e-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0546e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546e-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546e-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-218">Search-Flags</span></span>           | <span data-ttu-id="0546e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0546e-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="0546e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-220">System-Flags</span></span>           | <span data-ttu-id="0546e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0546e-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="0546e-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0546e-222">Classes used in</span></span>        | [<span data-ttu-id="0546e-223">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0546e-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0546e-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0546e-224">Windows Server 2012</span></span>



| <span data-ttu-id="0546e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="0546e-225">Entry</span></span> | <span data-ttu-id="0546e-226">Valor</span><span class="sxs-lookup"><span data-stu-id="0546e-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0546e-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="0546e-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0546e-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0546e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="0546e-229">System-Only</span></span>            | <span data-ttu-id="0546e-230">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-230">False</span></span>                                                              |
| <span data-ttu-id="0546e-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0546e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="0546e-232">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-232">False</span></span>                                                              |
| <span data-ttu-id="0546e-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="0546e-233">Is Indexed</span></span>             | <span data-ttu-id="0546e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-234">False</span></span>                                                              |
| <span data-ttu-id="0546e-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0546e-235">In Global Catalog</span></span>      | <span data-ttu-id="0546e-236">Falso</span><span class="sxs-lookup"><span data-stu-id="0546e-236">False</span></span>                                                              |
| <span data-ttu-id="0546e-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0546e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="0546e-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0546e-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0546e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0546e-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0546e-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="0546e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-241">Search-Flags</span></span>           | <span data-ttu-id="0546e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0546e-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="0546e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0546e-243">System-Flags</span></span>           | <span data-ttu-id="0546e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0546e-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="0546e-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0546e-245">Classes used in</span></span>        | [<span data-ttu-id="0546e-246">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0546e-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





