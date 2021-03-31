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
# <a name="localization-display-id-attribute"></a><span data-ttu-id="d69bc-105">Localização-exibição-atributo de ID</span><span class="sxs-lookup"><span data-stu-id="d69bc-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="d69bc-106">Usado para indexar no arquivo Extrts.mc para obter o displayName localizado para os objetos para fins de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d69bc-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="d69bc-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-107">Entry</span></span> | <span data-ttu-id="d69bc-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d69bc-109">CN</span><span class="sxs-lookup"><span data-stu-id="d69bc-109">CN</span></span>                | <span data-ttu-id="d69bc-110">Localização-exibição-ID</span><span class="sxs-lookup"><span data-stu-id="d69bc-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="d69bc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d69bc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d69bc-112">localizationDisplayId</span><span class="sxs-lookup"><span data-stu-id="d69bc-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="d69bc-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d69bc-113">Size</span></span>              | <span data-ttu-id="d69bc-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="d69bc-114">4 bytes</span></span>                              |
| <span data-ttu-id="d69bc-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d69bc-115">Update Privilege</span></span>  | <span data-ttu-id="d69bc-116">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="d69bc-116">Schema administrator</span></span>                 |
| <span data-ttu-id="d69bc-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d69bc-117">Update Frequency</span></span>  | <span data-ttu-id="d69bc-118">Uma ID nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="d69bc-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="d69bc-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-119">Attribute-Id</span></span>      | <span data-ttu-id="d69bc-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="d69bc-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="d69bc-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d69bc-121">System-Id-Guid</span></span>    | <span data-ttu-id="d69bc-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="d69bc-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="d69bc-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d69bc-123">Syntax</span></span>            | [<span data-ttu-id="d69bc-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="d69bc-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d69bc-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="d69bc-125">Implementations</span></span>

