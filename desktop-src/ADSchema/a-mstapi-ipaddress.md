---
title: atributo ms-TAPI-IP-address
description: Endereços IP de um computador cliente TAPI no qual um usuário está conectado. Esse atributo pode ser usado como um atributo genérico para manter os endereços IP do computador.
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- MS-TAPI-IP-address atributo AD Schema
- Esquema de AD do atributo msTAPI-IpAddress
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919464"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="b7549-106">atributo ms-TAPI-IP-address</span><span class="sxs-lookup"><span data-stu-id="b7549-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="b7549-107">Endereços IP de um computador cliente TAPI no qual um usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="b7549-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="b7549-108">Esse atributo pode ser usado como um atributo genérico para manter os endereços IP do computador.</span><span class="sxs-lookup"><span data-stu-id="b7549-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="b7549-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7549-109">Entry</span></span> | <span data-ttu-id="b7549-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b7549-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="b7549-111">CN</span><span class="sxs-lookup"><span data-stu-id="b7549-111">CN</span></span>                | <span data-ttu-id="b7549-112">MS-TAPI-IP-address</span><span class="sxs-lookup"><span data-stu-id="b7549-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="b7549-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b7549-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b7549-114">msTAPI-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b7549-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="b7549-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b7549-115">Size</span></span>              | <span data-ttu-id="b7549-116">Cada endereço IP é armazenado como uma cadeia de caracteres em uma notação. B. C. D.</span><span class="sxs-lookup"><span data-stu-id="b7549-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="b7549-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b7549-117">Update Privilege</span></span>  | <span data-ttu-id="b7549-118">Nenhum privilégio especial é necessário.</span><span class="sxs-lookup"><span data-stu-id="b7549-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="b7549-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b7549-119">Update Frequency</span></span>  | <span data-ttu-id="b7549-120">Normalmente muito baixo.</span><span class="sxs-lookup"><span data-stu-id="b7549-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="b7549-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7549-121">Attribute-Id</span></span>      | <span data-ttu-id="b7549-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="b7549-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="b7549-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b7549-123">System-Id-Guid</span></span>    | <span data-ttu-id="b7549-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="b7549-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="b7549-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7549-125">Syntax</span></span>            | [<span data-ttu-id="b7549-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b7549-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="b7549-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="b7549-127">Implementations</span></span>

