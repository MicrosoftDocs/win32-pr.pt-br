---
title: atributo ms-TAPI-Unique-Identifier
description: Fornece o nome de uma conferência multicast TAPI. É o atributo de nomenclatura da classe Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- MS-TAPI-atributo de identificador exclusivo do esquema do AD
- Esquema de AD do atributo msTAPI-UID
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369978"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="080cd-106">atributo ms-TAPI-Unique-Identifier</span><span class="sxs-lookup"><span data-stu-id="080cd-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="080cd-107">Fornece o nome de uma conferência multicast TAPI.</span><span class="sxs-lookup"><span data-stu-id="080cd-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="080cd-108">É o atributo de nomenclatura da classe Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="080cd-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="080cd-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="080cd-109">Entry</span></span> | <span data-ttu-id="080cd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="080cd-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="080cd-111">CN</span><span class="sxs-lookup"><span data-stu-id="080cd-111">CN</span></span>                | <span data-ttu-id="080cd-112">MS-TAPI-identificador exclusivo</span><span class="sxs-lookup"><span data-stu-id="080cd-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="080cd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="080cd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="080cd-114">msTAPI-UID</span><span class="sxs-lookup"><span data-stu-id="080cd-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="080cd-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="080cd-115">Size</span></span>              | <span data-ttu-id="080cd-116">Pode ser uma cadeia de caracteres arbitrária, normalmente abaixo de 100 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="080cd-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="080cd-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="080cd-117">Update Privilege</span></span>  | <span data-ttu-id="080cd-118">Nenhum privilégio especial é necessário.</span><span class="sxs-lookup"><span data-stu-id="080cd-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="080cd-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="080cd-119">Update Frequency</span></span>  | <span data-ttu-id="080cd-120">Defina uma vez no momento da criação do objeto de Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="080cd-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="080cd-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="080cd-121">Attribute-Id</span></span>      | <span data-ttu-id="080cd-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="080cd-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="080cd-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="080cd-123">System-Id-Guid</span></span>    | <span data-ttu-id="080cd-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span><span class="sxs-lookup"><span data-stu-id="080cd-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="080cd-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="080cd-125">Syntax</span></span>            | [<span data-ttu-id="080cd-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="080cd-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="080cd-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="080cd-127">Implementations</span></span>

-   [<span data-ttu-id="080cd-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="080cd-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="080cd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="080cd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="080cd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="080cd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="080cd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="080cd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="080cd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="080cd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="080cd-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="080cd-133">Windows Server 2003</span></span>



| <span data-ttu-id="080cd-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="080cd-134">Entry</span></span> | <span data-ttu-id="080cd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="080cd-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080cd-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="080cd-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080cd-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="080cd-138">System-Only</span></span>            | <span data-ttu-id="080cd-139">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="080cd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="080cd-141">True</span><span class="sxs-lookup"><span data-stu-id="080cd-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="080cd-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="080cd-142">Is Indexed</span></span>             | <span data-ttu-id="080cd-143">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="080cd-144">In Global Catalog</span></span>      | <span data-ttu-id="080cd-145">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="080cd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="080cd-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="080cd-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="080cd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080cd-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080cd-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-150">Search-Flags</span></span>           | <span data-ttu-id="080cd-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080cd-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-152">System-Flags</span></span>           | <span data-ttu-id="080cd-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080cd-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="080cd-154">Classes used in</span></span>        | [<span data-ttu-id="080cd-155">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="080cd-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="080cd-156">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="080cd-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="080cd-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="080cd-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="080cd-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="080cd-158">Entry</span></span> | <span data-ttu-id="080cd-159">Valor</span><span class="sxs-lookup"><span data-stu-id="080cd-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080cd-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="080cd-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080cd-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="080cd-162">System-Only</span></span>            | <span data-ttu-id="080cd-163">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="080cd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="080cd-165">True</span><span class="sxs-lookup"><span data-stu-id="080cd-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="080cd-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="080cd-166">Is Indexed</span></span>             | <span data-ttu-id="080cd-167">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="080cd-168">In Global Catalog</span></span>      | <span data-ttu-id="080cd-169">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="080cd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="080cd-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="080cd-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="080cd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080cd-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080cd-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-174">Search-Flags</span></span>           | <span data-ttu-id="080cd-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080cd-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-176">System-Flags</span></span>           | <span data-ttu-id="080cd-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080cd-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="080cd-178">Classes used in</span></span>        | [<span data-ttu-id="080cd-179">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="080cd-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="080cd-180">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="080cd-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="080cd-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="080cd-181">Windows Server 2008</span></span>



| <span data-ttu-id="080cd-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="080cd-182">Entry</span></span> | <span data-ttu-id="080cd-183">Valor</span><span class="sxs-lookup"><span data-stu-id="080cd-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080cd-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="080cd-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080cd-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="080cd-186">System-Only</span></span>            | <span data-ttu-id="080cd-187">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="080cd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="080cd-189">True</span><span class="sxs-lookup"><span data-stu-id="080cd-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="080cd-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="080cd-190">Is Indexed</span></span>             | <span data-ttu-id="080cd-191">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="080cd-192">In Global Catalog</span></span>      | <span data-ttu-id="080cd-193">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="080cd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="080cd-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="080cd-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="080cd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080cd-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080cd-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-198">Search-Flags</span></span>           | <span data-ttu-id="080cd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080cd-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-200">System-Flags</span></span>           | <span data-ttu-id="080cd-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080cd-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="080cd-202">Classes used in</span></span>        | [<span data-ttu-id="080cd-203">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="080cd-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="080cd-204">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="080cd-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="080cd-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="080cd-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="080cd-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="080cd-206">Entry</span></span> | <span data-ttu-id="080cd-207">Valor</span><span class="sxs-lookup"><span data-stu-id="080cd-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080cd-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="080cd-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080cd-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="080cd-210">System-Only</span></span>            | <span data-ttu-id="080cd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="080cd-212">Is-Single-Valued</span></span>       | <span data-ttu-id="080cd-213">True</span><span class="sxs-lookup"><span data-stu-id="080cd-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="080cd-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="080cd-214">Is Indexed</span></span>             | <span data-ttu-id="080cd-215">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="080cd-216">In Global Catalog</span></span>      | <span data-ttu-id="080cd-217">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="080cd-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="080cd-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="080cd-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="080cd-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080cd-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080cd-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-222">Search-Flags</span></span>           | <span data-ttu-id="080cd-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080cd-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-224">System-Flags</span></span>           | <span data-ttu-id="080cd-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080cd-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="080cd-226">Classes used in</span></span>        | [<span data-ttu-id="080cd-227">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="080cd-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="080cd-228">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="080cd-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="080cd-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="080cd-229">Windows Server 2012</span></span>



| <span data-ttu-id="080cd-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="080cd-230">Entry</span></span> | <span data-ttu-id="080cd-231">Valor</span><span class="sxs-lookup"><span data-stu-id="080cd-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="080cd-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="080cd-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="080cd-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="080cd-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="080cd-234">System-Only</span></span>            | <span data-ttu-id="080cd-235">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="080cd-236">Is-Single-Valued</span></span>       | <span data-ttu-id="080cd-237">True</span><span class="sxs-lookup"><span data-stu-id="080cd-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="080cd-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="080cd-238">Is Indexed</span></span>             | <span data-ttu-id="080cd-239">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="080cd-240">In Global Catalog</span></span>      | <span data-ttu-id="080cd-241">Falso</span><span class="sxs-lookup"><span data-stu-id="080cd-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="080cd-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="080cd-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="080cd-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="080cd-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="080cd-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="080cd-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="080cd-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="080cd-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-246">Search-Flags</span></span>           | <span data-ttu-id="080cd-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="080cd-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="080cd-248">System-Flags</span></span>           | <span data-ttu-id="080cd-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="080cd-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="080cd-250">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="080cd-250">Classes used in</span></span>        | [<span data-ttu-id="080cd-251">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="080cd-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="080cd-252">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="080cd-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





