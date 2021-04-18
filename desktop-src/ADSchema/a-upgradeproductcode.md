---
title: Atualizar-atributo de código do produto
description: Esse atributo contém o código do produto de outros pacotes, como aplicativos, que pode ser atualizado por esse pacote ou que pode atualizar este pacote.
ms.assetid: bf0ab06a-88a6-45af-ac9f-ee0ce648e51b
ms.tgt_platform: multiple
keywords:
- Upgrade-esquema de atributo de código do produto do AD
- Esquema de AD do atributo upgradeProductCode
topic_type:
- apiref
api_name:
- Upgrade-Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33734ec62665d301568f5f4152b39c5fbf4f94a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105771746"
---
# <a name="upgrade-product-code-attribute"></a><span data-ttu-id="b8ca1-105">Atualizar-atributo de código do produto</span><span class="sxs-lookup"><span data-stu-id="b8ca1-105">Upgrade-Product-Code attribute</span></span>

<span data-ttu-id="b8ca1-106">Esse atributo contém o código do produto de outros pacotes, como aplicativos, que pode ser atualizado por esse pacote ou que pode atualizar este pacote.</span><span class="sxs-lookup"><span data-stu-id="b8ca1-106">This attribute contains the product code of other packages, such as applications, that can be upgraded by this package, or that can upgrade this package.</span></span>



| <span data-ttu-id="b8ca1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-107">Entry</span></span> | <span data-ttu-id="b8ca1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b8ca1-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8ca1-109">CN</span></span>                | <span data-ttu-id="b8ca1-110">Atualização – código do produto</span><span class="sxs-lookup"><span data-stu-id="b8ca1-110">Upgrade-Product-Code</span></span>                                  |
| <span data-ttu-id="b8ca1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b8ca1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8ca1-112">upgradeProductCode</span><span class="sxs-lookup"><span data-stu-id="b8ca1-112">upgradeProductCode</span></span>                                    |
| <span data-ttu-id="b8ca1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b8ca1-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b8ca1-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b8ca1-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b8ca1-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b8ca1-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b8ca1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-116">Attribute-Id</span></span>      | <span data-ttu-id="b8ca1-117">1.2.840.113556.1.4.813</span><span class="sxs-lookup"><span data-stu-id="b8ca1-117">1.2.840.113556.1.4.813</span></span>                                |
| <span data-ttu-id="b8ca1-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8ca1-118">System-Id-Guid</span></span>    | <span data-ttu-id="b8ca1-119">d9e18312-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b8ca1-119">d9e18312-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="b8ca1-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ca1-120">Syntax</span></span>            | [<span data-ttu-id="b8ca1-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b8ca1-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="b8ca1-122">Implementations</span></span>

