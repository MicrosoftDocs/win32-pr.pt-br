---
title: Atributo MSI-script-Path
description: O caminho do arquivo de script de anúncio do Microsoft Installer para este aplicativo.
ms.assetid: 6ebe172c-42fc-4a36-940e-a48315d6496c
ms.tgt_platform: multiple
keywords:
- MSI-script-Path-esquema de atributo do AD
- Esquema de AD do atributo msiScriptPath
topic_type:
- apiref
api_name:
- Msi-Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ecce0bb7c082666136e69be8179cf3c5cdf7a6d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086913"
---
# <a name="msi-script-path-attribute"></a><span data-ttu-id="fc78e-105">Atributo MSI-script-Path</span><span class="sxs-lookup"><span data-stu-id="fc78e-105">Msi-Script-Path attribute</span></span>

<span data-ttu-id="fc78e-106">O caminho do arquivo de script de anúncio do Microsoft Installer para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc78e-106">The file path for the Microsoft installer advertisement script file for this application.</span></span>



| <span data-ttu-id="fc78e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-107">Entry</span></span> | <span data-ttu-id="fc78e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fc78e-109">CN</span><span class="sxs-lookup"><span data-stu-id="fc78e-109">CN</span></span>                | <span data-ttu-id="fc78e-110">MSI-script-Path</span><span class="sxs-lookup"><span data-stu-id="fc78e-110">Msi-Script-Path</span></span>                             |
| <span data-ttu-id="fc78e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fc78e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fc78e-112">msiScriptPath</span><span class="sxs-lookup"><span data-stu-id="fc78e-112">msiScriptPath</span></span>                               |
| <span data-ttu-id="fc78e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="fc78e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="fc78e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="fc78e-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fc78e-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="fc78e-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="fc78e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-116">Attribute-Id</span></span>      | <span data-ttu-id="fc78e-117">1.2.840.113556.1.4.15</span><span class="sxs-lookup"><span data-stu-id="fc78e-117">1.2.840.113556.1.4.15</span></span>                       |
| <span data-ttu-id="fc78e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fc78e-118">System-Id-Guid</span></span>    | <span data-ttu-id="fc78e-119">bf967937-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fc78e-119">bf967937-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="fc78e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc78e-120">Syntax</span></span>            | [<span data-ttu-id="fc78e-121">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fc78e-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fc78e-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="fc78e-122">Implementations</span></span>

