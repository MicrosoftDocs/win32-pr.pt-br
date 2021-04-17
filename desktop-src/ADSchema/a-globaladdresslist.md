---
title: Atributo de lista de endereços global
description: Esse atributo é usado em um contêiner do Microsoft Exchange para armazenar o nome distinto de uma GAL (lista de endereços global) recém-criada.
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- Atributo global-lista de endereços-esquema do AD
- Esquema de AD do atributo globalAddressList
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105748287"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="0bbc7-105">Atributo de lista de endereços global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-105">Global-Address-List attribute</span></span>

<span data-ttu-id="0bbc7-106">Esse atributo é usado em um contêiner do Microsoft Exchange para armazenar o nome distinto de uma GAL (lista de endereços global) recém-criada.</span><span class="sxs-lookup"><span data-stu-id="0bbc7-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="0bbc7-107">Esse atributo deve ter uma entrada antes que você possa habilitar clientes Messaging Application Programming Interface (MAPI) para usar uma GAL.</span><span class="sxs-lookup"><span data-stu-id="0bbc7-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="0bbc7-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-108">Entry</span></span> | <span data-ttu-id="0bbc7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="0bbc7-110">CN</span><span class="sxs-lookup"><span data-stu-id="0bbc7-110">CN</span></span>                | <span data-ttu-id="0bbc7-111">Lista de endereços global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="0bbc7-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0bbc7-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0bbc7-113">globalAddressList</span><span class="sxs-lookup"><span data-stu-id="0bbc7-113">globalAddressList</span></span>                       |
| <span data-ttu-id="0bbc7-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0bbc7-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="0bbc7-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0bbc7-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="0bbc7-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0bbc7-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="0bbc7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-117">Attribute-Id</span></span>      | <span data-ttu-id="0bbc7-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="0bbc7-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="0bbc7-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0bbc7-119">System-Id-Guid</span></span>    | <span data-ttu-id="0bbc7-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="0bbc7-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="0bbc7-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bbc7-121">Syntax</span></span>            | [<span data-ttu-id="0bbc7-122">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="0bbc7-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="0bbc7-123">Implementations</span></span>

