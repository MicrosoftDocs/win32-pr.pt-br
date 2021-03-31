---
title: msSFU-30-Order-atributo de número
description: Contém um valor que é usado pelo NIS para verificar se o mapa foi alterado.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- msSFU-30-Order-número de atributo do AD Schema
- Esquema de AD do atributo msSFU30OrderNumber
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086897"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="1dc5f-105">msSFU-30-Order-atributo de número</span><span class="sxs-lookup"><span data-stu-id="1dc5f-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="1dc5f-106">Contém um valor que é usado pelo NIS para verificar se o mapa foi alterado.</span><span class="sxs-lookup"><span data-stu-id="1dc5f-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="1dc5f-107">Toda vez que os dados armazenados no objeto [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md) são alterados, esse valor é incrementado.</span><span class="sxs-lookup"><span data-stu-id="1dc5f-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="1dc5f-108">Esse valor é usado para rastrear as alterações de dados entre chamadas **ypxfer** .</span><span class="sxs-lookup"><span data-stu-id="1dc5f-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="1dc5f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dc5f-109">Entry</span></span> | <span data-ttu-id="1dc5f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1dc5f-111">CN</span><span class="sxs-lookup"><span data-stu-id="1dc5f-111">CN</span></span>                | <span data-ttu-id="1dc5f-112">msSFU-30-ordem-número</span><span class="sxs-lookup"><span data-stu-id="1dc5f-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="1dc5f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1dc5f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1dc5f-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="1dc5f-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="1dc5f-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1dc5f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="1dc5f-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1dc5f-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1dc5f-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1dc5f-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1dc5f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1dc5f-118">Attribute-Id</span></span>      | <span data-ttu-id="1dc5f-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="1dc5f-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="1dc5f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1dc5f-120">System-Id-Guid</span></span>    | <span data-ttu-id="1dc5f-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="1dc5f-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="1dc5f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc5f-122">Syntax</span></span>            | [<span data-ttu-id="1dc5f-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1dc5f-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="1dc5f-124">Implementations</span></span>

-   [<span data-ttu-id="1dc5f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1dc5f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1dc5f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1dc5f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="1dc5f-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1dc5f-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1dc5f-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dc5f-130">Entry</span></span> | <span data-ttu-id="1dc5f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1dc5f-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="1dc5f-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dc5f-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dc5f-134">System-Only</span></span>            | <span data-ttu-id="1dc5f-135">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-135">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1dc5f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1dc5f-137">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-137">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="1dc5f-138">Is Indexed</span></span>             | <span data-ttu-id="1dc5f-139">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-139">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1dc5f-140">In Global Catalog</span></span>      | <span data-ttu-id="1dc5f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-141">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dc5f-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1dc5f-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="1dc5f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dc5f-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dc5f-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-146">Search-Flags</span></span>           | <span data-ttu-id="1dc5f-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1dc5f-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="1dc5f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-148">System-Flags</span></span>           | <span data-ttu-id="1dc5f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dc5f-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="1dc5f-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1dc5f-150">Classes used in</span></span>        | [<span data-ttu-id="1dc5f-151">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1dc5f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dc5f-152">Windows Server 2008</span></span>



| <span data-ttu-id="1dc5f-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dc5f-153">Entry</span></span> | <span data-ttu-id="1dc5f-154">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1dc5f-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="1dc5f-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dc5f-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dc5f-157">System-Only</span></span>            | <span data-ttu-id="1dc5f-158">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-158">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1dc5f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1dc5f-160">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-160">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="1dc5f-161">Is Indexed</span></span>             | <span data-ttu-id="1dc5f-162">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-162">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1dc5f-163">In Global Catalog</span></span>      | <span data-ttu-id="1dc5f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-164">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dc5f-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1dc5f-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="1dc5f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dc5f-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dc5f-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-169">Search-Flags</span></span>           | <span data-ttu-id="1dc5f-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1dc5f-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="1dc5f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-171">System-Flags</span></span>           | <span data-ttu-id="1dc5f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dc5f-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="1dc5f-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1dc5f-173">Classes used in</span></span>        | [<span data-ttu-id="1dc5f-174">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1dc5f-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1dc5f-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1dc5f-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dc5f-176">Entry</span></span> | <span data-ttu-id="1dc5f-177">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1dc5f-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="1dc5f-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dc5f-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dc5f-180">System-Only</span></span>            | <span data-ttu-id="1dc5f-181">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-181">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1dc5f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1dc5f-183">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-183">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="1dc5f-184">Is Indexed</span></span>             | <span data-ttu-id="1dc5f-185">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-185">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1dc5f-186">In Global Catalog</span></span>      | <span data-ttu-id="1dc5f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-187">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dc5f-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1dc5f-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="1dc5f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dc5f-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dc5f-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-192">Search-Flags</span></span>           | <span data-ttu-id="1dc5f-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1dc5f-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="1dc5f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-194">System-Flags</span></span>           | <span data-ttu-id="1dc5f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dc5f-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="1dc5f-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1dc5f-196">Classes used in</span></span>        | [<span data-ttu-id="1dc5f-197">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1dc5f-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1dc5f-198">Windows Server 2012</span></span>



| <span data-ttu-id="1dc5f-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="1dc5f-199">Entry</span></span> | <span data-ttu-id="1dc5f-200">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1dc5f-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="1dc5f-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1dc5f-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="1dc5f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1dc5f-203">System-Only</span></span>            | <span data-ttu-id="1dc5f-204">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-204">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1dc5f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1dc5f-206">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-206">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="1dc5f-207">Is Indexed</span></span>             | <span data-ttu-id="1dc5f-208">True</span><span class="sxs-lookup"><span data-stu-id="1dc5f-208">True</span></span>                                                           |
| <span data-ttu-id="1dc5f-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1dc5f-209">In Global Catalog</span></span>      | <span data-ttu-id="1dc5f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="1dc5f-210">False</span></span>                                                          |
| <span data-ttu-id="1dc5f-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1dc5f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1dc5f-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1dc5f-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="1dc5f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1dc5f-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1dc5f-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="1dc5f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-215">Search-Flags</span></span>           | <span data-ttu-id="1dc5f-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1dc5f-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="1dc5f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1dc5f-217">System-Flags</span></span>           | <span data-ttu-id="1dc5f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1dc5f-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="1dc5f-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1dc5f-219">Classes used in</span></span>        | [<span data-ttu-id="1dc5f-220">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="1dc5f-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





