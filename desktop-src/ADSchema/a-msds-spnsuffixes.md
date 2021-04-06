---
title: atributo ms-DS-SPN-Suffixs
description: Esse atributo descreve os sufixos dos nomes de host DNS usados pelos servidores na floresta. Esses sufixos DNS serão compartilhados com outras florestas que têm confiança entre florestas com essa floresta.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- ms-DS-SPN-suffix atributo AD Schema
- atributo msDS-SPNSuffixes do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919489"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="78103-106">atributo ms-DS-SPN-Suffixs</span><span class="sxs-lookup"><span data-stu-id="78103-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="78103-107">Esse atributo descreve os sufixos dos nomes de host DNS usados pelos servidores na floresta.</span><span class="sxs-lookup"><span data-stu-id="78103-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="78103-108">Esses sufixos DNS serão compartilhados com outras florestas que têm confiança entre florestas com essa floresta.</span><span class="sxs-lookup"><span data-stu-id="78103-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="78103-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="78103-109">Entry</span></span> | <span data-ttu-id="78103-110">Valor</span><span class="sxs-lookup"><span data-stu-id="78103-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="78103-111">CN</span><span class="sxs-lookup"><span data-stu-id="78103-111">CN</span></span>                | <span data-ttu-id="78103-112">ms-DS-SPN-sufixos</span><span class="sxs-lookup"><span data-stu-id="78103-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="78103-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="78103-113">Ldap-Display-Name</span></span> | <span data-ttu-id="78103-114">msDS-SPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="78103-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="78103-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="78103-115">Size</span></span>              | <span data-ttu-id="78103-116">255 bytes</span><span class="sxs-lookup"><span data-stu-id="78103-116">255 bytes</span></span>                                    |
| <span data-ttu-id="78103-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="78103-117">Update Privilege</span></span>  | <span data-ttu-id="78103-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="78103-118">Domain administrator</span></span>                         |
| <span data-ttu-id="78103-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="78103-119">Update Frequency</span></span>  | <span data-ttu-id="78103-120">Quando os servidores na floresta obtiverem um novo sufixo.</span><span class="sxs-lookup"><span data-stu-id="78103-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="78103-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78103-121">Attribute-Id</span></span>      | <span data-ttu-id="78103-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="78103-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="78103-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78103-123">System-Id-Guid</span></span>    | <span data-ttu-id="78103-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="78103-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="78103-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="78103-125">Syntax</span></span>            | [<span data-ttu-id="78103-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="78103-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="78103-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="78103-127">Implementations</span></span>

