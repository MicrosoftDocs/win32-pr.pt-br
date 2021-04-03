---
title: Template-Roots atributo
description: Esse atributo é usado no contêiner de configuração do Exchange para indicar onde os contêineres de modelo são armazenados. Essas informações são usadas pelo provedor de Active Directory MAPI.
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- Esquema de Template-Roots do atributo AD
- Esquema de AD do atributo templateRoots
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645499"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="39729-106">Template-Roots atributo</span><span class="sxs-lookup"><span data-stu-id="39729-106">Template-Roots attribute</span></span>

<span data-ttu-id="39729-107">Esse atributo é usado no contêiner de configuração do Exchange para indicar onde os contêineres de modelo são armazenados.</span><span class="sxs-lookup"><span data-stu-id="39729-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="39729-108">Essas informações são usadas pelo provedor de Active Directory MAPI.</span><span class="sxs-lookup"><span data-stu-id="39729-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="39729-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-109">Entry</span></span> | <span data-ttu-id="39729-110">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="39729-111">CN</span><span class="sxs-lookup"><span data-stu-id="39729-111">CN</span></span>                | <span data-ttu-id="39729-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="39729-112">Template-Roots</span></span>                          |
| <span data-ttu-id="39729-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39729-113">Ldap-Display-Name</span></span> | <span data-ttu-id="39729-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="39729-114">templateRoots</span></span>                           |
| <span data-ttu-id="39729-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="39729-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="39729-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="39729-116">Update Privilege</span></span>  | <span data-ttu-id="39729-117">Isso é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="39729-117">This is used by the system.</span></span>             |
| <span data-ttu-id="39729-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="39729-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="39729-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39729-119">Attribute-Id</span></span>      | <span data-ttu-id="39729-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="39729-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="39729-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39729-121">System-Id-Guid</span></span>    | <span data-ttu-id="39729-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="39729-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="39729-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="39729-123">Syntax</span></span>            | [<span data-ttu-id="39729-124">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="39729-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="39729-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="39729-125">Implementations</span></span>

