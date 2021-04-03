---
title: Localização-exibição-atributo de ID
description: Usado para indexar no arquivo Extrts.mc para obter o displayName localizado para os objetos para fins de interface do usuário.
ms.assetid: ed99d499-0064-4832-81ad-75fb3c8c548d
ms.tgt_platform: multiple
keywords:
- Localização-exibição-esquema do atributo de ID do AD
- Esquema de AD do atributo localizationDisplayId
topic_type:
- apiref
api_name:
- Localization-Display-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4d9453b04bd5c944784b68ff5e4442f00bf65f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645475"
---
# <a name="localization-display-id-attribute"></a><span data-ttu-id="21bb5-105">Localização-exibição-atributo de ID</span><span class="sxs-lookup"><span data-stu-id="21bb5-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="21bb5-106">Usado para indexar no arquivo Extrts.mc para obter o displayName localizado para os objetos para fins de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="21bb5-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="21bb5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-107">Entry</span></span> | <span data-ttu-id="21bb5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="21bb5-109">CN</span><span class="sxs-lookup"><span data-stu-id="21bb5-109">CN</span></span>                | <span data-ttu-id="21bb5-110">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="21bb5-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="21bb5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="21bb5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="21bb5-112">localizationDisplayId</span><span class="sxs-lookup"><span data-stu-id="21bb5-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="21bb5-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="21bb5-113">Size</span></span>              | <span data-ttu-id="21bb5-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="21bb5-114">4 bytes</span></span>                              |
| <span data-ttu-id="21bb5-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="21bb5-115">Update Privilege</span></span>  | <span data-ttu-id="21bb5-116">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="21bb5-116">Schema administrator</span></span>                 |
| <span data-ttu-id="21bb5-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="21bb5-117">Update Frequency</span></span>  | <span data-ttu-id="21bb5-118">Uma ID nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="21bb5-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="21bb5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-119">Attribute-Id</span></span>      | <span data-ttu-id="21bb5-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="21bb5-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="21bb5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="21bb5-121">System-Id-Guid</span></span>    | <span data-ttu-id="21bb5-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="21bb5-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="21bb5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="21bb5-123">Syntax</span></span>            | [<span data-ttu-id="21bb5-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="21bb5-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="21bb5-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="21bb5-125">Implementations</span></span>

-   [<span data-ttu-id="21bb5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21bb5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21bb5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21bb5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21bb5-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="21bb5-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="21bb5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21bb5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21bb5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21bb5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21bb5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21bb5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21bb5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21bb5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21bb5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21bb5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="21bb5-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-134">Entry</span></span> | <span data-ttu-id="21bb5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-138">System-Only</span></span>            | <span data-ttu-id="21bb5-139">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-139">False</span></span>                                                           |
| <span data-ttu-id="21bb5-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-141">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-141">True</span></span>                                                            |
| <span data-ttu-id="21bb5-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-142">Is Indexed</span></span>             | <span data-ttu-id="21bb5-143">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-143">False</span></span>                                                           |
| <span data-ttu-id="21bb5-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-144">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-145">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-145">False</span></span>                                                           |
| <span data-ttu-id="21bb5-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-150">Search-Flags</span></span>           | <span data-ttu-id="21bb5-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-152">System-Flags</span></span>           | <span data-ttu-id="21bb5-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-154">Classes used in</span></span>        | [<span data-ttu-id="21bb5-155">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21bb5-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21bb5-156">Windows Server 2003</span></span>



| <span data-ttu-id="21bb5-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-157">Entry</span></span> | <span data-ttu-id="21bb5-158">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-161">System-Only</span></span>            | <span data-ttu-id="21bb5-162">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-162">False</span></span>                                                           |
| <span data-ttu-id="21bb5-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-163">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-164">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-164">True</span></span>                                                            |
| <span data-ttu-id="21bb5-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-165">Is Indexed</span></span>             | <span data-ttu-id="21bb5-166">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-166">False</span></span>                                                           |
| <span data-ttu-id="21bb5-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-167">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-168">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-168">False</span></span>                                                           |
| <span data-ttu-id="21bb5-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-173">Search-Flags</span></span>           | <span data-ttu-id="21bb5-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-175">System-Flags</span></span>           | <span data-ttu-id="21bb5-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-177">Classes used in</span></span>        | [<span data-ttu-id="21bb5-178">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="21bb5-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="21bb5-179">ADAM</span></span>



| <span data-ttu-id="21bb5-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-180">Entry</span></span> | <span data-ttu-id="21bb5-181">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-184">System-Only</span></span>            | <span data-ttu-id="21bb5-185">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-185">False</span></span>                                                           |
| <span data-ttu-id="21bb5-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-186">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-187">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-187">True</span></span>                                                            |
| <span data-ttu-id="21bb5-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-188">Is Indexed</span></span>             | <span data-ttu-id="21bb5-189">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-189">False</span></span>                                                           |
| <span data-ttu-id="21bb5-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-190">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-191">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-191">False</span></span>                                                           |
| <span data-ttu-id="21bb5-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-196">Search-Flags</span></span>           | <span data-ttu-id="21bb5-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-198">System-Flags</span></span>           | <span data-ttu-id="21bb5-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-200">Classes used in</span></span>        | [<span data-ttu-id="21bb5-201">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21bb5-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21bb5-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21bb5-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-203">Entry</span></span> | <span data-ttu-id="21bb5-204">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-207">System-Only</span></span>            | <span data-ttu-id="21bb5-208">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-208">False</span></span>                                                           |
| <span data-ttu-id="21bb5-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-209">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-210">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-210">True</span></span>                                                            |
| <span data-ttu-id="21bb5-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-211">Is Indexed</span></span>             | <span data-ttu-id="21bb5-212">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-212">False</span></span>                                                           |
| <span data-ttu-id="21bb5-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-213">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-214">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-214">False</span></span>                                                           |
| <span data-ttu-id="21bb5-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-219">Search-Flags</span></span>           | <span data-ttu-id="21bb5-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-221">System-Flags</span></span>           | <span data-ttu-id="21bb5-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-223">Classes used in</span></span>        | [<span data-ttu-id="21bb5-224">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21bb5-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21bb5-225">Windows Server 2008</span></span>



| <span data-ttu-id="21bb5-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-226">Entry</span></span> | <span data-ttu-id="21bb5-227">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-230">System-Only</span></span>            | <span data-ttu-id="21bb5-231">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-231">False</span></span>                                                           |
| <span data-ttu-id="21bb5-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-232">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-233">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-233">True</span></span>                                                            |
| <span data-ttu-id="21bb5-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-234">Is Indexed</span></span>             | <span data-ttu-id="21bb5-235">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-235">False</span></span>                                                           |
| <span data-ttu-id="21bb5-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-236">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-237">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-237">False</span></span>                                                           |
| <span data-ttu-id="21bb5-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-242">Search-Flags</span></span>           | <span data-ttu-id="21bb5-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-244">System-Flags</span></span>           | <span data-ttu-id="21bb5-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-246">Classes used in</span></span>        | [<span data-ttu-id="21bb5-247">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21bb5-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21bb5-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21bb5-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-249">Entry</span></span> | <span data-ttu-id="21bb5-250">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-253">System-Only</span></span>            | <span data-ttu-id="21bb5-254">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-254">False</span></span>                                                           |
| <span data-ttu-id="21bb5-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-255">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-256">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-256">True</span></span>                                                            |
| <span data-ttu-id="21bb5-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-257">Is Indexed</span></span>             | <span data-ttu-id="21bb5-258">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-258">False</span></span>                                                           |
| <span data-ttu-id="21bb5-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-259">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-260">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-260">False</span></span>                                                           |
| <span data-ttu-id="21bb5-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-265">Search-Flags</span></span>           | <span data-ttu-id="21bb5-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-267">System-Flags</span></span>           | <span data-ttu-id="21bb5-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-269">Classes used in</span></span>        | [<span data-ttu-id="21bb5-270">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21bb5-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21bb5-271">Windows Server 2012</span></span>



| <span data-ttu-id="21bb5-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="21bb5-272">Entry</span></span> | <span data-ttu-id="21bb5-273">Valor</span><span class="sxs-lookup"><span data-stu-id="21bb5-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="21bb5-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="21bb5-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21bb5-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="21bb5-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="21bb5-276">System-Only</span></span>            | <span data-ttu-id="21bb5-277">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-277">False</span></span>                                                           |
| <span data-ttu-id="21bb5-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21bb5-278">Is-Single-Valued</span></span>       | <span data-ttu-id="21bb5-279">True</span><span class="sxs-lookup"><span data-stu-id="21bb5-279">True</span></span>                                                            |
| <span data-ttu-id="21bb5-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="21bb5-280">Is Indexed</span></span>             | <span data-ttu-id="21bb5-281">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-281">False</span></span>                                                           |
| <span data-ttu-id="21bb5-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21bb5-282">In Global Catalog</span></span>      | <span data-ttu-id="21bb5-283">Falso</span><span class="sxs-lookup"><span data-stu-id="21bb5-283">False</span></span>                                                           |
| <span data-ttu-id="21bb5-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21bb5-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="21bb5-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21bb5-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="21bb5-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21bb5-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21bb5-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="21bb5-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-288">Search-Flags</span></span>           | <span data-ttu-id="21bb5-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21bb5-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="21bb5-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21bb5-290">System-Flags</span></span>           | <span data-ttu-id="21bb5-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21bb5-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="21bb5-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21bb5-292">Classes used in</span></span>        | [<span data-ttu-id="21bb5-293">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="21bb5-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