-   [<span data-ttu-id="d69bc-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d69bc-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d69bc-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d69bc-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d69bc-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d69bc-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d69bc-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d69bc-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d69bc-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d69bc-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d69bc-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d69bc-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d69bc-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d69bc-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d69bc-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d69bc-133">Windows 2000 Server</span></span>



| <span data-ttu-id="d69bc-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-134">Entry</span></span> | <span data-ttu-id="d69bc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-138">System-Only</span></span>            | <span data-ttu-id="d69bc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-139">False</span></span>                                                           |
| <span data-ttu-id="d69bc-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-141">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-141">True</span></span>                                                            |
| <span data-ttu-id="d69bc-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-142">Is Indexed</span></span>             | <span data-ttu-id="d69bc-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-143">False</span></span>                                                           |
| <span data-ttu-id="d69bc-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-144">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-145">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-145">False</span></span>                                                           |
| <span data-ttu-id="d69bc-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-150">Search-Flags</span></span>           | <span data-ttu-id="d69bc-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-152">System-Flags</span></span>           | <span data-ttu-id="d69bc-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-154">Classes used in</span></span>        | [<span data-ttu-id="d69bc-155">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d69bc-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d69bc-156">Windows Server 2003</span></span>



| <span data-ttu-id="d69bc-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-157">Entry</span></span> | <span data-ttu-id="d69bc-158">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-161">System-Only</span></span>            | <span data-ttu-id="d69bc-162">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-162">False</span></span>                                                           |
| <span data-ttu-id="d69bc-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-164">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-164">True</span></span>                                                            |
| <span data-ttu-id="d69bc-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-165">Is Indexed</span></span>             | <span data-ttu-id="d69bc-166">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-166">False</span></span>                                                           |
| <span data-ttu-id="d69bc-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-167">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-168">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-168">False</span></span>                                                           |
| <span data-ttu-id="d69bc-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-173">Search-Flags</span></span>           | <span data-ttu-id="d69bc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-175">System-Flags</span></span>           | <span data-ttu-id="d69bc-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-177">Classes used in</span></span>        | [<span data-ttu-id="d69bc-178">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d69bc-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="d69bc-179">ADAM</span></span>



| <span data-ttu-id="d69bc-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-180">Entry</span></span> | <span data-ttu-id="d69bc-181">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-184">System-Only</span></span>            | <span data-ttu-id="d69bc-185">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-185">False</span></span>                                                           |
| <span data-ttu-id="d69bc-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-187">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-187">True</span></span>                                                            |
| <span data-ttu-id="d69bc-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-188">Is Indexed</span></span>             | <span data-ttu-id="d69bc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-189">False</span></span>                                                           |
| <span data-ttu-id="d69bc-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-190">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-191">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-191">False</span></span>                                                           |
| <span data-ttu-id="d69bc-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-196">Search-Flags</span></span>           | <span data-ttu-id="d69bc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-198">System-Flags</span></span>           | <span data-ttu-id="d69bc-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-200">Classes used in</span></span>        | [<span data-ttu-id="d69bc-201">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d69bc-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d69bc-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d69bc-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-203">Entry</span></span> | <span data-ttu-id="d69bc-204">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-207">System-Only</span></span>            | <span data-ttu-id="d69bc-208">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-208">False</span></span>                                                           |
| <span data-ttu-id="d69bc-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-210">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-210">True</span></span>                                                            |
| <span data-ttu-id="d69bc-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-211">Is Indexed</span></span>             | <span data-ttu-id="d69bc-212">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-212">False</span></span>                                                           |
| <span data-ttu-id="d69bc-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-213">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-214">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-214">False</span></span>                                                           |
| <span data-ttu-id="d69bc-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-219">Search-Flags</span></span>           | <span data-ttu-id="d69bc-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-221">System-Flags</span></span>           | <span data-ttu-id="d69bc-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-223">Classes used in</span></span>        | [<span data-ttu-id="d69bc-224">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d69bc-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d69bc-225">Windows Server 2008</span></span>



| <span data-ttu-id="d69bc-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-226">Entry</span></span> | <span data-ttu-id="d69bc-227">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-230">System-Only</span></span>            | <span data-ttu-id="d69bc-231">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-231">False</span></span>                                                           |
| <span data-ttu-id="d69bc-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-233">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-233">True</span></span>                                                            |
| <span data-ttu-id="d69bc-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-234">Is Indexed</span></span>             | <span data-ttu-id="d69bc-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-235">False</span></span>                                                           |
| <span data-ttu-id="d69bc-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-236">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-237">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-237">False</span></span>                                                           |
| <span data-ttu-id="d69bc-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-242">Search-Flags</span></span>           | <span data-ttu-id="d69bc-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-244">System-Flags</span></span>           | <span data-ttu-id="d69bc-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-246">Classes used in</span></span>        | [<span data-ttu-id="d69bc-247">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d69bc-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d69bc-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d69bc-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-249">Entry</span></span> | <span data-ttu-id="d69bc-250">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-253">System-Only</span></span>            | <span data-ttu-id="d69bc-254">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-254">False</span></span>                                                           |
| <span data-ttu-id="d69bc-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-255">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-256">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-256">True</span></span>                                                            |
| <span data-ttu-id="d69bc-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-257">Is Indexed</span></span>             | <span data-ttu-id="d69bc-258">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-258">False</span></span>                                                           |
| <span data-ttu-id="d69bc-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-259">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-260">False</span></span>                                                           |
| <span data-ttu-id="d69bc-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-265">Search-Flags</span></span>           | <span data-ttu-id="d69bc-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-267">System-Flags</span></span>           | <span data-ttu-id="d69bc-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-269">Classes used in</span></span>        | [<span data-ttu-id="d69bc-270">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d69bc-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d69bc-271">Windows Server 2012</span></span>



| <span data-ttu-id="d69bc-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="d69bc-272">Entry</span></span> | <span data-ttu-id="d69bc-273">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bc-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d69bc-274">ID do link</span><span class="sxs-lookup"><span data-stu-id="d69bc-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d69bc-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="d69bc-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="d69bc-276">System-Only</span></span>            | <span data-ttu-id="d69bc-277">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-277">False</span></span>                                                           |
| <span data-ttu-id="d69bc-278">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d69bc-278">Is-Single-Valued</span></span>       | <span data-ttu-id="d69bc-279">True</span><span class="sxs-lookup"><span data-stu-id="d69bc-279">True</span></span>                                                            |
| <span data-ttu-id="d69bc-280">É indexado</span><span class="sxs-lookup"><span data-stu-id="d69bc-280">Is Indexed</span></span>             | <span data-ttu-id="d69bc-281">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-281">False</span></span>                                                           |
| <span data-ttu-id="d69bc-282">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d69bc-282">In Global Catalog</span></span>      | <span data-ttu-id="d69bc-283">Falso</span><span class="sxs-lookup"><span data-stu-id="d69bc-283">False</span></span>                                                           |
| <span data-ttu-id="d69bc-284">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d69bc-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="d69bc-285">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d69bc-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="d69bc-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d69bc-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d69bc-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="d69bc-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-288">Search-Flags</span></span>           | <span data-ttu-id="d69bc-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d69bc-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="d69bc-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d69bc-290">System-Flags</span></span>           | <span data-ttu-id="d69bc-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d69bc-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="d69bc-292">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d69bc-292">Classes used in</span></span>        | [<span data-ttu-id="d69bc-293">**Controle-acesso-à direita**</span><span class="sxs-lookup"><span data-stu-id="d69bc-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





