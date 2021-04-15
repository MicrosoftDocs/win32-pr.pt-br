---
title: atributo ms-TAPI-Conference-blob
description: Um BLOB binário de dados que descreve várias propriedades de uma conferência multicast TAPI. Seu formato e conteúdo são determinados pelo valor do atributo Protocol-Id no mesmo objeto. Normalmente, os dados nesse BLOB estão em conformidade com RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-TAPI-Conference-blob
- Esquema de AD do atributo msTAPI-ConferenceBlob
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753860"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="4b4be-107">atributo ms-TAPI-Conference-blob</span><span class="sxs-lookup"><span data-stu-id="4b4be-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="4b4be-108">Um BLOB binário de dados que descreve várias propriedades de uma conferência multicast TAPI.</span><span class="sxs-lookup"><span data-stu-id="4b4be-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="4b4be-109">Seu formato e conteúdo são determinados pelo valor do atributo Protocol-Id no mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="4b4be-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="4b4be-110">Normalmente, os dados nesse BLOB estão em conformidade com RFC2327.</span><span class="sxs-lookup"><span data-stu-id="4b4be-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="4b4be-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b4be-111">Entry</span></span> | <span data-ttu-id="4b4be-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4be-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4be-113">CN</span><span class="sxs-lookup"><span data-stu-id="4b4be-113">CN</span></span>                | <span data-ttu-id="4b4be-114">MS-TAPI-Conference-blob</span><span class="sxs-lookup"><span data-stu-id="4b4be-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="4b4be-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4b4be-115">Ldap-Display-Name</span></span> | <span data-ttu-id="4b4be-116">msTAPI-ConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="4b4be-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="4b4be-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4b4be-117">Size</span></span>              | <span data-ttu-id="4b4be-118">Pode ter comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="4b4be-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="4b4be-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4b4be-119">Update Privilege</span></span>  | <span data-ttu-id="4b4be-120">Nenhum privilégio especial é necessário.</span><span class="sxs-lookup"><span data-stu-id="4b4be-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="4b4be-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4b4be-121">Update Frequency</span></span>  | <span data-ttu-id="4b4be-122">Pode mudar a critério de um proprietário de conferência TAPI quando alguns dados sobre a conferência precisarem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="4b4be-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="4b4be-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b4be-123">Attribute-Id</span></span>      | <span data-ttu-id="4b4be-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="4b4be-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="4b4be-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4b4be-125">System-Id-Guid</span></span>    | <span data-ttu-id="4b4be-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="4b4be-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="4b4be-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4be-127">Syntax</span></span>            | [<span data-ttu-id="4b4be-128">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="4b4be-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="4b4be-129">Implementações</span><span class="sxs-lookup"><span data-stu-id="4b4be-129">Implementations</span></span>

-   [<span data-ttu-id="4b4be-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b4be-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b4be-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b4be-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b4be-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b4be-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b4be-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b4be-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b4be-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b4be-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4b4be-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b4be-135">Windows Server 2003</span></span>



| <span data-ttu-id="4b4be-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b4be-136">Entry</span></span> | <span data-ttu-id="4b4be-137">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4be-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4b4be-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="4b4be-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b4be-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b4be-140">System-Only</span></span>            | <span data-ttu-id="4b4be-141">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-141">False</span></span>                                                             |
| <span data-ttu-id="4b4be-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4b4be-142">Is-Single-Valued</span></span>       | <span data-ttu-id="4b4be-143">True</span><span class="sxs-lookup"><span data-stu-id="4b4be-143">True</span></span>                                                              |
| <span data-ttu-id="4b4be-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="4b4be-144">Is Indexed</span></span>             | <span data-ttu-id="4b4be-145">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-145">False</span></span>                                                             |
| <span data-ttu-id="4b4be-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b4be-146">In Global Catalog</span></span>      | <span data-ttu-id="4b4be-147">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-147">False</span></span>                                                             |
| <span data-ttu-id="4b4be-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b4be-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b4be-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4b4be-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4b4be-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b4be-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b4be-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-152">Search-Flags</span></span>           | <span data-ttu-id="4b4be-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b4be-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="4b4be-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-154">System-Flags</span></span>           | <span data-ttu-id="4b4be-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b4be-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="4b4be-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4b4be-156">Classes used in</span></span>        | [<span data-ttu-id="4b4be-157">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="4b4be-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b4be-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b4be-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b4be-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b4be-159">Entry</span></span> | <span data-ttu-id="4b4be-160">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4be-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4b4be-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="4b4be-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b4be-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b4be-163">System-Only</span></span>            | <span data-ttu-id="4b4be-164">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-164">False</span></span>                                                             |
| <span data-ttu-id="4b4be-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4b4be-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4b4be-166">True</span><span class="sxs-lookup"><span data-stu-id="4b4be-166">True</span></span>                                                              |
| <span data-ttu-id="4b4be-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="4b4be-167">Is Indexed</span></span>             | <span data-ttu-id="4b4be-168">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-168">False</span></span>                                                             |
| <span data-ttu-id="4b4be-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b4be-169">In Global Catalog</span></span>      | <span data-ttu-id="4b4be-170">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-170">False</span></span>                                                             |
| <span data-ttu-id="4b4be-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b4be-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b4be-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4b4be-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4b4be-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b4be-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b4be-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-175">Search-Flags</span></span>           | <span data-ttu-id="4b4be-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b4be-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="4b4be-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-177">System-Flags</span></span>           | <span data-ttu-id="4b4be-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b4be-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="4b4be-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4b4be-179">Classes used in</span></span>        | [<span data-ttu-id="4b4be-180">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="4b4be-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b4be-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b4be-181">Windows Server 2008</span></span>



| <span data-ttu-id="4b4be-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b4be-182">Entry</span></span> | <span data-ttu-id="4b4be-183">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4be-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4b4be-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="4b4be-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b4be-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b4be-186">System-Only</span></span>            | <span data-ttu-id="4b4be-187">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-187">False</span></span>                                                             |
| <span data-ttu-id="4b4be-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4b4be-188">Is-Single-Valued</span></span>       | <span data-ttu-id="4b4be-189">True</span><span class="sxs-lookup"><span data-stu-id="4b4be-189">True</span></span>                                                              |
| <span data-ttu-id="4b4be-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="4b4be-190">Is Indexed</span></span>             | <span data-ttu-id="4b4be-191">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-191">False</span></span>                                                             |
| <span data-ttu-id="4b4be-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b4be-192">In Global Catalog</span></span>      | <span data-ttu-id="4b4be-193">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-193">False</span></span>                                                             |
| <span data-ttu-id="4b4be-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b4be-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b4be-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4b4be-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4b4be-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b4be-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b4be-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-198">Search-Flags</span></span>           | <span data-ttu-id="4b4be-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b4be-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="4b4be-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-200">System-Flags</span></span>           | <span data-ttu-id="4b4be-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b4be-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="4b4be-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4b4be-202">Classes used in</span></span>        | [<span data-ttu-id="4b4be-203">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="4b4be-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b4be-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b4be-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b4be-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b4be-205">Entry</span></span> | <span data-ttu-id="4b4be-206">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4be-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4b4be-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="4b4be-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b4be-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b4be-209">System-Only</span></span>            | <span data-ttu-id="4b4be-210">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-210">False</span></span>                                                             |
| <span data-ttu-id="4b4be-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4b4be-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4b4be-212">True</span><span class="sxs-lookup"><span data-stu-id="4b4be-212">True</span></span>                                                              |
| <span data-ttu-id="4b4be-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="4b4be-213">Is Indexed</span></span>             | <span data-ttu-id="4b4be-214">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-214">False</span></span>                                                             |
| <span data-ttu-id="4b4be-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b4be-215">In Global Catalog</span></span>      | <span data-ttu-id="4b4be-216">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-216">False</span></span>                                                             |
| <span data-ttu-id="4b4be-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b4be-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b4be-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4b4be-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4b4be-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b4be-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b4be-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-221">Search-Flags</span></span>           | <span data-ttu-id="4b4be-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b4be-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="4b4be-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-223">System-Flags</span></span>           | <span data-ttu-id="4b4be-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b4be-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="4b4be-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4b4be-225">Classes used in</span></span>        | [<span data-ttu-id="4b4be-226">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="4b4be-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b4be-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b4be-227">Windows Server 2012</span></span>



| <span data-ttu-id="4b4be-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b4be-228">Entry</span></span> | <span data-ttu-id="4b4be-229">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4be-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4b4be-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="4b4be-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b4be-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4b4be-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b4be-232">System-Only</span></span>            | <span data-ttu-id="4b4be-233">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-233">False</span></span>                                                             |
| <span data-ttu-id="4b4be-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4b4be-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4b4be-235">True</span><span class="sxs-lookup"><span data-stu-id="4b4be-235">True</span></span>                                                              |
| <span data-ttu-id="4b4be-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="4b4be-236">Is Indexed</span></span>             | <span data-ttu-id="4b4be-237">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-237">False</span></span>                                                             |
| <span data-ttu-id="4b4be-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4b4be-238">In Global Catalog</span></span>      | <span data-ttu-id="4b4be-239">Falso</span><span class="sxs-lookup"><span data-stu-id="4b4be-239">False</span></span>                                                             |
| <span data-ttu-id="4b4be-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4b4be-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b4be-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4b4be-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4b4be-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b4be-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b4be-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4b4be-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-244">Search-Flags</span></span>           | <span data-ttu-id="4b4be-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b4be-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="4b4be-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b4be-246">System-Flags</span></span>           | <span data-ttu-id="4b4be-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b4be-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="4b4be-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4b4be-248">Classes used in</span></span>        | [<span data-ttu-id="4b4be-249">**MS-TAPI-RT-Conference**</span><span class="sxs-lookup"><span data-stu-id="4b4be-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