-   [<span data-ttu-id="fc78e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fc78e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fc78e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fc78e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fc78e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fc78e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fc78e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fc78e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fc78e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fc78e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fc78e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fc78e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fc78e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc78e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="fc78e-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-130">Entry</span></span> | <span data-ttu-id="fc78e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fc78e-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="fc78e-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc78e-134">System-Only</span></span>            | <span data-ttu-id="fc78e-135">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-135">False</span></span>                                                            |
| <span data-ttu-id="fc78e-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fc78e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="fc78e-137">True</span><span class="sxs-lookup"><span data-stu-id="fc78e-137">True</span></span>                                                             |
| <span data-ttu-id="fc78e-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="fc78e-138">Is Indexed</span></span>             | <span data-ttu-id="fc78e-139">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-139">False</span></span>                                                            |
| <span data-ttu-id="fc78e-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fc78e-140">In Global Catalog</span></span>      | <span data-ttu-id="fc78e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-141">False</span></span>                                                            |
| <span data-ttu-id="fc78e-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fc78e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc78e-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fc78e-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="fc78e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc78e-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc78e-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-146">Search-Flags</span></span>           | <span data-ttu-id="fc78e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc78e-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="fc78e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-148">System-Flags</span></span>           | <span data-ttu-id="fc78e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fc78e-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="fc78e-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fc78e-150">Classes used in</span></span>        | [<span data-ttu-id="fc78e-151">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="fc78e-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fc78e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc78e-152">Windows Server 2003</span></span>



| <span data-ttu-id="fc78e-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-153">Entry</span></span> | <span data-ttu-id="fc78e-154">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fc78e-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="fc78e-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc78e-157">System-Only</span></span>            | <span data-ttu-id="fc78e-158">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-158">False</span></span>                                                            |
| <span data-ttu-id="fc78e-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fc78e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="fc78e-160">True</span><span class="sxs-lookup"><span data-stu-id="fc78e-160">True</span></span>                                                             |
| <span data-ttu-id="fc78e-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="fc78e-161">Is Indexed</span></span>             | <span data-ttu-id="fc78e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-162">False</span></span>                                                            |
| <span data-ttu-id="fc78e-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fc78e-163">In Global Catalog</span></span>      | <span data-ttu-id="fc78e-164">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-164">False</span></span>                                                            |
| <span data-ttu-id="fc78e-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fc78e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc78e-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fc78e-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="fc78e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc78e-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc78e-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-169">Search-Flags</span></span>           | <span data-ttu-id="fc78e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc78e-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="fc78e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-171">System-Flags</span></span>           | <span data-ttu-id="fc78e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fc78e-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="fc78e-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fc78e-173">Classes used in</span></span>        | [<span data-ttu-id="fc78e-174">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="fc78e-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fc78e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fc78e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fc78e-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-176">Entry</span></span> | <span data-ttu-id="fc78e-177">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fc78e-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="fc78e-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc78e-180">System-Only</span></span>            | <span data-ttu-id="fc78e-181">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-181">False</span></span>                                                            |
| <span data-ttu-id="fc78e-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fc78e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="fc78e-183">True</span><span class="sxs-lookup"><span data-stu-id="fc78e-183">True</span></span>                                                             |
| <span data-ttu-id="fc78e-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="fc78e-184">Is Indexed</span></span>             | <span data-ttu-id="fc78e-185">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-185">False</span></span>                                                            |
| <span data-ttu-id="fc78e-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fc78e-186">In Global Catalog</span></span>      | <span data-ttu-id="fc78e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-187">False</span></span>                                                            |
| <span data-ttu-id="fc78e-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fc78e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc78e-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fc78e-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="fc78e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc78e-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc78e-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-192">Search-Flags</span></span>           | <span data-ttu-id="fc78e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc78e-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="fc78e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-194">System-Flags</span></span>           | <span data-ttu-id="fc78e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fc78e-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="fc78e-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fc78e-196">Classes used in</span></span>        | [<span data-ttu-id="fc78e-197">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="fc78e-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fc78e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc78e-198">Windows Server 2008</span></span>



| <span data-ttu-id="fc78e-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-199">Entry</span></span> | <span data-ttu-id="fc78e-200">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fc78e-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="fc78e-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc78e-203">System-Only</span></span>            | <span data-ttu-id="fc78e-204">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-204">False</span></span>                                                            |
| <span data-ttu-id="fc78e-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fc78e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="fc78e-206">True</span><span class="sxs-lookup"><span data-stu-id="fc78e-206">True</span></span>                                                             |
| <span data-ttu-id="fc78e-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="fc78e-207">Is Indexed</span></span>             | <span data-ttu-id="fc78e-208">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-208">False</span></span>                                                            |
| <span data-ttu-id="fc78e-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fc78e-209">In Global Catalog</span></span>      | <span data-ttu-id="fc78e-210">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-210">False</span></span>                                                            |
| <span data-ttu-id="fc78e-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fc78e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc78e-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fc78e-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="fc78e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc78e-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc78e-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-215">Search-Flags</span></span>           | <span data-ttu-id="fc78e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc78e-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="fc78e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-217">System-Flags</span></span>           | <span data-ttu-id="fc78e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fc78e-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="fc78e-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fc78e-219">Classes used in</span></span>        | [<span data-ttu-id="fc78e-220">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="fc78e-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fc78e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fc78e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fc78e-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-222">Entry</span></span> | <span data-ttu-id="fc78e-223">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fc78e-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="fc78e-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc78e-226">System-Only</span></span>            | <span data-ttu-id="fc78e-227">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-227">False</span></span>                                                            |
| <span data-ttu-id="fc78e-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fc78e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="fc78e-229">True</span><span class="sxs-lookup"><span data-stu-id="fc78e-229">True</span></span>                                                             |
| <span data-ttu-id="fc78e-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="fc78e-230">Is Indexed</span></span>             | <span data-ttu-id="fc78e-231">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-231">False</span></span>                                                            |
| <span data-ttu-id="fc78e-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fc78e-232">In Global Catalog</span></span>      | <span data-ttu-id="fc78e-233">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-233">False</span></span>                                                            |
| <span data-ttu-id="fc78e-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fc78e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc78e-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fc78e-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="fc78e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc78e-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc78e-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-238">Search-Flags</span></span>           | <span data-ttu-id="fc78e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc78e-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="fc78e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-240">System-Flags</span></span>           | <span data-ttu-id="fc78e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fc78e-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="fc78e-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fc78e-242">Classes used in</span></span>        | [<span data-ttu-id="fc78e-243">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="fc78e-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fc78e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fc78e-244">Windows Server 2012</span></span>



| <span data-ttu-id="fc78e-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="fc78e-245">Entry</span></span> | <span data-ttu-id="fc78e-246">Valor</span><span class="sxs-lookup"><span data-stu-id="fc78e-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="fc78e-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="fc78e-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fc78e-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="fc78e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="fc78e-249">System-Only</span></span>            | <span data-ttu-id="fc78e-250">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-250">False</span></span>                                                            |
| <span data-ttu-id="fc78e-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fc78e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="fc78e-252">True</span><span class="sxs-lookup"><span data-stu-id="fc78e-252">True</span></span>                                                             |
| <span data-ttu-id="fc78e-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="fc78e-253">Is Indexed</span></span>             | <span data-ttu-id="fc78e-254">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-254">False</span></span>                                                            |
| <span data-ttu-id="fc78e-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fc78e-255">In Global Catalog</span></span>      | <span data-ttu-id="fc78e-256">Falso</span><span class="sxs-lookup"><span data-stu-id="fc78e-256">False</span></span>                                                            |
| <span data-ttu-id="fc78e-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fc78e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="fc78e-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fc78e-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="fc78e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fc78e-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fc78e-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="fc78e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-261">Search-Flags</span></span>           | <span data-ttu-id="fc78e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fc78e-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="fc78e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fc78e-263">System-Flags</span></span>           | <span data-ttu-id="fc78e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fc78e-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="fc78e-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fc78e-265">Classes used in</span></span>        | [<span data-ttu-id="fc78e-266">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="fc78e-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





