---
title: atributo ms-DS-Filter-containers
description: Uma cadeia de caracteres com valores múltiplos que contém os nomes das classes usadas para determinar quais tipos de contêiner devem ser mostrados pelo snap-in Active Directory usuários e computadores ao filtrar.
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-Filter-containers
- atributo msDS-FilterContainers do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087085"
---
# <a name="ms-ds-filter-containers-attribute"></a><span data-ttu-id="c455e-105">atributo ms-DS-Filter-containers</span><span class="sxs-lookup"><span data-stu-id="c455e-105">ms-DS-Filter-Containers attribute</span></span>

<span data-ttu-id="c455e-106">Uma cadeia de caracteres com valores múltiplos que contém os nomes das classes usadas para determinar quais tipos de contêiner devem ser mostrados pelo snap-in Active Directory usuários e computadores ao filtrar.</span><span class="sxs-lookup"><span data-stu-id="c455e-106">A multiple-valued string that contains the names of classes used to determine which container types should be shown by the Active Directory Users and Computers snap-in when filtering.</span></span>



| <span data-ttu-id="c455e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c455e-107">Entry</span></span> | <span data-ttu-id="c455e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c455e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c455e-109">CN</span><span class="sxs-lookup"><span data-stu-id="c455e-109">CN</span></span>                | <span data-ttu-id="c455e-110">ms-DS-Filter-containers</span><span class="sxs-lookup"><span data-stu-id="c455e-110">ms-DS-Filter-Containers</span></span>                     |
| <span data-ttu-id="c455e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c455e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c455e-112">msDS-FilterContainers</span><span class="sxs-lookup"><span data-stu-id="c455e-112">msDS-FilterContainers</span></span>                       |
| <span data-ttu-id="c455e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c455e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c455e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c455e-114">Update Privilege</span></span>  | <span data-ttu-id="c455e-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="c455e-115">Domain administrator</span></span>                        |
| <span data-ttu-id="c455e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c455e-116">Update Frequency</span></span>  | <span data-ttu-id="c455e-117">Quando a lista de tipos de contêiner é alterada.</span><span class="sxs-lookup"><span data-stu-id="c455e-117">When the list of container types changes.</span></span>   |
| <span data-ttu-id="c455e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c455e-118">Attribute-Id</span></span>      | <span data-ttu-id="c455e-119">1.2.840.113556.1.4.1703</span><span class="sxs-lookup"><span data-stu-id="c455e-119">1.2.840.113556.1.4.1703</span></span>                     |
| <span data-ttu-id="c455e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c455e-120">System-Id-Guid</span></span>    | <span data-ttu-id="c455e-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span><span class="sxs-lookup"><span data-stu-id="c455e-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span></span>        |
| <span data-ttu-id="c455e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c455e-122">Syntax</span></span>            | [<span data-ttu-id="c455e-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c455e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c455e-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="c455e-124">Implementations</span></span>

-   [<span data-ttu-id="c455e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c455e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c455e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c455e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c455e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c455e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c455e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c455e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c455e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c455e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c455e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c455e-130">Windows Server 2003</span></span>



| <span data-ttu-id="c455e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c455e-131">Entry</span></span> | <span data-ttu-id="c455e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c455e-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c455e-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="c455e-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c455e-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c455e-135">System-Only</span></span>            | <span data-ttu-id="c455e-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-136">False</span></span>                                               |
| <span data-ttu-id="c455e-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c455e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c455e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-138">False</span></span>                                               |
| <span data-ttu-id="c455e-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="c455e-139">Is Indexed</span></span>             | <span data-ttu-id="c455e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-140">False</span></span>                                               |
| <span data-ttu-id="c455e-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c455e-141">In Global Catalog</span></span>      | <span data-ttu-id="c455e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-142">False</span></span>                                               |
| <span data-ttu-id="c455e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c455e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c455e-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c455e-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c455e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c455e-145">Range-Lower</span></span>            | <span data-ttu-id="c455e-146">1</span><span class="sxs-lookup"><span data-stu-id="c455e-146">1</span></span>                                                   |
| <span data-ttu-id="c455e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c455e-147">Range-Upper</span></span>            | <span data-ttu-id="c455e-148">64</span><span class="sxs-lookup"><span data-stu-id="c455e-148">64</span></span>                                                  |
| <span data-ttu-id="c455e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-149">Search-Flags</span></span>           | <span data-ttu-id="c455e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c455e-150">0x00000000</span></span>                                          |
| <span data-ttu-id="c455e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-151">System-Flags</span></span>           | <span data-ttu-id="c455e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c455e-152">0x00000010</span></span>                                          |
| <span data-ttu-id="c455e-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c455e-153">Classes used in</span></span>        | [<span data-ttu-id="c455e-154">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="c455e-154">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c455e-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c455e-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c455e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="c455e-156">Entry</span></span> | <span data-ttu-id="c455e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="c455e-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c455e-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="c455e-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c455e-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c455e-160">System-Only</span></span>            | <span data-ttu-id="c455e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-161">False</span></span>                                               |
| <span data-ttu-id="c455e-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c455e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c455e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-163">False</span></span>                                               |
| <span data-ttu-id="c455e-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="c455e-164">Is Indexed</span></span>             | <span data-ttu-id="c455e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-165">False</span></span>                                               |
| <span data-ttu-id="c455e-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c455e-166">In Global Catalog</span></span>      | <span data-ttu-id="c455e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-167">False</span></span>                                               |
| <span data-ttu-id="c455e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c455e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c455e-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c455e-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c455e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c455e-170">Range-Lower</span></span>            | <span data-ttu-id="c455e-171">1</span><span class="sxs-lookup"><span data-stu-id="c455e-171">1</span></span>                                                   |
| <span data-ttu-id="c455e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c455e-172">Range-Upper</span></span>            | <span data-ttu-id="c455e-173">64</span><span class="sxs-lookup"><span data-stu-id="c455e-173">64</span></span>                                                  |
| <span data-ttu-id="c455e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-174">Search-Flags</span></span>           | <span data-ttu-id="c455e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c455e-175">0x00000000</span></span>                                          |
| <span data-ttu-id="c455e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-176">System-Flags</span></span>           | <span data-ttu-id="c455e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c455e-177">0x00000010</span></span>                                          |
| <span data-ttu-id="c455e-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c455e-178">Classes used in</span></span>        | [<span data-ttu-id="c455e-179">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="c455e-179">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c455e-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c455e-180">Windows Server 2008</span></span>



| <span data-ttu-id="c455e-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c455e-181">Entry</span></span> | <span data-ttu-id="c455e-182">Valor</span><span class="sxs-lookup"><span data-stu-id="c455e-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c455e-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="c455e-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c455e-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c455e-185">System-Only</span></span>            | <span data-ttu-id="c455e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-186">False</span></span>                                               |
| <span data-ttu-id="c455e-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c455e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c455e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-188">False</span></span>                                               |
| <span data-ttu-id="c455e-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="c455e-189">Is Indexed</span></span>             | <span data-ttu-id="c455e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-190">False</span></span>                                               |
| <span data-ttu-id="c455e-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c455e-191">In Global Catalog</span></span>      | <span data-ttu-id="c455e-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-192">False</span></span>                                               |
| <span data-ttu-id="c455e-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c455e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c455e-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c455e-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c455e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c455e-195">Range-Lower</span></span>            | <span data-ttu-id="c455e-196">1</span><span class="sxs-lookup"><span data-stu-id="c455e-196">1</span></span>                                                   |
| <span data-ttu-id="c455e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c455e-197">Range-Upper</span></span>            | <span data-ttu-id="c455e-198">64</span><span class="sxs-lookup"><span data-stu-id="c455e-198">64</span></span>                                                  |
| <span data-ttu-id="c455e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-199">Search-Flags</span></span>           | <span data-ttu-id="c455e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c455e-200">0x00000000</span></span>                                          |
| <span data-ttu-id="c455e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-201">System-Flags</span></span>           | <span data-ttu-id="c455e-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c455e-202">0x00000010</span></span>                                          |
| <span data-ttu-id="c455e-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c455e-203">Classes used in</span></span>        | [<span data-ttu-id="c455e-204">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="c455e-204">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c455e-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c455e-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c455e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="c455e-206">Entry</span></span> | <span data-ttu-id="c455e-207">Valor</span><span class="sxs-lookup"><span data-stu-id="c455e-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c455e-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="c455e-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c455e-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c455e-210">System-Only</span></span>            | <span data-ttu-id="c455e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-211">False</span></span>                                               |
| <span data-ttu-id="c455e-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c455e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c455e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-213">False</span></span>                                               |
| <span data-ttu-id="c455e-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="c455e-214">Is Indexed</span></span>             | <span data-ttu-id="c455e-215">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-215">False</span></span>                                               |
| <span data-ttu-id="c455e-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c455e-216">In Global Catalog</span></span>      | <span data-ttu-id="c455e-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-217">False</span></span>                                               |
| <span data-ttu-id="c455e-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c455e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c455e-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c455e-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c455e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c455e-220">Range-Lower</span></span>            | <span data-ttu-id="c455e-221">1</span><span class="sxs-lookup"><span data-stu-id="c455e-221">1</span></span>                                                   |
| <span data-ttu-id="c455e-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c455e-222">Range-Upper</span></span>            | <span data-ttu-id="c455e-223">64</span><span class="sxs-lookup"><span data-stu-id="c455e-223">64</span></span>                                                  |
| <span data-ttu-id="c455e-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-224">Search-Flags</span></span>           | <span data-ttu-id="c455e-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c455e-225">0x00000000</span></span>                                          |
| <span data-ttu-id="c455e-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-226">System-Flags</span></span>           | <span data-ttu-id="c455e-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c455e-227">0x00000010</span></span>                                          |
| <span data-ttu-id="c455e-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c455e-228">Classes used in</span></span>        | [<span data-ttu-id="c455e-229">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="c455e-229">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c455e-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c455e-230">Windows Server 2012</span></span>



| <span data-ttu-id="c455e-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="c455e-231">Entry</span></span> | <span data-ttu-id="c455e-232">Valor</span><span class="sxs-lookup"><span data-stu-id="c455e-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c455e-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="c455e-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c455e-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c455e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="c455e-235">System-Only</span></span>            | <span data-ttu-id="c455e-236">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-236">False</span></span>                                               |
| <span data-ttu-id="c455e-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c455e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="c455e-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-238">False</span></span>                                               |
| <span data-ttu-id="c455e-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="c455e-239">Is Indexed</span></span>             | <span data-ttu-id="c455e-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-240">False</span></span>                                               |
| <span data-ttu-id="c455e-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c455e-241">In Global Catalog</span></span>      | <span data-ttu-id="c455e-242">Falso</span><span class="sxs-lookup"><span data-stu-id="c455e-242">False</span></span>                                               |
| <span data-ttu-id="c455e-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c455e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="c455e-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c455e-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c455e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c455e-245">Range-Lower</span></span>            | <span data-ttu-id="c455e-246">1</span><span class="sxs-lookup"><span data-stu-id="c455e-246">1</span></span>                                                   |
| <span data-ttu-id="c455e-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c455e-247">Range-Upper</span></span>            | <span data-ttu-id="c455e-248">64</span><span class="sxs-lookup"><span data-stu-id="c455e-248">64</span></span>                                                  |
| <span data-ttu-id="c455e-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-249">Search-Flags</span></span>           | <span data-ttu-id="c455e-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c455e-250">0x00000000</span></span>                                          |
| <span data-ttu-id="c455e-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c455e-251">System-Flags</span></span>           | <span data-ttu-id="c455e-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c455e-252">0x00000010</span></span>                                          |
| <span data-ttu-id="c455e-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c455e-253">Classes used in</span></span>        | [<span data-ttu-id="c455e-254">**DS-UI-Settings**</span><span class="sxs-lookup"><span data-stu-id="c455e-254">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