-   [<span data-ttu-id="b7549-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7549-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7549-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7549-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7549-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7549-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7549-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7549-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7549-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7549-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b7549-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7549-133">Windows Server 2003</span></span>



| <span data-ttu-id="b7549-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7549-134">Entry</span></span> | <span data-ttu-id="b7549-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b7549-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b7549-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7549-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7549-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7549-138">System-Only</span></span>            | <span data-ttu-id="b7549-139">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-139">False</span></span>                                                     |
| <span data-ttu-id="b7549-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7549-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b7549-141">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-141">False</span></span>                                                     |
| <span data-ttu-id="b7549-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7549-142">Is Indexed</span></span>             | <span data-ttu-id="b7549-143">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-143">False</span></span>                                                     |
| <span data-ttu-id="b7549-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7549-144">In Global Catalog</span></span>      | <span data-ttu-id="b7549-145">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-145">False</span></span>                                                     |
| <span data-ttu-id="b7549-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7549-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7549-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7549-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b7549-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7549-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7549-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-150">Search-Flags</span></span>           | <span data-ttu-id="b7549-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7549-151">0x00000000</span></span>                                                |
| <span data-ttu-id="b7549-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-152">System-Flags</span></span>           | <span data-ttu-id="b7549-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7549-153">0x00000010</span></span>                                                |
| <span data-ttu-id="b7549-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7549-154">Classes used in</span></span>        | [<span data-ttu-id="b7549-155">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="b7549-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7549-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7549-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7549-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7549-157">Entry</span></span> | <span data-ttu-id="b7549-158">Valor</span><span class="sxs-lookup"><span data-stu-id="b7549-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b7549-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7549-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7549-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7549-161">System-Only</span></span>            | <span data-ttu-id="b7549-162">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-162">False</span></span>                                                     |
| <span data-ttu-id="b7549-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7549-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b7549-164">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-164">False</span></span>                                                     |
| <span data-ttu-id="b7549-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7549-165">Is Indexed</span></span>             | <span data-ttu-id="b7549-166">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-166">False</span></span>                                                     |
| <span data-ttu-id="b7549-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7549-167">In Global Catalog</span></span>      | <span data-ttu-id="b7549-168">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-168">False</span></span>                                                     |
| <span data-ttu-id="b7549-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7549-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7549-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7549-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b7549-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7549-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7549-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-173">Search-Flags</span></span>           | <span data-ttu-id="b7549-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7549-174">0x00000000</span></span>                                                |
| <span data-ttu-id="b7549-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-175">System-Flags</span></span>           | <span data-ttu-id="b7549-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7549-176">0x00000010</span></span>                                                |
| <span data-ttu-id="b7549-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7549-177">Classes used in</span></span>        | [<span data-ttu-id="b7549-178">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="b7549-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7549-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7549-179">Windows Server 2008</span></span>



| <span data-ttu-id="b7549-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7549-180">Entry</span></span> | <span data-ttu-id="b7549-181">Valor</span><span class="sxs-lookup"><span data-stu-id="b7549-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b7549-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7549-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7549-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7549-184">System-Only</span></span>            | <span data-ttu-id="b7549-185">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-185">False</span></span>                                                     |
| <span data-ttu-id="b7549-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7549-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b7549-187">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-187">False</span></span>                                                     |
| <span data-ttu-id="b7549-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7549-188">Is Indexed</span></span>             | <span data-ttu-id="b7549-189">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-189">False</span></span>                                                     |
| <span data-ttu-id="b7549-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7549-190">In Global Catalog</span></span>      | <span data-ttu-id="b7549-191">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-191">False</span></span>                                                     |
| <span data-ttu-id="b7549-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7549-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7549-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7549-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b7549-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7549-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7549-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-196">Search-Flags</span></span>           | <span data-ttu-id="b7549-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7549-197">0x00000000</span></span>                                                |
| <span data-ttu-id="b7549-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-198">System-Flags</span></span>           | <span data-ttu-id="b7549-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7549-199">0x00000010</span></span>                                                |
| <span data-ttu-id="b7549-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7549-200">Classes used in</span></span>        | [<span data-ttu-id="b7549-201">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="b7549-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7549-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7549-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7549-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7549-203">Entry</span></span> | <span data-ttu-id="b7549-204">Valor</span><span class="sxs-lookup"><span data-stu-id="b7549-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b7549-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7549-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7549-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7549-207">System-Only</span></span>            | <span data-ttu-id="b7549-208">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-208">False</span></span>                                                     |
| <span data-ttu-id="b7549-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7549-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b7549-210">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-210">False</span></span>                                                     |
| <span data-ttu-id="b7549-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7549-211">Is Indexed</span></span>             | <span data-ttu-id="b7549-212">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-212">False</span></span>                                                     |
| <span data-ttu-id="b7549-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7549-213">In Global Catalog</span></span>      | <span data-ttu-id="b7549-214">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-214">False</span></span>                                                     |
| <span data-ttu-id="b7549-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7549-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7549-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7549-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b7549-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7549-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7549-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-219">Search-Flags</span></span>           | <span data-ttu-id="b7549-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7549-220">0x00000000</span></span>                                                |
| <span data-ttu-id="b7549-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-221">System-Flags</span></span>           | <span data-ttu-id="b7549-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7549-222">0x00000010</span></span>                                                |
| <span data-ttu-id="b7549-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7549-223">Classes used in</span></span>        | [<span data-ttu-id="b7549-224">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="b7549-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7549-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7549-225">Windows Server 2012</span></span>



| <span data-ttu-id="b7549-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="b7549-226">Entry</span></span> | <span data-ttu-id="b7549-227">Valor</span><span class="sxs-lookup"><span data-stu-id="b7549-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b7549-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="b7549-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7549-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="b7549-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7549-230">System-Only</span></span>            | <span data-ttu-id="b7549-231">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-231">False</span></span>                                                     |
| <span data-ttu-id="b7549-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b7549-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b7549-233">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-233">False</span></span>                                                     |
| <span data-ttu-id="b7549-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="b7549-234">Is Indexed</span></span>             | <span data-ttu-id="b7549-235">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-235">False</span></span>                                                     |
| <span data-ttu-id="b7549-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b7549-236">In Global Catalog</span></span>      | <span data-ttu-id="b7549-237">Falso</span><span class="sxs-lookup"><span data-stu-id="b7549-237">False</span></span>                                                     |
| <span data-ttu-id="b7549-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b7549-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7549-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b7549-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="b7549-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7549-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7549-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="b7549-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-242">Search-Flags</span></span>           | <span data-ttu-id="b7549-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7549-243">0x00000000</span></span>                                                |
| <span data-ttu-id="b7549-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7549-244">System-Flags</span></span>           | <span data-ttu-id="b7549-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7549-245">0x00000010</span></span>                                                |
| <span data-ttu-id="b7549-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b7549-246">Classes used in</span></span>        | [<span data-ttu-id="b7549-247">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="b7549-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





