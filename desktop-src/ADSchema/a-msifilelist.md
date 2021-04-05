---
title: MSI-atributo de lista de arquivos
description: Esse atributo contém uma lista de arquivos do Microsoft Installer, como o arquivo MSI base (. msi) e arquivos de transformação MST (. MST).
ms.assetid: 259a13a2-bb34-49aa-862e-4159e887310c
ms.tgt_platform: multiple
keywords:
- MSI-arquivo-lista de atributos do AD Schema
- Esquema de AD do atributo msiFileList
topic_type:
- apiref
api_name:
- Msi-File-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05608cdf443ab053549fde7db509ca79be08b3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087071"
---
# <a name="msi-file-list-attribute"></a><span data-ttu-id="3ae09-105">MSI-atributo de lista de arquivos</span><span class="sxs-lookup"><span data-stu-id="3ae09-105">Msi-File-List attribute</span></span>

<span data-ttu-id="3ae09-106">Esse atributo contém uma lista de arquivos do Microsoft Installer, como o arquivo MSI base (. msi) e arquivos de transformação MST (. MST).</span><span class="sxs-lookup"><span data-stu-id="3ae09-106">This attribute contains a list of Microsoft installer files, such as the base MSI file (.msi) and MST transform files (.mst).</span></span>



| <span data-ttu-id="3ae09-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-107">Entry</span></span> | <span data-ttu-id="3ae09-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3ae09-109">CN</span><span class="sxs-lookup"><span data-stu-id="3ae09-109">CN</span></span>                | <span data-ttu-id="3ae09-110">MSI-lista de arquivos</span><span class="sxs-lookup"><span data-stu-id="3ae09-110">Msi-File-List</span></span>                               |
| <span data-ttu-id="3ae09-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3ae09-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3ae09-112">msiFileList</span><span class="sxs-lookup"><span data-stu-id="3ae09-112">msiFileList</span></span>                                 |
| <span data-ttu-id="3ae09-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3ae09-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="3ae09-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3ae09-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3ae09-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3ae09-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3ae09-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-116">Attribute-Id</span></span>      | <span data-ttu-id="3ae09-117">1.2.840.113556.1.4.671</span><span class="sxs-lookup"><span data-stu-id="3ae09-117">1.2.840.113556.1.4.671</span></span>                      |
| <span data-ttu-id="3ae09-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3ae09-118">System-Id-Guid</span></span>    | <span data-ttu-id="3ae09-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3ae09-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="3ae09-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ae09-120">Syntax</span></span>            | [<span data-ttu-id="3ae09-121">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3ae09-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3ae09-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="3ae09-122">Implementations</span></span>