-   [<span data-ttu-id="b8ca1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8ca1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8ca1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8ca1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8ca1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8ca1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8ca1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8ca1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b8ca1-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-130">Entry</span></span> | <span data-ttu-id="b8ca1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ca1-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ca1-134">System-Only</span></span>            | <span data-ttu-id="b8ca1-135">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-135">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ca1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ca1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-137">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ca1-138">Is Indexed</span></span>             | <span data-ttu-id="b8ca1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-139">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ca1-140">In Global Catalog</span></span>      | <span data-ttu-id="b8ca1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-141">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ca1-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ca1-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="b8ca1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ca1-144">Range-Lower</span></span>            | <span data-ttu-id="b8ca1-145">0</span><span class="sxs-lookup"><span data-stu-id="b8ca1-145">0</span></span>                                                                |
| <span data-ttu-id="b8ca1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ca1-146">Range-Upper</span></span>            | <span data-ttu-id="b8ca1-147">16</span><span class="sxs-lookup"><span data-stu-id="b8ca1-147">16</span></span>                                                               |
| <span data-ttu-id="b8ca1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-148">Search-Flags</span></span>           | <span data-ttu-id="b8ca1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ca1-149">0x00000000</span></span>                                                       |
| <span data-ttu-id="b8ca1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-150">System-Flags</span></span>           | <span data-ttu-id="b8ca1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ca1-151">0x00000010</span></span>                                                       |
| <span data-ttu-id="b8ca1-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ca1-152">Classes used in</span></span>        | [<span data-ttu-id="b8ca1-153">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8ca1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8ca1-154">Windows Server 2003</span></span>



| <span data-ttu-id="b8ca1-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-155">Entry</span></span> | <span data-ttu-id="b8ca1-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-156">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ca1-157">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-158">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ca1-159">System-Only</span></span>            | <span data-ttu-id="b8ca1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-160">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ca1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ca1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-162">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ca1-163">Is Indexed</span></span>             | <span data-ttu-id="b8ca1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-164">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ca1-165">In Global Catalog</span></span>      | <span data-ttu-id="b8ca1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-166">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ca1-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ca1-168">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="b8ca1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ca1-169">Range-Lower</span></span>            | <span data-ttu-id="b8ca1-170">0</span><span class="sxs-lookup"><span data-stu-id="b8ca1-170">0</span></span>                                                                |
| <span data-ttu-id="b8ca1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ca1-171">Range-Upper</span></span>            | <span data-ttu-id="b8ca1-172">16</span><span class="sxs-lookup"><span data-stu-id="b8ca1-172">16</span></span>                                                               |
| <span data-ttu-id="b8ca1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-173">Search-Flags</span></span>           | <span data-ttu-id="b8ca1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ca1-174">0x00000000</span></span>                                                       |
| <span data-ttu-id="b8ca1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-175">System-Flags</span></span>           | <span data-ttu-id="b8ca1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ca1-176">0x00000010</span></span>                                                       |
| <span data-ttu-id="b8ca1-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ca1-177">Classes used in</span></span>        | [<span data-ttu-id="b8ca1-178">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-178">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8ca1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8ca1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8ca1-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-180">Entry</span></span> | <span data-ttu-id="b8ca1-181">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-181">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ca1-182">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-183">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ca1-184">System-Only</span></span>            | <span data-ttu-id="b8ca1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-185">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ca1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ca1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-187">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ca1-188">Is Indexed</span></span>             | <span data-ttu-id="b8ca1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-189">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ca1-190">In Global Catalog</span></span>      | <span data-ttu-id="b8ca1-191">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-191">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ca1-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ca1-193">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="b8ca1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ca1-194">Range-Lower</span></span>            | <span data-ttu-id="b8ca1-195">0</span><span class="sxs-lookup"><span data-stu-id="b8ca1-195">0</span></span>                                                                |
| <span data-ttu-id="b8ca1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ca1-196">Range-Upper</span></span>            | <span data-ttu-id="b8ca1-197">16</span><span class="sxs-lookup"><span data-stu-id="b8ca1-197">16</span></span>                                                               |
| <span data-ttu-id="b8ca1-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-198">Search-Flags</span></span>           | <span data-ttu-id="b8ca1-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ca1-199">0x00000000</span></span>                                                       |
| <span data-ttu-id="b8ca1-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-200">System-Flags</span></span>           | <span data-ttu-id="b8ca1-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ca1-201">0x00000010</span></span>                                                       |
| <span data-ttu-id="b8ca1-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ca1-202">Classes used in</span></span>        | [<span data-ttu-id="b8ca1-203">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-203">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8ca1-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8ca1-204">Windows Server 2008</span></span>



| <span data-ttu-id="b8ca1-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-205">Entry</span></span> | <span data-ttu-id="b8ca1-206">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-206">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ca1-207">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-208">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ca1-209">System-Only</span></span>            | <span data-ttu-id="b8ca1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-210">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ca1-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ca1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-212">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ca1-213">Is Indexed</span></span>             | <span data-ttu-id="b8ca1-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-214">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ca1-215">In Global Catalog</span></span>      | <span data-ttu-id="b8ca1-216">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-216">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ca1-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ca1-218">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="b8ca1-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ca1-219">Range-Lower</span></span>            | <span data-ttu-id="b8ca1-220">0</span><span class="sxs-lookup"><span data-stu-id="b8ca1-220">0</span></span>                                                                |
| <span data-ttu-id="b8ca1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ca1-221">Range-Upper</span></span>            | <span data-ttu-id="b8ca1-222">16</span><span class="sxs-lookup"><span data-stu-id="b8ca1-222">16</span></span>                                                               |
| <span data-ttu-id="b8ca1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-223">Search-Flags</span></span>           | <span data-ttu-id="b8ca1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ca1-224">0x00000000</span></span>                                                       |
| <span data-ttu-id="b8ca1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-225">System-Flags</span></span>           | <span data-ttu-id="b8ca1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ca1-226">0x00000010</span></span>                                                       |
| <span data-ttu-id="b8ca1-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ca1-227">Classes used in</span></span>        | [<span data-ttu-id="b8ca1-228">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-228">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8ca1-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8ca1-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8ca1-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-230">Entry</span></span> | <span data-ttu-id="b8ca1-231">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-231">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ca1-232">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-233">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ca1-234">System-Only</span></span>            | <span data-ttu-id="b8ca1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-235">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ca1-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ca1-237">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-237">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ca1-238">Is Indexed</span></span>             | <span data-ttu-id="b8ca1-239">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-239">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ca1-240">In Global Catalog</span></span>      | <span data-ttu-id="b8ca1-241">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-241">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ca1-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ca1-243">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="b8ca1-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ca1-244">Range-Lower</span></span>            | <span data-ttu-id="b8ca1-245">0</span><span class="sxs-lookup"><span data-stu-id="b8ca1-245">0</span></span>                                                                |
| <span data-ttu-id="b8ca1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ca1-246">Range-Upper</span></span>            | <span data-ttu-id="b8ca1-247">16</span><span class="sxs-lookup"><span data-stu-id="b8ca1-247">16</span></span>                                                               |
| <span data-ttu-id="b8ca1-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-248">Search-Flags</span></span>           | <span data-ttu-id="b8ca1-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ca1-249">0x00000000</span></span>                                                       |
| <span data-ttu-id="b8ca1-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-250">System-Flags</span></span>           | <span data-ttu-id="b8ca1-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ca1-251">0x00000010</span></span>                                                       |
| <span data-ttu-id="b8ca1-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ca1-252">Classes used in</span></span>        | [<span data-ttu-id="b8ca1-253">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-253">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8ca1-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8ca1-254">Windows Server 2012</span></span>



| <span data-ttu-id="b8ca1-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8ca1-255">Entry</span></span> | <span data-ttu-id="b8ca1-256">Valor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-256">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b8ca1-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="b8ca1-257">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8ca1-258">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="b8ca1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8ca1-259">System-Only</span></span>            | <span data-ttu-id="b8ca1-260">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-260">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b8ca1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b8ca1-262">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-262">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="b8ca1-263">Is Indexed</span></span>             | <span data-ttu-id="b8ca1-264">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-264">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8ca1-265">In Global Catalog</span></span>      | <span data-ttu-id="b8ca1-266">Falso</span><span class="sxs-lookup"><span data-stu-id="b8ca1-266">False</span></span>                                                            |
| <span data-ttu-id="b8ca1-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b8ca1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8ca1-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b8ca1-268">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="b8ca1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8ca1-269">Range-Lower</span></span>            | <span data-ttu-id="b8ca1-270">0</span><span class="sxs-lookup"><span data-stu-id="b8ca1-270">0</span></span>                                                                |
| <span data-ttu-id="b8ca1-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8ca1-271">Range-Upper</span></span>            | <span data-ttu-id="b8ca1-272">16</span><span class="sxs-lookup"><span data-stu-id="b8ca1-272">16</span></span>                                                               |
| <span data-ttu-id="b8ca1-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-273">Search-Flags</span></span>           | <span data-ttu-id="b8ca1-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8ca1-274">0x00000000</span></span>                                                       |
| <span data-ttu-id="b8ca1-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8ca1-275">System-Flags</span></span>           | <span data-ttu-id="b8ca1-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8ca1-276">0x00000010</span></span>                                                       |
| <span data-ttu-id="b8ca1-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b8ca1-277">Classes used in</span></span>        | [<span data-ttu-id="b8ca1-278">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="b8ca1-278">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





