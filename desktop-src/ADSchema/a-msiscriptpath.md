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
# <a name="msi-script-path-attribute"></a><span data-ttu-id="59f66-105">Atributo MSI-script-Path</span><span class="sxs-lookup"><span data-stu-id="59f66-105">Msi-Script-Path attribute</span></span>

<span data-ttu-id="59f66-106">O caminho do arquivo de script de anúncio do Microsoft Installer para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59f66-106">The file path for the Microsoft installer advertisement script file for this application.</span></span>



| <span data-ttu-id="59f66-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-107">Entry</span></span> | <span data-ttu-id="59f66-108">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="59f66-109">CN</span><span class="sxs-lookup"><span data-stu-id="59f66-109">CN</span></span>                | <span data-ttu-id="59f66-110">MSI-script-Path</span><span class="sxs-lookup"><span data-stu-id="59f66-110">Msi-Script-Path</span></span>                             |
| <span data-ttu-id="59f66-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="59f66-111">Ldap-Display-Name</span></span> | <span data-ttu-id="59f66-112">msiScriptPath</span><span class="sxs-lookup"><span data-stu-id="59f66-112">msiScriptPath</span></span>                               |
| <span data-ttu-id="59f66-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="59f66-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="59f66-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="59f66-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="59f66-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="59f66-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="59f66-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-116">Attribute-Id</span></span>      | <span data-ttu-id="59f66-117">1.2.840.113556.1.4.15</span><span class="sxs-lookup"><span data-stu-id="59f66-117">1.2.840.113556.1.4.15</span></span>                       |
| <span data-ttu-id="59f66-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="59f66-118">System-Id-Guid</span></span>    | <span data-ttu-id="59f66-119">bf967937-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="59f66-119">bf967937-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="59f66-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="59f66-120">Syntax</span></span>            | [<span data-ttu-id="59f66-121">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="59f66-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="59f66-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="59f66-122">Implementations</span></span>

-   [<span data-ttu-id="59f66-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="59f66-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="59f66-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="59f66-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="59f66-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="59f66-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="59f66-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="59f66-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="59f66-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="59f66-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="59f66-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="59f66-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="59f66-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59f66-129">Windows 2000 Server</span></span>



| <span data-ttu-id="59f66-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-130">Entry</span></span> | <span data-ttu-id="59f66-131">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="59f66-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="59f66-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="59f66-134">System-Only</span></span>            | <span data-ttu-id="59f66-135">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-135">False</span></span>                                                            |
| <span data-ttu-id="59f66-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="59f66-136">Is-Single-Valued</span></span>       | <span data-ttu-id="59f66-137">True</span><span class="sxs-lookup"><span data-stu-id="59f66-137">True</span></span>                                                             |
| <span data-ttu-id="59f66-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="59f66-138">Is Indexed</span></span>             | <span data-ttu-id="59f66-139">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-139">False</span></span>                                                            |
| <span data-ttu-id="59f66-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="59f66-140">In Global Catalog</span></span>      | <span data-ttu-id="59f66-141">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-141">False</span></span>                                                            |
| <span data-ttu-id="59f66-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59f66-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="59f66-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="59f66-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="59f66-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59f66-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59f66-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-146">Search-Flags</span></span>           | <span data-ttu-id="59f66-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59f66-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="59f66-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-148">System-Flags</span></span>           | <span data-ttu-id="59f66-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59f66-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="59f66-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="59f66-150">Classes used in</span></span>        | [<span data-ttu-id="59f66-151">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="59f66-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="59f66-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59f66-152">Windows Server 2003</span></span>



| <span data-ttu-id="59f66-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-153">Entry</span></span> | <span data-ttu-id="59f66-154">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="59f66-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="59f66-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="59f66-157">System-Only</span></span>            | <span data-ttu-id="59f66-158">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-158">False</span></span>                                                            |
| <span data-ttu-id="59f66-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="59f66-159">Is-Single-Valued</span></span>       | <span data-ttu-id="59f66-160">True</span><span class="sxs-lookup"><span data-stu-id="59f66-160">True</span></span>                                                             |
| <span data-ttu-id="59f66-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="59f66-161">Is Indexed</span></span>             | <span data-ttu-id="59f66-162">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-162">False</span></span>                                                            |
| <span data-ttu-id="59f66-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="59f66-163">In Global Catalog</span></span>      | <span data-ttu-id="59f66-164">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-164">False</span></span>                                                            |
| <span data-ttu-id="59f66-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59f66-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="59f66-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="59f66-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="59f66-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59f66-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59f66-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-169">Search-Flags</span></span>           | <span data-ttu-id="59f66-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59f66-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="59f66-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-171">System-Flags</span></span>           | <span data-ttu-id="59f66-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59f66-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="59f66-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="59f66-173">Classes used in</span></span>        | [<span data-ttu-id="59f66-174">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="59f66-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="59f66-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="59f66-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="59f66-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-176">Entry</span></span> | <span data-ttu-id="59f66-177">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="59f66-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="59f66-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="59f66-180">System-Only</span></span>            | <span data-ttu-id="59f66-181">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-181">False</span></span>                                                            |
| <span data-ttu-id="59f66-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="59f66-182">Is-Single-Valued</span></span>       | <span data-ttu-id="59f66-183">True</span><span class="sxs-lookup"><span data-stu-id="59f66-183">True</span></span>                                                             |
| <span data-ttu-id="59f66-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="59f66-184">Is Indexed</span></span>             | <span data-ttu-id="59f66-185">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-185">False</span></span>                                                            |
| <span data-ttu-id="59f66-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="59f66-186">In Global Catalog</span></span>      | <span data-ttu-id="59f66-187">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-187">False</span></span>                                                            |
| <span data-ttu-id="59f66-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59f66-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="59f66-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="59f66-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="59f66-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59f66-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59f66-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-192">Search-Flags</span></span>           | <span data-ttu-id="59f66-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59f66-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="59f66-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-194">System-Flags</span></span>           | <span data-ttu-id="59f66-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59f66-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="59f66-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="59f66-196">Classes used in</span></span>        | [<span data-ttu-id="59f66-197">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="59f66-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="59f66-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59f66-198">Windows Server 2008</span></span>



| <span data-ttu-id="59f66-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-199">Entry</span></span> | <span data-ttu-id="59f66-200">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="59f66-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="59f66-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="59f66-203">System-Only</span></span>            | <span data-ttu-id="59f66-204">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-204">False</span></span>                                                            |
| <span data-ttu-id="59f66-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="59f66-205">Is-Single-Valued</span></span>       | <span data-ttu-id="59f66-206">True</span><span class="sxs-lookup"><span data-stu-id="59f66-206">True</span></span>                                                             |
| <span data-ttu-id="59f66-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="59f66-207">Is Indexed</span></span>             | <span data-ttu-id="59f66-208">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-208">False</span></span>                                                            |
| <span data-ttu-id="59f66-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="59f66-209">In Global Catalog</span></span>      | <span data-ttu-id="59f66-210">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-210">False</span></span>                                                            |
| <span data-ttu-id="59f66-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59f66-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="59f66-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="59f66-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="59f66-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59f66-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59f66-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-215">Search-Flags</span></span>           | <span data-ttu-id="59f66-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59f66-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="59f66-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-217">System-Flags</span></span>           | <span data-ttu-id="59f66-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59f66-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="59f66-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="59f66-219">Classes used in</span></span>        | [<span data-ttu-id="59f66-220">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="59f66-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="59f66-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59f66-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="59f66-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-222">Entry</span></span> | <span data-ttu-id="59f66-223">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="59f66-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="59f66-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="59f66-226">System-Only</span></span>            | <span data-ttu-id="59f66-227">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-227">False</span></span>                                                            |
| <span data-ttu-id="59f66-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="59f66-228">Is-Single-Valued</span></span>       | <span data-ttu-id="59f66-229">True</span><span class="sxs-lookup"><span data-stu-id="59f66-229">True</span></span>                                                             |
| <span data-ttu-id="59f66-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="59f66-230">Is Indexed</span></span>             | <span data-ttu-id="59f66-231">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-231">False</span></span>                                                            |
| <span data-ttu-id="59f66-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="59f66-232">In Global Catalog</span></span>      | <span data-ttu-id="59f66-233">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-233">False</span></span>                                                            |
| <span data-ttu-id="59f66-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59f66-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="59f66-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="59f66-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="59f66-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59f66-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59f66-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-238">Search-Flags</span></span>           | <span data-ttu-id="59f66-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59f66-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="59f66-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-240">System-Flags</span></span>           | <span data-ttu-id="59f66-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59f66-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="59f66-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="59f66-242">Classes used in</span></span>        | [<span data-ttu-id="59f66-243">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="59f66-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="59f66-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59f66-244">Windows Server 2012</span></span>



| <span data-ttu-id="59f66-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="59f66-245">Entry</span></span> | <span data-ttu-id="59f66-246">Valor</span><span class="sxs-lookup"><span data-stu-id="59f66-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="59f66-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="59f66-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59f66-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="59f66-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="59f66-249">System-Only</span></span>            | <span data-ttu-id="59f66-250">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-250">False</span></span>                                                            |
| <span data-ttu-id="59f66-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="59f66-251">Is-Single-Valued</span></span>       | <span data-ttu-id="59f66-252">True</span><span class="sxs-lookup"><span data-stu-id="59f66-252">True</span></span>                                                             |
| <span data-ttu-id="59f66-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="59f66-253">Is Indexed</span></span>             | <span data-ttu-id="59f66-254">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-254">False</span></span>                                                            |
| <span data-ttu-id="59f66-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="59f66-255">In Global Catalog</span></span>      | <span data-ttu-id="59f66-256">Falso</span><span class="sxs-lookup"><span data-stu-id="59f66-256">False</span></span>                                                            |
| <span data-ttu-id="59f66-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="59f66-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="59f66-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="59f66-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="59f66-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59f66-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59f66-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="59f66-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-261">Search-Flags</span></span>           | <span data-ttu-id="59f66-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59f66-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="59f66-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59f66-263">System-Flags</span></span>           | <span data-ttu-id="59f66-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59f66-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="59f66-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="59f66-265">Classes used in</span></span>        | [<span data-ttu-id="59f66-266">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="59f66-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





