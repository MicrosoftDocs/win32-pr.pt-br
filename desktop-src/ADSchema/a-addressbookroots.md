---
title: Atributo Address-Book-raízes
description: Usado pelo Exchange. O Exchange configura árvores de contêineres de catálogo de endereços para aparecer no catálogo de endereços MAPI. Esse atributo no objeto de configuração do Exchange lista as raízes das árvores de contêiner do catálogo de endereços. | Atributo Address-Book-raízes
ms.assetid: 7e6d2677-9818-4870-8429-50f73f9c8c1f
ms.tgt_platform: multiple
keywords:
- Atributo de raiz de catálogo de endereços-esquema do AD
- Esquema de AD do atributo addressBookRoots
topic_type:
- apiref
api_name:
- Address-Book-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab195744bb7fb5029a9a48aeca55d703e6e05b62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756067"
---
# <a name="address-book-roots-attribute"></a><span data-ttu-id="ddf24-108">Atributo Address-Book-raízes</span><span class="sxs-lookup"><span data-stu-id="ddf24-108">Address-Book-Roots attribute</span></span>

<span data-ttu-id="ddf24-109">Usado pelo Exchange.</span><span class="sxs-lookup"><span data-stu-id="ddf24-109">Used by Exchange.</span></span> <span data-ttu-id="ddf24-110">O Exchange configura árvores de contêineres de catálogo de endereços para aparecer no catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="ddf24-110">Exchange configures trees of address book containers to show up in the MAPI address book.</span></span> <span data-ttu-id="ddf24-111">Esse atributo no objeto de configuração do Exchange lista as raízes das árvores de contêiner do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ddf24-111">This attribute on the Exchange Config object lists the roots of the address book container trees.</span></span>



