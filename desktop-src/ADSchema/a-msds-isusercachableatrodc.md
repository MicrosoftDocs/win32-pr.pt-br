---
title: atributo ms-DS-is-User-armazenável-at-RODC
description: Para um RODC (controlador de domínio Read-Only), identifica se os segredos do usuário especificado podem ser armazenados em cache.
ms.assetid: 1118d0a9-2219-478a-82b0-8ea4bbeae47d
ms.tgt_platform: multiple
keywords:
- ms-DS-is-User-armazenável-at-RODC atributo AD Schema
- atributo msDS-IsUserCachableAtRodc do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Is-User-Cachable-At-Rodc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5699208cebe4c49321186813a64611f79ec52f4b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645563"
---
# <a name="ms-ds-is-user-cachable-at-rodc-attribute"></a><span data-ttu-id="7c267-105">atributo ms-DS-is-User-armazenável-at-RODC</span><span class="sxs-lookup"><span data-stu-id="7c267-105">ms-DS-Is-User-Cachable-At-Rodc attribute</span></span>

<span data-ttu-id="7c267-106">Para um RODC (controlador de domínio Read-Only), identifica se os segredos do usuário especificado podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="7c267-106">For a Read-Only Domain Controller (RODC), identifies whether the specified user's secrets can be cached.</span></span>



| <span data-ttu-id="7c267-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c267-107">Entry</span></span> | <span data-ttu-id="7c267-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7c267-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7c267-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c267-109">CN</span></span>                | <span data-ttu-id="7c267-110">ms-DS-is-User-armazenável-at-RODC</span><span class="sxs-lookup"><span data-stu-id="7c267-110">ms-DS-Is-User-Cachable-At-Rodc</span></span>       |
| <span data-ttu-id="7c267-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7c267-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7c267-112">msDS-IsUserCachableAtRodc</span><span class="sxs-lookup"><span data-stu-id="7c267-112">msDS-IsUserCachableAtRodc</span></span>            |
| <span data-ttu-id="7c267-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7c267-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="7c267-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7c267-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7c267-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7c267-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7c267-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c267-116">Attribute-Id</span></span>      | <span data-ttu-id="7c267-117">1.2.840.113556.1.4.2025</span><span class="sxs-lookup"><span data-stu-id="7c267-117">1.2.840.113556.1.4.2025</span></span>              |
| <span data-ttu-id="7c267-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7c267-118">System-Id-Guid</span></span>    | <span data-ttu-id="7c267-119">fe01245a-341f-4556-951f-48c033a89050</span><span class="sxs-lookup"><span data-stu-id="7c267-119">fe01245a-341f-4556-951f-48c033a89050</span></span> |
| <span data-ttu-id="7c267-120">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c267-120">Syntax</span></span>            | [<span data-ttu-id="7c267-121">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="7c267-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7c267-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="7c267-122">Implementations</span></span>

-   [<span data-ttu-id="7c267-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c267-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c267-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c267-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c267-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c267-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="7c267-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c267-126">Windows Server 2008</span></span>



| <span data-ttu-id="7c267-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c267-127">Entry</span></span> | <span data-ttu-id="7c267-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7c267-128">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c267-129">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c267-129">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="7c267-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c267-130">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="7c267-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c267-131">System-Only</span></span>            | <span data-ttu-id="7c267-132">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-132">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-133">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c267-133">Is-Single-Valued</span></span>       | <span data-ttu-id="7c267-134">True</span><span class="sxs-lookup"><span data-stu-id="7c267-134">True</span></span>                                                                                                                     |
| <span data-ttu-id="7c267-135">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c267-135">Is Indexed</span></span>             | <span data-ttu-id="7c267-136">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-136">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-137">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c267-137">In Global Catalog</span></span>      | <span data-ttu-id="7c267-138">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-138">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-139">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c267-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c267-140">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c267-140">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="7c267-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c267-141">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="7c267-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c267-142">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="7c267-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c267-143">Search-Flags</span></span>           | <span data-ttu-id="7c267-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c267-144">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="7c267-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c267-145">System-Flags</span></span>           | <span data-ttu-id="7c267-146">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7c267-146">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="7c267-147">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c267-147">Classes used in</span></span>        | [<span data-ttu-id="7c267-148">**Computador**</span><span class="sxs-lookup"><span data-stu-id="7c267-148">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="7c267-149">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7c267-149">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="7c267-150">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="7c267-150">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c267-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c267-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c267-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c267-152">Entry</span></span> | <span data-ttu-id="7c267-153">Valor</span><span class="sxs-lookup"><span data-stu-id="7c267-153">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c267-154">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c267-154">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="7c267-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c267-155">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="7c267-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c267-156">System-Only</span></span>            | <span data-ttu-id="7c267-157">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-157">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-158">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c267-158">Is-Single-Valued</span></span>       | <span data-ttu-id="7c267-159">True</span><span class="sxs-lookup"><span data-stu-id="7c267-159">True</span></span>                                                                                                                     |
| <span data-ttu-id="7c267-160">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c267-160">Is Indexed</span></span>             | <span data-ttu-id="7c267-161">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-161">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-162">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c267-162">In Global Catalog</span></span>      | <span data-ttu-id="7c267-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-163">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-164">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c267-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c267-165">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c267-165">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="7c267-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c267-166">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="7c267-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c267-167">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="7c267-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c267-168">Search-Flags</span></span>           | <span data-ttu-id="7c267-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c267-169">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="7c267-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c267-170">System-Flags</span></span>           | <span data-ttu-id="7c267-171">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7c267-171">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="7c267-172">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c267-172">Classes used in</span></span>        | [<span data-ttu-id="7c267-173">**Computador**</span><span class="sxs-lookup"><span data-stu-id="7c267-173">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="7c267-174">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7c267-174">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="7c267-175">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="7c267-175">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c267-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c267-176">Windows Server 2012</span></span>



| <span data-ttu-id="7c267-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="7c267-177">Entry</span></span> | <span data-ttu-id="7c267-178">Valor</span><span class="sxs-lookup"><span data-stu-id="7c267-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c267-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="7c267-179">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="7c267-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c267-180">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="7c267-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c267-181">System-Only</span></span>            | <span data-ttu-id="7c267-182">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-182">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7c267-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7c267-184">True</span><span class="sxs-lookup"><span data-stu-id="7c267-184">True</span></span>                                                                                                                     |
| <span data-ttu-id="7c267-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="7c267-185">Is Indexed</span></span>             | <span data-ttu-id="7c267-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-186">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7c267-187">In Global Catalog</span></span>      | <span data-ttu-id="7c267-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7c267-188">False</span></span>                                                                                                                    |
| <span data-ttu-id="7c267-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7c267-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c267-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7c267-190">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="7c267-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c267-191">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="7c267-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c267-192">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="7c267-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c267-193">Search-Flags</span></span>           | <span data-ttu-id="7c267-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c267-194">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="7c267-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c267-195">System-Flags</span></span>           | <span data-ttu-id="7c267-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7c267-196">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="7c267-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7c267-197">Classes used in</span></span>        | [<span data-ttu-id="7c267-198">**Computador**</span><span class="sxs-lookup"><span data-stu-id="7c267-198">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="7c267-199">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="7c267-199">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="7c267-200">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="7c267-200">**Server**</span></span>](c-server.md)<br/> |



 

 





