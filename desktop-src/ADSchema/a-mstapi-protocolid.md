---
title: atributo ms-TAPI-Protocol-ID
description: Esse atributo indica o tipo de conferência TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-TAPI-Protocol-ID
- Esquema de AD do atributo msTAPI-Protocolid
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087044"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="99199-105">atributo ms-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="99199-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="99199-106">Esse atributo indica o tipo de conferência TAPI.</span><span class="sxs-lookup"><span data-stu-id="99199-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="99199-107">Esse atributo é usado para determinar como o BLOB binário no atributo [**MS-TAPI-Conference-blob**](a-mstapi-conferenceblob.md) deve ser interpretado.</span><span class="sxs-lookup"><span data-stu-id="99199-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="99199-108">Esse atributo é uma cadeia de caracteres arbitrária, normalmente com menos de 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="99199-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="99199-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="99199-109">Entry</span></span> | <span data-ttu-id="99199-110">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="99199-111">CN</span><span class="sxs-lookup"><span data-stu-id="99199-111">CN</span></span>                | <span data-ttu-id="99199-112">MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="99199-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="99199-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="99199-113">Ldap-Display-Name</span></span> | <span data-ttu-id="99199-114">msTAPI-Protocolid</span><span class="sxs-lookup"><span data-stu-id="99199-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="99199-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="99199-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="99199-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="99199-116">Update Privilege</span></span>  | <span data-ttu-id="99199-117">Nenhum privilégio especial é necessário.</span><span class="sxs-lookup"><span data-stu-id="99199-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="99199-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="99199-118">Update Frequency</span></span>  | <span data-ttu-id="99199-119">Defina uma vez no momento da criação do objeto de Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="99199-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="99199-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="99199-120">Attribute-Id</span></span>      | <span data-ttu-id="99199-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="99199-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="99199-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="99199-122">System-Id-Guid</span></span>    | <span data-ttu-id="99199-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="99199-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="99199-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="99199-124">Syntax</span></span>            | [<span data-ttu-id="99199-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="99199-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="99199-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="99199-126">Implementations</span></span>

-   [<span data-ttu-id="99199-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="99199-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="99199-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="99199-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="99199-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="99199-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="99199-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="99199-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="99199-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="99199-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="99199-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99199-132">Windows Server 2003</span></span>



| <span data-ttu-id="99199-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="99199-133">Entry</span></span> | <span data-ttu-id="99199-134">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="99199-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="99199-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99199-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="99199-137">System-Only</span></span>            | <span data-ttu-id="99199-138">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-138">False</span></span>                                                             |
| <span data-ttu-id="99199-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99199-139">Is-Single-Valued</span></span>       | <span data-ttu-id="99199-140">True</span><span class="sxs-lookup"><span data-stu-id="99199-140">True</span></span>                                                              |
| <span data-ttu-id="99199-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="99199-141">Is Indexed</span></span>             | <span data-ttu-id="99199-142">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-142">False</span></span>                                                             |
| <span data-ttu-id="99199-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99199-143">In Global Catalog</span></span>      | <span data-ttu-id="99199-144">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-144">False</span></span>                                                             |
| <span data-ttu-id="99199-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99199-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="99199-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99199-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="99199-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99199-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="99199-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99199-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="99199-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-149">Search-Flags</span></span>           | <span data-ttu-id="99199-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99199-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="99199-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-151">System-Flags</span></span>           | <span data-ttu-id="99199-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99199-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="99199-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99199-153">Classes used in</span></span>        | [<span data-ttu-id="99199-154">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99199-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="99199-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="99199-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="99199-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="99199-156">Entry</span></span> | <span data-ttu-id="99199-157">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="99199-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="99199-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99199-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="99199-160">System-Only</span></span>            | <span data-ttu-id="99199-161">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-161">False</span></span>                                                             |
| <span data-ttu-id="99199-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99199-162">Is-Single-Valued</span></span>       | <span data-ttu-id="99199-163">True</span><span class="sxs-lookup"><span data-stu-id="99199-163">True</span></span>                                                              |
| <span data-ttu-id="99199-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="99199-164">Is Indexed</span></span>             | <span data-ttu-id="99199-165">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-165">False</span></span>                                                             |
| <span data-ttu-id="99199-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99199-166">In Global Catalog</span></span>      | <span data-ttu-id="99199-167">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-167">False</span></span>                                                             |
| <span data-ttu-id="99199-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99199-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="99199-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99199-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="99199-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99199-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="99199-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99199-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="99199-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-172">Search-Flags</span></span>           | <span data-ttu-id="99199-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99199-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="99199-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-174">System-Flags</span></span>           | <span data-ttu-id="99199-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99199-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="99199-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99199-176">Classes used in</span></span>        | [<span data-ttu-id="99199-177">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99199-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="99199-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99199-178">Windows Server 2008</span></span>



| <span data-ttu-id="99199-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="99199-179">Entry</span></span> | <span data-ttu-id="99199-180">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="99199-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="99199-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99199-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="99199-183">System-Only</span></span>            | <span data-ttu-id="99199-184">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-184">False</span></span>                                                             |
| <span data-ttu-id="99199-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99199-185">Is-Single-Valued</span></span>       | <span data-ttu-id="99199-186">True</span><span class="sxs-lookup"><span data-stu-id="99199-186">True</span></span>                                                              |
| <span data-ttu-id="99199-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="99199-187">Is Indexed</span></span>             | <span data-ttu-id="99199-188">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-188">False</span></span>                                                             |
| <span data-ttu-id="99199-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99199-189">In Global Catalog</span></span>      | <span data-ttu-id="99199-190">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-190">False</span></span>                                                             |
| <span data-ttu-id="99199-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99199-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="99199-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99199-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="99199-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99199-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="99199-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99199-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="99199-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-195">Search-Flags</span></span>           | <span data-ttu-id="99199-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99199-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="99199-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-197">System-Flags</span></span>           | <span data-ttu-id="99199-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99199-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="99199-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99199-199">Classes used in</span></span>        | [<span data-ttu-id="99199-200">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99199-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="99199-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99199-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="99199-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="99199-202">Entry</span></span> | <span data-ttu-id="99199-203">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="99199-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="99199-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99199-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="99199-206">System-Only</span></span>            | <span data-ttu-id="99199-207">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-207">False</span></span>                                                             |
| <span data-ttu-id="99199-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99199-208">Is-Single-Valued</span></span>       | <span data-ttu-id="99199-209">True</span><span class="sxs-lookup"><span data-stu-id="99199-209">True</span></span>                                                              |
| <span data-ttu-id="99199-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="99199-210">Is Indexed</span></span>             | <span data-ttu-id="99199-211">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-211">False</span></span>                                                             |
| <span data-ttu-id="99199-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99199-212">In Global Catalog</span></span>      | <span data-ttu-id="99199-213">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-213">False</span></span>                                                             |
| <span data-ttu-id="99199-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99199-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="99199-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99199-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="99199-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99199-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="99199-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99199-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="99199-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-218">Search-Flags</span></span>           | <span data-ttu-id="99199-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99199-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="99199-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-220">System-Flags</span></span>           | <span data-ttu-id="99199-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99199-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="99199-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99199-222">Classes used in</span></span>        | [<span data-ttu-id="99199-223">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99199-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="99199-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99199-224">Windows Server 2012</span></span>



| <span data-ttu-id="99199-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="99199-225">Entry</span></span> | <span data-ttu-id="99199-226">Valor</span><span class="sxs-lookup"><span data-stu-id="99199-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="99199-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="99199-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="99199-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="99199-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="99199-229">System-Only</span></span>            | <span data-ttu-id="99199-230">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-230">False</span></span>                                                             |
| <span data-ttu-id="99199-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="99199-231">Is-Single-Valued</span></span>       | <span data-ttu-id="99199-232">True</span><span class="sxs-lookup"><span data-stu-id="99199-232">True</span></span>                                                              |
| <span data-ttu-id="99199-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="99199-233">Is Indexed</span></span>             | <span data-ttu-id="99199-234">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-234">False</span></span>                                                             |
| <span data-ttu-id="99199-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="99199-235">In Global Catalog</span></span>      | <span data-ttu-id="99199-236">Falso</span><span class="sxs-lookup"><span data-stu-id="99199-236">False</span></span>                                                             |
| <span data-ttu-id="99199-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="99199-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="99199-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="99199-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="99199-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="99199-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="99199-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="99199-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="99199-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-241">Search-Flags</span></span>           | <span data-ttu-id="99199-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="99199-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="99199-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="99199-243">System-Flags</span></span>           | <span data-ttu-id="99199-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="99199-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="99199-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="99199-245">Classes used in</span></span>        | [<span data-ttu-id="99199-246">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="99199-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