-   [<span data-ttu-id="39729-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39729-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39729-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39729-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39729-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39729-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39729-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39729-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39729-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39729-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39729-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39729-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39729-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39729-132">Windows 2000 Server</span></span>



| <span data-ttu-id="39729-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-133">Entry</span></span> | <span data-ttu-id="39729-134">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39729-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="39729-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39729-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="39729-137">System-Only</span></span>            | <span data-ttu-id="39729-138">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-138">False</span></span>                                                                                |
| <span data-ttu-id="39729-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39729-139">Is-Single-Valued</span></span>       | <span data-ttu-id="39729-140">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-140">False</span></span>                                                                                |
| <span data-ttu-id="39729-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="39729-141">Is Indexed</span></span>             | <span data-ttu-id="39729-142">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-142">False</span></span>                                                                                |
| <span data-ttu-id="39729-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39729-143">In Global Catalog</span></span>      | <span data-ttu-id="39729-144">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-144">False</span></span>                                                                                |
| <span data-ttu-id="39729-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39729-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="39729-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39729-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="39729-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39729-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39729-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-149">Search-Flags</span></span>           | <span data-ttu-id="39729-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39729-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="39729-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-151">System-Flags</span></span>           | <span data-ttu-id="39729-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39729-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="39729-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39729-153">Classes used in</span></span>        | [<span data-ttu-id="39729-154">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="39729-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39729-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39729-155">Windows Server 2003</span></span>



| <span data-ttu-id="39729-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-156">Entry</span></span> | <span data-ttu-id="39729-157">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39729-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="39729-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39729-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="39729-160">System-Only</span></span>            | <span data-ttu-id="39729-161">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-161">False</span></span>                                                                                |
| <span data-ttu-id="39729-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39729-162">Is-Single-Valued</span></span>       | <span data-ttu-id="39729-163">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-163">False</span></span>                                                                                |
| <span data-ttu-id="39729-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="39729-164">Is Indexed</span></span>             | <span data-ttu-id="39729-165">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-165">False</span></span>                                                                                |
| <span data-ttu-id="39729-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39729-166">In Global Catalog</span></span>      | <span data-ttu-id="39729-167">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-167">False</span></span>                                                                                |
| <span data-ttu-id="39729-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39729-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="39729-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39729-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="39729-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39729-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39729-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-172">Search-Flags</span></span>           | <span data-ttu-id="39729-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39729-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="39729-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-174">System-Flags</span></span>           | <span data-ttu-id="39729-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39729-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="39729-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39729-176">Classes used in</span></span>        | [<span data-ttu-id="39729-177">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="39729-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39729-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39729-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39729-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-179">Entry</span></span> | <span data-ttu-id="39729-180">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39729-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="39729-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39729-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="39729-183">System-Only</span></span>            | <span data-ttu-id="39729-184">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-184">False</span></span>                                                                                |
| <span data-ttu-id="39729-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39729-185">Is-Single-Valued</span></span>       | <span data-ttu-id="39729-186">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-186">False</span></span>                                                                                |
| <span data-ttu-id="39729-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="39729-187">Is Indexed</span></span>             | <span data-ttu-id="39729-188">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-188">False</span></span>                                                                                |
| <span data-ttu-id="39729-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39729-189">In Global Catalog</span></span>      | <span data-ttu-id="39729-190">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-190">False</span></span>                                                                                |
| <span data-ttu-id="39729-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39729-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="39729-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39729-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="39729-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39729-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39729-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-195">Search-Flags</span></span>           | <span data-ttu-id="39729-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39729-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="39729-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-197">System-Flags</span></span>           | <span data-ttu-id="39729-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39729-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="39729-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39729-199">Classes used in</span></span>        | [<span data-ttu-id="39729-200">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="39729-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39729-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39729-201">Windows Server 2008</span></span>



| <span data-ttu-id="39729-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-202">Entry</span></span> | <span data-ttu-id="39729-203">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39729-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="39729-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39729-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="39729-206">System-Only</span></span>            | <span data-ttu-id="39729-207">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-207">False</span></span>                                                                                |
| <span data-ttu-id="39729-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39729-208">Is-Single-Valued</span></span>       | <span data-ttu-id="39729-209">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-209">False</span></span>                                                                                |
| <span data-ttu-id="39729-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="39729-210">Is Indexed</span></span>             | <span data-ttu-id="39729-211">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-211">False</span></span>                                                                                |
| <span data-ttu-id="39729-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39729-212">In Global Catalog</span></span>      | <span data-ttu-id="39729-213">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-213">False</span></span>                                                                                |
| <span data-ttu-id="39729-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39729-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="39729-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39729-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="39729-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39729-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39729-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-218">Search-Flags</span></span>           | <span data-ttu-id="39729-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39729-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="39729-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-220">System-Flags</span></span>           | <span data-ttu-id="39729-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39729-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="39729-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39729-222">Classes used in</span></span>        | [<span data-ttu-id="39729-223">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="39729-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39729-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39729-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39729-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-225">Entry</span></span> | <span data-ttu-id="39729-226">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39729-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="39729-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39729-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="39729-229">System-Only</span></span>            | <span data-ttu-id="39729-230">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-230">False</span></span>                                                                                |
| <span data-ttu-id="39729-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39729-231">Is-Single-Valued</span></span>       | <span data-ttu-id="39729-232">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-232">False</span></span>                                                                                |
| <span data-ttu-id="39729-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="39729-233">Is Indexed</span></span>             | <span data-ttu-id="39729-234">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-234">False</span></span>                                                                                |
| <span data-ttu-id="39729-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39729-235">In Global Catalog</span></span>      | <span data-ttu-id="39729-236">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-236">False</span></span>                                                                                |
| <span data-ttu-id="39729-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39729-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="39729-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39729-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="39729-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39729-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39729-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-241">Search-Flags</span></span>           | <span data-ttu-id="39729-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39729-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="39729-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-243">System-Flags</span></span>           | <span data-ttu-id="39729-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39729-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="39729-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39729-245">Classes used in</span></span>        | [<span data-ttu-id="39729-246">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="39729-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39729-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39729-247">Windows Server 2012</span></span>



| <span data-ttu-id="39729-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="39729-248">Entry</span></span> | <span data-ttu-id="39729-249">Valor</span><span class="sxs-lookup"><span data-stu-id="39729-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="39729-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="39729-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39729-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="39729-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="39729-252">System-Only</span></span>            | <span data-ttu-id="39729-253">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-253">False</span></span>                                                                                |
| <span data-ttu-id="39729-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39729-254">Is-Single-Valued</span></span>       | <span data-ttu-id="39729-255">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-255">False</span></span>                                                                                |
| <span data-ttu-id="39729-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="39729-256">Is Indexed</span></span>             | <span data-ttu-id="39729-257">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-257">False</span></span>                                                                                |
| <span data-ttu-id="39729-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39729-258">In Global Catalog</span></span>      | <span data-ttu-id="39729-259">Falso</span><span class="sxs-lookup"><span data-stu-id="39729-259">False</span></span>                                                                                |
| <span data-ttu-id="39729-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39729-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="39729-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39729-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="39729-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39729-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39729-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="39729-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-264">Search-Flags</span></span>           | <span data-ttu-id="39729-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39729-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="39729-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39729-266">System-Flags</span></span>           | <span data-ttu-id="39729-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39729-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="39729-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39729-268">Classes used in</span></span>        | [<span data-ttu-id="39729-269">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="39729-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