-   [<span data-ttu-id="3ae09-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3ae09-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3ae09-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3ae09-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3ae09-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3ae09-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3ae09-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3ae09-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3ae09-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3ae09-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3ae09-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3ae09-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3ae09-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3ae09-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3ae09-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-130">Entry</span></span> | <span data-ttu-id="3ae09-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3ae09-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ae09-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ae09-134">System-Only</span></span>            | <span data-ttu-id="3ae09-135">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-135">False</span></span>                                                            |
| <span data-ttu-id="3ae09-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ae09-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3ae09-137">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-137">False</span></span>                                                            |
| <span data-ttu-id="3ae09-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ae09-138">Is Indexed</span></span>             | <span data-ttu-id="3ae09-139">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-139">False</span></span>                                                            |
| <span data-ttu-id="3ae09-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ae09-140">In Global Catalog</span></span>      | <span data-ttu-id="3ae09-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-141">False</span></span>                                                            |
| <span data-ttu-id="3ae09-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ae09-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ae09-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ae09-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="3ae09-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ae09-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ae09-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-146">Search-Flags</span></span>           | <span data-ttu-id="3ae09-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ae09-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="3ae09-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-148">System-Flags</span></span>           | <span data-ttu-id="3ae09-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ae09-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="3ae09-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ae09-150">Classes used in</span></span>        | [<span data-ttu-id="3ae09-151">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="3ae09-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3ae09-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ae09-152">Windows Server 2003</span></span>



| <span data-ttu-id="3ae09-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-153">Entry</span></span> | <span data-ttu-id="3ae09-154">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3ae09-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ae09-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ae09-157">System-Only</span></span>            | <span data-ttu-id="3ae09-158">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-158">False</span></span>                                                            |
| <span data-ttu-id="3ae09-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ae09-159">Is-Single-Valued</span></span>       | <span data-ttu-id="3ae09-160">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-160">False</span></span>                                                            |
| <span data-ttu-id="3ae09-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ae09-161">Is Indexed</span></span>             | <span data-ttu-id="3ae09-162">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-162">False</span></span>                                                            |
| <span data-ttu-id="3ae09-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ae09-163">In Global Catalog</span></span>      | <span data-ttu-id="3ae09-164">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-164">False</span></span>                                                            |
| <span data-ttu-id="3ae09-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ae09-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ae09-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ae09-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="3ae09-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ae09-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ae09-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-169">Search-Flags</span></span>           | <span data-ttu-id="3ae09-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ae09-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="3ae09-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-171">System-Flags</span></span>           | <span data-ttu-id="3ae09-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ae09-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="3ae09-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ae09-173">Classes used in</span></span>        | [<span data-ttu-id="3ae09-174">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="3ae09-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3ae09-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3ae09-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3ae09-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-176">Entry</span></span> | <span data-ttu-id="3ae09-177">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3ae09-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ae09-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ae09-180">System-Only</span></span>            | <span data-ttu-id="3ae09-181">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-181">False</span></span>                                                            |
| <span data-ttu-id="3ae09-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ae09-182">Is-Single-Valued</span></span>       | <span data-ttu-id="3ae09-183">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-183">False</span></span>                                                            |
| <span data-ttu-id="3ae09-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ae09-184">Is Indexed</span></span>             | <span data-ttu-id="3ae09-185">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-185">False</span></span>                                                            |
| <span data-ttu-id="3ae09-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ae09-186">In Global Catalog</span></span>      | <span data-ttu-id="3ae09-187">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-187">False</span></span>                                                            |
| <span data-ttu-id="3ae09-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ae09-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ae09-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ae09-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="3ae09-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ae09-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ae09-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-192">Search-Flags</span></span>           | <span data-ttu-id="3ae09-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ae09-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="3ae09-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-194">System-Flags</span></span>           | <span data-ttu-id="3ae09-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ae09-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="3ae09-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ae09-196">Classes used in</span></span>        | [<span data-ttu-id="3ae09-197">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="3ae09-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3ae09-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ae09-198">Windows Server 2008</span></span>



| <span data-ttu-id="3ae09-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-199">Entry</span></span> | <span data-ttu-id="3ae09-200">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3ae09-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ae09-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ae09-203">System-Only</span></span>            | <span data-ttu-id="3ae09-204">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-204">False</span></span>                                                            |
| <span data-ttu-id="3ae09-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ae09-205">Is-Single-Valued</span></span>       | <span data-ttu-id="3ae09-206">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-206">False</span></span>                                                            |
| <span data-ttu-id="3ae09-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ae09-207">Is Indexed</span></span>             | <span data-ttu-id="3ae09-208">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-208">False</span></span>                                                            |
| <span data-ttu-id="3ae09-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ae09-209">In Global Catalog</span></span>      | <span data-ttu-id="3ae09-210">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-210">False</span></span>                                                            |
| <span data-ttu-id="3ae09-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ae09-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ae09-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ae09-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="3ae09-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ae09-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ae09-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-215">Search-Flags</span></span>           | <span data-ttu-id="3ae09-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ae09-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="3ae09-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-217">System-Flags</span></span>           | <span data-ttu-id="3ae09-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ae09-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="3ae09-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ae09-219">Classes used in</span></span>        | [<span data-ttu-id="3ae09-220">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="3ae09-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3ae09-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ae09-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3ae09-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-222">Entry</span></span> | <span data-ttu-id="3ae09-223">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3ae09-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ae09-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ae09-226">System-Only</span></span>            | <span data-ttu-id="3ae09-227">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-227">False</span></span>                                                            |
| <span data-ttu-id="3ae09-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ae09-228">Is-Single-Valued</span></span>       | <span data-ttu-id="3ae09-229">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-229">False</span></span>                                                            |
| <span data-ttu-id="3ae09-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ae09-230">Is Indexed</span></span>             | <span data-ttu-id="3ae09-231">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-231">False</span></span>                                                            |
| <span data-ttu-id="3ae09-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ae09-232">In Global Catalog</span></span>      | <span data-ttu-id="3ae09-233">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-233">False</span></span>                                                            |
| <span data-ttu-id="3ae09-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ae09-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ae09-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ae09-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="3ae09-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ae09-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ae09-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-238">Search-Flags</span></span>           | <span data-ttu-id="3ae09-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ae09-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="3ae09-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-240">System-Flags</span></span>           | <span data-ttu-id="3ae09-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ae09-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="3ae09-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ae09-242">Classes used in</span></span>        | [<span data-ttu-id="3ae09-243">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="3ae09-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3ae09-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ae09-244">Windows Server 2012</span></span>



| <span data-ttu-id="3ae09-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ae09-245">Entry</span></span> | <span data-ttu-id="3ae09-246">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae09-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="3ae09-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="3ae09-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ae09-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="3ae09-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ae09-249">System-Only</span></span>            | <span data-ttu-id="3ae09-250">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-250">False</span></span>                                                            |
| <span data-ttu-id="3ae09-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3ae09-251">Is-Single-Valued</span></span>       | <span data-ttu-id="3ae09-252">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-252">False</span></span>                                                            |
| <span data-ttu-id="3ae09-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="3ae09-253">Is Indexed</span></span>             | <span data-ttu-id="3ae09-254">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-254">False</span></span>                                                            |
| <span data-ttu-id="3ae09-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ae09-255">In Global Catalog</span></span>      | <span data-ttu-id="3ae09-256">Falso</span><span class="sxs-lookup"><span data-stu-id="3ae09-256">False</span></span>                                                            |
| <span data-ttu-id="3ae09-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3ae09-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ae09-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3ae09-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="3ae09-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ae09-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ae09-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="3ae09-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-261">Search-Flags</span></span>           | <span data-ttu-id="3ae09-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ae09-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="3ae09-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ae09-263">System-Flags</span></span>           | <span data-ttu-id="3ae09-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3ae09-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="3ae09-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3ae09-265">Classes used in</span></span>        | [<span data-ttu-id="3ae09-266">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="3ae09-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





