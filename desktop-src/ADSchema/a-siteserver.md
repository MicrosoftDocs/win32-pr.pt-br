---
title: Site-Server atributo
description: Licenciando servidor principal para um determinado site.
ms.assetid: bcae8c63-a953-4721-b2d1-96d0376592c6
ms.tgt_platform: multiple
keywords:
- Esquema de Site-Server do atributo AD
- Esquema de AD do atributo siteServer
topic_type:
- apiref
api_name:
- Site-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785057cd9ea23c05d58541450dc4c92a502877e5
ms.sourcegitcommit: f10bb95039c20a9de79f21e3fcb93a543f30a00e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104163676"
---
# <a name="site-server-attribute"></a><span data-ttu-id="c817e-105">Site-Server atributo</span><span class="sxs-lookup"><span data-stu-id="c817e-105">Site-Server attribute</span></span>

<span data-ttu-id="c817e-106">Licenciando servidor principal para um determinado site.</span><span class="sxs-lookup"><span data-stu-id="c817e-106">Licensing main server for a given Site.</span></span>



| <span data-ttu-id="c817e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-107">Entry</span></span> | <span data-ttu-id="c817e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="c817e-109">CN</span><span class="sxs-lookup"><span data-stu-id="c817e-109">CN</span></span>                | <span data-ttu-id="c817e-110">Site-Server</span><span class="sxs-lookup"><span data-stu-id="c817e-110">Site-Server</span></span>                                  |
| <span data-ttu-id="c817e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c817e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c817e-112">siteServer</span><span class="sxs-lookup"><span data-stu-id="c817e-112">siteServer</span></span>                                   |
| <span data-ttu-id="c817e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c817e-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="c817e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c817e-114">Update Privilege</span></span>  | <span data-ttu-id="c817e-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="c817e-115">Domain administrator</span></span>                         |
| <span data-ttu-id="c817e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c817e-116">Update Frequency</span></span>  | <span data-ttu-id="c817e-117">Sempre que o site de licenciamento precisar ser alterado.</span><span class="sxs-lookup"><span data-stu-id="c817e-117">Whenever the licensing site needs to change.</span></span> |
| <span data-ttu-id="c817e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-118">Attribute-Id</span></span>      | <span data-ttu-id="c817e-119">1.2.840.113556.1.4.494</span><span class="sxs-lookup"><span data-stu-id="c817e-119">1.2.840.113556.1.4.494</span></span>                       |
| <span data-ttu-id="c817e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c817e-120">System-Id-Guid</span></span>    | <span data-ttu-id="c817e-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c817e-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span></span>         |
| <span data-ttu-id="c817e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c817e-122">Syntax</span></span>            | [<span data-ttu-id="c817e-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c817e-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="c817e-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="c817e-124">Implementations</span></span>

-   [<span data-ttu-id="c817e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c817e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c817e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c817e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c817e-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c817e-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c817e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c817e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c817e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c817e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c817e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c817e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c817e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c817e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c817e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c817e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c817e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-133">Entry</span></span> | <span data-ttu-id="c817e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c817e-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-137">System-Only</span></span>            | <span data-ttu-id="c817e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-138">False</span></span>                                                                 |
| <span data-ttu-id="c817e-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-140">False</span></span>                                                                 |
| <span data-ttu-id="c817e-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-141">Is Indexed</span></span>             | <span data-ttu-id="c817e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-142">False</span></span>                                                                 |
| <span data-ttu-id="c817e-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-143">In Global Catalog</span></span>      | <span data-ttu-id="c817e-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-144">False</span></span>                                                                 |
| <span data-ttu-id="c817e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c817e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-149">Search-Flags</span></span>           | <span data-ttu-id="c817e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="c817e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-151">System-Flags</span></span>           | <span data-ttu-id="c817e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="c817e-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-153">Classes used in</span></span>        | [<span data-ttu-id="c817e-154">**Licenciamento – site-Settings**</span><span class="sxs-lookup"><span data-stu-id="c817e-154">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c817e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c817e-155">Windows Server 2003</span></span>



| <span data-ttu-id="c817e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-156">Entry</span></span> | <span data-ttu-id="c817e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c817e-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-160">System-Only</span></span>            | <span data-ttu-id="c817e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-161">False</span></span>                                                                 |
| <span data-ttu-id="c817e-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-163">False</span></span>                                                                 |
| <span data-ttu-id="c817e-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-164">Is Indexed</span></span>             | <span data-ttu-id="c817e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-165">False</span></span>                                                                 |
| <span data-ttu-id="c817e-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-166">In Global Catalog</span></span>      | <span data-ttu-id="c817e-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-167">False</span></span>                                                                 |
| <span data-ttu-id="c817e-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c817e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-172">Search-Flags</span></span>           | <span data-ttu-id="c817e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="c817e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-174">System-Flags</span></span>           | <span data-ttu-id="c817e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="c817e-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-176">Classes used in</span></span>        | [<span data-ttu-id="c817e-177">**Licenciamento – site-Settings**</span><span class="sxs-lookup"><span data-stu-id="c817e-177">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c817e-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="c817e-178">ADAM</span></span>



| <span data-ttu-id="c817e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-179">Entry</span></span> | <span data-ttu-id="c817e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c817e-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="c817e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="c817e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-183">System-Only</span></span>            | <span data-ttu-id="c817e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-184">False</span></span>        |
| <span data-ttu-id="c817e-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-186">False</span></span>        |
| <span data-ttu-id="c817e-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-187">Is Indexed</span></span>             | <span data-ttu-id="c817e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-188">False</span></span>        |
| <span data-ttu-id="c817e-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-189">In Global Catalog</span></span>      | <span data-ttu-id="c817e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-190">False</span></span>        |
| <span data-ttu-id="c817e-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="c817e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="c817e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="c817e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-195">Search-Flags</span></span>           | <span data-ttu-id="c817e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-196">0x00000000</span></span>   |
| <span data-ttu-id="c817e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-197">System-Flags</span></span>           | <span data-ttu-id="c817e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-198">0x00000010</span></span>   |
| <span data-ttu-id="c817e-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c817e-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c817e-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c817e-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-201">Entry</span></span> | <span data-ttu-id="c817e-202">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c817e-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-203">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-204">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-205">System-Only</span></span>            | <span data-ttu-id="c817e-206">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-206">False</span></span>                                                                 |
| <span data-ttu-id="c817e-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-208">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-208">False</span></span>                                                                 |
| <span data-ttu-id="c817e-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-209">Is Indexed</span></span>             | <span data-ttu-id="c817e-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-210">False</span></span>                                                                 |
| <span data-ttu-id="c817e-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-211">In Global Catalog</span></span>      | <span data-ttu-id="c817e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-212">False</span></span>                                                                 |
| <span data-ttu-id="c817e-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-214">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c817e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-215">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-216">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-217">Search-Flags</span></span>           | <span data-ttu-id="c817e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-218">0x00000000</span></span>                                                            |
| <span data-ttu-id="c817e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-219">System-Flags</span></span>           | <span data-ttu-id="c817e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-220">0x00000010</span></span>                                                            |
| <span data-ttu-id="c817e-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-221">Classes used in</span></span>        | [<span data-ttu-id="c817e-222">**Licenciamento – site-Settings**</span><span class="sxs-lookup"><span data-stu-id="c817e-222">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c817e-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c817e-223">Windows Server 2008</span></span>



| <span data-ttu-id="c817e-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-224">Entry</span></span> | <span data-ttu-id="c817e-225">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c817e-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-226">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-227">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-228">System-Only</span></span>            | <span data-ttu-id="c817e-229">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-229">False</span></span>                                                                 |
| <span data-ttu-id="c817e-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-231">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-231">False</span></span>                                                                 |
| <span data-ttu-id="c817e-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-232">Is Indexed</span></span>             | <span data-ttu-id="c817e-233">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-233">False</span></span>                                                                 |
| <span data-ttu-id="c817e-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-234">In Global Catalog</span></span>      | <span data-ttu-id="c817e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-235">False</span></span>                                                                 |
| <span data-ttu-id="c817e-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-237">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c817e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-238">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-239">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-240">Search-Flags</span></span>           | <span data-ttu-id="c817e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-241">0x00000000</span></span>                                                            |
| <span data-ttu-id="c817e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-242">System-Flags</span></span>           | <span data-ttu-id="c817e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-243">0x00000010</span></span>                                                            |
| <span data-ttu-id="c817e-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-244">Classes used in</span></span>        | [<span data-ttu-id="c817e-245">**Licenciamento – site-Settings**</span><span class="sxs-lookup"><span data-stu-id="c817e-245">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c817e-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c817e-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c817e-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-247">Entry</span></span> | <span data-ttu-id="c817e-248">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c817e-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-249">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-250">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-251">System-Only</span></span>            | <span data-ttu-id="c817e-252">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-252">False</span></span>                                                                 |
| <span data-ttu-id="c817e-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-254">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-254">False</span></span>                                                                 |
| <span data-ttu-id="c817e-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-255">Is Indexed</span></span>             | <span data-ttu-id="c817e-256">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-256">False</span></span>                                                                 |
| <span data-ttu-id="c817e-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-257">In Global Catalog</span></span>      | <span data-ttu-id="c817e-258">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-258">False</span></span>                                                                 |
| <span data-ttu-id="c817e-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-260">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c817e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-261">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-262">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-263">Search-Flags</span></span>           | <span data-ttu-id="c817e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-264">0x00000000</span></span>                                                            |
| <span data-ttu-id="c817e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-265">System-Flags</span></span>           | <span data-ttu-id="c817e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-266">0x00000010</span></span>                                                            |
| <span data-ttu-id="c817e-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-267">Classes used in</span></span>        | [<span data-ttu-id="c817e-268">**Licenciamento – site-Settings**</span><span class="sxs-lookup"><span data-stu-id="c817e-268">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c817e-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c817e-269">Windows Server 2012</span></span>



| <span data-ttu-id="c817e-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="c817e-270">Entry</span></span> | <span data-ttu-id="c817e-271">Valor</span><span class="sxs-lookup"><span data-stu-id="c817e-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c817e-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="c817e-272">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c817e-273">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="c817e-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="c817e-274">System-Only</span></span>            | <span data-ttu-id="c817e-275">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-275">False</span></span>                                                                 |
| <span data-ttu-id="c817e-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c817e-276">Is-Single-Valued</span></span>       | <span data-ttu-id="c817e-277">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-277">False</span></span>                                                                 |
| <span data-ttu-id="c817e-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="c817e-278">Is Indexed</span></span>             | <span data-ttu-id="c817e-279">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-279">False</span></span>                                                                 |
| <span data-ttu-id="c817e-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c817e-280">In Global Catalog</span></span>      | <span data-ttu-id="c817e-281">Falso</span><span class="sxs-lookup"><span data-stu-id="c817e-281">False</span></span>                                                                 |
| <span data-ttu-id="c817e-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c817e-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="c817e-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c817e-283">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="c817e-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c817e-284">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c817e-285">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="c817e-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-286">Search-Flags</span></span>           | <span data-ttu-id="c817e-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c817e-287">0x00000000</span></span>                                                            |
| <span data-ttu-id="c817e-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c817e-288">System-Flags</span></span>           | <span data-ttu-id="c817e-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c817e-289">0x00000010</span></span>                                                            |
| <span data-ttu-id="c817e-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c817e-290">Classes used in</span></span>        | [<span data-ttu-id="c817e-291">**Licenciamento – site-Settings**</span><span class="sxs-lookup"><span data-stu-id="c817e-291">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



 

 