| <span data-ttu-id="ddf24-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-112">Entry</span></span> | <span data-ttu-id="ddf24-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-113">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ddf24-114">CN</span><span class="sxs-lookup"><span data-stu-id="ddf24-114">CN</span></span>                | <span data-ttu-id="ddf24-115">Raízes de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="ddf24-115">Address-Book-Roots</span></span>                      |
| <span data-ttu-id="ddf24-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ddf24-116">Ldap-Display-Name</span></span> | <span data-ttu-id="ddf24-117">addressBookRoots</span><span class="sxs-lookup"><span data-stu-id="ddf24-117">addressBookRoots</span></span>                        |
| <span data-ttu-id="ddf24-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ddf24-118">Size</span></span>              | \-                                      |
| <span data-ttu-id="ddf24-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ddf24-119">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="ddf24-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ddf24-120">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="ddf24-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-121">Attribute-Id</span></span>      | <span data-ttu-id="ddf24-122">1.2.840.113556.1.4.1244</span><span class="sxs-lookup"><span data-stu-id="ddf24-122">1.2.840.113556.1.4.1244</span></span>                 |
| <span data-ttu-id="ddf24-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ddf24-123">System-Id-Guid</span></span>    | <span data-ttu-id="ddf24-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="ddf24-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="ddf24-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddf24-125">Syntax</span></span>            | [<span data-ttu-id="ddf24-126">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ddf24-126">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ddf24-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="ddf24-127">Implementations</span></span>

-   [<span data-ttu-id="ddf24-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ddf24-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ddf24-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ddf24-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ddf24-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ddf24-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ddf24-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ddf24-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ddf24-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ddf24-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ddf24-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ddf24-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ddf24-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ddf24-134">Windows 2000 Server</span></span>



| <span data-ttu-id="ddf24-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-135">Entry</span></span> | <span data-ttu-id="ddf24-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-136">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf24-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="ddf24-137">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-138">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf24-139">System-Only</span></span>            | <span data-ttu-id="ddf24-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-140">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ddf24-141">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf24-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-142">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="ddf24-143">Is Indexed</span></span>             | <span data-ttu-id="ddf24-144">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-144">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf24-145">In Global Catalog</span></span>      | <span data-ttu-id="ddf24-146">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-146">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ddf24-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf24-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ddf24-148">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="ddf24-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf24-149">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf24-150">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-151">Search-Flags</span></span>           | <span data-ttu-id="ddf24-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf24-152">0x00000000</span></span>                                                                           |
| <span data-ttu-id="ddf24-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-153">System-Flags</span></span>           | <span data-ttu-id="ddf24-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf24-154">0x00000010</span></span>                                                                           |
| <span data-ttu-id="ddf24-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ddf24-155">Classes used in</span></span>        | [<span data-ttu-id="ddf24-156">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="ddf24-156">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ddf24-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddf24-157">Windows Server 2003</span></span>



| <span data-ttu-id="ddf24-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-158">Entry</span></span> | <span data-ttu-id="ddf24-159">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-159">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf24-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="ddf24-160">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-161">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf24-162">System-Only</span></span>            | <span data-ttu-id="ddf24-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-163">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ddf24-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf24-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-165">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="ddf24-166">Is Indexed</span></span>             | <span data-ttu-id="ddf24-167">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-167">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf24-168">In Global Catalog</span></span>      | <span data-ttu-id="ddf24-169">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-169">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ddf24-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf24-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ddf24-171">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="ddf24-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf24-172">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf24-173">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-174">Search-Flags</span></span>           | <span data-ttu-id="ddf24-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf24-175">0x00000000</span></span>                                                                           |
| <span data-ttu-id="ddf24-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-176">System-Flags</span></span>           | <span data-ttu-id="ddf24-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf24-177">0x00000010</span></span>                                                                           |
| <span data-ttu-id="ddf24-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ddf24-178">Classes used in</span></span>        | [<span data-ttu-id="ddf24-179">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="ddf24-179">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ddf24-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ddf24-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ddf24-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-181">Entry</span></span> | <span data-ttu-id="ddf24-182">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-182">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf24-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="ddf24-183">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-184">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf24-185">System-Only</span></span>            | <span data-ttu-id="ddf24-186">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-186">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ddf24-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf24-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-188">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="ddf24-189">Is Indexed</span></span>             | <span data-ttu-id="ddf24-190">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-190">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf24-191">In Global Catalog</span></span>      | <span data-ttu-id="ddf24-192">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-192">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ddf24-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf24-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ddf24-194">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="ddf24-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf24-195">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf24-196">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-197">Search-Flags</span></span>           | <span data-ttu-id="ddf24-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf24-198">0x00000000</span></span>                                                                           |
| <span data-ttu-id="ddf24-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-199">System-Flags</span></span>           | <span data-ttu-id="ddf24-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf24-200">0x00000010</span></span>                                                                           |
| <span data-ttu-id="ddf24-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ddf24-201">Classes used in</span></span>        | [<span data-ttu-id="ddf24-202">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="ddf24-202">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ddf24-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddf24-203">Windows Server 2008</span></span>



| <span data-ttu-id="ddf24-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-204">Entry</span></span> | <span data-ttu-id="ddf24-205">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf24-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="ddf24-206">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-207">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf24-208">System-Only</span></span>            | <span data-ttu-id="ddf24-209">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-209">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ddf24-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf24-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-211">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="ddf24-212">Is Indexed</span></span>             | <span data-ttu-id="ddf24-213">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-213">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf24-214">In Global Catalog</span></span>      | <span data-ttu-id="ddf24-215">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-215">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ddf24-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf24-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ddf24-217">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="ddf24-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf24-218">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf24-219">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-220">Search-Flags</span></span>           | <span data-ttu-id="ddf24-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf24-221">0x00000000</span></span>                                                                           |
| <span data-ttu-id="ddf24-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-222">System-Flags</span></span>           | <span data-ttu-id="ddf24-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf24-223">0x00000010</span></span>                                                                           |
| <span data-ttu-id="ddf24-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ddf24-224">Classes used in</span></span>        | [<span data-ttu-id="ddf24-225">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="ddf24-225">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ddf24-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ddf24-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ddf24-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-227">Entry</span></span> | <span data-ttu-id="ddf24-228">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-228">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf24-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="ddf24-229">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-230">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf24-231">System-Only</span></span>            | <span data-ttu-id="ddf24-232">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-232">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ddf24-233">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf24-234">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-234">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="ddf24-235">Is Indexed</span></span>             | <span data-ttu-id="ddf24-236">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-236">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf24-237">In Global Catalog</span></span>      | <span data-ttu-id="ddf24-238">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-238">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ddf24-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf24-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ddf24-240">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="ddf24-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf24-241">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf24-242">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-243">Search-Flags</span></span>           | <span data-ttu-id="ddf24-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf24-244">0x00000000</span></span>                                                                           |
| <span data-ttu-id="ddf24-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-245">System-Flags</span></span>           | <span data-ttu-id="ddf24-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf24-246">0x00000010</span></span>                                                                           |
| <span data-ttu-id="ddf24-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ddf24-247">Classes used in</span></span>        | [<span data-ttu-id="ddf24-248">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="ddf24-248">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ddf24-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddf24-249">Windows Server 2012</span></span>



| <span data-ttu-id="ddf24-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="ddf24-250">Entry</span></span> | <span data-ttu-id="ddf24-251">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf24-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf24-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="ddf24-252">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf24-253">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="ddf24-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf24-254">System-Only</span></span>            | <span data-ttu-id="ddf24-255">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-255">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ddf24-256">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf24-257">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-257">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="ddf24-258">Is Indexed</span></span>             | <span data-ttu-id="ddf24-259">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-259">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ddf24-260">In Global Catalog</span></span>      | <span data-ttu-id="ddf24-261">Falso</span><span class="sxs-lookup"><span data-stu-id="ddf24-261">False</span></span>                                                                                |
| <span data-ttu-id="ddf24-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ddf24-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf24-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ddf24-263">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="ddf24-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf24-264">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf24-265">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="ddf24-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-266">Search-Flags</span></span>           | <span data-ttu-id="ddf24-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf24-267">0x00000000</span></span>                                                                           |
| <span data-ttu-id="ddf24-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf24-268">System-Flags</span></span>           | <span data-ttu-id="ddf24-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf24-269">0x00000010</span></span>                                                                           |
| <span data-ttu-id="ddf24-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ddf24-270">Classes used in</span></span>        | [<span data-ttu-id="ddf24-271">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="ddf24-271">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





