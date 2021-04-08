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
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="ffb5b-105">msSFU-30-Order-atributo de número</span><span class="sxs-lookup"><span data-stu-id="ffb5b-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="ffb5b-106">Contém um valor que é usado pelo NIS para verificar se o mapa foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ffb5b-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="ffb5b-107">Toda vez que os dados armazenados no objeto [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md) são alterados, esse valor é incrementado.</span><span class="sxs-lookup"><span data-stu-id="ffb5b-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="ffb5b-108">Esse valor é usado para rastrear as alterações de dados entre chamadas **ypxfer** .</span><span class="sxs-lookup"><span data-stu-id="ffb5b-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="ffb5b-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb5b-109">Entry</span></span> | <span data-ttu-id="ffb5b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ffb5b-111">CN</span><span class="sxs-lookup"><span data-stu-id="ffb5b-111">CN</span></span>                | <span data-ttu-id="ffb5b-112">msSFU-30-ordem-número</span><span class="sxs-lookup"><span data-stu-id="ffb5b-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="ffb5b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ffb5b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ffb5b-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="ffb5b-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="ffb5b-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ffb5b-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ffb5b-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ffb5b-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ffb5b-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ffb5b-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ffb5b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffb5b-118">Attribute-Id</span></span>      | <span data-ttu-id="ffb5b-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="ffb5b-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="ffb5b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ffb5b-120">System-Id-Guid</span></span>    | <span data-ttu-id="ffb5b-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="ffb5b-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="ffb5b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb5b-122">Syntax</span></span>            | [<span data-ttu-id="ffb5b-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ffb5b-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="ffb5b-124">Implementations</span></span>

-   [<span data-ttu-id="ffb5b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffb5b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffb5b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffb5b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffb5b-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffb5b-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffb5b-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb5b-130">Entry</span></span> | <span data-ttu-id="ffb5b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ffb5b-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb5b-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb5b-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb5b-134">System-Only</span></span>            | <span data-ttu-id="ffb5b-135">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-135">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb5b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb5b-137">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-137">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb5b-138">Is Indexed</span></span>             | <span data-ttu-id="ffb5b-139">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-139">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb5b-140">In Global Catalog</span></span>      | <span data-ttu-id="ffb5b-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-141">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb5b-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb5b-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="ffb5b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb5b-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb5b-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-146">Search-Flags</span></span>           | <span data-ttu-id="ffb5b-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffb5b-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="ffb5b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-148">System-Flags</span></span>           | <span data-ttu-id="ffb5b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb5b-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="ffb5b-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb5b-150">Classes used in</span></span>        | [<span data-ttu-id="ffb5b-151">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffb5b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffb5b-152">Windows Server 2008</span></span>



| <span data-ttu-id="ffb5b-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb5b-153">Entry</span></span> | <span data-ttu-id="ffb5b-154">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ffb5b-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb5b-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb5b-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb5b-157">System-Only</span></span>            | <span data-ttu-id="ffb5b-158">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-158">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb5b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb5b-160">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-160">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb5b-161">Is Indexed</span></span>             | <span data-ttu-id="ffb5b-162">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-162">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb5b-163">In Global Catalog</span></span>      | <span data-ttu-id="ffb5b-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-164">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb5b-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb5b-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="ffb5b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb5b-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb5b-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-169">Search-Flags</span></span>           | <span data-ttu-id="ffb5b-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffb5b-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="ffb5b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-171">System-Flags</span></span>           | <span data-ttu-id="ffb5b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb5b-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="ffb5b-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb5b-173">Classes used in</span></span>        | [<span data-ttu-id="ffb5b-174">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffb5b-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffb5b-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffb5b-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb5b-176">Entry</span></span> | <span data-ttu-id="ffb5b-177">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ffb5b-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb5b-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb5b-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb5b-180">System-Only</span></span>            | <span data-ttu-id="ffb5b-181">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-181">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb5b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb5b-183">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-183">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb5b-184">Is Indexed</span></span>             | <span data-ttu-id="ffb5b-185">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-185">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb5b-186">In Global Catalog</span></span>      | <span data-ttu-id="ffb5b-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-187">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb5b-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb5b-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="ffb5b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb5b-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb5b-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-192">Search-Flags</span></span>           | <span data-ttu-id="ffb5b-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffb5b-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="ffb5b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-194">System-Flags</span></span>           | <span data-ttu-id="ffb5b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb5b-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="ffb5b-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb5b-196">Classes used in</span></span>        | [<span data-ttu-id="ffb5b-197">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffb5b-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffb5b-198">Windows Server 2012</span></span>



| <span data-ttu-id="ffb5b-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb5b-199">Entry</span></span> | <span data-ttu-id="ffb5b-200">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ffb5b-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb5b-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb5b-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="ffb5b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb5b-203">System-Only</span></span>            | <span data-ttu-id="ffb5b-204">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-204">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb5b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb5b-206">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-206">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb5b-207">Is Indexed</span></span>             | <span data-ttu-id="ffb5b-208">True</span><span class="sxs-lookup"><span data-stu-id="ffb5b-208">True</span></span>                                                           |
| <span data-ttu-id="ffb5b-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb5b-209">In Global Catalog</span></span>      | <span data-ttu-id="ffb5b-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb5b-210">False</span></span>                                                          |
| <span data-ttu-id="ffb5b-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb5b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb5b-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb5b-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="ffb5b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb5b-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb5b-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="ffb5b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-215">Search-Flags</span></span>           | <span data-ttu-id="ffb5b-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ffb5b-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="ffb5b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb5b-217">System-Flags</span></span>           | <span data-ttu-id="ffb5b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb5b-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="ffb5b-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb5b-219">Classes used in</span></span>        | [<span data-ttu-id="ffb5b-220">**msSFU-30-Domain-info**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