-   [<span data-ttu-id="78103-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78103-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78103-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78103-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78103-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78103-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78103-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78103-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78103-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78103-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="78103-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78103-133">Windows Server 2003</span></span>



| <span data-ttu-id="78103-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="78103-134">Entry</span></span> | <span data-ttu-id="78103-135">Valor</span><span class="sxs-lookup"><span data-stu-id="78103-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="78103-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="78103-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78103-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="78103-138">System-Only</span></span>            | <span data-ttu-id="78103-139">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-139">False</span></span>                                                         |
| <span data-ttu-id="78103-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78103-140">Is-Single-Valued</span></span>       | <span data-ttu-id="78103-141">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-141">False</span></span>                                                         |
| <span data-ttu-id="78103-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="78103-142">Is Indexed</span></span>             | <span data-ttu-id="78103-143">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-143">False</span></span>                                                         |
| <span data-ttu-id="78103-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78103-144">In Global Catalog</span></span>      | <span data-ttu-id="78103-145">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-145">False</span></span>                                                         |
| <span data-ttu-id="78103-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78103-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="78103-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78103-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="78103-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78103-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="78103-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78103-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="78103-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-150">Search-Flags</span></span>           | <span data-ttu-id="78103-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78103-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="78103-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-152">System-Flags</span></span>           | <span data-ttu-id="78103-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78103-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="78103-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78103-154">Classes used in</span></span>        | [<span data-ttu-id="78103-155">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="78103-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78103-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78103-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78103-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="78103-157">Entry</span></span> | <span data-ttu-id="78103-158">Valor</span><span class="sxs-lookup"><span data-stu-id="78103-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="78103-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="78103-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78103-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="78103-161">System-Only</span></span>            | <span data-ttu-id="78103-162">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-162">False</span></span>                                                         |
| <span data-ttu-id="78103-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78103-163">Is-Single-Valued</span></span>       | <span data-ttu-id="78103-164">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-164">False</span></span>                                                         |
| <span data-ttu-id="78103-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="78103-165">Is Indexed</span></span>             | <span data-ttu-id="78103-166">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-166">False</span></span>                                                         |
| <span data-ttu-id="78103-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78103-167">In Global Catalog</span></span>      | <span data-ttu-id="78103-168">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-168">False</span></span>                                                         |
| <span data-ttu-id="78103-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78103-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="78103-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78103-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="78103-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78103-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="78103-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78103-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="78103-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-173">Search-Flags</span></span>           | <span data-ttu-id="78103-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78103-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="78103-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-175">System-Flags</span></span>           | <span data-ttu-id="78103-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78103-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="78103-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78103-177">Classes used in</span></span>        | [<span data-ttu-id="78103-178">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="78103-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78103-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78103-179">Windows Server 2008</span></span>



| <span data-ttu-id="78103-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="78103-180">Entry</span></span> | <span data-ttu-id="78103-181">Valor</span><span class="sxs-lookup"><span data-stu-id="78103-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="78103-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="78103-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78103-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="78103-184">System-Only</span></span>            | <span data-ttu-id="78103-185">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-185">False</span></span>                                                         |
| <span data-ttu-id="78103-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78103-186">Is-Single-Valued</span></span>       | <span data-ttu-id="78103-187">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-187">False</span></span>                                                         |
| <span data-ttu-id="78103-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="78103-188">Is Indexed</span></span>             | <span data-ttu-id="78103-189">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-189">False</span></span>                                                         |
| <span data-ttu-id="78103-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78103-190">In Global Catalog</span></span>      | <span data-ttu-id="78103-191">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-191">False</span></span>                                                         |
| <span data-ttu-id="78103-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78103-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="78103-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78103-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="78103-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78103-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="78103-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78103-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="78103-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-196">Search-Flags</span></span>           | <span data-ttu-id="78103-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78103-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="78103-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-198">System-Flags</span></span>           | <span data-ttu-id="78103-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78103-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="78103-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78103-200">Classes used in</span></span>        | [<span data-ttu-id="78103-201">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="78103-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78103-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78103-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78103-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="78103-203">Entry</span></span> | <span data-ttu-id="78103-204">Valor</span><span class="sxs-lookup"><span data-stu-id="78103-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="78103-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="78103-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78103-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="78103-207">System-Only</span></span>            | <span data-ttu-id="78103-208">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-208">False</span></span>                                                         |
| <span data-ttu-id="78103-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78103-209">Is-Single-Valued</span></span>       | <span data-ttu-id="78103-210">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-210">False</span></span>                                                         |
| <span data-ttu-id="78103-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="78103-211">Is Indexed</span></span>             | <span data-ttu-id="78103-212">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-212">False</span></span>                                                         |
| <span data-ttu-id="78103-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78103-213">In Global Catalog</span></span>      | <span data-ttu-id="78103-214">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-214">False</span></span>                                                         |
| <span data-ttu-id="78103-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78103-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="78103-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78103-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="78103-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78103-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="78103-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78103-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="78103-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-219">Search-Flags</span></span>           | <span data-ttu-id="78103-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78103-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="78103-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-221">System-Flags</span></span>           | <span data-ttu-id="78103-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78103-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="78103-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78103-223">Classes used in</span></span>        | [<span data-ttu-id="78103-224">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="78103-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78103-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78103-225">Windows Server 2012</span></span>



| <span data-ttu-id="78103-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="78103-226">Entry</span></span> | <span data-ttu-id="78103-227">Valor</span><span class="sxs-lookup"><span data-stu-id="78103-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="78103-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="78103-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78103-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="78103-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="78103-230">System-Only</span></span>            | <span data-ttu-id="78103-231">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-231">False</span></span>                                                         |
| <span data-ttu-id="78103-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78103-232">Is-Single-Valued</span></span>       | <span data-ttu-id="78103-233">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-233">False</span></span>                                                         |
| <span data-ttu-id="78103-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="78103-234">Is Indexed</span></span>             | <span data-ttu-id="78103-235">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-235">False</span></span>                                                         |
| <span data-ttu-id="78103-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78103-236">In Global Catalog</span></span>      | <span data-ttu-id="78103-237">Falso</span><span class="sxs-lookup"><span data-stu-id="78103-237">False</span></span>                                                         |
| <span data-ttu-id="78103-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78103-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="78103-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78103-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="78103-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78103-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="78103-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78103-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="78103-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-242">Search-Flags</span></span>           | <span data-ttu-id="78103-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78103-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="78103-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78103-244">System-Flags</span></span>           | <span data-ttu-id="78103-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78103-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="78103-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78103-246">Classes used in</span></span>        | [<span data-ttu-id="78103-247">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="78103-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