-   [<span data-ttu-id="0bbc7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0bbc7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0bbc7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0bbc7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0bbc7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0bbc7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0bbc7-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bbc7-130">Windows 2000 Server</span></span>



| <span data-ttu-id="0bbc7-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-131">Entry</span></span> | <span data-ttu-id="0bbc7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbc7-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="0bbc7-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbc7-135">System-Only</span></span>            | <span data-ttu-id="0bbc7-136">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-136">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0bbc7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbc7-138">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-138">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="0bbc7-139">Is Indexed</span></span>             | <span data-ttu-id="0bbc7-140">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-140">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-141">In Global Catalog</span></span>      | <span data-ttu-id="0bbc7-142">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-142">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbc7-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0bbc7-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="0bbc7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbc7-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbc7-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-147">Search-Flags</span></span>           | <span data-ttu-id="0bbc7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbc7-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="0bbc7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-149">System-Flags</span></span>           | <span data-ttu-id="0bbc7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbc7-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="0bbc7-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0bbc7-151">Classes used in</span></span>        | [<span data-ttu-id="0bbc7-152">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0bbc7-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0bbc7-153">Windows Server 2003</span></span>



| <span data-ttu-id="0bbc7-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-154">Entry</span></span> | <span data-ttu-id="0bbc7-155">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbc7-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="0bbc7-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbc7-158">System-Only</span></span>            | <span data-ttu-id="0bbc7-159">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-159">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0bbc7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbc7-161">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-161">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="0bbc7-162">Is Indexed</span></span>             | <span data-ttu-id="0bbc7-163">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-163">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-164">In Global Catalog</span></span>      | <span data-ttu-id="0bbc7-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-165">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbc7-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0bbc7-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="0bbc7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbc7-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbc7-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-170">Search-Flags</span></span>           | <span data-ttu-id="0bbc7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbc7-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="0bbc7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-172">System-Flags</span></span>           | <span data-ttu-id="0bbc7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbc7-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="0bbc7-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0bbc7-174">Classes used in</span></span>        | [<span data-ttu-id="0bbc7-175">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0bbc7-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0bbc7-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0bbc7-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-177">Entry</span></span> | <span data-ttu-id="0bbc7-178">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbc7-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="0bbc7-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbc7-181">System-Only</span></span>            | <span data-ttu-id="0bbc7-182">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-182">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0bbc7-183">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbc7-184">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-184">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="0bbc7-185">Is Indexed</span></span>             | <span data-ttu-id="0bbc7-186">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-186">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-187">In Global Catalog</span></span>      | <span data-ttu-id="0bbc7-188">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-188">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbc7-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0bbc7-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="0bbc7-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbc7-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbc7-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-193">Search-Flags</span></span>           | <span data-ttu-id="0bbc7-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbc7-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="0bbc7-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-195">System-Flags</span></span>           | <span data-ttu-id="0bbc7-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbc7-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="0bbc7-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0bbc7-197">Classes used in</span></span>        | [<span data-ttu-id="0bbc7-198">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0bbc7-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bbc7-199">Windows Server 2008</span></span>



| <span data-ttu-id="0bbc7-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-200">Entry</span></span> | <span data-ttu-id="0bbc7-201">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbc7-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="0bbc7-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbc7-204">System-Only</span></span>            | <span data-ttu-id="0bbc7-205">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-205">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0bbc7-206">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbc7-207">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-207">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="0bbc7-208">Is Indexed</span></span>             | <span data-ttu-id="0bbc7-209">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-209">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-210">In Global Catalog</span></span>      | <span data-ttu-id="0bbc7-211">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-211">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbc7-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0bbc7-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="0bbc7-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbc7-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbc7-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-216">Search-Flags</span></span>           | <span data-ttu-id="0bbc7-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbc7-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="0bbc7-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-218">System-Flags</span></span>           | <span data-ttu-id="0bbc7-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbc7-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="0bbc7-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0bbc7-220">Classes used in</span></span>        | [<span data-ttu-id="0bbc7-221">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0bbc7-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0bbc7-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0bbc7-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-223">Entry</span></span> | <span data-ttu-id="0bbc7-224">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbc7-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="0bbc7-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbc7-227">System-Only</span></span>            | <span data-ttu-id="0bbc7-228">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-228">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0bbc7-229">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbc7-230">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-230">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="0bbc7-231">Is Indexed</span></span>             | <span data-ttu-id="0bbc7-232">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-232">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-233">In Global Catalog</span></span>      | <span data-ttu-id="0bbc7-234">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-234">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbc7-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0bbc7-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="0bbc7-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbc7-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbc7-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-239">Search-Flags</span></span>           | <span data-ttu-id="0bbc7-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbc7-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="0bbc7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-241">System-Flags</span></span>           | <span data-ttu-id="0bbc7-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbc7-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="0bbc7-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0bbc7-243">Classes used in</span></span>        | [<span data-ttu-id="0bbc7-244">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0bbc7-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bbc7-245">Windows Server 2012</span></span>



| <span data-ttu-id="0bbc7-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbc7-246">Entry</span></span> | <span data-ttu-id="0bbc7-247">Valor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbc7-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="0bbc7-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbc7-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="0bbc7-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbc7-250">System-Only</span></span>            | <span data-ttu-id="0bbc7-251">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-251">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0bbc7-252">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbc7-253">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-253">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="0bbc7-254">Is Indexed</span></span>             | <span data-ttu-id="0bbc7-255">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-255">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0bbc7-256">In Global Catalog</span></span>      | <span data-ttu-id="0bbc7-257">Falso</span><span class="sxs-lookup"><span data-stu-id="0bbc7-257">False</span></span>                                                                                |
| <span data-ttu-id="0bbc7-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0bbc7-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbc7-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0bbc7-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="0bbc7-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbc7-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbc7-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="0bbc7-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-262">Search-Flags</span></span>           | <span data-ttu-id="0bbc7-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbc7-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="0bbc7-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbc7-264">System-Flags</span></span>           | <span data-ttu-id="0bbc7-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbc7-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="0bbc7-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0bbc7-266">Classes used in</span></span>        | [<span data-ttu-id="0bbc7-267">**Ms-Exch-Configuration-contêiner**</span><span class="sxs-lookup"><span data-stu-id="0bbc7-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





